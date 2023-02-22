---
title: 'Ajastetut ajot'
permalink: /dokumentaatio/ajastetutajot/
redirect_from:
  - /theme-setup/
toc: true
---

UNIX-crontabien rivin formaatti on minuutti tunti päivä kuukausi viikonpäivä, huomaa että minuutti ja tunti ovat siis "nurinpäin", eli rivin ensimmäinen arvo ilmaisee minuutit ja toinen tunnit.

Määrittelyt aikaväleille ovat mahdollisia. Esimerkiksi jos tunti-merkintänä on 7-22 ja minuuttimerkintänä */1 (yhden minuutin välein), ajetaan tehtävä klo 7.00-22.59.

## Uudelleenindeksointi

Indeksointi voidaan määritellä tapahtuvaksi yöllä poistamalla kommenttimerkki seuraavan crontab-rivin edestä. Indeksien varmuuskopiointi täytyy poistaa käytöstä uudelleenindeksoinnin ajaksi, jotta indeksointi ei keskeydy varmistuksen vuoksi.

```
# Uncomment rebuild_elastic_search.pl for complete ElacticSearch rebuild.
# Comment ksbackup --indices below when running this!!
# 46 23 * * *        $TRIGGER search_tools/rebuild_elasticsearch.pl -a -b -r -v -c 1000
```

## Lainaukseen ja varausten käsittelyyn liittyvät ajastetut tehtävät

```
#### Circulation & Holds ####
  01 00 * * *        $TRIGGER cronjobs/fines.pl -v -l -o /var/log/koha/fines
  10 00 * * *        $TRIGGER misc/expire_holds.sh EITILASTO KAUKOLAINA KOTIPALVEL
  15 00 * * *        $TRIGGER cronjobs/holds/auto_unsuspend_holds.pl
  20 00 * * *        $TRIGGER cronjobs/cart_to_shelf.pl --hours 1
  */1 07-22 * * *    $TRIGGER cronjobs/holds/build_holds_queue.pl
  */1 07-22 * * *    $TRIGGER cronjobs/holds/update-holds-to-pull.pl
```

Yllä olevat ajastukset ovat vakioita ja ne tapahtuvat kaikissa kimpoissa samaan aikaan.

* fines.pl - laskee lainassa olevasta aiheutuvat myöhästymismaksut
* expire_holds.sh - ajaa kaksi skriptiä:
  * cancel_expired_holds.pl, joka poistaa vanhentuneet varaukset ja lisää niistä aiheutuvat noutamattoman varauksen maksut
  * remove_hold_fees.pl, joka poistaa rivin perässä olevilta asiakastyypeiltä noutamattoman varauksen maksut
* auto_unsuspend_holds.pl - jatkaa keskeytettyjä varauksia, joiden keskeytyksen määräpäivä on saavutettu
* cart_to_shelf.pl - siirtää 'CART' (tänään palautetut) hyllypaikalla olevat niteet takaisin oikealle hyllpaikalleen, perässä oleva parametri kertoo kuinka kauan aikaa sitten palautetut niteet siirretään
* build_holds_queue.pl - muodostaa varausjonon tmp_holdsqueue -tauluun, tätä taulua käytetään ainakin varausjono-raportin näyttämiseen
* update-holds-to-pull.pl - muodostaa hyllyvarausraportin

## Asiakkaisiin ja muihin käyttäjiin liittyvät ajastetut tehtävät

```
#### Patrons ####
  01 00 * * *        $TRIGGER cronjobs/update_patrons_category.pl --confirm --too_old --from LAPSI      --to LAOMATOIMI
  01 00 * * *        $TRIGGER cronjobs/update_patrons_category.pl --confirm --too_old --from LAOMATOIMI --to HENKILO
  05 00 1 1 *        $TRIGGER cronjobs/turnofftheyearBlockBorrowersWithFines.pl -v -y $(($(date +\%Y)-1)) -c
  02 00 * * *        $TRIGGER cronjobs/drop_borrower_ss_blocks.pl -v -c
  */15 * * * *       $TRIGGER cronjobs/excess_login_attempts.pl
```

* update_patron_category.pl - muuttaa asiakastyyppejä, esimerkiksi lapsiasiakkaat aikuisiksi heidän saavuttaessaan asiakastyypin maksimi/minimi -ikärajat
  * Joissain Koha-Suomen kirjastoissa lapsiasiakkaan omatoimikäyttöoikeus voi vaikuttaa näihin ajoihin, jonka vuoksi rivejä voi olla crontabissa kaksi
* turnofftheyearBlockBorrowersWithFines.pl - asettaa käytöneston vuodenvaihteessa asiakkaille, joilla on maksuja
* drop_borrower_ss_blocks.pl - poistaa määräaikaiset käytönestot asiakkailta, joilla ne ovat vanhentuneet
* excess_login_attempts.pl - asettaa käytöneston asiakkaille, joilla on yli 50 epäonnistunutta kirjautumisyritystä
* Crontabin 'Patrons' osassa on myös käyttäjätunnusten käsittelyyn liittyviä ajoja, joita ei tietoturvasyistä ole kuvattu tässä dokumentissa

## Asiakasviestintä

```
#### Notices ####
  */15 09-19 * * *   $TRIGGER cronjobs/process_message_queue.pl
  00 20 * * *        $TRIGGER cronjobs/process_message_queue.pl
  40 08 * * *        $TRIGGER cronjobs/advance_notices.pl -c
  00 09 * * *        $TRIGGER cronjobs/overdue_notices.pl -letternumbers 12 -t -p -s
  10 09 * * *        $TRIGGER cronjobs/membership_expiry.pl -c -v
  50 20 * * *        $TRIGGER cronjobs/pate.pl --letters
```
* process_message_queue.pl - lähettää asiakkaille generoidut viestit (sms ja sähköposti)
  * ajetaan klo 9.15-19.45 + vielä kerran klo 20.00
* advance_notices.pl - muodostaa eräpäiväennakkoilmoitukset ja eräpäivämuistutukset viestijonoon
* overdue_notices.pl - muodostaa palautuskehotukset viestijonoon
* membership_expiry.pl - muodostaa kirjastokorttien vanhenemismuistutukset viestijonoon
* pate.pl - lähettää suomi.fi ja kirjeviestit, jos suomi.fi viestit on käytössä, crontabissa on erillinen rivi niitä varten
  * ajastus on tehty siten että kirjeviestit ehtivät mahdollisuuksien mukaan saman päivän käsittelyyn, jolloin ne ovat jakelussa niin pian kuin posti ehtii

## Laskutus

```
#### Sending Finvoices ####
  30 10 * * 3    $TRIGGER cronjobs/run_finvoice.pl /var/spool/koha/finvoice/ -p /etc/koha/finvoice-config.yaml -c LASKUOU -v --xsd /var/lib/koha/plugins/Koha/Plugin/Fi/KohaSuomi/OverdueTool/finvoice/Finvoice3.0.xsd --pretty
# 00 23 * * *    $TRIGGER cronjobs/run_finvoice.pl /var/spool/koha/finvoice/ -p /etc/koha/finvoice-config.yaml -c LASKURA -v --xsd /var/lib/koha/plugins/Koha/Plugin/Fi/KohaSuomi/OverdueTool/finvoice/Finvoice3.0.xsd --pretty
```

* muodostaa ja lähettää Finvoice-laskut laskutusryhmittäin (esimerkissä Oulun ja Raahen laskut)

## Hankinnat

```
#### Acquisition ####
  30 00 * * *        $TRIGGER cronjobs/purge_suggestions.pl -days 365
  */1 06-22 * * *    $TRIGGER cronjobs/runEditXImport.pl
  45 23 * * *        $TRIGGER cronjobs/notify_failed_editx.sh
  00 21 * * *        $TRIGGER cronjobs/requeue_failed_editx.sh
```
* purge_suggestions.pl - poistaa määriteltyä vanhemmat hankintaehdotukset
* runEditXImport.pl - käsittelee palvelimelle tulleet EDItX-sanomat
* notify_failed_editx.sh - lähettää sähköpostihuomautukset epäonnistuneista sanomien käsittelyistä
* requeue_failed_editx.sh - siirtää epäonnistuneet sanomat takaisin sanomajonoon uudelleenkäsittelyä varten

## Kuvailu

```
#### Catalog ####
  10 00 * * *        $TRIGGER cronjobs/merge_authorities.pl -b -v
  00 04 * * *        $TRIGGER cronjobs/update_totalissues.pl --incremental --use-stats
  25 01 * * *        cd /home/koha/marc21-fi-mangle && ./luo_virhelista.sh
# 15 00 1 * *        cd /home/koha/marc21-fi-mangle && ./get_fi_xmls.sh && ./update_frameworks_VASKI.sh
# 20 00 1 * *        /home/koha/Koha/misc/get_marc21_formatchecker_data_fi.sh
  0 1 * * *          $TRIGGER cronjobs/automatic_item_modification_by_age.pl -v -c
  */02 07-21 * * *   $TRIGGER cronjobs/run_broadcast_biblios.pl -a -i OUTI -c 5 --identifier --start_time 9 --block_component_parts -v
# 30 21 15 06 *      $TRIGGER batchRebuildBiblioTables.pl -c
```

* merge_authorities.pl - käsittelee auktoriteettitietueiden yhdistämispyynnöt
* update_totalissues.pl - laskee kuvailutietuekohtaiset kokonaislainamäärät
* luo_virhelista.sh - luo MARC-virhelistat
* get_fi_xmls.sh && update_frameworks_VASKI.sh - noutaa MARC-formaatin muutokset kansalliskirjaston palvelimilta sekä päivittää Kohan kuvailupohjat, tämä ajastettu ajo ei ole normaalisti käytössä, mutta se voidaan ottaa käyttöön jos formaattiin on tehty muutoksia
* get_marc21_formatchecker_data_fi.sh - noutaa koneluettavan MARC-formaatin kansalliskirjaston palvelimelta nalkutinta varten, tämä ajastettu ajo ei ole normaalisti käytössä, mutta se voidaan ottaa käyttöön jos koneluettavassa MARC-formaatissa on muutoksia
* automatic_item_modification_by_age.pl - muokkaa niteen ominaisuuksia niteen iän mukaan määriteltyjen sääntöjen mukaisesti (Työkalut -> Niteiden muokkaus iän mukaan)
* run_broadcast_biblios.pl - aktivoi paikalliskannan tietueet valutusta varten tai jotain
* batchRebuildBiblioTables.pl - päivittää biblio ja biblioitems-taulut jos esimerkiksi kuvailutietueita on muutettu suorina tietokanta-ajoina tai Koha-MARC mäppäyksiä on muutettu, tämä ajastettu ajo ei ole normaalisti käynnissä, mutta se voidaan tarvittaessa ottaa käyttöön

## Ylläpito ja automaattiset siivoukset

```
#### System administration ####
  45 02 1 1 *        $TRIGGER cleanup-scripts/cleanup_message_queue.pl -v -mail 3
  10 02 15 1 *       $TRIGGER cleanup-scripts/archive_action_logs.pl -v --years 1 --cleanup
  10 02 15 1 *       $TRIGGER cleanup-scripts/archive_statistics.pl -v --years 1 --cleanup
  10 01 1 * *        $TRIGGER cleanup-scripts/cleanup_edifact_messages.pl -v --months 12
  10 01 1 * *        $TRIGGER cleanup-scripts/cleanup_background_jobs.pl -v --months 1
  10 11 1 * *        $TRIGGER cleanup-scripts/cleanup_branchtransfers.pl --months 24 -v
# 03 02 15 1 *       $TRIGGER cleanup-scripts/truncate_search_history.pl -v -t
  05 02 * * *        $TRIGGER cleanup-scripts/cleanup_search_history.pl -v --days 30
  05 02 * * *        $TRIGGER cleanup-scripts/truncate_sessions.pl -v -t
  05 02 * * *        $TRIGGER cleanup-scripts/truncate_zebraqueue.pl -v -t
  30 09 * * *        ko-ssh-hostkey-check --force | mail -E -r admin@koha-suomi.fi -s "WARNING! SSH connections on $(cat /etc/ks-lxc-role) fail!" notifications@koha-suomi.fi
```

* cleanup_message_queue.pl - siivoaa viestijonon (asiakasviestit)
* archive_action_logs.pl - arkistoi vanhat action_log merkinnät vuositauluihin
* archive_statistics.pl - arkistoi vanhat statistics merkinnät vuositauluihin
* cleanup_edifact_messages.pl - poistaa vanhat EDI-sanomat EDIFACT-sivulta (sanomat säilyvät silti palvelimella)
* cleanup_background_jobs.pl - siivoaa taustatyölistalta onnistuneesti suoritetut taustatyöt (esimerkissä kuukautta vanhemmat merkinnät poistetaan)

## Tilastot

```
#### statistics ####
  10 01 * * *        $TRIGGER cronjobs/update_biblio_data_elements.pl --verbose 2
  10 02 1 1 *        $TRIGGER cronjobs/generate_okm_annual_statistics.pl --timeperiod 'lastyear' -r -v
  10 03 1 1 *        $TRIGGER cronjobs/generate_okm_annual_statistics.pl --timeperiod 'lastyear' --individual 'ALL' -r -v
  10 04 1 * *        $TRIGGER cronjobs/generate_okm_annual_statistics.pl --timeperiod 'lastmonth' --individual 'ALL' -r -v
# 20 01 * * *        cd /home/koha/Koha/misc/statistics && perl sanasto.fi.pl -o outi
  41 22 23 * *       $TRIGGER cronjobs/share_usage_with_koha_community.pl -v
```

* update_biblio_data_elements.pl - päivittää OKM-tilastointiin käytettävän biblio_data_elements -taulun kuvailutietueiden ja niteiden pohjalta
* generate_okm_annual_statistics.pl - luo OKM-tilastot, nämä luodaan vuositasolla OKM-tilastointiryhmäkohtaisesti sekä vuositasolla+kuukausitasolla kirjastoyksikkökohtaisesti
* sanasto.fi.pl - luo Sanasto-raportin
* share_usage_with_koha_community.pl - lähettää tilastotietoa Koha-yhteisön HEA-palveluun (kuvailutietueiden, niteiden, lainojen, kirjastoyksiköiden, asiakkaiden ym. kokonaismäärät sekä tietoja mm järjestelmäasetuksista)

## Varmistukset

```
#### Dumps and backups ####
# 20 7-22 * * *      $TRIGGER cronjobs/dumpdb --variable-data
  00 04 * * *        $TRIGGER cronjobs/dumpdb
  45 03   * * *      sudo /usr/local/bin/ksbackup --indices >> /var/log/koha/ksbackup.log 2>&1
  00 04   * * *      sudo /usr/local/bin/ksbackup --dirs    >> /var/log/koha/ksbackup.log 2>&1
```

* dumpdb - varmuuskopioi Koha-tietokannan konesalioperaattorin varmistusjärjestelmään (--variable-data vivulla voidaan kopioida esimerkiksi tunneittain paljon muuttuvat taulut kuten lainat ja varaukset, mutta tämä ei ole tällä hetkellä käytössä)
* ksbackup - varmuuskopioi Koha-kohtaiset asetukset, sekä indeksit ja muun palvelimella olevan tärkeän datan konesalioperaattorin varmistusjärjestelmään

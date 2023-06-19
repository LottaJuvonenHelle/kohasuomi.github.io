---
layout: single
permalink: /paakayttajat2023
header:
  overlay_color: '#5e616c'
  overlay_image: /assets/images/cropped-pexels-photo-113850.jpeg
toc: true
title: 'Koha-Suomen pääkäyttäjäryhmän muistiot 2023'
---

Koha-Suomen pääkäyttäjäryhmä kokoontuu kerran viikossa. Ylimmäisenä on aina uusin muistio.

## Viikko 25 muistio
Aika: 20.6.2023 klo 9.15
Läsnä:

**Yhteiset asiat:**

Etelästä pohjoiseen

## Viikko 24 muistio
Aika: 13.6.2023 klo 9.15 <br />
Läsnä: Leena Kinnunen (Lappi), Päivi Knuutinen (Vaara), Hanna Ikonen (Lumme), Piia Semenoff ja Pirkko-Liisa Lauhikari (OUTI), Kati Sillgren (Helle), Anni Rajala (Vaski)

**Yhteiset asiat:**
* Kirjataan muistiin: automaattien toimittajat Lyngsoe, Bibliotheca ja Mikroväylä ovat ilmoittaneet, että automaateissa voi ottaa käyttöön myös pidempiä PIN-koodeja kuin nyt on vain neljä numeroa.
  * Selvitetään onko pitempää PIN-koodia mahdollista käyttää kaikissa palveluissa, joihin niillä kirjaudutaan.
  * Vaski on lupautunut testaamaan.
* Varausjono-raportti / Koha-Suomen hyllyvarausraportti -> uudelleentarkasteltavaksi kumman ylläpitäminen olisi järkevintä?
Keskusteltu tiketissä [#578](https://github.com/KohaSuomi/Koha/issues/578). Kannattaisiko pääkäyttäjäryhmä asian selvittelyä, voidaanko edentää ehdotus uudelleentarkastelusta asiantuntijaryhmään? (Anni / Vaski)
  * Vaski ottaa asian uudestaan esille pääkäyttäjäpalaveriin kesälomien jälkeen. Keskustellaan silloin laajemmalla osanottajamäärällä miten näiden varaus-raporttien osalta edetään.

Pohjoisesta etelään

**Lappi**
* Tietue aiheuttaa Kohaan 500-virheen, syynä puutteellinen 942-kenttä. Vastaavia tietueita on vajaa 10, kehittäjä korjaa. 
* Kuvailun hakukenttä tyhjene, jos hakulauseella ei löydy mitään. Toimii siis toisin kuin tiedonhakukenttä. Olisiko joku järjestelmäasetus vai ominaisuus?
* Käyttäjätunnuksia tehty tiheään kesätyöntekijöille. 
* Muuten rauhallista. 

**Vaara**
* Lauantaina oli tapahtunut pari ihmeteltävää asiaa, joista tein nyt tiketit:
* https://github.com/KohaSuomi/Koha/issues/645 Varaustunnus vaihtui anonymisoiduksi vanhentuneiden varausten listalla, kun asiakas oli poistanut lainahistoriansa
* https://github.com/KohaSuomi/Koha/issues/646 Varauksen noutoaika pidentyi viikolla, kun tulostettiin uusi odottavan varauksen kuitti. Asiakkaalle ei lähtenyt viestiä uudesta noutoajasta
* Edge-selain kysyy varmenteen kahteen kertaan, toinen kerta Vaaran testikannalle. Ilmeisesti vika Meitan asetuksissa, teen sinne palvelupyynnön korjata asia.
* Muuten normaalia ylläpitoa.

**Lumme**
* Virhe 500 toistuu säännöllisen epäsäännöllisesti palautuksissa. Asiaa selvitellään edelleen. 
* Automaateilla otettiin käyttöön mahdollisuus, että asiakas saa lainattua niillä hyllyvarauksen, jota ei ole vielä palautettu Kohassa tai automaatilla.
* Muuten normaalia ylläpitoa.

**OUTI**
* Finvoice-laskujen ääkkösongelma saatu oletettavasti kuntoon.
  * Viime viikon laskutusajoissa oli muita ongelmia (Raahen laskutusaineistoa ei saatu ajettua ja Oulun laskutusaineisto oli ilmeisesti Monetralla siirretty väärälle laskutuspohjalle), joten korjauksen onnistuminen varmistuu tällä viikolla.
* Pieni erä Raahen Finvoice-laskuja saatu lähtemään, mutta laskut eivät ainakaan eilen vielä näkyneet Raahen Monetralla.
  * Palaverin jälkeen saimme tiedon, että laskut ovat siirtyneet nyt myös Monetralle.
* Väärälle asiakkaalle mennyt s-postia, kun Finna-tilin sähköpostikenttä ei päivity, jos sähköpostiosoite muutetaan Kohassa. Laitettu taas palautetta Finna-tukeen.
* Asiakkaalta tullut palautetta, että verkkokirjastossa kun asiakas siirtyy Lainat-sivulta Varaukset-sivulle, sivusto pyytää kirjautumaan uudelleen.
  * Ongelma saatiin toistettua, kun odotettiin Finnan kirjautumisajan umpeutumiseen asti. Ei ole saatu vastausta asiakkaalta, että johtuuko virhetilanne timeoutista.
* Takaajatieto vielä linkitettynä, vaikka asiakas on jo täysi-ikäinen. Tiketti: #641
  * Tiketissä mainittu raportti 167 Takajalalliset asiakkaat voi olla nopea ja helppo korjata toimivaksi. Sen avulla voisimme tarkistaa onko meillä enemmänkin takaajallisia henkilöasiakkaita?
* Kohan ohje suomeksi -ohjetta päivitetty.

**Vaski**
* Yksi työntekijä havainnut tapauksen, jossa asiakastietojen tallentaminen onnistui ilman osoitetietoja. Työntekijä muisteli, että kentät olisivat lomakkeelta puuttuneet kokonaan, mutta ei ollut asiasta täysin varma. Joka tapauksessa osoitetiedot olivat tyhjät, kun asiakasta tallentamisen jälkeen tarkasteli. Raporttihaulla (address = '') löytyi toinen vastaava tapaus, asiakastietue tallennettu 2.6.2023. Ei keksitty selitystä, mutta raportoidaan tämä vielä tiketiksi.
* Palautetta tullut siitä, ettei Koha-Suomen sivuilla haku löydä ohjeita. Todettiin, että haku on Githubin, joka ei ole erityisen hyvä.


## Viikko 23 muistio
Aika: 6.6.2023 klo 9.15 <br />
Läsnä: Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Kati Sillgren (Helle), Piia Semenoff ja Pirkko-Liisa Lauhikari (OUTI), Reetta Pihlaja (Siilinjärvi), Tuomas Kunttu (Kyyti), Hanna Ikonen (Lumme), Anni Rajala (Vaski), Leena Kinnunen (Lappi)

Etelästä pohjoiseen

**Vaara**
* normaalia ylläpitoa 
* ihmettelimme jälleen eilen sitä, että lainojen ja varausten määrä ei noudata laina- ja maksusäännöissä tehtyjä asetuksia. Teen tiketin, jotta kehittäjät voisivat jossain vaiheessa tutkia, eikö tälle todellakaan voi mitään. Ongelma on ollut olemassa jo vuosia.

**Lappi**
* Normaalia ylläpitoa
* Asiakkaan syntymäaika oli osunut kesäaikaan siirtymisen päivämäärälle, jonka vuoksi asiakkaan viivakoodi antoi virheen 500. Korjattu vaihtamalla syntymäpäivä. Emmi hoitaa selvitystä eteenpäin, tiketti #620
* Saarenkylän kirjasto remontissa 22.6. - 30.7. Saarenkylän kirjaston aineistolle ajetaan not_loan-tila. Muuten ei aiheuta suuria muutoksia, sillä kiinnioloajan kirjastoauto leikkii olevansa Saarenkylän kirjasto ko. kirjaston pihalla

**Helle**
* Asiakastiedon muokkauksen Käyttökieli-asiakasmääre on nyt Asiakas identiteetti -osiossa.
* Asiakastiedon muokkauksen Muut määreet -osio piilotettu.

**OUTI**
* OUTIn Finvoice-laskuissa puuttuvat ääkköset laskutettavan teoksen nimestä ja tekijältä. Tiedot ovat ”ArticleName”-kentässä. Asiakkaan Ilmoitukset-sivulla näkyvässä laskussa ääkköset näkyvät oikein, mutta kun laskutiedot siirtyvät kuntien laskutusohjelmiin, josta laskut lopullisesti tulostetaan, ääkköset ovat hävinneet ko. kentän tiedoilta. Ongelmaan ehkä löydetty ratkaisu. Piia tehnyt uudet testilaskut tänään, joista pääsemme tarkistamaan asian. Tiketti: https://github.com/KohaSuomi/Koha/issues/621
* OUTIssa deleted-tauluissa biblioitemnumberin ja biblionumberin epäsynkkaa. Ei onnistu tietueen tai/ja niteen poistot, tulee virhe 500. Ongelmasta tiketeissä: https://github.com/KohaSuomi/Koha/issues/604 ja https://github.com/KohaSuomi/Koha/issues/606.
* Asiakkaalta Matkapuhelin-kentästä ja SMS-kentästä ovat puhelin numerot kadonneet. Ruksi noutoilmoituksen lähettämisestä testiviestinä on asiakkaalla päällä.  Ei näy, että hänen tietojaan olisi kukaan muokannut. OUTIssa on tullut muutama tapaus esille ja Kyytissä yksi. Ongelmasta tiketissä: https://github.com/KohaSuomi/Koha/issues/607.
* Sähköpostina lähetettävien ilmoitusten lähettäjäosoite muuttunut versopäivityksessä. Nyt lähettäjänä on taas noutokirjaston sähköpostiosoite, kun se pitäisi olla noreply@koha-suomi.fi. Tiketti: https://github.com/KohaSuomi/Koha/issues/616
* Asiakas oli ilmoittanut, että hän oli saanut sähköpostiin ilmoituksen, että kirjastokorttisi PIN-koodi vaihdettiin. Asiakas oli kertonut, ettei hän ole sitä tehnyt. Asiakkaan muutoslokilla ei näkynyt tietoa, että PIN-koodi olisi vaihdettu asiakkaan tai virkailijan toimesta. Asiakkaan Ilmoitukset-sivulla ei ollut myöskään ko. ilmoitusta. Asiakkaan huollettavalle, jolla sama s-postiosoite kuin huoltajalla, ei ole PIN-koodia vaihdettu. Tietokannasta ei löydy muita asiakkaita, joilla olisi sama s-postiosoite kuin tällä henkilöllä. Asiakkaalta pyydetty s-posti vielä nähtäväksi, jotta voimme varmistaa, onko posti lähetetty OUTIsta vai mahdollisesti jostain toisesta Koha-Suomen kimpan kirjastosta, jossa olisi asiakkaan kaima ja gmaili olisi jättänyt huomiotta osoitteessa olleen mahdollisen pisteen. *Kokouksen ulkopuolinen tieto: Asiakkaalta saatu kopio s-postiviestistä. Viesti oli tullut OUTIsta." Tehty tiketti: https://github.com/KohaSuomi/Koha/issues/629*

**Siilinjärvi**
* Ei mainittavaa Kohassa
* Siilin kuvailija kävi opintomatkalla Vaarassa, kiitos opastuksesta!

**Kyyti**
* Uuden asiakkaan tervetuloviesti laitettu päälle eilen.
* Tuomas jää lomalle tämän viikon jälkeen ja palaa elokuussa. Kotkan Roosa Väisänen paikalla suuren osan kesää.

**Lumme**
* Normaalia ylläpitoa.
* Lumme-Finna temppuili viime viikon loppupuolella, ongelma saatiin korjattua kehittäjien puolella. Tarkkaa syytä sivujen ulkonäköasetusten katoamiselle ei saatu.
* Lumpeissa oli käytössä asetus, jolla lainoja sai uusittua, vaikka niihin oli varaus, jos vapaana oli saatavana olevia niteitä. Asetus jouduttiin ottamaan pois käytöstä, sillä se tuotti ongelmia lehtien varauksissa. Myös mahdolliset asiakkaiden kokemat ongelmat omien Finna-tietojen näkemisessä saattoivat johtua tästä asetuksesta. Tilannetta seuraillaan.

**Vaski**
* Finnassa otettu käyttöön kuljetustilaisen varauksen peruminen.
* Kohassa otettu käyttöön asetus AllowRenewalIfOtherItemsAvailable, joka sallii varatun teoksen lainan uusimisen silloin kun teoksella on varaukset täyttäviä niteitä vähintään niin paljon kuin varauksia. Lumpeissa asetuksesta oli luovuttu, koska asetus ei osannut huomioida nidevarauksia ja näin näyttää olevan edelleen (oli unohtunut Vaskilta testata). Yhteisöstä löytyi tiketti aiheesta ja sen pohjalta Githubissa nyt [tiketti 630](https://github.com/KohaSuomi/Koha/issues/630) jossa toiveena saada yhteisön korjaus käyttöön.
* Hitautta havaittu asiakashaussa, lisäksi raporteilla tullut proxy erroria ja Finnassa epäonnistunut lehtitietueiden saatavuustietojen haku. Asiakashaun hitautta havaittu muuallakin (muttei kaikkialla). Vaski tekee havainnoistaan tiketin.


## Viikko 22 muistio

Aika: 30.5.2023 klo 9.15 <br />
Läsnä: Anneli Österman ja Lari Strand (Koha-Suomi), Kati Sillgren (Helle), Päivi Knuutinen ja Irina Halminen (Vaara), Leena Kinnunen ja Pia Kusmin (Lappi), Reetta Pihlaja (Siilinjärvi), Susanna Sandell (Vaski), Piia Semenoff, Pirkko-Liisa Lauhikari, Veli-Pekka Marjoniemi (OUTI), Hanna Ikonen (Lumme)

**Yhteiset**
* Vaskin asiakasvarmenne vanhenee jo elokuussa
  * jotta päästään kaikissa kimpoissa samaan uusimistahtiin, uusi varmenne tulee kaikille jakoon ma 24.7.2023.
  * muilla kimpoilla uusi tulee siis jo aiemmin käyttöön ja vanha on käytettävissä pidempään kuin Vaskissa.
  * Pääkäyttäjät: vaihto mielummin jo toukokuussa, koska kesä-elokuu loma-aikaa kaikkialla
* [Kaksivaiheisen kirjautumisen käyttöönotto](https://koha-community.org/manual/22.11/en/html/patrons.html#two-factor-authentication-in-the-staff-interface)
* Show analytics/Näytä osakohteet -linkin piilotus?
  * Päätös: Piilotetaan linkki ja otsikko css:llä. Anneli tekee.
* [Viikon 22 päivitys](https://github.com/KohaSuomi/Koha/discussions/598)

Pohjoisesta etelään

**Vaara**
* Ceepos-kassan toiminnallisuutta kaivataan takaisin Joensuun pääkirjastossa eli maksujen kuittausta automaattisesti.
* asiakkaan varausten näkymisen ja Finnan kautta varausten teon ongelma johti siihen, että havaittiin alle 40 nidettä, joissa 952w-kenttä oli väärä eli 0000-00-00. Syynä tähän todennäköisimmin käyttäjän virhe eli kopioitu 952d-kentästä päiväys, joka on eri muodossa kuin kentässä w ja johtaa tallennuksessa päiväyksen nollautumiseen. Vaikka asiasta on tiedotettu, kaikki eivät muista, että päiväys tallentuu automaattisesti kun nidetieto tallennetaan. Tämän vuoksi piilotettiin w-kenttä näkyvistä eri kuvailupohjissa. Virheelliset päiväykset korjattu käsin.
* Enon kirjasto menee muutaman viikon sulkuun kesällä remonttien (ulkoa ja sisältä), sen aiheuttamista muutoksista tehty tiketti.

**Lappi**
* Asiakashaku aiheuttaa sekaannusta, kun hakukentissä on erilaiset hakukriteerit oletuksena. #556
* Tulevat ja loppuvat remonttit työllistävät taas kesänaikana.
* Intranetuserjs:ssä oli väärä attribuuttiarvo sotusiilon rimpsussa, Anneli korjasi. Sotut/avaimet vielä korjaamatta. 
* Normaalia ylläpitoa ja samoja pikkukorjauksia, kun muillakin kimpoilla.

**Siilinjärvi**
* Kohassa ei suurempaa mainittavaa, muutoin verkkomaksun käyttöönotto ja henkilökuntatilanne ajankohtaisia
* Testataan tiketin #476 css:t

**Vaski**
* Broomworksin Puppe saapumisvalvontatyökalua ollaan hankkimassa.
* Selvityksen alla otetaanko Hypernovan Koha SaaS-palveluna Oppimateriaalikeskukselle. Hypernova tarjoaa Kohan yhteisöversiota.
* Vaskissa Pääkäyttäjän vakityö tarjolla.
* Finnassa oli vanhoilla Apple-laitteilla ongelma, jonka Ere ilmeisesti sai ratkaistua.

**OUTI**
* Asiakkaille on tullut vielä miinusmerkkisiä maksuja, koska he pystyvät maksamaan verkkomaksupalvelussa saman maksun kahteen kertaan. Maalis-toukokuussa tuplamaksuja viidellä asiakkaalla.  

**Lumme**
* Asiakashaku aiheuttaa Lumpeissakin pientä sekaannusta. 
* Lumpeissa oli myös väärä attribuuttiarvo sotusiilon rimpsussa, Anneli korjasi.
* Normaalia pikkukorjauksia niin kuin muuallakin.


## Viikko 21 muistio

Aika: 23.5.2023 klo 9.15 <br />
Läsnä: Anneli Österman ja Kodo Korkalo (Koha-Suomi), Pia Kusmin (Lappi), Päivi Knuutinen ja Auli Rantasalo (Vaara), Kati Sillgren (Helle), Piia Semenoff, Pirkko-Liisa Lauhikari ja Veli-Pekka Marjoniemi (OUTI), Reetta Pihlaja (Siilinjärvi), Tuomas Kunttu (Kyyti), Anni Rajala (Vaski), Hanna Ikonen ja Katja Valjakka (Lumme)

**Yhteiset**
* Miten menee versionvaihdon jälkeen?
  * Opittavaa versionvaihdon prosesseista yms?
    * kalenteri suljetuksi jo ma, koska asiakkaat valittivat, että olisi ollut vielä pari tuntia aikaa uusia lainoja.
    * omien toimintojen arviointi, onko kaikelle edelleen tarvetta?
    * Finna kertoi vain, että "väärä käyttäjätunnus tai salasana", mikä oli hämmentänyt asiakkaita. Yleensä kertonut, että taustajärjestelmään ei saa yhteyttä.
    * tuotannossa tuli esille virheitä, joita ei ollut testeissä ilmaantunut tai huomattu -> kiinniolo jatkossa puoltoista päivää?
    * redusoituun kantaan isompi setti tietueita, asiakkaita, lehtitilauksia. Osakohteita enemmän. Enemmän erilaisissa nidetiloissa olevia niteitä. Asiakastiedot: asiakkailta puuttui huollettavia ja varauksia -> helpompi, jos asiakkaan kaikki huollettavat, varaukset ja lainat otettaisiin mukaan.
* Kaksvaiheinen kirjautuminen käyttöön superlibrarian-tunnuksille, jos käytössä on työälyluuri.
  *  TwoFactorAuthentication -järjestelmäasetukseen _Salli_
* Palataan takaisin normaaliin tikettien seurantaan ja päivitystahtiin.
  * Uudet tiketit Koha-repositorioon. (Muistakaa tehdä tiketit, ei töitä sähköpostin tai Matrixin kautta, ohi tiketöinnin)
  * Päivitykset kerran viikossa tiistaisin.
  * Muistakaa sulkea tekemänne tiketit, kun ne ovat valmiit/ratkaisu ehdotettu.
* [Tiketti 117](https://github.com/KohaSuomi/Koha-22x/issues/117) - hakutuloslistan piilotus aiheuttanut palautetta. Haku toimii vain kirjastokortilla tai asiakkaan koko nimellä (kaikki etunimet ja sukunimi). Piilotus tehty, jotta ei voi hakea esille kaikkia tietokannan asiakastietoja ja vältetään turhia asiakastietojen katselua.
  * Päätös: Viedään asia asiantuntijaryhmän päätettäväksi seuraavalla ehdotuksella: Poistetaan hakutulostaulukon piilotus ja piilotetaan taulukosta syntymäaika, osoite ja puhelinnumero -sarakkeet.
  * Sarakeasetukset eivät toimi, [tiketti 571](https://github.com/KohaSuomi/Koha/issues/571) 
* [Kohan ohje suomeksi -wikin päivityksen seurantatiketti](https://github.com/KohaSuomi/Koha/issues/549)
  * Sovittu, että kuvaa ei tarvitse vaihtaa, jos sisältää tiedot olennaisilta osin. Vaihdettava kuitenkin, jos kuva ei vastaa nykyistä ohjeistusta.
  * Jos kuvan vaihtaa, pääsee helpoimmalla, kun nimeää uuden kuvan samalla nimellä kuin entinen oli ja vie sen sitten githubiin. Vanha korvataan uudella.
* kehitysehdotukset [#555](https://github.com/KohaSuomi/Koha/issues/555) ja [#556](https://github.com/KohaSuomi/Koha/issues/556)
* [Vanhentuneet noutamattomat varaukset](https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/Valmiita_SQL-raportteja#Vanhentuneet-noutamattomat-varaukset) -raportti päivitetty käyttämään HOLDID-asiakasmäärettä.
* Laitetaanko total issues -cronit pois päältä? Aiheuttaa nyt [ylimääräisiä valutuksia](https://github.com/KohaSuomi/Koha-22x/issues/190). [Redmine tiketti 1849](https://tiketti.koha-suomi.fi/issues/1849) liittyy myös aiheeseen.
  * kokeillaan outissa, auttaisiko toistaiseksi pelkkä 942$0-kentän kytkennän katkaiseminen biblioitems-tauluun?
* [Tiistain päivityksen tiedote](https://github.com/KohaSuomi/Koha/discussions/566)
* [Tiketti 560](https://github.com/KohaSuomi/Koha/issues/560) - MARC-virheraporttien linkit Raporttien etusivulle
* Lomien päivitys [yhteystiedot-wikiin](https://github.com/KohaSuomi/Koha/wiki/Koha-yhteystiedot)

**Vaara**
* Vaarassa kaivataan takaisin nappulaa kuljetuksen peruuttamiseen palautustilanteessa. Koitetaan säätää kohdilleen.

**Kyyti**
* Kotkassa ja Iitissä ollut ongelmia kellutuksessa: niteitä menee tarpeettomasti kuljetustilaan. Kotka selvittää asiaa.

**Vaski**
* Päivityksen jälkeen tullut odotettua vähemmän viestejä henkilökunnalta, eniten ongelmia on aiheuttanut saapumiskäsittelyn epäonnistuminen josta tehtynä tiketti [#562](https://github.com/KohaSuomi/Koha/issues/562)

## Viikko 20 muistio

Aika: 16.5.2023 klo 9.15 <br />
Läsnä: Anneli Österman ja Kodo Korkalo (Koha-Suomi)

* Käytiin läpi, mitä pitää tehdä tuotannossa ennen kuin kirjastot voidaan avata sekä erilaisia versionvaihdon ongelmia.


## Viikko 19 muistio

Aika: 9.5.2023 klo 9.15 <br />
Läsnä: Päivi Knuutinen ja Irina Halminen (Vaara), Leena Kinnunen (Lappi), Tuomas Kunttu (Kyyti), Veli-Pekka Marjoniemi ja Pirkko-Liisa Lauhikari (Outi), Reetta Pihlaja (Siilinjärvi), Anneli Österman ja Lari Strand (Koha-Suomi), Kati Sillgren (Helle), Hanna Ikonen ja Katja Valjakka (Lumme)

**Yhteiset**
* Viikon 20 eli 16.5. eli versionvaihtopäivän pääkäyttäjäpalsu pidetään klo 10.15.
  * tarkistetaan yhdessä, että tarpeelliset muutokset ja toimet on tehty tai tulee tehdyksi.
* Testejä tai testaustuloksia kaivataan vielä ainakin näihin:
  * [SIP muutos - ksdev/ks-0043-KD-2608 #15](https://github.com/KohaSuomi/Koha-22x/issues/15)
  * [koha-plugin-add-marc-field-001 (KPM001) #85](https://github.com/KohaSuomi/Koha-22x/issues/85)
  * [koha-plugin-delete-biblio-components (KPDELC) #94](https://github.com/KohaSuomi/Koha-22x/issues/94)
* Keskiviikkona 10.5.2023 testi-kantojen päivitys versioon 22.11.
  * harjoitellaan varsinaista ensi viikon päivitystä.
  * testi-kannat pois käytöstä päivityksen ajan.

Etelästä pohjoiseen.

**Vaara**
* Kuvailun käyttöohjetta päivitetty uuteen versioon, vielä on osittain kesken. Viimeistely sitten versionvaihdon jälkeen.
* Toveri-plugin toimii Hypernovan mukaan uudessa versiossa, toivottavasti myös käytännössä versionvaihdon jälkeen.
* Virheilmoitus EDItX-tilaussanomissa, joka johtuu Elasticsearch-virheestä. Näiden käsittelyyn pitäisi saada parempi käytäntö, jottei jälkikäteen korjattavia tuplatilauksia syntyisi.

**Lappi**
* Tullut jonkinverran EditX-virheitä: virheellinen sanoma tai puuttunut title. Korjattu/korjaantuneet. 
* Nextiä testattu ja lisätty Githubin mukaan toimintoja ja säätöjä

**Kyyti**
* Virkailijoiden kirjastokorttinumero- ja käyttäjätunnuskenttiä on yhdenmukaistettu
* Samalla perustettu uusia asiakastyyppi, johon menevät vinkkaus- ym. työkortit. Sen myötä laina- ja maksusääntöjä päivitetty.

**OUTI**
* OUTIssa testattu verkkomaksuja Finna-nextillä niin, että siellä oli tuotantopalvelimen asetukset. Maksuprosessissa ei ilmennyt ongelmia. 
* Testattu Emmin kanssa Ceepos-maksuja nextin kanssa. Maksujen lähetys nextiltä Ceeposiin toimii, mutta maksetun maksun kuittaus takaisin Ceeposista Kohaan ei vielä toimi.
* OUTIn verkkomaksupalvelu ei toiminut ma 8.5. n. klo 11-15. CPU oli päivittänyt Oulun kaupungin verkkomaksusivustolle uuden sertifikaatin, mutta sertifikaattiin liittyvä yksi tiedosto oli valittu väärin, joka aiheutti ongelman.

**Siilinjärvi**
* Meiltä oli jäänyt testaamatta meille tärkeä Tulosta ilmoituksia #93 eli testataan seuraavaksi vielä se.

**Lumme**
* Nextin testailua ja lisätty GitHubin mukaan toimintoja.


## Viikko 18 muistio

Aika: 2.5.2023 klo 9.15 <br />
Läsnä: Anneli Österman ja Kodo Korkalo (Koha-Suomi), Susanna Sandell (Vaski), Päivi Knuutinen ja Auli Rantasalo (Vaara), Katja Valjakka ja Hanna Ikonen (Lumme), Reetta Pihlaja (Siilinjärvi), Piia Semenoff ja Veli-Pekka Marjoniemi (OUTI), Kati Sillgren (Helle)

**Yhteiset**
* [Z39.50-haku tiputtaa 001-kentästä BTJ:n kontrollinumeron pois](https://github.com/KohaSuomi/Koha-22x/issues/171)
  * Mitä tämän kanssa tehtäisiin?
  * Yksi vaihtoehto voisi olla ottaa asetus pois päältä ja tuoda nykyversion 001-liitännäinen uuteenkin versioon.
  * **Päätös**: Tuodaan vanha 001-liitännäinen, eikä käytetä autocontrolnumber-järjestelmäasetusta.
* Jos teette tuotantoon viestipohjiin muutoksia, muistakaa tehdä ne myös nextille.

Pohjoisesta etelään.

**OUTI**
* Raahen Finvoice-laskutus nytkähti taas eteenpäin (on ollut työn alla viime syksystä asti ja etenee hitaasti). Sovittu, että Raahe alkaa laskuttamaan tuotannossa vasta versionvaihdon jälkeen. Koetamme saada sen siiheksi osaltamme niin valmiiksi kuin mahdollista.
* Normaalia ylläpitoa ja versionvaihtoon liittyviä töitä

**Vaski**
* 19.4. Koha-katko pääsi Turun Sanomiin raflaavilla otsikoilla
* Tätistä valunut virheellisesti tietoja muutaman osakohteen päälle. Syy toistaiseksi tuntematon. Vaski tekee tiketin.

**Vaara**
* ei mitään eristyistä, mutta mainitsen uuden nidetyypin testauksen tuloksia
* Vaarassa tarvitaan uusi nidetyyppi, jonka laina-aika on 7 vrk, rajoitus 1, on varattavissa mutta ei uusittavissa, lyhyt noutoaika varauksella.
Nide ei saa kellua eikä sitä kuljeteta, eli se on lainattava aina kotikirjastostaan.
 * Testasin Vaaran tuotannossa lainaamista ja varaamista. Laina- ja maksusäännöissä nidetyypille laitoin varauksia sallituksi 1 kaikkiin kolmeen varausta koskevaan asetukseen, hyllyvaraus sallittu "Jos yhtään ei ole saatavilla". Nidetyypeittäin oleviin varaussääntöihin laitoin varaussääntö-sarakkeeseen "Mistä tahansa kirjastosta" ja varauksen noutokirjasto täsmää "niteen kotikirjasto".
 * Testaukseni mukaan varauksen rajoittaminen ei onnistu, vaikka säännössä määritellään vain yksi varaus sallituksi. Asiakas voi Finnan kautta
varata useita saman nidetyypin nimekkeitä. Kuljetuksen estäminen sen sijaan onnistuu, eli niteen voi varata noudettavaksi vain niteen kotikirjastosta. Jos asiakkaan kotikirjasto on joku muu eikä vaihda noutopaikkaa, tulee virheilmoitus "The supplied pickup location is not valid" (en ole vielä keksinyt, miten tuon saa suomeksi, mutta eiköhän se jostain onnistu). Hyllyvaraus sen sijaan ei onnistu, varauspainike ei tule ollenkaan näkyviin Finnassa, jos nide on saatavana-tilassa.
 * Nextillä uuden nidetyypin testaaminen ei oikein onnistunut, sillä varaaminen ei onnistu. Varausnapissa lukee Tarkista varaus. Kun siitä klikkaa, saa tekstin: "Kirjastojärjestelmään ei saatu yhteyttä. Tietoja, jotka liittyvät tiliisi kirjastossa, ei voida näyttää. Jos ongelma jatkuu, ota yhteyttä kirjastoon."

**Lumme**
* Lumpeiden chat-palvelu loppui 2.5. vähäisen käytön takia.
* Lumpeilla lisättiin myös maksujen osamaksumahdollisuus Finnaan.

**Siilinjärvi**
* Keskusteltu Kodon kanssa asiakasrekisterin siivoamisesta.
* Ei muuta mainittavaa.
 

## Viikko 17 muistio

Aika: 25.4.2023 klo 9.15 <br />
Läsnä: Tuomas Kunttu (Kyyti), Veli-Pekka Marjoniemi, Piia Semenoff, Pirkko-Liisa Lauhikari (OUTI), Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Pia Kusmin (Lappi), Reetta Pihlaja (Siilinjärvi), Hanna Ikonen, Katja Valjakka (Lumme), Susanna Sandell (Vaski)

**Yhteiset**
* [Nexteiltä siirrettävät](https://github.com/KohaSuomi/Koha-22x/wiki/Versiovaihdon-muistiinpanot#nextilt%C3%A4-tuotantoon), siirretäänkö asiakasrajoitukset ja asiakasmääreet?
  * Siirretään asiakasmääreet. Huolehdittava, että Nextillä on oikea määrä määreitä ennen versionvaihtoa.
  * Ei siirretä asiakasrajoituksia. Mikään kimppa ei ole vielä ainakaan lisännyt sinne uusia rajotteita.
* miten testailut menee?

Etelästä pohjoiseen

**Kyyti**
* Mitä kaksivaiheinen tunnistautuminen vaatii puhelimeen?
TOTP:tä tukeva ohjelma, Kohan ohjeiden mukaan esim. Google Authenticator, andOTP, FreeOTP
* Nextillä Kaikki lainat -kuitissa oleva uusintakertojen määrä <<items.renewals>> ei enää toimi, mutta <<issues.renewals_count>> vaikuttaisi toimivan.
* Nextillä varausten järjestys ei toimi oikein, koska uusi varaus menee ensimmäiseksi jonossa. Liittyy kuulemma tietokantojen redusointiin, esim. Vaskissa toimii oikein.
* Miten voisi saada esim. esineen varattavaksi siten, että sen voisi noutaa vain niteen sijaintikirjastosta (ettei lähde kuljetukseen)?
Voisi testata laina- ja maksusääntöjen Oletusvaraussääntö nidetyypeittäin -kohtaa. Varauksen noutokirjasto täsmää: niteen sijaintikirjasto.

**OUTI**
* Tuotanto-Finnassa asiakastietojen muutospyynnöt lakkasivat toimimasta ja asiakkaat saivat virheilmoituksen "Pyyntöä ei voitu käsitellä. Yritä uudestaan."  Ongelma oli myös Vaskissa. Ongelma johtui siitä, että Vaskissa ja OUTIssa oli ylikirjoitettu sivupohja myresearch/change-address-settings.phtml. Kun ylikirjoitus poistettiin, muutospyynnöt lähtivät taas toimimaan. Koska samaa ongelmaa on myös osalla next-Finnassa, niin kokeiltiin samaa korjausta myös siellä. Korjauksella saatiin varaustunnuksen muutospyyntö toimimaan, mutta osoitetietojen muutospyynnöt antavat edelleen next-Finnassa virheilmoituksen. 
* Link Mobility (SMS-palvelu) ottaa uuden varmenteen käyttöön 25.4.2023 klo 15.00. OUTIssa ei aiheuta toimenpiteitä Kohan eikä Webkaken osalta. 
* Oulussa on mennyt ja menee kirjastoja (Puolivälinkangas, Kaukovainio, Asema) kiinni remontin tai muun syyn vuoksi. Kiinnimenot ovat aiheuttaneet muutoksia Kohaan. 
* OUTIssa testataan next-Finnassa verkkomaksuja Ceeposin verkkomaksuportaalin kanssa. 

**Vaara**
* Viime viikolla otettiin käyttöön Finnaan muutos, jossa asiakas voi valita mitkä maksut maksaa eli ei ole pakko maksaa kaikkia maksuja kerralla.
* Vaaran henkilökunta on testannut nextiä ja useampi on kommentoinut, että hakutulokseen pitäisi saada niteen luokkatieto näkyviin.
* Testattu testattavia tikettejä ja muutakin mieleen juolahtavaa.

**Lappi**
* Muutamia EditX-virheitä tullut
* Normaalia ylläpitoa ja versionvaihtoon liittyviä töitä

**Siilinjärvi**
* Kaksivaiheinen tunnistautuminen ei ehkä tule käyttöön ainakaan heti
* Ei muuta mainittavaa

**Lumme**
* Lumpeissa sama ongelma kuin Outissa next-Finnassa, mitä tulee asiakkaiden osoitteenmuutospyyntöihin.
* Lumme-next Lumpeiden Koha-ryhmän kokeiltavaksi.
* Kokeiltiin auktorisoitujen arvojen muutoksia, jotta Tilanahtaus-status saataisiin toimimaan järkevästi Kohassa ja Finnassa. Kokeilut tämän osalta jatkuvat. 

**Vaski**
* Versiovaihdon asiakastiedotus alkamassa ja Nextin testaus laajennetaan koko henkilökunnalle
* Oppimateriaalikeskuksen järjestelmän uusiminen suunnitteilla


## Viikko 16 muistio

Aika: 18.4.2023 klo 9.15 <br />
Läsnä: Veli-Pekka Marjoniemi ja Pirkko-Liisa Lauhikari (OUTI), Kati Sillgren (Helle), Reetta Pihlaja (Siilinjärvi), Päivi Knuutinen ja Irina Halminen (Vaara), Hanna Ikonen (Lumme), Mikko Liimatainen (Vaski), Tuomas Kunttu (Kyyti)

**Yhteiset**

* Asiakasviestien ajastukset tällä hetkellä / Kodo
  * Helle 8.00 overdue_notices.pl, 8.40 advance_notices.pl, 9.10 membership_expiry, kirjeet ei lähde
  * Kyyti 8.40 advance_notices.pl, 9.00 overdue_notices.pl, 9.10 membership_expiry.pl, kirjeet 14.30 ja 20.50
  * Lappi 8.40 advance_notices.pl, 9.00 overdue_notices.pl, 9.10 membership_expiry.pl, kirjeet 20.50
  * Lumme 6.00 holds_reminder.pl, 9.10 membership_expiry.pl, 12.25 advance_notices.pl, 12.29 overdue_notices.pl, kirjeet 20.50
  * Outi 8.40 advance_notices.pl, 9.00 overdue_notices.pl, 9.10 membership_expiry.pl, kirjeet 20.50
  * Siili 0.20 overdue_notices.pl, 0.25 advance_notices.pl, kirjeet ei lähde
  * Vaara 00.25 advance_notices.pl, 22.04 overdue_notices.pl, 22.00 membership_expiry.pl, kirjeet 13.30 ja 22.15
  * Vaski 9.00 overdue_notices.pl, 12.19 advance_notices.pl, 9.10 membership_expiry.pl, kirjeet 20.50
  * Osa ajastuksista vaikuttaa omituisilta, osa päällekkäin huoltojen kanssa, runsaasti kimppakohtaista varianssia, miksi näin ja löytyisikö yhteistä linjaa näihin?
  
  **Päätös:** Ajastetaan viikkopalaverin 11 päätöksen mukaisesti: Kaikille kimpoille aina (ei vain huoltoikkunan aikaan) viestien generointi klo 9.11 ja viestien lähetys alkamaan klo 9.30. Uudet ajastukset unohtuivat tehdä 12.4., joten laitetaan päälle mahdollisimman pian eli jo tänään 18.4.2023. 
 
 * Hellen, Kyytin ja Lumpeen jonossa roikkuvat 'pending' tilaiset kirjeet aiheuttavat meille valvonnan virheilmoituksia / Kodo
   * Message queue has messages pending for 108 days (Kyyti)
   * Message queue has messages pending for 214 days (Helle)
   * Message queue has messages pending for 3 days (Lumme)
   * Voidaanko merkitä senteiksi tai failedeiksi esimerkiksi cronilla?
   
   **Päätös:** Helle, Kyyti ja Lumme tarkistavat itse säännöllisesti (mielellään päivittäin) pendign-tilassa roikkuvat viestit ja hoitavat ne itse pois. Jos viestejä paljon, voi tarvittaessa tehdä tiketin, niin kehittäjät poistavat ne ajona.

* Käykää läpi kirjepohjat ja muistakaa, että kirjeviestirajapinta / suomi.fi / postitus- ja kuorituspalvelut _eivät_ rivitä tekstejä automaattisesti. Jos tekstirivit ovat liian pitkiä, niin rivit yksinkertaisesti katkeavat kirjeellä oikeasta laidasta paperin reunan tullessa vastaan. Ainakin Juvan kirjeissä näyttää olevan hyvin pitkiä rivejä. Muistakaa myös, että nimeke voi yksinäänkin olla jo satoja merkkejä pitkä: "Sopimus Belgian kuningaskunnan, Tanskan kuningaskunnan, Saksan liittotasavallan, Helleenien tasavallan, Espanjan kuningaskunnan, Ranskan tasavallan, Irlannin, Italian tasavallan, Luxemburgin suurherttuakunnan, Alankomaiden kuningaskunnan, Portugalin tasavallan, Ison-Britannian ja Pohjois-Irlannin yhdistyneen kuningaskunnan (Euroopan unionin jäsenvaltiot) ja Norjan kuningaskunnan, Itävallan tasavallan, Suomen tasavallan ja Ruotsin kuningaskunnan välillä Norjan kuningaskunnan, Itävallan tasavallan, Suomen tasavallan ja Ruotsin kuningaskunnan liittymisestä Euroopan unioniin." / Kodo

  **Päätös:** Hyvä tarkistaa kaikissa kimpoissa kirjeviestipohjien rivitykset.
  
* Tikettien tekeminen ja kommentointi -ohje siirretty Redminestä Githubiin [Koha-repositorion wikiin](https://github.com/KohaSuomi/Koha/wiki/Tikettien-tekeminen-ja-kommentointi).

* Käännösmuutos varauksenteko-sivulle?
  * Varauksenteko-sivulta on piilotettu asiakashaun hakutulostaulukko, mistä johtuen asiakkaan hakeminen onnistuu käytännössä vain kirjastokortilla tai koko nimellä niin, että tuloksena on yksi ainoa vastaus. Hakukentän yläpuolella on kuitenkin ohje "Syötä kirjastokortin numero tai osa nimestä:" eli englanniksi "Enter patron card number or partial name:". On ehdotettu, että käännöstä muutettaisiin.
  * Jos muutos tehdään, on se sellainen, mikä pitää ylläpitää Koha-Suomessa jokaisessa versionvaihdossa. Muita vastaavia muutoksia on esim. phone-kentän nimeäminen Lankapuhelimeksi ja mobile-kentä Matkapuhelimeksi (yhteissö primary phoe ja other phone). Koska muutostarve johtuu meidän omasta piilotuksesta (pyritään vähentämään asiakastietojen katseluja), ei ole perusteltua muuttaa yhteisön käännöstiedostoihin käännöstä.
  
  **Päätös:** Kannatettiin ajatusta, että ohjeteksti olisi sen mukainen, kuin haku tulee tehdä eli ohjeistetaan, että asiakashaku tulee tehdä kirjastokortilla tai asiakkaan koko niemllä. Kehittäjät ehdottivat, että käännöstiedostojen ajojen jälkeen ajettaisiin aina automaattisesti skripti, joka muuttaisi kaikki Koha-Suomen omat ylläpidettävät käännösmuutokset halutuiksi. Kysytään vielä Annelin mielipidettä. 

* [Damaged-tila yliajaa muut tilat Finnassa](https://github.com/KohaSuomi/Finna-kehitysehdotukset/issues/2#issuecomment-1506892120)
  * Susanna: Finnassa pystytään priorisoimaan tilat. Priorisointi on toteutettuna tällä hetkellä meidän testinäkymään vaski.finna-pre.fi, mutta sitä on ilman Kohaan pääsyä muiden hankala testata. Meidän testauksen perusteella kaikki näyttää menevän oikein. Miten edetään?
  
  **Päätös:** Vaski testaa nextillä ja versionvaihdon jälkeen tuotannossa. Vaskin kokemusten perusteella katsotaan, tehdäänkö tilojen priorisointi Finnassa myös muille kimpoille.

**OUTI**
* OUTIn uuden version henkilökunnan testaukset alkoivat 17.4. Jokaista Kohan ja verkkokirjaston osa-aluetta testaa kaksi henkilöä ja kirjaavat testaushuomiot testaustaulukkoon. Isompia ongelmia ei ainakaan ensimmäisen päivän aikana tullut esille.
* Kansalliskirjastosta oli tullut ilmoitus, että joissakin Melindan tietueissa on käytössä 852 5-osakenttä, joka ei oikeasti kuulu formaattiin, joten Heikkisen Antti pyysi, että säädetään TäTin Nalkuttimeen asetukseen, että myös tämä kenttä pääsee läpi.

**Siilinjärvi**
* Ei mainittavaa

**Vaara**
* Tiina Vauhkonen lopettanut pääkäyttäjänä
* Vaaran henkilökunnalle annettu oikeus koekäyttää nextiä. Vielä ei ole juurikaan tullut kommentointia.

**Lumme**
* Automaatit toimivat taas.
* Nextin testaus laajenee Lumpeiden pääkäyttäjille.

**Vaski**
* Verkkomaksun testauksesta voi sopia Kansalliskirjaston kanssa, että Nexteille halutaan kiinni testausympäristö. Vaskissa oma toteutus testattavana.
* Damaged-tilojen priorisointia verkkokirjastossa testattu. Kuljetus ohittaa damaged-tilat. Not-loan on väärässä kohtaa.

**Kyyti**

* Nextillä ISSUESLIP-kuitissa oleva uusintakertojen määrä <<items.renewals>> ei enää toimi. Kokeilin vaihtaa siihen <<issues.renewals_count>> ja se ilmeisesti toimii. Kannattaa muidenkin testata.
* Nextillä perustiedot-näytöltä puuttuu Vie/Tuo-painike. Teen siitä tiketin.
* Sivulla https://github.com/KohaSuomi/Koha-22x/wiki/Versiovaihdon-muistiinpanot lukee, että tiputetaan seuraavat taulut: okm_statistics, okm_statistics_logs ja biblio_data_elements. Varmistin, että nämä siis todella poistuvat. Näitä korvaavat uudet taulut ovat: koha_plugin_fi_kohasuomi_okmstats_biblio_data_elements ja koha_plugin_fi_kohasuomi_okmstats_okm_statistics

## Viikko 15 muistio

Aika: 11.4.2023 klo 9.15 <br />
Läsnä: Anni Rajala (Vaski), Pirkko-Liisa Lauhikari ja Veli-Pekka Marjoniemi (OUTI), Kati Sillgren (Helle), Tuomas Kunttu (Kyyti), Hanna Ikonen (Lumme), Anneli Österman, Pasi Kallinen ja Kodo Korkalo (Koha-Suomi)

**Yhteiset**
* Oletuskieli -> suomi, tehdään ajo kaikille asiakkaille, jotta ei tulostu sekakielisiä kuitteja. [Liittyy tikettiin Koha-22x/#151](https://github.com/KohaSuomi/Koha-22x/issues/151).
* Muistattehan tehdä tiketit sip-tunnuspyynnöistä. Ei pelkkää sähköpostiviestiä, jotta muutoksista/pyynnöistä jää jälki tikettijärjestelmään ja ne saadaan tilastoitua.
* [Ehdota esitystä KohaConiin 14.-18.8.2023](https://github.com/KohaSuomi/Koha/discussions/492)

**Vaski**
* Turun pk:n musaosasto kiinni 4 viikkoa, ei-saatavilla olevalle aineistolle lisätty erikoistila.
* Finna-testaus nextiä vasten suurimmaksi osaksi tehty.
* Verkkomaksamisen testaus? Sovittiin, että Vaski selvittää Finna-toimistolta josko olisi mahdollista järjestää testausmahdollisuus. Testata pitäisi kolmessa eri ympäristössä (Turun oma toteutus, Ceepos, suora Paytrail-yhteys), mutta palataan testaaviin kimppoihin seuraavassa pääkäyttäjäpalaverissa.
* Testattu asetusta AllowRenewalIfOtherItemsAvailable nextillä (versiossa 22.x tullut muutoksia) ja testauksen perusteella tulkitsee nyt saatavilla oleviksi niteiksi ainoastaan hyllyssä olevat niteet (joilla ei ole erikoistilaa) sekä koti-/siirtoyksikköön kuljettavat niteet. Asetus voi mahdollisesti edelleen aiheuttaa suorituskykyongelmia, OUTIssa on taannoin jouduttu ottamaan asetus pois käytöstä koska asiakkaat eivät pääseet omiin tietoihinsa. Kyytissä asetus on nytkin käytössä. Vaski kokeilee mahdollisesti asetuksen käyttöönottoa heti versiopäivityksen jälkeen.

**OUTI**
* Ei mitään erikoista.

**Kyyti**
* Kyytin toinen pääkäyttäjä on Roosa Väisänen Kotkasta. 

**Lumme**
* Automaateilla palvelinongelmia. Ongelmia selvitellään.


## Viikko 14 muistio

Aika: 4.4.2023 klo 9.15 <br />
Läsnä: Veli-Pekka Marjoniemi (OUTI), Kati Sillgren (Helle), Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Reetta Pihlaja (Siilinjärvi), Hanna Ikonen ja Katja Valjakka (Lumme), Pia Kusmin (Lappi), Anneli Österman (Koha-Suomi)

**Yhteiset**
- Koha-Suomen harjoittelija Ville esittäytyi.
- Versionvaihdon työt aloitetaan ma 15.5.2023 klo 22 tietokanta-ajoilla. Eli palvelut on pois käytöstä tuosta lähtien.
- Uusia pääkäyttäjiä: Lumme ja Kyyti
- huoltoikkuna tulossa 12.4.2023, tiedossa katkoja tietokanta-ajojen vuoksi. [Huoltotiedote](https://github.com/KohaSuomi/Koha/discussions/491)

Pohjoisesta etelään.

**OUTI**
* Normaalia ylläpitoa ja nextin testausta.

**Vaara**
* Normaalia ylläpitoa ja nextin testausta.

**Siilinjärvi**
* Normaalia ylläpitoa ja nextin testausta.

**Lumme**
* Normaalia ylläpitoa ja nextin testausta.

**Lappi**
* Normaalia ylläpitoa ja nextin testausta.


## Viikko 13 muistio

Aika: 28.3.2023 klo 9.15 <br />
Läsnä: Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Veli-Pekka Marjoniemi ja Pirkko-Liisa Lauhikari (OUTI), Heli Auranen, Timo Pesonen, Katja Valjakka (Lumme), Reetta Pihlaja (Siilinjärvi), Kati Sillgren (Helle), Tuomas Kunttu (Kyyti), Pia Kusmin (Lappi), Anneli Österman ja Lari Strand (Koha-Suomi)

**Yhteiset**
* nideryhmien käyttöönottoaikataulu
  * Suurin osa pääkäyttäjistä oli sitä mieltä, että käyttöönotto vasta versionvaihdon jälkeen
* cardnumber-kenttään käyttäjätunnus, jotta voidaan ottaa käyttää triggeri, joka pitää cardnumberin ja userid:n synkassa keskenään.
* [Uudet virkailijaoikeudet](https://github.com/KohaSuomi/Koha-22x/wiki/Uudet-virkailijaoikeudet)
* SIP2-pyynnöt, teettehän myös tiketin, kun laitatte tunnuspyynnön sähköpostiin.
* [Kimppojen logot voi laittaa tähän tikettiin talteen](https://github.com/KohaSuomi/Koha-22x/issues/18)
* OPACAllowUserToChangeBranch - Finna ei noudata tätä, joten ei merkitystä, mitä valitaan. Voi laittaa Suspended varmuuden välttämiseksi, jos siihen joskus tulee muutosta.

Kuulumiset etelästä pohjoiseen.

**Vaski**
* Koha-testaus työn alla, pyritään testaamaan tietyt seikat pääsiäiseen mennessä.
* Pohdittiin, onko tarpeen vaihtaa Finnan oletusnäkymä versionvaihdon yhteydessä. Luultavasti ei, mutta testataan Omat tiedot -sivu ja varausten toiminta erityisen tarkasti. Testauksen perusteella päätetään, miten toimitaan. Vaihdossa toki täytyisi varmistaa tilastojen siirtyminen näkymästä toiseen, joten mieluummin pidettäisiin vanha oletusnäkymä.
* Oltiin kiinnostuneita siitä, mihin kellonaikaan päivitys alkaa 16.5., jotta voidaan tiedottaa henkilökunnalle ja asiakkaille. Ei vielä tarkkaa tietoa, Anneli sanoi että selvittää tätä.

**Vaara**
* ei mitään erityistä, nextin testausta ja tuotantotietokannan siivousta vajavaisten aineistotietojen (aineistotyyppi epämääräinen yläkäsite) takia

**OUTI**
* Ei mitää erityistä. 
* Yhdestä kirjastosta on tullut ihmettelyä, että yhdellä asiakkaalla mobiilikortin viivakoodi ei ollut näkynyt verkkokirjaston Kirjastokortit-sivulla, kun hänen maksuraja oli ylittynyt. Viivakoodin tilalla oli ollut  teksti "Asiakas lainauskiellossa" tjs. Kun maksut oli maksettu, mobiilikortti oli tullut näkyviin. Tuessa testattu, mutta vastaavaa ongelmaa ei ole saatu aikaan. Myös Finna-tilillä mobiilikortti näkyy, vaikka asiakkaan maksuraja on ylittynyt. Nyt jälkikäteen tuli mieleen, että olisikohan asiakas ja kirjaston työntekijät katsoneet ensin vahingossa mobiilikorttia asiakkaan tiedoissa väärältä sivulta esim. asiakkaan Omat-tiedot sivulta. Tiedä häntä, sillä kaikki on mahdollista. :D

**Lumme**
* Kirjeviestien lähettämisessä häiriötilanne 13.2. alkaen. Tilanne huomattu 24.3.
* Tilejä lukkiutunut ja jäljet näyttävät johtavan Ellibsiin.
* 100% pääkäyttäjä aloittaa viikolla 14, Hanna Ikonen.
* Nextin testaus ja säätö jatkuu.

**Siilinjärvi**
* Kunnasta tullut ilmoitus, että verkkomaksaminen on nyt valmis käyttöönottoon. Siirretään sitä versionvaihdon yli, mikäli mahdollista.
* Koska kuljetustilan peruminen Finnassa tuntuu toimivan ongelmitta muuaalla, otetaan se meilläkin nyt käyttöön.
* Jos maa on asiakastiedoissa turhaa tietoa, piilotetaan se pois Kohasta ja Finnasta.

**Helle**
* Asiakkaalla on ollut yksi varaus niteettömään tietueeseen. Kohassa asiakkaan Varaukset-välilehdellä yksikään asiakkaan varauksista ei näkynyt.
* Yksi Sotuteekin käyttäjistä ilmoittanut, että Sotuteekki heittää toiminnosta ulos pikaisesti. Useimmiten yhden haun jälkeen (muutaman minuutin jälkeen). Toisinaan Sotuteekki saattaa pysyä auki vähän kauemmin. 

**Kyyti**
* Haminasta on tiedusteltu tilastojen saamista ulkoiseen järjestelmään ns. johdon työpöydälle. Kohassa ei vielä sellaista ominaisuutta ole. Koha-Suomen strategiassa asia on mainittu. Anneli selvittää vielä, mikä ongelma oli raporttien JSONiin liittyen.

**Lappi**
* Ei mitää erityistä. Versionvaihtoa ja normi ylläpitoa.

## Viikko 12 muistio

Aika: 21.3.2023 klo 9.15 <br />
Läsnä: Veli-Pekka Marjoniemi ja Pirkko-Liisa Lauhikari (OUTI), Kati Sillgren (Helle), Reetta Pihlaja (Siilinjärvi), Pia Kusmin (Lappi), Heli Auranen, Tenho Volanen, Timo Pesonen (Lumme), Anni Rajala (Vaski), Anneli Österman ja Pasi Kallinen (Koha-Suomi)

**Yhteiset**
* Pohdintaan: Meillä säilytetään kimpasta riippuen ei-aktiivisten asiakkaiden tiedot 5-6 vuotta, mutta tiedot poistetaan asiakkaan pyynnöstä jo sitä ennen. Laskut pitää säilyttää lain mukaan 10 vuotta lähdejärjestelmässä. Voiko asiakkaan poistaa, jos häneltä on laskutettu aineistoa alle 10 vuotta sitten poistopyynnön ajankohdasta?
  * Pirkko-Liisa kyseleen Oulun arkistonhallintahenkilöltä tarkempia tietoja. Jatketaan sen jälkeen asian pohdintaa.
* [Koha-klinikka 29.3.2023 klo 9-11](https://github.com/KohaSuomi/Koha/discussions/469). Esitellään uutta versiota.
* [Versionvaihdon tiedote 2](https://github.com/KohaSuomi/Koha/discussions/471)
* [Finna-nextit](https://github.com/KohaSuomi/Koha-22x/wiki/Finna-nextit)
* Maksut-osiossa Tapahtumat-välilehdellä nappien lisäpiilotuksia? Onko Tulosta ja Maksa turhia?<br />
![kuva](https://user-images.githubusercontent.com/33121325/226279846-d976157d-2e54-42bc-9e74-1102cf3c6d5c.png)
  * Reetta tekee tiketin piilotuksista Koha-repositorioon. Anneli tutkii sopivassa välissä, miten piilotukset onnistuu.
* [Varaustunnus asiakasmääreeksi](https://github.com/KohaSuomi/Koha-22x/wiki/Mit%C3%A4-pit%C3%A4%C3%A4-tehd%C3%A4-next-kannassa#varaustunnus-asiakasm%C3%A4%C3%A4reeksi)
* Kohan ohje suomeksi päivitysvastuut, aiemmin näin:
  * Asiakkaat: Piia Semenoff
  * Lainaus: Pirkko Lauhikari
  * Maksut: Lumpeet
  * Varaukset: Lumpeet
  * Kuvailu: Päivi Knuutinen
  * Kausijulkaisut: Vaski
  * Hankinta: Anneli Österman
  * Listat ja Kori: Lappi
  * Raportit: Anneli Österman
  * Tiedonhaku: Kyyti
  * Kuittitulostuksen asetukset: Pirkko-Liisa Lauhikari
  * Työkalut
    * 12.1-12.3 Asiakaslistat - Myöhästymisilmoitusten määrittely: Reetta Pihlaja
    * 12.4. Lähetä laskuja -> tämä pitäis saada pois numeroinnista
    * 12.5-12.10 Asiakkaiden poisto - Tietueiden muokkaus: Lappi (HUOM! osa siirtynyt Kuvailu-osioon)
    * 12.11 Automaattinen niteen muokkaus: Kati Sillgren
    * 12.12 MARC-muokkauksen pohjat: Kati Sillgren
    * 12.13 Kalenteri: Piia Semenoff
    * 12.14 Lokien katselu: Tuomas Kunttu
    * 12.15-12.17 Uutiset-Siirtokokoelmat: Tuomas Kunttu
  * [Kohan ohje suomeksi -muotoiluohjeet](https://github.com/KohaSuomi/kohasuomi.github.io/wiki/Kohan-ohje-suomeksi--muotoiluohjeistus)

Kuulumiset pohjoisesta etelään.

**OUTI**
* Verkkokirjaston Finna-tilin sähköpostikentässä olevaa s-postiosoitetta käytetään mm. verkkomaksujen maksukuittien lähettämiseen, mutta tähän s-postikenttään ei päivity tieto, jos asiakkaan sähköpostiosoite on muutettu Kohan asiakastietoihin tai Finnassa asiakkaan Omat tiedot -osion ”Kirjaston ylläpitämät henkilötiedot -osioon”. Aasiakkaan on itse päivitettävä muuttunut s-postiosoite Finna-tilin kenttään. 
Finna-tuki on ottanut pohdittavakseen, mitä ongelmalle voitaisiin tehdä. Ehdotimme, että Finna-tilin sähköposti-kenttä pitäisi aina päivittyä, jos asiakaan osoite muutetaan Kohaan tai ”Kirjaston ylläpitämät henkilötiedot” -osioon. Toinen vaihtoehto voisi olla, että sähköpostit lähetetään aina siihen osoitteeseen, joka on ”Kirjaston ylläpitämät henkilötiedot” -osiossa. 

**Siilinjärvi**
* Tehty tiketti [#476](https://github.com/KohaSuomi/Koha/issues/476) painikkeiden lisäpiilotuksesta
* Ei muuta erikoista

**Lappi**
* Normi ylläpitoa
* Versionvaihtoon liittyviä töitä

**Lumme**
* Nextin säätöjä tehty, testailu käynnistetään laajemmin.

**Vaski**
* Perusylläpitoa ja Nextin testaamista.

## Viikko 11 muistio

Aika: 14.3.2023 klo 9.15 <br />
Läsnä: Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Pia Kusmin (Lappi), Tuomas Kunttu (Kyyti), Veli-Pekka Marjoniemi ja Pirkko-Liisa Lauhikari (OUTI), Heli Auranen, Timo Pesonen (Lumme), Reetta Pihlaja (Siilinjärvi)

**Yhteiset**
* Tapahtumalokin (action_logs) aktiivisen taulun datan siivous arkistotauluun kuukausittain. Siivousajo vuositasolla liian raskas. /Lari
* Viesti-cronien ajastukset säännöllisen huoltoikkunan aikavälin ulkopuolelle?
  * Tällä hetkellä on osassa kimppoja ajastettu huoltoikkunan aikavälille (klo 7-9) mm. advance_notices, overdue_notices ja membership_expiry -cronit ja ne eivät tule ajetuksi automaattisesti. 
  * Kaikki cronit on estetty huoltoikkunan ajaksi eli kuukauden toisena keskiviikkona klo 6.50 - 9.10 ei ajeta croneja.
  * **Päätös**: Ajastetaan kaikille kimpoille aina (ei vain huoltoikkunan aikaan) viestien generointi klo 9.11 ja viestien lähetys alkamaan klo 9.30. Ajastus muutetaan 12.4.2023 lähtien.
* https://github.com/KohaSuomi/Finna-kehitysehdotukset/issues/2 Listattujen nidetilojen priorisointi
* [Versionvaihdon testattavien tilanne](https://github.com/orgs/KohaSuomi/projects/6/views/3)
* OAI-PMH saatu toimimaan, joten nyt Anneli voi pyytää testi-Finnat next-kannoille.

Kuulumiset etelästä pohjoiseen.

**Vaara**
* Päivi testannut nextillä hieman, tallentanut asetuksia jne. Pääkäyttäjien yhteinen katselmus vielä tekemättä.
* Testattavien tikettien tutkailu jäi lyhyeen, kun en osannut tarttua moneenkaan tikettiin ymmärryksen puutteen vuoksi.

**Lappi**
* Lapissakin otetiin käyttöön yläpalkin Koha-asioiden alasvetovalikko. Kiitos Helle ja Kati vinkistä.
* Versionvaihtoon liittyviä töitä, mm. asetusten määrittelyä Nextiin. Testaus pyritään alkamaan mahdollisiman pian.

**Kyyti**
* Kansikuvien näkymiseen liittyvään tekemääni [tikettiin](https://bugs.koha-community.org/bugzilla3/show_bug.cgi?id=33193) Bugzillassa on vastattu. 
Sen perusteella asia on liian vaihea korjattavaksi.
* Lähikirjastossa palautettu nide ei ole mennyt kuljetustilaan, vaikka palautettaessa siitä tulee ilmoitus ("Palauta tämä nide kirjastoon X"). Nide näkyy Lähetettävät kuljetuksen -raportilla, mutta ei vastaanottavan kirjaston Vastaanotettavat kuljetukset -raportilla. Silti nide on saatavana-tilassa. Mitään syytä asialle ei löytynyt. Tilanteen saa korjattua, kun ensin vaihtaa kirjautumiskirjaston vastaanottavaksi kirjastoksi ja palauttamalla niteen ja sitten vaihtaa kirjautumiskirjaston takaisin ja paluttaa niteen. Nyt kuljetustila menee päälle.

**OUTI**
* Asiakkaalta oli tullut palautetta, että kun hän kirjautuu mobiililaitteella verkkokirjastoon käyttäen Firefoxia ja hänellä on päällä automaattinen käyttäjätunnuksen ja salasanan täyttöä, PIN-koodi tulee selväkielisenä Kirjaudu sisään -painikkeeseen/painikkeen päälle. Chromella vastaavaa ongelmaa ei tullut. Asiakas oli asentanut Firefoxin uudelleenkin, mutta sekään ei ollut auttanut. Lopulta selvisi, että ongelma tuli asiakkaalla OnePlus Nord 2T 5G -puhelimella. Vika liittyy ilmeisesti valmistajan käyttöjärjestelmään ja selaimeen. Oulun it-tiimi testasi myös muiden valmistajien laitteilla, eikä ongelmaa saatu niissä toistettua.
* Luetteloijilta tuli palautetta, että TäTin nalkutin herjaa 884 5 -kentästä: ”ei formaatissa”. Eli nalkutin tärppäsi kiinni kyseiseen kenttään, koska se ei oikeasti kuulu MARC21-formaattiin. Kentän 884 5-osakenttä on nyt lisätty TäTin nalkuttimeen, joten ei pitäisi herjata siitä enää. Heikkisen Antti on yhteydessä Melindaan 884 5-kentän käytöstä.
*  Toinen Kirjastopalvelun tietuepaketeista, joka oli tullut 7.3., näytti, että se olisi tuotu, mutta tietueita ei löytynyt TäTistä. Anneli poisti paketin tuonnin ja toi sen uudestaan. Paketin sisältämät tietueet alkoivat löytyä saman tien TäTistä. Tietueet olivat tulleet tietokantaan jo ensimmäisen tuonnin yhteydessä, mutta Anneli arveli, että ne eivät olleet jostain syystä indeksoituneet.
*  Nexstiä säädetty. Yhdessä katsottu, mitä otetaan käyttöön uusista ominaisuuksista, IntranetuserCSS:n ja -JS:n vapaaehtoisista määrityksistä.

**Lumme**
* Nextin säätäminen aloitettu
* Otetiin käyttöön yläpalkin Koha-asioiden alasvetovalikko heti viime viikon kokouksen jälkeen, kiitos vinkistä.

**Siilinjärvi**
* Nextin tutkailu ja säätäminen aloitettu täälläkin.
* Siilin muista poikkeavat croni-ajastukset voidaan yhtenäistää muiden kimppojen kanssa.
* Muuten ei erikoista.

## Viikko 10 muistio

Aika: 7.3.2023 klo 9.15 <br />
Läsnä: Leena Kinnunen, Pia Kusmin (Lappi), Pirkko-Liisa Lauhikari ja Veli-Pekka Marjoniemi (OUTI), Kati Sillgren (Helle), Heli Auranen, Katja Valjakka (Lumme), Päivi Knuutinen (Vaara), Tuomas Kunttu (Kyyti), Reetta Pihlaja (Siilinjärvi)

**Yhteiset**
* [Finna-liitännäisen Readme-osioon](https://github.com/KohaSuomi/koha-plugin-rest-di/blob/master/README.md#sysprefs) kerätty, mitä järjestelmäasetuksia Finna-liitännäinen hyödyntää.
* Kuvailupohjissa Hinta voimassa alkaen ja Hankintapvm ei-pakollisiksi.
  * Hinta voimassa alkaen (replacementpricedate) ei kannata olla pakollinen, koska silloin siihen on pakko kirjoittaa jotain ja siihen tulee myös arvoja 0000-00-00, joista [Finna ei tykkää](https://github.com/KohaSuomi/Koha/issues/280). Kenttä täyttyy automaattisesti tallennuspäivällä, kun kenttä ei ole pakollinen.
  * Hankintapvm (dateaccessioned) täyttyy myös automaattisesti, kun siihen on kuvailupohjassa liitetty dateaccessioned-pl-liitännäinen. Ei ole tarvettaa laittaa pakolliseksi kuten datereceived aikanaan.
  * Päätös: otetaan pois kenttien pakollisuus. Pääkäyttäjien tehtävä muutos manuaalisesti kuvailupohjiin tuotantoon ja nextiin.
* Mitä tietoja tarvitsee siirtää nextiltä tuotantoon versonvaihdon aikaan. Edellisessä versionvaihdossa kerättiin [tällaista listaa](https://tiketti.koha-suomi.fi/projects/mls/wiki/P%C3%A4%C3%A4k%C3%A4ytt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-21-muistio).
  * järjestelmäasetukset
  * kuittipohjat
  * asiakasrajoitukset?
  * asiakasmääreet?
* IntranetNav-järjestelmäasetuksessa olevat linkit ajantasalle. Jos linkkejä vielä Redmineen, päivitättehän ne ohjaamaan GitHubiin vastaaville sivuille.
* Onko tarvetta omalle kanavalle versionvaihdolle Matrixiin?
* next-kannat
   * [mitä pitää muistaa tehdä next-kannassa](https://github.com/KohaSuomi/Koha-22x/wiki/Mit%C3%A4-pit%C3%A4%C3%A4-tehd%C3%A4-next-kannassa) 
   * finnat, Anneli pyytää kaikille, kunhan Kirkesin next olemassa
   * kaikki muut paitsi kirkes olemassa

**Lappi**
* Lapin pääkäyttäjät lomalla 10.3., ei päivystystä
* Nextiin viety asetuksia. Jaettu Käyttäjäryhmälle ja pääkäyttäjille testivastuita. 
* Otettu käyttöön uusia asetuksia: Nidetunnus varauksen saapumisilmoitukseen, Tiettyjen teosten valinta tarkempaan tarkasteluun, 
Epäonnistuneiden kirjautumisyritysten aktiivinen seuranta, Asiakaslajien viestiasetusten oletusruksit poistettu. 
* Kysy Kohasta pidetty onnistuneesti, käsiteltiin mm. tiedonhakua ja käyttäjiltä Padletilla kerättyjä kommentteja ja ongelmia. Päätetty järjestää jatkossa kaksi kertaa vuodessa. 

**OUTI**
* Uuden version uudet järjestelmäasetukset, IntranetUserCSS:t ja JS:t käyty läpi Annelin suositusten mukaan. Testaajia pyydetty henkilökunnasta.
* Otettu käyttöön Finnan ominaisuus, että asiakas voi perua itse kuljetettavana olevan varauksensa. 
* Nyt Celiat näkyvät Kirja-aineistotyypin alatyypeissä Äänikirja, joka jää faseteissa isojen tulosten kohdalla näkymättömiin. Piia kysynyt Finna-tuesta, olisiko mahdollista, että Kirja-valikko aukeaisi siten, että Äänikirja-aineistotyyppi näkyisi aina heti asiakkaalle hakutulosten määrästä riippumatta. Finna-tuki vastasi, että ei onnistu.
* Oulussa Puolivälinkankaan kirjasto menee remonttiin ja suljetaan 6.4.2023. Kirjaston kokoelma siirretään Koskelan kirjastoon, joka on ollut pitkään kiinni ja kirjastolle on nyt löytynyt väistötilat. Koskelan kirjasto avataan kesällä.

**Lumme**
* Automaateissa ongelmia. Palautusautomaatti ihan jumissa ja lainausautomaatit pätkivät. Sip palvelin käynnistetty uudelleen ja Lyngsoe käynnisti ohjelmat uudelleen. Lopulta lähti toimimaan.

**Vaara**
* Ei erityisempää. Päivi testannut nextiä ja käynyt läpi järjestelmäasetukset Annelin listauksen mukaan. Muut pääkäyttäjät eivät ole ehtineet juurikaan testaamaan ja yhteinen palaveri järjestämättä.
* Päivi testaillut PowerBIn raportteja ja toimintaa.

**Kyyti**
* Kyytissä lapsiasiakkaan yläikäraja on ollut 15 vuotta. Ja henkilöasiakkaan alaikäraja niin ikään 15 vuotta. Tästä seuraa se, että 15-vuotiaan voi tallentaa sekä lapsi- että henkilöasiakkaana. Jos tallentaa lapsena, muuttaa croni kyllä seuraavana yönä henkilöasiakkaaksi.
Näin asetuksen kuuluukin olla, jotta croni toimii oikein.
* Mitä kuuluu tiketille [#204](https://github.com/KohaSuomi/Koha/issues/204)? - on edelleen työn alla, joten ei vielä kuulukaan tuotannossa toimia.

**Siilinjärvi**
* Ei erityisempää, yritetään päästä kärryille nextin testaamisesta
* Sähköpostit kulkevat hyvin uudella noreply-osoitteella. Paitsi kuittiteksteihin unohtui vaihtaa meidän oma vanha kirjasto(at)siilinjarvi.fi, nyt vaihdettu.
* Kirjautumisyritys-asetukset pitäisi nyt olla meilläkin kunnossa.
* Luettelointipohjien ei-pakollisuudet päivitetty tuotantoon ja nextiin.


## Viikko 9 muistio

Aika: 28.2.2023 klo 9.15 <br />
Läsnä: Anneli Österman ja Kodo Korkalo (Koha-Suomi), Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Veli-Pekka Marjoniemi (OUTI), Kati Sillgren (Helle), Anni Rajala (Vaski), Leena Kinnunen (Lappi), Reetta Pihlaja (Siilinjärvi), Heli Auranen, Timo Pesonen (Lumme)

**Yhteiset**
* [Ajastetut ajot](https://koha-suomi.fi/dokumentaatio/ajastetutajot/) kuvattu ohjeisiin ja esittelyvideo [Crontabista](https://PPwww.youtube.com/watch?v=otIk2KIWPxM) Youtubessa.
* [Maksut sähköpostikuittiin](https://tiketti.koha-suomi.fi/issues/4245)
* Tiketti [KohaSuomi/Koha #204](https://github.com/KohaSuomi/Koha/issues/204) - kaikilta pois oletusviestiasetukset?
  * Sovittiin, että kaikki ottaa pois oletusviestiasetukset, koska jos käyttäjä unohtaa ottaa rastit pois, ei ne poistu tiketissä luodulla JS-rimpsulla ja tiketin alkuperäinen ongelma jatkuu.
* Ei päivitettävää vkolla 9
* Vkolla 10 säännöllinen huoltoikkuna
  * tulossa käyttöjärjestelmäpäivityksiä, mahdollisesti pieniä katkoja, jos palvelimet joudutaan käynnistämään uudelleen. 

**Vaara**
* Pyydetty Finnatukea laittamaan päälle asetus, jonka mukaan asiakas voi peruuttaa kuljetettavana olevan varauksen Finnan kautta. Tiedotettu henkilökuntaa asiasta eikä ole tullut ihmettelyä.
* Vaaran next-kannan testausta. Ulkoasu ei ole ihanteellinen huonoine kontrasteineen ja pienine fontteineen. Pitää testata zoomauksen kanssa, miten vaikuttaa näkymiin ja ryhtyä testaamaan myös tikettien mukaisia toimintoja.
* Itsepalvelulainaus tarkoitus laittaa päälle huomenna Kiihtelysvaaran kirjastossa. Kirjautumisongelman syy on selvinnyt (siivousajo) ja se korjataan vasta versionvaihdon jälkeen, joten siihen saakka mennään nykyisellä "virityksellä".

**OUTI**
* Kuljetettavana olevan varauksen peruminen testi-Finnassa:
  * Testeissä ei ongelmia.
  * Kysytty muilta OUTI-kirjastoilta mielipidettä, ne ketkä ovat jo kommentoineet ovat todenneet hyväksi muutokseksi.
* Muuten normaalia tukityötä.

**Helle**
* Lasse lisännyt niteet Porvoon niteettömille artikkeli-tietueille https://github.com/KohaSuomi/Koha/issues/419
* Emmi perunut tietueettomat tilaukset https://github.com/KohaSuomi/Koha/issues/452
* Emmi poistanut vanhat, kevään 2022 epäonnistuneet EditX-sanomat https://github.com/KohaSuomi/Koha/issues/453
* Lisätty maksut näkymään lainaus-sähköpostikuitille ja palautus-sähköpostikuitille Annelin ratkaisulla https://tiketti.koha-suomi.fi/issues/4245

**Vaski**
* Turun pk:n tunneloidut palautusautomaatit lakanneet toimimasta 27.2. iltana. Vian selvittelyä jatketaan, mukana Bittiguru ja Turun tietoliikenne.

**Lappi**
* Rauhallista.
* Tänään Kysy Kohasta -webinaari Lapille: ohjeita, vastauksia ongelmiin ja ärsyttäviin ominaisuuksiin, vinkkejä, teasereita.

**Siilinjärvi**
* Vaihdettu tänään sähköpostiviestien lähettäjäksi noreply@koha-suomi.fi
* Oletusviestiasetusten poisto ei aiheuta meillä ongelmia, tekstiviestitäpät poistettu ja tiedotettu henkilökuntaa, sähköpostitäppiä ei ollutkaan.
* Kuljetustilan poisto Finnassa kiinnostaa myös meitä, työn alle.

**Lumme**
* Oletusviestiasetuksista poistettu valmiit täpät


## Viikko 8 muistio

Aika: 21.2.2023 klo 9.15 <br />
Läsnä: Leena Kinnunen, Pia Kusmin (Lappi), Päivi Knuutinen ja Auli Rantasalo (Vaara), Tuomas Kunttu (Kyyti), Pirkko-Liisa Lauhikari ja Veli-Pekka Marjoniemi (OUTI), Kati Sillgren (Helle), Susanna Sandell (Vaski), Heli Auranen, Katja Valjakka, Timo Pesonen (Lumme)

**Yhteiset**
* Asiantuntijatyöryhmän kokouksesta
  * stafflogininstructions-järjestelmäasetukseen muistutus kirjaston valinnasta, jos työskentelee useammassa toimipisteessä. [Redmine-tiketti #4467](https://tiketti.koha-suomi.fi/issues/4467)
  * [Varausten oletusvoimassaoloaika kolmeen vuoteen.](https://github.com/KohaSuomi/Koha/issues/451)
* Mikä sms-operaattori käytössä?
  * Lappi: Link Mobility
  * OUTI: Link Mobility
  * Siili: Link Mobility
  * Vaara: Link Mobility
  * Lumme: Link Mobility
  * Kyyti: Arena Interactive
  * Helle: Telia
  * Vaski: DNA
* [Redmine-tiketti #4461](https://tiketti.koha-suomi.fi/issues/4461) - onko kommenteissa vielä jotain sellaisia toiveita, joita ei nykyään vielä ole? Jos on, teettekö niistä uudet tiketit tarvittaessa GitHubiin.
* [Ratkaisu ehdotettu -tiketit](https://github.com/orgs/KohaSuomi/projects/4/views/15)
  * 505 - Lapin testaus puuttuu vielä?

**Lappi**
* Rauhallista, valmistaudutaan omaan Kysy Kohasta-webinaariin
* Käyttäjäryhmä aktivoitu, saatu pari jäsentä lisää. 

**Vaara**
* ei mitään erityistä mainittavaa

**Kyyti**
* Kysyin tekstiviestien tuplaviestien poistamisesta. Ominaisuus on siis Kohan yhteisökoodissa.
* Redminen tiketti [#1849](https://tiketti.koha-suomi.fi/issues/1849) vaatisi edelleen huomiota. Anneli ottaa asian esille.
* Olen kirjoittanut tikettiä yhteisön Bugzillaan [#5303](https://tiketti.koha-suomi.fi/issues/5303) ja pyysin että joku kokeneempi katsoisi tekstin vielä läpi.

**OUTI**
* Rauhallista tukityötä.
* Versionvaihdon testaustaulukon kaikki osa-alueet käyty alustavasti läpi.

**Helle**
* Porvoon tunneloidulla palautusautomaatilla oli pakollinen käyttökatko 8.-15.2.2023. Automaatti kuormitti palomuuria muodostamalla jatkuvasti uusia (satoja) yhteyksiä. Tunnelointi rakennettu uudestaan. Tähän osallistuivat: palvelinsalin operaattori, Porvoon IT, Telia.

**Vaski**
* Pohdittiin viestipohjien testausta next-ympäristössä. Testaus todettiin tarpeelliseksi.
* Varausjono-raportin testaustuloksia kaivattiin.

## Viikko 7 muistio

Aika: 14.2.2023 klo 9.15 <br />
Läsnä: Anni Rajala (Vaski), Mikko Liimatainen (Vaski), Susanna Sandell (Vaski), Anneli Österman ja Lari Strand (Koha-Suomi), Kati Sillgren (Helle), Tuomas Kunttu (Kyyti), Heli Auranen, Timo Pesonen (Lumme), Reetta Pihlaja (Siilinjärvi), Pia Kusmin (Lappi), Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Pirkko-Liisa Lauhikari (OUTI)

**Yhteiset**
* Käydään läpi uuden version [uudet ominaisuudet](https://github.com/KohaSuomi/Koha-22x/wiki/Uutta) -listaus. Tallennetaan tämä osio. [Tallenne uusien esittelystä](https://www.youtube.com/watch?v=IUophuEubSM)
* Idea: kerran kuussa esim. klo 13-15 _Bugi-perjantai_, jossa testataan ja sign offataan meille tärkeitä ominaisuuksia/tikettejä. Aloitus versionvaihdon jälkeen. Emmi lupautunut kehittäjistä mukaan, testaajiksi pääkäyttäjiä.
* [Viikon 7 päivitys](https://github.com/KohaSuomi/Koha/discussions/432)
* next-kantojen tilanne
  * datan redusointiskripti melkein valmis
  * ensin tehdään Vaara Annelin pyynnöstä, sitten muut
* [Kohan ohje suomeksi -muotoiluohjeistukset](https://github.com/KohaSuomi/kohasuomi.github.io/wiki/Kohan-ohje-suomeksi--muotoiluohjeistus) tehty. Ohjeita voi noudattaa jo nyt, mutta viimeistään silloin, kun päivitetään ohjeet uutta versiota vastaavaksi.



## Viikko 6 muistio

Aika: 7.2.2023 klo 9.15 <br />
Läsnä: Reetta Pihlaja (Siilinjärvi), Tuomas Kunttu (Kyyti), Christer Skog (Kyyti), Kati Sillgren (Helle), Veli-Pekka Marjoniemi ja Pirkko-Liisa Lauhikari (OUTI), Anneli Österman ja Kodo Korkalo (Koha-Suomi), Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Susanna Sandell (Vaski), Heli Auranen, Timo Pesonen (Lumme), Leena Kinnunen (Lappi)

**Yhteiset**

* Vuosi vaihtunut, onko [Integraatiot-lista](https://github.com/KohaSuomi/Koha/wiki/Integraatiot) ajan tasalla?
* Koha-Suomen nettisivuille siirretty
  * [Tietoturvaohje](https://koha-suomi.fi/dokumentaatio/tietoturvaohje/)
  * [Tietojen säilytysajat](https://koha-suomi.fi/dokumentaatio/tietojensailytysajat/)
* Ei viikkopäivitystä, koska ei ollut päivitettävää
* Keskiviikkona säännöllinen huoltoikkuna, jolloin vaihdetaan palomuurin muistikampoja. Ei pitäisi aiheuttaa katkoksia.
  * Voi vaikuttaa tunneloituihin automaatteihin
* [Finna-kehitysehdotusten](https://github.com/KohaSuomi/Finna-kehitysehdotukset/issues) läpikäynti /Susanna
  * Käytiin läpi kolme ehdotusta ja kirjattiin niihin päätökset.
* [Lapin, OUTIn ja Vaskin action_logs-taulujen korjaukset](https://github.com/KohaSuomi/Koha/issues/403) aiheuttaa viivettä tietojen replikoinnissa masterilta slaveen.

**Siilinjärvi**

* Mikro-Väylä päivittänyt loputkin automaatit viikolla 4 ja lisännyt asetuksiin Sipinstitution id:t
* Ei muuta

**Kyyti**
* On selvitelty ongelmaa, jossa asiakkaalla oli lainassa kirjoja, joita hän ei ollut lainannut. Selityksenä vaikuttaisi olevan, että hänen jälkeensä automaatille tulleen lainaukset ovat kirjautuneet hänen kirjastokortilleen.
* Tehty tiketti [#404 Noutamattoman varauksen määräytyminen nidetyypin mukaan](https://github.com/KohaSuomi/Koha/issues/404)

**OUTI**
* Oulun Finvoice-laskutusprojekti saatu toivottavasti nyt valmiiksi.
* Tuplaverkkomaksuja tulee yhä. OUTIsta laitettu ongelmasta palautetta myös Finna-tukeen. Palautteeseen laitetiin pari esimerkkiä, joissa asiakkaan ja maksun tiedot, tuplamaksujen pvm ja kellonajat.

**Helle**
* Pornaisten kirjaston tunneloitu automaatti poistettu käytöstä. Uusi käyttöön otettu automaatti toimii tietoturvallisesti ilman tunnelointia.

**Vaara**
* Lehtitietueisiin ryhdytty lisäämään luokka, jotta saadaan signumit oikeanlaiseksi.
* Viime viikon keskiviikkona iski hetkellinen paniikki, kun tiketin 232 (Vanhat omatoimikäytön estoblokit tulisi ajaa pois päältä) ajo oli tehty. Vaarassa se tarkoitti kaikkien omatoimikäytön estoa, koska Toveri käyttää tätä toimintoa sallimaan sisäänpääsyn. Onneksi tilanne saatiin nopeasti korjattua, kun huomasin asian.
* Itsepalvelulainaukseen tehty muutos otettu testaukseen, toivottavasti kirjautuminen onnistuu sen myötä.

**Vaski**
* Ei uutta

**Lappi**
* Tätistä valui Celia-tietue valui 6 väärän tietueen päälle, koska TäTin tietueella oli 020a-kentässä tallennettuna
tyhjä välilyönti joka löytyi myös näistä tietueista.

* Tornion asiakas on saanut Finnassa uusiessa lainalle eräpäivän Tornion kiinniolopäivälle.
Remontin takia eräpäivät on muutettu, ja niihin on tulossa vielä uusi ajo.

* OKM-tilasto ajetaan vielä uudelleen, koska Yhteispohjoismaisen auton osalta tarvitaan "autoittain" eriteltynä.
Nyt koottu OKM-ryhmiksi, joista ei saa eri kuntien osalta tuloksia. Tehdään "auto"-kohtaiset ryhmät ja ajetaan OKM uudelleen.

* Kysy Kohasta Lapille 28.2. : kerätty kysymyksiä ja kommentteja Padletilla henkilöstöltä.

* Redminen omat tiketit osittain läpikäymättä, yritetään ennättää hoitaa kuntoon.


## Viikko 5 muistio

Aika: 31.1.2023 klo 9.15<br />
Läsnä: Leena Kinnunen, Pia Kusmin (Lappi), Heli Auranen, Tenho Volanen, Timo Pesonen (Lumme), Päivi Knuutinen ja Auli Rantasalo (Vaara), Veli-Pekka Marjoniemi ja Pirkko-Liisa Lauhikari (OUTI), Anneli Österman ja Emmi Takkinen (Koha-Suomi), Kati Sillgren (Helle), Reetta Pihlaja (Siilinjärvi, paikalla yhteisten asioiden ajan), Mikko Liimatainen (Vaski)


**Yhteiset**
* [Vkon 5 päivitys](https://github.com/KohaSuomi/Koha/discussions/396)
* [Versionvaihtoon keskittyminen](https://github.com/KohaSuomi/Koha/discussions/395)
* [Onko tiketti Koha #311 ok kaikilla?](https://github.com/KohaSuomi/Koha/issues/311)
* Onko kaikki tarkistanut indeksin toimivuuden [tiketin 213](https://github.com/KohaSuomi/Koha/issues/213) muutoksen jälkeen?
* Miten olisi helpointa seurata työn valmiusastetta silloin, kun sama työ tehdään kaikille kimpoille? [Yksi ehdotus](https://github.com/KohaSuomi/Koha/issues/213#issuecomment-1405045158).
  * Ehdotus ei toiminut, koska pääkäyttäjien write-oikeuksilla ei pysty muokkaamaan toisten kommentteja.
  * Emmi löysi ohjeen [GitHubin Task-toimintoon](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/about-task-lists)
  * Sovittiin, että tehdään seuranta niin, että Anneli/joku muu lisää yhden kommentin, jossa tehdään seuranta. Kun asia on omassa kimpassa ok, yksi kimpan pääkäyttäjistä käy peukuttamassa kommenttia, jolloin peukkujen määrästä voi päätellä, onko kaikki tehty.
  * Anneli testaili vielä kokouksen jälkeen ja yhdisti peukutuksen Task-toimintoon näin: ![kuva](https://user-images.githubusercontent.com/33121325/215745423-71572ea9-a647-411e-89d1-659e821de834.png)
  * Anneli tai joku muu admin käy lisäämässä raksit peukkujen perusteella kommenttiin.
* Kun versionvaihdon next-kannat saadaan käyttöön, mitä kantaa Anneli saa käyttää esim. IntranetUserCSS:ien ja IntranetUserJS:ien testaamiseen?
  * Vaara ilmoittautui vapaaehtoiseksi
  * Anneli päivittää [Järjestelmäasetukset-sivulle](https://koha-suomi.fi/dokumentaatio/jarjestelmaasetukset/), mitkä rimpsut toimivat versiossa 22.11.
* Bugin tekeminen yhteisön [Bugzillaan](https://bugs.koha-community.org/bugzilla3/).
  * Rekisteröidy
  * [Yhteisön raportointiohjeistus](https://wiki.koha-community.org/wiki/Bug_Reporting_Guidelines)
  * [Bugzillan ohje tiketin tekemiseen](https://bugzilla.readthedocs.io/en/5.2/using/filing.html#reporting-a-new-bug)
  * [Koha-yhteisön sandboxit](https://wiki.koha-community.org/wiki/Sandboxes)
* Kohan ohje suomeksi - Asiakkaat -> [Rajoitukset-osioon](https://koha-suomi.fi/dokumentaatio/asiakkaat/#1510-rajoitukset) lisätty Tili lukittu ja rajoite moninaisista epäonnistuneista kirjautumisyrityksistä
  * Pirkko-Liisa lisää vielä linkin Lainaus-osiosta näihin ohjeisiin.
* [Nideryhmät versiossa 22.11](https://github.com/KohaSuomi/Koha-22x/wiki/Uutta#nideryhm%C3%A4t) - otetaanko käyttöön ja pyydetäänkö Finnaankin?
  * Toimintoa pidettiin hyvänä, varsinkin jos siihen saadaan yhdistettyä Koha-Suomen tekemänä triggereitä ja ajoa, jotka luovat nideryhmät automaattisesti kausijulkaisutilausten perusteella ja vievät enumchronin perusteella niteet oikeaan nideryhmään.
  * Kysytään Finna-toimistosta, saisiko Finnaankin tuen ainakin varausten tekemiseen. 
  * 
**Lappi**
* Tukipostissa rauhallista
* Koha-käyttäjäryhmän kokous pitkästä aikaa. Päätettiin asetusten käyttöönotosta, osa jo ed. versiopäivityksessä tulleita ominaisuuksia, osa Kirkes-järjestelmäasetusten läpikäynnissä esille tulleita asioita. 
* Tornion kirjasto suljetaan jo ensi viikolla. Muut kirjaston sulkutoimet saatu tehtyä, mutta ongelmana varausten keskeyttäminen ja noutopaikan estäminen, koska ei ole toista toimipistettä, joka voitaisiin Finnassa osoittaa noutopisteeksi. 

**Lumme**
* Uudet OKM tilastot ajettu 30.1.2023
* Lumpeilla jäänyt viestiasetusten defaultteihin sähköposti, jolloin sähköpostikohtiin on tullut täpät myös niille asiakkaille, joilla asiakastiedoissa ei ole sähköpostia. Tästä johtuen on tullut paljon epäonnistuneita viestejä. Tehtäneen massa-ajo, jolla saadaan asiakkaiden asetukset kohdalleen.

**Vaara**
* Kehuja viime viikon päivityksestä eli hyllyvarauslistan sijaintikirjaston korostuksesta. Kuulemma paras muutos aikoihin :)
* ei mitään muuta erityistä mainittavaa

**OUTI**
* Finna-tuesta on tullut vastaus, että varauksen oletusvoimassaoloaika voidaan muuttaa Koha-ajurin asetuksissa. Asiasta lisää asiakaswikissä: https://www.kiwi.fi/display/Finna/Koha-ajurin+asetukset#Kohaajurinasetukset-Varaukset. Oletusvoimassaoloajan muuttaminen kolmeen vuoteen käsitellään seuraavassa asiantuntijatyöryhmän kokouksessa.
* Oulun Finvoice laskutuksessa vielä ongelmana, että niteen viivakoodi ja nidetyyppi saataisiin näkyviin laskulle. Aluksi tiedot olivat ArticleName-tägissä, mutta tägin merkkimäärä ei saa ylittää 100 merkkiä ja jossain tapauksissa näin käy. ArticleDescription-kenttä ei välity laskulle. Nyt Monetralta ovat ehdottaneet, että tiedot laitettaisiin RowFreeText-elementtiin. Testaukset jatkuvat.
* Varauksen tekosivulle lisätty ohjeteksti, kun tehdään nidevaraus: "Valitse noutokirjasto niteen kohdalta, jos teet nidevaruksen". Tekstin voi lisätä CSS:llä. Ohje Redminen tiketissä #5475.

**Kyyti**
* Päivitin uuden tarratulostustiedon Koha-Suomen käyttöohjeisiin https://koha-suomi.fi/dokumentaatio/tyokalut/#12164-tarratulostusty%C3%B6kalu
* Siirtoraportissa oli jotain häikkää, mutta se oikeni päivän kuluessa.

**Helle**
* Porvoon Kerkkoon kirjaston lainoille on tullut lainojen eräpäiviksi kirjaston kalenteriin tallennettuja kiinniolopäiviä. Tämä johtui siitä, että Kerkkoon kirjastosta on lainattu niteitä, joiden sijainkirjasto ei ole ollut Kerkkoon kirjasto. Lainauksessa käytetään niteen sijaintikirjaston kalenteria. Tiketti https://github.com/KohaSuomi/Koha/issues/273 (Tiketissä https://tiketti.koha-suomi.fi/issues/5452 tarkemmin asetusten circcontrol JA homeorholdingbranch arvoihin liittyen.)

**Siilinjärvi**
* Ei mainittavaa.

**Vaski**
* Uuden version testausta aloitellaan
* Tarve saada kuiteille takemmat nimeketiedot. Nämä löytyvätkin nykyään biblio subtitle, part_number ja part_name -kentistä.

## Viikko 4 muistio

Aika: 24.1.2023 klo 9.15<br />
Läsnä: Anneli Österman, Kodo Korkalo, Pirkko-Liisa Lauhikari ja Veli-Pekka Marjoniemi (OUTI), Reetta Pihlaja (Siilinjärvi), Heli Auranen, Katja Valjakka (Lumme), Kati Sillgren (Helle), Mikko Liimatainen (Vaski), Leena Kinnunen, Pia Kusmin (Lappi) 

**Yhteiset**
* [Viikon 4 päivitys](https://github.com/KohaSuomi/Koha/discussions/381)
* OKM-tilastot suurimmalla osalla kunnossa. Osalla kimpoista/kirjastoista on vielä isoja määriä virheellisiä signumeita ja cn_sort-tietoja, jolloin kirjojen jako kauno/tieto-akselilla menee väärin.
  * Näiden etsimiseen ei ole kunnollista raporttia, mutta raportilla [Niteet, joiden cn_sort-kenttä alkaa kirjaimella](https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/Valmiita_SQL-raportteja#Niteet-joiden-cn_sort-kentt%C3%A4-alkaa-kirjaimella) voi selailla todennäköisesti virheellisiä.
* [Häiriö- ja huoltotiedotteet](https://github.com/KohaSuomi/Koha/discussions/categories/huolto-ja-h%C3%A4iri%C3%B6tiedotteet) vastaisuudessa GitHubin discussionsiin omana "aihealueenaan".
* Outlook/Hotmail,complainttaavat asiakkaat, lähtevän postin palvelimen "maine" ja viestien perillemeno / Kodo
  * Microsoftin sähköpostiohjelmissa on jonkinlainen "complain" nappi (en tiedä tarkkaan nimeä, koska minulla ei ole käytössä Microsoftin sähköposteja). Tämän napin painaminen kirjastosta tuleen sähköpostiviestin kohdalla aiheuttaa sen, että viestistä lähtee roskaposti-ilmoitus Microsoftille. Napin painamisesti tulee myös ilmoitus lähettävän palvelimen ylläpitäjälle, eli tässä tapauksessa konesalioperaattorille.
  * Tällaisia "complaitteja" on operaattorin mukaan tullut lähes 800 kappaletta ja ongelma on, että suuret määrät "complaintteja" aiheuttaa konesalioperaattorin lähtevän postin palvelimelle mainehaittaa. Viestien perillemeno hankaloituu ja viestit tulevat luokitelluksi esimerkiksi roskapostiksi tai jäävät kokonaan menemättä perille. Ongelma koskee kaikkien Koha-Suomi kirjastojen lisäksi myös kaikkia muita konesalioperaattorin asiakkaita, jotka käyttävät samaa lähtevän postin palvelinta.
  * Oletuksena oli, että asiakkaat ovat kenties olleet siinä käsityksessä, että "complain" napin painaminen välittyy kirjastojen tietoon ja asiakkaat ovat voineet luulla, että kirjastojen viesteistä pääsee halutessaan tällä tavalla eroon. Näin ei siis kuitenkaan ole, vaan tieto "complaintista" tulee ainoastaan konesalioperaattorille ja Microsoftille. Se ei tule Koha-Suomelle eikä kirjastoille.
  * Ajatus oli lähettää operaattorin palvelimelta "complain" nappia painaneiden asiakkaiden sähköpostiin automaattivastaus, jossa asiakasta olisi ohjeistettu tekemään haluamansa muutokset viestiasetuksiin Finnassa ja neuvottu myös tarvittaessa lisäämään kirjastojen viestien lähettäjä luotettujen lähettäjien listalle. Näyttää kuitenkin siltä, että "complaint" syntyy ainakin joissain tilanteissa jollain tapaa automatisoidusti ja ilman asiakkaan toimenpiteitä, joten automaattivastauksen lähettäminen ei tunnu tarkoituksenmukaiselta.
  * Konesalioperaattori toimittaa listan sellaisten asiakkaiden sähköpostiosoitteista, joiden sähköpostista on lähtenyt "complaint" ja kirjastojen kanssa yhteistyössä sitten voidaan tarvittaessa kontaktoida näitä asiakkaita ja ohjeistaa kirjastojen viestien kanssa toimimisessa.
* Sanaston tilastoajot tehty ja toimitettu

**OUTI**
* Raahen ensimmäiset Finvoice-testilaskut lähetetty Kohasta CGI:n edustapalvelimelle, josta laskujen pitäisi siirtyä Rondoon Siirinetin avulla.
* Oulun aineistovalitsijat ovat pyytäneet, että saisiko hankintaportaalin sanomasta Kohaan tiedon, onko tilattu nide muovitettu vai muovittamaton. Woimalta ovat ilmoittaneet, että heidän puoleltaan tämä onnistuu. Kysytty valitsijoilta, mihin tieto halutaan näkyviin: hankinnan tilausrivin huomautuksiin vai pitäisikö olla nidekohtainen tieto? Jos nidekohtainen tieto, missä sen pitäisi Kohassa näkyä? Pitääkö tiedon olla jotenkin haettavissa? Asia vielä siis selvityksessä.
* Lisätäänkö varausten oletusvoimassaoloaikaa vuosi lisää eli kahdesta vuodesta kolmeen vuoteen? Kukaan ei vastuanut ehdotusta. Pirkko-Liisa kysyy Finna-tuesta, onko lisäys mahdollista Finnassa ja viedään sittten päätettäväksi asiantuntijaryhmään.
* Myös OUTIsta ollaan yhteydessä Finna-tukeen tuplaverkkomaksuongelmasta. Vaarasta Päivi on ollut jo yhteysessä ongelmasta, mutta saanut vähän ynseän vastauksen, että hieman hankala tutkia ja ottaa kantaa, mitä tuplamaksutilanteissa on tapahtunut. Jos Finnan verkkomaksu mahdollistaa maksutapahtuman aloittamisen kahteen kertaan, se pitäisi estää.

**Siilinjärvi**
* Otetaan siirtyminen noreply(at)koha-suomi.fi -viestiosoitteeseen työn alle. Tarkistettiin, että muutos tehdään kirjastoasetuksiin https://koha-suomi.fi/dokumentaatio/asetukset/#1-kirjastot
* Edellisen viikon muistiosta bongattu Haminan kuntaäppi. Siilissä Geniemin kuntaäppi (kirjastokortti + "kevyt" verkkokirjasto) on ollut käytössä noin 3 kk, ja palaute asiakkailta on ollut myönteistä.

**Lumme**
* Okm tilastoraportti ei vielä kunnossa. Varkaudessa signumit väärässä järjestyksessä ja myös muissa kirjastoissa useita väärin tehtyjä signumeita. Kehittäjät yrittävät oikaista.
* Vaihto Noreply-viestivastauksiin mennyt tähän asti hyvin. Kaksi kirjastoa vielä vaiheessa.

**Helle**
* Passiiviset Koha-käyttäjät kirjautuvat nyt automaattisesti ulos aiempaa nopeammin, eli Kohan automaattisen aikakatkaisun aikaa on lyhennetty.
* Ei lainata -nidetilan popuptekstien suurennos on otettu käyttöön.
* Hae tietokannasta -hakuun on otettu käyttöön valmiit valittavat hakukentät.
* Hae asiakkaita -hakuehdoksi on lisätty Matkapuhelin. Lajittelu-hakuehdot on piilotettu käytöstä.
* Asiakastiedon asiakkaan tietoruutu on laitettu näkyville (osoitetiedot eivät näy).
* Asiakaspalvelussa on tullut vastaan asiakastieto (ID 15510), jolle on jäänyt muodostumatta lainan (ep. 4.10.2022) 1. myöhästymisilmoitus 12.10.2022. Kyseisen päivän aamuna on ollut Koha-palvelimien huoltokatko. 

**Vaski**
* Anni tarkistanut Mikroväylän automaattien maksujen erotinmerkin. SipFeesDecimalSeparator asetukseen tulee laittaa piste, jotta maksut tulostuvat kuitille oikein.
* Asiakastietojen inforuutuun toivottaisiin tarkennusta "Tili on lukittu" tekstille. Tekstiin voisi laittaa tiedon liian monesta kirjautumisyrityksestä, mikäli tuota ei käytetä muuhun. Myös ohjeisiin selitys kirjautumisyritysten aiheuttamista lukituksista ja rajoituksista.

**Lappi**
* Rauhallista, ei kummempaa


## Viikko 3 muistio

Aika: 17.1.2023 klo 9.15<br />
Läsnä: Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Anneli Österman, Emmi Takkinen, Tuomas Kunttu (Kyyti), Kati Sillgren (Helle), Pia Kusmin ja Leena Kinnunen (Lappi), Heli Auranen, Katja Valjakka (Lumme), Mikko Liimatainen (Vaski), Pirkko-Liisa Lauhikari ja Veli-Pekka Marjoniemi (OUTI)

**Yhteiset**
* Kohan ohje suomeksi -muotoilujen yhtenäistäminen?
  * työryhmä miettii yhtenäiset muotoiluohjeet: Päivi, Tuomas, Anneli
  * jos joku vielä haluaa mukaan, ilmoita Annelille.
    * Kinnusen Leena ilmoittautui jälkikäteen mukaan 
* [Viikon 3 päivitys](https://github.com/KohaSuomi/Koha/discussions/369)
* Githubin esittelyvideot [kaikille](https://youtu.be/cPVSi2xFBIQ) - [pääkäyttäjille](https://youtu.be/J-lzJv7ginE)
* [Kirkesin järjestelmäasetusten läpikäynti, osa 1](https://youtu.be/lyETIF-Xd2Y)
* Tilastoinnissa virhe [KPOKM-5](https://github.com/KohaSuomi/koha-plugin-OKM-stats/issues/5) /Emmi
  * Emmi korjaa virheen ja tiedottaa, kun tilastot on luotu uudelleen.
  * Tätissä on [SQL-kysely](https://tati.koha-suomi.fi/cgi-bin/koha/reports/guided_reports.pl?phase=Run+this+report&reports=243&limit=200), jolla voi hakea tietueet, joissa luokka alkaa kirjaimella. 
* Redmineen kirjautuminen otetaan pois päältä muilta kuin pääkäyttäjiltä.
* [Asiantuntijaryhmän kokous](https://koha-suomi.fi/asiantuntijaryhma2023#asiantuntijaryhm%C3%A4n-muistio-123)
  * [Finna-kehitysehdotukset](https://koha-suomi.fi/asiantuntijaryhma2023#2-finna-kehitysehdotukset)
  * [Infoboksin piilotuksen poisto](https://koha-suomi.fi/dokumentaatio/intranetusercss/#asiakkaan-tietoruudun-piilotus-asiakastiedoista-vasemmasta-reunasta)
    * Tarkista, että HidePersonalPatronDetailOnCirculation asetus on päällä

**Vaara**
* Tuplaverkkomaksuja oli lopulta vain kourallinen, neljä oikeasti tuplasti maksettuja (suuruudeltaan 1,80-5,25 euroa). Toivotaan, että näitä ei tule enempää.
* Joensuun kaupunki ilmoitti perjantaina iltapäivällä, että Ceepos-kassaan kirjautuminen muuttuu (kysyy käyttäjätunnusta). Tieto ei tietenkään kulkeutunut lauantaina työskenteleville, joten kassa pysyi kiinni. Täytyy antaa palautetta muutosten ajankohdan suunnittelusta.

**Lumme**
* Varkaudessa huomattiin OKM tilaston epäonnistuminen vuodelta 2022. Kehittäjät korjaavat tilastot maanantaihin 23.1. mennessä.
* Normaalia ylläpitoa.

**Kyyti**
* CD-levyjen laina-aikaa pidennettiin 28 vuorokauteen viime viikolla.
* Haminan kaupunki on toteuttanut mobiiliapplikaation, jossa on myös sähköinen kirjastokortti sekä tiedonhaku, varaus ja lainojen uusinta. Rajapinta Kohaan on tehty. Löytyy sovelluskaupoista Hamina-haulla.

**OUTI**
* Verkkokirjastossa oli viikonloppuna la-yönä ja su-aamupäivällä jumitilanne, joka aiheutti sen, etteivät asiakkaat saaneet palvelussa näkyville omia lainoja ja varauksia. Ongelman aiheutti arkistointiajon jumiutuminen. Sama ongelma oli myös Vaskissa ja Lapissa.
* Tuplaverkkomaksujen (10 kpl) aiheuttajan selvittäminen vielä vaiheessa.
* Raahen finvoice laskutuksen testaukset ehkä alkamassa lähiaikoina. Oulun laskutuspohjassa vielä vähän säätöä.
* Oulun Byströmin nuorten palvelun kokoelma (alle 1000 nidettä) tulossa käyttöön koko OUTIlle.
* Oulun omatoimikirjastojen laitteistoja vaihdetaan Mikro-Väylän laitteista Lyngsoin laitteisiin.

**Helle**
* Finna-toimisto ilmoittanut yhdestä verkkomaksusta, joka ei ole poistunut Kohasta.
* Niteet/Näytä niteen lainahistoria -tiedosssa ihmetyttänyt Viimeisin havainto -kentän aika, joka on versionvaihtopäiväyksen ajalta: 7.6.2022 12:59. Sama tieto on sekä niteen sijaintikirjastolla (Tesjoki) että kotikirjastolla (Loviisa). Esim. nide itemnumber=1418340, joka on ollut saatavilla versionvaihdon aikaan.
* Onkohan Kohasta toimivaa rajapintaa Konica-Milton-tulostuspalvelulle? Palaverissa saatu tieto: Jos nykyiset Kohan rajapinnat eivät ole yhteensopivia, vaatii rajapinta Koha-kehitystä. Kouvolassa on käytössä Canon-tulostuspalvelu ja Kohan rajapinta toimii.
* Mikä onkaan käytäntö muilla kimpoilla e-palveluihin kirjautumiseen silloin, kun kyseessä on esim. yhteisöasiakas (ei henkilöasiakas)?
* Ehdotettu, että OKM-tilastoinnin kauno/tieto-jaottelu perustuisi niteen luokkaan eikä tietueen luokkaan. Kokouksen jälkeen katsoin, mitä OKM-ohjeistus kertoo:  Kirjat jaetaan aikuisten sekä lasten ja nuorten kauno- ja tietokirjoihin kunkin kirjaston oman käytännön mukaan.
Tieto mainitaan (ainakin) kohdassa 3 Aineistot ja kokoelmat, Kauno ja tietokirjat sekä kohdassa 4 Aineisto: lainaus
https://www.kirjastot.fi/sites/default/files/content/Yleisten_kirjastojen_tilasto-ohjeet_2022_0.pdf

**Lappi**
* Ceepos-kassasta tulee ylimääräisiä maksujen poistoja. Onko vika kassassa vai käyttäjässä? Ongelma vielä selvityksessä. Todennäköisesti käyttäjässä, ohjeistetaan uudelleen.
* Valmistelussa Kysy Kohasta -tilaisuus Lapin henkilökunnalle sekä Kohan käyttäjäryhmän kokous. 

**Vaski**
* Raportteja siivotessa ihmetelty Antin tekemiä raportteja ja mietitty onko ne tehty jostain yhteisestä tarpeesta.
* Versiopäivityksen testikannasta kiinnostaa tuleeko data anonymisoituna.
* Finnan maksuongelmat selvityksessä. Ilmeni, että ongelma johtui maksujen pyöristyksestä.

## Viikko 2 muistio

Aika: 10.1.2023 klo 9.15<br />
Läsnä: Anni Rajala (Vaski), Leena Kinnunen ja Pia Kusmin (Lappi), Heli Auranen, Timo Pesonen (Lumme), Reetta Pihlaja (Siilinjärvi), Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Veli-Pekka Marjoniemi (OUTI), Tuomas Kunttu (Kyyti), Anneli Österman ja Kodo Korkalo (Koha-Suomi), Johanna Miettunen (3AMK), Kati Sillgren (Helle)

**Yhteiset**
* [Vkon 2 päivitys](https://github.com/KohaSuomi/Koha/discussions/357)
* Keskiviikon huoltokatko / Kodo
  * Huoltokatkon aikana vaihdetaan viallisia muistikampoja. [Toimintasuunnitelma](https://koha-suomi.fi/kohasuomi2023#tammikuun-huoltokatkon-toimintasuunnitelma) 
* Keskiviikon Kirkes-kimpan järjestelmäasetuskoulutus siirretty puoli tuntia myöhemmäksi ja Jitsiin. Uusi aika ja paikka päivitetty [koulutustiedotteeseen](https://github.com/KohaSuomi/Koha/discussions/320).

**Vaski**
* Vaski-tasoinen kellutuskokeilu aloitettu eilen, kokeilussa kellutetaan vain musiikki cd:itä.
* Havaittu, että tilaussanoman käsittely epäonnistunuu välillä ensimmäisellä yrityksellä (https://github.com/KohaSuomi/Koha/issues/353). Tätä saatu jo selviteltyä ja liittyy ilmeisesti ElasticSearch-ongelmaan.


**Lappi**
* Ylimääräisiä tuplasti veloitettuja maksuja 37 kpl, muutama Finnasta ja enemmän Kemin Ceepokselta. Liittynee tikettiin #351
* Muistutettu varalainausjärjestelmästä, suositeltu KOCT:ia. Yhdellä tunnuksella pääsy ei onnistu. 
* SMS-numeron siirto Finnasta Kohaan toimii, korjattu myös mobiilinumeron kopioituminen mobile-kentästä sms-kenttään
* Kerätään kysymyksiä, ei toimivia ja toimivia juttuja Kohasta käyttäjiltä helmikuun lopun Kysy Kohasta-webinaariin
* Virkailijaoikeuksia tarkistettu, mutta ongelmana  raportit, jotka antavat liikaa tietoa

**Lumme**
* vanhentuneet varaukset eivät poistu - satunnainen mutta toistuva ongelma#356. Tehty tiketti 9.1., Emmi hoitaa asiaa
* Asiakkaalla näkyi Palautusilmoitukset välilehdellä palautusilmoituksia. Väittää palauttaneensa toiminto (https://tiketti.koha-suomi.fi/projects/versionvaihto/wiki/Uusia_ominaisuuksia#Ilmoittaa-palauttaneensa-toiminto). Piilotus Intranetusercss  /*Piilotetaan asiakastietojen sivulla näkyvä 'Palautusilmoitukset' nappula (eng. 'Claims')*/ ul.nav.nav-tabs li a#return-claims-tab { display:none;}

**Siilinjärvi**
* ei mainittavaa

**Vaara**
* Myös Vaarassa tuplasti veloitettuja/kuitattuja maksuja eli asiakkailla plussaldoa.
* Muuten normaalia ylläpitoa.

**OUTI**
* OUTIssa myös tuplasti veloitettuja maksuja, asia selvityksessä.
* Henkilökunnalta kyselyä liittyen ongelmiin kausijulkaisujen vastaanottamisessa tilauskauden päättymisen jälkeen. Ratkaisuna tilauskauden jatkaminen.
* Muuten normaalia ylläpitoa.

**Kyyti**
* Keskusteltiin pitkään maksuista, jotka asiakkaat ovat maksaneet kahteen kertaan Finnassa. Toistaiseksi näitä lienee syytä seurata raporteilla.
* CD-levyjen laina-aika muuttuu. Tehty tiketti #358 nidetyyppimuutokselle.

**Helle**
* Koha-näytön yläreunaan lisätyt omat linkit eivät ole enää päällekkäin pienemmillä näytöillä, kun osa omista linkeistä niputettiin samaan alasvetovalikkoon. 

## Viikko 1 muistio

Aika: 3.1.2023 klo 9.15<br />
Läsnä: Päivi Knuutinen, Irina Halminen ja Auli Rantasalo (Vaara), Heli Auranen, Katja Valjakka, Timo Pesonen (Lumme), Reetta Pihlaja (Siilinjärvi), Piia Semenoff ja Veli-Pekka Marjoniemi (OUTI), Anni Rajala (Vaski), Leena Kinnunen, Pia Kusmin (Lappi)

**Yhteiset**
* Tikettien label "enhancement" on jaettu "kahtia", jotta erottaa paremmin ne kehitysehdotukset, joiden kehitys on asiantuntijaryhmässä päätetty tehdä yhteisössä oman työn sijaan.
  * local enhancement -> kehitys tehdään itse
  * community enhancement -> kehitysehdotus viedään yhteisön bugzillaan.
    *  työnjakoasia: voisiko alkuperäinen tiketin tekijä tehdä bugi-ilmoituksen myös bugzillaan? Päätös: alkuperäinen tiketin tekijä tekee, muut auttaa tarvittaessa.
* [Varauksen tiedot lokilla](https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/Valmiita_SQL-raportteja#Varauksen-tiedot-lokilla) -raportin kuvaus päivitetty vastaaman nykyversiota.
* [Viikon 1 päivitys](https://github.com/KohaSuomi/Koha/discussions/347)
* Kaikki kimpat käy läpi tammikuun loppuun mennessä Redminessä Palaute-projektissa olevat tiketit ja sulkee valmiit ja sellaiset, jotka eivät ole enää ajankohtaisia. Lopuista katsotaan, mitkä kannattaa siirtää uusiksi tiketeiksi GitHubiin.

**Vaara**
* Kysymys Finnassa tapahtuneista varauksista ja niiden poistumisesta muilta kimpoilta. Ainoastaan Lapissa oli vastaava tapaus viime viikolla. Tutkitaan vielä asiaa.
* Ei muuta mainittavaa, vuoden viimeinen viikko oli rauhallinen.

**Lumme**
* Kirjeitä jumittunut 20 lokakuulta asti, lähetetty 14.12. ja myöhemmin muodostuneet kirjeet.
* Suomenniemen toveriin uudet aukiolot. Hypernovalta ei ole tullut blugaria Lari tekee Lumpeille oman.
* Toenperän kirjastojen erottaminen toisistaan tehty Finnassa, kohassa vielä vähän vaiheessa. Kirjastoauto Jasso jatkaa entisten Toenperän kuntien palvelemista.

**Siilinjärvi**
* Tavoitteena tänä vuonna saada käyttöön verkkomaksaminen. Aloitettu vanhojen laskutus- ja perintämappien perkaaminen ja tietojen siivous Kohasta. Kaikenlaisia maksuja sitä löytyykin!

**OUTI**
* Käyttösääntömuutoksia tehty Kohaan
  * uusintojen määrä laskettu 10 -> 7
  * konsolipelien lainamäärä nostettu 2 -> 4 eli asiakas voi lainata nyt yhteensä 8 peliä, jos lainaa 4 lasten konsolipeliä ja 4 aikuisten. Aiheuttaa henkilökunnassa keskustelua.
* Omatoimikirjastojen erä- ja noutopäivä ylityksiä vähennetty tälle vuodelle. Aiheuttaa henkilökunnassa keskustelua.

**Vaski**
* Ei erityisiä kuulumisia. Asiakaspalvelusta tiedusteltu, poistetaanko vanhentuneet maksamattomat automaattisesti. Siivousajoa ei vielä ole käytössä ja se edellyttää huolellista suunnittelua, Anneli vie asian eteenpäin kehittäjien viikkopalaveriin.

**Lappi**
* Rauhallinen vuodenvaihde.
* Käyttäjäoikeuksista on ollut kaksi raporttia, toisella voi hakea kaikkien käyttäjien kaikki oikeudet ja toisella oikeusryhmittäin. Rapsat menneet ilmeisesti rikki edellisessä päivityksessä. Vaaralla ilmeisesti näistä toimiva versio? Lari lupasi katsoa Lapin raportteja. 
* Työn alla käyttäjätunnusten tarkistus, aloitetaan vanhentuneiden maksujen poisto. 

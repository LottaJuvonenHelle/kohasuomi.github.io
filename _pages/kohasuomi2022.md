---
title: 'Koha-Suomen vuoden 2022 muistiot'
header:
  overlay_color: '#5e616c'
  overlay_image: /assets/images/cropped-pexels-photo-113850.jpeg
permalink: /kohasuomi2022
redirect_from:
  - /theme-setup/
toc: true
layout: single
hidden: true
---

Kehittäjien viikkopalaverit vuodelta 2022.

## Viikon 52 muistio

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-52-muistio

Aika: 29.12.2022 klo 10
Läsnä: Anneli, Pasi, Ari, Kodo, Lasse, Emmi, Lari

### Torstain palaveri

* Päivystysvuorot viikosta 1 alkaen

* Viikon 1 päivitys
  * [KohaSuomi/Koha #331](https://github.com/KohaSuomi/Koha/issues/331) Suojatut kentät näkyvät tyhjinä z39.50-haulla tietueita korvattaessa
  * [KohaSuomi/Koha #334](https://github.com/KohaSuomi/Koha/issues/334)
  * SQL-raportit hakemaan slave-kannasta masterin sijaan, jotta vältytään tietokannan taulujen lukkiutuminen raskaissa kyselyissä sekä master-kannan kuormaa saadaan kevennettyä.

* [KohaSuomi/Koha #308](https://github.com/KohaSuomi/Koha/issues/308) Tietueen Varaukset-sivulla asiakas-sarakkeen tietoja ei ladata jos käyttäjältä puuttuu edit_borrowers-oikeus /Emmi
  * Onko ok vaihtaa endpointin tarvitsema permission view_borrowers_from_any_library?
  * Tuodaan korjaus yhteisöstä testattavaksi

* Lumpeissa kirjeviestit ei ollut lähtenyt pariin kuukauteen zippitiedoston luonnissa olleen virheen vuoksi.
  * kirjeet lähetetty uudelleen

* Vaskissa oli viikolla 51 kaksi kertaa katkos ti-ke. Katkos todennäköisesti johtui siitä, että yhtä raskasta kyselyä ajoi yhtä aikaa useampi henkilö.
  * altdbh:ta ei ilmeisesti ole portattu nykyiseen versioon, eli raportit ajetaan masterissa eikä slavessa.

* Muistiot viikosta 1 lähtien [githubissa](https://github.com/KohaSuomi/kohasuomi.github.io/blob/master/_pages/kohasuomi23.md) eli [Koha-Suomen sivuilla](https://koha-suomi.fi/kohasuomi23]

[Palaa muistion alkuun](https://koha-suomi.fi/kohasuomi2022#viikon-52-muistio) | [Palaa sivun alkuun](/kohasuomi2022)


## Viikon 51 muistio

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-51-muistio

### Maanantain palaveri

Aika: 19.12.2022 klo 10
Läsnä: Ari, Anneli, Emmi, Kodo, Lari, Lasse, Pasi

* Viikon 51 päivitys (mahdollisesti):
  * [KohaSuomi/koha-plugin-overdue-tool #39](https://github.com/KohaSuomi/koha-plugin-overdue-tool/issues/3) Laskutettujen niteiden määrän ja laskutetun aineiston yhteissumma ei aina täsmää
  * [KohaSuomi/Koha #233](https://github.com/KohaSuomi/Koha/issues/233) Hyllyvarausraporttin On-shelf-sarakkeen JA Varaus-sarakkeen kirjastotunnus-arvon korostus silloin, kun kirjastotunnus löytyy molemmista sarakkeista- Ei mene tämä vielä, koska vaatii at-ryhmän päätöksen. Seuraava kokous 16.1. eli mennee viikon 3 päivitykseen.

* Valutuksessa otetaan käyttöön uusi versio Melindan rajapinnasta
  * Vaatii meidän päässä vain endpointin urlin vaihtamisen Tätin Biblio exporter palveluun (tati.koha-suomi.fi/service). 
  * [Ohjeet urlin vaihtoon täällä]"https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/KohaSuomiServices-mikropalvelu#Biblio-exporter".

* Asiantuntijaryhmässä käsiteltyjen kehitysehdotusten aikataulutus ja vastuutus

* SIP2oHTTP(s) Proxy starttipalaverin aikataulutus ja kutsuminen koolle

### Torstain palaveri

* "Yhteystiedot lisätty Koha-Suomen nettisivuille":https://koha-suomi.fi/yhteystiedot
  * Kuvat kaikista? Kuvaamossa?
  * [Githubin wikissä pääkäyttäjien (ja meidän) yhteystiedot](https://github.com/KohaSuomi/Koha/wiki/Koha-yhteystiedot)

* Tehdäänkö viikolla 52 viikkopäivitystä? Ei tehdä.

* Sanaston raportit vuodelle 2022, tammikuun 16. pvä mennessä, vaatii edellisen raporttiskriptin tuonnin, tuodaan koha-suomi-utility -repoon, Pasi hoitaa.

* Versionvaihto repo tehty

[Palaa muistion alkuun](https://koha-suomi.fi/kohasuomi2022#viikon-51-muistio) | [Palaa sivun alkuun](https://koha-suomi.fi/kohasuomi2022)


## Viikon 50 muistio

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-50-muistio

Aika: 12.12.2022 klo 12
Läsnä: Ari, Anneli, Emmi, Kodo, Lari, Lasse, Pasi, Oskari

### Maanantain palaveri

* "KohaSuomi/Koha #294":https://github.com/KohaSuomi/Koha/issues/294 TUVR-yksikön voimassa olevien varausten keskeytys määräajaksi
  * Määräaika 14.12.

* Vko 50 päivitys
  * Otetaan käyttöön valutuspalvelun keskeytys yön ajaksi. Kodo hoitaa.

### Torstain palaveri

Läsnä: Anneli, Ari, Emmi, Kodo, Lari, Lasse, Pasi

* Tikettien seuranta -projekti julkiseksi?
  * virkailijoiden (ja tieteellisten) helpompi seurata tikettejä ilman, että joutuvat rekisteröitymään
  * Päätös: muutettiin julkiseksi

* Kuvailuryhmän muistiot
  * kuinka tiukasti muistio-sivun päivitysoikeuksia saa rajattua? Kuvailijoilla kiertävä sihteerivuoro, eli kaikkien pitäisi pystyä päivittämään muistioita.
  * Päätös: laitetaan Koha-Suomen sivuille samaan paikkaan kuin muutkin ja samalla tavalla. Anneli selvittää, voisiko päivityksen tehdä pääasiassa esim. Knuutisen Päivi (jo päivitysoikeudet) ja Heikkisen Antti (ei vielä päivitysoikeuksia)

* Itsepalvelun timeout
  * Itsepalvelu kirjautuu ulos yön aikana

* tietueen erämuokkauksessa outissa lisätty kenttä menee oikeaan kohtaan, hellessä esikatselussa viimeiseksi. #4964
  * Pasi tutkii

* Asiakkaille vain koosteviestejä #5269
  * tehdään vkon 51 päivityksen yhteydessä
  * Tiketissä oleva triggeri tuotantoihin
  * Täppien ajo updateilla vanhoille asiakkaille
  * Ei-digest transporttien poisto Koha-kannoista, jotta Finna ei mahdollista koostetäpän poistamista, nykyinen taulu kannattaa ottaa talteen varmuuden välttämiseksi

* Suomi.fi palaveri
  * XML+PDF/SFTP siirtotavasta poistumassa mahdollisuus olla lähettämättä paperikirjeitä
  ** kirjastojen kannalta tilanne on hankala, koska Suomi.fi postituspalvelun käyttöönotosta tarvittaisiin päätös kustakin kimpan kunnasta
  ** Suomi.fi ei mahdollista paperikirjeiden lähettämistä hetuttomille asiakkaille, joten johtaisi kahteen päällekkäiseen sopimukseen (kimppojen oma ja suomi.fi)
  ** myös sopimustekniset asiat voivat sitoa kuntien/kimppojen käsiä tässä
  * VIA ei jatka REST-rajapintansa ylläpitoa/kehittämistä, ainoaksi mahdollisuudeksi jää WebServices jos ei haluta lähettää kirjeitä
  ** WebServices on testaamaton ja tekniseltä toteutukseltaan epätyydyttävä (mm. erillinen Java-kielinen signer-moduli tarvitaan)
  * Palaveri Suomi.fi väen kanssa asiasta maanantaina 19.12. Ari, Anneli, Kodo ja Knuutisen Päivi paikalle.

* "KohaSuomi/Koha #295":https://github.com/KohaSuomi/Koha/issues/295 Vaski: okm-tilastovääristymän korjaaminen  

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-50-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikon 49 muistio

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-49-muistio

Aika: 5.12.2022 klo 10
Läsnä: Anneli, Ari, Emmi, Kodo, Lari, Pasi


  *Maanantai  *

* Tilastointipalaverissa (29.11.) esiin nousseet asiat
  * Hätyytellään vielä kertaalleen, että tunnus tarvitaan.

* Konversiot (Kirkes ja vähän muutkin tulevat)
  * bulkmarcimport menee uusiksi ja samalla kaikki muutkin meidän omat bulk*import -skriptit, eli koko import-ketju täytyy suunnitella ja koodata uusiksi versiovaihdoksen jäljiltä.
  * Jos yritettäisiin päästä tässäkin mahdollisimman lähelle yhteisöversiota, eli luovutaan bulkmarcimportia lukuunottamatta import-työkaluista ja tuodaan data kantaan suorina sql insertteinä.
  ** Pitäisi toimia, on tehty ennenkin mm. Kyytin ja Lumpeen konversioiden aikana, mutta ei kyllä ole testattu pitkään pitkään aikaan.
  ** Kuinka paljon bulkmarcimportin Koha-Suomi (oplibmatcher, preserve biblionumber, component parts) ja kansalliskirjasto (holdings-tuki) ominaisuuksista tarvitaan edelleen mukaan.

* Bibliografisten tietueiden deduplikointi konversioissa
  * Deduplikointi ei ole ongelma Kirkeksessä, koska kyseessä on kokonaan uusi Koha-installaatio, jatkossa tuotaessa uusia kirjastoja entisten kimppojen osaksi tämä on kuitenkin viimeistään ratkaistava.
  * Oplibmatcher toimii Zebran varassa, joten ei ole ElasticSearchiin vaihtamisen jälkeen enää ollut käyttökelpoinen.
  * Konversiovaiheessa deduplikaatiotauluja vasten vai import-vaiheessa ISBN/standarditunnisteet, samaan tapaan kuin valutus ja EDItX?
 
* Pitäisikö pyrkiä Aurora-konversioissa ensisijaisesti säilyttämään Aurora ID:t, jolloin niistä tulisi suoraan Kohan biblionumbereita, borrowernumbereita ja itemnumbereita?
  * Vanhassa Koha-Suomen bulkmarcimportissa tämä on toteutettuna Vaski-konversion ajalta, eikä luultavasti ole kovin vaikea portattava uuteenkaan versioon.
  * Helpottaisi datan yhdistelyä kannassa import-vaiheessa ja mahdollisesti nopeuttaisi jonkin verran datan tuontia Koha-kantaan, PAITSI jos ollaan tuomassa dataa vanhaan kantaan ja biblionumberit, itemnumberit ja borrowernumberit joudutaan muuttamaan.
  * Finna-listat ym säilyisivät automaattisesti toimivina.

* Päivystäjät, muistakaa ajaa service-checkit aamuisin ja korjata mahdolliset ongelmat.

* Discussions -githubissa

* Nalkutin laitettu päälle Tätissä.
  * ohitetaan seuraavat kentät: 09x,046z,59x,880,9xx,xxx9,8565,579
  * 046z tämän vuoksi: https://tiketti.koha-suomi.fi/issues/5404

  *Torstai  *

* ma 12.12. asiantuntijaryhmän palsu klo 9, pitäisikö siirtää KS-palsu myöhemmäksi?
  * Siirretään klo 12

* onko vuodenvaihteessa tehtäviä hommia?
  * Anneli kysyy pääkäyttäjiltä

* Githubin testijakso päättynyt, pääkäyttäjät eivät nähneet estettä tikettien osalta siirtymiseen Redminestä Githubiin.

* "Vuoden 2023 muistioille":https://koha-suomi.fi/muistiot koti

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-49-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikon 48 muistio

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-48-muistio

Aika: 28.11.2022 klo 10
Läsnä: Ari, Emmi, Kodo, Lari, Pasi

* Viikon 48 päivitys
  * "KohaSuomi/Koha #269":https://github.com/KohaSuomi/Koha/issues/269 Käännösmuutos vahvista lainaus popuppiin

### Torstain palaveri

* "Koha 22.11 julkaistu":https://koha-community.org/koha-22-11-released/ -> versionvaihdon käynnistys

* Päivystysvuorot viikosta 49 alkaen
  * Emmi ja Kodo
  * Pasi ja Anneli
  * Lari ja Emmi

* Raision epäonnistuneita laskupaketteja päätynyt Suomen Kuntaperinnälle 

* Viikon 50 päivitys
  * Viikon 49 päivitys ohitetaan itsenäisyyspäivän vuoksi.
  * https://github.com/KohaSuomi/koha-plugin-ceepos-integration/issues/1
  * https://github.com/KohaSuomi/Koha/issues/204

* Tikettien työnkulku https://github.com/KohaSuomi/Koha/wiki/Tikettien-ty%C3%B6nkulku
  * "Valmis" -> "Suljettu", koska välttämättä mitään ei tehty?

* Salasanasuojatut raportit ja tiivisteiden laskenta, esimerkiksi https://vaski-test.koha-suomi.fi/cgi-bin/koha/reports/guided_reports.pl?reports=2182&phase=Edit%20SQL
  * Komentoriviltä: echo -n "salasana" | md5sum (-n on tärkeä, koska se estää echoa tuuppaamasta ylimääräistä enteriä salasanan loppuun ja muutamasta tiivistettä aivan toiseksi kuin on tarkoitus)
  * MariaDB clientissa: select md5('salasana');
  * Kodo tekee tiivistelaskurin tallennettuihin raportteihin.

* Suomi.fi viestitestaukset keskiviikkona 30.11.
  * 3.8. tullut puutteellisia viestejä, miksi?
  * NoSendOC_Edita ei kuulemma ole tarkoitettu tuotantokäyttöön, mutta se on silti tuotantokäytössä muutamassa paikkaa (mm. meillä)

* Backuppitila konesalissa
  * /home/[tunnus]/backup
  * Ohjeet principiossa (tosin suppeat)

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-48-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikon 47 muistio

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-47-muistio

Aika: 21.11.2022 klo 10
Läsnä: Emmi, Kodo, Lari, Pasi

* Raision Finvoice-laskut eivät lähde eteenpäin  
  * Syynä mitä luultavammin se, että Svean päässä on säädetty hakemisto-oikeuksia. Pyydetty Vaskin pääkäyttäjiä olemaan vielä yhteydessä Sveaan ja varmistamaan tämä.
* "KohaSuomi/Koha #215":https://github.com/KohaSuomi/Koha/issues/215 Kuvailupohjiin käyttöön 942$b-kenttä
  * Ehtiikö tämän viikon päivitykseen?
  * Pasi hoitaa.

* Viikon 47 päivitys:
  * "KohaSuomi/koha-plugin-overdue-tool #2":https://github.com/KohaSuomi/koha-plugin-overdue-tool/issues/2 Laskutusliitännäiseen lisätty tieto laskutettujen niteiden määrästä ja laskutetun aineiston kokonaissumma

### Torstain palaveri

* Päivystys
  * Pyritään järjestämään niin, että päivystysparina on aina työnsä aamulla aloittava ja toisena illemmalle työskentelevä.  
  * Puhelin ohjataan sen viiko ns. päpäivystäjälle (kalenterissa ensimmäisenä oleva nimi)
* Lomat
  * Jokainen merkkaa ehdotuksensa kalenteriin
* Viikon 48 päivitys

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-47-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikon 46 muistio

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-46-muistio

Aika: 14.11.2022 klo 10
Läsnä: Ari, Anneli, Emmi, Kodo, Lari, Pasi

* Emon ja osakohteiden valutus
  * Tällä hetkellä Kohan päässä emon valutus vetää mukaan myös osakohteet (vaikkei tälle olisi välttämättä tarvetta), tähän olisi tarvetta yrittää saada muutos.
  * Otetaanko meillä työn alle? Kuka tekee? Millä aikataululla keretään?
  * Päätös: otetaan työn alle viimeistään sitten, kun Johanna palaa hommiin.

### Torstain palaveri

* Versionvaihdon tiketöinti
  * riittääkö pelkkä projekti vai pitääkö tehdä erillinen repositorio?
  * Päätös: tehdään sekä uusi repositorio että projekti.
  * Anneli tekee projektin, Kodo tekee repositorion

* #5600 ilmeisesti kesken Johannalla
  * Emmi tutkii

* koulutusten tallentaminen jatkossa

* Viikon 47 päivitys

## Laina- ja maksusääntöä ei voinut poistaa

Kohan ylläpidossa ei voinut poistaa laina- ja maksusääntöä. Ongelma johtui Koha-Suomen lisäämästä varauksen noutoaika -sarakkeen puutteellisesta käsittelystä. Ongelma on nyt korjattu.

!{width:45%}lainasaannot8.png!

Liittyy Github-tikettin "Koha #259":https://github.com/KohaSuomi/Koha/issues/259

#lainajamaksusäännöt #ylläpito

## Perustiedot-näytölle muutoksia

Perustiedot-näytölle tulee parannuksia. Näkyville tulee mm. aineistotyyppi

#4592 eli tietuenäytön muutokset
* Kansikuvien haku ei enää hidasta hakutuloksia samaan tapaan kuin ennen.

## Niteen sublocation-arvon kuvaus autorisoiduista arvoista näkyville Finnaan.

Finnaa varten on tehty plugin (Authorised values endpoints) joka tarjoaa Finnalle selkokieliset kuvaukset sublocationeista. Finna käyttää tätä tietoa jatkossa näyttääkseen niteen sublocationin kuvauksen autorisoiduista arvoista niteen tiedoissa.
Lisätään tuotantoihin tiistaina 22.11. Finnoihin tehdään sen jälkeen muutos heidän aikataulullaan.

Liittyy redmine-tikettiin:https://tiketti.koha-suomi.fi/issues/5476

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-46-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikon 45 muistio

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-45-muistio

Aika: 7.11.2022 klo 10
Läsnä: Ari, Anneli, Emmi, Kodo, Lari, Pasi

* "strategiapajan yhteenvedon anti":https://tiketti.koha-suomi.fi/attachments/5663/Koha-SuomiOystrategianarviointi2022.pdf
  * päivystävä kehittäjä pääkäyttäjien palaveriin
  * Ari keskustelee yhteisestä kehittäjäpalaverista Kansalliskirjaston kanssa
  * Kodo mukaan asiantuntijaryhmän kokouksiin

* raportterin siirrin eli miten Raportointipalveluun siirretään data
  * Lari tiedustelee tilannetta

* Viikon 45 päivitys
  * #4234 - Finna-pluginiin lastseen-arvon päivitys
  * Github-tiketti 242 - käännösmuutos
  * Hyllyvarausraportin päivitys, no hold allowed. Github-tiketti 226.
  * Aineistotyyppi lainaukseen ja palautukseen, jos ehditään tekemään muutos, että näytetään auktorisoidun arvon kuvaus. G-238
  * https://github.com/KohaSuomi/Koha/issues/213?
  ** tehdään ensin Siiliin uudelleenindeksointi, sitten muille
  * Muutetaan TäTin tietueiden valutusta ja valmistaudutaan valutuksen keskeyttämiseen yön ajaksi. Yöllisistä valumisista on ollut ongelmia.
  * https://github.com/KohaSuomi/Koha/issues/207

* Versionvaihdot-projektissa 16 avointa tikettiä. Muut suljettu tai siirretty muihin projekteihin. Loppujen tilanne?
  * Käydään läpi torstain palaverissa.

### Torstain palaveri

* Viikon 46 päivitys

Hyllyvarausraportti

Hyllyvarausraportin taustalla on ajo, joka kerää raportin tarvitsemat tiedot ajastetusti. Jos ajo ei ole päällä ja yrittää hyllyvaraussivulle, saa käyttäjä virheen 500. Tämä on nyt korjattu niin, että hyllyvarausraporttisivu aukeaa tyhjänä ja otsikkona on "Holds to pull reported on xx.xx.xxxx" eli suomeksi "Hyllyvarausraportti luotu xx.xx.xxxx"

!{width:45%}hyllyvarausraportti.png!

Liittyy "Github-tikettiin 254":https://github.com/KohaSuomi/Koha/issues/254

#hyllyvarausraportti #virhetilanne

Viestipohjien ylläpito

Viestiepohjien ylläpidossa jos kopioi pohjan tietylle kirjastolle, mutta valitsikin sitten peruuta, kopioitui pohjan tiedot siltikin kirjastolle. Tämä on nyt korjattu ja viestipohjan tiedot eivät kopioidu kohdekirjastolle, jos valitaan peruuta.

!{width:35%}viestipohja.png!

Liittyy "Github-tikettiin 237":https://github.com/KohaSuomi/Koha/issues/237

#viestipohjat

  * mahdollisesti 204, jos ehditään testata

* tiketit ja repositoriot
  * tiketit tehdään kuten ennenkin Koha-repositorioon, mutta siirretään tarvittaessa muihin repoihin, jos ne liittyvät niihin. Esim. jos tiketti liittyy tarratyökaluun, siirretään se kyseiseen repoon.
  ** lisätään repositorioihin tieto suomeksi selkokielisesti, mihin toimintoon se liittyy.
  * Tiketin seuranta -projektissa näkyy kaikki tiketit reposta huolimatta, jos niihin vain on muistettu laittaa projekti-tieto.
  * Kaikki Koha-Suomen tiketit näkyvät, kun klikkaa Githubin yläreunasta "Issues-linkkiä":https://github.com/issues ja muuttaa hakukenttään seuraavan tiedon "is:open is:issue user:kohasuomi archived:false" (ilman hipsuja).
  * tikettien siirrolla pyritään sujuvoittamaan koodikannan ylläpitoa, kun tiettyyn koodiin liittyvät tiketit ovat koodin yhteydessä.

* loginattempts

* Lasse Pouru aloittaa Johannan sijaisena 12.12. Turussa.

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-45-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikon 44 muistio

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-44-muistio

Aika: 31.10.2022 klo 10
Läsnä: Anneli, Ari, Emmi, Kodo, Lari, Oskari, Pasi

* Päivystysvuorot viikosta 45 eteenpäin
  * Vko 45 Anneli ja Pasi
  * Vko 46 Lari ja Kodo
  * Vko 47 Emmi ja Pasi
  * Vko 48 Anneli ja Lari

* Maanantain viikkopalaveri siirrettiin kello kymmeneksi.

* Tietokanta-ajona muutetut nidetilat ei päivity indeksiin? Kusminin Pian kysymys Pääkäyttäjät - Yleinen -kanavalla.
  * Uudelleenindeksointi Lapille ma-ti-yöksi: Emmi
  * Indeksin dumppaus pitää poistaa käytöstä indeksoinnin ajaksi.
  * Jatkossa olisi hyvä tehdä uudelleenindeksointi aina, kun tehdään isoja tilamuutoksia tietokanta-ajona. Kodo lisää tiedon Principioon.

* Tiistain päivitys
  * "GitHub tiketti 222":https://github.com/KohaSuomi/Koha/issues/222 - Siirtotoiminnon rikkinäisen linkin korjaus
  * Yksi käännöskorjaus, Anneli täydentää tähän muutoksen.
  * lastseen-arvon päivitys RESTin borrower/status-kirjautumisessa #4234. Finna-kirjautuminen pitää vielä tarkistaa (Anneli tarkistaa).

### Torstain palaveri

* Viikon 45 päivitys
  * #4234 - Finna-pluginiin lastseen-arvon päivitys
  * Github-tiketti 242 - käännösmuutos
  * Hyllyvarausraportin päivitys, jos se saadaan testattua ajoissa. Github-tiketti 226.
  * Aineistotyyppi lainaukseen ja palautukseen, jos ehditään tekemään muutos, että näytetään auktorisoidun arvon kuvaus. G-238

* strategiapajan yhteenvedon anti
  * siirretään maanantaille

* valutuksen ongelmat
  * osa internal server error -ongelmista johtuu siitä, että elasticsearch käy yöllä alhaalla
  ** valutus-daemon käynnissä aina, myös varsinaisen valutusajan ulkopuolella. -> Muutetaan pysähtymään 00-06.
  * totalissues-arvon päivittyminen
  ** Ratkaisu: katkaistaan kuvailupohjien ja biblioitems.totalissues -linkki ja tehdään erillinen cron laskemaan lainamäärät suoraan biblioitems-tauluun
  * päivällä olevat internal server error -ilmoitukset

* "#215":https://github.com/KohaSuomi/Koha/issues/215
  * Pasi hoitaa

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-44-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikon 43 muistio

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-43-muistio

Aika: 24.10.2022 klo 12
Läsnä: Kodo Korkalo, Ari Mäkiranta, Emmi Takkinen, Lari Strand, Anneli Österman

* Service Check
  * Ehdotus: SSH avaintarkistusten sähköpostinotifikaatiot kytketään pois käytöstä ja viikon päivystäjät ajavat aina aamulla töihin tullessaan kojump *-prod ko-service-check, jolla saadaan listattua kussakin kontainerissa syntyneet mahdolliset ongelmat (mukaanluettuna SSH avainvirheet) ja niihin pystytään reagoimaan heti. 
  * Uusi "warning" ilmoitustaso.
  * *Päätös*: päivystäjä ajaa aamuisin.
  ** voi ajaa myös, jos tulee ilmoituksia ongelmista.

* Vim->Vis palvelimilla ja kontainereissa? (https://github.com/martanne/vis/wiki/FAQ)
  * Vis oletukseksi ja siirtymäajan jälkeen poistetaan kokonaan Vim käytöstä.

* harjoittelijan aikataulu?
  * koulutus alkaa 27.10., harjoittelun aikataulu vielä avoin.

* Oulussa pe 4.11.2022 virkistypäivä, Anneli myös virkistymässä. Voiko esim. Pekurin kirjastoon antaa päivän ajaksi päivystäjien puhelinnumeron?

* Tiistain päivitys
  * #5606 - Niteiden poisto eräajona ja virheellinen viivakoodi - virhe 500
  * "G-tiketti 197":https://github.com/KohaSuomi/Koha/issues/197 eli signum 942m-kentästä ekana
  * Editx-validoinnin parannukset
  * "G-tiketti 224":https://github.com/KohaSuomi/Koha/issues/224 Finvoice-validointi epäonnistuu, jos AuthorName on yli 100 merkkiä pitkä
  * "Käännökset":https://github.com/KohaSuomi/Koha/issues/222 - github-tiketti 222

### Torstain palaveri

* TäTien floating_matrixit
* Slaven kummitustaulu kirkestestillä ja orpo .ibd

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-43-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikon 42 muistio

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-42-muistio

Aika: 17.10.2022 klo 12
Läsnä: Anneli, Lari, Emmi, Pasi, Kodo

* Jos käytössä on Toveri-plugin, sen tarvitsemat käyttöoikeudet näkyvät listalla valittavana mutta ilman kuvausta. Voisiko lisätä esim. jQueryllä?
  * Muutosta voi pyytää Hypernovalta.

* Tiistain päivitys
  * categorycode-muutos statistics-tauluun
  * "marc-kuvailuvirheraportit":https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/MARC-luettelointivirheraportit toimintaan ja näkyville.
  ** vaatii pfsensessä muutoksia sekä muutosten käyttöönoton tiistai-aamuna. -> Muutoksia ei tarvita
  ** ajastukset päälle 17.10.
  * kuvailupohjien automaattinen päivitys käyttöön tätissä ja paikallisissa kannoissa 17.10.
  * #5590 - asiakastyypin vaihtaminen asettaa asiakkaalle asiakastyypin oletusviestiasetukset ilmoittamatta. Tuodaan yhteisöstä korjaus, jossa virkailijalle annetaan ilmoitus, että asetukset muutetaan asiakastyypin oletuksiksi. Jos klikkaa ok, asetukset vaihdetaan. Jos klikkaa peruuta, asetuksia ei vaihdeta.

### Torstain palaveri

* Tiistain päivitys
  * #5606 - Niteiden poisto eräajona ja virheellinen viivakoodi - virhe 500
  * "G-tiketti 197":https://github.com/KohaSuomi/Koha/issues/197 eli signum 942m-kentästä ekana?
  * Editx-validoinnin parannukset
  * https://github.com/KohaSuomi/Koha/issues/211?

* "G-tiketti 214":https://github.com/KohaSuomi/Koha/issues/214 - onko mahdollista toteuttaa? Aiemminhan nuo tiedot laskettiin proelaskutus-tiedostosta.
  * todennäköisesti jonkinlainen ratkaisu on toteutettavissa, mutta aikataulullisesti sellaista ei ole mahdollista toteuttaa ihan heti. Anneli kysyy, pystyykö esim. Digi toteuttamaan skriptin, joka laskee tiedot heidän yhdistämästään xml-tiedostosta.


* #5065 - "Mahdollistaakohan uusi versio ilman koodimuutosta sen, että Hyllyvaraukset-raportin kerralla näytettävän hakutulosmäärän oletusarvo on Kaikki?"
  * muutos on todella hankala toteuttaa nykyisessäkin versiossa. Kodo kirjoittaa perustelut tikettiin.

* #5605 - huoltajan "suhde" putoaa pois.
  * Emmi tutkii asiaa.
  * Testatessa huomattiin myös, että virhetilanteessa lapsiasiakkaalle tuodaan huoltajan yhteystiedot (osoite, puhnro, email), vaikka kenttiin olisi jo kirjoitettu tiedot. Ilmeisesti siinä tilanteessa aktivoituu jotenkin PrefillGuaranteeField-järjestelmäasetus, vaikka ei pitäisi. Sen pitäisi toimia vain, kun lähdetään tekemään uutta lapsi/huollettava-asiakasta klikkaamalla huoltajan tiedoissa "Lisää huollettava".

* Koha-Suomelle tulee harjoittelija todennäköisesti Ouluun. Tarkka aloitusaika ei ole vielä tiedossa.

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-42-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikon 41 muistio

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-41-muistio

Aika: 10.10.2022 klo 12
Läsnä: Anneli, Lari, Emmi, Pasi, Ari, Kodo

* Raxit eli Rantasalmi omaksi kunnaksi
  * Kirjastoryhmät sopiviksi - Lumpeen Koha-pääkäyttäjät
  * Lumpeen Finna-pääkäyttäjä kysyy, miten saa kuntatasot muutettua Finnassa
  * yhteydenotot Koha-Suomeen päin Matrixissa tai sähköpostitse support(at)koha-suomi.fi


* GET /api/v1/holds vaatii edit borrowersin, miksi?
  * Pasi on yhteyksissä Geniemiin

* RACI

* #4234 - last seen -arvo
  * Päätös: muutetaan borrower/status-endpoint päivittämään lastseen-arvo
  * Tarkistetaan, päivittääkö Finnaan kirjautuminen lastseen-arvon

* Finna-plugin
  * tarjotaan Kansalliskirjastolle Finna-plugiin tehtyjä patcheja.

* Asiakkaiden tilien voimassaolo: Päätös: ajopäivästä 10v kaikilla kimpoilla
  * otetaan huomioon sotuttomat niissä kimpoissa, joissa se on tarpeen

### Torstain palaveri

* #5629 - Uusi sarake categorycode statistics-tauluun
  * aikataulu: 
  ** ti 18.10.2022 päivityksessä koodimuutos ja skeeman päivitys
  ** tietojen vienti usercodesta categorycodeen tai päätellään borrowernumberista, jos usercodea ei ole. Tehdään pari kimppaa kerrallaan öisin.
  ** sen jälkeen tiputetaan usercode-sarake taulusta
  ** Vastuussa: Emmi

* Tätin ja Melindan ongelmia
  * yksi erä jäänyt staging-tilaan kun Elastic mennyt alta
  ** Emmi lataa tiedoston palvelimelta ja Anneli vie sen tietueiden välivarastoinnilla Tätiin.
  * Melindaan syntynyt tuplia
  ** Palvelimella oli prosessit päällä tuplasti, ylimääräisten pysäytys auttoi ongelmaan.

* Kyytin Haminan ja Siilinjärven kuntasovellus
  * Toimii samalla tavalla kuin Finna. Kuntasovelluksessa kaikki liikenne kulkee Geniemin palvelimen kautta.

* Tullut EDItX-sanomia, joissa vain marcxml. Ne jäävät processing-tilaan.
  * näistäkin lähtee jatkossa virheilmoitus sähköpostiin

* Suomi.fi-viesteille ei saa valittua täppää, templatet ei noudata tietokannassa määritettyjä viestiasetustyyppejä. Sama ongelma koosteviesti-täpän kohdalla.
  * Pasi tutkii

* "Github-tiketti 204":https://github.com/KohaSuomi/Koha/issues/204
  * Korjataan toistaiseksi javascriptillä sekä se, että täpät poistuu, kun sähköpostiosoite poistetaan ja että täpät eivät ole valittavissa, jos sähköpostiosoitetta ei ole.

* Tiistain päivitys
  * categorycode-muutos statistics-tauluun
  * "marc-kuvailuvirheraportit":https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/MARC-luettelointivirheraportit toimintaan ja näkyville.
  ** vaatii pfsensessä muutoksia sekä muutosten käyttöönoton tiistai-aamuna.
  ** ajastukset päälle
  * kuvailupohjien automaattinen päivitys käyttöön tätissä ja paikallisissa kannoissa

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-41-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikon 40 muistio

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-40-muistio

Aika: 3.10.2022 klo 12
Läsnä: Ari, Anneli, Johanna, Kodo, Lari, Pasi

* Testi-Tätin RCN-täsmäytyssäännöt ei toimi ajatellusti. Kaikki KP:n päiväpakettien tietueet täsmäytyy yhteen tietueeseen.
  * Laitettiin testi-tätiin RCN:n sääntöön pelkkä 035a ja katsotaan, miten käy. Anneli kysyy Antilta, voisiko KP lisätä osakohteisiinkin 035a:n

* Koha-Suomen seminaarin aikainen hotelli
  * Helka

* taustatöitä jää edelleen aloitettu-tilaan
  * Pasi tutkii lokeja, löytyiskö jotain.

* Tunnistamo-murheita
  * Tunnistamo haluaisi syntymäajan, mutta semmoista ei borrowers/statuksesta tule, vaan tule pelkkä ikä
  * Ehdotettu oauthia + patrons/validationia, josta syntymäaika ilmeisestikin saataisiin
  * Toinen vaihtoehto on olla tallentamatta syntymäaikoja ja ikätietoja tunnistamoon ja kysyä ne "on demand" Kohasta aina kun asiakas kirjautuu tunnistamoon

* biblio_metadata bakkitaulut, mitä, miksi?
  * Outissa, Vaarassa, Lapissa ja Lumpeessa on biblio_metadata_20220614, tätissä biblio_metadata_20220616
  * Jos eivät ole tarpeen niin voisi varmaan poistaa, ovat melko isoja tauluja
  * Päätös: liittynee biblionumber/biblioitems-taulujen biblionumberepäsynkkaan. Voidaan tiputtaa.

* Branchtransfers
  * Branchtransfersissa on niteiden kuljetustiloja vuodesta 2014 asti (Vaara), näitä lienee turha säilytellä
  * Puhuttu kehittäjäkanavalla 1-2 vuoden säilytysajasta, vanhemmat pois?
  * Branchtransfersin voisi ehkä ottaa siivousten jälkeen mukaan tietokantojen tuntidumppeihin

* Kirkes
  * Kirkes kuulumiset on että Kirkekseen ei kuulu paljon mitään.

* Githubissa pääkäyttäjien oikeudet, miten saadaan heillekin oikeus lisätä tiketit Tikettien seuranta -projektiin?
  * Lisättiin superlibrarians-tiimille write-oikeudet. Kokeillaan, riittääkö.

* Haminan kunta-appi tarvitsee rajapintakuvauksen
  * Toimitetaan samat tiedot kuin Siilinjärven kuin kunta-appia varten on toimitettu.

* Suomi.fi-viesteissä käyttökatkos ke 5.10.2022 klo 12.30-13.30. Cronin disablointi keskiviikkona.

* Päivystäjät vko 41 lähtien
  * Vko 41 Anneli ja Lari
  * Vko 42 Emmi ja Pasi
  * Vko 43 Anneli ja Kodo
  * Vko 44 Lari ja Emmi

* Tiistain päivitys
  * Kellutukseen tulevat seuraavat korjaukset
  ** Kirjastotunnuksessa voidaan käyttää %-merkkiä, jolloin kunnan kaikille toimipisteille voidaan määrittää vain yksi yleissääntö
  ** Asetuksen ei enää tulisi yrittää täsmäyttää niteeseen kaikkia olemassa olevia sääntöjä
  * Finna-rajapinnan pluginin päivitys.
  ** Varaustunnus tarkistetaan Finnassa ennen kuin se lähetetään Kohaan.
  ** Rajapinnan vaatimia oikeuksia on karsittu.
  * Varaustunnusten käsittelyyn korjauksia Kohassa
  ** Jos varaustunnus on jo olemassa, tulee nyt ilmoitus, että se on jo toisella asiakkaalla.
  ** Tallentamattomat tiedot eivät enää tipahda lomakkeelta, jos virheilmoituksen saa.

### Torstain palaveri

* SmartBoxin kanssa säädetty luukkuautomaatin lainaustoiminnallisuuden kanssa

* RACI Koha-Suomen ja Bittigurun välille.

* #5120 Vaskista kyseltiin emottomien listan perään
  * Pasi ajaa listan illalla.

* Valutuksen blokkausta paranneltu, mahdollista on ajaa massana mikropalvelun aktivointitauluun blocked-arvo, vaatii kimpasta tiedon mistä päiväyksestä taaksepäin blokataan.

* Tiistain päivitys
  * Laskutustyökaluun erillinen ryhmäasetus huoltajan rajoitukselle. Laskutusryhmässä pitää käydä kytkemässä päälle, jos se halutaan.
  ** Nykyiset rajoitusasetukset tippuu pois, joten ne pitää käydä asettamassa uudelleen halutulla tavalla kaikille ryhmille.
  * Uudempi versio Raportointi-liitännäisestä
  * Hyllytarkenne näkymään niteen palautuksessa, https://github.com/KohaSuomi/Koha/issues/198
  ** Ajakaa päivityksessä ./translate install fi-FI ja ./translate install sv-SE, jotta tulee kieliversioihinkin näkyviin.
  * Finto-plugineista poistettu kenttien täyttämisen yhteydessä olleet animaatiot (testataan, josko pluginien käytettävyys paranee)

* Huoltoikkuna 12.10.2022 ja tulossa käyttökatko.

* altdb-toiminto taas pystyyn - Kodo tekee

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-40-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikon 39 muistio

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-39-muistio

Aika: 26.9.2022 klo 12.30
Läsnä: Anneli, Emmi, Johanna, Lari, Pasi

* Päivitys tehdäänkin jo ma-ilta klo 22 jälkeen, Lari tiedottaa pääkäyttäjiä.

### Torstain palaveri

* Varaustunnuksen uniikkiuden tarkistaminen: Asiakasmääreen voi määrittää uniikiksi nyt käytettävän othernames-kentän sijaan. https://tiketti.koha-suomi.fi/issues/5605. PatronDuplicateMatchingAddFields ei toimi.
  * #5627 varaustunnuksen tarkistus Finnassa. Ennen Finnassa tehtiin tarkistus "lennossa", mutta Finna-toimisto vastannut, että tarkistusta ei tehdä Finnassa. Mitenköhän tuo on ennen toiminut?
  ** Lari tehnyt Finna-rajapintaan muutoksen, että Koha valittaa/välittää tiedon, jos varaustunnus on jo käytössä. Testataan testi-Finnassa
  ** Seuraavaan vesionvaihtoon muutetaan varaustunnus asiakasmääreeksi ja puretaan nykyinen oma othernames-säätö
  ** Tehdään väliaikainen korjaus nykyiseen tapaan, muutetaan virheilmoitus informatiivisemmaksi ja tutkitaan, saako lomakkeen tiedot säilymään paremmin tuplatapauksessa.

* Asiakkaan kotikirjaston vaihto Finnassa (Kotikirjasto (lyhenne), rajapinnassa "library_id": "JOE_PYH" esim.): Tuki olemassa Finna-pluginissa. Pitäisi saada kulkemaan Finnasta/Finnaan. Yhteys Finna-tukeen?
  * Lari kysyy Tuomakselta, ehtisikö hän olemaan yhteydessä Finna-toimistoon.

* Tietueiden vienti paikalliskannasta Tätiin ja niiden täydennys Tätissä?
  * Ari keskustelee asiasta johtajien aamukahveilla

* Yhteisössä on palautettu asiakaslaji sarake statistics-tauluun, bug "7021":https://bugs.koha-community.org/bugzilla3/show_bug.cgi?id=7021
  * Mietitty Elementsissä muutoksen tuomista meille jo nyt ja tarvittavien muutosten tekemistä kantaan valmiiksi, jotta on vähemmän työtä ja kadonnutta dataa versionvaihdossa.
  * Päätös: Emmi tuo muutoksen yhteisöstä ja tekee tarvittavat tietokantamuutokset/ajot.

* #5566 kehitysehdotuksissa, tuli kyselyä, ehtisikö/voisiko tuota toteuttaa ennen kuin Oulussa otetaan Finvoice käyttöön?
  * Johanna tutkii, miten onnistuu

* Suomi.fi palvelussa huoltokatko 5.10. klo 12.30-13.30, jolloin vältettävä Suomi.fi-viestien lähettämistä.
  * säädettävä cron pois päältä, kalenterissa muistutus. Ensi viikon päivystäjien Pasin ja Kodon muistettava tehdä.

* Versionvaihto-projektin avoimet tiketit: kaikki käy omansa läpi ja sulkee valmiit. Katsotaan sitten yhdessä loput. Neuvotaan avaamaan uusi tiketti, jos ongelma palaa/esiintyy uudelleen.

* Maanantaina alkaa Githubin testijakso.

* Tiistain päivitys
  * Kellutukseen tulevat seuraavat korjaukset
  ** Kirjastotunnuksessa voidaan käyttää %-merkkiä, jolloin kunnan kaikille toimipisteille voidaan määrittää vain yksi yleissääntö
  ** Asetuksen ei enää tulisi yrittää täsmäyttää niteeseen kaikkia olemassa olevia sääntöjä

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-39-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikon 38 muistio

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-38-muistio

Aika: 19.9.2022
Läsnä: Anneli, Ari (poistui 12.30), Emmi, Johanna, Kodo, Lari, Pasi

* Tuotannon päivitys - versiotiedote
  * Finto-Asteri-plugiin korjaus toistuvien kenttien kloonaukseen.
  * SCO-käännösparannuksia
  * SCO-korjauksia
  * Vaihtoehtoinen nidetyyppi EditX:ssä.

* "Asiantuntijaryhmän kokouksesta":https://tiketti.koha-suomi.fi/projects/mls/wiki/Asiantuntijat_-_Vuosi_2022#Muistio-622
  * Sähköpostin lähettäjäosoite, vaskin ja outin eri kokemukset spf:n tarpeesta
  * asiakkuuden voimassaoloaika
  * kellutusryhmät - floatrules
  * Githubin testausaika loka-marraskuu

* Valtakunnallinen tilastointi ja rajapinnat
  * Ei käsitelty, koska Ari ei ollut paikalla

* Kyyti, editx ja vaihtoehtoiset nidetyypit
  * katsooko toiminto vain FundNumber-tägin?
  * Johanna tekee muutoksen, että tieto haetaan vähän eri tavalla.

### Torstain palaveri

* Koha ja raportointipalvelu - työpaja maanantaina 26.9. klo 8-16
* Laskutusasioiden jatkaja Johanna ollessa poissa?
* #5594 Kati huomautti seuraavasta:
  * Jos pääsanana on esim. U2, joka 110$a-kentässä on kuvailtu kuvailusääntöjen mukaan kenttään muodossa "U2,", signumissa otetaan huomioon myös pilkku.

* SSN-kannasta käyttäjien poistaminen, jos käyttäjällä logissa rivejä?
  * Lisätään kantaan uusi kenttä joka kertoo onko käyttäjä poistettu, mutta ei oikeasti poisteta käyttäjätietoja. (ts. toimitaan kuten sql-kantojen kanssa pitäisikin)

* Tiistain päivitys
  * #5594 Signum-pluginit ja pääsanojen välilyönnit - signumiin muodostuvat välilyönnit korvataan alaviivalla
  * Laskutustyökalun päivityksiä
  ** Finvoice-lähetys joko zip-pakettina tai yksittäisinä xml-tiedostoina. 
  ** Finvoicen xml-tiedostojen lähetys rivivaihtojen kanssa tai ilman.
  ** Mahdollisuus saada holhoajan tiedot erikseen laskulle, uusi ryhmäasetus tätä varten: "Muuta takaajakäsittely". Finvoice-esimerkki pohjaan lisäys tätä varten. https://github.com/KohaSuomi/koha-plugin-overdue-tool/blob/21.11/Koha/Plugin/Fi/KohaSuomi/OverdueTool/examples/finvoice-example.xml#L36
  ** "Luonti onnistui"-ilmoituksen näkyminen sivun yläreunassa ja sulkemispainike.
  * Tietuenäytölle valutuksen aktivointinappi ja ilmoitus milloin on aktivoitu.
  * Itsepalvelulainaus: virheilmoitus käyttäjälle, jos viivakoodia ei löydy palauttaessa.
  * Loput Finto-pluginit: finto_seko_noind.pl, finto_seko_nouri_noind.pl, finto_seko.pl, finto_slm-local.pl, finto_yso-aika_ind2_7.pl, finto_yso-aika_noind.pl, finto_yso-aika.pl, finto_yso-kauno_noind.pl, finto_yso-kauno.pl, finto_ysopaikat_noind.pl, finto_ysopaikat.pl

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-38-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikon 37 muistio

Aika: ma 12.9.2022 klo 12.00-
Läsnä: Ari, Lari, Johanna, Emmi, Pasi, Kodo ja Anneli

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-37-muistio

* ByWatersin viivakoodi-plugaria testattu /Emmi
  * Todettu puutteelliseksi ja toimimattomaksi

* Vaskissa oli jälleen onnistuttu hyppäämään 9000 viivakoodin yli #5545 /Emmi
  * Virkailija lisäilee numeroita viivakoodin perään, joka saa generaattorin kasvattamaan viivakoodien pituutta, ei saa tehdä näin!

* Itsepalvelun Valmis-näppäin ei toimi kaikissa selaimissa/selainversioissa #5604 / Anneli
  * Vaikuttaisi siltä, että ongelma voisi olla siinä, että jquery-kirjaston osoitetta ei ole ohitettu Pfsensessä. Tehdään ohitus ja testataan, auttoiko se.
  * Kodo tekee säännön valmiiksi ja Johanna painaa apply-nappia ti-aamuna.

* Asiakkaan kirjastokortin tai muun omituisen tiedon lukeminen itsepalvelulainauksessa lainauskenttään heittää geneerisen Kohan virheilmoitussivun / Kodo

* SIP-processing -tilan automaattikohtaisen asetuksen testaus / Kodo

* Mitä tulossa huomiseen päivitykseen mukaan eli versiotiedote? / Anneli
  * #5544 - osakohde
  * #5457 - hankintatiedot
  * käännökset
  * #4590 - Asteri-plugin
  * #5244 - Itsepalvelulainaus-korjaus, asiakkaan kotikirjasto tulostuu kuittiin, eikä kirjautuneen kirjaston
  * #5459 - Ilmoituspohjan kopioiminen sellaiselle kirjastolle, jolla sellainen jo on.
  * #5333 - Pikanäppäimien korjaus

* Aikatauludokumentti päivitetty (https://tiketti.koha-suomi.fi/projects/mls/wiki/Aikataulu_2020-2021), pari avointa asiaa / Kodo
  * Palomuurien IP-rajaus selvitettävä BittiGurulta
  ** Kodo kysyy Bittigurulta keskiviikon huoltokatkon aikaan.
  * YSO-konversion tilanne ja toimintasuunnitelma
  * RDA-konversion tilanne ja toimintasuunnitelma
  * EBooking varausjärjestelmän SIP2OHTTP-tilanne
  * Aineistotyyppi ei näy Kohassa, XSLT?
  * Vaskin Melindan tilanne
  * Testi-TäTi/Testi-Melinda onko vielä ajankohtainen?

* Kirkes projektia käynnistellään pikkuhiljaa / Kodo
  * Kirkes-repo + Dokumentaatiota ja malleja GitHubiin, repoa ei voine avata julkiseksi
  * Kirkes-väki saatu aika kivasti jo Matrixiin ja GitHubiin
  * Kokoukset perjantaisin klo 9

* Huoltokatkossa käyttispäivityksiä, joten lyhyet katkot keskiviikkona todennäköisiä / Kodo

### Torstain palaveri

* #5452 lainojen väärin kirjautuneet uusinnat ensilainasta
  * ongelmana kuinka rajata korjaus koskemaan vain verkkokirjastossa tehtyjä uusintoja, muuten kaikki uusinnat tietyllä aikavälillä "korjautuvat"
  ** ei haitanne?/AÖ

* jättimäiset kansikuvat, saako ne määritettyä xslt:llä aina tiettyyn kokoon? #5420
  * css:llä voisi onnistua
  * Pasi ottaa tiketin itselleen

* Kuusamosta ihmeteltiin sql-kyselyn ja OKM-tilastoliitännäisen isoa eroa lainatilastoissa esim. tammikuulta /Anneli
  * Emmi ja Johanna tutki koodia ja sieltä löytyi virhe, että poistettujen niteiden lainoja ei lasketa mukaan tilastoihin.
  * Emmi korjaa koodin ja tilastot ajetaan uudelleen.
  * Edellinen ei kuitenkaan selitä miksi alkuvuodenkin lainoissa on heittoa, sillä virhe on ollut olemassa vasta 2 kuukautta.
  * Luultavasti vika ollut plugarin edellisessä versiossa, mutta missä kohdin on arvoitus. Ajetaan tilastot uudelleen joka tapauksessa.

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-37-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 36 muistio

Aika: ma 5.9.2022 klo 12.00-
Läsnä: Ari, Lari, Johanna, Emmi, Pasi, Kodo ja Anneli

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-36-muistio

* Päivystysvuorot viikosta 37 alkaen
  * Pasi ja Kodo
  * Johanna ja Anneli
  * Emmi ja Lari
  * Pasi ja Kodo

* Teknisessä dokumentaatiossa päivitystarvetta ja uusien ohjeiden tarvetta. Mihinpäin Githubia ne laitetaan?
  * Samaan paikkaan kuin Kohan ohje suomeksi, mutta omaksi osioiksi.

* Biblioservice tietokannan dumppaus päivittäin, menee tati-prod -varmuuskopiohakemistoon.

* Vastaisuudessa lyhyt kuvaus commit messageen kun principiota päivitetään, jotta on helpompi seurata siellä tapahtuneita muutoksia tarvitsematta lukea läpi koko dokumenttia.
  * "Tikettien tilannetaulukkoon":https://github.com/KohaSuomi/koha-suomi-utility/blob/master/docs/k-s_git_branches.ods samanlainen lyhyt kuvaus, kun tekee muutoksia.

* Branchien nimeäminen jatkossa ja tulevaa versiopäivitystä silmälläpitäen
  * ks- ja KD/Bug-numeroiden lisäksi lyhyt parin sanan kuvaus mitä branchissa on, tämä voidaan ottaa käyttöön heti
  * ksdev/ jatkossa muotoon ks[tuleva koha-suomi julkaisuversio]/
  * esimerkiksi ks22/0100-KD-5678-kikkura-x
  * build-production nimetään uudelleen build-release, koska skriptillä rakennellaan muutakin kuin tuotantoympäristöjä
  * pohjana käytettävä yhteisöversion branch nimetään esimerkiksi ks22/koha-vnn.nn, jolloin se voidaan ottaa automaattisesti koha-suomi jakeluversion pohjaksi
  * otetaan käyttöön kstest/nnnn-KD-nnnn-kuvaus branchit testejä varten, testejä rakennettaessa mukaan kaikki tietyn tuotantoversion branchit+kstest/ -alkuiset
  * jakeluversio Koha-Suomesta rakennetaan jatkossa build-release:n komentoriviparametrin perusteella, esimerkiksi build-release ks22
  * Nykyisiä ksdev-brancheja ei nimetä uudelleen, seuraavasta versiosta lähtien tehdään branchit oikeilla nimillä ks22/...
  * build-release vaatii pienen korjauksen järjestysnumeroiden käsittelyyn, jotta järjestämisen tarkistus tapahtuu oikeasta kentästä
  * Pasi hoitaa build-release -muutokset

### Torstain palaveri

* Kuvailutietueiden niteiden kokonaislainamäärien oikaisu: https://tiketti.koha-suomi.fi/issues/4525. Tiketti Vaskin, mutta sama operaatio pitäisi tehdä muissakin kimpoissa.

* Redminen siivousta ja GitHubiin siirtymisen valmistelua
  * Hyvin vanhat, ei enää ajankohtaiset tiketit suljettu
  * Vanhat projektit, kuten KohaD ja Server suljettu
  * Manage nimetty uudelleen "Muistiot ja keskustelu" sekä tiketöinti sieltä poistettu käytöstä

* Mitä tälle tehdään? https://tiketti.koha-suomi.fi/projects/mls/wiki/Aikataulu_2020-2021 Hoidettujahan nuo toki kaikki on, pitäisikö tämä vielä varmuuden välttämiseksi käydä läpi ja katsoa onko jotain olennaista unohtunut?

* Kellutusryhmät ja -säännöt
  * Tällä hetkellä kellutusryhmien käyttäminen ei ole pakollista, sillä kellutussäännön lisääminen kirjastopisteiden välille kelluttaa (tai ei kelluta hieman säännöstä riippuen) pisteiden kaiken muun aineiston automaattisesti
  * Alkuperäinen tarkoitus oli kuitenkin, että kellutus perustuu nimenomaan kellutusryhmään kuulumiseen, säännöillä vain estetään esim. tietyn aineistolajin kelluminen
  * Tämä on mahdollista muuttaa, mutta muuttaako se tilannetta mitenkään oleellisesti parempaan
  * Viedään asiantuntijaryhmän päätettäväksi kuinka tämän kanssa toimitaan

* #5452 Verkkokirjastossa tehdyt uusinnat ovat kirjautuneet Finna-api-käyttäjän kotikirjaston mukaan
  * virhe ehtinyt olla päällä n. puoli kuukautta versionvaihon jälkeen, esim. Kyytissä tämä on johtanut Kouvolan pääkirjastossa n. 13 000 ylimääräiseen lainaan ja n. 2500 ylimääräiseen asiakkaaseen
  * sama virhe koskee pseudonymisoituja lainoja, osalla kimpoista ollut myös RenewalLog pois päältä (ilmeisesti oli jossain vaiheessa sovittu, että se olisi päällä), todennäköisesti issues-tauluistakaan ei ole apua
  * ainut vaihtoehto vaikuttaisi olevan uusintojen oikaiseminen ensilainan perusteella (vai voidaanko olettaa, että lainaajan kotikirjasto on yhtä oikein/väärin?)  
  * otetaan uusintojen kirjasto ensilainan mukaan kuten pitääkin

* Signum pluginien korjaus
  * Pääkäyttäjäpalaverissa päätettiin 6.9. muuttaa signum-pluginien tuottamat välilyönnit pääsanoissa alaviivoiksi (_). Tällä saadaan korjattua tarratulostimen pääsananvalintaongelma. #5594
  * Päivitetään plugarit ja tuodaan korjaus testeille.

* Päivitysaikataulu?
  * otetaan käyttöön säännöllinen tuotantokantojen päivitysaikataulu. Päivitys tehdään kerran viikossa tiistaisin, jos päivitettävää on.
  * Päivystäjä hoitaa ja huolehtii, että muut laittavat muutoksensa julkaisukuntoon ennen tiistaita.
  * samalla päivitys myös käännöksille aina.

* 09 sanoman käsittely ja noutoilmoitukset Smartboxeilla
  * Automaattipalautuksista ei generoidu noutoilmoituskirjettä eikä aineisto siirry noudettavana tilaan ennen tiskipalautusta
  * Niteet pitäisi Smartboxilla piipata sekä automaatille luukkua täytettäessä (jotta automaatti tietää missä luukussa ne ovat) että Kohan virkailijaliittymään (jotta aineisto muuttuu noudettavaksi ja asiakas saa noutoilmoituksen)
  * Cron-skripti voisi hoitaa Smartbox-automaatin toimipisteessä olevat processing tilaiset reserves-taulussa siten että niille tehtäisiin Kohan return-modulilla automaattinen "tiskipalautus"?
  * Asiakaspalautuksissa ja virkailijan tekemässä palautuksessa pitäisi toimia eri tavalla
  ** Entäs jos automaattiin palautuu asiakkaan palauttamana nide johon seuraavan tärppäävän varauksen noutopaikka on se sama automaatti, silloin noutoilmoituskirjettä ei saisi lähteä ennenkuin henkilökunta on käsitellyt niteen ja siirtänyt sen oikeaan luukkuun noudettavaksi. Kaksi tunnusta?

* Kantapalvelimen resurssihärö, ylipitkät kyselyt ja ko-db-reaper
  * Kantapalvelimelle (nat) oli jäänyt pyörimään johonkin ihme limboon hyvin vanhoja kyselyjä, jotka pikkuhiljaa söivät kantapalvelimen prosessoriaikaa. Kyselyt on tapettu.
  * Jatkossa ylipitkät kyselyt voidaan siivota kantapalvelimelta pois automaattisesti tarkoitusta varten kirjoitetulla skriptillä.
  * ko-db-connections reportoi nyt yhteyksien lisäksi myös ajossa olevien ja nukkuvien tietokantaprosessien määrät, sekä "stupidly long queries", eli yli tunnin ajossa olleet SQL-kyselyt.

* Raahen laskutus, laskujen siirtäminen Rondoon.
  * Siirretään aineisto sftp:llä, muiden tapojen rakentaminen vie aikaa ja vaatii kunnon testaamisen.

* Uutta Finto-Asteri-plugia on testattu Oulussa, Turussa ja Joensuussa. Voidaan muuttaa Finto-plugit toimimaan uusien javascript-kirjastojen mukaan.
  * Laitetaan Finto-Asteri-plugi tuotantoon ja Lari muuttaa muut Finto-plugit yhteensopiviksi Kohan kanssa.

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-36-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 35 muistio

Aika: 29.8.2022 klo 12
Läsnä: Ari, Antti, Lari, Johanna, Kodo, Anneli ja Emmi

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-35-muistio

* Testien kantojen anonymisointi
  * Kysellään pääkäyttäjien mielipiteet tiistain palaverissa ja päätetään anonymisoinnista.

* Paperikirjeiden uudelleenlähetyksen tarve
  * Kysellään pääkäyttäjien mielipiteet tiistain palaverissa ja päätetään uudelleenlähetyksestä.
  * Ei kiireinen korjattava

* OUTIn automaattiputoilujen syynä oli todennäköisesti hurjaan mittaan kasvanut SIP-loki
  * Ongelma vaikuttaa poistuneen nyt kun rotaatio on korjattu.
  * OCFS2:lla tiedostoihin appendointi vaikuttaa olevan hitaahkoa, johtuneeko metadatan synkkauksista nodejen välillä vai kirjoittaako OCFS2 appendin yhteydessä itseasiassa koko lokitiedoston SANille uudestaan?
  * Katkot ilmenivät ilmeisesti aina tiedostojärjestelmän committien (kun isoa lokitiedostoa kirjoitettiin SANiin) yhteydessä jos automaatti sattui juuri sen commitin aikaan olemaan yhteydessä SIP-palvelimelle.

* Sähköpostit eivät mene perille gmail-osoitteisiin Kohasta jos palautusosoite/vastausosoite on eri domainilla kuin from-osoite
  * Jostain syystä tällöin smtp.mailfrom osoitteeksi tulee palautusosoitteen/vastausosoitteen domain
  * Esimerkiksi jos lähettäjäosoitteeksi on määritelty @koha-suomi.fi ja palautusosoite/vastausosoite on @outikirjastot.fi, on smtp.mailfrom @outikirjastot.fi ja header.from @koha-suomi.fi, jolloin DMARC-tarkistus feilaa ja posti merkitään Googlen päässä roskapostiksi
  * Qu'est-ce qu'on fait?

* Tiketti 4353
  * signumbuilder tuottaa viallisia signumheader:eitä eli teoksen pääsanoja
  ** signumbuilder tuottaa pääsanoja, joissa on välilyöntejä, esim. "5 M" tai "70 ". Oikeellinen pääsana: "5MI" tai "70O"
  * se, että pääsanassa on välilyönti aiheuttaa ongelmia signumYKL, signumLoc, signumHeading arvojen paikantamisesa
  * Ratkaistaanko asia korjaamalla signumbuilder, vai muuttamalla tarratulostimen koodia ottamaan signumbuilderin virheelliset pääsanat
  ** jos asia korjataan muuttamalla tarratulostimen koodia, niin se ei silti korjaa aiemmin mainittua ongelmaa, missä pääsanan välilyönnit (joita ei pitäisi olla) estävät YKL / Loc / Heading oikeellista paikantamista.

* KohaCon2022
  * "Osallistutaan etänä":http://koha-us.org/events/conferences/kohacon22/ Ilmoittautuminen 31.8.2022 mennessä.

### Torstain palaveri

* ByWaterSolution tehnyt plugarin "koha-plugin-barcode-prefixer":https://github.com/bywatersolutions/koha-plugin-barcode-prefixer
  * ilmeisesti tämän olisi tarkoitus toimia samaan tapaan kuin K-S:n BarcodePrefix-asetus
  * lisäksi plugarilla voi ilmeisesti määrittää prefixin asiakkaiden korttinumeroille
  * tätä voisi testata (tällä ei tosin ehkä täysin voida korvata BarcodePrefix-asetus, sillä Editx-plugari käyttää sitä)

* Plack reloadin vaikutus Kohaan ja automaatteihin
  * Virkailijaliittymässä havaittavissa 10-15 sekunnin toimintaviive, mutta järjestelmä toipuu sen jälkeen kauniisti
  * Automaateilla katko aiheuttaa automaatin "putoamisen" jos se sattui olemaan Kohaan yhteydessä juuri reloadin aikaan
  * Ei helposti ratkaistavissa, workerien kääntäminen vie sen ajan mitä se vie. Pienemmän worker-määrän kääntäminen on nopeampaa, mutta pienempi worker-määrä voi aiheuttaa muita ongelmia.
  * Joko hyväksytään että satunnaiset ~5 automaattia voivat pudota reloadissa ja tiedotetaan viiveestä ennakkoon esimerkiksi "Pääkäyttäjät - Automaatit" -kanavalla, tai vaihtoehtoisesti vältetään reloadeja päivällä
  * Automaattien retryn voisi yrittää yhteistyössä automaattitoimittajien kanssa viilata semmoiseksi että katkenneen tapahtuman jälkeen yhteys muodostettaisiin uudelleen mahdollisimman nopeasti (~20 sek päästä?) eikä asiakasta törmäytettäisi virheeseen.
  * Restartin vaikutus on vielä drastisempi, siinä tapetaan workerien lisäksi myös Plackin master-prosessi, jolloin tarjoillaan noin viiden sekunnin ajan "Service unavailablea" myös virkailijaliittymästä, kunnes uusi master-prosessi saadaan käyntiin. Sen jälkeen joudutaan vielä odottelemaan se 10-15 sekuntia niitä workereitä.

* Sähköpostien lähetys 
  * iso osa kimpoista oli valmis luopumaan bounce-viestien läpikäynnistä.
  ** OUTIssa haluttiin tarkistaa ensin Nooralta -> voidaan luopua bounce-viestien läpikäynnistä.
  ** Vaskissa haluttiin säilyttää vaskikirjastot-domain, mutta aikoivat vielä keskustella asiasta.

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-35-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 34 muistio

Aika: 22.8.2022 klo 12
Läsnä: Antti, Lari, Emmi, Johanna ja Kodo

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-34-muistio

* Nodejen varmistusten laajentaminen ja kotihakemistojen siivous
  * Otetaan käyttöön edusta- ja tietokantanodejen /home ja /root -hakemistojen varmistukset, joten siivotkaa kotihakemistoistanne pois tarpeettomat tiedostot

* Kirkes tulille keskiviikkona, Koha-Suomeen neljä uutta kuntaa (Tuusula, Järvenpää, Kerava ja Mäntsälä) ja 8 uutta kirjastoa.
  * Vain 4 kuntaa, mutta väkimäärältään sijoittuu Lumpeen ja Vaaran väliin
  * Wikipedia kertoo: "Oman kunnankirjaston kokoelman ulkopuolisista varauksita peritään pieni maksu.", käytäntö poikkeaa muista Koha-Suomi -kirjastoista sekä tiekartan linjauksista, eikä taida olla toteutettavissa järkevästi Kohassa.

* Finna-JSONiksi top-listat Pasin koodilla suoraan feature-branchiksi? Yhteisössä hook ollut työn alla joka mahdollistaisi plugarisoinnin (https://bugs.koha-community.org/bugzilla3/show_bug.cgi?id=24724)

### Torstain palaveri

* #5537 käsittely (jälleen)
  * Ongelma on luultua pienempi
  * Ongelma on asia, mikä korjaantuu tulevissa Koha versioissa
  ** deleteditems -taulun käytöstä luovutaan 
  ** Kun nide poistetaan, items.itemnumber ei muutu null vaan items -tauluun tulee uusi kenttä, joka kertoo, onko nide poistettu
  * => Tiketin hylkäys?

* Sertifikaattikriisin jälkipyykki, korjaus ja opittua
  * Aiheutti noin tunnin käyttökatkon
  * Uusinta testattu Vaskissa ja siellä se toimi ongelmitta
  * Muiden kimppojen sertifikaatteja uusittaessa törmättiin ilmeisesti pfsensen bugiin, pfsense suuttui tyhjistä CRL:istä (certificate revocation list)
  * Ratkaistiin poistamalla CRL:t käytöstä fronteilta, ne olivat tyhjiä joka tapauksessa
  * Jos sertifikaatteja tarvii perua, voidaan se poistaa frontin hyväksymien sertifikaattien listalta, CRL:ää ei välttämättä tarvita
  * Myös revokointi CRL:n kautta on mahdollinen, silloin täytyy luoda CRL ja ottaa se kiinni halutulle frontille, tämä tuntuu kuitenkin vähän turhalta
  * Uusintaohje päivitetty principioon
  * Jatkossa testit ensin ja vasta kun ne on todettu toimiviksi, muutokset tuotantoihin, periaatteessa tämä kyllä tosiaan oli jo testattu Vaskissa

* .ksbashrc olennaisilta osin dokumentoitu Principioon, "Kontainerien aliakset ja oikotiet"

* Checksummausten laajentaminen ja sähköpostihuomautukset
  * Käsitellään asia vielä uudelleen maanantaina kun Annelikin on paikalla ja sen jälkeen pääkäyttäjäpalaverissa tiistaina.
  * Suositellaan testikantojen anonymisointia.

* Vanhoja kontainerien rootfs-shardeja poistettu, ssn ja koha-1706 vielä olemassa, kauanko säilytetään?
  * Säilytetään seuraavan Koha-versiopäivityksen yli.

* Paperikirjeiden uudelleenlähetys?
  * Käsitellään asia vielä uudelleen maanantaina kun Annelikin on paikalla ja sen jälkeen pääkäyttäjäpalaverissa tiistaina.

* Melinda-palaveri ja Kansalliskirjaston Slack
  * Palaveriin osallistuu myös Emmi ja Lari.

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-34-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 33 muistio

Aika: 15.8.2022 klo 12
Läsnä: Antti, Ari, Emmi, Johanna, Kodo, Lari

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-33-muistio

* Päivystyvuorot viikosta 34 eteenpäin
  * Kodo ja Lari
  * Johanna ja Anneli
  * Emmi Ja Lari

* Liikunta- ja kulttuurisetelit?

* Ceepos-kassaintegraatio: otetaan tuotanto käyttöön yhdellä Oulun pääkirjaston kassalla. Katsotaan miten alkaa sujumaan ja laajennetaan sitten. 

* SSN-työkalut ja sotu-siilon varmuuskopiointi siirretty tietokantapalvelimille ja turva-kontti ajettu alas.

* Päivitetty log4perl ja logrotate-skriptit käyttöön Vaaran tuotannossa, katsotaan miltä näyttää ja otetaan käyttöön muuallakin.

### Torstain palaveri

* Outissa 15-20 minuutin käyttöhäiriö maanantaina 15.8.

* Konversioympäristö Kirkestä varten tehty, otetaan kirkes-test sitten testikäyttöön tälle projektille. Projektiryhmä kokoontuu ensimmäisen kerran ensi viikon keskiviikkona klo 13.00-14.30.

* Mystinen asiakasvarmenneongelma pääasiallisena riesana tällä hetkellä. Aiheutti eilen noin tunnin käyttökatkon kaikissa kimpoissa. Selvittely jatkuu.
  * Bootataan haproxy tänään 18.8. klo 14.45 ja katsotaan tulisiko se sillä järkiinsä. Aiheuttaa lyhyen katkon kimpoissa, tiedotetaan pääkäyttäjiä.

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-33-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 32 muistio

Aika: 8.8.2022 klo 12
Läsnä: Ari, Johanna, Antti, Pasi, Lari ja Emmi

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-32-muistio

* Ceepos-kassaintegraation on lähes valmis, testataan ensin Oulussa.

*Torstain palaveri*
* #5566, Laskutusliitännäinen: takaajan rajoite ei poistu automaattisesti, kun kaikki laskutetut on palautettu
  * Rajoituksen poistuminen on kytketty Kohan omiin prosesseihin, toiminto on siis linkitetty aineistoon. Takaajaa ei ole millään tavalla linkitetty aineistoon, joten tiedon poistaminen ei ole teknisesti mahdollista siten että se tapahtuisi luotettavasti.

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-32-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 31 muistio

Aika: 1.8.2022 klo 12
Läsnä: Antti, Ari, Pasi, Emmi, Kodo ja Johanna

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-31-muistio
* Tuntidumpit takaisin käyttöön?
  * tarkoitus kytkeä takaisin päälle, olivat katkolla versiopäivityksen ajan.

* Turva-kontti ja SSN varmuuskopiot (ja haproxy)
  * Turva-konttii ei enää pääse osoitteella. Kontti on vielä päällä, jotta saadaan otettua siitä dumppeja.

* https://tiketti.koha-suomi.fi/issues/5544 - -Search.pm:ään (tai mihin se nyt kuuluukin)- Koha/Biblio.pm get_components_query koodimuutos, joka poistaa katkaisun käytöstä kontrollinumeroilla (rcn?) haettaessa?
  ** rcn-indeksin tyyppimuutoksella numeeriseksi ei vaikutusta.
  ** kontrollinumeron laittaminen sitaatteihin rcn-haussa näyttäisi tekevän oikean asian, tarvitaan muutos hakuihin ja pitäisi viedä myös yhteisöön.

* Käännöspuutteet ja uusi tuotanto.
  * Odotellaan, että Anneli palaa lomalta.

* Automaattiputoilut ja timeoutit.

* Muutosten vienti GitHubin kautta testiympäristöihin viemättä niitä tuotantoihin.
  * Päivitysajoon tehty muutoksia, jotta voidaan viedä vain testille. Katso "kehittäjien ohjeet":https://tiketti.koha-suomi.fi/projects/versionvaihto/wiki/Kehitt%C3%A4jien_ohjeet#Uusien-ominaisuuksien-vienti-testiin-ja-tuotantohaaran-p%C3%A4ivitys-alustavat-ohjeet

* Vaaran kirjastotunnusten muutos https://tiketti.koha-suomi.fi/issues/5548

* noreply@outikirjastot.fi -> noreply@koha-suomi.fi Outissa.

### Torstain palaveri

* #5561 - Finnassa näkyvien palautuskehoitusten otsikon ja selitteiden muutosehdotukset
  * tuli esiin pääkäyttäjäpalsussa, onko korjattavissa meidän päässä vai Finnassa?
  * "ei tietoa" korjaus mahdollisesti Finnan päässä, muuten Kohan pohjia muuttamalla
* #5337 - accountlines ja timestamp-sarake
  * voisiko tämän tehdä jossain vaiheessa?
  * annetaan olla tässä vaiheessa, jos joku kyselee niin katsotaan sitten uudestaan
* Tuotantojen päivitys
  * Johanna päivittää 10.8. huoltokatkon puitteissa

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-31-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

## Viikko 30 muistio

Aika: 25.7.2022 klo 12
Läsnä: Anneli, Antti, Lari, Pasi, Emmi, Kodo ja Johanna

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-30-muistio

* https://tiketti.koha-suomi.fi/issues/5269 - mitä tehdään?
  * Poistetaan message_transports taulusta ei-koosteviestien transportit, joka hävittää koostetäpät Finnasta  (testattu ja toimii).
  * Tehdään tietokantaan triggeri, joka pakottaa täpät paikalleen aina kun asiakkaan viestivalintoja muutetaan.
  * Piilotetaan koostetäppä Kohan liittymästä css:llä.
  * Ajetaan digest-täpät paikalleen kaikille asiakkaille joilla niitä ei ole.

* https://tiketti.koha-suomi.fi/issues/5532
  * Ei tehdä korjauksia lastseen-arvon mukaan, koska arvot voivat olla korjauksen jälkeen yhtä väärin. OKM-tilastot lasketaan laskentakaavan mukaan, joten ei vaikuta niihin. Kokoelmatyön kannalta poistotilastot ovat väärin, mutta tiedotetaan virheestä.

* https://tiketti.koha-suomi.fi/issues/5542 - koska tarkemmin ottaen tulee saataville?
  * Viikolla 30.

* https://tiketti.koha-suomi.fi/issues/5523 - testitulosten kirjaus ja miten edetään?

* https://tiketti.koha-suomi.fi/issues/5544 - Search.pm:ään (tai mihin se nyt kuuluukin) koodimuutos, joka poistaa katkaisun käytöstä kontrollinumeroilla (rcn?) haettaessa?
  * kokeillaan muuttaa Siilin testillä rcn-indeksin tyyppi numeeriseksi ja indeksoidaan uudelleen.
  * tarkistetaan, onko kannoissa vanhoja ei-numeerisia 001-kenttiä.

* Unpkg.com:in takkuilu ja tällä hetkellä netin yli ladattavat (js) kirjastot.
  * Muutetaan pluginit käyttämään paikallisia kirjastoja.

* Nalkutin -plugari valmis, vaatii kohan päivitystä.

* Turva-kontti voidaan ajaa alas, Kodo tekee. Pois myös haproxysta.

### Torstain palaveri

* Joku mukaan pääkäyttäjien viikkopalsuihin Annelin loman aikana?
  * Jompi kumpi tai kumpikin päivystäjästä osallistuu.

* matrix & threadit

* RCN-täsmäytyssääntö
  * Antti H. laittanut KP:lle pyynnön lisätä 035a myös osakohteille. Siellä lomaillaan 4.8.2022 saakka ja Antti 14.8.2022 saakka.
  * kannattaisiko sääntöön lisätä myös 022a ja 035a niiden 001/003-sääntöjen lisäksi? Vai lakkaako se toimimasta kokonaan?

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-30-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 29 muistio

Aika: 18.7.2022 klo 12
Läsnä: Anneli, Antti, Lari, Pasi, Emmi ja Kodo

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-29-muistio

* Tarratulostus - tänään vastaanotettu lista rajoittuu kotikirjaston mukaan
  * Laitetaan testille testattavaksi.

* Päivystys vuorot viikosta 30->
  * Johanna ja Pasi
  * Emmi ja Kodo
  * Lari ja Antti
  * Johanna ja Emmi

### Torstain palaveri

* Background jobsien säilytysaika.
  * Säilytetään 2 viikkoa, siivotaan sitä vanhemmat onnistuneet työt pois päivittäin.

* Vanhempien (vuoden 2022) tilausten hintatietojen muutos alvittomiin - aikataulu?
  * Tehdään ajo ensin siilin testille ja jos se näyttää hyvältä, niin tehdään muihinkin kimppoihin vähintään vuoden 2022 tilauksille. 

* Sähköpostiosoite sip-sanomassa.
  * Hoidetaan pois template-muutoksella.

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-29-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 28 muistio

Aika: 11.7.2022 klo 12
Läsnä: Anneli, Antti, Lari, Pasi ja Emmi

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-28-muistio

* Kirkes pyytänyt testikantaan pääsyä
  * Nostetaan testi pystyyn ja päivitellään tietokanta, katsotaan tämän jälkeen mitä asetuksia/muutoksia pitäisi tehdä.

### Torstain palsu

* #5484 - voidaanko edistää itse yhteisössä, jotta saadaan korjaus ongelmaan? AutoHoldFill-toiminto on käytössä ainakin OUTIssa ja Hellessä ja sen laittaminen pois päältä aiheuttaisi varausten käsittelyyn runsaasti lisää hiirellä napsuttelua.
  * Lari tuo yhteisöstä korjauksen testille ja testaillaan toimiiko se.

* #5495 - nidehaku jumii signumin lopussa oleviin välilyönteihin. Mikä tuohon olisi järkevin korjaus? Poistaa ajona ylimääräiset välilyönnit vai tehdä yhteisöön tiketti, että haku jumii? Vai kumpikin?
  * Emmi tekee ajon, jolla poistetaan ylimääräiset välilyönnit itemcallnumbereiden perästä

* #5520 - OUTIssa deleteditems barcode ei-uniikiksi
  * Antti tekee muutoksen ma-aamuna aikaisin.

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-28-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 26 muistio

Aika: 30.6.2022 klo 10
Läsnä: Ari, Anneli, Antti, Lari ja Pasi

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-26-muistio

* Tarratulostustyökaluun toivottu tarran ohitusominaisuus. Onko turvallista toteuttaa, koska lasertulostimilla ei saa tulostaa kahdesti samalle arkille? Muita riskitekijöitä kirjattu "tikettiin 4580":https://tiketti.koha-suomi.fi/issues/4580.
  * Ei toteuteta toistaiseksi, koska ominaisuus sallii tulostimien käytön niiden valmistajien suositusten vastaisesti, jolloin voi aiheutua laitteen rikkoutumista ja vaaratilanteita. Keskustellaan vielä pääkäyttäjien kanssa tiedottamisesta.

* Hankinassa tilattu-sarake laskee hinnat verollisen hinnan mukaan. Budjetti ja käytetty-sarake on verottomia, jolloin käytettyjen varojen seuraaminen on hankalaa. Budjetti menee miinukselle liian aikaisin. "Tiketti 5487":https://tiketti.koha-suomi.fi/issues/5487
  * Korjauksena kaikkiin aqorders-taulun hintakenttiin veroton hinta? -> Tehdään tietokanta-ajo.

* Melindaan viennissä ongelmana, että tietue ei siirry Melindaan. Tätissä siirtotyökalu jää vain rullaamaan ja siirtoraportille ei tule mitään kirjausta yrityksestä. Liittyy ehkä osakohteettomiin tietueisiin.
  * Odotellaan, pystyisikö Antti H. vahvistamaan epäilyn. Jos hän saa vietyä Melindaan tietueen, jossa on osakohteita, päässään ehkä vähän eteenpäin tutkinnassa.

* Naantalissa Finvoice-ongelma. Viesti support-lootassa.
  * Pasi tutkii.

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-26-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 25 muistio

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-25-muistio

* Päivystys vko 25 eteenpäin

* Finvoice-testaus Oulussa
  * SFTP-yhteyden osoite ja tunnus.
  * Etsitään laskutusryhmän viitenumero sequence-taulusta.

* "952j":https://tiketti.koha-suomi.fi/issues/5476
  * Tutkitaan oai-pmh-tiedosto tarkemmin.

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-25-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 23 muistio

Aika: 6.6.2022
Läsnä: Ari, Emmi, Johanna, Pasi, Lari, Kodo, Anneli

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-23-muistio

* Toimintasuunnitelma versiopäivitystä varten
  * Tänään 6.6. kello 13 mennessä asetukset testeillä valmiina (Pääkäyttäjät)
  * Verkkokirjastoon kirjautuminen estetään klo 21. jälkeen (Pääkäyttäjät)
  * Tuotannon cronit disabloidaan tarvittavilta osin (kaikki mikä muuten tapahtuisi klo 21.05 jälkeen, Kodo)
  * Illalla klo 21.05 palvelut alas ja dumpit tuotannoista (Kodo)
  ** Dumpataan tietokanta, indeksit ja kimppakohtaiset hakemistot konteista kahdessa erässä alkaen 21.06 ja 21.36, valmista kaikkien kimppojen osalta ehkä noin klo 22.15, jos Bittigurun varmuuskopiopalvelin ei heittäydy hitailemaan.
  * Käyttöoikeusmigraatio kun dumpit valmiit (Emmi)
  * Konttipohjien vaihto (kloonataan nykyinen testi uudeksi tuotannoksi, Kodo)
  * Kontit ylös ja konfiguraatioiden vaihto + tuotannon uusi crontab 
  * Ajastetaan klo 23.00 alkaen updatedatabase + database cleanups for version upgrade 2h porrastuksella, isommat kannat ensin (tehdään skripti joka ajaa molemmat peräkkäin, Johanna)
  ** OUTI ja Vaski klo 23
  ** Vaara ja Lumme klo 01
  ** Lappi ja Kyyti klo 03
  ** Helle, Siili ja Täti klo 05
  * Tsekataan että ajastukset lähtevät suunnitellusti käyntiin
  * Aamulla tarkistetaan vahingot

* Päivityksen jälkeen huolehdittavat cron-ajot
  * advance_notices
  * overdue_notices
  * fines
  * update_patron_categories

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-23-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 22 muistio

Aika: 30.5.2022
Läsnä: Ari, Emmi, Johanna, Pasi, Lari, Kodo, Anneli

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-22-muistio

* LUMME-kirjastot: Koha antaa kahta eri eräpäivää #5410 
  * osa eräpäivistä mennyt juhannusaatolle, vaikka kalentereissa oli tehty ylistykset kys. päivälle
  * voiko johtua slaven delaysta?
  * Mikkeli Pääkirjaston kohdalla johtui tod.näk. liian myöhäisestä kalenteri muutoksesta, epäiltiin muuallakin olleen samaa vikaa

* Versionvaihdon aikataulu
  * Kuivaharjoittelun perusteella versionvaihto pystytään ajallisesti toteuttamaan suunnitellussa aikataulussa.

### Torstain palaveri

* MARC yhdistämisen säännöt
  * Pääkäyttäjät ja luetteloijat päättävät tuodaanko toiminallisuus uuteen versioon jossain vaiheessa

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-22-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 21 muistio

Aika: 23.5.2022
Läsnä: Ari, Emmi, Johanna, Pasi, Lari, Kodo

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-21-muistio

* Päivi Vaarasta toivoi, että huomiseen pääkäyttäjäpalsuun menisi kehittäjä paikalle, joka selostaa tämän viikon tietokantojen testipäivityskuvion.
  * sovittiin, että Kodo osallistuu palsuun

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-21-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 20 muistio

Aika: 16.5.2022
Läsnä: Ari, Emmi, Johanna, Anneli, Pasi, Lari, Kodo

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-20-muistio

* ssn-delete-user ei voi poistaa käyttäjää

* Finvoicen käyttöönotto versiopäivityksen jälkeen Oulussa ja Raahessa - aikataulu versionpäivityksen jälkeen. ProeLaskutus-rajapinta ei toimi enää uudessa versiossa.

### Torstain palaveri

* Testataan ensi viikolla tuotantokantojen päivitys, päivityksen ajan testit eivät ole käytössä, aikataulu:
  * Siilinjärven tuotannosta muodostetaan uusi testikanta nykyisen testikannan rinnalle ti-ke yönä (24.-25.5.), tällä testataan uusien testikantojen luontiin tarkoitettu automaatio.
  * Siilinjärven testikannan vaihto ja päivitykset keskiviikkona 25.5., jolloin siilinjärven testi on pois käytöstä joitakin tunteja.
  * Asetustaulut otetaan talteen nykyisistä testikannoista keskiviikkona 25.5. Kannat lienee myös hyvä dumpata varmuuden välttämiseksi.
  * Nykyisten testikantojen tipautus ja muiden uusien testikantojen muodostaminen ajastetaan tapahtuvaksi 25.5.-26.5. (ilta/yö ja helatorstai), jolloin tietokantakuormaa on vähän.
  * 27.5.-29.5. ajetaan testikantoihin tietokantapäivityksiä, koska perjantai on aukiolopäivä, on luultavasti viisasta porrastaa päivityksiä hieman.
  * Tarkistukset ja korjaukset alkuviikolla 22.

*HUOM! Vanhoja testikantoja ei enää palauteta takaisin, joten on tärkeää, että kaikki asetukset tulee tehtyä ennen 25.5.!*

*HUOM 2! Käynnissä olevat laina-aikatestit ym tulee olla valmiina 25.5. mennessä!*


"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-20-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 19 muistio

Aika: 9.5.2022
Läsnä: Emmi, Johanna, Lari, Pasi, Kodo, Anneli, Ari

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-19-muistio

*  Käytiin läpi versionvaihdon välittömät tiketit.

### Torstain palaveri

* Pelkällä tool-käyttäjäoikeudella ei pääse liitännäisiin 
  * suositellaan lisättäväksi inventory-käyttäjäoikeus heille, joilla ei työtehtävien vuoksi ole mitään tools-osion oikeutta.

* Laskutus-liitännäiseen pääsyn rajaus
  * lisätään liitännäisen konfiguraatioon toiminto, johon voi lisätä borrowernumberit, joilla pääsy laskutukseen


"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-19-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 18 muistio

Aika: 2.5.2022
Läsnä: Emmi, Johanna, Lari, Pasi, Kodo, Anneli, Ari

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-18-muistio

* ovedue-maksujen määrittely, siirrettäisiinkö koko maksukuvio kirjepohjien yhteyteen, jolloin voitaisiin liittää maksu mihin tahansa viestiin?
  * voisi kelvata yhteisölle, siellä on hieman tämänsuuntainen tiketti, joka on kuitenkin pysähtynyt
  * varsinaisen maksun lisäämisen asiakkaalle voisi kirjoittaa viestien käsittelyyn, kun viesti merkitään lähetetyksi ja sen voisi lisätä vain jos lähetys on onnistunut
  * maksun selitteeksi voisi tulla kirjepohjan otsikko suoraan ja tyypiksi vaikka joku "messages" tai sitten kirjepohjan koodi?

### Torstain palaveri

* Vain koosteilmoitus -kentät ei aktiiviseksi #5369
  * Tämä on aikanaan "korjattu" meillä yhteisöön tehdyn "Move C4::Members::Messaging to Koha namespace" tikettiin "18595":https://bugs.koha-community.org/bugzilla3/show_bug.cgi?id=18595, joka taas on riippuvainen "Koha objects for messaging preferences" tikettiin "17499":https://bugs.koha-community.org/bugzilla3/show_bug.cgi?id=17499
  * Nuo molemmat on aika massiivisia muutoksia, onko järkeä tuoda ne taas meille vai yritetäänkö korjata ongelma ilman niitä?
  * Yritetään korjata venkslaamalla tietokannan arvoja tai luomalla jquery-rimpsu

* Maksujen maksimimäärä-kenttä tyhjenee kun laina- ja maksusääntörivin ottaa muokkaukseen #5375
  * Korjattu versiossa 21.11.06, meillä on 21.11.03. Tuodaanko korjaus tämän version päälle? Tai voitaisiin myös päivittää tuohon 21.11.06, mutta riskinä on että jokin leviää siinä vaiheessa.
  * Tuodaan korjaus meidän version päälle, päivitys mahdollisesti rikkoisi jotain

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-18-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 17 muistio

Aika: 25.4.2022
Läsnä: Emmi, Johanna, Lari, Pasi, Kodo, Anneli

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-17-muistio

* Päivystysvuorot vko 18 ->
  * Vko 18: Lari ja Emmi
  * Vko 19: Kodo ja Pasi
  * Vko 20: Anneli ja Johanna
  * Vko 21: Lari ja Emmi
  * Vko 22: Kodo ja Pasi
  * Vko 23: Anneli ja Johanna

* build-production-branch skripti ja merge-ongelmat

* Lapin niteiden notforloan-arvon palautus nollaksi ei onnistu #5351, ajo näyttäisi jäävään sending data tilaan
  * muutos koskee sen verran montaa nidettä (+330000 kpl), että ajo on luultavasti siksi hidas
  * kokeillaan onnistuisiko ajo nopeammin, kun luodaan update-lauseke kullekin muutettavalle niteelle ja ajetaan ne sql-tiedoston kautta 

* notforloan-tilaisten niteiden varattavuus #5353
  * näyttää käyttäytyvän eri kimpoissa eri tavalla, jostain syystä esimerkiksi OUTIssa notforloan-status hävittää niteen hyllyvarauslistalta, mutta taas esimerkiksi Siilinjärvellä ei. Oletettavasti joku järjestelmäasetus, mutta mikä?
  * Tähän liittyvillä TrapHoldsOnOrder ja SkipHoldTrapOnNotForLoanValue asetuksilla ei näytä olevan vaikutusta.
  * UpdateNotforloanStatusOnCheckin sen sijaan vaikuttaa, jos siellä on määriteltynä statusmuutos nollaksi palautuksessa, notforloan-niteet tulevat Siilinjärvellä hyllyvarauslistalle, muuten eivät.

* cronjobtimer muutokset
  * Skriptit voivat nyt sijaita joko Koha/misc -hakemiston alla tai utilityssä.
  * Utilityssä olevat skriptit ovat ensisijaisia verrattuna Koha/misc -hakemistossa oleviin. Jos samanniminen skripti on kummassakin paikkaa, vain utilityssä oleva ajetaan.

* kirjeviestien testaus
  * Kopioidaan OUTI-kirjepohjat tuotannosta ja testataan kirjeiden lähetys outi-testiltä

* log4perl lokittamaan syslogin kautta
  * Lokitiedostojen käyttöoikeusongelmista päästään kun vaihdetaan log4perl appenderiksi syslog, jolloin log4perl lähettää syslog-daemonille lokituspyynnön ja syslogd hoitaa varsinaisen lokituksen.
  * https://metacpan.org/dist/Log-Log4perl/view/lib/Log/Log4perl/FAQ.pm#How-can-a-process-under-user-id-A-log-to-a-file-under-user-id-B

* kirjastoryhmät konvertoitunut hassusti __SEARCH_GROUP__-ryhmän alle
  * ajetaan tietokannassa erillisiksi ryhmiksi
  * pääkäyttäjien pitää käydä lisäämässä hakuryhmille täppä kohtaan "Use for staff search groups" (Muokkaa ryhmää)

* Canonin Uniflow-järjestelmä siirtyy käyttämään borrowers/status endpointia (plugin, lisätty email jota tarvitsevat). Tällä hetkellä heidän käyttämästään Auth/Sessionista luovutaan versionvaihdossa.
  * /auth/session endpointin luopumisesta ollaan oltu yhteydessä myös Viddlaan ja Webkakeen.

### Torstain palaveri

* Käytiin läpi versionvaihdon välitön-tilaiset tiketit.

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-17-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 16 muistio

Aika: 18.4.2022
Läsnä: Emmi, Johanna, Lari, Pasi, Kodo, Ari

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-16-muistio

* Ei merkittäviä tapahtumia, käytiin läpi mitä kullakin kehittäjällä ollut työn alla versionvaihtoon liittyen.

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-16-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 15 muistio

Aika: 11.4.2022
Läsnä: Emmi, Johanna, Lari, Pasi, Kodo, Anneli

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-15-muistio

* Portaali spämmää Hellelle samoja tilauksia 10 minuutin välein. Portaalin SSH-avain on poistettu Hellestä väliaikaisesti.

### Torstain palaveri

* Korjataan tyhjät relationship-sarakkeet tuotannoista, niin ei tarvitse korjailla tätä updatedatabase.pl:ään tai muuten korjailla versionvaihdon jälkeen
* Luodaan kellutukseen alustavasti syspreffi, jolla saadaan aineisto kellumaan hyllypaikan ja kokoelmakoodin mukaan. Edistetään sitten yhteisöön ajan kanssa sinne kelpaavampaa ratkaisua.  

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-15-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 14 muistio

Aika: 4.4.2022
Läsnä: Ari, Emmi, Johanna, Lari, Pasi, Anneli

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-14-muistio

* Kohan asiakasvarmenteet vanhenee lähiaikoina - uusimisen aikataulu ja organisointi
* Vaskissa, Hellessä, Lumpeessa ja Lapissa Editx-sanomat epäonnistuneet puuttuviin tilitietoihin (mm. DeliverLocation tyhjä aina yhdessä tilauksen tietueessa), pyydetty korjaamaan ja lähettämään sanomat uudelleen.
* Koha-Suomen ominaisuuksien toteutusjärjestyksestä
  * Ominaisuudet käyty läpi. Merkitty prioriteetilla "välitön" ne tiketit, jotka on oltava toiminnassa, kun versio vaihtuu.

### Torstain palaveri

* Kesälomat
  * Käsitellään ensi viikolla


"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-14-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 13 muistio

Aika: 28.3.2022 klo 12.30 - 13.30
Läsnä: Ari, Emmi, Johanna, Kodo, Lari, Pasi

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-13-muistio

* Hellen kummajaissanomat
  * Sekä viime viikolla selvittelyn alla ollut sanoma portaali_order_20220323132308.xml ja Woimalta uudelleen lähettetty sanoma portaali_order_20220328111023.xml (siirretty failed-archiveen) epäonnistuvat samasta syystä: _No vendor for SAN 284​980 (qualifier 91) in vendor_edi_accounts._
  * Viime viikolla asiaa selviteltiin meidän päässä, eikä sanomasta löydetty mitään kummaa. Kannasta tarkistettiin, että kyseisellä SANilla ja qualifierilla tulisi löytyä vendor_id (24). Viime viikon sanomasta poiketen uudessa sanomassa ei ole kuin yksi teos, ISBN 978-5-4370-0336-7 https://helle.koha-suomi.fi/cgi-bin/koha/catalogue/search.pl?q=978-5-4370-0336-7, joka näyttäisi edelleen menevän kantaan ja indeksoituvan, mutta käsittelyn epäonnistuessa se poistetaan kannasta ja indeksi jää paikalleen. 
  *  Syitä outoiluun on kaksi. 1) Kantaan tallennettu SAN sisälsi omituisia merkkejä. Tunnus on nyt tallennettu kantaan uudestaan oikeassa muodossa. 2) Tilaussanomassa tullut SAN sisältää ylimääräistä unicode-merkkisekoilua. Virhe on pyydetty korjaamaan hankintaportaalin päässä ja myös virhesanomat on pyydetty lähettämään uudelleen.

* Versionvaihto: RabbitMQ - tarvitaan uusi kontti jossa se pyörii? misc/background_jobs_worker.pl pyörimään jokaiseen -prod ja -test ympäristöön?
  * Pyöritään toistaiseksi ilman Rabbittia (vaatisi uuden virtuaalikoneen yms), pääkäyttäjien testattava riittääkö tuo workerin toiminta ilman sitä.

* Vastaanoton nopeuttaminen uudessa versiossa. Tehty yhteisöön tiketti. https://bugs.koha-community.org/bugzilla3/show_bug.cgi?id=30359

### Torstain palaveri

* Päivystysvuorot viikko 14 ->
  * Vko 14: Anneli ja Johanna
  * Vko 15 Lari ja Emmi
  * Vko 16: Kodo ja Pasi
  * Vko 17 Anneli ja Johanna

* Hellessä 10. tietuetta, jotka näkyvät Kohan haussa, mutta avatessa ilmoittavat ettei tietuetta ole Kohassa #5315
  * liittyvät jo korjattuihin virheellisiin sanomiin, ilmeisesti indeksoituneet vaikka tietue ei ole mennyt kantaan

* TLS-suojaus sähköpostipalvelimelle?
  * esim. ouka.fi-domain merkitty valtion sähköpostipalvelimilla TLS-pakotetuksi domainiksi ja nyt Bittigurun sähköpostipalvelimelta lähtevissä viesteissä ei ole TLS päällä, jolloin viestit hylätään vastaanottavan palvelimen päässä.
  * Ei toteuteta TLS:ää tässä vaiheessa, vaan muutetaan aiemman suunnitelman mukaisesti viestit lähtemään koha-suomi.fi osoitteista kimppakohtaisten domainien sijaan.

* OAI/PMH oli rikki ja palautteli infernal server erroreita tietuepoiminnassa
  * koha-oai.conf konfiguraatiotiedostoa korjattu, jolla ongelma ratkesi
  * testiympäristöjen Finna-poiminnat käynnissä ja valmistunevat tämän viikon aikana
  * Kansalliskirjastolta pyydetty kimppakohtaiset testi-finnanäkymät
  * Pääkäyttäjiä pyydetty tarkistamaan OAI/PMH asetukset testikannoista

* Salasanagenerointi toteutettiin JQuerylla (https://tiketti.koha-suomi.fi/issues/4647 ja https://tiketti.koha-suomi.fi/projects/versionvaihto/wiki/J%C3%A4rjestelm%C3%A4asetusmuutokset#Henkil%C3%B6asiakkaan-salasanan-generointi-4-numeroinen-PIN)

* background_jobs_worker
  * käynnissä ja käytössä nyt kaikissa kimpoissa, pyydetty pääkäyttäjiä testaamaan eräajoja
  * käynnistyy vastaisuudessa kontin käynnistyksen yhteydessä rc.local:ista

* Päivistyshommina ollut lähinnä EDItX:n kanssa säätämistä Hellessä ja Outissa.

* EDItX virheraportoinnin ajastusta muutettu, koska lokirotaatio ehti napata lokimerkinnät alta pois vanhalla ajastuksella ja tuloksena oli virhesanomia, joista puuttui lokista kaiveltu merkintä siitä, mikä varsinaisesti meni vikaan.

* "On pimeä korpi ja kivinen tie, ja usein se käytävä liukaskin lie." Uuden version käännöksissä vielä hieman viilattavaa...
* !{width:40%}kuva.png!

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-13-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 12 muistio

Aika: 21.3.2022
Läsnä: Ari, Anneli, Emmi, Johanna, Lari, Pasi

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-12-muistio

* Salasanan generointi #4554
  * Mitä kaikkea otettava huomioon?
  * Toteutetaanko javascript-rimpsuna vai plugarina?
* Support-laatikkoon tullut viesti Suomi.fi-viestien varmenteen uusimisesta 28.3-29.3.
  * Vaatiiko meiltä toimenpiteitä?
  * Todettiin ettei meidän päässä tarvita toimenpiteitä, koska "Muutos ei vaikuta esim. SFTP-pohjaisiin tiedostonsiirto-integraatioihin"
* Uuden version kielivalinnat ja viestipohjat
  * default tuntuisi tarkoittavan englantia - ennen englanti oli erikseen valittavissa. Aiheuttaa ongelmia, koska default-pohjassa on nyt suomenkielinen ja lisäksi tarvitaan englanti.
  * viestipohjissa näkyy viestityypit kahteen kertaan, viba konversiossa?
  * Tämän aiheuttajaksi paljastui käännöstiedostoihin väärään paikkaan päätynyt OPACin käännöksien prog-hakemisto, joka ei enää uudessa versiossa sisällä oikeita käännöstiedostoja. OPACin käännökset haetaan nykyisin hakemistosta /Koha/koha-tmpl/opac-tmpl/bootstrap. Tästä syystä viestipohjiin ja asiakasviestien kielivalintaan ei löytynyt kaikkia käännettyjä kieliä.   

### Torstain palaveri

* https://bugs.koha-community.org/bugzilla3/show_bug.cgi?id=30207

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-12-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 11 muistio

Aika: 14.3.2022
Läsnä: Ari, Anneli, Emmi, Johanna, Kodo, Lari, Pasi

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-11-muistio

* Testikantojen pystytys #5282
  * Kannat on konvertoitu ja sisäänkirjautuminen onnistuu
  * pisimpään meni OUTIssa (yli 18h kun cronien ajat lasketaan yhteen), mutta oletettavasti action_log- ja statistics-taulujen siivouksilla aikaa saa typistettyä
  * Elasticsearchin päivittämisessä vielä ongelmia 
  ** -tästä syytä ainakaan tietueiden lisäys ei onnistu, eikä indeksointia ole vielä voitu tehdä- 
  ** Fiksattu ja ohjeet tulee versiopäivityswikiin
  ** laitetaan indeksoitumaan pari- kolme kerralla tällä viikolla

* Lienee syytä informoida Kirkestä että niiden kirkes-test on nyt hetken aikaa höpsis.
* Vaskin luettelointipohjat päivitetty, MARC-päivittäjä ei pyöri automaattisesti tällä hetkellä.

### Torstain palaveri

* mitä tietoja kopioidaan testistä tuotantoon versiopäivityksen yhteydessä?
  * järjestelmäasetukset
  * viestipohjat
  * asiakastyypit (asetukset muuttuu)
  * tarkennetaan
* Testi-Täti yhteisöversioon
  * käytössä, mikropalvelu puuttuu
* testikannat uudelleenindeksoitu onnistuneesti
* versionpäivityksen aikajanan väliaikapäivitys?
* MARC-kuvailupohjat Tätissä: https://tiketti.koha-suomi.fi/issues/5277
* Tehdäänkö ennen versionvaihtoa: https://tiketti.koha-suomi.fi/issues/5269
* Elasticin mäppäykset eivät toimi, koska uudessa versiossa ei voi mäpätä samaa kenttää useampaan indeksiin


"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-11-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 10 muistio

Aika: 7.3.2022
Läsnä: Johanna, Kodo, Lari, Pasi, Emmi

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-10-muistio

* Webkake-parannukset
* ssn-add-user antaa nyt oletuksena find-ssn oikeuden, koska useimmiten se halutaan antaa
  * jos lisätään virkailijaliittymiä (lähinnä siis esimerkiksi kimppojen konversioiden yhteydessä), niin pitää muistaa tipauttaa se virkailijaliittymäkäyttäjältä ssn-disallow-find [käyttäjätunnus]

### Torstain palaveri

* Päivystysvuorot vko 11->
  * vko 11 Emmi ja Lari
  * vko 12 Johanna ja Anneli
  * vko 13 Pasi ja Kodo

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-10-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 9 muistio

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-9-muistio

Aika: 28.2.2022
Läsnä: Anneli, Johanna, Kodo, Lari, Pasi, Ari, Emmi

* Versionvaihdon aikataulutusta
  * Alustava päivä ti 7.6.2022
  * To 3.3.2022 tehdään alustava aikataulu versionvaihdon wikiin.

* Onko seuraavassa huoltokatkossa tulossa käyttökatkosta?
  * ei ole tulossa isoja katkoksia. Lyhyt n. 20 s katkos tulee.

* Kesälomat
  * Toiveet yhteiseen Tutanota-kalenteriin ensi maanantaihin mennessä.

### Torstain palaveri

* batch_rebuild_biblio ja replikointiviive 1.3. klo 22.00 - 2.3. klo 8.30
  * Samaan aikaan ollut käynnissä myös muita ajoja, joilla voi olla vaikutus asiaan
  * Varoitusta/hälytystä ei ole tullut Zabbixixsta häiriön aikana, selvitetään asiaa Bittigurun kanssa perjantaina 4.3.

* SmartBox-pilotti palaveri tänään klo 12.30

* Finnamaterials Lappiin ja sen jälkeen batchrebuildbiblios-ajo

* Tulostusasetukset-kuvat github.io ohjeeseen

* Testikannat communityyn
  * muutetaan, kunhan saatu testattua kuljetusten tiputuskoodin muutos myös automaattipalautuksilla
  * community.koha-suomi.fi-kantaan laitetaan jatkossa nykyisen version testikanta, jotta se on käytettävissä edes jossain kriittisiä testejä varten.

* Versiovaihdon aikataulutus
  * "Alustava aikataulu":https://tiketti.koha-suomi.fi/projects/versionvaihto/wiki/Aikataulu ja "Ganttissa aikajanaa":https://tiketti.koha-suomi.fi/projects/versionvaihto/issues/gantt

* Toverit
  * Hypernova olisi enemmän nykyisen toveri-rajapinnan plugarisoinnin kannalla, mutta ei täysin sulje pois SIP2oHTTP:n käyttämistäkään
  * Aiheuttaa "jonkin verran" kehityskustannuksia Joensuun seutukirjastolle, tarvitaan tarjous toteutusvaihtoehdoista Hypernovalta
  * SIP2oHTTP voi vaatia hieman muutoksia myös meidän pään SIP2oHTTP-rajapintaan (aukioloaika järjestelmäasetuksen noudattaminen)
  * Nykyisellä toteutuksella ei voida luopua asiakkaiden omatoimiblokkauksista Kohan liittymässä, koska Toverissa ei ole mahdollisuutta blokata asiakkaita ovikoneelta käsin
  * Keskustellaan Toveria käyttävien kirjastojen kanssa asiasta viikolla 11

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-9-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 8 muistio

Aika: 21.2.2022
Läsnä: Anneli, Johanna, Kodo, Lari, Pasi, Ari, Emmi

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-8-muistio

* Versiopäivitys
  * Vaihdetaan kimppojen testi-installaatiot käyttämään community-koodia ja ajetaan tietokantapäivitykset
  * Testaukset valmiiksi toukokuun loppuun mennessä, sen jälkeen mahdolliset korjaukset ja tuotantojen versionvaihto kesällä

* "Korvaushinta verottomaksi":https://tiketti.koha-suomi.fi/issues/5261 - aikataulutus
  * jos helppo ja nopea, tehdään, mutta muuten menee versionpäivityksen jälkeen.

* *ssn -kannat
  * kimppakohtaiset ssn-kannat voidaan pudottaa

* borrowersin ylimääräiset othernames-indeksit
  * Joissain kimpoissa oli jopa kuusi othernames-indeksiä borrowers-taulussa, pudoteltu pois, othernames_3 säilytetty

* SmartBox-palaveri tänään klo 13
  * Borrowers/status toimii suunnitellusti
  * SmartBox hoitaa testilaitteen Rovaniemelle
  * Palaveerataan vielä Lapin ja SmartBoxin kanssa ja käydään läpi miten käytännössä SmartBoxin ja Kohan kanssa toimitaan

### Torstain palaveri

* SmartBox pilotin aloituspalaveri Lapin ja SmartBoxin kanssa 3.3. klo 12.30

* Sertifikaatit Applen i-laitteita varten
  * Voidaan jaella keskitetysti ainakin MobileIron-etähallinnalla
  * Jakelu tehdään p12 formaatissa ja se toimii uusissa i-laitteissa Safari-selainten kanssa
  * .crt -formaatti ei asiakasvarmenteiden suhteen ole mahdollinen, koska paketoituna pitää olla sekä itse sertifikaatti että sitä vastaava avain. Paketointi taas onnistuu vain p12 -formaattiin.
 
* Kimppakohtaiset ssn-kannat pudotettu

* Testikannat siivottu ja tietotyyppimuutokset biblio/biblioitems-tauluihin tehty
  * Lisätään vielä muutaman taulun tipautus
  * Ajastetaan tapahtuvaksi tuotannoissa illalla, aikaa yhden kimpan kannan käsittelyyn menee noin puoli tuntia

* Imcoden kanssa palaveerattu pohjoismaisen Koha-yhteistyön tiimoilta ja tarkoituksena saada aikaiseksi "Letter of intent", jossa yhteistyökuviosta tehdään julkinen, mutta ei mitenkään varsinaisesti juridisesti sitova

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-8-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 7 muistio

Aika: 14.2.2022
Läsnä:  Anneli, Johanna, Kodo, Lari, Pasi

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-7-muistio

* Biblio_data_elementsiin lisättävät sarakkeet:
  * Anneli huomautti, että tauluun menevät myös osakohteet. Rajataanko nämä jatkossa pois vai lisätäänkö sarake component_part?
  ** lisätään sarake host_record, joka kertoo emotietueen. Jos null, niin se ei ole osakohde
  * Plugariin hahmoteltu deleted_on saraketta, johon kopioitaisiin timestamp deletedbiblioitems-taulusta.
  * Onko encoding_level (nimiön 17 merkkipaikka - Koodaustaso) tarpeellinen?
  ** Ei tarvita.
  * Tiputetaan sanomalehdet/aikakauslehdet pois okm-raporteilta.
  * Tarkempi luokka fiction sarakkeen lisäksi?
  ** mielellään kyllä. Ja vielä niin, että otettaisiin mukaan vain ensimmäinen 084a:n esiintymä. Jos esiintymiä on useampi, on ne biblioitems-taulussa cn_class-sarakkeessa eroteltuna |-merkillä. Helpottaisi hakuja, jos olisi vain yksi luokka.
  ** Päätös: tiputetaan biblioitems.cn_class-sarakkeesta toistumat triggerillä
  * Muita usein tarvittavia tietoja:
  ** biblioitems.isnb (ongelma, jos useampi esiintymä. eroteltu |-merkillä) - tiputetaan triggerillä muut ja tallennetaan vain ensimmäinen esiintymä
  ** biblioitems.ean (ongelma, jos useampi esiintymä. eroteltu |-merkillä) - tiputetaan triggerillä muut ja tallennetaan vain ensimmäinen esiintymä
  ** biblioitems.issn(ongelma, jos useampi esiintymä. eroteltu |-merkillä) - tiputetaan triggerillä muut ja tallennetaan vain ensimmäinen esiintymä
  * "toivotaan, että yhteisö pääsee eroon deleted- ja old-tauluista":https://bugs.koha-community.org/bugzilla3/show_bug.cgi?id=20271.

* Annelin loma siirtyi päivällä aiemmaksi, uusi lomajakso pe 4.3. - to 10.3. Pärjääkö Johanna pe yksin päivystyksessä, puhelujen siirto Johannalle?
  * Johanna pärjää

* OUTIn automaattikummittelut
  * Tietokantapalvelimalla näkyy Waiting for table metadata lock ilmoituksia OUTIn borrowers-taululle. Ilmoituksia näyttää aiheuttavan borrower-taulun lastseen-arvon päivitys.
  * OUTIssa 14.2.2022 klo 13.17 otettu outissa pois päältä TrackLastPatronActivity-järjestelmäasetus, joka päivittää asiakkaan Last seen -arvon. Ratkaisu ei ole pysyvä, vaan sen tarkoitus on ainoastaan auttaa ongelman selvittämisessä.
  * Muilla kimpoilla vastaavia ilmoituksia ei näy.

### Torstain palaveri

* Ylimääräiset 'othernames' indeksit borrowersissa ja KD-2190. Mitähän tässä nyt on taustalla?
  * Poistetaan ylimääräiset, jätetään vain testin vaatima othernames_3

* Start transaction, binlog ja replikointi (https://dev.mysql.com/doc/mysql-replication-excerpt/8.0/en/replication-features-transactions.html)
  * Täytyy perehtyä tarkemmin milloin transaction on binloggauksen kanssa ongelma.
  * Tässä vaiheessa kirjoitetaan ja testataan kyselyt huolellisesti ennen muutosten tekemistä kantaan, mutta tehdään varsinaiset muutokset ilman transactionia.

* Pakettienhallintakorjaus konteissa
  * Dokumentoidaan principioon.

* Binlogien automatisoitu siivous
  * Dokumentoidaan principioon.

* ko_slave_delay pelaa nyt myös masterilta käsin

* sip2ohttp xml lokitus ennen parsintaa
  * On jo toteutettu ja Outilla käytössäkin, voidaan tarkistella halutut sanomat suoraan sipohttp.log:ista

* Valtori on avannut palvelimen IP:t Suomi.Fi-palvelulle.

* Zabbix -> Matrix integraatio?
  * Selvitetään Bittigurun kanssa miten Zabbix-hälyt saadaan kulkemaan Matrixiin

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-7-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

----

## Viikko 6 muistio

Aika: 7.2.2022 klo 12.00
Läsnä: Anneli, Ari, Emmi, Johanna, Kodo, Lari, Pasi

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-6-muistio

* Uutiset-osio nettisivuille (Redminestä)?
  * Etusivuksi ja nykyisen etusivun sisältö "Koha" sivulle tiivistetysti
  * Etusivulla voidaan mahdollisesti pitää lyhyt esittely

* Laskutustyökalu
  * Taipa-palvelimen sftp-yhteys takkuilee. Ilmeisesti useampi node, jotka tarjoilevat eri server fingerprinttiä, jolloin sftp-yhteys epäonnistuu kun meidän pää ei tunnista vastapään palvelinta oikein.
  * ODUECLAIM- eli elaskut. Eivät lähteneet OUTIssa, koska oli blokattu e-kirjeistä. Nyt blokki poistettu ja elaskut lähtevät. Korjattu myös tyhjien nollalaskujen muodostuminen.

* message_queuen peukaloiminen suoraan SQL:llä ei kestä start transactionia. Putoo automaatit ja Koha menee kopsis. Elikä siis hyvin tarkasti vain tehdä ajot ilman transactionia jos viestijonoa täytyy säätää.

* TäTi: Z39.50-poiminta pudottaa 020-kentästä ISBN:n väliviivat #5207
  * Kokeillaan ottaa eka pois testistä, katsotaan vaikuttaako täsmäytykseen. Triggerin pitäisi hoitaa se editX-sanomissa.

* Slaven hyödyntäminen raporteissa, tilastoissa ym.
  * Hyllyvarausraportit generoidaan jo slavella.
  * Uusi KohaSuomi-spesifi moduli, jolla voidaan käyttää raportteihin ja muuhun pelkkiä selectejä sisältäviin tietokantakyselyihin slavea.
  * Guided.pl muutettu käyttämään uutta modulia, jolloin raporttikyselyt ajetaan slavella. Testiin tänään.

* SCO-yhteyksien suojaus
  * Keskusteltiin SCO-yhteyksien käyttöönotoista ja yhteyksien suojaamisesta.
  * OUTIssa käytössä asiakasvarmenteet, jotka ilmeisesti kuitenkin ainakin Windows-päätteillä vaativat vastapään ylläpitäjiltä melkoisesti kikkailua. Ei ehkä ihan optimaalinen ratkaisu.

* PostiMessaging huoltokatkot
  * 12.2. ja 19.2.2022
  * Muutoksia myös sftp-palvelimella
  * Soitettu PostiMessagingin Service Deskiin ja server fingerprinttien ei pitäisi muuttua.
  * Kirjastoissa syytä kuitnekin tarkistaa, että kirjeet varmasti menivät oikein noiden päivien jälkeen.
  * Jos failed-tilaisia vähän, niin kirjastoissa voidaan käydä painelemassa Kohan liittymässä "Resend", jos paljon, niin kehittäjiä voi pyytää asettamaan epäonnistuneet viestit takaisin "pending" -tilaisiksi.

* PostiMessaging PDF-kirjeet: kirjeeseen näyttäisi tulevan oikea ylämarginaali, ainakin testillä luoduissa kirjeissä.
  * Kysytään PostiMessagingilta lisätietoa, jos ongelma onkin heidän päässä.

### Torstain palaveri

* Tilastointiin muutama muutos:
  * BiblioDataElements.pm käyttämään tietokanta slavea #5260 
  ** viety masteriin, ei vielä tuotannossa (odottaa että C4::KohaSuomi::Tweaks viedään tuotantohaaraan)
  * biblio_data_elements-taulun päivitys myös kun MARC muuttuu #5264 
  ** voisi vielä testata esim. OUTIssa, lähinnä kiinnostaa paljonko vaikuttaa cronin suoritusaikaan 
  * kielikoodi 008-kentästä #5263 
  ** vielä tekeillä, testattava
  ** HUOM! muutos vaatii sitten biblio_data_elementsin pakkopäivityksen, kerta taulua halutaan käyttää SQL-raporteissa

* PostiMessaging PDF-kirjeet, koodissa oleva mm ei ole sama paperilla. Nostettu arvoa 16mm mikä on tulostettuna n. 13mm.

* Asiakasvarmenteiden uusiminen, ohjeet el principiossa.

* Laskujen eräpäivän määrittäminen laskutustyökalussa.

* OUTIn tahmat
  * Tiistaina ja keskiviikkona neljän aikoihin automaattiputoiluja ja yleistä tahmailua
  * Tiistaina tehty muutoksia pfsenseen, mutta ei ole aiheuttanut ongelmia missään muussa kimpassa (vastaus saatu Vaski, Vaara, Kyyti)
  * Ilmeisesti ei myöskään aiheuttanyt ongelmia muissa OUTI-kimpan kirjastoissa Oulua lukuunottamatta
  * Keskiviikkona tehty pfsenselle muutos, mutta se on tehty jo kahden aikoihin, kun taas Oulun ongelmat ovat ajoittuneet noin kello neljään, eli ei sovi ajallisestikaan
  * OUTIn testillä ja tuotannosta siivottu pois satoja ylimääräisiä SIP-palvelimen threadeja, jotka syntyneet luultavasti alueittaisen SIP-jaon seurauksena. Tällä ei selvästikään kuitenkaan vaikutusta, koska keskiviikkonakin on ollut pätkimistä.

* Huoltoikkuna keskiviikkona
  * Päivitettiin nodejen ja kontainerien käyttikset
  * Zabbixiin pääsy nyt olemassa Kodolla, muille pitää pyytää tunnukset bittigurulta

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-6-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 5 muistio

Aika 31.1.2022 klo 12
Läsnä: Anneli, Ari, Emmi, Johanna, Kodo, Lari, Pasi

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-5-muistio

* Kotisivumuutokset
  * Yhtiökokous => Muistiot, jonka alle redminestä jatkossa Managen alta muistiot + se mitä "Yhtiökokous" -sivulla nyt on, oisko joku muu nimi sivulle parempi kuin muistiot?
  * Dokumentaatio => Ohjeita
  * Yhteystietoihin voisi lisätä henkilöstön, ehkä jopa naamakuvilla, jos halutaan, pääkäyttäjien yhteystiedot joko samalle sivulle tai principion ja muiden yksityisten dokumenttien kaveriksi.

* Pikaviestinvalinta
  * Testailtu RocketChattia ja paria Matrix-clienttia (element.io ja cinny)
  * Valinta kallistui Matrix-pikaviestimiin
  * Käyttäjät voivat itse valita haluamansa asiakasohjelman eikä olla sidottuja yhden toimittajan clienttiin
  * Kirjautuminen onnistuu Github-tunnuksilla, jotka pääkäyttäjät tarvitsevat joka tapauksessa jatkossa kun tiketöinti siirtyy GitHubiin
  * E2E salaus tuntuu "valmiimmalta" ja paremmin toimivalta kuin RocketChatin
  * IRC:in tapaan hajautettu eikä riipu yhdestä keskuspalvelimesta
  * Käyttö ei aiheuta mitään lisäkustannuksia (ilmainen on aina kiva)
  * Rocketin etuna oli Thread-tuki, joka vaikuttaisi kuitenkin olevan kehitteillä myös Matrix-yhteisössä
  * Rocket vaikutti melko bugiselta, esimerkiksi Ctrl+F5 näppäinyhdistelmää sai olla hapuilemassa päntiönään

* GitHub
  * Githubin enterprise tai teams-tiliä ei tarvittane, voidaan jatkaa free:llä (ilmainen on aina kiva)
  * Githubin teams-toimintoja voisi testailla esimerkiksi kuvailijoiden viestintätyökaluna, se soveltuisi ehkä kohtalaisen hyvin "ei-reaaliaikaiseen" viestintään
  * Miten saadaan vanhat tiketit talteen, jotta ei menetetä vuosien tietovarantoa? Viedään Redminestä "Palaute" ja "Kehitysehdotukset" projektien tiketit github API:n kautta githubiin, miten tikettinumeroiden kanssa toimitaan?

* Pääkäyttäjien organisointi GitHubiin ja Matrixiin + koulutusta
  * Miten hoidetaan?
  * Pääkäyttjille ohjeistus pääkäyttäjien palsussa GitHub-tunnusten luonnista ja Matrixiin liittymisestä.
  * GitHub-koulutus vähän myöhemmin.

* SmartBox
  * SmartBoxista palaveerataan tämän palaverin jälkeen

* Hyllyvaraukset slavelta
  * Testattu Vaarassa, alussa skandiongelma, joka korjattiin, ilmeisesti ei muita ongelmia havaittu
  * Replikoinnissa kyllä perjantaina lagia, johtui ilmeisesti tilastotaulujen päivittämisestä, täytyy tutkia multithread-replikointia
  * Maanantai aamuna lagi 0 sekuntia

* Kotkan kirjeet kuosissa, tuotantoon tänä aamuna (31.1.)

* PDF-kirjeessä osoitteen asemointi ikkunaan. Lumpeesta lähtevissä kirjeissä kirjaston osoite jää yläreunan alle, pitäisi laskea alemmas.

* Mikroväylän automaatit
  * 99-viestien spämmäyskäytännöstä luovuttu uudessa ohjelmistoversiossa, joka on jo asennettu osaan automaateista.
  * Lainojen uusinta -ominaisuus tulee tulevaisuudessa käyttämään sip2-viestejä oikeaoppisesti (renew).

* Seuraava huoltokatko 9.2.
  * Tietoturvapäivityksiä asennetaan, aiheutuu pieni käyttökatko kuhunkin kimppaan

### Torstain palaveri

* kaikissa kimpoissa internal server error 1.2.2022 klo 15.30 ja klo 19 maissa. Myös 2.2.2022 klo 12 maissa kaikki Kohat kaatui.
  * ongelma johtui MariaDB:n tmp:n täyttymisestä, jonka syynä oletettavasti eräs uusi hankintaraportti
  * konesalioperaattorin valvontajärjestelmässä oli konfiguraatiovirhe, jonka vuoksi levytilanseuranta ei toiminut oikein, operaattori korjaa ja jatkossa hälytykset levytilan loppumisesta saadaan ennen kuin levy on täynnä
  * otetaan käyttöön kokoraja MariaDB-tempeille
  * siirretään raporttien ajo slavelle, jolloin ongelmallistenkaan raporttien ajo ei aiheuta häiriöitä Kohan päivittäiskäyttöön
  * rakennetaan loggeri jolla seurataan temppitilan käyttöä

* päivystysvuorot vko 6 eteenpäin

* Vaara: Verkkomaksujen jako kunnittain #5252
  * Päädyttiin tulokseen, ettei tätä toteuteta. Kommentit tiketissä.

* kaikkiin kimppoihin päälle samat logitukset? Esim. Vaarassa ei ole RenewalLog-päällä, joten tiketin #5220 tietojen haku ei onnistu.
  * interface kirjautuu todennäköisesti väärin verkkokirjastouusinnoissa intranet-uusinnoiksi. Mistä voisi johtua?
  * ongelma on ollut jo pitkään, tutkitaan ja korjataan versiopäivityksen jälkeen
  * yhtenäiset logitukset on hyvä ajatus

* OUTIssa marras-joulukuulla suht paljon niteitä, joille ei ole muodostunut HANK-alkuista viivakoodia editx-tilauksissa. Tämä aiheuttaa jonkin verran ongelmaa automaateilla, koska ne hakevat teoksen tiedot viivakoodin perusteella.
  * Tutkitaan saako niteille lisättyä "dummy" viivakoodin

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-5-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 4 muistio

Aika 24.1.2022 klo 12
Läsnä: Anneli, Emmi, Johanna, Kodo, Lari, Pasi

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-4-muistio

* SmartBox
  * SmartBoxille lähetetty kuvaukset sip2ohttp:stä ja borrowers/statuksesta + SIP2 dokumentaatio.

* Sotu-siilon ylläpitoon muutama uusi työkalu
  * "ssn-cleanup", joka siivoaa siilosta pois asiakastietueissa kiinni olemattomat sotut, ajettava tietokantapalvelimella root-oikeuksin, jotta pääsee tarkastamaan kaikki koha-kannat
  * ehkä voisi tehdä käyttäjän jolla on select kaikkien koha-kantojan borrower_attributes -tauluihin
  * "ssn-allow-findssn" ja "ssn-disallow-findssn" joilla voidaan sallia/poistaa käyttäjän oikeus sotujen hakuun. 

* Varmistukset ja palautukset
  * Palautusten dokumentaatiota lisätty, mutta homma mutkistuu mitä "syvemmän tason" palautuksiin mennään.
  * Hostinodejen /etc -varmistukset käytössä, ei vielä tietokantpalvelimella. Pitäisikö /var varmistaa myös, ehkä ei tarvi?

* Lapin kirjeet viilattu nyt hienoon kuosiin, Kotkan kirjeet ohjelmassa seuraavaksi.

* Mailx bög Lumpeissa ja muualla korjattu.
  * Muutos on kaiketi jäänyt tekemättä viimeisimpinä uuten konesaliin siirtyneille kimpoille.
  * Esimerkiksi editx-virheraportit ja sanomien uudelleenkäsittely ei ole toiminut tämän vuoksi joissain kimpoissa.

* Vaskin automaattipalaveri tulossa.
  * Lari osallistuu, ongelmat kylläkin varmaan automaattipäässä (RFID-lukujen ja deaktivointien/aktivointien hitauteen ei Kohan päällä ole vaikutusta)

* Principio on nyt Githubissa, ylläpito ja täydentely vastaisuudessa sinne.

* Raporttien suojaaminen salasanalla.
  * Raportteja voidaan nyt tarvittaessa suojata salasanalla, hommaa on testattu lainahistoria-raportin kanssa.

* Slavea käyttävä versio holds to pullista testeillä.
  * Vaara lupautui testaamaan, joten sieltäpä sitten kuuluu kuinka toimi.

* MariaDB idle threadit, master.err timeoutit ja wait_timeout
  * Tietokantayhteys pudottelee yli 10 minuuttia vanhat käyttämättömät tietokantayhteydet, näitä ilmoituksia kertyy master.err -lokiin tuhansia päivittäin. Koha ei jostain syystä sulje tietokantayhteyksiä oikein.
  * Jos yhteydet ovat worker-kohtaisia, voitaisiin kenties kasvattaa tuntuvasti wait_timeouttia. Riskinä on se, että idle-yhteyksien määrä voi karata käsistä ja max_connections tulla käyntiin. Tehtävä huolellisesti ja koko ajan tietokantayhteyksiä seuraten.

* Webkakecon
  * Hellestä puuttui webkaken konfiguraatio, josta syystä webkake-lainat eivät näkyneet Helle-Kohassa, korjattu.
  * Ovat ilmeisesti kuitenkin paikallaan muissa kimpoissa.

* Kuljetustilassa olevat noudettavien varausten niteet
  * Tehdään pieni koodimuutos varausten käsittelyyn. Tipautetaan kuljetukset kun varaustauluun tulee merkintä 'W' (Waiting).
  * Muutos voitanee pudottaa versiopäivityksessä, joten kyseessä on tilapäispaikka.

* Koha-Suomi kotisivujen päivitykset
  * Tekstimuutokset, joissa suurimmat höpöhöpöt korjattu
  * Uusi kartta

* Vaskin konversiossa kärsineet maksut nollattu #4972

* Kemin Ceeposkassayhteyksiä ei ole saatu vieläkään toimimaan.

* Sequences-taulun nollautuminen korjattu, eikä tuplaviivakoodeja enää näyttäisi syntyvän #5206

* 3 lainaa uusittu, kuittiin on tulostunut vain 2 uusittuun lainaan uusi eräpäivä #4788

* Vaski-testillä XML-validointi testissä SIPoHTTP:n kanssa Bibliothecan automaattien kanssa.

* Versionvaihtotiketit jaettu kehittäjille.

### Torstain palaveri

* Plackin reload aiheuttaa automaattien putoamisen, koodin työntäminen tuotantoon kesken päivää siis tipauttaa automaatit.
* SmartBoxin toimittajalle kelpaa joko sip2ohttps tai borrowers/status, haluavat palaveerata.
* Asiantuntijaryhmän päätös: editx ja niteen korvaushinta alvittomaksi

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-4-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 3 muistio

Aika: 17.1.2022 klo 12
Läsnä: Ari, Anneli, Emmi, Johanna, Kodo, Lari, Pasi

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-3-muistio

* Vaski: Konvertoituneissa lyhennetyissä maksuissa ongelmia #4972
  * Sovitaan Vaskin kanssa testauksesta  

* Sequences-taulun nollautuminen #5206
  * Jos kimpassa on käytössä useampi kuin yksi prefix, taulu nollaantuu aina kun "uusi" prefix tulee tarkistettavaksi

* Käyttökatko
  * Päivitettiin tietokantapalvelinten käyttikset.
  * Master-palvelimelta kaksi muistikampaa rikki, joten vaihdettiin masteriin kaksi kampaa slavelta. Slaveen vaihdetaan kammat kunhan Fujitsun huolto ehtii paikalle. Slave menee toistaiseksi hieman pienemmällä buffer poolilla, jotta sopii kokonaan ehjään muistiin, ei pitäisi olla vaikutusta juuri mihinkään.
  * Bittiguru ja Fujitsu hoitavat vaihdot, ei aiheuta töitä meille.
  * Slave-palvelimen toinen iSCSI-kortti oli pudonnut linjalta, mutta tokeni bootissa. Fujitsu ei kuulemma vaihda korttia vielä yhdestä häiriöstä, koska kyseessä voi olla esimerkiksi ajuriongelma. En kuitenkaan usko ajuriongelmaan, koska kortit toimivat ongelmitta viidessä kaikkiaan kuudesta nodesta. Jos olisi ajuriongelma, niin putoilisivat muuallakin.
  * Katkoilmoituksesta puuttuu redirect, joten se näkyy ainoastaan Kohan "kotisivun" paikalla, täytyy korjata.

* Versionvaihdon organisointia ja tikettien jakoa aihepiireihin tehty
* Laskutustyökalua on paranneltu ja se on kaikissa kimpoissa testissä.

### Torstain palaveri

* Versionvaihton tehtävänjakoa aloitettiin.

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-3-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022##

---

## Viikko 2 muistio

Aika: 10.1.2022 klo 12
Läsnä: Ari, Anneli, Emmi, Johanna, Kodo, Lari, Pasi

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-2-muistio

* päivystysvuorot vkosta 3 eteenpäin
  * Vko 3 Pasi ja Lari
  * Vko 4 Anneli ja Johanna
  * Vko 5 Emmi ja Kodo

* versionvaihdon aikataulutus?
  * tehdään aikataulutus ma 17.1.2022 viikkopalaverin yhteydessä/jälkeen

* käyttökatko ke 12.1.2022

### Torstain palaveri

* Indeksointihäiriö Lumpeessa, Hellessä ja Vaarassa
  * Indeksimäppäysten käyttöönottoon liittynyt häiriö aiheutti indeksien rikkoutumisen, indeksit palautettiin edellispäivän varmuuskopioista

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-2-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

---

## Viikko 1 muistio

Aika: 3.1.2022 klo 12.00
Läsnä: Anneli, Ari, Johanna, Emmi, Kodo, Lari

"Pääkäyttäjien viikon muistio":https://tiketti.koha-suomi.fi/projects/mls/wiki/P%c3%a4%c3%a4k%c3%a4ytt%c3%a4j%c3%a4t_-_vuosi_2022#Viikko-1-muistio

* Failed-tilaisia sms-viestejä ei ole juurikaan?
  * OUTIlaiset kysyvät Link Mobilityltä, lähetetäänkö kuittauksia edelleen.

* Perjantain nimipalvelinongelma ja tiedotus
  * Kysymyksissä oli MPY:n nimipalvelimille kohdistunut palvelunestohyökkäys.
  * Laaditaan tiedotussuunnitelma niitä tilanteita varten, että nimipalvelin ei toimi.
  * Tiedotetaan vielä pääkäyttäjiä ja kirjastojen johtajia ongelman syistä ja korjauksesta.

* Huoltokatko 12.1.
  * Read erroreita bethillä kun workereitä kierrätetään. Muilla nodeilla ei ongelmaa saman datan kanssa. Huoltokatkossa beth kaapeloidaan uusiksi.
  * Päivitetään tietokantapalvelinten käyttis, josta lyhyt käyttökatko kaikissa kimpoissa.
  * Väsätään huoltokatko-ilmoitus, joka voidaan ottaa käyttöön kerralla kaikissa kimpoissa suoraan host-nodeilta.

* NFS-katkomista testattu muuttamalla offsite-synkkausta siten ettei se satu päällekkäin onsite-varmistusten kanssa. Ratkaisu ei ole pysyvä, koska esimerkiksi tuntidumpit päivittyvät nyt offisitelle turhan harvoin, mutta tällä voidaan tarkistaa liittyykö katkoitu offsite-varmistuksiin.

* Sähköpostiasetuksia oiottu tuotannoissa, jolloin sähköpostin lähettäminen myös koha-suomi.fi laatikoihin onnistuu. Paha vain kun sähköpostit menevät spämmiin tutanotassa. SPF:n pitäisi olla DNS:llä kunnossa, missähän mahtaa olla vika? Hellessä ja Kyytissä konfiguraatiossa oli muutakin viilattavaa.

* Nodet varmuuskopioivat nyt myös kontainerien roottitiedostojärjestelmät ja host-toolsit. Homma toimii siten että nodet "sopivat" keskenään mikä niistä milloinkin tekee varmistukset, jolloin varmistus voidaan pitää jokaisen noden crontabissa ilman että tapahtuu päällekkäisiä varmistuksia.
  * *Muistakaa ottaa varmuuskopion salasana talteen omaan salasanahallintaanne!*

* ko-db-connections lisätty tietokantapalvelimelle, se laskee avoimien SQL-yhteyksien määrän. Jos ilmenee jossain vaiheessa tahmaa tietokantayhteyksissä, niin tällä voi tsekata onko raja täynnä (tällä hetkellä 1200). Jos raja täynnä, niin muutos tietokantapalvelimen konfiguraatioon sekä mysql-clientillä suoraan käynnissä olevalle palvelimelle, ei muistaakseni tarvitse mariadb-restarttia.

* Automaattikummittelut OUTIssa vähentyneet todella paljon. Yksittäisiä häröjä ilmenee, mutta se nyt ei ole OUTIn automaattimäärällä mikään ihme.

* Vaara uudelleenindeksoitu, indeksissä oli ihmeellisiä reikiä.

* Teostietonäytön optimointiajatus
  * Kirjastoryhmittäinen välilehti + laiska lataus, jolloin kerralla ladattavaa nidemäärää saadaan karsittua rajusti.
  * Tiketissä #345

* Vastuunjako Bittigurun ja Koha-Suomen välillä
  * Tietokantapalvelinten keskinäisestä työnjaosta keskusteltu Bittigurun kanssa, vastuunjako tässä suhteessa epäselvä. Liittyy mariadb:n asetuksiin, jolla ei ole selkeää vastuuhenkilöä. Onko edes osoitettavissa välttämättä, koska osa astuksista liittyy selvästi palvelin- ja laitealustaan ja osa taas ohjelmistopuolen optimointeihin. Kumpaan näistä tuo työnjakokuvio kuuluu?
  * Kutsutaan koolle kokous ja ryhdytään työstämään vastuunjakotaulukkoa OUTIn RACI-matriisin pohjalta. Aikataulullisesti sijoittuu varmaankin tammi-helmikuun taitteeseen, meiltä Ari, Kodo ja Lari.

### Perjantain palaveri

* Huoltokatkoilmoitus
  * Kodo tehnyt huoltokatkoilmoituksen, jolla voi estää käyttäjien pääsyn Kohaan huoltokatkojen aikaan.

* DNS-DDOS tiedote lähtenyt pääkäyttäjille ja johtajille

* Tiedostojen metsästely vanhalta LummeStagingilta ja kadonneiden lampaiden palautus Redmineen
  * Johanna kävi Diseciltä hakemassa puuttuvat tiedostot ja Kodo laittoi ne paikoilleen.

* Laskutusliitännäiseen uusia ominaisuuksia
  * Laskutettavien listaaminen näytölle laiskalla latauksella.
  * Laskujen massaluonti.

* Versionvaihdon aikataulutus?
  * Asiakasryhmällä ja summalla suodattaminen.
  * Uusi lähetystapa: Einvoice. Laskut voi laittaa lähtemään asiakkaille e-kirjeenä.

"Palaa muistion alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022#Viikko-1-muistio | "Palaa sivun alkuun":https://tiketti.koha-suomi.fi/projects/mls/wiki/Kehitt%C3%A4j%C3%A4t_-_vuosi_2022

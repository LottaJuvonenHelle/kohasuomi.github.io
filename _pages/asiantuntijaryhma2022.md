---
layout: single
permalink: /asiantuntijaryhma2022
hidden: true
header:
  overlay_color: '#5e616c'
  overlay_image: /assets/images/cropped-pexels-photo-113850.jpeg
toc: true
title: 'Koha-Suomen asiantuntijaryhmä 2022'
---

Koha-Suomen asiantuntijaryhmän kokoukset vuonna 2022.

## Muistio 9/22

Aika 12.12.2022 klo 9
Läsnä: Anneli Österman, Kodo Korkalo, Ari Mäkiranta, Kati Sillgren, Päivi Knuutinen, Susanna Sandell, Tuomas Kunttu, Leena Kinnunen

### 1. Arin ajankohtaiset

* Lasse Pouru aloittaa 12.12.2022 Johannan sijaisena. Lasse työskentelee Turussa.
* GIthub testausta tehtiin 2 kuukautta ja kokemukset puoltavat siirtymistä Githubiin.

### 2. Versionvaihto

Testikannat käyttöön mahdollisimman pian. Tavoiteaikataulu versionvaihdolle ti 16.5.2023. Optiona jatketaan tarvittaessa ke 17.5.2023. Selvitetään kimpoissa onko 1,5 päivän kiinniolo ok.

Edellisessä versionvaihdossa huomatut ongelmat
* testaamaan päästiin liian myöhään.
* testikantaan vietävä datamäärä turhan iso, pienempikin määrä riittää testaukseen.
* cronien päälle laittaminen
  * ei ollut tietoa, mitkä päällä ja milloin ne laitetaan päälle
* Kansalliskirjaston/Finna-toimiston kanssa aikataulusta sopiminen
  * tehdään keskitetymmin Koha-Suomen kautta
* testaus piti tehdä moneen kertaan
* versionvaihto oli lähellä kesälomakautta ja tekijöitä jäi heti lomille ja pieni joukko jäi tekemään jälkisiivouksia
* katkon ajankohta
  * tieto mahdollisimman pian kirjastoille
* rajapinnat
* tiedotus - missä mitäkin löytyy oli epäselvää
* kuvailu - työkalut valmistuivat hitaasti
* testikannassa tarvittaisiin käyttöön kaikki toiminnot
* tieto/listaus, mitkä ei toimi käyttöönotossa

### 3. Kehitysehdotusten läpikäyntiä

Käsiteltävät tiketit:

Käsiteltiin Redminestä tiketit:
* #5381
* #5391
* #5403
* #5415

GitHubista käsiteltiin tiketti: 
* [koha 274](https://github.com/KohaSuomi/Koha/issues/274)

Kuhunkin tikettiin kirjattiin päätös.

### 4. Vaskin itsepalveluautomaattien kilpailutus

Susanna kertoi lyhyen koosteen kilpailutuksesta. Koko tarjouspyyntö: [Tarjouspyynto12092022.pdf](https://github.com/KohaSuomi/kohasuomi.github.io/files/12076801/Tarjouspyynto12092022.pdf)

### 5. Seuraava kokous

Seuraava asiantuntijaryhmän kokous ma 16.1.2023 klo 9.

### 6. Muut asiat

Tuomaksen PowerBI-esittely 25.1.2023 klo 9-11.

---

## Muistio 8/22

Aika: 14.11.2022 klo 13
Läsnä: Anneli Österman, Kodo Korkalo, Päivi Knuutinen, Susanna Sandell, Kati Sillgren, Ari Mäkiranta, Noora Valkonen, Tuomas Kunttu, Katja Valjakka
Poissa: Pia Kusmin

### 1. Arin ajankohtaiset

* Yhtiöllä aloitti harjoittelija, joka jatkaa toukokuuhun 2023 saakka. 
* Johannan sijaisena aloittaa Lasse Pouru, joka aloittaa 12.12.2022 ja työskentelee Turussa.

### 2. Tiekartan tilanne

Käytiin läpi ja päivitettiin tiekartta.

[Tiekartta2022paivitysmarraskuu.xlsx](https://github.com/KohaSuomi/kohasuomi.github.io/files/12076809/Tiekartta2022paivitysmarraskuu.xlsx)

### 3. Kehitysehdotusten läpikäyntiä

Jatkossa kehittäjä mukana.

Käsiteltävät kehitysehdotukset:
* [Redmine #4717](https://tiketti.koha-suomi.fi/issues/4717)- Nalkutin ei huomauta tuplapääkirjauksesta
* [Redmine #4781](https://tiketti.koha-suomi.fi/issues/4781) - Maksujen poisto eräajona
* [Redmine #4807](https://tiketti.koha-suomi.fi/issues/4807) - Varaustunnnus asiakkaan lisämääreeksi
* [Redmine #4815](https://tiketti.koha-suomi.fi/issues/4815) - Eräpäiväilmoituksiin tieto varatusta niteestä
* [Redmine #4816](https://tiketti.koha-suomi.fi/issues/4816) - Kirjastokortin numeron syöttäminen jaksottain
* [Redmine #4891](https://tiketti.koha-suomi.fi/issues/4891) - Support robots.txt rate limit in check-url-quick.pl
* [Redmine #4892](https://tiketti.koha-suomi.fi/issues/4892) - Make the SELECT query in check-url-quick.pl non-blocking
* [Redmine #4920](https://tiketti.koha-suomi.fi/issues/4920) - Lainojen uusinta -toiminto: uusinnan eräpäiväkalenterin valittavaksi vaihtoehdoksi Muista istunnolle
* [Redmine #4950](https://tiketti.koha-suomi.fi/issues/4950) - Viivakoodien lisääminen tarratulostukseen listan kautta
* [Redmine #4964](https://tiketti.koha-suomi.fi/issues/4964) - Työkalut, MARC-muokkauksen pohjat: mahdollisuus lisätä tietueella jo olemassa olevan kentän uusi kenttätoistuma
* [Redmine #4965](https://tiketti.koha-suomi.fi/issues/4965) - Työkalut, MARC-muokkauksen pohjat: kentän indikaattorien käsittelymahdollisuus
* [Redmine #5064](https://tiketti.koha-suomi.fi/issues/5064) - Helle: Finna-rajapintaan tarvitaan määritys siitä, että itse lisättyjen maksutyyppien maksut eivät vaikuta asiakkaan lainakieltorajaan eikä varauskieltorajaan
* [Redmine #5069](https://tiketti.koha-suomi.fi/issues/5069) - Niteiden muokkaukseen/lisäykseen nidetyypin automaattinen valinta
* [Redmine #5129](https://tiketti.koha-suomi.fi/issues/5129) - Asiakkaan viestiasetuksiin Ei ilmoitusta-toiminto
* [Redmine #5152](https://tiketti.koha-suomi.fi/issues/5152) - KohaSuomi Microservices -palvelun Reports-sivulle haku-laatikko
* [Redmine #5276](https://tiketti.koha-suomi.fi/issues/5276) - Siirtoraportti-liitännäiseen vieraillut linkit eri väriseksi
* [Redmine #5298](https://tiketti.koha-suomi.fi/issues/5298) - Finna-haun upottaminen kirjaston verkkosivuille
* [Redmine #5306](https://tiketti.koha-suomi.fi/issues/5306) - Kalenterin sulkupäivien muokkaukseen lisäominaisuus
* [Redmine #5307](https://tiketti.koha-suomi.fi/issues/5307) - Pikahakuun poistoruksi
* [Redmine #5334](https://tiketti.koha-suomi.fi/issues/5334) - Lainakuitin tulostus printteripainikkeesta tulostaa asiakkaan kaikki lainat

Kaikki listatut kehitysehdotukset käytiin läpi. Osa hylättiin, lopuille mietittiin toteutusaikataulua ja toteutetaanko se itse vai tehdäänkö suoraan tiketti yhteisöön. Päätökset kirjattiin aina tikettiin.

### 4. Strategia-pajan koonnin läpikäynti

Koha-seminaarissa oli 28.10.2022 strategia-paja. Käytiin läpi "pajan yhteenveto":https://tiketti.koha-suomi.fi/attachments/5663/Koha-SuomiOystrategianarviointi2022.pdf.

### 5. Muut asiat

* Sähkökatkoihin varautuminen.
  * Konesalissa sähkönsyöttö on kahdennettu (kuten kaikki muukin), eli virtaa saadaan kahta erillistä piuhaa pitkin.
  * Lisäksi on vielä erillinen varavirtalaite, joka hyppää puikkoihin siinä vaiheessa jos molemmat syöttölinjat ovat pimeinä, tällä varavirtalaitteella pärjätään jonkin aikaa, tarkkaa aika ei tiedossa.
  * Nimipalvelun tarjoaja MPY (Mikkelin puhelin yhdistys) hallinoi koha-suomi.fi-osoitteita. Heillä on käytössä järeät UPS-laitteet (nopeasti reagoiva pieni varavirtalaite) ja varavoimalaite. Käytännössä UPS-hoksaa heti kun sähköt katkeavat ja syöttää laitteille virtaa niin kauan että varavoimalaite ehtii hätiin. Varavoimalaite syöttää virtaa niin kauan kuin sille on polttoainetta saatavana.
  * Palvelujen kannalta sähkökatkojen ei pitäisi tulla näkyväksi muuten kuin korkeintaan kuntien sähköjärjestelmien häiriöiden vuoksi, jolloin työasemille tai verkkolaitteille ei välttämättä kunnan sisällä ole virtaa tarjolla. 
    * Kunnissa on mahdollisesti voitu varautua sähkökatkoihin varustamalla työasemat ja verkkolaitteet varavirralla, halutessanne voitte tarkistaa asian omasta kunnastanne.
  * Kohalle on kaksi offline-lainausjärjestelmää Koha offline circulation (Windows-ohjelma) ja Koha offline circulation tool (Firefox-liitännäinen), jotka kumpikin toimii. Niiden käyttöä kannattaa harjoitella ennen tositilannetta.
  * Kunnissa kannattaa miettiä, missä tilanteessa kirjasto laitetaan kiinni.

* Keskusteltiin, voisiko Tuomas pitää PowerBI-esittelyn.
  * sql-raportit jakoon kaikille jo ennakkoon

* Versionvaihto tapahtuu toukokuussa 2023. Asiantuntijat/pääkäyttäjät selvittävät onko kimpoissa sellaisia päiviä, jolloin päivitystä ei voi tehdä. 

---

## Muistio 7/22

Aika: 10.10.2022 klo 9
Läsnä: Anneli Österman, Pia Kusmin, Tuomas Kunttu, Päivi Knuutinen, Katja Valjakka, Susanna Sandell, Kati Sillgren, Ari Mäkiranta, Noora Valkonen

### 1. Arin ajankohtaiset

* Määräaikainen kehittäjä on etsinnässä. Töitä olisi ainakin marraskuun 2023 loppuun saakka.
 

### 2. Tietojen säilytysajat

[Tietojen säilytysajat](https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/Tietojen_s%C3%A4ilytysajat) -wikisivulla ei ole selkeitä päätöksiä. Tarkistetaan päätökset ja selkiytetään tiedot.

### 3. Koha-Seminaari

To 27.10 yhteinen päivä tieteellisten kirjastojen kanssa. Pe aamupäivänä strategiatyöpaja yhtiön strategian uudistamiseksi. Esitykset striimataan.

Aamu 10-12
Avaus 10-10.10
10.10-10.30 Koha-Suomi tiekartta (Ari Mäkiranta)
10.30-11.00 Tieteelliset tiekartta (Pekka Uotila)
11.00-11.20 KohaCon 2023 (Esa-Pekka tai Andrii)
11.20-11.40 Bibframe (Kansalliskirjasto)
11.40-12.00 Tiedolla johtamisen projekti (Rebekka Pilppula)
12-13 Lounas

Iltapäivä
Työpajat
13-13.15 Ryhmiin jakautuminen
13.15-14.30 työpajat 1. Ideoiden vaihto ja hyvät käytännöt 
14.30-15.15 2. Tekninen työpaja 
15-15.45 Purku ja lopetus

Pe 9-12 Yleisten Koha-kirjastojen strategiapaja


---

## Muistio 6/22

Aika: 16.9.2022 klo 10-11.30
Läsnä: Ari Mäkiranta, Kati Sillgren, Katja Valjakka, Päivi Knuutinen, Pia Kusmin, Susanna Sandell, Anneli Österman

*Aiheet*

### 1. Arin ajankohtaiset

* Kirkes-kimpan liittymisprojekti on aloitettu. Alustava aikataulu käyttöönotolle on syksy 2023.
* Palvelinsalissa on 2 kertaa hajonnut tietokantapalvelimien muistikampoja uudelleen käynnistyksen yhteydessä. Tämä viittaa vikaan joko emolevyissä tai virransyötössä. Bittiguru tutkii asiaa yhdessä laitteiden valmistajan eli Fujitsun kanssa.
* Määräaikaisen kehittäjän rekry laitetaan pian auki.
* KohaCon23 järjestetään elokuussa 2023 Helsingissä, Kansalliskirjasto järjestelyvastuussa. Koha-Suomi osallistuu järjestelyihin jollain tasolla.

### 2. Työryhmien vuosisuunnitelmat

Käytiin läpi pääkäyttäjä- ja kuvailuryhmän vuosisunnitelmat ja hyväksyttiin ne.

Pääkäyttäjät: [paakayttajatvuosisuunnitelma2022.docx](https://github.com/KohaSuomi/kohasuomi.github.io/files/12076821/paakayttajatvuosisuunnitelma2022.docx)

Kuvailijat: [kuvailijatvuosisuunnitelma2022.docx](https://github.com/KohaSuomi/kohasuomi.github.io/files/12076825/kuvailijatvuosisuunnitelma2022.docx)

### 3. Henkilötunnuksettomien asiakkaiden voimassaoloaika

Vaarassa, Kyytissä ja Vaskissa on käytössä toimintatapa, että henkilötunnuksettomien asiakkuuden voimassaoloaika on yksi vuosi. Päivi pyysi Itä-Suomen AVIlta selvityksen, voiko henkilötunnuksettomien asiakkuus olla voimassa lyhyemmän ajan kuin muiden asiakkaiden. AVIsta oli pyydetty kannanotto yhdenvertaisuusvaltuutetulta


> Yhdenvertaisuuslain 8 §:n syrjinnän kiellon nojalla ketään ei saa syrjiä iän, alkuperän, kansalaisuuden, kielen, uskonnon, vakaumuksen, mielipiteen, poliittisen toiminnan, ammattiyhdistystoiminnan, perhesuhteiden, terveydentilan, vammaisuuden, seksuaalisen suuntautumisen tai muun henkilöön liittyvän syyn perusteella. Syrjintä on kielletty riippumatta siitä, perustuuko se henkilöä itseään vai jotakuta toista koskevaan tosiseikkaan tai oletukseen.
> 
> Hetuttomuus voi olla tällainen YVL 8 §:ssä mainittu muu henkilöön liittyvä syy, eikä henkilöä saa siis asettaa muita epäedullisempaan asemaan hetuttomuuden perusteella, jollei sille ole lain hyväksymää oikeuttamisperustetta. YVL 11 §:n mukaan oikeuttamisperuste on olemassa, jos erilaisella kohtelulla on hyväksyttävä tavoite ja keinot tavoitteen saavuttamiseksi ovat oikeasuhtaisia.
> 
> Vaikka kirjastokorttien voimassaolon rajoitus asettaa hetuttomat henkilöt eri asemaan, on korttien voimassaolorajoituksilla kuitenkin hyväksyttäviä ja oikeasuhtaisia tavoitteita kirjaston toiminnan turvaamiseksi. Emme myöskään katso, että kirjastokortin uusiminen välttämättä asettaa hetuttomat henkilöt sellaiseen epäedulliseen asemaan, mitä voitaisiin tulkita syrjinnäksi yhdenvertaisuuslain nojalla. Tällaisesta tilanteesta voisi olla kyse, jos hetuttomien henkilöiden kirjastopalveluita tai lainausoikeutta olisi rajoitettu laajemmin.

**Päätös**: 

Todettiin, että henkilötunnuksettomilla voi lausunnon perusteella olla lyhyempi kirjastokortin voimassaoloaika.

Vuoden määräajalla jatkavat: Vaara, Vaski, Kyyti?
Sama voimassaoloaika kuin henkilöasiakkailla: Lappi, OUTI, Helle, Lumme, Siilinjärvi?

Tarkistetaan Kirkes.

### 4. Kellutus

Kehittäjät toivoivat keskustelua, onko tarpeen toteuttaa ominaisuus, että aina vaaditaan kellutusryhmä, jotta kellutusta tapahtuisi. Vai riittääkö vain, että FloatRules -asetuksessa tehdään määritykset. 

Todettiin keskustelujen pohjalta, että nykyinen tapa, että kellutuksen voi määrittää pelkästään joko kellutus/kirjastoryhmällä tai FloatRules-asetuksella antaa enemmän mahdollisuuksia kuin tilanne, jossa aina pitää olla kellutusryhmä.

**Päätös**: Säilytetään nykyinen tapa, että ei vaadita kellutusryhmää.

### 5. Tiketit Githubiin - testiaika

Sovitaan ajankohta, jolloin käytetään tiketöinnissä testauksen vuoksi pelkästään Githubia. Testin tarkoituksena on kokeilla, soveltuuko Github tiketöinnissä ja niiden hallinnoinnissa korvaamaan Redmineä.

*Päätös*: Testiaika loka-marraskuu, jonka jälkeen pääkäyttäjäryhmä arvioi, soveltuuko Github meidän käyttöön. Asiantuntijaryhmä tekee pääkäyttäjien ja kehittäjien arvion pohjalta päätöksen.

### 6. Koha-seminaari

Helsingissä 27.-28.10.2022. Ohjelma.


* tiekartan esittely
* yhtiön uusi strategia
* tiedolla johtamisen projektin tuloksia
* tieteellisten aiheet
* bibframe? - esitys ja työpaja

Työpaja
* bibframe
* strategia
* hyvien käytäntöjen jako -paja

Ari jatkaa yhteydenpitoa tieteellisten puolelle. Ilmoittautuminen tulossa, Kansalliskirjasto organisoi.


### 7. Tiekartan tilannekatsaus

Käytiin läpi tiekartta ja merkittiin vihreällä valmistuneet osiot.

Päivitetty tiekartta: attachment:Tiekartta2022paivityssyyskuu.xlsx

### 8. Muut asiat

* Koha-Suomi-domain sähköpostiosoitteessa
  * Vaski haluaa pitää käytössä vaskikirjastot.fi-osoitteen. Vaskissa on tehty spf-sääntö vain vaskikirjastot.fi-domainille ja ongelmia ei ole. Ei kuntakohtaisia sääntöjä. OUTIssakin on ollut käytössä outikirjastot.fi-domain ja spf-sääntö on jouduttu tekemään kaikkiin kuntiin. Testataan lisää, mistä tällainen päinvastainen kokemus johtuu.

* Virkailijaliittymässä tehdyssä uusinnassa tilastoitumiskirjastona käytetään virkailijan kirjautumiskirjastoa, ei lainannutta kirjastoa. Eräpäivä menee lainanneen kirjaston eräpäiväkalenterin mukaan, vaikka laina uusitaan toisessa kirjastossa. Onko tämä toimintatapa ok vai pitäisikö uusinta kirjautua tällaisessakin tapauksessa lainanneen kirjaston mukaan?
  * **Päätös**: toimintatapa on looginen, ei vaadi muutosta.

### 9. Seuraavat kokoukset

Ma 10.10. klo 9
Ma 14.11. klo 13
Ma 12.12. klo 9

---

## Muistio 5/22

Aika: 30.5.2022
Läsnä: Leena Kinnunen ja Pia Kusmin (Lappi), Tuomas Kunttu (Kyyti), Päivi Knuutinen (Vaara), Susanna Sandell (Vaski), Noora Valkonen (OUTI), Ari Mäkiranta (Koha-Suomi), Kati Sillgren (Helle), Katja Valjakka (Lumme), Anneli Österman (Koha-Suomi)

*Aiheet*

### 1. Arin ajankohtaiset

* Kehittäjien työaika mennyt lähes kokonaan versionvaihdon valmisteluun.
* Asiantuntijaryhmän jäsenet kaudelle 2022-23. Kimpoista pitäisi saada ehdotukset elokuun alkuun, kun uusi hallitus kokoontuu ensimmäisen kerran.
* Korkeakouluharjoittelija Antti Kiviniemi aloittaa Joensuussa 6.6.2022.

### 2. Kohan itsepalvelulainauksen piilotukset ja pin-koodi

Tietetoturvasyistä aiemmin on piilotettu itsepalvelulainauksesta vanhemmat lainat. Nyt tiedot tarvitaan mm. Vaara-kirjastoissa näkyviin, jotta asiakkaat voivat uusia vanhempia lainojaan.

**Päätös**: Pyritään siihen, että itsepalvelussa laitetaan kaikkialla pin-koodikysely päälle ja jätetään lainat näkyville. Piilotetaan maksut-välilehti css:llä, koska koko maksuhistoria näkyy ja voi olla asiakkaalle hämmentävä.

### 3. Versionvaihdon kuulumiset

Versionvaihdon valmistelu edennyt hyvin vain muutama isompi yllätys on tullut vastaan, mutta nekin on saatu ratkaistua. 25.-30.5 tehtiin koeponnistus, jossa testattiin testikantojen päivitys ja palautus. Aikataulun riittävyys tarkistetaan kehittäjien viikkopalaverissa 30.5.2022.

Kaikille käyttäjille suunnatun uusien ominaisuuksien esittely-diasarja tulossa. Mahdollisesti videoita, jos ehditään.

### 4. Henkilötunnuksettomien asiakkuuden voimassaoloaika

Vaarassa, Kyytissä ja Vaskissa on käytössä toimintatapa, että henkilötunnuksettomien asiakkuuden voimassaoloaika on yksi vuosi. Edellisessä kokouksessa päätettiin selvittää, olisiko yhteneväisyyden vuoksi mahdollista ottaa käyttöö kaikissa kimpoissa sama toimintapa.

Vaara, Kyyti, OUTI ja Vaski kysyvät alueensa AVI:lta linjauksen, miten henkilötunnuksettomien asiakkaiden voimassaoloaika voidaan määrittää. Voidaanko lainausoikeus rajata lyhyemmäksi kuin normaalisti henkilöasiakkailla. Päivi koordinoi.

### 5. Koha-seminaari

Viikolla 43 Helsingissä, ehdotetaan tieteellisille kirjastoille alustavasti to-pe 27.10.-28.10.2022. Toivotaan runsasta live-osallistumista, mutta selvitellään esitysten striimaamista.

Aiheita:
* tiekartan esittely
* yhtiön uusi strategia
* tiedolla johtamisen projektin tuloksia
* tieteellisten aiheet
* puhuja Ruotsista?

Ehdotuksia aiheiksi voi lähettää Arille tai Annelille elokuun puoliväliin mennessä.

### 6. Muut asiat

Annelin on tarkoitus aloittaa vuoden 2023 alusta kahdeksi vuodeksi 100 % Koha-Suomen pääkäyttäjänä.

---

## Muistio 4/22

Aika: 9.5.2022 klo 13.15
Läsnä: Päivi Knuutinen, Ari Mäkiranta, Pia Kusmin, Asko Autio, Kodo Korkalo, Tuomas Kunttu, Johanna Räisä, Kati Sillgren, Katja Valjakka, Anneli Österman

### 1. Arin ajankohtaiset

### 2. Kirjastokorttien vanhenemisaika

Päätettiin, että henkilöasiakkaiden (lapset ja aikuiset) tietojen voimassaoloaika on 10 vuotta. Muutos tehdään syksyyn mennessä. Kyyti ja Lumme käyttää asian johtoryhmissä.

Osalla kimpoista on lisäksi käytössä käyttösääntö, että henkilötunnuksettomien asiakkaiden tilin voimassaoloaika on 1 vuosi. Loput kimpat selvittää, voisiko toimintatavan ottaa käyttöön myös muissa kimpoissa.

### 3. Nimen piilotus uudessa versiossa eri näytöillä

[Nimen piilotus eri näytöillä](https://tiketti.koha-suomi.fi/issues/4602)

**Päätös**: Piilotetaan asiakkaan infoboksi vasemmasta reunasta ja tarpeen mukaan asiakkaan yhteystietoja poppareista CSS:llä.

Asiakkaan nimi näkyy jatkossa lainausnäytöllä.

### 4. GDPR:n mukainen asiakastietojen katselun lokitus

[GDPR:n mukainen asiakastietojen katselun lokitus](https://tiketti.koha-suomi.fi/issues/4633)

Halutaan lokitettavaksi:
* kun asiakastietoja muutetaan, kirjataan sekä vanha että uusi arvo
  * tärkeää myös, onko muutoksen tehnyt asiakas itse vai virkailija
* Lokitetaan asiakastietojen katselu asiakastiedoissa (kaikki alasivut) ja asiakashaussa

### 5. Viestin lähetysmaksu viestityypeittäin

Palautuskehotusmaksu viestipohjaan. Voi syntyä useampi maksu, jos asiakas lainannut samalla eräpäivällä useammasta kirjastosta. Onko ok ja lainmukainen?

Päätös: Jatketaan selvittelyä versionvaihdon jälkeen ja tutkitaan saadaanko estettyä tuplamaksut.

### 6. Tiekartta

Käydään läpi tiekartta. Liitteenä attachment:Tiekarttayleinenosa.pdf, attachment:Tiekartta2022valmistelu.xlsx, attachment:tiekartta2022.pdf

**Päätös:** Hyväksytään tiekartta. Jatkossa seuranta tehdään vuoden ensimmäisessä kokouksessa.

### 7. Seuraava kokous

Ma 30.5.2022 klo 9.15.

---

## Muistio 3/22

Aika: 16.3.2022 klo 9.15
Läsnä: Ari Mäkiranta, Asko Autio (Vaski), Noora Valkonen (OUTI), Pia Kusmin (Lappi), Susanna Sandell (Vaski), Kati Sillgren (Helle), Päivi Knuutinen (Vaara), Anneli Österman, Tuomas Kunttu (Kyyti)

### 1. Arin ajankohtaiset

* Kehittäjien työaika suunnataan pääosin versionvaihtoon
* Smartbox integraatiota edistetään Rovaniemen kanssa
* Toveri-integraatio vaatii versiopäivityksen yhteydessä muutoksia. Vaihtoehtoina Plugin-toteutus tai SIP2overhttps tuki Tovereihin
* Melindaan liittyvä jatkokehitys tapahtuu aikaisintaan syksyllä Kansalliskirjaston henkilöstöresurssien vuoksi.

### 2. Versionvaihto

[Järjestelmäasetuksista ja uusista ominaisuuksista](https://tiketti.koha-suomi.fi/projects/versionvaihto/wiki/Uusia_ominaisuuksia) keskustelu käydään GitHubin keskustelupalstalla, jotta yksi aihe pysyy koossa. Lopputulema kirjataan suosituksena "Uusia ominaisuuksia":https://tiketti.koha-suomi.fi/projects/versionvaihto/wiki/Uusia_ominaisuuksia -wikiin. Huomioitava, että asetuksissa pitää ottaa huomioon kimpan käyttösäännöt.

[Versionvaihdon aikataulu](https://tiketti.koha-suomi.fi/projects/versionvaihto/issues/gantt).

### 3. Tiekartta

Käytiin läpi tiekartta ja tehtiin alustava aikataulutus tuleville vuosille. Priorisointi on tehty aiemmissa kokouksissa. Liitteenä tiekartan valmistelu-tiedosto. attachment:Tiekartta2022valmistelu.xlsx

### 4. Asiakastietojen vanhentuminen ja lainakielto

Kimpoissa käydään keskustelu, voidaanko siirtyä pidempään (10-100 v) henkilöasiakkaiden (lapset ja aikuiset) asiakkuuden voimassaoloaikaan, jotta asiakkaan kirjaston käyttö ei esty.

Liitteenä kimppojen nykyiset asiakastietojen voimassaoloajat. attachment:Kimppojenasiakkuuksienvoimassaoloajat.docx

### 5. Muut asiat

Ei muita asioita.

### 6. Seuraava kokous

Seuraava kokous on ke 13.4.2022 klo 13.15.

---

## Muistio 2/22

Aika: 23.2.2022 klo klo 9.15
Läsnä: Ari Mäkiranta, Anneli Österman, Päivi Knuutinen, Pia Kusmin, Katri Sillgren, Noora Valkonen, Asko Autio, Tuomas Kunttu


### 1. Arin ajankohtaiset

* Palvelinsali alkaa olla hyvässä vaiheessa  eikä isompia muutoksia sinne tarvitse tällä hetkellä tehdä. säännöllisissä huoltoikkunoissa käyttökatkoja tulee lähinnä silloin, kun palvelinten käyttöjärjestelmiä päivitetään.
* Varastokirjasto on aloittanut kaukolainaprojektinsa ja he pitävät Koha-Suomea ajantasalla ja kysyvät meiltä matalalla kynnyksellä tietoja.
* smartbox paketinnoutoautomaatit. Smartbox on testaillut Kohan rajapintaa heidän järjestelmäänsä ja se näyttää toimivan halutulla tavalla. Ainakin Lapissa on ollut kiinnostusta palveluun ja seuraavaksi palvelua on tarkotus testata Rovaniemellä oikean automaantin avulla. 

### 2. Tiekartta

Pe 25.2.2022 Koha-Suomen tiekartta-webinaari.

### 3. Versionvaihto

Aikataulu. Kimppojen toiveet ja esteet.

**Päätös**: tavoitteena versionvaihto ti 7.6.2022, vähintään yksi päivä kiinni, tarvittaessa puoltoista päivää. Pyritään saamaan e-aineistot mahdollisimman nopeasti auki.

Kehittäjien työaika suunnataan tästä lähtien versionvaihtoon ja hoidetaan vain kriittiset muut tehtävät. Kirjastoilta tarvitaan keväälle iso työpanos uuden version testaukseen.

### 4. Koha-seminaari

Syksyllä? Tieteellisille ehdotetaan aikahaarukkaa syyskuun lopusta lokakuun loppuun.

Aiheita?
* tiedolla johtaminen
* esitys tiekartasta?
* yhtiön strategia
* uudet alustat = GitHub Redminen tilalle
* versionvaihdon kokemukset

### 5. Muut asiat

Helle: Osoite ja lainakielto

Hellen johtoryhmä on käsitellyt kahdessa viimeisimmässä kokouksessaan Kohan asiakastietojen päivitystarvetta sekä siihen liittyvää automaattista lainauskieltoa.

Helle-johtoryhmän kokouksessa pe 18.2.2022 mainittiin nämä:
-	toiminnon tulisi toimia niin, että asiakkaalle ei mene automaattisesti lainauskieltoa
-	tai vaihtoehtoisesti: saisiko asiakastietojen päivitystarpeeseen liittyvän viestin (MEMBERSHIP_EXPIRY) lähetyksen asiakkaille niin, että viesti ei ole kytköksissä asiakastilin vanhentuminen -automatiikkaan

Kirjaston asiakkaan lainauskiellosta on kysytty Kuntaliiton lakimies Minna Antilalta:
Hänen kantansa oli, että lainausoikeutta ei voi kytkeä tietojen päivitysvaatimukseen.
Perusteena se, että yksilön sekä oikeudet että velvollisuudet pitää säätää laissa, ja koska 
kirjastolaki ei säädä tällaista perustetta lainausoikeuden menetykselle, peruste ei ole lainmukainen.

Ote kirjastolaista:

15 §
Lainauskielto ja kirjaston käyttökielto
Kirjaston käyttäjä ei saa lainata kirjaston aineistoja, jos hän ei ole palauttanut aiemmin lainaamiaan aineistoja 14 §:ssä tarkoitetuissa käyttösäännöissä määrätyssä määräajassa tai suorittanut 12 §:n 2 momentissa tarkoitettuja maksuja (lainauskielto). Lainauskielto päättyy välittömästi, kun aineisto on palautettu tai maksut on suoritettu.

Kohan asiakastiedoissa on nämä asiakkaalle lainauskiellon aiheuttavat valittavat toiminnot.
Tarkista osoite – tämä piiloon/pois käytöstä?

Aikuinen-asiakastyypin asiakastietoon lisätty Tarkista osoite = kyllä

**Päätös:** Kerätään kaikkien kimppojen asiakastietojen voimassaoloaika. Tieto Annelille.

Asiakasviestinnässä voisi tutkia uudemmassa versiossa käytettävissä olevien viestiliitännäisten mahdollisuuksia: "Koha mailer plugin ja emailer":https://www.youtube.com/watch?v=serAmqPf9WA

### 6. Seuraava kokous

Seuraava kokous ke 16.3.2022 klo 9.15.

---

## Kokous 1/22

Aika 26.1.2022 klo 9.15
Läsnä: Ari Mäkiranta (Koha-Suomi), Leena Kinnunen (Lappi), Katri Sillgren (Helle), Tuomas Kunttu (Kyyti), Susanna Sandell (Vaski), Asko Autio (Vaski), Anneli Österman (Koha-Suomi), Noora Valkonen (OUTI), Päivi Knuutinen (Vaara), Katja Valjakka (Lumme) 

### 1. Arin ajankohtaiset

### 2. Asiantuntijaryhmän vuosisuunnitelma 2022

Käytiin läpi vuosisuunnitelma: attachment:Asiantuntijaryhmän_vuosisuunnitelma2022.docx

### 3. Versionvaihdon tilanne

Tiketit käyty läpi ja vastuutettu kehittäjille. Seuraavaksi aikataulutetaan koko projekti ja tehdään suunnitelma.

### 4. Muut asiat

#### 4.1 Aineiston korvaushinnat alvittomiksi.

verottajan mukaan korvaus kadonneesta/tuhoutuneesta aineistosta on arvonlisäverotonta: https://www.vero.fi/syventavat-vero-ohjeet/ohje-hakusivu/48609/vahingonkorvaus_ja_vahingonkorvauksen_l/tässä

Tässä vielä tuo KHO:n päätös korvaushintojen alvittomuudesta:

"KHO 22.3.2001 T 526

Yhtiö vuokrasi videokasetteja ja muuta irtainta omaisuutta kuten videolaitteita, televisioita ja pelikasetteja lyhytaikaisilla vuokrasopimuksilla. Mikäli kasetteja ja muuta vuokrattua omaisuutta ei määräaikaan mennessä palautettu eikä vuokralleottajan ja vuokranantajan välillä ollut tehty jatkovuokrasopimusta, perittiin alalla sovellettavien yleisten vuokrausehtojen mukaan ylityspäiviltä vuokratun omaisuuden puolitoistakertainen vuokra (viivästyskorvaus) korvauksena siitä vahingosta, joka vuokranantajalle oli syntynyt kolmansilta saamatta jääneiden vuokratuottojen menetyksenä, perintäkuluna ja muuna taloudellisena tappiona. Viivästyskorvaus perittiin enintään 30 päivän ajalta, jonka jälkeen perittiin lisäksi korvaus kuten tuhoutuneesta omaisuudesta. Mikäli vuokrattu omaisuus oli tuhoutunut tai sitä ei voitu muutoin palauttaa taikka se palautettiin korjauskelvottomana, vuokralleottaja oli velvollinen maksamaan vuokranantajalle omaisuuden arvoa vastaavan korvauksen.

Vuokratun omaisuuden palautuksen myöhästymisen johdosta asiakkaalta perittävää viivästyskorvausta ja vuokratun omaisuuden palauttamatta jättämisen johdosta asiakkaalta perittävää korvausta ei pidetty arvonlisäverolain 73 §:n 1 momentissa tarkoitettuina myynnistä suoritettavan veron perusteeseen luettavina vastikkeina vaan vahingonkorvauksen luonteisina erinä, joista yhtiön ei ollut suoritettava arvonlisäveroa."

**Päätös:** EDItX-rajapintaan tehdään muutos, että niteelle viedään korvaushinta alvittomana. Tiedotus muutoksesta pääkäyttäjien kautta.

#### 4.2. Huoltokatkon ajankohta

Kirjastoilta tullut palautetta huoltokatkon ajankohdasta. Keskusteltiin asiasta ja todettiin, että ajankohtaa ei voi  muuttaa. Huoltokatko on kerran kuukaudessa kuukauden toinen keskiviikko, eikä katkoa tule välttämättä joka kuukausi.

#### 4.3 E-kirjeiden lähetys

Keskusteltiin kirjeviestien lähetyksestä ja siitä, että se kannattaisi tehdä keskitetysti e-kirjeinä. Selvitetään Kyytissä ja Hellessä, voisiko ottaa käyttöön kimpan yhteisen e-kirjeiden lähetyssopimuksen. Koha-Suomi selvittelee myös, olisiko mahdollista saada Koha-Suomelle keskitetty sopimus ja Koha-Suomi laskuttaa kimppoja. Taustalla tavoite pyrkiä yhteisiin toimintatapoihin.

### 5. Seuraava kokous

Seuraava kokous 23.2.2022 klo 9.15.

---

## Tiekarttakokoukset

### Kehityksen tiekartta

Asiantuntijaryhmä piti kaksi kokousta, joissa suunnitteli Kohan kehityksen tiekarttaa. Seuraavaksi dokumenttia käsitellään kimpoissa, jonka jälkeen asiantuntijaryhmä käy sen läpi vielä kertaalleen. Sen jälkeen dokumentti menee Koha-Suomen hallituksen käsittelyyn.

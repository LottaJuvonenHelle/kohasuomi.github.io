---
layout: single
permalink: /paakayttajat2024
header:
  overlay_color: '#5e616c'
  overlay_image: /assets/images/cropped-pexels-photo-113850.jpeg
toc: true
title: 'Koha-Suomen pääkäyttäjäryhmän muistiot 2024'
---

Koha-Suomen pääkäyttäjäryhmä kokoontuu kerran viikossa. Ylimmäisenä on aina uusin muistio.

## Viikko 12

Aika: 19.3.2024 klo 9.15<br />
Läsnä: Anneli Österman ja Lari Strand (Koha-Suomi), Tuomas Kunttu (Kyyti), Anni Rajala (Vaski), Päivi Knuutinen ja Auli Rantasalo (Vaara), Hanna Ikonen (Lumme), Piia Semenoff (OUTI), Reetta Pihlaja (Siilinjärvi), Noora Suvanto (Lappi), Kati Sillgren ja Lotta Juvonen (Helle), Annika Helastila ja Elina Uotila (Kirkes)

**Yhteiset**
* [Kori-toiminnosta nidetyyppi-sarakkeen piilotus](https://github.com/KohaSuomi/Koha/issues/411#issuecomment-1976349820)
* [Asiantuntijaryhmän muistio 4/24](https://github.com/KohaSuomi/Koha/discussions/1123)

**Kyyti**
* Uuden version ominaisuudesta kysyin, että voiko Varauksen teosta vahvistusviesti (EmailPatronWhenHoldIsPlaced) -toiminnon päälle laittaminen aiheuttaa mitään kuormaongelmaa sähköpostipalvelimella? - Ei kuulemma aiheuta.
* Testasin Ennakkovaraukset-ominaisuutta. Ei oikein vaikuta vielä toimivalta. Tein ennakkovarauksen. Sen jälkeen lainasin toiselle asiakkaalle ongelmitta, vaikka meni ennakkovarauksen päälle. Toisella kertaa antoi lainata ennakkovarauksen alkuun asti. Siinäkin tapauksessa antoi kuitenkin uusia lainan huolimata ennakkovarauksesta.
* Nextillä asiakkaan tiedoissa näkyy Reklamaatiot-välilehti. Tuotannossa ei näy. Johtuu ilmeisesti nextin BundleLostValue-asetuksesta, joka on päällä, koska nidepaketit ovat käytössä. Tuotannossa sama asetus on myös päällä, mutta silti reklamaatiot-välilehti ei näy. Asetuksen toiminta on siis muuttunut.

**Vaski**
* Mietitty pitäisikö Othernames-kentän kielikäännös muuttaa Muu nimi -> Kutsumanimi. Palaverissa todettiin, ettei ole tarpeen.
* Kirjastojen atk-ihmisten kokoontumisajot Turussa 25.-26.4.2024. Vaskin pääkäyttäjille voi huikata, jos ei ole saanut kutsua ja haluaisi osallistua.

**Vaara**
* Kysymys tarpeettomien aineistotyyppien poistosta tarkan haun näkymästä sai kielteisen vastauksen. Kehittäjien mielestä voi aiheutua ongelmaa, jos aineistotyyppejä poistaa auktorisoiduista arvoista. Harmi kun ei ole mitään muuta tapaa piilottaa tästä hakunäkymästä näitä tarpeettomia aineistotyyppejä.

**Lumme**
* Normaalia ylläpitoa.

**OUTI**
* Puppe on alustavasti otettu Oulussa käyttöön vuoden 2024 loppuun.
* Uuden version käyttöönottovalmisteluja tehty.
* Normaalia ylläpitoa
* Vaskista saatu raportti, jolla haetaan kannasta asiakkaan vahingossa poistamat varaukset. Raportin avulla voimme OUTIssa luopua käytännöstä, että etsimme lokilta varaukset ja tallennamme ne yksi kerrallaan asiakkaalle takaisin. Nyt voimme toimittaa listan poistetuista varauksista asiakkaalle ja hän voi halutessaan tallentaa ne itse verkkokirjastossa. Suurkiitos raportista!

**Siilinjärvi**
* Kohassa ei mainittavaa, kunnan yt-neuvottelut mietityttävät.

**Lappi**
* Asiakkaiden viesteissä otettu käyttöön kirjastokortinnumeron osittainen piilotus.
* Normaalia ylläpitoa.

**Helle**
* Uudet varapääkäyttäjät Lotta Juvonen ja Vilgot Strömsholm ovat aloittaneet.
* Uudessa versiossa on Niteiden erämuokkaus -toiminnossa uusina ominaisuuksina: Jätä pois paikallisten varausten jonosta JA Palauta niteet. Ehdotettu ominaisuuksien poistamista käytöstä (piilottamista). Palaverissa todettiin, että toteutukselle on tarve. Tiketti [#123](https://github.com/KohaSuomi/Koha-23x/issues/123)

**Kirkes**
* Käyty läpi Nextin järjestelmäasetuksia.
* Kirkes-johtoryhmä harkitsee noutamattomien varausten maksun poistamista lapsiasiakkailta, mutta päätöstä ei ole vielä tehty. Varaudutaan kuitenkin poistoajon käyttöönottoon.
* Salasananvaihtoviestit laitettaneen päälle jollain aikataululla. 


## Viikko 11

Aika: 11.3.2024 klo 9.15<br />
Läsnä: Anneli Österman ja Emmi Takkinen (Koha-Suomi), Päivi Knuutinen ja Auli Rantasalo (Vaara), Annika Helastila (Kirkes), Leena Kinnunen, Pia Kusmin, Maria Joona (Lappi), Reetta Pihlaja (Siilinjärvi), Pirkko-Liisa Lauhikari ja Piia Semenoff (OUTI), Hanna Ikonen ja Katja Valjakka (Lumme), Kati Sillgren (Helle)

**Yhteiset**
* [Viikon 11 päivitys](https://github.com/KohaSuomi/Koha/discussions/1115)
* [Huoltokatko keskiviikkona](https://github.com/KohaSuomi/Koha/discussions/1108)
* String freeze viikosta 12 lähtien eli viikkopäivityksiä ei tehdä tästä lähtien ja keskitytään versiovaihdon ominaisuuksien valmistelemiseen.
* [Tiketti #336](https://github.com/KohaSuomi/Koha/issues/336#issuecomment-1968753873)
  * "Jos valitsi hyllypaikan, hyllytarkenteen ja kokoelmakoodin siten, ettei sellaisella kombinaatiolla entuudestaan ollut yhtään nidettä, niin kenttään tuli tyhjä arvo. Voisikohan tässä käyttää tuota osakentän oletusarvoa, vai onko parempi jättää kenttä tyhjäksi, jotta se täytetään sitten asianmukaisesti?" - Miten kannattaisi toimia?

Pohjoisesta etelään

**Vaara**
* normaalia ylläpitoa ja versionvaihdon tikettien testausta
* lisäksi PowerBI:n raportin muokkaamista

**Kirkes**
* selvitellään lehtien vastaanottamisessa ilmenneitä epäjohdonmukaisuuksia.

**Lappi**
* Normaalia yläpitoa

**Siilinjärvi**
* ei erityistä, intranetuser- ja järjestelmäasetusten läpikäynti vihdoin aloiteltu nextillä

**OUTI**
* Oulun luetteloinnissa ja hankinnassa oli huomattu, että jos tekee itse hankintoja Kohassa ja poimii valmiin tietueen ulkoisesta lähteestä, muodostuu tietueelle kaksi 000-kenttää, varsinainen 000-kenttä ja ”nam a22 8i 4500” -kenttä. Sama tilanne muodostuu myös, jos Hankinnan lomakkeella tekee tyhjästä uuden tietueen. Annelin neuvon mukaan, kannattaa käydä poistamassa ACQ-kuvailupohjan 000-kentän oletusarvo "nam a22 8i 4500", jottei tietueelle synny kahta 000-kenttää. Tarkemmin tiketissä: https://github.com/KohaSuomi/Koha/issues/1114  
* OUTIssa poistetaan myös lakkautetut kirjastot/toimipisteet tietokannasta, koska kirjastojen poistot eivät ole aiheuttaneet ongelmia muissakaan kimpoissa. Poiston voi tehdä sen jälkeen, kun kirjaston vuositilastot on otettu talteen, eikä kirjastolla ole enää asiakkaita, niteitä yms.
* OUTIssa otetaan käyttöön 13.3.2024 maksujen jaottelu julkis- ja yksityisoikeudellisiin maksuihin asiakkaan tiedossa.

**Lumme**
* Normaalia ylläpitoa. Tulevan version järjestelmä- ja IntranetUser-asetusten läpikäyntiä.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2024#viikko-11) - [Palaa sivun alkuun](/paakayttajat2024)

## Viikko 10

Aika: 5.3.2024 klo 9.15<br />
Läsnä: Anneli Österman ja Pasi Kallinen (Koha-Suomi), Anni Rajala (Vaski), Leena Kinnunen (Lappi), Päivi Knuutinen ja Auli Rantasalo (Vaara), Hanna Ikonen (Lumme), Pirkko-Liisa Lauhikari, Piia Semenoff ja Veli-Pekka Marjoniemi (OUTI), Tuomas Kunttu (Kyyti), Kati Sillgren (Helle), Annika Helastila ja Elina Uotila (Kirkes)

**Yhteiset asiat**
* [HOLDDGST eli varausten koosteviesti](https://github.com/KohaSuomi/Koha-23x/wiki/Uudet-viestipohjat#holddgst) -uusi toiminnallisuus versiossa 23.11 - toiminnallisuuden hyvät ja huonot puolet.
  * toimii vain sms/email-pohjilla
  * asiakaskohtaisesti valittavissa, mutta pitäisikö pakottaa tai piilottaa kaikilta?
  * Päätös: Piilotetaan koostetäppä kaikilta
* Valmistautumista kokoelmatyön koulutukseen:
  * Onko teillä kimpoissa hyviksi havaittuja kokoelmiin liittyviä SQL-raportteja, joita ei vielä löydy Raporttikirjastosta?
    * Jos löytyy, niin lisäilettekö niitä Raporttikirjastoon Kokoelma-osioon parin viikon sisällä?
  * Nidehaku ja räätälöidyt hakukentät, joista tullaan puhumaan ja kannattaa lisätä nidehaun hakukenttiin ylläpidossa:
    * Luokka (084$a)
    * Aineistotyyppi (942$c) [auktorisoiduksi arvoksi MTYPE]
    * Kielikoodit eri MARC-kentistä (041$adhjp)
    * Asiasanat (655$a, 650$a)
    * Yleinen huomautus (952$z)
    * Huomautus virkailijalle (952$x) 
* [Viikon 10 päivitys](https://github.com/KohaSuomi/Koha/discussions/1107)
* [Huoltoikkuna 13.3.](https://github.com/KohaSuomi/Koha/discussions/1108) - katko tiedossa

Etelästä pohjoiseen

**Vaski**
* Otettu käyttöön mahdollisuus muokata jopa 10 000 nidettä erämuokkauksessa
* Tehty nideraportteja kirjastojen remonttisulkemisia varten, pääkirjaston kirjallisuus ja taiteet -osasto suljetaan lohkoittain joten tarvitaan useampi raportti.
* Pupen tilausten kohdentamisen parantamiseksi Broomworks pyytänyt lisäoikeuden vendors_manage. Sovittiin, että laitetaan vielä viestiä tästä Matrixin kautta. Jos/kun asia ok niin Anni huolehtii integraatiot-sivun ja OUTIn tiketin päivityksestä.
* Turun lainauskaappi alkanut antaa eräpäiväksi kuluvan päivän. Ongelma alkanut viime viikon päivityksessä tehdyn muutoksen seurauksena. Käydään vielä katsomassa automaatin asetuksia ennen kuin tehdään tiketti.

**Lappi**
* Kimpan johtoryhmä päätti luopua kirjastokortin kuntatunnuksesta ja siirtyä LAPPI-alkuisiin kortteihin. 
* Rovaniemen pääkirjasto väistötilassa 2.5. eteenpäin vuoden (siirtymä vaiheittain jo huhtikuun aikana). Perustetaan yksi uusi kirjasto aineiston käsittelyä varten, mutten mennään melko pitkälti toissavuoden väistötilan säännöillä. 
* Käyttäjäryhmän päätösten mukaisesti tehty pieniä muutoksia asetuksiin.

**Vaara**
* Viime viikolla saatiin Ceepos-kassat toimimaan, kun vaihdettiin vanha IntranetUserJS-rimpsu paikoilleen.
* Oli unohdettu tallentaa Kohan kalenteriin pääsiäisen poikkeusaukiolot, joten eräpäiviä tuli pääsiäisen pyhille. Onneksi erämuokkauksella sai korjattua eräpäivät oikeaan päivään ja kalenteri päivitetty vaihtuvilla pyhäpäivillä.
* Vaarassa on raportti, jolla saa kiinni asiakkaat, joiden rekisteröitymispäivämäärä on tulevaisuudessa. Tänä aamuna raportilla löytyi kaksi yhteisöasiakasta, joiden rekisteröitymispäivämäärä oli elokuussa 2024. Ilmeisesti se ei aiheuta onneksi muuta kuin tilastovirheen, jos tutkailee uusia asiakkaita. Harmillista silti, että tarpeettomasti muokataan tuota päivämäärää.

**Lumme**
* Tehty Finnaan pieniä käännösmuutoksia asiakasliittymään. Tilaa PIN-koodi vaihdettu "Vaihda PIN-koodiksi", Kohasta tulevat käsin lisätyt asiakasrajoitukset näkyvät jatkossa "Kirjastokortillasi on rajoitus. Ole yhteydessä kirjastoosi kirjaston palveluaikana."
* Nalkutin saatu toimimaan tuotantonnossa, nyt Marc-virhelistauksen raportti on pienentynyt n. 95 000 tietueesta 17 500 tietueeseen.
* Yhteiset käyttösäännöt tulivat voimaan 1.3. ja noutamattoman varauksen maksu nousi kahteen euroon.

**OUTI**
* Poistettu kirjastokorttinumerot s-postiviesteinä menevistä palautuskehotuksista ja eräpäivämuistutuksista. Jatkossa viesteissä näkyy vain kortin kolme viimeistä numeroa.
* Pystytäänkö Koha-Suomella arvioimaan, milloin nextille olisi saatu siirrettyä kaikki Koha-Suomen omat muutokset, jotta kimpassa voitaisiin toteuttaa isommat testaukset? Anneli lupaili aikataulua viikon 11 alkupuolella.

**Kyyti**
* Uuden version uudet asetukset käyty läpi
* Löytyi teos, jolla oli kaksi tietuetta: toiseen ei päässyt (Tietuetta 1500602 ei ole tietokannassa), mutta siinä oli kiinni nide ja toinen tietue toimi normaalisti ja siinä oli edellisen tietueen niteen hankintatiedot. Neuvottiin liittämään nide toimivaan tietueeseen (Muokkaa | Liitä nide). Tämä toimi hyvin. Sitten piti vielä pyytää kehittäjää poistamaan toimimaton tietue pois indeksistä [#1112](https://github.com/KohaSuomi/Koha/issues/1112)

**Helle**
* AutoFrameCode-liitännäisen käyttöönotossa olin unohtanut vaihtaa musiikkiäänitepohjalle oikean tunnuksen (tunnus ei ole sama kuin TäTin vastaavalla kuvailupohjalla). Väärästä määrityksestä johtuen ko. kuvailupohjaan liittyvän tietueen niteet eivät näkyneet oikein eivätkä olleet muokattavissa.
* Kausijulkaisut-toiminnossa tehtyjen toimintojen myötä muutamista käsitellyistä tietueista on muodostunut tuplatietueita. Tietueiden niteiden nidevarauksessa havaittu haasteita. (Helle-Finnassa varauksenteko onnistunut normaaliin tapaan.)
[#1041](https://github.com/KohaSuomi/Koha/issues/1041)
* Noudettavissa olevat varaukset -toiminnon Asiakas-sarake piilotettu.
* Tänä aamuna Kohan kirjautumisnäytöllä lisätekstinä Virhe: Tili lukittu. Kohaan kirjautuminen onnistui. Anneli lisäsi tapaustiedon Ongelmatilanteita-koosteeseen.
Ongelman syy: Todennäköisesti jollain tunnuksella on cardnumber/userid tyhjä ('') ja kyseisen tunnuksen epäonnistuneiden kirjautumisten määrä on ylittänyt sallitun maksimin.

**Kirkes**
* Ei mainittavaa. 


[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2024#viikko-10) - [Palaa sivun alkuun](/paakayttajat2024)

## Viikko 9

Aika: 27.2.2024 klo 9.15<br />
Läsnä: Anneli Österman (Koha-Suomi), Päivi Knuutinen ja Irina Halminen (Vaara), Pirkko-Liisa Lauhikari, Piia Semenoff ja Veli-Pekka Marjoniemi (OUTI), Pia Kusmin ja Maria Joona (Lappi), Kati Sillgren (Helle), Hanna Ikonen (Lumme), Mikko Liimatainen (Vaski)

**Yhteiset**
* [Varauksen keskeytyksen ja aktivoinnin käännösmuutosehdotukset](https://github.com/KohaSuomi/Koha-translations/issues/19#issuecomment-1954070069)
* [Viikon 9 päivitys](https://github.com/KohaSuomi/Koha/discussions/1098)
* Pääkäyttäjäryhmän vuosisuunnitelma: [paakayttajatvuosisuunnitelma2024.docx](https://github.com/KohaSuomi/kohasuomi.github.io/files/14416128/paakayttajatvuosisuunnitelma2024.docx)
* Asiantuntijaryhmästä tehtäväksi:
  * [Waitingreserves.pl-sivulle mahdollisuus näyttää asiakkaan tiedoista vain varaustunniste #367](https://github.com/KohaSuomi/Koha/issues/367)
    * Koha-Suomen asiantuntijaryhmä 26.2.2024: Suositus, että Asiakas-sarake piilotetaan sarakeasetuksissa. Pääkäyttäjien tehtävissä.
  * [Ylläpito/Kirjastot ja ryhmät: mahdollisuus lisätä Nimi-arvo suomen lisäksi ruotsiksi ja englanniksi #448](https://github.com/KohaSuomi/Koha/issues/448)
    * Koha-Suomen asiantuntijaryhmä 26.2.2024: Yhteisössä on avoinna aiheesta parikin bugia. Pyydetään pääkäyttäjiä käymään kommentoimassa tiketteihin, että toiminto olisi tärkeä, jotta saadaan yhteisöä aktivoitumaan. 

Pohjoisesta etelään

**Vaara**
* Ceepos-kassan testailut jatkuu, kun asetuksiin on muutettu sääntöä. Auli palaa lomalta huomenna, jolloin päästään testaamaan eri maksuvirityksiä ja niiden toimintaa.
* Muuten normaalia ylläpitoa, ei mainittavaa.

**OUTI**
* Pyhäjoella on poistettu käytöstä Monelan ja Pirttikosken kirjastot.
* Kutsumanimikentän saaminen näkyville tuotanto-Finnaan. Asia työn alla Larilla ja Erellä.
* Mietinnässä OUTIn Koha-ryhmässä uusien kokoelmien Dekkari, Helppolukuinen ja Selko lyhenteet ja kuvailut.
* Puppe otettiin perjantaina kehden viikon koekäyttöön. Koha-tukeen ei ole ainakaan vielä kuulunut miten menee. Palataan asiaan myöhemmin, kun kuullaan käyttökokemuksia.
* OUTIssa  on paljon hyväksytty varaustunnisteita, joissa on erikoismerkkejä. Pohdittiin voisiko muut kirjastot ottaa Vaskin validoinnin käyttöön, mutta koska OUTIn Finna-tuki oli tehnyt tästä jo kehitysehdotuksen Kansalliskirjastoon, päätettiin odottaa sen etenemistä.

**Lappi**
* Normaalia ylläpitoa.

**Helle**
* Kirjastoista kysytty Webkaken kaukolainojen näkymistä Kohaan.
* Tiedonhaun kirjasto + hyllypaikka -haku ei anna oikeaa hakutulosta Kohassa eikä Finnassa. Palaverissa saatu tieto/kertaus siitä, että hakuun tarvittavia indeksointeja puuttuu.
* Finnan Aikuiset-fasetin JA Lapset ja nuoret -fasetin käyttöä varten olisi tarpeellistsa saada tietueiden kiinteämittaiseen kenttään 008/22 massatäydennystä esim. tietueiden niteiden hyllypaikka-arvojen perusteella. Tämän mahdolliseen toteutukseen lienee parempi ajankohta joskus myöhemmin.

**Lumme**
* Perusylläpitoa.

**Vaski**
* Timeout-asetuksen muuttaminen puoleen tuntiin herättänyt paljon keskustelua. Aika koetaan hyvin lyhyeksi monissa kirjastoissa. Lisäksi uloskirjautumisen näkymättömyys aiheuttanut hämmennystä, kun uudelleenkirjatuminen saattaa alkaa niteen palautuksesta ja kirjautumisen jälkeen palautuu samaan tilanteeseen, johon edellinen käyttäjä oli Kohan jättänyt. Saisikohan Kohan oikeasti kirjaamaan käyttäjän pihalle, kun aika tulee täyteen, jolloin se näkyisi paremmin seuraavalle käyttäjälle? Tässä toki riskinä, että sama käyttäjä menettää jotain tekemäänsä, jos Koha ei palauta käyttäjää takaisin samalle sivulle.
* Käyttäjille, jotka vaihtavat työskentelypaikkaa usein, on ajateltu helpotusta arkeen selainliitännäisestä, joka tarjoaisi kirjautumisessa aina kyseisen toimipisteen, jossa kone sijaitsee. Tällä saataisiin käytännössä muutettua kirjautuminen toimipistekohtaiseksi nykyisen käyttäjäkohtaisen sijaan. Liitännäisestä on tehty prototyyppi, johon voi asettaa haluamansa kirjaston kirjastolyhenteen perusteella ja tallentaa tiedon selaimeen. Tähän olisi suunnitteilla hakea kirjastotiedot rajapinnasta.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2024#viikko-9) - [Palaa sivun alkuun](/paakayttajat2024)

## Viikko 8

Aika: 20.2.2024 klo 9.15<br />
Läsnä: Anneli Österman, Kodo Korkalo ja Lari Strand (Koha-Suomi), Anni Rajala (Vaski), Pia Kusmin ja Maria Joona (Lappi), Päivi Knuutinen ja Auli Rantasalo (Vaara), Hanna Ikonen (Lumme), Pirkko-Liisa Lauhikari ja Piia Semenoff (OUTI), Annika Helastila ja Elina Uotila (Kirkes), Tuomas Kunttu (Kyyti), Kati Sillgren (Helle), Reetta Pihlaja (Siilinjärvi)


**Yhteiset**
* [Viikon 8 päivitys](https://github.com/KohaSuomi/Koha/discussions/1087)
* Pääkäyttäjäryhmän vuosisuunnitelma 2024 työn alle: [paakayttajatvuosisuunnitelma2024.docx](https://github.com/KohaSuomi/kohasuomi.github.io/files/14331227/paakayttajatvuosisuunnitelma2024.docx)
  * käsitellään ensi viikon kokouksessa, kun kaikki ovat ehtineet katsoa dokumentin läpi ja Anneli pyytänyt Arilta tarkempaa ohjeistusta.

Etelästä pohjoiseen

**Vaski**

* Seinäjoelle (Eepos-kimpalle) pidetään tänään Koha-esittely.
* Turun pääkirjaston Kirjallisuus ja Taiteet -osasto menee remonttiin. Palautuvan aineiston sijoittelu mietinnässä.
* Myös kaksi Turun lähikirjastoa menossa remontin vuoksi kiinni.
* Kysyttiin onko mieltä sellaisessa ehdotuksessa, että nidehaun tuloksissa voisi näyttää 1000 nidettä (=saisi vietyä 1000 niteen joukon erämuokkaukseen). Selvisi, että Kohassa voi nykyään MaxItemsToDisplayForBatch... -asetuksilla määrittää paljonko niteitä esikatselussa näytetään ja paljonko niteitä voidaan kerralla muokata/poistaa. Kirkeksellä display-asetuksissa 1000 ja process 10000, ja toiminut hyvin. Vaskissa testataan samaa, helpottaa niteiden erämuokkauksia.

**Lappi**
* Rovaniemen remontti ja kiinnimeno lähenee. Eräpäivät ylitettiin ja samalla selvisi ongelma verkkokirjaston uusinnoissa. Finna käyttikin uusinnoissa Finna-API kirjaston kalenteria, jolloin nyt kaikkien kirjastojen eräpäivät siirtyivät 13.5. asti. Vika korjattiin circcontrol asetusta muuttamalla.
* Maksniemen kirjasto suljetaan kevään aikana. Suunnittelut sulkemisesta aloitettu.
* Ranualla otetaan toukokuussa käyttöön Smartbox.
* Tiketin #1083 tietueet korjattu, koska aiheuttivat indeksointi ongelman (saatavuus tieto näytti eri paikoissa eriä).
* Tuli vastaan varauksia, jotka olivat varaussijalla 0, mutta asiakas ei niitä ole saanut. Selvisi, että automaateilta menee osa varauksista suoraan hyllyyn, koska asiakkaat laittavat niteet väärään paikkaan. Tiedotetaan henkilökuntaa ja vinkataa automaateista saaravaan raporttiin tarkistettavista niteistä. 
* Kysy Kohasta -koulutus tulossa 19.3.

**OUTI**
* Uuden Tietuesiirtäjän säätöä (Antti ja Johanna). Tiketti #915
* Muhoksen Hyrkin alakoulu aloittaa lainaamisen. Lisätty hyllytarkenne.
* Tyrnävän kirjakaapin eräpäiväkuittiongelma. Lainauskuittiin ei tulostunut eräpäivää. Ennen versiopäivitystä 12-paluuviestissä on tullut eräpäivä AH-kentässä normaalisti. Versiopäivityksen jälkeen tilanne muuttui. Jos lähetetään 11-viestissä "no block" = ”Y”, niin AH-kenttä tulee tyhjänä, vaikka Koha ilmoittaa lainauksesta tai uusinnasta. Lainalla on myös Kohasta katsottuna eräpäivä, mutta AH-kentässä se ei tule. Oulun automaateilla ei tätä ongelmaa ollut vaan ainoastaan Tyrnävän kirjakaapissa.
  * Tiketti #1084
  * Yhteisössä on korjaus, joka on tuotu OUTI-testille ja Lappi-testille. Näyttää toimivan Lappi-testillä, mutta OUTIssa testataan vielä tällä viikolla. Jos kaikki menee hyvin tuodaan tuotantoon ensi tiistaina.
* OUTI Koha-ryhmän päätöksiä: 
  * uudet kokoelmat Dekkari, Selko, Helppolukuiset
  * uusi nidetyyppi laina-aika-7 vrk, myöhästymismaksu 0,40 e/pv, ei uusittava, ei varattava
  * asiakkaiden s-postiviesteistä (eräpäiväilmoitukset ja palautuskehotukset) jätetään koko kirjastokortin numero pois, vain kolme viimeistä merkkiä jätetään viesteihin.
  * Sotu-avaimettomille asiakkaille lisätään huomautusviesti (joka näkyy myös verkkokirjastossa) henkilötunnuksen puuttumisesta. Poistetaan mahdolliset siihen liittyvät rajoitukset.
  * Maksujen erottelu julkis- ja yksityisoikeudellisiin asiakkaan tiedoissa otetaan OUTIssa käyttöön:
Maksu-näkymän tekstimuutosehdotus asiakkaan Lainat- ja Tiedot näytöllä, jos mahdollista toteuttaa: "Asiakkaalla on lainauskieltoon vaikuttavia maksuja €16.00. Yhteensä (sis. maksut, jotka eivät vaikuta lainauskieltoon): €34.00.
     Anneli kysyy tieteelliseltä voiko lausetta muuttaa, vaikuttaako se tieteellisten kirjastojen toimintaan?
     OUTI tekee tästä tiketin. Tiketti: https://github.com/KohaSuomi/Koha/issues/1089
* Tullut kysymyksiä tilastoista.

**Vaara**
* Viime viikolla Outista Pirkko-Liisa kertoi raportista, jolla saa 245$h-kentän tiedot haettua. Pyysin raportin myös Vaaraan ja ajoin sen. Tuloksena oli yli 300 riviä erilaisia "yleismääreitä". Osa voidaan poistaa RDA-konversiossa suoraan, mutta osa sisältää tekijätietoja ym. jotka kuuluvat ihan toiseen osakenttään. Korjaan noita, missä on säilytettävää tietoa.
* Viime viikon päivityksessä Ceepos-kassan toiminnossa havaittiin ongelma, että osittain maksuja maksettaessa kassa näyttää eri summan kuin mitä Kohassa näkyy (virkailija syöttää esim. 2.00 euroa, Ceepos näyttää 2,30). Tätä nyt pallotellaan Meitan ja Ceepoksen välillä. Viimeisin tieto on, että Koha toimii väärin. Miksi se toimisi vain Joensuussa väärin?

**Lumme**
* Perusylläpitoa, pienten asioiden selvittämistä.
* Maaliskuussa otetaan käyttöön myös sähköpostimuistutus vaihtoehdoksi asiakkaille lähtevään 1. muistutusilmoitukseen.

**Kirkes**
* Mana-tietämyskanta on otettu käyttöön.
* Yksittäinen Suomi.fi-viesti lähtenyt useamman kerran, mistä DVV on ilmoittanut. Kyse on luultavasti silkasta vahingosta. 

**Kyyti**
* Käyty läpi uuden version IntranetuserCSS-rimpsu.  Löytyi yksi lisäys, jota tarvitaan jos käytössä ovat nidepaketit. Anneli lisäsi sen ohjeisiin: https://github.com/KohaSuomi/Koha-23x/wiki/IntranetUserCSS

**Siilinjärvi**
* Ei mainittavaa
* Tilastojen teko oli tällä kertaa helppoa ja mukavaa, koska tilastotyökalun antamat luvut olivat selkeitä ja loogisia. Kiitos kehittäjät!

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2024#viikko-8) - [Palaa sivun alkuun](/paakayttajat2024)

## Viikko 7

Aika: 13.2.2024 klo 9.15<br />
Läsnä: Anneli Österman ja Pasi Kallinen (Koha-Suomi), Pirkko-Liisa Lauhikari, Piia Semenoff, Veli-Pekka Marjoniemi (OUTI), Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Reetta Pihlaja (Siilinjärvi), Kati Sillgren (Helle), Tuomas Kunttu (Kyyti), Roosa Väisänen (Kyyti), Annika Helastila (Kirkes), Elina Uotila (Kirkes)

**Yhteiset**
* [Redusointi ja sip-tunnukset](https://github.com/KohaSuomi/Koha/issues/838#issuecomment-1931608560) - ehdotus toimintatavasta
  * kaikki tekevät testitunnukset ja toimittavat joko supportiin tai Larille Matrixissa.
* [Viikon 7 päivitys](https://github.com/KohaSuomi/Koha/discussions/1071)
  * Kuvailupohjan liitännäiseen pitää käydä lisäämässä asetukset, jotka löytyvät tiketistä.
* [Integraatiot-wikiin](https://github.com/KohaSuomi/Koha/wiki/Integraatiot) lisätty ohjeistusta rajapintojen avaamista ja sulkemista varten sekä mitä käyttäjäoikeuksia tunnukset tarvitsevat.
* Ei huoltokatkoa helmikuussa.
* [Pupen esittely 21.2.2024 klo 10](https://github.com/KohaSuomi/Koha/discussions/1068)
* Lari kysyy: Testi-Finnat ja kutsumanimi, oletteko ehtineet tarkistamaan?
  * sama muutos pitää pyytää myös nextien Finnoille.
  * Käykää testaamassa ja kuittaamassa [tikettiin Finna-kehitysehdotukset #22](https://github.com/KohaSuomi/Finna-kehitysehdotukset/issues/22) viimeistään pe 16.2.2024.

Pohjoisesta etelään

**OUTI**
* Otettu käyttöön uusi Tietuesiirtäjä. Tänä aamuna ensimmäiset tietueet siirtyneet Kohaan.
* Oulu ottaa kahdeksi viikoksi koekäyttöön Puppe-tilaustenvastaanottotyökalun 23.2.2023. Jos työkalu toimii, se jää ilmeisesti käyttöön.
* Oulun luetteloinnista tuli tiedoksi, että RDA-konversiossa poistuu kokonaan 245h-kenttä (Aineiston yleismääre). Ilmeisesti kentän tietojen annetaan hävitä konversiossa.
* Tehty varauksen keskeytykseen liittyvät tekstimuutokset Finnaan.

**Vaara**
* Joensuu-apin päivityksessä otettu käyttöön HionDigitalin tekemä sovellus, jolla Vaarojen asiakkaat pääsevät apin kautta uusimaan lainojaan, tekemään varauksia ja keveitä tiedonhakuja.
* Vaara-Finnassa muokattu maksunäkymää lisäämällä sinne tiedotusta maksamiseen liittyvissä asioissa.
* Cineast-elokuvapalvelu tulossa kuun vaihteessa käyttöön Vaarassa asiakkaille (nyt henkilökunnalla demokäyttö kokeiltavana)

**Siilinjärvi**
* Vuorelan kirjaston lainaus/palautusautomaatti seisahtelee itsekseen omatoimiaikana. Kohan päästä ei löytynyt vikaa, jatketaan selvittelyä Tieran ja Mikroväylän kanssa.
* Hetu/hetuavain näyttäisi puuttuvan n. 600 henkilöasiakkaalta, osa näistä käyty jo läpi aiemmin ja huomautus lisätty. Lisätään lopuillekin ja muistutellaan taas hetun tallentamisesta oikein.
* Emottomien osakohteiden poisto vielä vaiheessa, PasiK:n toimittama listaus vaatii vielä lisäselvittelyä.

**Helle**
* Poistettu massana 17269 emotonta osakohdetta. Listaus poistettavista Pasi Kalliselta.
* Niteelle tullut lainatessa eräpäiväksi lainauspäivä. Syynä kirjastokortillisen lainaajatiedon virheellinen Takaaja-asiakastyyppi. Takaaja-asiakastyyppi ei sisälly Hellen laina- ja maksusääntöihin.
* Kaukolaina-asiakastyypin salasanan generointiin tuli muutos. Lari Strand teki tarvittavat ylläpitomuutokset.

**Kirkes**
* E-kirjaston Cineast-elokuvapalvelu otettu käyttöön Viddlan sulkeuduttua, päivitelty integraatiolistaan.
* Kirjastokortittomille asiakkaille on muodostunut KIRKON-tunnus asiakastietojen kirjastokorttikenttään konversion seurauksena. Siivotaan nämä hiljalleen pois.
* Järvenpäässä vaihdettu tulostimien toimittaja Canoniin. Mahdollisuus rakentaa rajapinta Kohaan.
  

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2024#viikko-7) - [Palaa sivun alkuun](/paakayttajat2024)

## Viikko 6

Aika: 6.2.2024 klo 9.15<br />
Läsnä: Anneli Österman ja Lari Strand (Koha-Suomi), Iina Niemi (Vaski), Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Leena Kinnunen ja Pia Kusmin (Lappi), Tuomas Kunttu (Kyyti), Pirkko-Liisa Lauhikari (OUTI), Reetta Pihlaja (Siilinjärvi), Annika Helastila ja Elina Uotila (Kirkes), Kati Sillgren (Helle)

**Yhteiset**
* [Viikon 6 päivitys](https://github.com/KohaSuomi/Koha/discussions/1057)
* [Asiantuntijaryhmän muistio 2/24](https://koha-suomi.fi/asiantuntijaryhma2024#asiantuntijaryhm%C3%A4n-muistio-224) - keskeneräinen kirjoitushetkellä
* [Indeksointi- ja tiedonhakuryhmän muistio 1/2024](https://github.com/KohaSuomi/Koha/discussions/1047)
* Muistutuksena, että torstaina jatketaan uudemman version [ominaisuuksien läpikäyntiä](https://github.com/KohaSuomi/Koha/discussions/1054)
* 23.11-version IntranetUserCSS:t käyty läpi ja korjattu tarvittaessa. Kannattaa tyhjentää asetus kokonaan (ota talteen vanhat vaikka muistioon) ja lisäile sitten tarvittavat uudelleen. Näin mukaan ei jää vahingossa vanhoja/toimimattomia rimpsuja.
  * JS:t työn alla.

Etelästä pohjoiseen

**Vaski**

* Ei mainittavaa

**Vaara**
* Edellisellä viikolla kertomani emottomien osakohteiden korjausajo vaati lopulta neljä yritystä, ennen kuin raportti oli sellainen, että tietueet saattoi poistaa. Samalla korjattiin myös 001-kentän kontrollinumerot vastaamaan biblionumberia ja trimmattiin 003-kentistä tyhjiä merkkejä pois.
* Eilen kesken iltapäivän meni vaara.finna.fi:ssä rikki jotain: lainoja ei voinut uusia, niteiden saatavuus ei näkynyt, tapahtumien kuvat ja tiedot eivät näkyneet eikä myöskään uutiset. Selvisi, että vika oli lopulta Smileen chat-palvelussa, joka rikkoi jotain Finnassa. Muilla kimpoilla ei ollut samaa ongelmaa kuin Vaaralla ja Outilla. Finna-tuesta neuvottiin kommentoimaan chat-palvelu pois päältä, kunnes se on korjattu.

**Lappi**
* noreply-toiminnon käyttöönotto ei Lapissa aiheuttanut ilmeisesti mitään ongelmia. Noreplyä on ollut odottamassa 2. palautuskehotuksen salliminen sähköpostilla, otetaan se nyt työn alle.
* Sotuttomia asiakkaita käyty läpi ja merkitty näille rajoitus ja tieto sotun lisäämisestä. Kolmesta kirjastosta tullut palautetta, että sotut olisi heidän mielestään laitettu asiakkaille, ja ne olisivat nyt jotenkin kadonneet. Keskusteltiin, onko muualla havaittu samaa ja mikä voisi olla syynä. Lappi tekee kehitysehdotuksen sotun tallennuksen kehittämisestä niin, että sotua ei vahingossa jäisi tallentamatta. 

**Kyyti**
* Viime viikon kirjastojen sähköpostiosoitteiden muutos vaikutti laajasti Kyytin viesteihin. Tekstiviesteihin ilmestyi yksi yhteinen lähettäjänimi (Hamina), kun aiemmin lähettäjä oli oman kunnan nimi. Tekstiviestien osalta selvittely on vielä kesken. PDF-viestien tulostus meni myös sekaisin. Näiden viestien käsittely onnistuu uusilla ohjeistuksilla. Tiedottamista on riittänyt.

**OUTI**
* Oulun luetteloinnista Heikkisen Antilta tullut huomio, että jostakin syystä Mikropalvelu ei näytä ymmärtävän venäjänkielisen aineiston tietueissa olevia 9-osakentän sisältäviä kenttiä, vaan tuplaa ne, vaikka niiden sisältö on täysin sama. Tiketti: https://github.com/KohaSuomi/KohaSuomiServices/issues/13

**Siilinjärvi**
* ei mainittavaa Kohassa, muuten kiirettä.

**Kirkes**
* Keravan kirjastossa ei ollut nide tärpännyt Mäntsälän kirjastoauton varaukseen. Kirjastoautojen lainasäännöissä on muutenkin epäjohdonmukaisuuksia, mutta tutkitaan aina, kun tulee jotain ilmi.
* Järvenpäässä mietitään raportteja, joita lähettää Raportterin kautta kaupungin tietovarantoon. Elina tutkailee Oulun päivitettyä BI-raporttia, josko sitä voisi hyödyntää (Raportti täällä: https://github.com/KohaSuomi/Koha/issues/1051).

**Helle**
* Kehittäjä Lari Strand löysi ratkaisun siihen, miksi Helle-Finnan saatavuusnäkymässä tietueen kaikki niteet näkyvät Varattu-tilaisina, vaikka saatavilla olevia niteitä on enemmän kuin varauksia. Liittyy Kohan asetukseen AllowItemsOnHoldCheckoutSIP. Tiketti https://github.com/KohaSuomi/Koha/issues/1035
* Yhdestä Hankintaportaalin tilauksesta ei ole muodostunut tilausta Helle-Kohaan. Ilmoitusta virheellisestä tilaussanomasta ei ole tullut, eikä tilauksesta ole jälkeä EDIFACT-sanomissa. Hankintaportaalissa tilauksen tehnyt on saanut aineistotoimittajan vahvistusviestin tilauksesta.
* Ennakkoilmoitus-asiakasviesteissä on otettu käyttöön tieto lainaajakirjastosta. Tiketti https://github.com/KohaSuomi/Koha/issues/299


[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2024#viikko-6) - [Palaa sivun alkuun](/paakayttajat2024)

## Viikko 5

Aika: 30.1.2024 klo 9.15<br />
Läsnä: Leena Kinnunen (Lappi), Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Iina Niemi (Vaski), Hanna Ikonen (Lumme), Annika Helastila (Kirkes), Piia Semenoff ja Pirkko-Liisa Lauhikari (OUTI), Kati Sillgren (Helle), Tuomas Kunttu ja Roosa  Väisänen (Kyyti), Anneli Österman, Lari Strand, Johanna Räisä (Koha-Suomi)

**Yhteiset**
* [Yksiselitteinen ilmaisu varauksen keskeytyksen viimeiselle voimassaolopäivälle #19](https://github.com/KohaSuomi/Koha-translations/issues/19#issuecomment-1883024818)
  * Käydään Matrixin Finna-Yleinen-kanavan ehdotukset läpi
  * Pohdittiin erilaisia vaihtoehtoja päädyttiin tällaiseen vaihtoehtoon jäädytystä lisättäessä: Valitse päivä, jolloin varaus aktivoituu automaattisesti (vapaaehtoinen):
  * Kun varaus on jäädytetty/keskeytetty: Jäädytetty (väliaikaisesti keskeytetty) / Keskeytetty. Varaus aktivoituu xx.xx.xxxx (tai jos teksti paikkaan ei voi vaikuttaa, niin xx.xx.xxxx varaus aktivoituu)
  * Muutokset pystynee tekemään itse käännöksiin, joten jokainen kimppa voi tehdä ne itse.
* RenewAccruingItemInOpac ja RenewAccruingItemWhenPaid -asetuksia testattu OUTIssa.
  * asetukset toimivat kuvauksensa mukaisesti eli vain myöhässä olevien lainat uusitaan maksun jälkeen, jos ne on uusittavissa. Lastenaineistoa, joista ei kerry maksuja, ei uusita.
  * kimppakohtaisesti päätettävä, otetaanko käyttöön
  * Finnan maksusivua kannattaa joka tapauksessa parantaa ja selkeyttää, jotta asiakkaan hoksaavat käydä uusimassa lainansa.
* [Viikon 5 päivitys](https://github.com/KohaSuomi/Koha/discussions/1044)
* Bugi-perjantait harvennetaan joka toiseen kuukauteen, koska testattavia ei ole tarpeeksi.
* [Mana-testausten kokemukset](https://github.com/KohaSuomi/Koha/issues/677#issuecomment-1911734442)

Pohjoisesta etelään

**Lappi**
* Posion ja Sodankylän koulukirjastojen kanssa säätöä nidetyyppien, budjettien ja hankintaportaalin kanssa
* Edit-tilit näkymässä ei ole mahdollisuutta järjestää sarakkeita aakkosiin eikä suodatusta. Sovittiin, että Lappi tekee tästä kehitysehdotuksen yhteisöön
* Jos nide on poistettu, Finnan lainahistoriassa teos näkyy lainahistoriassa, mutta nimekkeenä on ei tietoa. Tehdään tiketti, jos niteen tiedot saisi näkyville esim. poistettujen tauluista tms.
* Kysytty, saisiko viivakoodin tilalle 2D-koodin, jättäisin tarralle lisää tilaa muulle tiedolle: ei tällä hetkellä mahdollista.

**Vaara**
* Päivi testannut Manan kuten yhteisissä asioissa mainittu
* Pasi Kallinen teki tiketin [#348](https://github.com/orgs/KohaSuomi/projects/4/views/1?filterQuery=348&pane=issue&itemId=17340272) toiveen mukaisesti viime yönä ajon, jonka tuloksena saatiin virhelista Vaaran emottomista osakohteista. Lista sisälsi myös virheilmoituksia tyyliin ERROR:Missing 001 [https://vaara.koha-suomi.fi/cgi-bin/koha/catalogue/detail.pl?biblionumber=151219] ja ERROR:003 needs trimming ( FI-BTJ) [https://vaara.koha-suomi.fi/cgi-bin/koha/catalogue/detail.pl?biblionumber=11298936]. Noiden virheiden korjaus täytynee tehdä muihinkin tietokantoihin, joten Pasi tekee sen tietokanta-ajona. 
Emottomien osakohteiden tietuelistauksen kohdalla on tapahtunut muutos, sillä siihen listaukseen tuli myös tietueita, jotka eivät olleet emottomia. Pasi korjaa skriptin tänään ja huomenna pääsen uudelleen testaamaan emottomien poistoa ajosta tulevan raportin avulla.

**Lumme**
* Täti-luetteloijat ovat alkaneet käydä läpi tietokannan tuplia ja triploja. Indeksiin jää edelleen roikkumaan poistettuja tietueita ja ongelma on selvittelyn alla.
* Kimpalla ja Lumme-Energialla oli sama lähettäjätunnus, minkä vuoksi kirjaston ja sähköyhtiön viestit alkoivat mennä samaan ketjuun. Ongelma poistui, kun kirjaston lähettäjätunnukseksi vaihdettiin "Kirjasto".

**Kirkes**
* Eri kimpan kaukopalvelija on ollut ihmeissään, kun Kirkes-Finna näyttää niteen havaintokirjaston kotikirjaston sijaan. Jos tarvetta, voidaan tehdä sääntö, joka sallii nidevaraukset kaukopalvelu-asiakasryhmälle. 
* MARC-virheraporttien käyttöönottoa odotellaan edelleen (tiketti https://github.com/KohaSuomi/Koha/issues/1015).

**OUTI**
* Ma 30.1. ajettu saapumisilmoitus tekstiviestinä täppä asiakkaille, joilla on puhelin numero Tekstiviesti numeroon -kentässä ja joilla ei ollut viestiasetuksissa valittuna mitään saapumisilmoitusten lähetystapaa ts. heillä oli sekä tekstiviesti- että sähköpostivalinnat tyhjinä. Liittyy tikettiin: https://github.com/KohaSuomi/Koha/issues/848.
* Oulun luetteloinnissa oli huomattu, että jos tilataan aineistoa, jolla ei ole varsinaista standardinumeroa, jolla yhdistää tietueen jo tietokannassa olevaan saman nimiseen tietueeseen, niin uusi hankintatietue ei tietenkään osaa yhdistyä siihen jo olemassa olevaan tietueeseen, vaan muodostaa uuden tuplatietueen. Sen päälle valuu sitten TäTistä oma, uusi täystietue osakohteineen. Mutta koska tietokannasta löytyi jo saman nimekkeen täystietue osakohteineen, niin Mikropalvelu hylkää kokonaan uuden tietueen valuvat osakohteet ja osakohteet olivat kadonneet myös tietueelta, joka oli jo ennestään tietokannassa. Olisikohan mitään keinoa täsmäyttää tietueita, joilla ei ole 020- tai 024-kentässä mitään tunnuksia, jotta vastaavaa ei tapahtuisi? Tiketti: https://github.com/KohaSuomi/KohaSuomiServices/issues/12
* OUTIin vanhojen lainassa olevien lainojen vanhentuneita myöhästymismaksuja on vanhennettu writeoff-ajona pariin kertaan. Ensimmäisen ajon 24.1. jälkeen maksut kertyvät asiakkaille uudestaan, mutta ajo tehtiin 29.1. uudestaan korjatulla skriptillä, eivätkä vanhennetut maksut ole enää kerääntyneet uudestaan.
* OUTIn Finna-testillä näkyy nyt oikein kutsumanimi ja varaustunniste. Tehdään tiketti, johon kirjataan kaikki tarvittavat toimenpiteet, jotka on tehtävä, jotta varaustunniste tulee jatkossa Finnaan oikein holdid-kentässä ja kutsumanimi calling_name-kentässä niille kirjastoille, jotka ottavat kutsumanimi-kentän käyttöön.

**Helle**
* Huomattu kausijulkaisutietueita, jotka tulevat tiedonhakuun tuplana. Nyt palaverissa saatu tieto, että tämä liittyy indeksointivirheeseen. Helle-tiketti (tehty pe 26.1.2024) https://github.com/KohaSuomi/Koha/issues/1041

**Kyyti**
* Kotkassa avattiin syksyllä uusi Lastenkulttuurikeskus, jonne meni pieni kokoelma lastenkirjoja. Niteiden oli tarkoitus olla vain Lakussa paikan päällä luettavissa, joten niiden tilaksi laitettiin "Ei lainattavissa (Ei varattavissa eikä lainattavissa)" ja yleiseksi huomautukseksi tieto niiden sijainnista Lakussa. Nyt on pohdittu, että jos näitä niteitä voisikin lainata Lastenkulttuurikeskukselta. Tämän seurauksena Kotkassa on alettu testaamaan Kohan itsepalvelulainausta.

**Vaski**

* Ei mainittavaa


[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2024#viikko-5) - [Palaa sivun alkuun](/paakayttajat2024)

## Viikko 4

Aika: 23.1.2024 klo 9.15<br />
Läsnä: Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Reetta Pihlaja (Siilinjärvi), Piia Semenoff ja Pirkko-Liisa Lauhikari (OUTI), Hanna Ikonen (Lumme), Annika Helastila ja Elina Uotila (Kirkes), Kati Sillgren (Helle), Tuomas Kunttu (Kyyti), Roosa Väisänen (Kyyti), Anneli Österman, Kodo Korkalo ja Lari Strand (Koha-Suomi), Mikko Liimatainen (Vaski), Leena Kinnunen ja Pia Kusmin (Lappi)

**Yhteiset**
* [SQL-raporttien jakaminen Koha-yhteisön Mana-tietokantaan #677](https://github.com/KohaSuomi/Koha/issues/677) tiketissä on ohjeet, kuinka käyttöönotto tapahtuu Kohan päässä ja kuinka raportteja jaetaan ja haetaan.
  * Päivi testaa ensin ja kertoo kokemuksia. Katsotaan sen jälkeen muut.
* [Tikettien tekeminen ja kommentointi](https://github.com/KohaSuomi/Koha/wiki/Tikettien-tekeminen-ja-kommentointi) -wikiä päivitetty.
  * lisätty tähdennys, että tikettejä saa tehdä vain pääkäyttäjät, koska ilmeisesti Github antaa nykyään kaikkien rekisteröityneiden käyttäjien lisätä tikettejä.
* [Viikon 4 päivitys](https://github.com/KohaSuomi/Koha/discussions/1025)
  * käännösmuutos myös Finnaan?
    * jokainen kimppa tekee itse muutoksen Finnan käännöksiin.
* Finnassa tänään päivitys, jossa mukana varaustunnus/kutsumanimi-muutos
    * muutos on tehtävä kaikkiin kimppoihin yhtä aikaa, koska vaatii Kohan päivityksen.
    * Finnaan tarvitaan uusi lomakepohja käyttöön, jotta tiedot menevät oikeisiin kenttiin Finnasta Kohaan.
    * OUTI tekee Finna-toimistoon pyynnön kaikkien puolesta. Kutsumanimi-kenttä halutaan vain OUTIssa ja Vaskissa käyttöön eli muissa kimpoissa sitä ei haluta näkyviin.
    * Vaski on pyytänyt testille lomakkeiden korjauksen. OUTI odottaa, miten ne lähtee toimimaan ja pyytää sitten itselle testille. 
* Vanhentuneet maksut -ajossa muodostunut myöhässä olleille lainoille uudet myöhästymismaksut
  * Muutetaan vanhentamisskirpti writeoffaamaan, noteen tieto mitätöinnistä.
  * muutetaan accountlines-taulusta expired-maksurivit writeoff-maksuriveiksi. 
  * OUTIssa ja Kyytissä date-kenttä päivittynyt 2021 tehdyn myöhästymismaksumuutoksen vuoksi, jolloin lainassa olleiden niteiden maksurivit päivittyi. Tuolloin ei vielä ollut erillistä timestamp-kenttää. Nyt kun date on päivittynyt, maksurivit eivät tulleet mukaan vanhentamisajoon.
  * OUTI ja Kyyti tekee tiketit päivämäärien korjauksista Vaskin skriptillä ja sen jälkeen maksut vanhennetaan korjatulla vanhentamisskriptillä
* Alla olevilla raporteilla voi hakea asiakkaat, joilla on maksut muodostunut uudelleen. Ne joutuu käymään läpi käsin ja writeoffaamaan ylimääräiset maksut.
```
SELECT DISTINCT i.borrowernumber
FROM issues i
INNER JOIN accountlines al ON i.itemnumber = al.itemnumber AND i.borrowernumber = al.borrowernumber
INNER JOIN (SELECT borrowernumber from accountlines
			 WHERE credit_type_code = 'EXPIRED') as exp ON exp.borrowernumber = al.borrowernumber
WHERE al.debit_type_code = 'OVERDUE'
AND date(i.date_due) < '2019-01-01'
ORDER BY 1 ASC
```

* Kannattaisiko ottaa käyttöön RenewAccruingItemInOpac ja RenewAccruingItemWhenPaid -asetukset? Testattava ennen käyttöönottoa.
  * asetuksissa rajoitteena se, että jos tietueeseen liittyy varaus tai uusimiskerrat täynnä, niin uusintaa ei voida tehdä
  * miten käy, jos maksaa maksun vain osittain? Järjestelmäastuksen kuvauksen mukaan uusinta tehdään vain, jos kaikki maksut maksetaan.
  * OUTIssa Pirkko-Liisa testaa ja katsotaan sen jälkeen, kannattaako ottaa käyttöön. 
* Uusien ominaisuuksien esittely suurelle yleisölle ke 17.4.2024 klo 13 - tallennetaan
* Pääkäyttäjille esittely to 1.2.2024 klo 10 - tallennetaan

Etelästä pohjoiseen

**Vaara**
* Joensuun kaupungin tilaama Koha-appi on osa Joensuun kaupungin mobiilisovellusta. Toimitettu testitunnukset kehittäjille.
* Päivi korjaillut musiikkiaineistojen koodausta mm. musiikkitallenne-aineistotyypiltä eli tarkentanut 007-kentän koodausta ja vaihtanut oikean aineistotyypin osakohteelle. Kaikki tähtää RDA-konversion parempaan onnistumiseen, kun lähtödata on paremmassa kuosissa. Odotellaan myös kehittäjien tekemiä massakorjauksia tietyille kentille, jotka (miltei) kaikissa kimpoissa kaipaavat korjausta.
* Eilen saatiin Vaaran next-kanta käyttöön ja Päivi on testannut jo muutaman tiketin kautta toimintoja. 
 
**Siilinjärvi**
* OPACPrivacy-asetus oli Älä salli, nyt korjattu Salli eli Yksityisyysasetus käännösmuutoksineen näkyy virkailijaliittymässäkin.
* [#1018](https://github.com/KohaSuomi/Koha/issues/1018) ongelmana Siilissä, sen sijaan mitätöityjen vanhentuneiden maksujen uudelleen kertyminen [#804](https://github.com/KohaSuomi/Koha/issues/804) ei koske meitä

**OUTI**
* OUTIssa oli syntynyt ainakin Oulun lasten- ja nuorten kirjatilauksille ylimääräisiä haamuniteitä maalis-toukokuun aikana 2023. Tapauksia oli tullut vastaan n. kymmenkunta. Ylimääräiset niteet oli huomannut hankintaa tekevä henkilö, kun hän oli käynyt läpi Oulun osalta raporttia "Nimekkeet, joissa on niteitä tilattu-tilassa". Ylimääräinen tilattu-tilassa oleva nide oli syntynyt eri välilehdelle missä olivat kirjaston muut oikeasti tilatut niteet. Haamunide oli syntynyt tietokantaan muutamaa tuntia aiemmin kuin varsinaiset tilatut niteet. Tiketti: https://github.com/KohaSuomi/Koha/issues/1024
* Finna-tukeen laitettu maksujen maksimimäärärajasta, joka ei aivan toimi lainojen uusinnassa. Eli Finna sallii sentin enemmän maksuja kuin Kohan järjestelmäasetuksiin on määritelty maksujen maksimäärästä. Varausten teossa maksuraja toimii eli varauksia ei pysty tekemään, jos maksujen maksimimäärä on ylittynyt.
* Oulun Ceepos-palvelin siirretty viime viikonloppuna (la-su välisenä yönä) Istekille. Siirto ei työllistänyt Koha-tukea. Ceepos oli saatu toimimaan ennen kirjaston asiakaspalvelun alkua. Verkkomaksupalvelu oli pois käytöstä siirron ajan.
* Selvisi miksi kaikilla asiakkailla ei näy Finnassa Lainat-näytöllä "Uusi kaikki"-nappi. Kun lainoja on 26 tai sitä enemmän, niin silloin nappi katoaa, sillä lainat näkyvät tuolloin useammalla sivulla kuin yhdellä. Laitoimme Finna-tukeen viestiä, että katoaako nappi sen vuoksi ettei sillä voi uusia kaikkia lainoja, jos lainat jakautuvat usealle sivulle? Ehdotimme, että voisivatko kaikki lainat näkyä yhdellä sivulla, jolloin nappi näkyisi kaikille asiakkaille eikä katoaisi välillä?

**Lumme**
* Asiakasrekisterin läpikäynti ja sen siivous on mennyt vähän eteenpäin. Tällä hetkellä tehty raportteja ei-aktiivisista asiakkaista.
* Henkilökunnalla on välillä vaikeuksia muistaa tallentaa sotua sotusiiloon. Tähän toivottiin jonkinlaista ratkaisua tai muistutusta. Myöhemmin mahdollisesti tulossa kaksivaiheinen asiakkaan lisääminen: ensin lisätään mahdollinen sotu ja vasta sen jälkeen pääsee lisäämään asiakkaan tietoja.

**Kirkes**
* Koska järjestelmä vaihtui kesken vuoden, nyt yritetään yhdistää Auroran ja Kohan aikana kertyneitä tilastoja niin, että lopputulos olisi OKM-tilastoja varten mahdollisimman oikea.

**Helle**
* Integraatiot-listaan tehty yksi päivitys (tarkennus) Helleen liittyen
* Helle-Finnassa saatavuustiedot saattavat edelleen näkyä väärin, kun nimekkeeseen kohdistuu varaus/varauksia. Keskustelua käyty Finna-toimiston kanssa, mutta ratkaisua ei ole löytynyt. Olisiko tähän ratkaisu Kohan puolella? Tiketti tehty https://github.com/KohaSuomi/Koha/issues/1035

**Kyyti**
* Kovasti nyt kiirettä muidenkin kuin Koha-asioiden kanssa
* Kysyin, että haittaako kun "Hallinnoi välivarastoituja MARC-tietueita"-osiossa on 20 sivua vanhoja (2018) Btj:n ennakkolistoja vai pitäisikö niitä poistaa. - Eivät kuulemma haittaa.
* Kotkassa tehty uusi Koha-tunnus ja asennettu varmenne ja kuittitulostimen asetukset.

**Vaski**
* Finnassa varaukset ja lainat sivuilla on valintaruutu kaikkien lainojen tai varausten valitsemiseen ilman selitettä. Tästä aiheutuu ongelmia, koska asiakkaat voivat helposti peruuttaa kaikki varauksensa tietämättä tekevänsä niin. Mietitään tähän ratkaisua esimerkiksi peruttavien varausten määrän näyttämistä poiston vahvistus ruudussa.

**Lappi**
* RDA-muutosta varten kuvailutiimi kokoaa korjausajolistaa
* Varmistettiin perustelut asiakkaalle, miksi henkilötunnus on tallennettava myös lapsiasiakkaalle. 

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2024#viikko-4) - [Palaa sivun alkuun](/paakayttajat2024)

## Viikko 3

Aika: 16.1.2024 klo 9.15<br />
Läsnä: Piia Semenoff, Pirkko-Liisa Lauhikari ja Veli-Pekka Marjoniemi (OUTI), Päivi Knuutinen (Vaara), Anni Rajala (Vaski), Kati Sillgren (Helle), Hanna Ikonen (Lumme), Anneli Österman ja Pasi Kallinen (Koha-Suomi), Tuomas Kunttu (Kyyti), Reetta Pihlaja (Siilinjärvi), Leena Kinnunen, Pia Kusmin ja Maria Joona (Lappi)

**Yhteiset**
* Onko [Integraatiot-lista](https://github.com/KohaSuomi/Koha/wiki/Integraatiot) oman kimpan osalta ajantasalla? Uusia, poistuneita?
* [Yksiselitteinen ilmaisu varauksen keskeytyksen viimeiselle voimassaolopäivälle #19](https://github.com/KohaSuomi/Koha-translations/issues/19#issuecomment-1883024818)
  * Anneli muuttaa until-tekstit niin, että valitaan ensimmäinen päivämäärä, jolloin varaus jatkuu.
  * Anneli tekee tiketin yhteisöön until-sanan epämääräisyydestä
  * Finnan käännökset kannattaa myös katsoa läpi ja jos joku keksii hyvät käännökset, voi niitä ehdottaa Finna-kanavalla Matrixissa. Käydään läpi ensi viikolla ja päätetään, mitkä niistä olisi hyvä ja laitetaan sitten Finna-toimistoon pyyntö muuttaa teksti kaikille kerralla.
* [Vkon 3 päivitys](https://github.com/KohaSuomi/Koha/discussions/1010)
* Muistutus: [Useamman samanaikaisen varauksen varaamisessa valinnan poisto tietueelta ei vaikuta ja varaus tehdään silti #780](https://github.com/KohaSuomi/Koha/issues/780) - CSS:n lisäys
* Sovittiin, että kimpoissa kerätään lista yleisimmin käytetyistä kielikoodeista, jolta puuttuu vielä selkokielinen käännös, joka näkyy faseteissa. Lisätään niille sitten käännös tietokannan tauluun. Ei lisätä käännöstä kaikille mahdollisille yli 400 kielikoodille. Tällä hetkellä käännös löytyy 116 kielikoodille. Listat kirjataan [tikettiin #885](https://github.com/KohaSuomi/Koha/issues/885).

Pohjoisesta etelään

**OUTI**
* Kempeleen liikuntalainaamolle on tehty uusi nidetyyppi, joka on muutoin sama kuin meidän lyhytlainat, mutta laina-aika on 3 vrk.
* Vaalan kirjastosta on tullut myös toive, että haluaisivat saman tyyppisen uuden nidetyypin, mutta jossa laina-aika olisikin 7 vrk.
* Muhoksen kirjasto on mennyt remontin vuoksi kokonaan kiinni eilen 15.1. ja on loppukuun kiinni. Kirjaston niteet muutettu Muuttolaatikossa-tilaan.
* OUTIssa maksujen maksimimäärä on Finnassa sentin isompi kuin Kohassa. 
  * OUTIssa lainauskiellon raja on 11,99 euroa.
  * Jos asiakkaalla on maksuja 12,00 euroa, asiakas on Kohassa lainauskiellossa, mutta Finnassa raja tulee vastaan, kun asiakkaalla on maksuja 12,01 euroa.
  * Finnaan tulee kyllä ilmoitus, että kirjastokorttisi on lainauskiellossa, mutta asiakas pystyy uusimaan lainansa.
  * Tätä ei ole havaittu muissa kimpoissa.
    * Sovittiin, että muissa kimpoissa tätä testataan ja kirjataan asiasta Matrixin Finna-kanavalle ja Pirkko-Liisa ottaa lopuksi yhteyttä Finna-tukeen.
   
**Vaara**
* ei mitään erityistä mainittavaa, paitsi tiedustelu Firefox esr-versiosta, mikä muilla kimpoilla on käytössä. Suurimmalla osalla Firefox 115.6.0esr tai 115.3.1esr. Vaarassa vanhempia versioita. Pitää pyytää päivittämään.

**Vaski**
* Pidemmät pin-koodit otettu virallisesti käyttöön (muutokset automaateille, ovilukijoille ja verkkokirjastoon tehty jo aiemmin, mutta tästä viikosta eteenpäin aletaan varsinaisesti tarjoamaan 4-10 numeroa pitkää koodia).
* ATK-ihmisten kokoontumisajot Turussa 25.-26.4.2024, vanhalla jakelulistalla lähtenyt ennakkotieto eilen. Esitys-ehdotuksia otetaan vastaan. Ohjelma ja ilmoittautumislinkki tulossa, kunhan valmistuvat.
* Seinäjoki pyytänyt Koha-esittelyä helmikuulle.

**Helle**
* Asiakastiedon avausyrityksesta Koha antanut Virhe 500 -ilmoituksen. Syy: asiakastiedossa oli syntymäaika-arvona kesäaikaan siirtymispäivä. Tiketti #624
* Marc-mäppäysmuutos tehty sovitusti 15.1.2024 (biblio.copyrightdate-sarakkeeseen MARC-kentät 264c ja 260c).

**Lumme**
* Normaalia ylläpitoa.

**Kyyti**
* Ei erityistä, vasta töihin palattu.

**Siilinjärvi**
* Ei erityistä
* Joudutaan ehkä tekemään uusi nidetyyppi konsolipeleille, jotta niille saadaan tiukempi lainarajoitus. Tämä yksittäisen asiakkaan vuoksi.

**Lappi**
* Kemin kassa saatu toimimaan päivityksen jälkeen.
* Posion koulukirjastoa varten tehty uusi nidetyyppi 56 vrk:n aineistoille. 

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2024#viikko-3) - [Palaa sivun alkuun](/paakayttajat2024)

## Viikko 2

Aika: 9.1.2024 klo 9.15<br />
Läsnä: Anneli Österman, Kassu Pohto, Lari Strand (Koha-Suomi), Reetta Pihlaja (Siilinjärvi), Kati Sillgren (Helle), Pirkko-Liisa Lauhikari ja Piia Semenoff (OUTI), Leena Kinnunen ja Pia Kusmin (Lappi), Päivi Knuutinen, Auli Rantasalo, Irina Halminen (Vaara), Hanna Ikonen (Lumme), Mikko Liimatainen (Vaski), Annika Helastila, Elina Uotila (Kirkes)

**Yhteiset**
* Etenemisaikataulu [tiketille 693 eli publicationyear/copyrightdate -mäppäysmuutos](https://github.com/KohaSuomi/Koha/issues/693)
  * [Mäppäysmuutoksen teko-ohje](https://koha-suomi.fi/dokumentaatio/asetukset/#19-kohan-marc-m%C3%A4%C3%A4ritykset)
  * Porrastetaan niin, että ajetaan kaksi kimppaa/yö. Mäppäysmuutos pitää tehdä ennen ajoa. Peukuta tiketissä seurantakommenttia, kun mäppäysmuutos on tehty. Lari täppäilee biblio-ajon täpät.
    * 9.1. Lappi ja OUTI
    * 10.1. Siili ja Vaara
    * 11.1. Lumme Kyyti
    * 15.1. Helle ja Kirkes
    * 16.1. Vaski
* Miten kannattaa edetä [tiketin #780](https://github.com/KohaSuomi/Koha/issues/780) suhteen?
  * Riittääkö raksien piilotus vai pitäisikö raksit saada vaikuttamaan.
    * Päätös: piilotetaan raksit
* [Haluaako joku testata](https://github.com/KohaSuomi/Koha/issues/628)?
* [Vkon 2 päivitys](https://github.com/KohaSuomi/Koha/discussions/999)
* [Huoltoikkuna keskiviikkona 10.1.2024](https://github.com/KohaSuomi/Koha/discussions/993)
  * [Redmine suljetaan](https://github.com/KohaSuomi/Koha/discussions/994)

Etelästä pohjoiseen

**Siilinjärvi**
* Ei mitään merkittävää
* Paitsi edelleen ihmetellään Finna-toimiston kanssa, miksi lainaushistoria Finnassa näkyy tietokoneella, mutta ei mobiililaitetta käytettäessä. Lainaushistoria tuntuu olevan asiakkaille kuitenkin tärkeä asia. Keskusteltiin laajemminkin lainaushistoriasta, esim. poistettujen niteiden puuttumisesta lainaushistoriassa.

**Helle**
* Asiakkaan maksujen poistosta muodostunut maksuihin hyvitettävää poistettavien maksujen arvosta. Voisiko johtua siitä, että ko. maksuja on poistettu kahdessa kirjastossa lähes samaan aikaan (maksutapahtumissa sekunnin aikaero accountlines-taulussa).

**OUTI**
* Muutamilla asiakastunnuksilla hävinnyt verkkokirjastosta Lainat-sivulta ”Uusi kaikki” toimintapainike. Ongelmasta laitettu Finna-tukeen.
* Ilmoitetaan Finna-tukeen, että kaikille Koha-Suomen kimpoille voivat laittaa tuotantoon palautuskehotusten tekstit ja käännökset.
* Koha-jumit 8.1. n. klo 9.37 ja 9.1. n. klo 9.32. Aiheuttajana OUTIa vaivanneet tietokantataulujen lukkiutumiset. Yritetään tehdä koha-suomimuutos, jolla näistä ongelmista päästäisiin eroon.
* Oulun kaupungin laskutusjärjestelmä muuttuu Intimestä Unit4:een.
* Teoksen varaukset sivulla ”Saatavana, ei lainattavissa” (damaged-arvo) olevilla niteillä näkyy Varaus-sarakkeessa ”Nide vaurioitunut”. Edellisessä versossa käännöksenä oli ”Ei varattavissa”. Päätettiin, ettei tehdä käännöstä tälle.

**Lappi**
* kysyttiin miten niteiden tilat vaikuttavat OKM:n lainatilastoihin. Tieto löytyy OKM-raportin asetuksista.
* Kemissä päivitetty CPU:n kassa ja yhteydet Kohaan katkenneet, asia ilmeisesti CPU:lla ja Kodolla hoidossa.
* Lapin henkilökunnan Kysy Kohasta -tilaisuus suunnnittelussa, samoin käyttäjäryhmän kokous.

**Vaara**
* Tilastotietojen keruu alkanut
* Päivi yritti saada Vaskin viikolla 51 kertoman tyylisen nidetyypin käyttöön. Nidetyypissä voi varata esineen vain niteen kotikirjastosta
lainattavaksi. Testi-Finnassa varauspainike ei tullut ollenkaan näkyviin, jos asiakkaan kotikirjasto oli muu kuin ko. esineen kotikirjasto. Kun 
asiakas oli samasta kirjastosta kuin esine, varauspainike tuli näkyviin. Kysyin neuvoa myös Vaskista, mutta ei sielläkään keksitty mikä olisi eri tavalla
asetuksissa meidän järjestelmissä.
* Hyllyvarauslista on joidenkin mielestä epäselvä, mikä kummastuttaa.

**Lumme**
* Lumpeissa ollut syksyllä usein indeksointivirheitä tietueiden poistojen jälkeen. Ongelma näyttää johtuvan siitä, että Koha luo indekseille replikan, joka ei toimi. Nyt nämä replikat on tiputettu pois.
* Asiakas toivoi Finnaan tulostettavaa versiota lainaushistoriasta. Tämä ei ole käytännöllistä listan jatkuvan päivittymisen takia, joten asiaa ei viedä eteenpäin.

**Vaski**
* Varauksen keskeytyksessä viimeistä päivää ei lasketa keskytykseen mukaan. Tämä on toisin aiempaa käsitystä, jonka takia käänösteksteissä ja verkkokirjastossa puhutaan keskeytyksen viimeisestä voimassaolopäivästä
* Järjestelmänvaihdon ajalta huomattiin maksuja, joissa maksun muodostumispäivä on virheellisesti 4.6.2021. Nämä maksut eivät nyt poistu automaattisesti niin kuin pitäisi.
* Puppe ollut käytössä muutaman viikon ajan. Tunnelmat olleet positiivisia. Voidaan järjestää esittely muillekin Pupen käytöstä.

**Kirkes**
* Sarastian mukaan zip-tiedostona tulevat yksittäiset laskut ovat liian työläiltä. Kuitenkin Vaskista lähtevät laskut samalla tavalla. Jatketaan asian selvittelyä ensi viikolla, kun Emmi palaa lomalta.
* Lisätty Tarramuutos -tila käyttöön ohjeen (https://github.com/KohaSuomi/Koha/issues/799) mukaisesti. Ihmetellään sen toimintaa vielä.
* Toivottiin Videopelien lainamäärät -raportin korjausta ja kyseltiin mahdollisuutta selvittää seutulainojen lukumäärää.

[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2024#viikko-2) - [Palaa sivun alkuun](/paakayttajat2024)

## Viikko 1

Aika: 2.1.2024 klo 9.15<br />
Läsnä: Anneli Österman, Emmi Takkinen ja Lari Strand (Koha-Suomi), Reetta Pihlaja (Siilinjärvi), Leena Kinnunen ja Pia Kusmin (Lappi), Hanna Ikonen (Lumme), Päivi Knuutinen ja Irina Halminen (Vaara), Pirkko-Liisa Lauhikari ja Piia Semenoff (OUTI), Mikko Liimatainen (Vaski)

**Yhteiset**
* Kuittaus [tikettiin 459](https://github.com/KohaSuomi/Koha/issues/459), kun järjestelmäasetus muutettu.

Pohjoisesta etelään.

**Siilinjärvi**
* Maksujen mitätöinnit näyttäisivät menneen ainakin päällisin puolin ok.
* Unohtunut mainita: joulukuussa esitelty Kangasniemelle pienen kirjaston Koha-pääkäyttäjän tehtäviä.

**Lappi**
* Korjattu BTJ:n vanhat kirjankansilinkit (72376 kpl).
* Muita pieniä korjauksia
* Joissakin tietueissa Koha ja Finna ei osaa näyttää oikein &-merkkiä, vaan ne näkyvät tekstinä &amp;. Koskee lähinnä hankintatietueita, korjaantuu todennäköisesti, kun tulee täysi tietue.

**Lumme**
* Ei mitään mainittavaa.

**Vaara**
* Ei mitään mainittavaa.

**OUTI**
* Asiakkaalta tullut palautetta, että Finnan lainaus- ja varaussivuilla olevat toimintopainikkeet ”Uusi valitut”, ”Uusi kaikki”, ”Muokkaa valittuja” ja ”Peru valitut” ovat niin harmaita ja huomaamattomia, että niitä on hankala huomata sivuilta. OUTIn Finna-tuki reklamoinut asiasta Finnaan.
* Asiakkaalta tuli palautetta, että hänen kahdesta lainasta vain toisesta oli tullut lainakuitti sähköpostiin.Tiketti: [OUTI: Kaikki asiakkaan lainat eivät muodostuneet "Lainasit tänään"-viestiin · Issue #991 · KohaSuomi/Koha (github.com). ](https://github.com/KohaSuomi/Koha/issues/991)
* Finnassa näkyvien palautuskehotusten otsikon ja selitteiden tekstimuutokset. Tiketti: [Finnassa näkyvien palautuskehotusten otsikon ja selitteiden muutokset · Issue #21 · KohaSuomi/Finna-kehitysehdotukset (github.com).](https://github.com/KohaSuomi/Finna-kehitysehdotukset/issues/21) Voisiko kimpat, joissa ruotsinkieliset sivut käytössä, tarkistaa, että palautuskehotusten tekstit näkyvät myös ruotsiksi oikein. Pyydetään sitten Finna-tukea laittamaan käännökset kaikille kimpoille tuotantoon.
* Raahen pieni Haapajoen kirjaston toiminta laikkaa 1.2.2024. Tehtävänä lakkautukseen liittyviä toimenpiteitä.

**Vaski**
* Ei mitään mainittavaa.
  
[Palaa muistion alkuun](https://koha-suomi.fi/paakayttajat2024#viikko-1) - [Palaa sivun alkuun](/paakayttajat2024)

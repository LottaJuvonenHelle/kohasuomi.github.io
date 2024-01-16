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

## Viikko 3

Aika: 16.1.2024 klo 9.15<br />
Läsnä: Piia Semenoff, Pirkko-Liisa Lauhikari ja Veli-Pekka Marjoniemi (OUTI) 

**Yhteiset**
* Onko [Integraatiot-lista](https://github.com/KohaSuomi/Koha/wiki/Integraatiot) oman kimpan osalta ajantasalla? Uusia, poistuneita?
* [Yksiselitteinen ilmaisu varauksen keskeytyksen viimeiselle voimassaolopäivälle #19](https://github.com/KohaSuomi/Koha-translations/issues/19#issuecomment-1883024818)
* [Vkon 3 päivitys](https://github.com/KohaSuomi/Koha/discussions/1010)
* [Useamman samanaikaisen varauksen varaamisessa valinnan poisto tietueelta ei vaikuta ja varaus tehdään silti #780](https://github.com/KohaSuomi/Koha/issues/780) - CSS:n lisäys

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

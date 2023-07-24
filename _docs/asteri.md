---
title: 'Asteri-liitännäiset'
permalink: /dokumentaatio/asteri/
redirect_from:
  - /theme-setup/
toc: true
---

Asteri-liitännäisellä pystyy hakemaan Kansalliskirjaston auktoriteettitietokanta Asterista auktorisoituja nimimuotoja. Liitännäisen nimi on finto_finaf.pl ja sen voi 
kytkeä käyttöön MARC-luettelointipohjien ylläpidossa tarvittaviin MARC-kenttiin (lista alla). Primääriluettelointi tehdään TäTissä, joten liitännäisiä ei tarvitse ottaa käyttöön paikalliskannoissa. 
TäTissä se on käytössä kaikissa luettelointipohjissa paitsi oletuspohjassa. Siinä se ei ole käytössä, jotta nimitietoja pystyy tarvittaessa muokkaamaan, 
jos Asterista/Kanto-tietokannoista tulee puutteelliset tiedot (puuttuu esim. pilkku tai piste).

## Liitännäisen määrittäminen käyttöön

Mene Ylläpito -> MARC-kuvailupohjat

Asteri-liitännäinen lisätään kenttiin 100a, 110a, 111a, 600a, 610a, 611a, 700a, 710a, 711a, 800a, 810a ja 811a kaikkiin muihin pohjiin paitsi oletuspohjaan.

## Liitännäisen toimintatapa

Liitännäinen hakee toimijanimitiedot KANTO:sta ja tallentaa Asterista auktoriteettitietueen TäTiin. Tekijäkenttään tulee nimitiedot 
ja 0-osakenttään Asteri-ID. Lisää myös syntymäajan d-osakenttään, jos sellaiset auktoriteettitietueesta löytyy. 
Yhteisönimissä voi olla mukana tarkenteita suluissa nimen perässä, kuten Metallica (yhtye).

Hae a-kentässä toimijanimellä ja valitse sopiva.
![](/assets/files/docs/Ohjeet/asteri.png)

Liitännäinen hakee Asterista auktoritettitietueen tiedot. Tuo ne tietokantaan klikkaamalla alareunasta "Valitse".
![](/assets/files/docs/Ohjeet/asteri2.png)

Tiedot viedään oikeisiin osakenttiin.
![](/assets/files/docs/Ohjeet/asteri3.png)

Välimerkityksen lisääminen puuttuu vielä pluginista. Jos auktoriteettitietueen mukana ei tule pilkkua a-osakenttään toimijanimen loppuun, on toimittava niin, että vaihtaa lopuksi luettelointipohjan oletuspohjaksi ja lisää tarvittavat välimerkit (pilkku tai piste) a-kentän loppuun. Voi myös vaihtaa kehittyneeseen editoriin.

Jos auktoriteettitietuetta ei löydy Asterista, lisätään nimi oletuspohjan kautta. TäTiin ei tehdä erillistä auktoriteettitietuetta.

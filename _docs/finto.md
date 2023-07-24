---
title: 'Finto-liitännäiset'
permalink: /dokumentaatio/finto/
redirect_from:
  - /theme-setup/
toc: true
---

## Finto-liitännäiset

Finto-liitännäiset ovat käytössä Täti-tietokannassa.

Kuvailussa voidaan käyttää liitännäisiä, jotka hakevat tiedot Finton sanastoista. Kun liitännäinen on lisätty kenttään, kuvailija voi kirjoittaa kyseiseen kenttään hakutermin, jolla sanastosta haetaan, ja valita sopivan arvon suoraan valikosta. Osakenttään tulee siis valittu arvo, osakenttään 0 tulee lähde-URI, ja osakenttään 2 tulee lähteen nimi, esim. "yso/fin"

Finto-liitännäisten nimet alkavat "finto_", jonka jälkeen on sanasto, josta plugin hakee tiedot (esim. "seko", "yso"). Jos nimessä on "local", sallii plugin myös paikallisen arvon lisäämisen, ja jos pluginin nimi päättyy "_ind", asettaa se myös kentän toisen indikaattorin arvoksi "7".

### Liitännäisen määrittäminen käyttöön

Kannattaa tehdä ainakin nämä määritykset alkuunsa:

MARC-kenttä|Kentän kuvaus|Liitännäinen
---|---|---
257$a|Tuottajan maa|finto_ysopaikat.pl
370$g|Teoksen tai ekspression luontipaikka|finto_ysopaikat.pl
650$a|Aihetta ilmaiseva termi tai maantieteellinen nimi|finto_yso-kauno.pl
651$a|Maantieteellinen nimi|finto_ysopaikat.pl
655$a|Lajityyppiä/muotoa kuvaava temi tai fokustermi|finto_slm-local.pl

Ylläpito -> MARC-kuvailupohjat

Valitse muokattavan kuvailupohjan kohdalta Toiminnot -> MARC-rakenne
![](/assets/files/docs/Ohjeet/finto.png)

Hae muokattava kenttä
![](/assets/files/docs/Ohjeet/finto2.png)

Valitse kentän kohdalla Toiminnot -> Näytä osakentät
![](/assets/files/docs/Ohjeet/finto3.png)

Valitse oikean osakentän kohdalla _Muokkaa_
![](/assets/files/docs/Ohjeet/finto4.png)

Mene Muut vaihtoehdot (valitse yksi) -osioon ja mahdollisesti poista ensin Sanasto-valinta.
![](/assets/files/docs/Ohjeet/finto5.png)

Valitse sitten Liitännäinen-valikosta tarvittava liitännäinen ja tallenna muutokset.
![](/assets/files/docs/Ohjeet/finto6.png)

Tarkista, että kentän tiedoissa näkyy juuri valittu liitännäinen.
![](/assets/files/docs/Ohjeet/finto7.png)

Muokkaa myös muut kentät. Helpoiten pääset kentän valintaan "murupolusta" klikkaamalla.
![](/assets/files/docs/Ohjeet/finto8.png)


### Liitännäisen toiminta kuvailussa

Liitännäisiä on useamman tyyppisiä ja ne toimivat pääsääntöisesti samalla periaatteella. Osassa voi kuitenkin käyttää myös "paikallisia" termejä, jolloin liitännäinen toimii vähän eri tavalla.

#### YSO/Kauno

Liitännäinen noudattaa käyttöliittymän kielivalintaa eli kun Kohassa on käyttökielenä suomi, haetaan suomenkielisiä termejä. Kun taas käyttöliittymän kieli on ruotsi, haetaan termejä ruotsinkielisestä sanastosta.

Liitännäisiä on kaksi, jotka liitetään eri kenttiin:

Liitännäinen|Liitettävä kenttä
---|---
finto_yso-kauno.pl|650a
finto_ysopaikat.pl|651a

Kun kenttään alkaa kirjoittamaan termiä, lähtee liitännäinen hakemaan sitä Fintosta ja ehdottaa hakua vastaavia termejä. Sulkeissa termin perässä lukee, kummasta sanastosta, ysosta vai kaunosta, termiä ehdotetaan.
![](/assets/files/docs/Ohjeet/finto9.png)

Kun listalta valitsee termin, tuodaan sen tiedot oikeisiin kenttiin. 0-kenttään lisätään linkki termiin ysossa ja 2-kenttään asiasanan/termin lähde.
![](/assets/files/docs/Ohjeet/finto10.png)

#### SLM - Suomalainen lajityyppi- ja muotosanasto

Liitännäinen on 655a-kentässä ja nimeltään finto_slm-local.pl.

Kun 655-kenttään alkaa kirjoittamaan termiä, lähtee liitännäinen hakemaan sitä SLM-termeistä ja ehdottaa vastaavia termejä.
![](/assets/files/docs/Ohjeet/finto11.png)

Kun listalta valitsee termin, tuodaan sen tiedot oikeisiin kenttiin. 0-kenttään lisätään linkki termiin SLM-sanastossa ja 2-kenttään termin lähde.
![](/assets/files/docs/Ohjeet/finto12.png)

Kun tämä pluginin on käytössä, pystyy kirjoittamaan myös ns. paikallisia termejä. Tällöin 655a-kenttään kirjoitetaan haluttu sana ja 2-kenttään tulee termin lähteeksi "local" sekä 2. indikaattoriksi '7'. **HUOM!** Tällä hetkellä pitää ensin painaa a-kentän viereistä editoria, jotta oman termin lisääminen onnistuu.

!fintoplug13.png!

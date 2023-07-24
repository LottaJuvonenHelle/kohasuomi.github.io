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

KIR-kuvailupohjassa on määritetty käyttöön seuraavat liitännäiset:

| Kenttä | Osakenttä | Selite | Liitännäinen |
|---|---|---|---|
| 100      | a           | Henkilönnimi                                      | finto_finaf.pl            |
| 110      | a           | Yhteisönnimi                                      | finto_finaf.pl            |
| 111      | a           | Kokouksen tai hallintoalueen nimi                 | finto_finaf.pl            |
| 257      | a           | Tuottajan maa                                     | finto_ysopaikat_noind.pl  |
| 370      | g           | Teoksen tai ekspression luontipaikka              | finto_ysopaikat_noind.pl  |
| 382      | a           | Esityskokoonpano                                  | finto_seko_nouri_noind.pl |
| 382      | b           | Solisti                                           | finto_seko_nouri_noind.pl |
| 382      | d           | Sivusoitin                                        | finto_seko_nouri_noind.pl |
| 382      | p           | Vaihtoehtoinen esityskokoonpano                   | finto_seko_nouri_noind.pl |
| 385      | a           | Kohderyhmä                                        | finto_yso-kauno_noind.pl  |
| 386      | a           | Tekijä                                            | finto_yso-kauno_noind.pl  |
| 388      | a           | Luomisaika                                        | finto_yso-aika.pl         |
| 600      | a           | Henkilönnimi                                      | finto_finaf.pl            |
| 610      | a           | Yhteisönnimi                                      | finto_finaf.pl            |
| 611      | a           | Kokouksen tai hallintoalueen nimi                 | finto_finaf.pl            |
| 648      | a           | Aikaa ilmaiseva termi                             | finto_yso-aika_noind.pl   |
| 650      | a           | Aihetta ilmaiseva termi tai maantieteellinen nimi | finto_yso-kauno.pl        |
| 651      | a           | Maantieteellinen nimi                             | finto_ysopaikat.pl        |
| 655      | a           | Lajityyppiä/muotoa kuvaava termi tai fokustermi   | finto_slm-local.pl        |
| 700      | a           | Henkilönnimi                                      | finto_finaf.pl            |
| 710      | a           | Yhteisönnimi                                      | finto_finaf.pl            |
| 711      | a           | Kokouksen tai hallintoalueen nimi                 | finto_finaf.pl            |
| 800      | a           | Henkilönnimi                                      | finto_finaf.pl            |
| 810      | a           | Yhteisönnimi                                      | finto_finaf.pl            |
| 811      | a           | Kokouksen tai hallintoalueen nimi                 | finto_finaf.pl            |


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

#### YSO - yleinen suomalainen ontologia ja KAUNO - fiktiivisen aineiston ontologia

Liitännäisiä on kaksi eri versiota ja niiden nimet ovat _finto_yso-kauno.pl_ ja _finto_yso-kauno_noind.pl_. Toinen versio lisää myöskin indikaattorin. Liitännäiset hakevat sekä YSOsta että KAUNOsta.


[YSO - Yleinen suomalainen ontologia](https://finto.fi/yso/fi/)

[KAUNO - fiktiivisen aineiston ontologia](https://finto.fi/kauno/fi/)

Liitännäiset noudattavat käyttöliittymän kielivalintaa eli kun Kohassa on käyttökielenä suomi, haetaan suomenkielisiä termejä. Kun taas käyttöliittymän kieli on ruotsi, haetaan termejä ruotsinkielisestä sanastosta.

Kun kenttään alkaa kirjoittamaan termiä, lähtee liitännäinen hakemaan sitä Fintosta ja ehdottaa hakua vastaavia termejä. Sulkeissa termin perässä lukee, kummasta sanastosta, ysosta vai kaunosta, termiä ehdotetaan.
![](/assets/files/docs/Ohjeet/finto9.png)

Kun listalta valitsee termin, tuodaan sen tiedot oikeisiin kenttiin. 0-kenttään lisätään linkki termiin ysossa ja 2-kenttään asiasanan/termin lähde.
![](/assets/files/docs/Ohjeet/finto10.png)

#### SLM - Suomalainen lajityyppi- ja muotosanasto

Liitännäinen on 655$a-kentässä ja nimeltään _finto_slm-local.pl_.

[SLM - Suomalainen lajityyppi- ja muotosanasto](https://finto.fi/slm/fi/)

Kun 655-kenttään alkaa kirjoittamaan termiä, lähtee liitännäinen hakemaan sitä SLM-termeistä ja ehdottaa vastaavia termejä.
![](/assets/files/docs/Ohjeet/finto11.png)

Kun listalta valitsee termin, tuodaan sen tiedot oikeisiin kenttiin. 0-kenttään lisätään linkki termiin SLM-sanastossa ja 2-kenttään termin lähde.
![](/assets/files/docs/Ohjeet/finto12.png)

Kun tämä pluginin on käytössä, pystyy kirjoittamaan myös ns. paikallisia termejä. Tällöin 655$a-kenttään kirjoitetaan haluttu sana ja 2-kenttään tulee termin lähteeksi "local" sekä 2. indikaattoriksi '7'. **HUOM!** Tällä hetkellä pitää ensin painaa a-kentän viereistä editoria, jotta oman termin lisääminen onnistuu.

![](/assets/files/docs/Ohjeet/finto13.png)

#### YSO-aika

Liitännäisiä on kaksi ja ne ovat nimeltään _finto_yso-aika.pl_ ja _finto_yso-aika_noind.pl_. Ne toimivat muuten samoin, mutta toinen lisää myös indikaattorin.
[YSO-aika](https://finto.fi/yso-aika/fi/index)

finto_yso-aika.pl kentässä 388$a
![](/assets/files/docs/Ohjeet/finto15.png)

finto_yso-aika_noind.pl kentässä 648$a
![](/assets/files/docs/Ohjeet/finto14.png)



#### YSO-paikat

Liitännäisiä on kaksi ja ovat nimeltäään _finto_ysopaikat.pl_ ja _finto_ysopaikat_noind.pl_. Ne toimivat muuten samoin, mutta toinen lisää myös indikaattorin.
[YSO-paikat](https://finto.fi/yso-paikat/fi/)


finto_ysopaikat.pl kentässä 651$a
![](/assets/files/docs/Ohjeet/finto16.png)


#### Asteri

Asteri-tietokantaan liitetty liitännäinen on nimeltään _finto_finaf.pl_. Sen tarkempi kuvaus ja käyttöönotto-ohjeet löytyvät [Asteri-sivulta](https://koha-suomi.fi/dokumentaatio/asteri/).

#### SEKO - Suomalainen esityskokoonpanosanasto

YSO/Seko-liitännäinen _finto_seko_nouri_noind.pl_ ei ole vielä varsinaisesti käytössä, mutta se on tehty valmiiksi sitä varten, että se otetaan käyttöön jossain vaiheessa.

[SEKO - Suomalainen esityskokoonpanosanasto](https://finto.fi/seko/fi/)

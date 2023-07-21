

## Finto-plugin

Luetteloinnissa voidaan käyttää liitännäisiä, jotka hakevat tiedot Finton sanastoista. Kun liitännäinen on lisätty kenttään, luetteloija voi kirjoittaa kyseiseen kenttään hakutermin, jolla sanastosta haetaan, ja valita sopivan arvon suoraan valikosta. Osakenttään tulee siis valittu arvo, osakenttään 0 tulee lähde-URI, ja osakenttään 2 tulee lähteen nimi, esim. "yso/fin"

Finto-pluginien nimet alkavat "finto_", jonka jälkeen on sanasto, josta plugin hakee tiedot (esim. "seko", "yso"). Jos nimessä on "local", sallii plugin myös paikallisen arvon lisäämisen, ja jos pluginin nimi päättyy "_ind", asettaa se myös kentän toisen indikaattorin arvoksi "7".

Finto-pluginit ovat käytössä Täti-tietokannassa.

### Pluginin määrittäminen käyttöön

Kannattaa tehdä ainakin nämä määritykset alkuunsa:

MARC-kenttä|Kentän kuvaus|Liitännäinen
---|---|---
257$a|Tuottajan maa|finto_ysopaikat.pl
370$g|Teoksen tai ekspression luontipaikka|finto_ysopaikat.pl
650$a|Aihetta ilmaiseva termi tai maantieteellinen nimi|finto_yso-kauno_ind.pl
651$a|Maantieteellinen nimi|finto_ysopaikat-local_ind.pl
655$a|Lajityyppiä/muotoa kuvaava temi tai fokustermi|finto_slm-local_ind.pl

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


### Pluginin toiminta luetteloinnissa

Plugineja on useamman tyyppisiä ja ne toimivat pääsääntöisesti samalla periaatteella. Osassa voi kuitenkin käyttää myös "paikallisia" termejä, jolloin liitännäinen toimii vähän eri tavalla.

#### YSO/Kauno

Plugin noudattaa käyttöliittymän kielivalintaa eli kun Kohassa on käyttökielenä suomi, haetaan suomenkielisiä termejä. Kun taas käyttöliittymän kieli on ruotsi, haetaan termejä ruotsinkielisestä sanastosta.

*Huom!* Järjestä kentät luettelointisääntöjen mukaiseen järjestykseen. Esimerkkikuvissa järjestystä ei ole muutettu.

Kun kenttään alkaa kirjoittamaan termiä, lähtee plugin hakemaan sitä Fintosta ja ehdottaa hakua vastaavia termejä. Sulkeissa termin perässä lukee, kummasta sanastosta, ysosta vai kaunosta, termiä ehdotetaan.
!fintoplug9.png!

Kun listalta valitsee termin, tuodaan sen tiedot oikeisiin kenttiin. 0-kenttään lisätään linkki termiin ysossa ja 2-kenttään asiasanan/termin lähde.
!fintoplug10.png!

#### SLM - Suomalainen lajityyppi- ja muotosanasto

Kun kenttää alkaa kirjoittamaan termiä, lähtee plugin hakemaan sitä SLM-termeistä ja ehdottaa vastaavia termejä.
!fintoplug11.png!

Kun listalta valitsee termin, tuodaan sen tiedot oikeisiin kenttiin. 0-kenttään lisätään linkki termiin SLM-sanastossa ja 2-kenttään termin lähde.
!fintoplug12.png!

Kun tämä pluginin on käytössä, pystyy kirjoittamaan myös ns. paikallisia termejä. Tällöin listalta valitaan itse kirjoitettu termi, jolloin se siirtyy oikeaan kenttään ja 2-kenttään tulee termin lähteeksi "local"
!fintoplug13.png!

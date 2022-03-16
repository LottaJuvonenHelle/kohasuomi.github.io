---
title: 'Kohan ohje suomeksi'
permalink: /dokumentaatio/lainaus/
redirect_from:
  - /theme-setup/
toc: true
---

# 2. Lainaus

Käytä lainaustoiminnoissa Firefox-selainta, jolla voit määrittää asiakaskuitit 
tulostumaan automaattisesti (ohje kohdassa 9. Kuittitulostuksen
asetukset). Koha-Suomi tukee Firefox ESR-versiota.

Lainauksen toimintoihin pääset useilla eri tavoilla. Virkailijaliittymän
etusivulla on pikakuvakkeita, joista pääset ohjelman eri toimintoihin,
mm. lainaus- ja palautustoimintoihin. Kaikista lainauksenvalvonnan
toiminnoista on listaus **Lainaus ja palautus** -sivulla, jonne pääset
jokaisen sivun vasemmasta yläreunasta olevasta linkistä.

![](/assets/files/docs/Lainaus/lainaus.png)

Ohjelman pikanäppäimet:

- tiedonhaku Alt+Q
- lainaus Alt+U
- palautus Alt+R
- lainakuitti Alt+P

## 2.1. Lainaaminen

Aloita lainaaminen lukemalla asiakkaan kirjastokortin viivakoodi
**Lainaus**-kenttään tai hakemalla asiakkaan tiedot hänen nimelläään.
Toimi kirjastosi käytäntöjen mukaan.

![](/assets/files/docs/Lainaus/lainaus_asiakastunnus.png)

Lue lainattavan niteen viivakoodi nidekenttään.

![](/assets/files/docs/Lainaus/lainaaminen.png)

Viimeksi lainatun niteen tiedot näkyvät **Lainattu**-kentässä.

**Tärkeää:**

- Monet viivakoodinlukijat lähettävät automaattisesti rivinvaihdon,
  joten **Lainaus**-painiketta ei tarvitse välttämättä klikata.
- Jos niteen viivakoodia ei löydy, saat ehdotuksen pikaluettelointiin
  niteen lisäämiseksi. Toiminto ei ole välttämättä kaikilla kimpoilla
  käytössä.

**Lainausasetukset**

- Asetuksissa on mahdollista määritellä lainattavalle aineistolle muu
  eräpäivä kuin oletuseräpäivä. Tämä vaihtoehto tulee näkyviin vain,
  jos järjestelmäasetuksissa on määritelty, että virkailijalla on
  oikeus muuttaa eräpäivää lainatessa.
- Jos kimpalla käytössä **automaattinen uusinta**, ohjelma uusii
  lainatut teokset automaattisesti lainasääntöjen mukaisesti.
- Toiminnolla **Älä lyhennä laina-aikaa varausten määrän pohjalta**
  voi ohittaa järjestelmäasetuksen, jolla lyhennetään laina-aikaa, jos
  teoksen varausmäärä menee asetuksissa määritellyn rajan yli. Valinta tulee näkyviin vain kimpoissa, jossa tämä järjestelmäasetus on päällä.

## 2.1.1 Kuittien tulostaminen

Kun olet lainannut kaikki asiakkaan lainat, voit tulostaa lainauskuitin
eri tavoilla. Toimi kimppasi käytäntöjen mukaan.

- Voit tulostaa kuitin lainauskentän oikeassa yläkulmassa näkyvästä tulostimen kuvasta.
- Voit tulostaa kuitin painamalla näppäimistöltä **Enter**. (Huom.
  järjestelmäasetuksista riippuen, Enter voi myös tyhjentää
  asiakastiedot).
- Voit tulostaa kuitin painamalla pikanäppäimiä **Alt+P**.
- Voit myös klikata asiakastietojen yläpuolelta auki
  **Tulosta**-valikon ja valita **Tänään lainatut**.

![](/assets/files/docs/Lainaus/tulostakuitti.png)

Tulosta -valikosta voit tulostaa myös:

- **Asiakastietojen yhteenveto:** A4-tuloste asiakastiedoista,
  lainoista, varauksista ja maksujen tilitystiedoista. Tätä ei
  suositella tulostettavan.
- **Tulosta kuitti:** tulostaa kaikki asiakkaan lainat kuitille.
  Tulosteessa erotellaan myöhässä olevat lainat oman otsikon alle.
- **Tänään lainatut:** tulostaa tänään lainattujen ja uusittujen
  lainojen tiedot kuitille.
- **Tulosta tänään palautetut:** antaa asiakkaan palautuksista kuitin.
- **Maksut:** tulostaa asiakkaan maksujen tilitiedot kuitille.

Kimpan pääkäyttäjät voivat muokata kuiteille tulostuvia tietoja.

## 2.1.2 Asiakastietojen tyhjennys näytöltä

Kun lopetat lainaamisen, näytöltä pitää tyhjeentää asiakkaan tiedot.
Näytön voit tyhjentää kahdella tavalla:

- painamalla **Enter**. (Huom! asetuksista riippuen, Enter voi myös
  tulostaa asiakkaan lainakuitin).
- klikkaamalla **X** lainauskentän oikeasta yläkulmasta.

![](/assets/files/docs/Lainaus/tyhjennys.png)

---

## 2.2 Lainausviestit

### 2.2.1 Huomautus liitteistä

Jos lainaat niteen, joka sisältää useita osia ja tieto osista on
tallennettu niteen tietoihin kenttään 3 (Liitteiden määrä), saat
ponnahdusikkunan, jossa kerrotaan montako osaa nide sisältää.

![](/assets/files/docs/Lainaus/huomsisallosta.png)

## 2.3 Lainaamisen estot

Joissakin tilanteissa Koha estää lainaamasta aineistoa asiakkaalle, jos
järjestelmäasetuksissa estot ovat laitettu päälle. Näissä tilanteissa
näytölle tulee huomautus lainaamisen eston syystä.

### 2.3.1 Asiakkaalla on liikaa maksuja

![](/assets/files/docs/Lainaus/liikaamaksuja.png)  
Hox! Uusintatilanteessa ohjelma ei ilmoita, jos sallittujen maksujen
raja on ylittynyt.

### 2.3.2 Asiakkaalla on rajoite (lainauskielto)

- Asiakas voidaan asettaa lainauskieltoon, kun palautuskehotus tai
  lasku on lähetetty.
- Jos lähetetään lasku esim. turmeltuneesta aineistosta, pitää
  manuaalisesti lisätä asiakkaan tietoihin rajoite. Rajoitteen voi
  lisätä asiakastietojen muokkauksessa tai välilehdellä
  **Rajoitukset** -&gt; **Lisää rajoitus**. Lisää
  **Kommentti**-kenttään tieto rajoitteen syystä ja mahdollinen
  vanhenemispäivämäärä. Tallenna.  
  ![](/assets/files/docs/Lainaus/rajoite1.png)

### 2.3.3 Asiakkaan osoitetiedot ovat väärät

Jos asiakkan tiedoissa on päällä asetus, että osoite on tarkistettava,
lainaus estyy.  
![](/assets/files/docs/Lainaus/vaaraosoite1.png)

Lainaustilanteessa tulee huomautus:  
![](/assets/files/docs/Lainaus/tarkistaosoite.png)

Huomautuksen voi poistaa, kun osoitetiedot on korjattu ja vaihtaa asiakkaan muokkausnäytöllä täpän
**Käyttäjätilin huomautukset** -kohdassa **Tarkista osoite** -kohtaan
“Ei”.

### 2.3.4 Asiakas on kadottanut kirjastokorttinsa

Asiakasrekisteriin on merkitty huomautus kadonneesta kirjastokortista.  
![](/assets/files/docs/Lainaus/kadonnutkortti.png)

Lainaustilanteessa tulee huomautus:  
![](/assets/files/docs/Lainaus/korttikadonnut.png)

Kun asiakkaan kirjastokortti on kadonnut, toimi kimpassa sovittujen
käytäntöjen mukaan.  
Huomautuksen voi poistaa asiakkaan tiedoissa vaihtamalla täppä
**Käyttäjätilin huomautukset** -kohdassa **Kortti kadonnut** -kohtaan
“Ei”.

### 2.3.5 Asiakkaalle on laitettu rajoite (lainauskielto)

Asiakkaille voit laittaa rajoitteita, jotka aiheuttavat lainaukiellon.
Rajoitteet voivat olla voimassa toistaiseksi tai määräajan. Rajoitteen
voit lisätä muokkaamalla asiakastiedoissa kohtaa **Asiakkaan
rajoitukset** tai välilehdellä **Rajoitukset**. Jos rajoite halutaan
olemaan voimassa vain tietyn ajan, laita **Vanhenee**-kohtaan viimeinen
voimassaolopäivä.

Toistaiseksi voimassa oleva rajoite:

![](/assets/files/docs/Lainaus/rajoite1.png)

Määräajan voimassa oleva rajoite:

![](/assets/files/docs/Lainaus/rajoite2.png)

## 2.4 Lainaushuomautukset

Joskus lainaustilanteessa näytölle voi tulla keltaisessa laatikossa
oleva huomautus. Nämä huomautukset on käsiteltävä/huomioitava ennen
lainaamisen jatkamista.

### Aineisto on varattu jollekin toiselle asiakkaalle. Varausta ei ole vielä otettu kiinni.

<img src="/assets/files/docs/Lainaus/lainhuom1.png" alt="" style="width:70.0%" />

### Nide on varaushyllyssä varattuna toiselle asiakkaalle.

![](/assets/files/docs/Lainaus/lainhuom2.png)

- Jos esimerkiksi toinen perheenjäsen haluaa lainata varatun
  aineiston, valitse **Poista varaus** ja klikkaa **Kyllä, lainaa
  (Y).** Varaus poistuu alkuperäiseltä varaajalta.

### Nide on jo lainassa tällä asiakkaalla.

![](/assets/files/docs/Lainaus/lainhuom3.png)

### Aineisto on lainassa toisella asiakkaalla.

![](/assets/files/docs/Lainaus/lainhuom4.png)

### Aineistoa ei lainata (niteen tila on “Ei lainattavissa”).

![](/assets/files/docs/Lainaus/lainhuom5.png)

### Asiakkaalla on liian monta lainaa.

![](/assets/files/docs/Lainaus/lainhuom6.png)

### Viivakoodia ei löytynyt.

![](/assets/files/docs/Lainaus/lainhuom7.png)

- Kohassa on mahdollista käyttää pikaluettelointia, jos se on sallittu
  järjestelmäasetuksissa.

### Lainattava nide on merkitty kadonneeksi.

![](/assets/files/docs/Lainaus/lainhuom8.png)

- Lainausasetusten määrittelystä riippuu, tuleeko huomautusta.

### Lainattavalla niteellä on ikärajoitus, ja asiakas on liian nuori.

![](/assets/files/docs/Lainaus/lainhuom9.png)

### Lainattavalla niteellä on paljon varauksia, jonka takia lyhennetään laina-aikaa.

![](/assets/files/docs/Lainaus/lainhuom10.png)

- Huom! Asetus ei välttämättä ole päällä kimppasi Kohassa.




## **Lainat**

**Lainassa**-painikkeesta saat näkyville asiakkaan kaikki lainat.  
![](/assets/files/docs/Lainaus/lainassa.png)

Ensimmäisenä näkyvät tänään lainatut lainat.

![](/assets/files/docs/Lainaus/lainat_naytto.png)

**Sarakkeen näkyvyys** -valikosta voit valita, mitä sarakkeita
Lainassa-välilehdellä näytetään.

![](/assets/files/docs/Lainaus/sarakkeen_nakyvyys.png)

## Varaukset

**Varaukset**-välilehdellä näkyvät asiakkaan varaukset ja missä tilassa varaukset ovat. Välilehdellä
voit poistaa varauksia, keskeyttää ja jatkaa varausten voimassaoloaikaa
käyttämällä varausten alapuolella olevia toimintopainikkeita, mikäli ne
ovat sallittu järjestelmäasetuksissa. 

![](/assets/files/docs/Lainaus/varaukset.png)

## Huomautukset

Jos asiakkaalle on tehty huomautuksia, ne näkyvät oikeassa reunassa
lainausosion vieressä punaisella.  
Huomautuksissa näkyvät myös maksut mikäli niitä on ja asiakkaan noutoa
odottavat varaukset.

![](/assets/files/docs/Lainaus/huomautukset.png)

## Vanhentunut asiakastieto

Jos asiakastiedot vaativat määräaikaistarkistuksen (parametreissä
määritelty), näyttöön tulee ilmoitus:

![](/assets/files/docs/Lainaus/vanhentunut.png)

Tarkista asiakkaan yhteystiedot (osoite, puhelin numero,
sähköpostiosoite, viestiasetukset). Jos tiedot ovat ajantasalla, klikkaa
**Uusinta**. Jos tiedot täytyy päivittää, muokkaa ja päivitä tiedot ensin linkistä **Muokkaa tietoja**.

Käyttöoikeuden voi jatkaa myös valikosta **Muita toimintoja**,
valitsemalla **Asiakkaan käyttöoikeuden jatkaminen**.

![](/assets/files/docs/Lainaus/vanhentunut2.png)








---

## 2.4 Uusinta

Lainassa olevien niteiden laina-ajan voi uusia sen mukaan, mitä
ylläpidon Laina- ja käyttömaksusäännöissä on määritelty.

Asiakkaat voivat uusia lainojaan verkkokirjastossa, mutta uusinnan voi
tehdä myös Kohan virkailijaliittymällä kirjastossa. Tämän voi tehdä
kahdella eri tavalla.

1. Asiakkaan tiedoissa olevalla Lainassa-välilehdellä.

![](/assets/files/docs/Lainaus/uusinta.png)

- Uusinta-sarakkeessa näet, kuinka monta kertaa kukin nide on uusittu
  ja uusinnan valintaruudun kunkin niteen kohdalla. Valitse uusittavat
  niteet ja klikkaa näytön alareunasta painiketta **Uusi tai palauta
  valitut niteet** tai jos uusit kaikki lainat, klikkaa **Uusi
  kaikki** -painiketta.
- Uusinta-sarakkeen yläreunassa olevalla toiminnolla “valitse kaikki”
  voit valita uusittavaksi kaikki lainat, jotka on mahdollista uusia.
  Toiminto “ei valintaa” poistaa valinnat.
- Jos Sarakkeen näkyvyys -valikosta on valittu Palautus-toiminto
  aktiiviseksi, voit palauttaa lainat valitsemalla palautettavat
  niteet **Palautus**-sarakkeesta ja klikkaamalla näytön alareunasta
  painiketta **Uusi tai palauta valitut niteet**.
- Jos kimpassa on käytössä asetus, joka estää uusimisen samana päivänä
  uudestaan, tulee huomautus “Ei uusintaa ennen…”. Lainan voi uusia
  uudelleen kyseisen päivämäärän ja kellonajan jälkeen. Huomautus
  tulee, kun päivittää Lainassa-välilehden tai käy välillä toisella
  sivulla.  
  ![](/assets/files/docs/Lainaus/uusinta6.png)

2. Uusinta Lainaus ja palautus -sivun Uusinta-linkistä.

- Huomio kirjastosi käyttösäännöt. Joissain kirjastoissa uusittaessa
  pitää olla kirjastokortti mukana eli tätä toimintoa ei saa silloin
  käyttää, mikäli käyttösäännöt edellyttävät kirjastokorttia
  uusintatilanteessa.

![](/assets/files/docs/Lainaus/uusinta1.png)

Uusi lainat lukemalla niteen viivakoodi uusintakentään.

![](/assets/files/docs/Lainaus/uusinta2.png)

Jos niteen uusiminen onnistuu, saat ilmoituksen.

![](/assets/files/docs/Lainaus/uusinta3.png)

Jos nide ei ole lainassa, saat ilmoituksen.

![](/assets/files/docs/Lainaus/uusinta5.png)

Jos viivakoodia ei löydy, saat ilmoituksen.

![](/assets/files/docs/Lainaus/uusinta4.png)

---

## 2.5 Palauttaminen

Aineiston palauttamiseen pääset eri näyttöjen kautta.

![](/assets/files/docs/Lainaus/palautus.png)

Kaikista lainaustenvalvonnan toiminnoista on listaus **Lainaus ja
palautus** -sivulla, jonne pääset jokaisen sivun vasemmasta yläreunasta
olevasta linkistä.

### Aineiston palauttaminen

Kun palautat aineistoa, lue niteen viivakoodi palautuskenttään.
Palautetun niteen tiedot tulevat näytölle.

![](/assets/files/docs/Lainaus/palautus1.png)

---

## 2.5.1 Palautuksen viestit

### Toisen kirjaston aineisto

Jos olet palauttamassa jonkun muun kirjaston aineistoa, saat viestin,
jossa ilmoitetaan mihin kirjastoon nide pitää kuljettaa.

![](/assets/files/docs/Lainaus/palautusviesti1.png)

- Tämän jälkeen niteen tilaksi muuttuu _Kuljetettavana_.  
  ![](/assets/files/docs/Lainaus/palautusviesti2.png)

<!-- -->

- Nide pitää palauttaa kotikirjastossaan, jotta sen tilaksi muuttuu
  Saatavana.

### Useita osia sisältävä nide

Jos palautat niteen, joka sisältää useita osia ja tieto osista on
tallennettu niteen tietoihin kenttään 3 (Liitteiden määrä), saat
ponnahdusikkunan, jossa kerrotaan montako osaa nide sisältää.  
![](/assets/files/docs/Lainaus/huomsisallosta.png)

### Varatun niteen palautus

Jos palautat niteen, josta on varaus, saat siitä ilmoituksen.  
![](/assets/files/docs/Lainaus/palautusviesti3.png)

- Valitsemalla toiminnon **Vahvista varaus**, nide menee
  Odottaa-tilaan.
- Toiminnolla **Tulosta kuitti ja vahvista**, ohjelma tulostaa
  varauksen Infokuitin ja muuttaa niteen Odottaa-tilaan.
- Toiminnolla **Älä huomioi**, niteen tilaksi jää saatavana ja varaus
  säilyy asiakkaalla voimassa olevana.

![](/assets/files/docs/Lainaus/palautusviesti4.png)

### Varaus toisessa kirjastossa

Jos palautat niteen, josta on varaus jossain toisessa kirjastossa, saat
ilmoituksen ja tiedon, mihin kirjastoon nide pitää kuljettaa.

![](/assets/files/docs/Lainaus/palautusviesti5.png)

- Valitsemalla **Vahvista varaus ja kuljetus**, merkitset niteen
  kuljetettavaksi siihen kirjastoon, missä on varatun aineiston
  noutopaikka.
- Toiminnolla **Tulosta kuitti, kuljeta ja vahvista**, tulostaa
  ohjelma varauksen kuljetuskuitin ja merkitsee niteen kuljetettavaksi
  siihen kirjastoon, missä on varatun aineiston noutopaikka.
- Toiminnolla **Älä huomioi**, niteen tilaksi jää saatavana ja varaus
  säilyy asiakkaalla voimassa olevana.

![](/assets/files/docs/Lainaus/palautusviesti6.png)

### Asiakkaan maksut

Jos järjestelmä on asetettu näyttämään maksut palautuksen yhteydessä,
saat keltapohjaisen viestin asiakkaan maksuista.  
![](/assets/files/docs/Lainaus/palautusviesti7.png)

### Kadonneeksi merkityt niteet

Jos palautat kadonneeksi merkityn niteen, saat seuraavan ilmoituksen:  
![](/assets/files/docs/Lainaus/palautusviesti8.png)

---

## 2.6 Lainausnäytön huomautukset

Lainausnäytölle voi tallentaa lyhyitä viestejä, jotka näkyvät lainatessa
asiakkaalle.

### Viestien lisääminen asiakkaalle

Lainauskentän oikealla puolella on huomautuksia, joista alimmaisena on
**Viestit**. Valitsemalla **Lisää uusi viesti**, voit lisätä asiakkaalle
uuden viestin.

![](/assets/files/docs/Lainaus/lainausviesti1.png)

Kun valitset **Lisää uusi viest**, pääset valitsemaan, näytetäänkö
viesti vain virkailijoille vai myös asiakkaalle asiakasliittymässä
(valikossa asiakkaan nimi).

![](/assets/files/docs/Lainaus/lainausviesti2.png)

Voit valita viestin esimääritellyistä viesteistä tai kirjoittaa oman
viestin. Kimpan pääkäyttäjät voivat lisätä esimääriteltyjä viestejä.

![](/assets/files/docs/Lainaus/lainausviesti3.png)

- HUOMIO! Viesti asiakkaalle näkyy myös virkailijoille.

### Viestin näkyminen

Viesti näkyy asiakkaalle ja/tai virkailijalle lainausnäytön oikeassa
reunassa. Lihavoidut, punaiset viestit näkyvät vain virkailijoille,
kursiivilla näkyvät viestit sekä asiakkaalle että virkailijoille.

![](/assets/files/docs/Lainaus/lainausviesti4.png)

Viestin näkyminen Kohan asiakasliittymässä:

![](/assets/files/docs/Lainaus/lainausviesti5.png)

---

## 2.7 Varaukset

Asiakas voi varata aineistoa Kohassa. Lainaus- ja käyttömaksusäännöissä
ja asiakastyyppien ylläpidossa on määritelty säännöt, minkä mukaan
varauksia voi tehdä.

### Varauksen teko tiedonhaun kautta

Varauksen voi tehdä usealla tavalla. Yksinkertaisin tapa on tehdä varaus
nimeketietojen näytön yläreunasta _Varaa_-napista.

![](/assets/files/docs/Lainaus/varaus1.png)

Varauksen voi tehdä myös hakutuloslistauksessa:

- näytön yläreunassa _Varaa_-napista, kun on valinnut näytöltä
  varattavat nimekkeet
- nimeketietojen jäljessä olevasta _Varauksia_-linkistä.

![](/assets/files/docs/Lainaus/varaus2.png)

Kun teet varauksen, täytyy asiakkaan tiedot hakea näytölle joko kortin
viivakoodilla tai asiakkaan nimellä hakemalla. Huom! Noudata kirjastosi
sovittuja käytäntöjä.

![](/assets/files/docs/Lainaus/varaus3.png)

### Varauksen teko asiakastietojen kautta

Voit tehdä varauksen myös asiakastiedoista päin. Klikkaa _Hae ja varaa_
-nappia…

![](/assets/files/docs/Lainaus/varaus4.png)

…hae tarvittava nimeke ja tee varaus.

![](/assets/files/docs/Lainaus/varaus5.png)

Kun olet valinnut asiakkaan, jolle varaus tehdään, voi varauksen tietoja
tarkentaa:

- _Muuta_-laatikkkoon voit kirjoittaa varaukseen liittyviä lisätietoja
  tarvittaessa.
- Valitse _Noutopaikkaan_ kirjasto, mistä asiakas noutaa aineiston.
- Jos varaus halutaan alkamaan tulevaisuudessa, anna _Varauksen
  alkamispvm_ -laatikkoon aloituspäivämäärä. Muuten siihen tallentuu
  kuluva päivä.
- Jos varaus halutaan olemaan voimassa vain tiettyyn päivämäärään
  saakka, merkitse päiväys _Varaus vanhenee_ -laatikkoon.
- Oletuksena on _Varaa seuraava vapaa nide_. Jos haluat tietyn niteen
  varaukseen, valitse nide listalta _Varaus_-sarakkeesta.
- Varausten määrän voit valita _Tee varauksia (määrä)_ -sarakkeesta.

![](/assets/files/docs/Lainaus/varaus6.png)

### Useampi varaus kerralla

Jos haluat tehdä varauksen useammasta nimekkeestä kerralla, valitse
nimekkeiden vasemmalta puolelta valintaruudusta halutut nimekkeet ja
klikkaa _Varaa_-nappia.

![](/assets/files/docs/Lainaus/varaus7.png)

Varaussivulle listautuu valitut teokset. Valitse noutopaikka ja klikkaa
_Varaa_.

![](/assets/files/docs/Lainaus/varaus8.png)

---

## 2.8 Varausten käsittely

Varauksia voi muuttaa ja peruuttaa _Varaukset_-välilehdellä, jonne
pääsee nimeketietueen vasemmalla olevasta valikosta. Myös asiakkaan
varauksista käsin pääsee varauksiin klikkaamalla
_Varaukset_-välilehdellä teoksen nimeä.

![](/assets/files/docs/Lainaus/varaus13.png) tai ![](/assets/files/docs/Lainaus/varaus22.png)

Varauslistalla voit muuttaa varausten järjestystä, noutopaikkaa tai
keskeyttää tai peruuttaa varauksen.

![](/assets/files/docs/Lainaus/teevaraus.png)

### Varausten järjestyksen muuttaminen

Jos jostain syystä täytyy varausjonon järjestystä muuttaa (ei saa tehdä
ilman erityistä syytä), se tapahtuu muuttamalla Järjestys jonossa
-sarakkeessa olevia numeroarvoja. Tai klikkailemalla vihreitä nuolia.
Huom! Tätä oikeutta ei välttämäti ole kaikilla työntekijöillä.

![](/assets/files/docs/Lainaus/varaus15.png)

- Jos muutat järjestystä jonossa tai poistat varauksen, muista klikata
  _Päivitä varaukset_ -nappia tallentaaksesi toiminnot.

### Varauksen kiinnittäminen viimeiseksi jonossa

Jos klikkaat varauksen oikealla puolella olevaa vihreää nuolta, varaus
menee viimeiseksi listalle ja pysyy viimeisenä, vaikka uusia varauksia
tulisi sen jälkeen. Tämä toiminto voi olla tarpeellinen esim.
kotipalveluasiakkaiden kohdalla, joilla niteiden laina-aika voi venyä
pidemmäksi kuin muilla asiakkailla.

![](/assets/files/docs/Lainaus/varausalas.png)

Kun varauksen kohdalla näkyy vihreä nuoli, jonka alla on viiva, se
tarkoittaa, että varaus pysyy alimmaisena jonossa.

![](/assets/files/docs/Lainaus/varaus17.png)

### Yksittäisen varauksen keskeyttäminen

Jos asiakas haluaa keskeyttää yksittäisen varauksensa tietyksi ajaksi,
sen voi tehdä valitsemalla kalenterikuvakkeesta päivämäärän, mihin asti
varaus on keskeytettynä ja klikkaamalla Keskeytä-nappia.

![](/assets/files/docs/Lainaus/varauksenkes.png)

Kun varaus on keskeytetty, varauksen kohdalle tulee _Jatka_-nappi ja
näkyy päivämäärä, mihin saakka keskeytys on voimassa. Voit palauttaa
varauksen voimaan myös (tyhjentämällä päivämäärän ja) klikkaamalla
Jatka.

![](/assets/files/docs/Lainaus/keskeytyksenjatk.png)

### Asiakkaan kaikkien varauksien keskeyttäminen

Jos asiakas haluaa keskeyttää kaikki varauksensa, voi sen tehdä
asiakkaan tiedoissa _Varaukset_-välilehdellä klikkaamalla _Keskeytä
kaikki varaukset_ -nappia. Vastaavasti varaukset saa taas voimaan
klikkaamalla _Jatka kaikkia keskeytettyjä varauksia_ -nappia.

![](/assets/files/docs/Lainaus/varaus23.png)

### Varauksen poistaminen

Varauksen poistaminen onnistuu yksitellen klikkaamalla varauksen
kohdalla punaista ruksia.

![](/assets/files/docs/Lainaus/varauksenpoisto1.png)

Varauksen voi myös poistaa asiakkaan tiedoissa _Varaukset_-välilehdellä
valitsemalla Poista?-sarakkeeseen “Kyllä” ja klikkaamalla _Peruuta
valitut varaukset_ -nappia.

![](/assets/files/docs/Lainaus/varauksenpoistoA.png)

Useita varauksia kerralla voit poistaa merkitsemällä kunkin varauksen
alasvetovalikosta poistettavaksi ja klikkaamalla lopuksi _Päivitä
varaukset_.

![](/assets/files/docs/Lainaus/varauksenpoisto.png)

---

## 2.9 Varausten kiinnijääminen

Varaus voi jäädä kiinni joko virkailijaliittymässä palautettaessa tai
palautusautomaatilla palautettaessa.

### 2.9.1 Varaus palautetaan virkailijaliittymässä

Kun palautetaan varattuja niteitä, tulee varauksesta ilmoitus.

Kun varauksen noutokirjasto on **sama** kuin mihin nide on palautettu:  
![](/assets/files/docs/Lainaus/varauksenkiinitys1.png)  
Kun varaus hyväksytään, asiakkaalle **lähtee noutoilmoitus**.

Kun varauksen noutokirjasto on **eri** kuin mihin nide on palautettu:  
![](/assets/files/docs/Lainaus/varauksenkiinitys2.png)  
Tässä tapauksessa nide menee kuljetustilaan, eikä asiakkaalle lähde
vielä noutoilmoitusta. Ilmoitus lähtee vasta, kun nide palautetaan
noutokirjastossa.

**Huomaa:** Molemmissa tapauksissa varaus vahvistetaan tai tulostetaan
kuitti ja hyväksytään varauksen kiinnijääminen. _Älä huomioi_ jättää
varauksen voimaan asiakkaalle, mutta sallii lainaamisen toiselle
asiakkaalle (ohjelma huomauttaa varauksesta).

### 2.9.2 Varaus palautetaan automaattiin

Jos kimpassa on käytössä varatun aineiston noutoilmoitusten
viivästäminen automaattipalautuksille, menevät kaikki automaatilla
palautetut varatut niteet kuljetustilaan. Myös noutopisteeseen
palautuneet jäävät odottamaan “kuljetusta” uudelleenkäsittelyyn.
Käytännössä kaikki automaattiin palautetut varaukset pitää siis
palauttaa noutopisteessä uudelleen virkailijaliittymässä, vasta siinä
vaiheessa noutoilmoitus lähtee asiakkaalle.

Jos viivästys ei ole käytössä, lähtee noutoilmoitus asiakkaalle heti,
kun aineisto palautetaan automaattiin.

### 2.9.3 Varausten näkyminen asiakkaan tiedoissa

Asiakkaan tiedoissa näkyy _Varaukset_-välilehdellä, minne varattu nide
on palautettu ja milloin.

**Virkailijaliittymässä palautettu varaus:**  
![](/assets/files/docs/Lainaus/viivastys3.png)

1.  Kuljetettavana noutokirjastoon
2.  Odottaa noutopisteessä

**Automaattiin palautettu:**

Jos noutoilmoitusten viivästäminen automaattipalautuksissa ei ole
käytössä, näkyy varaus samalla tavalla kuin yllä olevassa tapauksessa.

Jos käytössä on noutoilmoitusten viivästäminen, näkyy varaus näin:

![](/assets/files/docs/Lainaus/viivastys.png)

### 2.9.4 Kiinni jääneiden varausten näkyminen kokoelmatiedoissa ja varausjonossa

**Kokoelmat**-välilehdellä nidetiedoissa näkyy varatun ja kuljetuksessa
olevan niteen tilanne.  
![](/assets/files/docs/Lainaus/viivastys5.png)

1.  Automaatilla palautettu, noutoilmoitusta ei vielä lähetetty. Varaus
    näkyy nidevarauksena.
2.  Noudettavissa oleva, noutoilmoitus lähetetty

**Varausjono**-sivulla kiinni jäänyt varaus voi olla kolmessa eri
tilassa:  
![](/assets/files/docs/Lainaus/viivastys4.png)

1.  _Ylimmäisenä:_ automaatilla palautettu, kiinni jäänyt varaus,
    noutoilmoitusta ei vielä lähetetty. Priority-sarakkeessa varaus on
    In transit/Kuljetettavana-tilassa.
2.  _Keskimmäisenä:_ noudettavissa oleva, noutoilmoitus lähetetty.
    Priority-sarakkeessa tietona Waiting/Odottaa
3.  _Alimmaisen:_ Kuljetettavana oleva varaus.

---

## Varauksen noutaa muu kuin varaaja itse

Jos varauksen noutaa joku muu kuin varaaja itse (perheenjäsen tai muu
valtuutettu), saat huomautuksen, josta pitää ensin valita Peruuta varaus
(poistaa varauksen varaajan tiedoista) ja sitten Kyllä, lainaa (Y).

![](/assets/files/docs/Lainaus/varaus28.jpg)

---

## 2.10 Siirto-toiminto

Kirjastokimpassa voit siirtää niteitä toiseen kirjastoon käyttämällä
**Siirto**-työkalua.

- Valitse: Lainaus ja palautus -&gt; **Siirto**

![](/assets/files/docs/Lainaus/siirto1.png)  
Valitse alasvetovalikosta kirjasto, johon olet siirtämässä aineistoa ja
lue siirrettävän niteen viivakoodi _Syötä viivakoodi_ -kohtaan. Paina
lopuksi **OK**.

![](/assets/files/docs/Lainaus/siirto2.png)  
Nyt niteeseen tulee palautuksessa tieto määränpäästä..

![](/assets/files/docs/Lainaus/siirto3.png)  
ja niteen tilaksi kuljetuksessa.

![](/assets/files/docs/Lainaus/siirto4.png)

Kun nide saapuu kohteeseen, se on siellä palautettava, jotta nide ei ole
enää kuljetuksessa.

Nidettä ei ole pysyvästi siirretty kohdekirjastoon. Niteen kotikirjasto
ei muutu, mutta nykyinen paikka on toinen kirjasto.

![](/assets/files/docs/Lainaus/siirto5.png)

---

## 2.11 Kirjaston valinta

Oletuksena on, että kirjaudut virkailijatyökaluun kotikirjastossasi.
Kirjaston nimi näkyy virkailijatyökaluikkunan oikeassa yläreunassa.
**Tärkeää:** Lainat ja palautukset rekisteröityvät tunnukselle valitun
kirjaston mukaan.

![](/assets/files/docs/Lainaus/valinta1.png)

Jos työskentelet useammassa kirjastossa, pääset valitsemaan kirjaston
_Aseta kirjasto_ -napista. Valitse kirjasto alasvetovalikosta ja klikkaa
OK.

![](/assets/files/docs/Lainaus/valinta3.png)  
Valitsemasi kirjasto tulee näkyviin oikeaan yläkulmaan ja toiminnot
tapahtuvat valitsemassasi kirjastossa (lainat, palautukset jne.)

## 2.12 Pikaluettelointi (ei käytössä)

[Koha Manual - Fast Add
Cataloging](http://manual.koha-community.org/3.16/en/fastaddcat.html)

---

## 2.13 Lainauksen raportit

Useimmat raportit saadaan Raportit-moduulin kautta, mutta joitakin
raportteja löytyy myös Lainauksen toiminnoista.

Mene: _Lainaus ja palautus_ -&gt; _Lainausraportit_.

![](/assets/files/docs/Lainaus/raportti1.png)

### Varausjono

Tämä raportti näyttää kaikki varaukset kirjastossasi.

![](/assets/files/docs/Lainaus/raportti2.png)

### Hyllyvaraukset

**Huomioi:** Koha-Suomi on tehnyt oman versionsa hyllyvarauslistasta. Se
on kuvattu [wikin
Raportit-osiossa](https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/7_Raportit#722-Hyllyvaraukset)

Tämä listaus näyttää kaikki nimekkeet, joista on varauksia ja joilla on
niteitä saatavana. Ensin kannattaa tarkistaa ne varaukset, joissa
noutokirjastona on oma kirjasto/oman kunnan toinen kirjasto.
Noutokirjaston näkee viimeisestä sarakkeesta “Varauspvm ja noutopaikka”.

![](/assets/files/docs/Lainaus/raportti4.png)

Voit rajata hakua _Tarkenna tuloksia_ -valikosta vasemmalla.
Oletusarvona alkupäivämääränä on 365 vrk ennen kuluvaa päivää, mutta
päivämäärän voi muuttaa ennen hakua.

![](/assets/files/docs/Lainaus/raportti5.png)

Voit suodattaa hakutuloksesta _Kirjastot_-sarakkeen alla olevasta
valikosta oman kirjastosi aineistot esille. Jos valintaa ei ole tehty,
näkyvillä on _Ei mitään_.

![](/assets/files/docs/Lainaus/raportti6.png)

Näytön alareunassa näkyy, minkä verran aineistoa on suodatettu.

![](/assets/files/docs/Lainaus/lainrap6.png)

Voit muokata sarakkeiden näkyvyyttä..

![](/assets/files/docs/Lainaus/raportti7.png)

..ja lajitella hakutuloksia nuolimerkinnöistä.

![](/assets/files/docs/Lainaus/raportti8.png)

Hyllyvarauslistan voi tulostaa **ctrl+p** -näppäinyhdistelmällä.

### Noudettavissa olevat varaukset

Tämä raportti näyttää kaikki kirjastossasi noutoa odottavat niteet.

![](/assets/files/docs/Lainaus/nouto1.png)

Niteet, joiden noutoaika on mennyt umpeen, näkyvät _Vanhentuneet
varaukset_ -välilehdellä.

### Varauksia per nide

Tällä raportilla näet mm. varausten määrän yhtä nidettä kohti.

![](/assets/files/docs/Lainaus/pernide.png)

### Vastaanotettavat kuljetukset

Tässä raportissa näkyvät ne niteet, jotka Kohan mukaan on kuljetuksessa
kirjastoosi.

![](/assets/files/docs/Lainaus/kuljetus.png)

### Myöhässä

Koska tämä raportti vie paljon resursseja, sen määritykset annetaan
ennen raportin ajamista.

![](/assets/files/docs/Lainaus/raportti9.png)

### Myöhässä ja maksuja

![](/assets/files/docs/Lainaus/lainrap12.png)

---

## 2.14 Kirjaston sisäisen käytön seuranta

Ei vielä sisältöä.

---

## 2.15 Offline eli yhteydettömän tilan lainaus

Vaikka nettiyhteys ei toimisi, voit jatkaa lainaamista. Vaihtoehtoina on

1.  **Offline lainausohjelma Windowsille** (KOC). Erillinen ohjelma
    yksittäisille lainauskoneille. Tätä voi käyttää, kun ei ole yhteyttä
    internetiin. **Tämä on suositeltava vaihtoehto**
2.  **Koha Offline Circulation Tool** (KOCT), joka on selaimen lisäosa.
    Tätä voi käyttää esimerksi yllättävien verkkoyhteyskatkoksien
    aikana.
3.  **Yhteydettömän tilan lainaus**, jota voi käyttää, kun tietää
    ennakkoon, ettei yhteyttä ole. Esimerkiksi kirjastoautossa. **Ei
    suositella käytettäväksi**

### 2.15.1. Offline lainausohjelma Windowsille (KOC)

https://koha-community.org/manual/16.11/html/ch05s13.html  
tai  
http://manual.koha-community.org/3.8/en/offlinecirc.html  
Englanninkielinen asennettava ohjelma, jota ei ole käännetty suomeksi.

Ohjelman asennus- ja käyttöohjeohje PDF-muodossa: document\#36

![](/assets/files/docs/Lainaus/Offline_11.png)

Ennen kuin lainaus aloitetaan, voi tuoda .koc-tiedoston.
Asiakastiedoston tekevät kehittäjät, jotka toimittavat sen
tietoturvallisesti paikkaan, mistä käyttäjät saavat sen kopioitua omalle
koneelle. Tiedoston hyöty on siinä, että lainaustilanteessa näkyy
asiakkaan nimi, lainat sekä maksut. Tiedoston luomiseen menee tunteja,
joten äkillisissä tapauksissa tätä toimintoa ei voida käyttää.

**Huomaa:** Tietoturvan vuoksi ei ole kuitenkaan hyvä, että tehdään ns.
paikallisia kopioita asiakasrekisteristä. Ohjelmaa voi käyttää ilman
borrowers.db –tiedostoa.

Offline-ohjelmassa valitaan Database -&gt; Select Borrowers DB File.
Omalta koneelta valitaan tuotu .koc-tiedosto (useimmiten ladatut
tiedostot -kansiossa) ja klikataan Avaa.

![](/assets/files/docs/Lainaus/Offline_11_1.png)

Lainaaminen tehdään Issues-välilehdellä. Asiakkaan kirjastokortin numero
luetaan _Borrower Cardnumber_ -kenttään (tai tehdään haku
asiakastietoihin Search-laatikon kautta). Kun olet syöttänyt
kirjastokortin numeron, klikkaa \_Accept. Lainattavat teokset luetaan
_Item Barcode_ -kenttään ja Asiakkaan lainat näkyvät _Previously Scanned
Barcodes_ -ikkunassa. Eräpäivää ei voi tässä määritellä, mutta se
määrittyy automaattisesti aineistolle, kun lainaukset siirretään
pääjärjestelmään. Asiakkaalle voi antaa aineistolajin mukaisen
eräpäivälapun (kuittia ei pysty tulostamaan).

![](/assets/files/docs/Lainaus/Offline_12.png)

Kun asiakkaalle on lainattu kaikki aineisto, klikkaa _OK_ sivun
alareunassa. Päivän ensimmäisen lainaajan jälkeen saat ikkunan, jossa
valitset, millä nimellä ja mihin kansioon haluat tallentaa
offline-tiedostot. Kaikki loput asiakkaat ja lainat tallentuvat samaan
tiedostoon tai tiedostopaikkaan automaattisesti. Kannattaa käyttää aina
samaa kaavaa, sillä tiedosto pitää osata myös hakea kansiosta, kun
tiedot siirretään pääjärjestelmään. Esimerkissä on käytetty työpöytää
tallennuspaikkana ja oletustiedostonnimeä (koostuu päivämäärästä ja
kellonajasta: vvvv-kk-pp tunti-minuutti-sekunti-sekunninsadasosa).

![](/assets/files/docs/Lainaus/Offline_13.png)

_Returns_-välilehdellä voi tehdä palautuksia, mutta se ei ole
suositeltavaa varausten takia.

![](/assets/files/docs/Lainaus/Offline_14.png)

_History_~~välilehdellä näkyy kuluvan päivän lainaus~~ ja
palautustapahtumat.  
Type-sarakkeessa _issue_ tarkoittaa lainausta.

![](/assets/files/docs/Lainaus/Offlinehistory.png)

Kun nettiyhteys on jälleen käytettävissä, voit siirtää
offline-lainaukset pääjärjestelmään.  
Mene _Lainaus ja palautus_ -näyttöön ja valitse sieltä _Lähetä
yhteydettömän tilan lainaustiedosto (\*.koc)_.

![](/assets/files/docs/Lainaus/Offline_16.png)

Seuraavalla näytöllä etsi _Selaa_-napista tallennettu tiedosto.

![](/assets/files/docs/Lainaus/Offline_17.png)

Esimerkissä tiedosto tallennettiin työpöydälle. Kun olet valinnut
tiedoston, klikkaa _Avaa_-nappia ikkunan oikeassa alareunassa.

![](/assets/files/docs/Lainaus/Offline_18.png)

Tiedosto näkyy nyt valittuna. Klikkaa _Lähetä tiedosto_.

![](/assets/files/docs/Lainaus/Offline_19.png)

Kun lähetyksen tila on 100%, klikkaa _Lisää yhteydettömän tilan jonoon_.

![](/assets/files/docs/Lainaus/Offline_20.png)

Jos tiedostoja on useampia, tee kaikille sama toiminto klikkaamalla
Lähetä toinen KOC-tiedosto.  
Kun kaikki tiedostot on lähetetty, klikkaa _Näytä käsittelyä odottavat
yhteydettömän tilan tapahtumat_.

![](/assets/files/docs/Lainaus/Offline_21.png)

Seuraavalla näytöllä valitset kaikki rivit (jos siellä ei ole mitään
virheilmoituksia, ne rivit voit jättää vaikka valitsematta jos sellaisia
on) ja klikkaa _Käsittele_.

![](/assets/files/docs/Lainaus/Offline_22.png)

Kun saat alla olevan näytön, lähetys on onnistunut.

![](/assets/files/docs/Lainaus/Offline_23.png)

**Lopuksi**

Lopuksi **poista koneeltasi tiedostot täydellisesti**.

Etsi koneeltasi tiedosto, johon lainat tallennettiin.
Esimerkkitapauksessa Resurssin hallinta, Työpöytä. Klikkaa tiedosto(t)
aktiiviseksi ja paina sen jälkeen yhtä aikaa Shift + Del. Ohjelma kysyy
haluatko poistaa pysyvästi (lopullisesti). Vastaa kyllä.

Huom! Nämä tiedostot on poistettava kokonaan, koska Koha Offline
Circulation tallentaa kaikki lainat samaan paikkaan. Koha menee
sekaisin, jos useiden päivien lainat siirtyvät pääjärjestelmään yhä
uudelleen.

![](/assets/files/docs/Lainaus/Offline_24.png)

![](/assets/files/docs/Lainaus/Offline_25.png)

### 2.15.2 Koha Offline Circulation Tool (KOCT)

http://manual.koha-community.org/3.16/en/offlinecirc.html  
englanninkielinen lisäosa, jota ei ole käännetty suomeksi.

Ohje asennukseen ja käyttöön:

attachment:KOCTOffline-asennusjakäyttö.pdf

Lainausnäkymä:  
![](/assets/files/docs/Lainaus/KOCTLainausnäkymä.png)

### 2.15.3 Yhteydettömän tilan lainaus

**Tämä ei ole suositeltava tapa**

#### Etukäteen tehtävät toimet

Ennen yhteydettömän tilan lainausta täytyy työasemalle ladata
tiedostoja.

Mene: Lainaus ja palautus -&gt; Yhteydettömän tilan lainaus.

![](/assets/files/docs/Lainaus/Offline_1.png)

Synkronoi tiedostot jokaisella työasemalla klikkaamalla
Synkronoidaan-linkkiä.

![](/assets/files/docs/Lainaus/Offline_2.png)

Tämä antaa sinun ladata paikallisen kopion asiakkaista ja
lainaustiedoista. Klikkaa _Lataa tietueet_ sivun vasemmassa yläreunassa.
Kun tiedot on ladattu, näet niiden viimeisimmän päivitysajankohdan.

![](/assets/files/docs/Lainaus/Offline_3.png)

**Päivitys pitäisi tehdä säännöllisesti, jotta yhteyskatkon aikana olisi
mahdollisimman tuoreet tiedot käytettävissä.** Päivitys kestää pitkään.

#### Lainaaminen

Kun verkkoyhteys ei ole käytettävissä, mene Yhteydettömän tilan
lainaukseen Kohassa ja klikkaa _Lainaus_.

Lainaaminen aloitetaan lukemalla lainaajan kirjastokortti sivun yllä
olevaan laatikkooon. Jos näppäilet asiakastunnuksen, käytä isoja
kirjaimia. Asiakkaan tiedot, olemassaolevat lainat ja maksut tulevat
näytölle.

![](/assets/files/docs/Lainaus/Offline_4.png)

Lue lainattavan niteen viivakoodi ja anna eräpäivä. Jos et anna
eräpäivää, Koha muistuttaa asiasta.

![](/assets/files/docs/Lainaus/Offline_5.png)

Kun nide on lainattu, se ilmestyy asiakkaan tietoihin.

![](/assets/files/docs/Lainaus/Offline_6.png)

#### Kohan yhteydettömän tilan tietojen lataaminen

Kun nettiyhteys on taas käytettävissä, synkronoi yhteydettömän tilan
lainaukset (ja palautukset) klikkaamalla _Lähetystapahtumat_ (nuoli
ylöspäin) klikkaamalla _Odottavat yhteydettömän tilan toimet_. Linkin
yläpuolella voi lukea myös ettei ole odottavia tapahtumia, varmista
kuitenkin asia Odottavan yhteydettömän tilan toimet linkistä.

![](/assets/files/docs/Lainaus/Offline_7.png)  
![](/assets/files/docs/Lainaus/Offline_8.png)

Saat näytölle listan tapahtumista, jotka odottavat lataamista
tietokantaan.

![](/assets/files/docs/Lainaus/Offline_9.png)

Kun kaikista koneista on lähetetty yhteydettömän tilan lainaukset
tietokantaan, voit valita rastittamalla ne kaikki tai vain ne, jotka
haluat käsitellä Kohaan.

- Klikkaa _Käsittele_-nappia ja Koha tallentaa jokaisen toiminnon
  yksitellen. Jokaiselle toiminnolle (issue = lainaus, return =
  palautus) on oma rivinsä ja ilmoitus onnistuuko toiminnon
  tallentaminen Kohaan.

&gt;\* **Onnistui**, jos toiminto on tallennettu onnistuneesti  
&gt;\* **Asiakasta ei löytynyt**, jos asiakkaan kortin numero on
väärin  
&gt;\* **Nidettä ei löytynyt**, jos niteen viivaakoodi on väärin.  
&gt;\* **Nide ei ole lainassa**, jos palautit saatavilla olevan niteen.

Kun käsittely on valmis, saat yhteenvedon tapahtumista.

![](/assets/files/docs/Lainaus/Offline_10.png)

---

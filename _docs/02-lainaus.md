---
title: 'Kohan ohje suomeksi'
permalink: /dokumentaatio/lainaus/
redirect_from:
  - /theme-setup/
toc: true
---

# 2. Lainaus ja palautus

Käytä lainaustoiminnoissa Firefox-selainta, jolla voit määrittää asiakaskuitit 
tulostumaan automaattisesti (ohje kohdassa 9. Kuittitulostuksen
asetukset). Koha-Suomi suosittelee Firefox ESR-version käyttöä.

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

![](/assets/files/docs/Lainaus/lainaaminen.PNG)

- Viimeksi lainatun niteen tiedot näkyvät **Lainattu**-kentässä.
- Jos klikkaat täpän kohtaan **Näytä aina lainat reaaliaikaisesti**, lainaustilanteessa kaikki asiakkaan lainat näkyvät näytöllä. Tämä valinta voi olla piilotettuna kimpassasi.

**Tärkeää:**

- Monet viivakoodinlukijat lähettävät automaattisesti rivinvaihdon,
  joten **Lainaus**-painiketta ei tarvitse välttämättä klikata.
- Jos niteen viivakoodia ei löydy, saat ehdotuksen pikaluettelointiin
  niteen lisäämiseksi. Toiminto ei ole välttämättä kaikilla kimpoilla
  käytössä.

**Lainausasetukset**

![](/assets/files/docs/Lainaus/lainausasetukset.PNG)

- Asetuksissa on mahdollista määritellä lainattavalle aineistolle muu
  eräpäivä kuin oletuseräpäivä. Tämä vaihtoehto tulee näkyviin vain,
  jos järjestelmäasetuksissa on määritelty, että virkailijalla on
  oikeus muuttaa eräpäivää lainatessa.
- Jos kimpalla on käytössä **automaattinen uusinta**, ohjelma uusii
  lainatut teokset automaattisesti lainasääntöjen mukaisesti.
- Toiminnolla **Älä lyhennä laina-aikaa varausten määrän pohjalta**
  voi ohittaa järjestelmäasetuksen, jolla lyhennetään laina-aikaa, jos
  teoksen varausmäärä menee asetuksissa määritellyn rajan yli. Valinta tulee näkyviin vain kimpoissa, jossa tämä järjestelmäasetus on käytössä.

### 2.1.1 Kuittien tulostaminen

Kun olet lainannut kaikki asiakkaan lainat, voit tulostaa lainauskuitin
eri tavoilla. Toimi kimppasi käytäntöjen mukaan.

Kuitin voit tulostaa:
- Painamalla näppäimistöltä **Enter**. (Huom.
  järjestelmäasetuksista riippuen, Enter voi myös tyhjentää
  asiakastiedot).
- Painamalla pikanäppäimiä **Alt+P**.
- Asiakastietojen yläpuolelta olevasta **Tulosta**-valikosta valitsemalla **Tänään lainatut**.
  
**Huom!** Lainauskentän oikeassa yläkulmassa näkyvästä tulostimen kuvasta tulostuvat kaikki asiakkaalla lainassa olevat lainat kuitille.
![](/assets/files/docs/Lainaus/tulostin.PNG)

**Tulosta** -valikosta voit tulostaa myös kuitin:

![](/assets/files/docs/Lainaus/tulostakuitti.PNG)

- **Asiakastietojen yhteenveto:** A4-tuloste asiakastiedoista,
  lainoista, varauksista ja maksujen tilitystiedoista. Tätä ei
  suositella tulostettavan.
- **Tulosta kuitti:** tulostaa kaikki asiakkaan lainat kuitille.
  Tulosteessa erotellaan myöhässä olevat lainat oman otsikon alle.
- **Tänään lainatut:** tulostaa tänään lainattujen ja uusittujen
  lainojen tiedot kuitille.
- **Tulosta erääntyneet**: tulostaa erääntyneet lainat, jos asiakkaalla on myöhässä olevia lainoja.
- **Tulosta tänään palautetut:** antaa asiakkaan palautuksista kuitin.

Kimpan pääkäyttäjät voivat muokata kuiteille tulostuvia tietoja.

### 2.1.2 Asiakastietojen tyhjennys näytöltä

Kun lopetat lainaamisen, näytöltä on hyvä tyhjeentää asiakkaan tiedot.
Näytön voit tyhjentää kahdella tavalla:

- Painamalla **Enter**. (Huom! asetuksista riippuen, Enter voi tulostaa myös
  asiakkaan lainakuitin).
- Klikkaamalla **X-merkkiä** lainauskentän oikeasta yläkulmasta.

![](/assets/files/docs/Lainaus/tyhjennys.PNG)

---

## 2.2 Lainaamisen estot

Joissakin tilanteissa Koha estää lainaamasta aineistoa asiakkaalle, jos
estot ovat laitettu päälle järjestelmäasetuksissa. Näissä tilanteissa
näytölle tulee huomautus lainaamisen eston syystä.

### 2.2.1 Asiakkaalla on liikaa maksuja

![](/assets/files/docs/Lainaus/liikaamaksuja.png)  
Hox! Uusintatilanteessa ohjelma ei ilmoita, jos sallittujen maksujen
raja on ylittynyt.

### 2.2.2 Asiakkaalla on rajoitus (lainauskielto)

Asiakkaille voidaan tallentaa rajoitus, joka aiheuttaa lainauskiellon, esim. kun lasku on lähetetty.
Rajoitus voi olla voimassa toistaiseksi tai määräajan. 

Rajoituksen voit tallentaa asiakastietojen muokkausnäytöllä kohdassa **Asiakkaan
rajoitukset** tai välilehdellä **Rajoitukset**. Laita **Selitys**-kenttään rajoituksen syy ja jos rajoitus halutaan
olemaan voimassa vain tietyn ajan, laita **Vanhenee**-kohtaan viimeinen
voimassaolopäivä.

  ![](/assets/files/docs/Lainaus/rajoitteenlisäys.PNG)
  
  Tallenna rajoitus **Lisää rajoitus** -painikkeesta.  
  
  Asiakkaan Tiedot ja Lainaus -näytöillä rajoitus näkyy näin:
  
  ![](/assets/files/docs/Lainaus/rajoite1.PNG)

### 2.2.3 Asiakkaan osoitetiedot ovat väärät

Jos asiakkan tiedoissa on päällä asetus, että osoite on tarkistettava,
lainaus estyy.  
![](/assets/files/docs/Lainaus/vaaraosoite1.png)

Lainaustilanteessa tulee huomautus:  
![](/assets/files/docs/Lainaus/tarkistaosoite.PNG)

Huomautuksen voit poistaa, kun olet korjannut asiakkaan osoitetiedot. Vaihda asiakastietojen muokkausnäytöllä täppä 
**Käyttäjätilin huomautukset** -osiossa **Tarkista osoite** -kohtaan
“Ei” ja tallenna asiakastietojen muokkausnäyttö.

### 2.2.4 Asiakkaan kirjastokortti on kadonnut

Kun asiakas ilmoittaa kirjastokorttinsa kadonneen, tallenna tieto asiakastietojen muokkausnäytöllä osioon **Käyttäjätilin huomautukset** kohtaan **Kortti kadonnut** "Kllä".

![](/assets/files/docs/Lainaus/korttikadonnut1.PNG)

Lainaustilanteessa tulee huomautus:  
![](/assets/files/docs/Lainaus/korttikadonnut.PNG)

Kun asiakkaan kirjastokortti on kadonnut, toimi kimpassa sovittujen
käytäntöjen mukaan.  
Huomautuksen voit poistaa asiakastietojen muokkausnäytöllä vaihtamalla täppä
**Käyttäjätilin huomautukset** -osiossa **Kortti kadonnut** -kohtaan
“Ei”.

---

## 2.3 Lainauksen viestit ja huomautukset

### 2.3.1 Huomautus liitteistä

Jos lainaat niteen, joka sisältää useita osia ja tieto osista on
tallennettu niteen tietoihin kenttään 3 (Liitteiden määrä), saat
ponnahdusikkunan, jossa kerrotaan montako osaa nide sisältää.

![](/assets/files/docs/Lainaus/huomsisallosta.PNG)

Joskus lainaustilanteessa näytölle voi tulla keltaisessa laatikossa
oleva huomautus. Nämä huomautukset on käsiteltävä/huomioitava ennen
lainaamisen jatkamista.

### 2.3.2 Aineisto on varattu jollekin toiselle asiakkaalle. Varausta ei ole vielä otettu kiinni.

![](/assets/files/docs/Lainaus/lainhuom1.PNG)

### 2.3.3 Nide on varaushyllyssä varattuna toiselle asiakkaalle.

![](/assets/files/docs/Lainaus/lainhuom2.PNG)

- Jos esimerkiksi toinen perheenjäsen haluaa lainata varatun
  aineiston, valitse **Poista varaus** ja klikkaa **Kyllä, lainaa
  (Y)**. Varaus poistuu alkuperäiseltä varaajalta.
- Jos valitset vaihtoehdon **Peruuta odottava-tila** ja klikkaat **Kyllä, lainaa
  (Y)**, alkuperäisen varaajan noutoa odottanut varaus muuttuu takaisin voimassaolevaksi. 

### 2.3.4 Nide on jo lainassa tällä asiakkaalla.

![](/assets/files/docs/Lainaus/lainhuom3.PNG)

### 2.3.5 Aineisto on lainassa toisella asiakkaalla.

![](/assets/files/docs/Lainaus/lainhuom4.PNG)

### 2.3.6 Aineistoa ei lainata (niteen tila on “Ei lainattavissa”).

![](/assets/files/docs/Lainaus/lainhuom5.PNG)

- Lainauseston ohituksen salliminen määritellään järjestelmäasetuksissa.

### 2.3.7 Asiakkaalla on liian monta lainaa.

![](/assets/files/docs/Lainaus/lainhuom6.png)

- Lainauseston ohituksen salliminen määritellään järjestelmäasetuksissa.

### 2.3.8 Viivakoodia ei löytynyt.

![](/assets/files/docs/Lainaus/lainhuom7.png)

- Pikaluettelointi on mahdollista, jos se on sallittu
  järjestelmäasetuksissa.

### 2.3.9 Lainattava nide on merkitty kadonneeksi.

![](/assets/files/docs/Lainaus/lainhuom8.png)

- Järjestelmäasetuksissa voidaan määritellä, tuleeko kadonneeksi merkitystä niteestä huomautusta.

### 2.3.10 Lainattavalla niteellä on ikärajoitus, ja asiakas on liian nuori.

![](/assets/files/docs/Lainaus/lainhuom9.PNG)

- Ikärajoituksen ohituksen salliminen määritellään järjestelmäasetuksissa.

### 2.3.11 Lainattavalla niteellä on paljon varauksia, jonka takia lyhennetään laina-aikaa.

![](/assets/files/docs/Lainaus/lainhuom10.PNG)

- Laina-ajan lyhennys määritellään järjestelmäasetuksissa. Välttämättä se ei ole päällä kimppasi kirjastossa.

---

## 2.4 Asiakkaan lainat

**Lainassa**-painikkeesta saat näkyville asiakkaan kaikki lainat.  
![](/assets/files/docs/Lainaus/lainassa.PNG)

**Sarakkeet** -valikosta voit valita, mitä sarakkeita
Lainassa-välilehdellä näytetään.

![](/assets/files/docs/Lainaus/sarakkeen_nakyvyys.PNG)

**Vie**-valikosta voit tulostaa, kopioida tai viedä asiakkaan lainat Excel- tai CSV-tiedostoiksi.

![](/assets/files/docs/Lainaus/vie.PNG)

Valikosta **Lainojen määrä nidetyypeittäin** näet asiakkaan kaikki lainat yhteenlaskettuna nidetyypeittäin.

Ensimmäisenä näkyvät tänään lainatut lainat.
Myöhässä olevien lainojen eräpäivät näkyvät punaisella.

![](/assets/files/docs/Lainaus/lainat_naytto.PNG)

### 2.4.1 Lainojen uusinta

Lainassa olevien niteiden laina-ajan voit uusia sen mukaan, mitä järjestelmän
ylläpidon laina- ja maksusäännöissä on määritelty.

Lainat voi uusia asiakkaan tiedoissa Lainassa-välilehdellä tai Lainaus ja palautus -sivulla.

Huom! Jos asiakkaan sallittujen maksujen raja on ylittynyt, ohjelma ei huomauta siitä uusintatilanteessa.

#### 2.4.1.1 Lainojen uusinta asiakkaan tiedoissa olevalla Lainassa-välilehdellä.

![](/assets/files/docs/Lainaus/uusinta.png)

- Uusinta-sarakkeesta näet, kuinka monta kertaa kukin nide on uusittu. 
  Valitse uusittavat niteet ruksaamalla uusinnan valintaruutu uusittavan niteen kohdalla ja klikkaa näytön alareunasta painiketta **Uusi tai palauta
  valitut niteet** tai jos uusit kaikki lainat, klikkaa **Uusi
  kaikki** -painiketta.
  
- Uusinta-sarakkeen yläreunassa olevalla toiminnolla “valitse kaikki”
  voit valita uusittavaksi kaikki lainat, jotka on mahdollista uusia.
  Toiminto “ei valintaa” poistaa valinnat.
  
- Jos kimpassa on käytössä asetus, joka estää uusimisen samana päivänä
  uudestaan, tulee huomautus “Ei uusintaa ennen…”. Lainan voi uusia
  uudelleen kyseisen päivämäärän ja kellonajan jälkeen. Huomautus
  tulee, kun päivittää Lainassa-välilehden tai käy välillä toisella
  sivulla.  
  ![](/assets/files/docs/Lainaus/uusinta6.png)
  
  - Jos kimpassa on sallittu lainojen palauttaminen Lainassa-välilehdellä ja Sarakkeen näkyvyys -valikosta on valittu Palautus-toiminto
  aktiiviseksi, voit palauttaa lainat valitsemalla palautettavat
  niteet **Palautus**-sarakkeesta ja klikkaamalla näytön alareunasta
  painiketta **Uusi tai palauta valitut niteet**.
  
- Jos kimpassa on käytössä **Ilmoittaa palauttaneensa** -toiminto, toiminto painikkeen **Palautusilmoitukset** saat näkyville myös Sarakkeen näkyvyys -valikosta.       Toimintoa voi käyttää tilanteissa, kun asiakas ilmoittaa, että hän on palauttanut lainan, joka näkyy vielä hänen lainoissaan. Ko. niteen kohdalle tallentuu      merkintä, että asiakas sanoo palauttaneensa lainan. Tieto lainasta tallentuu myös Palautusilmoitukset-välilehdelle.  

![](/assets/files/docs/Lainaus/ilmoittaa_palauttaneensa.PNG)

Järjestelmäasetuksiin voidaan määritellä, kuinka monen "ilmoittaa palauttaneensa" -lainan jälkeen ohjelma huomauttaa määrästä virkailijalle.

#### 2.4.1.2 Uusinta Lainaus ja palautus -sivun Uusinta-linkistä.

- Huomio kirjastosi käyttösäännöt. Joissain kirjastoissa käyttösäännöt edellyttävät kirjastokorttia
  uusintatilanteessa eli tätä toimintoa ei saa silloin
  käyttää.

![](/assets/files/docs/Lainaus/uusinta1.PNG)

Uusi lainat lukemalla niteen viivakoodi uusintakentään.
Voit antaa uusittaville lainoille halutessasi eri eräpäivän, kuin nidetyypin oletuslaina-aika on.

![](/assets/files/docs/Lainaus/uusinta2.PNG)

Jos niteen uusiminen onnistuu, saat ilmoituksen.

![](/assets/files/docs/Lainaus/uusinta3.png)

Jos nide ei ole lainassa, saat ilmoituksen.

![](/assets/files/docs/Lainaus/uusinta5.PNG)

Jos viivakoodia ei löydy, saat ilmoituksen.

![](/assets/files/docs/Lainaus/uusinta4.PNG)

---

## 2.5 Asiakkaan varaukset

**Varaukset**-välilehdellä näet asiakkaan varaukset ja missä tilassa varaukset ovat. Ennen kuin varaus on jäänyt kiinni, voit vaihtaa varauksen noutopaikan, poistaa varauksen, keskeyttää varauksen tai jatkaa keskeytetyn varauksen, mikäli toiminnnot
ovat sallittu järjestelmäasetuksissa. 

![](/assets/files/docs/Lainaus/varaukset2.PNG)

---

## 2.6 Asiakkaan rajoitukset, huomautukset ja viestit

### 2.6.1 Asiakkaan rajoitukset

Voit asettaa asiakkaalle rajoituksen, joka estää lainaamisen ja uusimisen. 

Rajoituksen voit lisätä asiakastietojen muokkausnäytöllä:

![](/assets/files/docs/Lainaus/rajoitus1.PNG)

tai Rajoitukset-välilehdellä:

![](/assets/files/docs/Lainaus/rajoitus2.PNG)

Rajoitus näkyy asiakkaan Lainaus- ja Tiedot-näytöillä sekä Rajoitukset-välilehdellä.
Rajoituksen voi ohittaa tilapäisesti, jos käyttäjän oikeudet sen sallivat.

![](/assets/files/docs/Lainaus/rajoitus3.PNG)

#### 2.6.1.1 Rajoituksen poistaminen

Asiakastietojen muokkausnäytöllä poista rajoitus laittamalla täppä kohtaan **Poista** ja tallenna sivu.

![](/assets/files/docs/Lainaus/rajoite_poisto1.PNG)

Rajoitukset-välilehdellä poista rajoitus painamalla **Poista**-painiketta. 

![](/assets/files/docs/Lainaus/rajoite_poisto2.PNG)

Ohjelma varmistaa poiston ilmoituksella "Poista rajoitus?", valitse **OK**.

![](/assets/files/docs/Lainaus/rajoite_poisto3.PNG)


### 2.6.2 Huomautukset asiakastiedoissa

Voit tallentaa asiakastietojen muokkausnäytöllä asiakkaalle huomautuksia, jotka näkyvät asiakkaan Lainaus- ja Tiedot-näytöillä. 

![](/assets/files/docs/Lainaus/huomautukset1.PNG)

### 2.6.3 Viestit asiakastiedoissa

Voit lisätä asiakkaalle lyhyitä viestejä, jotka näkyvät asiakkaan Lainaus- ja Tiedot-näytöillä.
Viestin voit lisätä joko toimintapainikkeesta **Lisää viesti** tai linkistä **+Lisää uusi viesti**.

[![](/assets/files/docs/Lainaus/viesti1.PNG)

Kun valitset **Lisää uusi viesti**, pääset valitsemaan, näytetäänkö
viesti vain virkailijoille vai myös asiakkaalle verkkokirjastossa
(valikossa asiakkaan nimi).

[![](/assets/files/docs/Lainaus/lainausviesti2.PNG)

Voit valita viestin esimääritellyistä viesteistä tai kirjoittaa oman
viestin tyhjään kenttään. Kimpan pääkäyttäjät voivat lisätä esimääriteltyjä viestejä.

![](/assets/files/docs/Lainaus/lainausviesti3.PNG)

- HUOMIO! Viesti asiakkaalle näkyy myös virkailijoille.


### 2.6.3 Vanhentunut asiakastieto

Jos asiakastiedot vaativat määräaikaistarkistuksen (parametreissä
määritelty), näyttöön tulee ilmoitus:

![](/assets/files/docs/Lainaus/vanhentunut.png)

Tarkista asiakkaan yhteystiedot (osoite, puhelinnumero,
sähköpostiosoite, viestiasetukset). Jos tiedot ovat ajantasalla, klikkaa
**Uusinta**. Jos tiedot täytyy päivittää, muokkaa ja päivitä tiedot ensin linkistä **Muokkaa tietoja**.

Käyttöoikeuden voi jatkaa myös valikosta **Muita toimintoja**,
valitsemalla **Asiakkaan käyttöoikeuden jatkaminen**.

![](/assets/files/docs/Lainaus/vanhentunut2.png)

---

## 2.7 Palauttaminen

Aineiston palauttamiseen pääset eri näyttöjen kautta.

![](/assets/files/docs/Lainaus/palautus.PNG)

Kaikista lainaustenvalvonnan toiminnoista on listaus **Lainaus ja
palautus** -sivulla, jonne pääset jokaisen sivun vasemmasta yläreunasta
olevasta linkistä.

### 2.7.1 Aineiston palauttaminen

Kun palautat aineistoa, lue niteen viivakoodi Palautus-kenttään.
Palautetun niteen tiedot tulevat näytölle.

![](/assets/files/docs/Lainaus/palautus1.PNG)

**Sarakkeet**-valikosta voit valita, mitä tietoja Palautus-näytöllä näytetään. 

**Vie**-valikosta voit tulostaa, kopioida tai viedä palautetut niteet Excel- tai CSV-tiedostoiksi.

Jos teoksesta on varaus ja saat näytölle ilmoituksen: **Maksuja ei peritä käsin peruutetuista varauksista**, voit poistaa varauksen tällä sivulla ilman, että asaikkaalle tulee noutamattoman varauksen maksua. Jos palautetusta teoksesta ei ole varausta, ilmoitusta ei tarvitse huomioida.


### 2.7.2 Palautuksen viestit

### 2.7.2.1 Toisen kirjaston aineiston palautus

Jos olet palauttamassa jonkun muun kirjaston aineistoa, saat viestin,
jossa ilmoitetaan mihin kirjastoon nide pitää kuljettaa.

![](/assets/files/docs/Lainaus/palautusviesti1.PNG)

- Palautuksen jälkeen niteen tilaksi muuttuu _Kuljetettavana_.  
  ![](/assets/files/docs/Lainaus/palautusviesti2.PNG)

- Nide pitää palauttaa kotikirjastossaan, jotta sen tilaksi muuttuu
  Saatavana-tila.


### 2.7.2.2 Useita osia sisältävän niteen palautus

Jos palautat niteen, joka sisältää useita osia ja tieto osista on
tallennettu niteen tietoihin kenttään 3 (Liitteiden määrä), saat
ilmoituksen, jossa kerrotaan montako osaa nide sisältää.  
![](/assets/files/docs/Lainaus/palautusviesti9.PNG)


### 2.7.2.3 Varatun niteen palautus

Järjestelmäasetuksissa voidaan määritellä, tulostetaanko varauksen info- ja kuljetuskuitti automaattisesti vai pitääkö virkailijan vahvistaa kuitin tulostaminen. 

***Varauksen infokuitin tulostaminen manuaalisesti***:

- Kun palautat niteen, josta on varaus, saat siitä ilmoituksen:

![](/assets/files/docs/Lainaus/palautusviesti10.PNG)

- Valitsemalla toiminnon **Vahvista varaus**, nide menee Odottaa-tilaan.
- Toiminnolla **Tulosta kuitti ja vahvista**, ohjelma tulostaa varauksen infokuitin ja muuttaa niteen Odottaa-tilaan. 
- Toiminnolla **Älä huomioi**, nide jää Saatavana-tilaan ja varaus säilyy asiakkaalla voimassa olevana.

Jos palautat varatun niteen toistamiseen samalla näytöllä, saat ilmoituksen, jossa on mahdollista poistaa varaus toiminnolla **Poista varaus**. 

![](/assets/files/docs/Lainaus/palautusviesti11.PNG)

- Poistetusta varauksesta ei tallennu asiakkaalle noutamattoman varauksen maksua, kun poisto tehdään samalla palautusnäytöllä, kuin alkuperäinen palautus on tehty. Varausviestin taakse jää ilmoitus **"Maksuja ei peritä käsin peruutetuista varauksista"**.

***Varauksen infokuitin tulostuminen automaattisesti***:

- Kun palautat niteen, josta on varaus, saat siitä ilmoituksen:

![](/assets/files/docs/Lainaus/palautusviesti3.PNG)

- Jos järjestelmäasetuksiin on määritelty, että varauskuitit tulostuvat automaattisesti, tulostuu varauksen infokuitti heti, kun olet palauttanut varatun niteen. 
- Jos palautat niteen toisen kerran, ohjelma vaatii manuaalisen varausilmoituksen kuittauksen.


### 2.7.4.4 Varaus toisessa kirjastossa

Jos palautat niteen, josta on varaus jossain toisessa kirjastossa, saat
ilmoituksen ja tiedon, mihin kirjastoon nide pitää kuljettaa.

***Varauksen kuljetuskuitin tulostaminen manuaalisesti***:

![](/assets/files/docs/Lainaus/palautusviesti5.PNG)

- Valitsemalla **Vahvista varaus ja kuljetus**, vahvistat niteen kuljetettavaksi kirjastoon, missä on varauksen noutopaikka.
- Toiminnolla **Tulosta kuitti, kuljeta ja vahvista**, ohjelma tulostaa varauksen kuljetuskuitin ja merkitsee niteen kuljetustilaan kirjastoon, missä on varauksen noutopaikka. 
- Toiminnolla **Älä huomioi**, nide jää Saatavana-tilaan ja varaus säilyy asiakkaalla voimassa olevana.

***Varauksen kuljetuskuitin tulostuminen automaattisesti***:

![](/assets/files/docs/Lainaus/palautusviesti13.PNG)

- Jos järjestelmäasetuksiin on määritelty, että varauskuitit tulostuvat automaattisesti, tulostuu varauksen kuljetuskuitti heti, kun olet palauttanut varatun niteen. 


### 2.7.2.5 Asiakkaan maksut palautusnäytöllä

Jos järjestelmä on asetettu näyttämään maksut palautuksen yhteydessä,
saat keltapohjaisen viestin asiakkaan maksuista.  
![](/assets/files/docs/Lainaus/palautusviesti7.png)


### 2.7.2.6 Kadonneeksi merkityn niteen palauttaminen

Jos palautat kadonneeksi merkityn niteen, saat seuraavan ilmoituksen:  
![](/assets/files/docs/Lainaus/palautusviesti8.PNG)
- Kadonnut-tila poistuu niteeltä automaattisesti, jos järjestelmäasetuksiin on näin määritelty. 


### 2.7.2.7 Laskutetun niteen palauttaminen

Jos palautat niteen, joka on laskutettu, saat seuraavan ilmoituksen:
![](/assets/files/docs/Lainaus/palautusviesti12.PNG)

- Niteen laskutettutila ei poistu automaattisesti, jos järjestelmäasetuksissa on näin määritelty.


---

## 2.8 Siirto-toiminto

Kirjastokimpassa voit siirtää niteitä toiseen kirjastoon käyttämällä
**Siirto**-työkalua.

- Valitse: Lainaus ja palautus -&gt; **Siirto**

![](/assets/files/docs/Lainaus/Siirto.png)  
Valitse alasvetovalikosta kirjasto, johon olet siirtämässä aineistoa ja
lue siirrettävän niteen viivakoodi _Syötä viivakoodi_ -kohtaan. Paina
lopuksi **OK**.

![](/assets/files/docs/Lainaus/Siirto1_2.png)  
Nyt niteeseen tulee palautuksessa tieto määränpäästä..

![](/assets/files/docs/Lainaus/Siirto1_3.png)  
ja niteen tilaksi kuljetuksessa.

![](/assets/files/docs/Lainaus/Siirto1_4.png)

Kun nide saapuu kohteeseen, se on siellä palautettava, jotta nide ei ole
enää kuljetuksessa.

Nidettä ei ole pysyvästi siirretty kohdekirjastoon. Niteen kotikirjasto
ei muutu, mutta nykyinen paikka on toinen kirjasto.

![](/assets/files/docs/Lainaus/Siirto1_5.png)

---

## 2.9 Kirjaston valinta

Oletuksena on, että kirjaudut virkailijatyökaluun kotikirjastossasi.
Kirjaston nimi näkyy virkailijatyökaluikkunan oikeassa yläreunassa.
**Tärkeää:** Lainat ja palautukset rekisteröityvät tunnukselle valitun
kirjaston mukaan.

![](/assets/files/docs/Lainaus/kirjastovalinta.png)

Jos työskentelet useammassa kirjastossa, pääset valitsemaan kirjaston
_Aseta kirjasto_ -napista. Valitse kirjasto alasvetovalikosta ja klikkaa
OK.

![](/assets/files/docs/Lainaus/kirjastovalinta2.png)  
Valitsemasi kirjasto tulee näkyviin oikeaan yläkulmaan ja toiminnot
tapahtuvat valitsemassasi kirjastossa (lainat, palautukset jne.)

## 2.10 Pikakuvailu

Kuvailusääntöjen mukaisesti.

---

## 2.11 Lainauksen valmiit raportit

Useimmat raportit saadaan Raportit-moduulin kautta, mutta joitakin
raportteja löytyy myös Lainauksen toiminnoista.

### Varausjono

Tämä raportti näyttää kaikki varaukset mitkä kohdistuvat kirjastosi aineistoon. 

**Huomaa:** Tämä ei ole Koha-Suomen suosittelema raportti hyllyvarausten
käsittelyyn.

![](/assets/files/docs/Lainaus/raportit1001.png)

- Voit rajata raportin ajovaiheessa nidetyypin, kokoelman ja hyllypaikan mukaan.

![](/assets/files/docs/Lainaus/raportti2.png)

Hakutuloksia voi suodattaa ja järjestellä yläreunan valikon avulla.
Näkyvillä olevia sarakkeita voi säätää _Sarakkeet_
-painikkeella ja tiedot voi viedä Excel- tai CSV-muotoon, kopioida ja tulostaa.

### Hyllyvaraukset

**Huomaa:** Koha-Suomi suosittelee käyttämään tätä raporttia, kun
etsitään hyllyvarauksia.

**Huomaa myös:** Hyllyvarausraportti ei ole täysin reaaliaikainen,
vaikka se avautuukin nykyään nopeammin kuin ennen. Hyllyvarausraportin
tiedot haetaan tausta-ajolla, jonka kesto on varausten määrästä riippuen
muutamasta sekunnista useampaan minuuttiin. Tänä aikana käsiteltävien
niteiden ja varausten tiedot voivat muuttua ja listalle voi tulla
tietoa, joka ei pidä enää katseluhetkellä paikkansa. Tästä voi myös
johtua, että listalle voi päätyä tilanne, että toisesta kirjastosta
omaan kirjastoon kuljetettavana oleva nide näyttäisi olevan listan
mukaan hyllyssä omassa kirjastossa. Nide on palautettu kesken ajon ja
mennyt kuljetustilaan. Kuljetettavan niteen sijaintikirjastona on
tietokannassa kohdekirjasto. Tälle epäreaaliaikaisuudelle ei ikävä kyllä
voi tehdä mitään, koska tausta-ajolla kuluu työhönsä oma aikansa ja
tilanne taustalla muuttuu koko ajan, kun niteitä palautetaan lainasta
tai joku muu ehtii palauttaa omassa hyllyssä paikalla olevan niteen.

Hyllyvaraukset raportilla pystyy hakemaan näytölle kaikki voimassa
olevat hyllyvaraukset. Raportin toimintaan on tehty Koha-Suomessa
muutoksia käyttäjien toiveiden perusteella.

Vinkkejä:

- valitse kirjasto-sarakkeista oma kirjasto, jolloin pystyt helposti
  tarkistamaan omassa kirjastossa paikalla olevat varaukset, joiden
  noutopiste on myös oma kirjastosi.
- rajaa lista esimerkiksi materiaalin mukaan pelkkiin DVD-levyihin
  tai hyllypaikan mukaan aikuisten hyllypaikalle.
- tarkista, ettei listalle ole jäänyt varauksia roikkumaan pitkäksi
  aikaa järjestämällä Varauspvm-sarake nousevasti, jolloin
  ylimmäiseksi tulee vanhimmat varaukset.

Listaus näyttää kaikki nimekkeet, joista on varauksia ja joilla on
niteitä saatavana. Ensin kannattaa tarkistaa ne varaukset, joissa
noutokirjastona on oma kirjasto/oman kunnan toinen kirjasto.
Noutokirjaston kuudennesta sarakkeesta "Varaus". 

![](/assets/files/docs/Lainaus/hyllyvaraus1.png)

Voit suodattaa hakutuloksesta "On shelf" -sarakkeen alla olevasta
valikosta oman kirjastosi aineistot esille. Jos valintaa ei ole tehty,
näkyvillä on _Ei mitään_.

![](/assets/files/docs/Lainaus/hyllyvaraus2.png)

Näytön alareunassa näkyy, minkä verran aineistoa on suodatettu.

![](/assets/files/docs/Lainaus/lainrap6.png)

Voit halutessasi säätää näkyviä sarakkeita ”Sarakkeet”-kohdasta ylävalikosta.

![](/assets/files/docs/Lainaus/hyllyvaraus4.png)

- Voit lajitella hakutuloksia otsikkorivin nuolimerkinnöistä.
- Vie-napista hyllyvarauslistan voi viedä Excel- tai CSV-muotoon, kopioida tai tulostaa. Jos raportin haluaa välttämättä tulostaa, kannattaa se tehdä tämän nappulan kautta, koska tiedot asettuu paperille tällöin paremmin.

### Noudettavissa olevat varaukset

Tämä raportti näyttää kaikki kirjastossasi noutoa odottavat niteet.

![](/assets/files/docs/Lainaus/kaikkinoudettavat.png)

HUOM! Vanhentuneet varaukset eivät enää näy oikein tämän näytön välilehdellä. Käytä vanhentuneiden varausten etsimiseksi 
sql-raporttia :

> select othernames as 'Varaustunnus', b.title as 'Teos', i.barcode as 'Viivakoodi', bi.itemtype as 'Aineistotyyppi'
from old_reserves o
JOIN biblio b using (biblionumber)
JOIN biblioitems bi using (biblionumber)
JOIN borrowers using (borrowernumber)
JOIN items i using (itemnumber)
where o.branchcode=<<Valitse kirjasto|branches>>
and o.cancellationdate between <<Vanhentumispäivä alkaen|date>> AND <<Päättyen|date>>
and o.found='W'
AND o.expirationdate = (o.cancellationdate - INTERVAL 1 DAY)
order by 1,2


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

## 2.12 Offline eli yhteydettömän tilan lainaus

Vaikka nettiyhteys ei toimisi, voit jatkaa lainaamista. Vaihtoehtoina on

1.  **Offline lainausohjelma Windowsille** (KOC). Erillinen ohjelma
    yksittäisille lainauskoneille. Tätä voi käyttää, kun ei ole yhteyttä
    internetiin.
2.  **Koha Offline Circulation Tool** (KOCT), joka on selaimen lisäosa.
    Tätä voi käyttää esimerksi yllättävien verkkoyhteyskatkoksien
    aikana.
3.  **Yhteydettömän tilan lainaus**, jota voi käyttää, kun tietää
    ennakkoon, ettei yhteyttä ole. Esimerkiksi kirjastoautossa. **Ei
    suositella käytettäväksi**

### 2.12.1. Offline lainausohjelma Windowsille (KOC)

[Ohjelman asennus- ja käyttöohje PDF-muodossa]
(https://github.com/KohaSuomi/kohasuomi.github.io/blob/master/assets/files/docs/Lainaus/Koha%20Offline%20Circulation.pdf)

https://github.com/KohaSuomi/kohasuomi.github.io/blob/master/assets/files/docs/Lainaus/Koha%20Offline%20Circulation.pdf

### 2.12.2 Koha Offline Circulation Tool (KOCT)

Englanninkielinen lisäosa.

[Ohje pdf-muodossa](https://github.com/KohaSuomi/kohasuomi.github.io/blob/d1dc796fbb0a91ac574f2e5e628df28ecd894eb5/assets/files/Koha%20Offline%20Circulation%20Tool%20(KOCT).pdf)


### 2.12.3 Yhteydettömän tilan lainaus

**Tämä ei ole suositeltava tapa**

[Yhteydettömän lainauksen ohje pdf-muodossa](https://github.com/KohaSuomi/kohasuomi.github.io/blob/8b5a19ba3ab67748beb2da63e68fd8d8da71ca19/assets/files/Yhteydetonlainaus.pdf)
---

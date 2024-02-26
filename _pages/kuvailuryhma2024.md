---
layout: single
permalink: /kuvailuryhma2024
header:
  overlay_color: '#5e616c'
  overlay_image: /assets/images/cropped-pexels-photo-113850.jpeg
toc: true
title: 'Koha-Suomen kuvailuryhmän muistiot 2024'
---


## Kuvailuryhmän muistio 2/2024 ##

Aika: 15.2.2024 klo 13.15–14.40

Osallistujat: Mauri Aittaniemi (Lappi), Merja Hakulinen (Lumme), pj. Antti Heikkinen (OUTI), Pasi Hynninen (Helle), Suvi Kauranen (Kirkes), Päivi Knuutinen (Vaara), Marjukka Laapotti (Lastu), Tarja Mäkinen (Kyyti), Johanna Ranta (Kyyti), Marja Soisalo (Vaara), Anna Viitanen (Vaski)

### Asialista ###

#### 1.	Kokouksen avaus ja sihteerin valinta ####

Sihteerivuorossa oli Tarja Mäkinen.

#### 2.	RDA-konversioiden eteneminen ####

Kansalliskirjastossa korjaukset vielä kesken. Odotetaan niiden valmistumista ennen kuin järjestetään toinen testikierros. Kannattaa huomata, että konversiossa vanhoilta tietueilta poistuu 245$h-kenttä. Kentässä on ilmaistu hakasuluissa yleismääre, mutta siihen voi olla eksynyt myös toiseen osakenttään kuuluvaa tietoa. OUTIssa on tehty raportteja, joilla voi tarvittaessa hakea tällaiset tietueet ja selata läpi, onko joukossa tietueita, jotka kannattaisi korjata ennen konversiota.

#### 3.	YSO-konversion testaustuloksia Vaskissa ####
<ul>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/1040" target="_blank">YSA/YSO-konversion testausta</a> </li>
  <li>Kannattaa tutustua etukäteen, millaisia lokitiedostoja konversio-ohjelma tuottaa: <a href="https://www.kiwi.fi/display/ysall2yso/Konversio-ohjelman+lokitiedostot" target="_blank">YSA/YSO-konversio-ohjelman lokitiedostot</a> </li>
</ul>

Anna Viitanen kertoi Vaskin testaustuloksista – toimii niin hyvin kuin mahdollista. Virheet johtuneet siitä, että termit olivat virheellisiä tai vanhentuneita, eivät itse konversiosta. Osa virheellisistäkin oli konvertoitunut oikein. Jos yhdessä tietueessa oli ollut sama asiasana useaan kertaan eri asiasanaketjuissa, se oli konvertoidussa tietueessa siististi vain yhden kerran. Antti kysyy Kansalliskirjastosta vielä päivitystä 648-kentän konversiosääntöihin.

#### 4.	Melindan kuvailukoulutukset ####

Kimpoissa oli kyselty, millaista kuvailukoulutusta tarvittaisiin. Vastaukset vaihtelivat ja tuli ilmi, että kimppojen välillä on edelleen eroja siinä, miten kuvailu on järjestetty. Osassa kuvailu on keskitetty yhteen tai muutamaan kuntaan. Osassa kuvaillaan joka kunnassa. TäTi-tunnuksia on jaettu enemmän kuin mitä TäTiin kuvailevia oikeasti on. Eniten koulutusta toivottiin seuraavissa asioissa:
<ul>
  <li>kiinteämittaiset kentät</li>
  <li>osakohteet ja niiden käsittelyn ongelmatilanteet</li>
  <li>kertaus Kohassa kuvailusta</li>
  <li>esineet ja harvinaisemmat aineistotyypit</li>
  <li>Melinda-tietueiden käsittely</li>
  <li>Mikropalvelun toiminnot eli miten kuvailutiedot siirretään TäTistä Melindaan ja Melindasta TäTiin</li>
</ul>
  
#### 5.	TäTin ja paikalliskantojen emottomat osakohteet ####
<ul>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/348" target="_blank">Emottomien osakohteiden poisto ajona</a> </li>
  <li>Raportissa myös luettelo virheellisistä osakohteista, joista osa pitäisi korjata </li>
  <li>ERROR:773w org "FI-Arto" does not match "FI-MELINDA" -> osakohteissa toinen 773w-kenttä, jossa linkki ARTO-tietokantaan. Kysytty Melindasta, mitä tarkoittaa. Vastattu, että jos Melindan osakohteissa on toinen 773w-kenttä, jossa on FI-Arton kontrollinumero, niin sen voi poistaa tietueista, jos Melinda-tietueen linkki on toimiva </li>
  <li>ERROR:ldr/7 is m -> osakohde monografiana, korjattava. Nykyään ei linkity enää emoon, vaikka emotietue on tietokannassa </li>
  <li>ERROR:773w org "FI-MELINDA" does not match "FI-TATI" -> Joko Melindaan vienti jäänyt vaillinaiseksi eli osakohteiden 003-kenttä jäänyt päivittymättä (FI-TATI -> FI-MELINDA), tai Melinda-tietueelle TäTissä tehtyjä uusia osakohteita, joita ei ole viety Melindaan. Nämä kannattaa korjata ensin TäTissä. Antti käy läpi TäTin virheraportin näiden osalta. </li>
  <li>TäTissä myös ERROR:773w org "FI-TATI" does not match "FI-MELINDA" -> Näissä tietueissa on jotain häikkää, joka pitää selvittää Melindan kanssa.</li>
</ul>

#### 6.	337a-kentän käännösvirhe ruotsinkielisissä RDA-tietueissa: oförmedlad -> omedierad ####
<ul>
  <li>TäTissä 2573 kpl -> korjataan joko RDA-konversiossa tai konversioiden jälkeen, kun on aikaa </li>
  <li>Voi korjata Tietueiden muokkaus eräajona -toiminnolla:</li>
    <ol>
    <li> Hae tietueet hakulausekkeella: media-type-term:oförmedlad </li>
    <li> Tarkista, ettei joukossa ole tietueita, joilla saattaa olla useampi 337-kenttä. Tällaiset tietueet kannattaa korjata käsin erikseen. </li>
    <li> Siirrä tietueet koriin </li>
    <li> Muokkaa tietueet eräajolla (Marc-muokkausten pohja: Päivitä olemassa oleva tai lisää uusi kenttä 337$a arvolla omedierad) </li>
    </ol>
</ul>

#### 7.	Moniviestimien kuvailu ####
<ul>
  <li>Moniviestinten primaarikuvailu on vähentynyt </li>
  <li>Toistaiseksi ei ole tarvetta päivittää moniviestimien kuvailupohjaa TäTissä </li>
</ul>

#### 8.	Muita asioita ####
<ul>
    <li>Toimijanimimuutosten päivitykset TäTissä (TäTissä on 5 vuotta vanhempia RDA-tietueita ja myös Melindaan linkittämättömiä Melinda-tietueita)</li>
  <ul>
  <li>olisi hyvä tarkistaa, onko tietue TäTissä, ja tehdä tarvittavat korjaukset siellä </li>
  <li>ei tuoda Melindasta TäTiin vanhoja, huonoja tietueita (omaan tietokantaan voi tuoda) </li>
  </ul>
    <li><a href="https://github.com/KohaSuomi/Koha/discussions/1068" target="_blank">Puppe-tilaustenvastaanottotyökalun esittely 21.2.</a> </li>
</ul>

#### 9.	Seuraava kokous To 14.3. klo 13.15 ####


---
## Kuvailuryhmän muistio 1/2024 ##

Aika: 25.1.2024 klo 13.15–14.41

Osallistujat: Mauri Aittaniemi (Lappi), Merja Hakulinen (Lumme), pj. Antti Heikkinen (OUTI), Pasi Hynninen (Helle), Päivi Knuutinen (Vaara), Sani Kuosmanen (Kirkes), Marjukka Laapotti (Lastu), Tarja Mäkinen (Kyyti), Johanna Ranta (Kyyti), Anna Viitanen (Vaski), Anneli Österman (Koha-Suomi), Johanna Räisä (Koha-Suomi, kohdat 2-4), Emmi Takkinen (Koha-Suomi, kohdat 2-4)

Poissa: Marja Soisalo (Vaara)

### Asialista ###

#### 1.	Kokouksen avaus ja sihteerin valinta ####

Päivi Knuutinen oli sihteerivuorossa ja valmistautunut tehtävään.

#### 2.	Tilannekatsaus RDA-konversioiden testituloksiin ####
<ul>
  <li>RDA-konversiossa testattujen nimekkeiden kohdalla on huomattu puutteita konversiosäännöissä etenkin ruotsin kielellä kuvailtujen nimekkeiden kohdalla. (Tiketti: <a href="https://github.com/KohaSuomi/Koha/issues/974" target="_blank">RDA-konversion testaus</a>)  </li>
  <li>Joistakin konversiovirheistä on hankala sanoa, johtuuko virhe itse tietueesta vai konversiosääntöjen puutteista.</li>
  <li>Kansalliskirjasto on luvannut päivittää konversiosääntöjään. Osa päivityksistä on jo tehty, muttei kaikkia. Antti kysyy Kansalliskirjastosta neuvoa virhetapausten selvittelyyn.</li>
  <li>Tietokantojen siivous- ja korjausajoja olisi syytä saada tehtyä ennen kuin RDA-konversio tehdään, jotta konversio onnistuisi paremmin ja jäisi vähemmän käsin korjattavaa tietoa. Päivi Knuutinen tekee tarvittaessa tiketit GitHubiin ja kukin kimppa saa kommentoida, tarvitseeko jonkin tietyn korjauksen omaan tietokantaansa.</li>
  <li>Todettiin, että jos nimeke on jo RDA-kuvailtu, sitä ei enää konvertoida, jolloin työ nopeutuu.</li>
  <li>Vaskissa voidaan testata YSA/YSO-konversiota ensimmäisenä, sillä siellä aineisto on jo RDA-muodossa. Päivi tekee tiketin, johon kerätään testattavia tietueita. [Lisäys 26.1.: Tiketti: <a href="https://github.com/KohaSuomi/Koha/issues/1040" target="_blank">YSA/YSO-konversion testausta</a>] </li>
</ul>

#### 3.	Uuden tietuesiirtäjän käyttöönotto ####
<ul>
  <li>Miten Vaaran ja Vaskin testaukset etenevät?</li>
- Vaaran testaus ei ole toimiva, koska Vaaran testikanta on redusoitu. Vaskin testaustulokset ovat lupaavia.
  <li>Tietuesiirtäjään liittyvä tiketti (odotustilassa): <a href="https://github.com/KohaSuomi/Koha/issues/286" target="_blank">Siirtoraportti-toimintoon tieto, onko siirtoraportin tietue uusi täydellisesti kuvailtu tietue VAI jo olemassa olevan täydellisesti kuvaillun tietueen muutostietue</a> </li>
- Johanna Räisän mielestä tämä on mahdollista toteuttaa tavalla tai toisella.
  <li>Osakohteiden aineistotyypin lisäys vielä työn alla </li>
  <li>Asennus voidaan aloittaa yhdestä kimpasta, tarkastella tilannetta hetken aikaa ja sitten laajentaa muihin.</li>
</ul>

#### 4.	5- ja 9-osakenttien suojaukset Mikropalvelussa ####
<ul>
  <li>Pitäisikö poistaa, koska estävät niiden kenttien muokkaamisen, jotka sisältävät jommankumman osakentän?</li>
- Johanna Räisä miettii, miten voisi toteuttaa. Testattava.
  <li>Mikropalvelun toiminta siirtymässä uudelle liitännäiselle: <a href="https://github.com/KohaSuomi/koha-plugin-broadcast-biblios/issues/4" target="_blank">Melinda-vientien ja -tuontien siirtäminen liitännäiseen</a> </li>
</ul>

#### 5.	MARC-virheellisten tietueiden korjausajot ja muut massakorjaukset ####
<ul>
  <li>Taulukko Kohan massakorjauksista ja tikettien laadinta </li>
- Sovittiin, että käsitellään tulevissa kokouksissa aina muutama korjausehdotus kerrallaan, mitkä kimpoista tarvitsevat kyseiset korjausajot, ja tehdään näistä sitten tarvittaessa tiketit.
  <li>Kumean tekemät muutokset Metatietosanastossa tai Melindaan pyytämät korjausajot </li>
  <ul>
<li>Missä vaiheessa lisätään taulukkoon? </li>
-Päivitetään sitä mukaa kun näistä ilmoitetaan Kumean muistioissa.
<li>Sanaston muutosten vaikutukset kuvailupohjien valikkoihin: Jos esim. termi ”avattu nimeke” jää pois, poistetaanko auktorisoitujen arvojen valikosta heti? 
-> Vanhaa tietuetta muokatessa pitää huomata, että jos tietueessa on jokin vanhentunut termi, joka puuttuu valikosta, niin se katoaa, kun tietueen aukaisee valikon sisältävällä kuvailupohjalla. Termiä ei myöskään näy perustiedot-näytöllä, jos tietue on tallennettu valikon sisältävällä kuvailupohjalla.</li>
- Sovittiin, että valikot ajantasaistetaan.
  </ul>
</ul>

#### 6.	Kuulumisia Koha-Suomi-Melinda-työryhmän kokouksesta 24.1. ####
<ul>
  <li>TäTi-putken valmistelu etenee omalla painollaan. Seuraavaksi Kirjastopalvelun tietueet jaotellaan osakohteettomiin ja osakohteellisiin paketteihin ja testataan, miten niiden siirtäminen ja Melinda-tietueisiin yhdistäminen onnistuu.</li>
  <li>Kuvailukoulutusta mahdollisesti elo/syyskuussa, kun Lastun käyttöönotto on lähempänä.</li>
  <li>Seuraava työryhmän kokous 9.4.</li>
</ul>
-> Seuraavaan kokoukseen mennessä kukin kimppa miettii, millaista kuvailukoulutusta olisi tarpeen järjestää. Onko koulutus pelkästään Koha-Melinda-asioihin keskittyvä vai kuinka paljon itse kuvailuun keskittyvä? Tarvitaanko koulutusta esim. Kohan kuvailutyökalujen tai Mikropalvelun toiminnoista, Fennica/Viola- tai muiden Melinda-tietueiden käsittelystä vai joidenkin tiettyjen aineistolajien kuvailusta?


#### 7.	Tikettejä ####
<ul>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/1006" target="_blank">Välimerkkiongelma Z39.50/SRU-haussa</a> </li>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/998" target="_blank">Marc-virheiden korjausta kentästä 007-s</a> </li>
   - Kimppojen kommentoitava, halutaanko korjausajo omaan kimppaan.
</ul>

#### 8.	Muita asioita ####

TäTissä on paljon yksittäisiä MARC-virheitä, joita on muutamia/virhe. Kukin kimppa voisi korjata tällaisia virheitä itse, jos oman kirjaston tunnus näkyy tietuerivillä. 

#### 9.	Seuraavat kokoukset ####
<ul>
   <li>To 15.2. klo 13.15 </li>
   <li>To 14.3. klo 13.15 </li>
   <li>Ke 17.4. klo 13.15 </li>
   <li>To 16.5. klo 13.15 </li>
</ul>



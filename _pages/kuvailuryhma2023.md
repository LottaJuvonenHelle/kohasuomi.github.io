---
layout: single
permalink: /kuvailuryhma2023
header:
  overlay_color: '#5e616c'
  overlay_image: /assets/images/cropped-pexels-photo-113850.jpeg
toc: true
title: 'Koha-Suomen kuvailuryhmän muistiot 2023'
---

## Kuvailuryhmän muistio 9/2023

Aika: 14.12.2023 klo 13.15–14.40

Osallistujat: Mauri Aittaniemi (Lappi), Merja Hakulinen (Lumme), pj. Antti Heikkinen (OUTI), Pasi Hynninen (Helle), Suvi Kauranen (Kirkes), Päivi Knuutinen (Vaara), Marjukka Laapotti (Lastu), Tarja Mäkinen (Kyyti), Marja Soisalo (Vaara), Anna Viitanen (Vaski), Anneli Österman (Koha-Suomi), Johanna Räisä (Koha-Suomi, kohdat 2 & 3)

Poissa: Johanna Ranta (Kyyti)

### Asialista ###

#### 1.	Kokouksen avaus ja sihteerin valinta ####

Kokous avattiin ja sihteeriksi valittiin Suvi Kauranen.

#### 2.	RDA- ja YSO-konversioiden tilanne ####
<ul>
   <li>RDA: <a href="https://github.com/KohaSuomi/Koha/issues/834" target="_blank">RDA-konversio kaikkiin kimppoihin, joissa sitä ei ole tehty</a> </li>
	<ul>
	<li>Johanna Räisä aloittanut RDA-konversiopaketin (USEMARCON) testaamisen testi-TäTi-tietokannassa. Tärkeimmät testiajot tehty, mutta esim. kyrillisten kirjainten ajoa ei ole testattu.</li>
	<li>Konversiossa on tärkeää huomioida, että konversio-ohjelma ei osaa erottaa, onko tietokannassa jo osittain RDA:n mukaista tietoa, vaan ajaa muutokset kaikkiin kenttiin.</li>
	<li>Keskusteltiin niiden kimppojen kokemuksista, joissa RDA-konversio on jo tehty. Konversiosääntöjä on tärkeää testata hyvin etukäteen, mutta myös jälkikäteen voi tehdä korjauksia. Vaskin kokemusten 	mukaan oleellista on kiinnittää huomiota käsin poimittuihin tietueisiin, koska niissä voi tapahtua poikkeuksia esim. musiikin lyhenteissä. Samoin ruotsinkielisen aineiston kanssa kannattaa olla 		tarkkana, sillä suomenkielinen konversio-ohjelma tekee tietueista helposti sekakielisiä.</li>
	<li>Sovittiin, että jokainen kimppaa, johon paikalliskannan RDA-konversio on tulossa, kokoaa listan kriittisiksi kokemistaan bibliografisista tietueista, joita erityisesti halutaan testata ennen 		konversiota. Listalle kerätään esim. ruotsin-, venäjän- ja saamenkielistä aineistoa, erilaista musiikkiaineistoa (nuotteja, levyjä ja moniviestimiä) ja omia erikoisuuksia. </li>
	<li>Listat toimitetaan Johannalle. Päivi tekee listasta tiketin GitHubiin. Listalle mieluiten biblionumberit. Listat valmiina tammikuun alussa. Listalle riittää tietueita sen verran kuin niitä 		haluaa käydä läpi tietueita tarkastellessa. Osakohteet on listattava myös erikseen, jos haluaa niitä mukaan. Listaukseen voi pyytää tarvittaessa apua kimpan pääkäyttäjiltä. Tiketti lisätty 15.12.: <a href="https://github.com/KohaSuomi/Koha/issues/974" target="_blank">RDA-konversion testaus</a></li>
	<li>Jos testeissä ei ilmene mitään erityistä, Johanna ajaa tietokantoihin ensin ISBD-konversion (tarvittaessa) ja sen jälkeen RDA-konversion. Kyrillisten kirjainten konversiota ei välttämättä 		tarvita.</li>
	</ul>
   <li>YSO: <a href="https://github.com/KohaSuomi/Koha/issues/390" target="_blank">YSA-YSO-konversio kaikille kimpoille</a> </li>
	<ul>
	<li>Johanna aloittanut myös YSA-YSO-konversion testaamisen Testi-TäTissä. </li>
	<li>Kaunokki-Kauno-konversiota ei tehdä tässä konversiossa. </li>
	</ul>
</ul>

#### 3.	Valutuksen siirtäminen broadcast biblios -liitännäiselle ####
<ul>
   <li><a href="https://github.com/KohaSuomi/Koha/issues/915" target="_blank">Valutuksen siirtäminen broadcast biblios liitännäiselle</a> </li>
   <li>Tietuesiirtäjä ja siirtoraportti </li>
</ul>
<ul>
   <li>Uuden valutusliitännäisen nimi: Tietuesiirtäjä.</li>
   <li>Vie/Tuo-nappi tuo tietueet edelleen Mikropalvelun kautta ja näiden tietueiden valutukset näkyvät vanhassa siirtoraportissa.</li>
   <li>Johanna ja Antti testanneet valutuksen toimivuutta OUTIn testikannassa.</li>
   <li>Osakohteet ovat toimineet hyvin. Nyt kaikki valuvat kerralla, eikä osa jää matkalle.</li>
   <li>Osakohteet näkyvät tietuesiirtäjän ”siirtoraportilla” joko emon yhteydessä tai sitten erikseen, jos emolle ei ole tehty paikalliskannassa mitään muutosta.</li>
   <li>Tietuesiirtäjän siirtoraportilla näkyy tietuenumeroiden lisäksi myös tekijä, nimeke ja aineistotyyppi. Tarvittaessa saa näkyviin myös tietueen koko Marcin.</li>
   <li>Joitakin puutteita on vielä, esim. osakohteiden 942$c ei toimi oikein, vaan kenttäsuojaus estää myös kokonaan uuden kentän siirtymisen.</li>
   <li>Sovittiin, että Johanna laittaa testauksen päälle myös Vaskin ja Vaaran testikantoihin.</li>
   <li>Tarkoitus on siirtää koko Mikropalvelun toiminto uudelle liitännäiselle seuraavan versiopäivityksen yhteydessä. Tietuesiirtäjä voidaan asentaa jo aiemmin, jos se todetaan toimivaksi.</li>
</ul>

#### 4.	Kirjastopalvelun ja Ekstranetin toiminta ####
<ul>
	<li>Kirjastopalvelulla on runsaasti teoksia, joihin ei tule kuvailua, vaikka Ekstranetissä lukee, että kuvaillaan. Usein syynä, että KP ei saa kuvailukappaletta. Esim. saamenkielinen aineisto odottaa 	hyvin pitkään. </li>
	<li>Kirjastopalvelu on muuttamassa kuvailukäytäntöään niin, että vähintään kolmen kimpan on tilattava teos, jotta se kuvaillaan (koskee kirja-aineistoa). Helle-kimpalle kolmen kimpan vaatimus on 		ongelma, koska heillä on monta ruotsinkielistä kirjastoa, mutta kaikki samassa kimpassa. Sama ongelma koskee saamenkielistä aineistoa: tilataan samasta kimpasta ja usein pientoimittajilta. </li>
	<li>Pohdittiin, tuleeko Kirjastopalvelun uudesta käytännöstä ongelmia ja kuinka Kirjastopalvelua tarvittaessa lähestytään. </li>
	<li>Päätettiin odottaa uudistuksen käyttöönottoa ja katsoa pari kuukautta, kuinka alkaa sujua. </li>
	<li>Päätettiin, että uudistuksen jälkeen kuvailua odotetaan noin 8–12 viikkoa ja sen jälkeen sitä karhutaan Kirjastopalvelusta. Voi myös kuvailla itse. </li>
	<li>Keskusteltiin Kirjastopalvelu-tietueiden virheistä. Virheellisten tietueiden määrä on lisääntynyt, mutta hankala sanoa, onko virhe KP:n tekemä vai syntynyt myöhemmin Melindassa (esim. Helmet-		tietueiden erätuonti voi aiheuttaa sen). Välillä on haastavaa tietää, pitääkö virheestä ilmoittaa KP:lle vai ei. </li>
	<li>Muutamassa kimpassa on havaittu, että tietueiden kansikuva- ja kuvauslinkit eivät toimi, jos tietueessa on BTJ-linkki. Ongelma koskeen vanhempaa, noin 2014–2015, julkaistua aineistoa. 			Kirjavälityksen ja Bookyn linkit toimivat. Asiasta on kysytty Kirjastopalvelusta, mutta ei ole saatu vielä vastausta. [Lisäys muistioon 15.12. Annan sähköposti: Finnassa tilanne on korjattu, niin 		että Finna ei hae kuvaa/kuvausta BTJ:n linkistä vaan käyttää Kirjavälityksen linkkiä tai muuta lähdettä. Finnassa pitäisi siis näkyä kansikuvat ja kuvaukset oikein, vaikka Kohan paikalliskannoissa ei 	näy. Kohassa myös tiketti: <a href="https://github.com/KohaSuomi/Koha/issues/982" target="_blank">BTJ:n vanhojen linkkien korjaus</a>] </li>
</ul>

#### 5.	Koha-Suomen yhteinen bibliografinen tietokanta ####
<ul>
   <li>Paikalliskannat ja TäTi yhdistetään yhdeksi tietokannaksi</li>
   <li>Projekti alkaa vuoden 2024 aikana</li>
   <li>Koha-seminaarissa 28.11. sovittuja alustavia askelmerkkejä:</li>
	<ul>
		<li>RDA- ja YSO-konversiot niissä kannoissa, joissa niitä ei ole vielä tehty </li>
		<li>Paikalliskantojen siivous </li>
		<li>Selvitettävä, millaisia paikallisia erityistietokantoja on ja millaisia kirjastokohtaisia tietoja on kirjattu kuvailutietueisiin ja mihin kenttiin aikojen saatossa (jatkossa nämä tiedot 			ehkä niteisiin tai varastotietueisiin) </li>
	</ul>
</ul>
<ul>
   <li>Aikataulu ei vielä selvillä, mutta Koha-Suomen pääprojekteja</li>
   <li>Keskusteltiin aiheesta. Tietokantojen yhtenäistämisen kannalta tärkeintä on siivota paikalliskantoja. </li>
   <li>Paikalliskantojen siivouksessa tärkeintä on poistaa/yhdistellä tuplatietueita.</li>
   <li>Sovittiin, että jaetaan hyviä siivousvinkkejä, esim. raportteja.</li>
   <li>TäTistä löytyy joitakin tuplatietueita etsiviä raportteja, joihin pääkäyttäjillä pääsy. Anneli lisää raportit Koha-Suomen yhteiseen raporttikirjastoon, josta kimppojen pääkäyttäjät voivat siirtää ne paikalliskantoihinsa. Raportit ovat hitaita. Myös OUTIin on tehty erilaisia raportteja, joita voi tarvittaessa siirtää raporttikirjastoon.</li>
</ul>

#### 6.	MARC-virheellisten tietueiden korjausajot ja muut massakorjaukset ####
<ul>
   <li>Taulukko Marc-virheiden korjausehdotuksista</li>
   <li>Kaikille on tehty korjausajo: <a href="https://github.com/KohaSuomi/Koha/issues/931" target="_blank">Kiinteämittaisten kenttien korjaus: 008-MU/24–29 </a>, mutta se ei korjannut ihan kaikkia virheitä, vaan vain ne, joissa merkkijono alkaa |-merkillä.</li>
   <li><a href="https://github.com/KohaSuomi/Koha/issues/438" target="_blank">Vaski: Korjauksia osakohteiden aineistolajeihin (musiikkitallenne)</a> -> Onko muissa kimpoissa samoja ongelmia?</li>
</ul>
<ul>
   <li>Marc-virheiden korjausehdotus -taulukkoon kimpat voivat merkitä haluavatko korjausajon. Antti laittaa taulukon Koha Teamsiin ja lähettää taulukon ryhmälle sähköpostilla, jotta taulukkoa voi kommentoida.</li>
   <li>Vaskin tiketti ollut auki todella pitkään. Toivottiin, että korjausajopyyntöjä (ja muitakin kuvailutikettejä) käsiteltäisiin nopeammin.</li>
   <li>Pohdittiin kuinka pitäisi toimia, jos yksi kimppa tekee korjausajopyynnön ja muut eivät huomaa, että kaikkiin paikalliskantoihin tehdään korjaus. Sovittiin, että tiketteihin voi jokainen kimppa kommentoida tahtooko ajon vai ei. Pidetään kuvailuryhmä hyvin ajan tasalla uusista tiketeistä. Antin taulukko on hyvä ja ehkäisee sitä, että jollekin kimpalle jää ajo tekemättä.</li>
</ul>

#### 7.	Katsaus TäTin tietuepoistoihin ja -korjauksiin ####
<ul>
   <li>Melkein kaikki tarvittavat tietueet poistettu</li>
   <li>Jäljellä virheellisiä RDA-tietueita ja tuplatietueita</li>
   <li>Marc-virheellisiä tietueita vähän yli 2000 jäljellä</li>
</ul>

#### 8.	Tikettejä ####

<a href="https://github.com/KohaSuomi/Koha/issues/945" target="_blank">Nalkutin käyttöön jo tietojen tuontivaiheessa TäTiin</a>

#### 9.	Seuraava kokous ja ehdotuksia kevään kokouspäiviksi ####
<ul>
   <li>Tammikuun kokous on to 25.1. klo 13.15.</li>
   <li>Muita kokousaikoja ei vielä sovittu.</li>
</ul>

---
## Kuvailuryhmän muistio 8/2023

Aika: 8.11.2023 klo 13.15–14.45

Osallistujat: Mauri Aittaniemi (Lappi), Merja Hakulinen (Lumme), pj. Antti Heikkinen (OUTI), Pasi Hynninen (Helle), Suvi Kauranen (Kirkes), Päivi Knuutinen (Vaara), Marjukka Laapotti (Lastu), Risto Mikkonen (Vaski), Tarja Mäkinen (Kyyti), Marja Soisalo (Vaara) 

Poissa: Johanna Ranta (Kyyti), Anneli Österman (Koha-Suomi)

### Asialista ###

#### 1.	Kokouksen avaus ja sihteerin valinta ####

Kokous avattiin ja sihteeriksi valittiin Pasi Hynninen.

#### 2.	Lastu-kirjastojen edustaja ryhmään ####

Ryhmään uutena jäsenenä liittynyt Lastu-kirjastojen Marjukka Laapotti Lahden kaupunginkirjastosta toivotettiin tervetulleeksi ja suoritettiin lyhyt esittelykierros.

#### 3.	TäTin tietuepoistot ####
<ul>
  <li>Vanhoista KP:n kirjatietueista suurin osa on poistettu, mutta näitä listaavassa raportissa on joukossa on myös virheellisiä RDA-tietueita: esim. 040e-kentästä puuttuu RDA-merkintä. (RDA-merkintä löytyy useimmiten 040d-kentästä). Lisäksi raportilla näkyy 2023 muokattuja vanhoja tietueita (nimenmuutokset jne.). 
    - Päivi katsoo voiko asialle tehdä mitään (massakorjaus). </li>
	<li>Nyt on olemassa raportit myös äänitteille, nuoteille, videotallenteille, äänikirjoille ja elektroniselle aineistolle, mutta mukana ei pitäisi olla ISBD- eikä RDA-tietueita. Pohdittavaksi jää vielä äänitteiden ja nuottien osalta, kannatttaako niitä poistaa vai ei. </li>
	<li>TäTiin lisätty raportti, joka hakee tietueet, joissa ääkköset kummalliset. - Päivi on poistanut raportilla löytyneet tietueet jo. </li>
	<li>Mitä tehdään virheellisille tai vanhentuneille ”omille” TäTi-tietueille? 
    - Jokainen voi hakea näitä TäTistä kimppansa tai kirjastonsa ISIL-tunnuksella. Kannattaa hakea etenkin aiemmin käytetyillä tunnuksilla, jos niitä on käytetty (esim. FI-Rm, FI-Om, FI-Mm).</li>
	<li>Marc-virheelliset tietueet vähentyneet merkittävästi, tällä hetkellä vähän alle 5000 jäljellä, niistä yli 2000 884 5-osakentän sisältäviä tietueita. Saisiko tämän kentän pois raportilta, jottei se haittaisi korjauksia? 
    - Antti tiedustelee asiaa Annelilta.</li>
	<li>Todettiin, että poistot olisi hyvä tehdä ennen RDA- ja YSO-konversioita.</li>
</ul>

#### 4.	Koha-Suomi Melindaan -työryhmän kokous 24.10. ####
<ul>
  <li>RDA- ja YSO-konversiot tehdään nyt syksyn ja talven aikana, ei jäädä odottelemaan uutta RDA:ta</li>
	<li>TäTi-putki edistyy: nyt mahdollista tutkia päivittäisten uusien Kirjastopalvelun tietueiden siirtymistä Melindaan.</li>
	<li>Kokouksen jälkeen tehtyjä TäTi-putken testihavaintoja:</li>
 <ul>
  <li>Kirjastopalvelun korjaustietueet eivät aina yhdisty järkevästi Melinda-tietueeseen niissä tapauksissa, joissa KP ei korjaa tietueita itse Melindaan. Varsinkin kirjoitusvirheiden korjaus ei oikein onnistu, vaan näistä tulee tuplakenttiä. Myöskään esim. 250-kenttän lisätty painostieto ei siirry Melinda-tietueeseen, koska Melinda pitää tyhjääkin 250-kenttää painostietona.</li>
	<li>Melinda-tietuetta suositaan yleensä aina, joten Melinda-tietueen pääkirjaus säilyy, vaikka olisi virheellinen. Myöskään pääkirjauksen korjaus ei onnistu korjaustietueen kautta.</li>
	<li>Melindasta kysytty, voisiko erätuonnista erottaa tietueet, joiden pääkirjauksessa on eroja, mutta se ei onnistu, koska kyseessä on niin suuri työ, ettei siihen ole resursseja tällä hetkellä.</li>
	<li>Osa tietueista ei siirry Melindaan ollenkaan, jos törmäävät siellä Melindan tuplatarkistuksiin. Melindasta kysytty, pystyykö päivittäisistä tai yhden paketin ei-yhdistettävistä tietueista saamaan jotakin erillistä listausta/raporttia. Vastaus: Erätuonti saa niistä restiltä infon, mutta se miten sitä infoa käsitellään, vaatii miettimistä.</li>
	<li>Kirjastopalvelun tietue siirtyy Melindan ennakkotietueen päälle suhteellisen hyvin. Ainoastaan jotkin lisätekijä- ja sarjakentät voivat muodostua tuplakentiksi, jos niiden tiedot eroavat toisistaan.</li>
	<li>Jatkoon pohdittavaksi: mitä Kirjastopalvelun korjaustietueille pitäisi tehdä?</li>
  </ul>
	<li>Johanna on rakentanut TäTiin toiminnon, joka lisää Kirjastopalvelun toimittamiin osakohteisiin 035a-kentän ((FI-BTJ)xxxxx) aamuisten erätuontien yhteydessä. Tämä toiminto on jo päällä. Tarkoitus on jossain vaiheessa muuttaa tietueiden täsmäytyskentäksi 035a eikä 001- ja 003-kentän yhdistelmä.</li>
	<li>Melinda-koulutusta koko Koha-Suomen kuvailijoille keväällä 2024 (toukokuu)? - Helle-kirjastot olivat kyselleet koulutusta. Melinda periaatteessa suostuvainen, mutta haluaisivat koko Koha-kirjastojen laajuista koulutustapahtumaa. Päätettiin, että kukin kimppa tahollaan miettii millaista oppia tarvitsevat.</li>
  <li>Seuraava Koha-Suomi Melindaan -työryhmän kokous 24.1.2024</li>
</ul>

#### 5.	Paikalliskantojen siirtoraportin korjaus- ja kehitysehdotuksia (jatkoa edellisestä kokouksesta) ####
<ul>
  <li>Uudesta Vaski-kirjastojen kehittämästä uutuustietueiden seuraamiseen tarkoitetusta SQL-raportista huolimatta totesimme siirtoraportin tarpeellisuuden edelleen (tietueiden valutushistorian näkeminen, keskeytyneet, aktivoinnin tarkistaminen).</li>
	<li>Kannatimme vahvasti ajatusta kehittää Kohaan uusi SQL-raportti muutostietueiden seurantaan. Raportissa olisi tärkeää näkyä etenkin ne tietueet, joiden muutokset vaikuttavat tarroihin (kentät: 084, 1XX, 245, mahd. 300). Antti laatii alustavan luonnoksen siitä, miten raportin pitäisi toimia ja mitä sillä pitäisi näkyä, ja lähettää sen Kohan pääkäyttäjille.</li>
	<li>Siirtoraportin kehittämiseksi ehdotettiin esim. värikoodeja sekä aineistolajin, nimekkeen ja tyypin (lastenaineisto vaiko aikuisten) ilmaisemista ilman klikkauksia.</li>
	<li>**Lisäys 14.11: ** Kokouksen jälkeen tullutta uutta tietoa: Valutustoiminto muuttuu lähiaikoina, mikä vaikuttaa myös siirtoraportin ulkomuotoon. Lisää asiasta tiketissä: <a href="https://github.com/KohaSuomi/Koha/issues/915" target="_blank">Valutuksen siirtäminen broadcast biblios liitännäiselle.</a> </li>
</ul>

#### 6.	Koha-Suomeen on perustettu uusi tiedonhaku- ja indeksointityöryhmä #####

Ryhmälle osoitetut tiketit löytyvät GitHubin Tikettien seurannan kautta.

#### 7. Uusia tikettejä ####
<ul>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/844" target="_blank">Osakenttään 942b merkitty valutuksen esto ei aina toimi</a> </li>
	<li><a href="https://github.com/KohaSuomi/Koha/issues/475" target="_blank">Osakohteiden näkyminen, jos niiden 245a-kentässä ei ole mitään</a> -> Tämä on saatu toimimaan nyt, mutta edelleen jää pohdittavaksi, pitäisikö ne tietueet korjata jotenkin, joilta puuttuu nimeke 245-kentästä. </li>
	<li><a href="https://github.com/KohaSuomi/Koha/issues/580" target="_blank">Tietueen kuvailun virheilmoituksen Mene kenttään -linkki ei toimi</a> </li>
	<li><a href="https://github.com/KohaSuomi/Koha/issues/901" target="_blank">TäTin proxy Error</a> </li>
	<li>Redminestä on myös siirretty vanhoja tikettejä GitHubiin</li>
</ul>

#### 8.	Muita asioita ####
<ul>
  <li>YKN:n metatietoryhmän kokous 7.11.2023: Metatietoprojektin jatkoprojekti hidastuu, koska Melindan alusta ei vaihdu uuteen vielä vuonna 2025.</li>
  <li>Kansalliskirjaston osaamiseen liittyvä tulevaisuustyöpaja järjestetään 15.11., ja YKN: metatietoryhmän jäsenet ovat saaneet siihen kutsun.</li>
  <li>Mikropalvelun käyttäjätunnuksissa olleet kytkentävirheet on saatu korjattua.</li>
</ul>

#### 9.	Seuraava kokous torstaina 14.12. Klo 13.15 ####


---
## Kuvailuryhmän muistio 7/2023

Aika: 18.10.2023 klo 13.15–14.45

Osallistujat: Mauri Aittaniemi (Lappi), Merja Hakulinen (Lumme), pj. Antti Heikkinen (OUTI), Pasi Hynninen (Helle), Sani Kuosmanen (Kirkes), Päivi Knuutinen (Vaara), Tarja Mäkinen (Kyyti), Marja Soisalo (Vaara), Anna Viitanen (Vaski), Anneli Österman (Koha-Suomi)

Poissa: Johanna Ranta (Kyyti)

### Asialista ###

#### 1.	Kokouksen avaus ja sihteerin valinta ####

Sihteeriksi valittiin Mauri Aittaniemi Rovaniemen kaupunginkirjastosta.

#### 2.	Melindassa tehtävät massakorjausajot ja vastaavat korjaukset TäTissä ja paikalliskannoissa ####
<ul>
  <li><a href="https://www.kiwi.fi/display/kumea/2023-09-06" target="_blank">Kumean muistio 6.9.2023:</a> </li>
<ul>
  <li>Kohta 3.1. sidottu -> kovakantinen, nidottu -> pehmeäkantinen </li>
  <li>Kohta 3.3. 246i-osakenttien korjaus ja päivitys. TäTin auktorisoitujen arvojen valikko on nyt ajan tasalla. Fraaseja on poistettu Kumean <a href="https://www.kiwi.fi/display/kumea/Metatietosanastosta+poistetut+fraasit" target="_blank">listauksen</a> mukaan. Miten nämä pitäisi tehdä tietokannassa, esim. kansinimeke merkitään nykyään indikaattoreilla? </li>
</ul>
  <li><a href="https://www.kiwi.fi/display/kumea/2023-09-27" target="_blank">Kumean muistio 27.9.2023:</a> </li>
<ul>
  <li>3.1. Kentässä 588 on käytetty fraasia "Osan numero irtopäällyksestä"; näin ei kuitenkaan pitäisi tehdä. (Anna kertoi, että tämä asia on menossa vielä uudelleen käsittelyyn Kumeassa)</li>
  <li>3.2. Poistetaanko Disney, Walt -kirjaukset 100- ja 700-kentistä?</li>
</ul>
  <li>Muita Melindassa viime aikoina tehtyjä muutoksia <a href="https://www.kiwi.fi/display/melinda/Talonmies+tiedottaa+10.10.23" target="_blank">Talonmiehen kirjeessä:</a> ”Jos Metatietosanastosta poistettuja ja Melindassa korjattuja fraaseja ei korjata paikalliskannoissa, ne näkyvät helposti väärin Finnassa ja valuvat kenties takaisin Melindaan.”</li>
</ul>

Kaikenlaisia korjauksia alkaa olla kertynyt (ja kertyy jatkossakin) jo siinä määrin, että voisi olla hyvä kehittää jonkinlainen suunnitelma näiden käsittelemiseksi. Korjauksia pitäisi tehdä, koska paikalliskantojen virheet näkyvät Finnassa. Osan korjauksista voi tehdä Tietueiden muokkaus eräajona -toiminnolla, mutta osaan vaaditaan kehittäjien apua. Kehittäjien tehtäväksi annettavista korjausajoista pitää laatia selkeä tiketti aina yhdestä asiasta kerrallaan. Tiketissä pitää mainita, mitä pitää tehdä ja mihin kaikkiin tietokantoihin. Kätevintä olisi korjata tietueet ensin TäTissä ja sieltä korjatut valuisivat paikallistietokantoihin, mutta korjattavia tietueita jää tästä huolimatta vielä paikalliskantoihinkin, koska kaikkia tietueita ei ole TäTissä.

**Päätös:** Laaditaan Excel-taulukko korjattavista asioista ja määritellään siihen priorisointijärjestys eri korjausajoista. Antti tekee taulukon pohjan. 

TäTistä tulisi lisäksi siivota pois vanhentuneita tietueita. Siellä on (kokousta pidettäessä) muun muassa 325 000 monografiatietuetta ilman RDA-tietoa sekä äänite- ja videotietueita ajalta ennen ISBD:tä. Siivotessa voisi samalla luopua näistä. Anneli on tehnyt TäTiin eri raportteja, joiden avulla tietueita voi poistaa. Raporteilla voi poistaa 1000 tietuetta kerrallaan. Kysyttiin, onko kaikilla oikeus tehdä TäTiin eräpoistoja. Ilmeni että oikeuksia ei kuvailuryhmäläisillä ollut, mutta Päivi Knuutinen lupasi lisätä eräpoisto-oikeudet Anna Viitaselle ja Mauri Aittaniemelle. Lisää halukkaita voi ilmoittautua Päiville. Vanhentuneiden tietueiden poiston jälkeen TäTin tietueiden käsittely helpottuisi.

#### 3.	Kuulumisia Kirjastopalvelun asiakasohjausryhmän kokouksesta 3.10. ####

Kirjastopalvelun ilmoittama, uusi kuvailuun liittyvä periaate kolmesta kirjastokimpan tilauksesta herätti hieman keskustelua. Kirjastopalvelu kuvailee jatkossa ensisijaisesti tuotteet, joita on tilannut vähintään kolme kirjastokimppaa. Kokouksessa muistutettiin Extranetin olemassaolosta ja palautteen jättämismahdollisuudesta.

#### 4.	Monikielisen kirjaston siirtokokoelmat eri kirjastoissa ####

Kysymys Oulusta muille kirjastoille: Tilaatteko aineistoa Monikielisestä kirjastosta siirtokokoelmaksi ja miten toimitte Kohassa niiden kanssa?

Monikielisten siirtokokoelmien suhteen Koha-Suomen kirjastoissa on erilaisia käytäntöjä, ja osalla näitä pääkaupunkiseudulta tulevia siirtokokoelmia ei ole ollenkaan. OUTI-kirjastoissa siirtokokoelmien teosten tietueet poimitaan paikalliskantaan ja korjataan. Teokset voivat käydä siirtona useammankin kerran, mikä tarkoittaa että sama tietue poimitaan ja muokataan silloin monta kertaa. Siirtokokoelmia käytetään myös ainakin Helle-, Lumme- ja Vaski-kirjastoissa. Yleensä tapana vaikutti olevan, että poimittuja tietueita ei muokata siirtokokoelman tuontia varten. Tarpeettomat tietueet tulee joka tapauksessa poistaa järjestelmästä, kun teokset palautetaan monikieliseen kirjastoon.

#### 5.	Valutus TäTistä paikalliskantoihin ####

OUTIssa on viime aikoina ollut aika paljon ongelmia aamuisten valutusten kanssa. Tietueet jäävät valumatta Internal server errorin takia. Vaski-kirjastojen osalta Anna Viitanen kertoi, että osa Kirjastopalvelun tietueista on jäänyt valumatta järjestelmään. Vaski-kirjastoissa on kehitetty kätevä raportti, josta näkee viimeisen vuorokauden aikana ennakkotietueiden päälle valuneet TäTin tietueet. Kyseinen raportti löytyy nyt Koha-Suomen yhteisestä <a href="https://koha-suomi.fi/dokumentaatio/raporttikirjasto/" target="_blank">raporttikirjastosta</a>, josta kimppojen pääkäyttäjät voivat lisätä sen omien paikalliskantojensa raportteihin.

#### 6.	Finnan toimijanimien rikastustoiminto ####
<ul>
  <li>OUTI-Finnan haravointiasetuksista piti pyytää laittamaan MarcAuthEnrichment-toiminto päälle, jotta toimijanimien rikastustoiminto toimii OUTIssa. Asiasta tarkemmin Finnan sivuilla: <a href="https://www.kiwi.fi/display/Finna/Tietueiden+rikastus+Finnan+indeksiin" target="_blank">Tietueiden rikastus Finnan indeksiin</a> </li>
  <li>Onko muilla toiminnassa? </li>
</ul>

Vaskissa on yritetty laittaa päälle, mutta ei ole onnistunut. Antti kehotti selvittämään kirjastokimpoittain, onko rikastustoiminto otettu käyttöön.

#### 7.	Paikalliskantojen siirtoraportin korjaus- ja kehitysehdotuksia ####

Nyt kun Johanna Räisä on tullut takaisin, niin siirtoraporttiin voisi pyytää joitakin parannuksia. Aiemmin on ainakin keskusteltu siitä, että sellaiset tietueet, joissa on vain muuttunut 005-kentän aikaleima, voisi karsia pois raportista.

005-kenttä sisältää aikaleiman. Jos tietueessa ei ole muutettu mitään, vain tallennettu, silloin ainoa raportissa näkyvä muutos on muuttunut aikaleima. Keskusteltiin, että aikaleimalliset muutokset voisi jättää pois raportista. Tämä helpottaisi ja nopeuttaisi siirtoraportin läpikäymistä. Mietitään lisää parannusehdotuksia seuraavaan kokoukseen.

#### 8.	Tikettejä, joissa on tapahtunut jotakin edistystä: ####
<ul>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/807" target="_blank">Valutus: Viivalliset ISMN-tunnukset eivät valu TäTistä paikalliskantaan</a> </li>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/592" target="_blank">Tietueen tuominen TäTistä Vaaraan ei tuo oikeaa tallennuspohjaa</a> </li>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/750" target="_blank">Finna-aineistotyyppi äänikirja myös Kohan aineistotyypiksi/MTYPE:ksi</a> </li>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/390" target="_blank">YSA-YSO-konversio kaikille kimpoille</a> </li>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/834" target="_blank">RDA-konversio kaikkiin kimppoihin, joissa sitä ei ole tehty</a> </li>
  <li>Nalkutin on asennettu takaisin TäTiin, mutta edelleen on ongelmana: <a href="https://github.com/KohaSuomi/Koha/issues/458" target="_blank">Tuplatietue TäTissä, kun yrittää muokata tietuetta</a> </li>
</ul>

#### 9.	Muita asioita ####
<ul>
  <li>Koha-seminaari järjestetään Keravalla 28.11. n. klo 10–16. Aiheena tulee olemaan mm. kuvailu, Bibframe, linkitetty data. <a href="https://github.com/KohaSuomi/Koha/discussions/850" target="_blank">Ohjelma ja ilmoittautuminen</a> </li>
  <li>Elasticsearch-koulutus ke 1.11. klo 13 (Anneli Österman pitää).</li>
</ul>
Suositeltiin osallistumista molempiin.

#### 10.	Seuraava kokous keskiviikkona 8.11. Klo 13.15 ####


---
## Kuvailuryhmän muistio 6/2023

Aika: 13.9.2023 klo 13.15–14.30

Osallistujat: Merja Hakulinen (Lumme), pj. Antti Heikkinen (OUTI), Pasi Hynninen (Helle), Suvi Kauranen (Kirkes), Päivi Knuutinen (Vaara), Tarja Mäkinen (Kyyti), Marja Soisalo (Vaara), Anna Viitanen (Vaski), Anneli Österman (Koha-Suomi)

Poissa: Mauri Aittaniemi (Lappi), Johanna Ranta (Kyyti)

### Asialista ###

#### 1.	Kokouksen avaus ja sihteerin valinta ####

Sihteeriksi valittiin Merja Hakulinen. Mauri Aittaniemen sihteerivuoro on seuraavassa kokouksessa.

#### 2.	Osakohteiden aineistotyyppien muodostumisen ongelmat #####

Osakohteiden aineistotyypit siirtyvät huonosti tietueisiin. Ehdotettiin tietokanta-ajoa säännöllisin väliajoin, jolloin virheellisiä osakohteita ei tarvitsisi etsiä itse. Sellainen ajo on olemassa, joka ottaa aineistotyypit kiinteistä kentistä 942-kenttään. Päivi Knuutinen tekee tukipyynnön, jotta tietokanta-ajolla saadaan osakohteille oikeat aineistotyypit. Kaikki aineistotyypit eivät ehkä tule tietokanta-ajosta huolimatta oikein, kuten Blu-ray-äänilevy (kiinteissä kentissä CD:n arvot). Aineistotyypit vaikuttavat myös OKM:n pyytämiin tilastointeihin.

Kokouksen jälkeen lisätty tiketti: <a href="https://github.com/KohaSuomi/Koha/issues/776" target="_blank">Aineistotyypittömien osakohteiden korjausajo</a>

#### 3.	Kuvailuun liittyvät keskeneräiset tiketit ja versiopäivityksistä johtuvat korjaukset ####
<ul>
  <li>Tiketeistä huolimatta Nalkuttimen toiminta ja osakohteiden aineistotyyppien korjaukset eivät etene. Nalkutin ei toimi TäTissä eikä se ilmoita kuvailussa olevista virheistä. Kokouksen aikana tuli tieto, että Nalkutin on jo testi-TäTissä, mutta sitä pitää vielä testata.</li>
  <li>Aikaisemmin hyvin toimineet asiat toimivat nyt huonommin, koska versiopäivityksessä pois jääneitä toimintoja ei ole korjattu tai laitettu vielä päälle.</li>
  <li>Kohan kehittäjät voisivat huolehtia tiketeistä järjestelmällisemmin ja nopeammin, jotta korjaukset kuvailijoiden työvälineisiin saataisiin kohtuullisessa ajassa.</li>
  <li>Ehdotus asioiden jouduttamiseksi: Kirjastokimppojen palvelupäälliköt ottaisivat suoraan yhteyttä vastaaviin tahoihin ja vaatisivat toimenpiteitä (toimitusjohtaja, hallitus, asiantuntijaryhmä).</li>
</ul>

#### 4.	Tietueiden käsittely TäTissä ####
<ul>
  <li>Muistakaa viedä Melindasta tuodut tietueet aina takaisin Melindaan, jotta päivitysyhteys pysyy. Muuten tietueet eivät pysy ajan tasalla ja voi käydä niin, että muokataan vahingossa vanhentuneita tietueita turhaan.</li>
  <li>Koska Nalkutin ei toimi tällä hetkellä, muistakaa laittaa oikeat indikaattorit. Huomatkaa varsinkin kenttä 648, jossa YSO-aika-plugin ei aseta indikaattoria automaattisesti, vaan indikaattori on laitettava käsin. Kentässä 2. indikaattori on joko 4 tai 7.</li>
  <li>TäTissä on edelleen paljon Koha-Suomen kirjastojen kuvailemia tai muokkaamia tietueita, joissa on MARC-virheitä. Näitä voisi korjailla oman kimpan käsittelemien tietueiden osalta silloin kun aikaa on tai poistaa tietueet ehkä kokonaan, jos ne ovat jo vanhentuneita. Oman kimpan virheellisiä tietueita voi hakea virheellisten tietueiden listasta selaimen Find-toimintoa käyttämällä omalla ISIL-tunnuksella: <a href="https://tati.koha-suomi.fi/marc_virheet.tatiprod.html" target="_blank">TäTin virheelliset tietueet</a> </li>
</ul>

#### 5.	Marc-virheraportin korjausajot ####

Antti Heikkinen on tehnyt taulukon korjausehdotuksista. Kaikilla on nyt kiireistä, joten asiaan palataan tämän vuoden lopulla. Ensin korjataan tiedonhakuun vaikuttavat ongelmat. Tietueiden korjausajo pitäisi tehdä niin, etteivät tietueet aktivoidu valutukseen eikä niiden aikaleimankaan tarvitsisi ehkä muuttua. Korjaukset olisi hyvä tehdä ennen seuraavia konversioita (esim. RDA) tai tietokantojen mahdollisia yhdistämisiä.

#### 6.	TäTin ja Melindan eri ohjeiden päivitys Koha Teamsin Kuvailukanavalle ####
<ul>
  <li>Koha Teamsin Kuvailukanavalta löytyvät päivitetyt kuvailuohjeet. Sekä uudet että vanhat kuvailijat tarvitsevat ohjeita.</li>
  <li>Kirjastopalvelun maaliskuussa 2023 julkaisemassa tiedotteessa kerrotaan, että ukrainan- ja venäjänkielisen aineiston translitterointi tehdään kokonaan Kansallinen standardi SFS 4900:lla. Sitä aiemmin heillä on ollut tapana laittaa päänimeke 246-kenttään ISO 9 standardilla. Seurataan, vieläkö tämä käytäntö jatkuu. Antti muokkaa tämän kohdan päivitettyyn TäTi-ohjeistukseen.</li>
  <li>Kuvailuohjeita löytyy vielä Redminesta, josta ne siirretään GitHubiin.</li>
</ul>

#### 7.	Koha-Suomi-Melinda-työryhmän kokous 23.8. ####
<ul>
  <li>TäTi-putken rakennus edistyy. Tällä hetkellä mietitään, miten saataisiin Kirjastopalvelun tietueiden päiväpaketit kätevimmin TäTistä Melindaan niin, että replikointiyhteys säilyy (Melinda-ID ja TATI-Low-tag). Koska Helmetistä on jo aiemmin siirretty KP:n tietueita, niin tämänhetkisen katselmuksen perusteella tietueiden vienti ja yhdistyminen Melinda-tietueisiin näyttää aika hyvältä.</li>
  <li>Pahimmat Helmetin eräajojen virheet on nyt korjattu. Tietueita voi nyt korjata itse, mutta jos huomaatte joitakin edelleen toistuvia virheitä, niin Melindaan voi ilmoittaa.
Helmetin tietueissa olevat kirjoitusvirheet tulevat edelleen tuplakenttinä, eivätkä välttämättä korjaannut, ellei Helmet itse hoksaa niitä korjata.</li>
  <li>Johanna Räisä palaa töihin 18.9. Sen jälkeen ehkä vihdoin päästään eteenpäin RDA- ja YSO-konversioissa ja muussa valutukseen ja Melindaan liittyvässä kehitystyössä.</li>
  <li>Seuraava kokous 24.10. Klo 14.00.</li>
</ul>

#### 8.	Uusia tikettejä ####
<ul>
  <li>Kuvailupohjat eivät ole tällä hetkellä ajan tasalla. Pohjien viimeisin MARC-formaatin päivitys on ollut kesällä 2021. Sen jälkeen on tullut ainakin jo kolme päivitystä, joista viimeisin kesäkuussa 2023. Tähän liittyy tiketit:</li>
<ul>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/256" target="_blank">[Tukipyyntö] Kuvailupohjien automaattinen päivitys</a> </li>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/747" target="_blank">Kuvailupohjat eivät ole päivittyneet automaattisesti</a> </li>
</ul>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/718" target="_blank">Osakentän 775t lisääminen title-hakukenttään</a> </li>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/750" target="_blank">Finna-aineistotyyppi äänikirja myös Kohan aineistotyypiksi/MTYPE:ksi</a> </li>
</ul>

#### 9.	Muita asioita ####
<ul>
  <li>Kirkes-kirjastojen koulutukset</li>
<ul>
  <li>RDA-koulutukset 4. & 5.9.</li>
  <li>Kohan kuvailutyökalujen koulutus 7.9. (Anneli) & 21.9. (Antti)</li>
  <li>Melindan käyttöönottokoulutus 4.10.</li>
  <li>Kirkes-kirjastojen liittyminen on sujunut hyvin. He aloittavat kuvailun 4.10. jälkeen. Valutus alkaa ehkä Antin koulutuksen 21.9. jälkeen, mutta vaatii kehittäjiltä vielä säätämistä ja testaamista.</li>
</ul>
  <li>Kirjastopalvelun asiakasohjausryhmän kokous 3.10.</li>
<ul>
  <li>Antti ja Anna osallistuvat asiakasryhmän kokoukseen.</li>
  <li>Keskustelussa ilmeni seuraavia kysymyksiä:</li>
<ul>
  <li>Miksi kuvailu on niin hidasta? Suomenkielisessäkin aineistossa kestää välillä tosi kauan.</li>
  <li>Onko eri aineistoilla työnjako tai kiireellisyys-/ruuhkautumisjärjestys? Jos jotakin aineistolajia kertyy paljon, siirretäänkö tähän enemmän resursseja?</li>
  <li>Miksi Extranet-pyynnöt viipyvät?</li>
  <li>Millä perusteella vieraskielinen aineisto kuvaillaan tai ei kuvailla (esim. saman tekijän kirjat, lisäpakettitilauksesta huolimatta)?</li>
</ul>
  <li>Muita huomioita:</li>
<ul>
  <li>Helle-kirjastojen kokemus lastenkirjallisuuden kuvailun viipymisestä</li>
  <li>Ensi vuoden alusta lähtien kolmella eri kirjastokimpalla pitää olla Kirjastopalvelun tilaus kyseisestä aineistosta, jotta aineisto kuvaillaan.</li>
  <li>Nyt jo Kirjastopalvelu ilmoittaa, ettei liian vähälevikkistä aineistoa kuvailla.</li>
  <li>Kirjastopalvelu kuvailee vieraskielistä aineistoa myös suoraan ulkomaisten tietokantojen avulla, eli kuvailukappaleita ei ole heidän saatavillaan.</li>
</ul>
</ul>
<li>Lastu-kirjastot (Asikkala, Hartola, Heinola, Hollola, Kärkölä, Lahti, Orimattila, Padasjoki ja Sysmä) liittymässä Koha-Suomeen todennäköisesti syksyllä 2024.</li>
<li>TäTiin on lisätty kuvailupohjien 003-kenttään liitännäinen, joka lisää kenttään FI-TATI-tunnuksen kenttää klikkaamalla, silloin kun kyseinen kenttä on tyhjä.</li>
</ul>

#### 10.	Seuraavat kokousajat ####
<ul>
  <li>Ke 18.10. klo 13.15</li>
  <li>Ke 8.11. klo 13.15</li>
  <li>To 14.12. klo 13.15</li>
</ul>


---
## Kuvailuryhmän muistio 5/2023

Aika: 24.5.2023 klo 13.00–13.35

Osallistujat: Merja Hakulinen (Lumme), pj. Antti Heikkinen (OUTI), Pasi Hynninen (Helle), Suvi Kauranen (Kirkes), Päivi Knuutinen (Vaara), Tarja Mäkinen (Kyyti), Johanna Ranta (Kyyti), Marja Soisalo (Vaara), Anna Viitanen (Vaski), Anneli Österman (Koha-Suomi)

Poissa: Mauri Aittaniemi (Lappi)

### Asialista ###

#### 1.	Kokouksen avaus ja sihteerin valinta ####

Sihteeriksi valittiin Anna Viitanen.

#### 2.	Versionvaihtokuulumiset #####

Versionvaihdon jälkeen kuvailu on toiminut ilman suuria ongelmia. Tausta-ajoissa on ollut hitautta, minkä takia osakohteiden tallentumisessa paikalliskantoihin kestää välillä tavallista pidempään. Vie/tuo -napin klikkauksen jälkeen kannattaa odottaa rauhassa osakohteiden tallentumista. Tausta-ajojen hitaudesta on tehty tiketti: <a href="https://github.com/KohaSuomi/Koha/issues/582" target="_blank">Taustatöissä hitautta</a>

OUTIssa oli ongelmia Kohan pluginien, kenttien toistamisen ja poistamisen kanssa Firefoxin vanhempaa 78-versiota käytettäessä. Tiistain päivitys poisti ongelmat. Lisäksi helatorstaina ja viikonloppuna valui OUTIn vanhojen tietueiden päälle tietueita ilman selvää syytä: <a href="https://github.com/KohaSuomi/Koha/issues/583" target="_blank">TäTistä valunut vanhojen tietueiden päälle tietueita ilman kenenkään käsittelyä</a>

Päivi kaipaa kommentteja Koha-Suomen ohjeiden kuvailua koskevaan kohtaan. Keskusteltiin siitä, kannattaako Mikropalveluun liittyvät ohjeet ottaa osaksi kuvailuohjetta, vai olisiko niiden parempi olla (linkin takana) GitHubissa. Sovittiin, että katsotaan ohjeet läpi ja lähetetään kommentit/korjausehdotukset Päiville viimeistään 31.5.

<https://koha-suomi.fi/dokumentaatio/kuvailu/>

#### 3.	TäTin Finto-liitännäisten toiminta uudessa versiossa ####

Asiasanakenttiä toistettaessa liitännäinen pitää aktivoida a-osakentän oikeassa laidassa olevasta editorinapista. Asteri-liitännäinen ei aluksi toiminut kenttiä toistettaessa, nyt sekin on jo saatu toimimaan.

<p> <a href="https://github.com/KohaSuomi/Koha-22x/issues/22" target="_blank">Finto-plugit - ksdev/ks-0070-KD-4590-Finto-value-builders</a> </p>
<p> <a href="https://github.com/KohaSuomi/Koha-22x/issues/182" target="_blank">finto_finaf.pl -pluginin toimintojen alustusfunktiot</a> </p>

#### 4.	Kehitysehdotus ####

024-kenttään pitäisi saada samanlainen väliviivat pudottava tietokantatriggeri kuin on 020-kentässäkin. Näin nuottien valutus toimisi paremmin. Antti tekee tästä kehitysehdotuksen.

#### 5.	Ongelma 880-kenttiä sisältävien tietueiden viemisessä TäTistä Melindaan ####

Jos Melinda-tietueessa on Alephille ylipitkä 880-kenttä (yleensä tiivistelmä), Koha ei osaa näyttää sitä oikein, mikäli ylipitkä kenttä on katkottu väärin Alephissa. Jos tällaista tietuetta muokkaa TäTissä ja vie muutoksen Melindaan, tietue palautuu takaisin oudon näköisenä, koska 880-kentän 6-osakenttä ja a-osakenttä eivät kuulu enää samaan 880-kenttään vaan ovat tietueessa omina toistuminaan. Ongelma korjaantuu yleensä sillä, että tuo tietueen uudestaan Mikropalvelulla Melindasta.

Esim. Melinda-tietue 018727852

<p>Tietue Melindassa:</p>
<p>880 8 	|6 520-08/(N </p>
<p>880 8 	|9   </p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|a "Мне самому </p>


<p>Tietue TäTissä oikeassa muodossa:</p>
<p>880 8 	|6 520-08/(N </p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;|a "Мне самому </p>


Liittyy tähän: <a href="https://www.kiwi.fi/pages/viewpage.action?pageId=191070355" target="_blank">Ylipitkät kentät Alephissa ja Melindassa - Melinda - kansallinen metatietovaranto - Yleinen sivusto (kiwi.fi)</a>

Antti selvittelee vielä, onko ongelma Mikropalvelussa ja/tai voitaisiinko Melindan päässä tehdä näille tietueille jotakin.

#### 6.	Uusi tiketti ####

Osakohteiden päälle valui Vaskissa vääriä tietoja: <a href="https://github.com/KohaSuomi/Koha/issues/527" target="_blank">Osakohteiden päälle valunut väärät tiedot</a>

#### 7.	Muita asioita ####

<ul>
  <li>Kirkes-kirjastojen koulutus (RDA-koulutukset 4. & 5.9.) -> Onko tarvetta tarkistaa tai päivittää Kohaan ja TäTiin liittyviä kuvailuohjeita sitä ennen? </li>
  <li>Kohti metatietovisiota -projektin loppuraportti luettavissa: <a href="https://www.kirjastot.fi/sites/default/files/content/ykn_kohti_metatietovisiota_loppuraportti2023.pdf" target="_blank">Kohti metatietovisiota -selvitysprojektin raportointi</a>  </li>
  <li>Marc-virheraportteihin pääsee nyt käsiksi TäTistä/paikalliskannoista. Aikaisemmin raportteihin oli linkit Redminessä: <a href="https://github.com/KohaSuomi/Koha/issues/560" target="_blank">Redminessä olevat MARC-kuvailuvirheraportit eivät toimi enää</a> </li>
</ul>

#### 8.	Seuraava kokous 13.9. klo 13.15 ####


---
## Kuvailuryhmän muistio 4/2023

Aika: 19.4.2023 klo 13.15–14.45

Osallistujat: Mauri Aittaniemi (Lappi), Merja Hakulinen (Lumme), pj. Antti Heikkinen (OUTI), Pasi Hynninen (Helle), Suvi Kauranen (Kirkes), Päivi Knuutinen (Vaara), Tarja Mäkinen (Kyyti), Johanna Ranta (Kyyti), Marja Soisalo (Vaara), Anna Viitanen (Vaski)

Poissa: Anneli Österman (Koha-Suomi)

### Asialista ###

#### 1.	Kokouksen avaus ja sihteerin valinta ####

Sihteeriksi valittiin Marja Soisalo.

#### 2.	Kirkes-kirjastojen edustaja ryhmään ####

Käytiin ryhmäläisten esittelykierros ja Suvi Kauranen (Järvenpään kaupunginkirjasto) kertoi Kirkes-kimpan kuvailuasioista. 

#### 3.	Vuosisuunnitelma 2023 ####

Käytiin läpi Antin tekemät muutokset ja lisäykset. Antti lähettää päivitetyn version suunnitelmasta kuvailuryhmäläisille kommentoitavaksi.

#### 4.	Uuden TäTin asetukset ####

<ul>
  <li><a href="https://github.com/KohaSuomi/Koha-22x/wiki/Uutta#applyframeworkdefaults" target="_blank">ApplyFrameworkDefaults</a> </li>
  <li>Päätettiin valita luettelointipohjan oletusarvoista vaihtoehto ”uutta tietuetta kuvailtaessa” (when cataloguing new records).</li>
</ul>

#### 5.	Kuvailupohjien auktorisoitujen arvojen valikot ####

<ul>
  <li>Ongelmana se, että jos valikoissa ei ole kaikki arvot sekä ruotsiksi että suomeksi, niin ne kentät, joissa on termit molemmilla kielillä, saattavat tyhjentyä, kun tietueen muokkauksen yhteydessä vaihtaa oletuspohjasta johonkin toiseen pohjaan.</li>
  <li>Päätettiin lisätä kirjapohjaan ruotsinkieliset termit auktorisoitujen arvojen valikkoihin.</li>
  <li>Kirja (Ruotsi) -pohjalla kuvaillut tietueet siirretään kirjapohjalle jossain vaiheessa korjausajona.</li>
  <li>Kuvailijoiden kannattaa tehdä ruotsinkielisen aineiston kuvailu kirjapohjalla.</li>
</ul>

#### 6.	Muita asioita ####

<ul>
  <li>Edellisestä kokouksesta 22.3.: Ruotsinkielisen kaunokirjallisuuden asiasanojen järjestys tietueessa -> Siskusta ja Melindasta ei ollut apua, joten ongelma jää Finnan ratkaistavaksi.</li>
  <li>Fiktiivisen aineiston lisäluokan 084-kentässä ja kohdehenkilöiden tai -yhteisöjen nimet voi halutessaan suomentaa ruotsinkielisessä kaunossa.</li>
  <li>Siilijärvelle on saatu uusi kuvailija, mutta liittynee ryhmään vasta syksyllä.</li>
  <li>Löytyykö Koha-Suomen kirjastoista harvinaisempien vieraiden kielien osaajia kuvailijoiden avuksi (esim. japani, kiina, kreikka, arabia, turkki, ukraina, jne.)? Nimenomaan OUTIssa ja Vaskissa tarvetta harvinaisempien kielin osaamiselle.</li>
  <li>Jos Melindasta poimitun tietueen tallentaminen TäTissä ei onnistu sen takia, että jonkin kentän 5-osakenttä ei kuulu Marc-formaattiin, kannattaa olla yhteydessä pääkäyttäjiin, jotka lisäävät kentän Nalkuttimen asetuksiin.</li>
  <li>Seuraava Koha-Suomi Melindaan -työryhmän kokous 24.5.2023 Klo 14</li>
</ul>

#### 7.	Seuraava kokous keskiviikkona 24.5.2023 klo 13 ####


---
## Kuvailuryhmän muistio 3/2023

Aika: 22.3.2023 klo 13.15-14:34

Osallistujat: Helena Backman-Karvonen (Helle), Merja Hakulinen (Lumme), pj. Antti Heikkinen (OUTI), Päivi Knuutinen (Vaara), Tarja Mäkinen (Kyyti), Johanna Ranta (Kyyti), Marja Soisalo (Vaara), Anna Viitanen (Vaski), Anneli Österman (Koha-Suomi)

Poissa: Mauri Aittaniemi (Lappi)

### Asialista ###

#### 1.	Kokouksen avaus ja sihteerin valinta ####

Sihteeriksi valittiin Johanna Ranta.

#### 2.	Asiantuntijaryhmästä kysymys ####

Kehitysehdotus <https://tiketti.koha-suomi.fi/issues/4005> sisältää kuvailuryhmälle tehtävän: ”Kuvailutiedot - säännöllisesti toimiva automatiikka turhien niteettömien tietueiden ja emottomien osakohteiden poistoon halutuin säännöin (esim. rajataan toiminnosta pois tietyt aineistolajit). Turha niteetön tietue on hankala tunnistaa koneellisesti. Jos saadaan luotua hyvä säännöstö, niin sitten voidaan tehdä ajoja.” Pystytäänkö luomaan yhteinen sääntö, jonka mukaan turhat niteettömät tietueet voidaan siivota tietokannasta?

<ul>
  <li>OUTIssa säästettäviä niteettömiä nimekkeitä ainakin kausijulkaisuissa ja mikrofilmeissä,
Vaarassa kausijulkaisujen emot ja jotain verkkoaineistoja, Kyytissä e-kirjat ja e-äänikirjat, Hellessä Viddla-elokuvat. Vaskissa kaikki tyhjät tietueet ovat turhia tietueita </li>
  <li>Niteettömät tietueet voi poistaa ajolla, jos tietyt aineistolajit (verkkoaineistot, kausijulkaisut, mikrofilmit) rajataan sen ulkopuolelle </li>
</ul>

#### 3.	Ruotsinkielisen kaunokirjallisuuden asiasanojen järjestys ####

Helle-kirjastoista on tullut toive, että ruotsinkieliset asiasanat näkyisivät ensimmäisinä Finnan tietuenäytöllä ja sitten vasta suomenkieliset. Joissakin tietueissa suomenkieliset ovat ensimmäisinä, esim. Ragnar Jónassonin teos Utlämnad.
<ul>
  <li>Finnasta on kysytty asiasanojen järjestyksestä. Vastaus: ”Asiasanojen järjestys hieman vaikea säätää asetusmuutoksella tai ei näytä löytyvän asetusta, jolla voisi säätää järjestystä. Tuo kehitysehdotus on edelleen listalla.” </li>
  <li>Asiasanojen järjestykseen voi vaikuttaa lisäämällä suomenkieliset asiasanat vasta kaikkien ruotsinkielisten jälkeen, mutta tekevätkö kaikki Melinda-kirjastot niin. Osa kirjastoista ei lisää suomenkielisiä asiasanoja ruotsinkieliseen kaunokirjallisuuteen ollenkaan. </li>
  <li>Kyytissä lisätty suomenkieliset Kaunon asiasanat ensin, koska Melindan automatiikka lisää suomenkieliset YSO-, YSO-paikat-, YSO-aika- ja SLM-termit ruotsinkielisten edelle </li>
  <li>Helena kysyy Siskulta asiasanojen järjestyksestä </li>
  <li>Lisäys 29.3.: Asiasanojen järjestelyautomatiikasta kysytty Melindasta 22.3.: Lähtökohtaisesti järjestyksen säilyttämisestä ei luvata mitään, koska sen säilyttäminen on vaikeaa/monimutkaista. Esim. tietueiden massakorjausohjelma voi muuttaa järjestyksiä. Asiasanojen järjestystä on ohjelmoitu kuitenkin näin: ”yso/fin tulee ensin (ja niissä Fenni-keepatut ensin), sitten yso/swe, sitten on jotain ind2-pohjaisia sorttauksia ja viimeiseksi tulevat asiasanat, joiden ind2=4.” 655-kentässä on sama logiikka slm-sanaston osalta. Tietueiden välillä on kuitenkin paljon eroja riippuen siitä, mistä ne ovat Melindaan tulleet ja onko niitä käsitelty massakorjaimilla. </li>
</ul>

#### 4.	Aloittelevan kuvailijan vertaistukiryhmä/kanava Koha Teamsiin, mikä nimeksi? ####

Kanavan nimeksi tulee Kysy kuvailusta.

#### 5.	Kuulumisia Koha-Suomi Melindaan -työryhmän kokouksesta 21.3.2023 ####

<ul>
  <li>TäTi-Melinda putki edelleen vaiheessa, tällä hetkellä odotetaan lisää tietueiden katselmoijia </li>
  <li>Koha-Suomi tarkistaa, tarvitaanko Kirkes-kirjastoissa RDA-koulutusta. Pyydetään seuraavaan kuvailuryhmän kokoukseen edustaja myös Kirkes-kirjastoista </li>
  <li>Helmet-Melinda-erätuontiputken käyttöönoton aiheuttamia tuplakenttiä tietueissa ei kannata toistaiseksi korjata itse, koska korjaamattomat tietueet saattavat tulla takaisin uuden päivityksen myötä </li>
</ul>

#### 6.	Uusia tikettejä ####
 
<ul>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/348" target="_blank">Emottomien osakohteiden poisto ajona</a> </li>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/458" target="_blank">Tuplatietue TäTissä, kun yrittää muokata tietuetta</a> </li>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/454" target="_blank">Tilaustietueet eivät yhdisty aina oikein, kun 024a-kentästä tarkistetaan vain ensimmäinen osakenttä</a> </li>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/475" target="_blank">Osakohteiden näkyminen, jos niiden 245a-kentässä ei ole mitään</a> </li>
</ul>

#### 7.	<a href="https://github.com/KohaSuomi/Koha/issues/288" target="_blank">Tiketti 288: Signumbuilderista pois 130a-kenttä</a> ####

Tämä korjaantuu seuraavassa versiossa. Muistakaa testata, kun testaatte uutta versiota

#### 8.	Muita asioita ####

<ul>
  <li>Jos TäTissä tulee jotain ongelmia tietueiden viennissä tai tuonnissa Melindaan, jotka vaikuttavat valutuksen kautta paikalliskantoihin, niin olisi hyvä ilmoittaa Teamsissa, mitä on tapahtunut ja onko ongelma jo korjauksessa tai korjattu. Väärin valumiset näkyvät heti paikalliskantojen siirtoraportilla. Varsinkin osakohteellisten tietueiden kanssa on ylipäänsä oltava tarkkana.</li>
  <li>Toivottiin ruotsinkielistä kuvailupohjaa kirjoille -> Tehdään TäTiin, nimeksi Kirja (Ruotsi) </li>
  <li>Vuosisuunnitelma 2023: Käsitellään seuraavassa kokouksessa, Antti lähettää alustavan pohjan kommentoitavaksi sitä ennen. </li>
  <li>Seuraavassa kokouksessa käsiteltävänä myös uuden version kuvailupohjiin liittyvä järjestelmäasetus: <a href="https://github.com/KohaSuomi/Koha-22x/wiki/Uutta#applyframeworkdefaults" target="_blank">ApplyFrameworkDefaults</a> </li>
  <li>Koha-klinikka 29.3. </li>
</ul>

#### 9. Seuraava kokous keskiviikkona 19.4.2023 klo 13.15- ####


---
## Kuvailuryhmän muistio 2/2023

Aika: 22.2.2023 klo 13.15-14.20

Osallistujat: Mauri Aittaniemi (Lappi), Merja Hakulinen (Lumme), pj. Antti Heikkinen (OUTI), Pasi Hynninen (Helle), Päivi Knuutinen (Vaara), Johanna Ranta (Kyyti), Marja Soisalo (Vaara), Anna Viitanen (Vaski)

Poissa: Tarja Mäkinen (Kyyti), Anneli Österman (Koha-Suomi)

### Asialista ###

#### 1.	Kokouksen avaus ja sihteerin valinta ####

Puheenjohtaja Antti Heikkinen avasi kokouksen ja todettiin, että sihteerivuorossa on Päivi Knuutinen.

#### 2.	Melindan toimijanimimuutosten korjaukset TäTissä ja paikalliskannoissa ####

<ul> 
  <li>Edellisessä kokouksessa puhuttiin Kirjastopalvelun vanhojen (ajalta ennen RDA:ta) tietueiden poistamisesta TäTistä, jottei niitä tarvitsisi korjata, mutta on vaikea päättää sopivaa aikarajaa. Sovittiin, että mietitään mikä voisi olla sopiva ajankohta, jos tietueet päätetään poistaa, ja että toistaiseksi korjataan vain ne RDA-muotoiset tietueet, joita Kirjastopalvelu ei korjaa.</li>
  </ul>

Päätettiin selvittää, mikä määrä on kirjatietueita, joissa 003-kentässä on FI-BTJ ja 040e-kentässä ei ole RDA-merkintää. Nämä voitaisiin poistaa TäTistä. Kun TäTiin korjataan toimijanimiä, ei riitä pelkästään 100a-kentän korjaaminen, vaan täytyy korjata myös 500a- ja 900a-kentät sekä muutkin mahdolliset tietueessa olevat virheet. 

Lisäys 23.2.: Poistettavia tietueita (tekstiaineisto) on TäTissä 345 700 kpl.

Lisäksi huomioitiin, että Kansalliskirjasto näyttäisi korjaavan vain kirja-aineiston toimijanimet eikä esim. nuottien. Marja kyselee tästä Kansalliskirjastosta.
  
#### 3.	TäTin kuvailupohjat ja auktorisoidut arvot -valikot  ####
  
<ul>
  <li>Testi-TäTissä on ollut erilaisia valikkoja testattavana. Antti Heikkinen lähettää käyttöön otettavien valikkojen listauksen Päivi Knuutiselle TäTiin käyttöönotettavaksi.</li>
  <li>Joissakin valikoissa mukana vielä Metatietosanastosta otettuja ISBD-termejä. Kumean vuoden 2023 toimintasuunnitelmassa Metatietosanaston ISBD-termeistä:</li>
 <ul><li>i.	<a href="https://www.kiwi.fi/display/kumea/Kumean+toimintakertomus+2022+ja+toimintasuunnitelma+2023" target="_blank">Metatietosanaston termien tarkastaminen: ISBD-termien poistaminen ja uuden RDA:n termien lisääminen</a> </li></ul>
  
 Koska tämä on Kumeassa työn alla, jätetään odottamaan työn tulosta.</ul>
  
#### 4.	Uusi 020-kentän käytäntö: <https://wiki.helsinki.fi/pages/viewpage.action?pageId=455738956> ####
<ul>
  <li>Eri kansityypit kotimaisessa ja ulkomaisessa aineistossa -> Aiheuttaako toimenpiteiden muutoksia TäTi/Melinda-kuvailussa?</li>
  
  Toimitaan Kumean ohjeiden mukaisesti.</ul>
  
#### 5.	YSO-konversio, vanhentuneet/päivittyneet asiasanat ja Kohan tietueiden erämuokkaustyökalut ####
 
Tarkasteltiin Kohan erämuokkaustyökaluja. MARC-muokkauksen pohjien avulla voi tehdä erilaisia korjauksia ja lisäyksiä tietueiden eri kenttiin, paitsi ei kiinteisiin kenttiin tai kenttien indikaattoreihin. Hyviä ja käteviä tietueiden muokkaustoimintoja saa jakaa muillekin. YSO-konversiossa päivittyy vanhentuneet asiasanat nykyään käytettäviin termeihin suurimmilta osin.

#### 6.	Aloittelevan kuvailijan vertaistukiryhmä/kanava Koha Teamsiin? ####

Keskusteltiin vertaistukiryhmän tarpeellisuudesta ja osa kimpoista ilmoitti, että olisi tarpeen. Loput kimpat kyselevät vielä omilta kuvailijoiltaan tarpeellisuudesta. Lisäksi selvitetään, pystyykö Oulun Teamsissa muut kuin oman organisaation jäsenet avaamaan puheluyhteyttä, jos sellainen olisi käytännöllisempi tietyissä opastustilanteissa.

#### 7.	Koha-Suomi Melindaan -työryhmän kokous 25.1.2023 ####

<ul>
  <li>Kirjastopalvelun TäTi-tietueputki edistyy vähitellen, keväällä ehkä valmista </li>
  <li>Asterin uusi teos/ekspressiokanta (FIN13) -> ei saada ihan vielä käyttöön </li>
  <li>RDA- ja YSO-konversioita voisi alkaa työstämään versionvaihdon jälkeen </li>
  <li>Kirkes-kirjastojen Melinda-koulutus? Aikaisintaan syksyllä, koulutusmateriaali päivitettävä. </li>
  <li>Lisäksi työryhmän ulkopuolella on keskusteltu Melindan tämänhetkisestä tuplakontrollista, koska Celia-tietueet törmäävät taas useammin Melindassa oleviin e-äänikirjoihin. Rajapintapäivityksessä Melindan matcheri päivittyi ja muutos johtunee siitä. Tähän pyritään saamaan jonkinlaista parannusta Melindan päässä. </li>
  <li>Seuraava kokous 21.3.2023 </li>
</ul>

#### 8.	Uusia ja Redminesta siirrettyjä tikettejä: ####

<ul>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/429" target="_blank">Osakohteellisten tietueiden yhdistely ei poista osakohteita</a> </li>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/417" target="_blank">Helle: listaus tietueiden toimimattomista 856u-kentän linkeistä</a> </li>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/390" target="_blank">YSA-YSO-konversio kaikille kimpoille</a> </li>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/373" target="_blank">Finto-liitännäinen Metatietosanastosta</a> </li>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/352" target="_blank">TäTi: Z39.50-poiminta pudottaa 020-kentästä ISBN:n väliviivat</a> </li>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/350" target="_blank">Perustiedot-näytön puutteet</a> </li>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/348" target="_blank">Emottomien osakohteiden poisto ajona</a> </li>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/335" target="_blank">Työkalut, MARC-muokkauksen pohjat: kentän indikaattorien käsittelymahdollisuus</a> </li>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/333" target="_blank">Z39.50-tietueyhdistelyssä suojatut kentät eivät ole muokattavissa/poistettavissa. Lisäksi suojatun kentän muokkaus tallentuu uutena kenttätoistumana ja muokattu kenttä säilyy tietueella</a> </li>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/332" target="_blank">Tietueelta putoaa 942c-kenttä z39.50-haulla tietueita yhdisteltäessä</a> </li>
  <li><a href="https://github.com/KohaSuomi/Koha/issues/312" target="_blank">Helle: tietueelle massamuokkauksessa lisätty uusi kenttä ei näy kaikilla Koha-näytöillä/toiminnoilla oikealla paikalla. Koskee sekä jo tietueella olemassa olevan kentän uuden kenttätoistuman lisäystä että tietueelle lisättyä täysin uutta kenttää.</a> </li>
  <li>Kannattaa ottaa omaan seurantaan kiinnostavat tiketit. </li>
  </ul>

#### 9.	Muita asioita ####

<ul>
  <li>Valutuksesta: Jos siirtoraportin keskeytyneet-välilehdellä lukee tietueiden kohdalla ”Internal server error”, niin tämä saattaa usein viitata siihen, että tietokannassa on tuplatietue jostakin nimekkeestä, jolloin osakohteet ovat törmänneet toisiinsa. </li>
  <li>Finnaan on tullut uusi aineistotyyppi äänikirjoja varten, tuotantoon 3.3. alkaen. Myös Daisy-äänikirjoille on oma ikoninsa. Kohan kehittäjien asialistalla tarvittavia toimenpiteitä varten 23.2.2023. 
    
[Lisäys 24.2.] <a href="https://koha-suomi.fi/kohasuomi2023#torstain-2322023-klo-10-palaveri" target="_blank">Kehittäjien muistio 23.2.</a>: Toteutetaan Kohassa versiopäivityksen jälkeen.</li>
 </ul>
  
#### 10.	Seuraava kokous 22.3.2023 klo 13.15- #### 

Puheenjohtaja päätti kokouksen klo 14.20.


---
## Kuvailuryhmän muistio 1/2023

Aika: 18.1.2023 klo 13.15–14.30

Osallistujat: Mauri Aittaniemi (Lappi), Merja Hakulinen (Lumme), pj. Antti Heikkinen (OUTI), siht. Pasi Hynninen (Helle), Päivi Knuutinen (Vaara), Tarja Mäkinen (Kyyti), Johanna Ranta (Kyyti), Marja Soisalo (Vaara), Anna Viitanen (Vaski), Anneli Österman (Koha-Suomi)


### Asialista ###

#### 1.	Kokouksen avaus ja sihteerin valinta ####

Sihteeriksi valittiin Pasi Hynninen.

#### 2.	Melindan toimijanimimuutosten korjaukset ####

<ul>
  <li>Tietueet olisi hyvä korjata myös TäTissä, jotta ne olisivat ajan tasalla. Miten tämä olisi järkevintä tehdä/organisoida?</li>
  <li>Kirjastopalvelu päivittää viisi vuotta tuoreemmat omat tietueensa: kentät 1xx, 6xx ja 7xx sekä lisäksi viittauskenttä 9xx, jossa vanha nimimuoto. Miten tehdään viittä vuotta vanhempien KP:n tietueiden kanssa?</li>
</ul>

Tähän asti tietueet on huomattaessa korjattu TäTissä ja lähetetty Melindan kautta paikalliskantoihin. Aiheesta käydyssä vilkkaassa keskustelussa eniten kannatusta sai ehdotus poistaa Kirjastopalvelun viittä vuotta vanhemmat tietueet. Asia jätettiin pöydälle seuraavaan kokoukseen, jotta jokainen kimppa voisi arvioida poiston vaikutuksia omaan työskentelyynsä sekä onko viiden vuoden raja hyväksyttävissä. Toistaiseksi korjataan vain ne RDA-muotoiset tietueet, joita Kirjastopalvelu ei korjaa.

#### 3.	TäTin vanhat ja virheelliset Kirjastopalvelun tietueet ####
<ul>
  <li>Anneli on alkanut poistamaan tietueita, joissa 008/6-merkkipaikalla on virheellinen arvo. Jonkin verran jää tietueita jäljelle käsin korjattavaksi.</li>
</ul>

Anneli on poistanut jo yli 40 tuhatta tietuetta.

#### 4.	Otetaanko käyttöön Asterin uusi teos/ekspressiokanta (FIN13)? ####

Tietokanta päätettiin ottaa käyttöön. Antti selvittelee vielä yksityiskohtia.

#### 5.	TäTin kuvailupohjat ja 041-kentän kielikoodit-valikko (+ muutkin auktorisoidut arvot -valikot) ####

Antti esitteli kielikoodit-pudotusvalikkoa. Hyvältä vaikutti. Valikkoa testataan elokuva ja lautapelipohjissa. Pudotusvalikkoja on tulossa myös muihin kenttiin.

#### 6.	Nalkuttimen tilanne Vaarassa ####

Marja kertoi tuplaongelmia esiintyvän joskus tietueita korjattaessa. Asiaa selvitellään.

#### 7.	Kuulumisia YKN:n metatietoryhmästä ####
<ul>
  <li>Kohti metatietovisiota -projektin tilannekatsaus: <a href="https://www.kirjastot.fi/uutiset/uutiset/kohti-metatietovisiota-projektin-tilannekatsaus?language_content_entity=fi" target="_blank">Tiedote Kirjastot.fi:n uutisissa</a> </li>
  <li>Tutustuminen Ruotsissa sovellettaviin kuvailukäytäntöihin 8.–10.2.</li>
<ul>
  <li>matkaan ovat lähdössä metatietoprojektin ohjausryhmän nimeämät metatietoryhmän jäsenet Antti Heikkinen (Oulu/Koha), Katriina Jylhä (Vaasa/Mikromarc ja Quria), Saijamari Pakkala (Tampere/Aurora), Kaisa Hypén (Turku/matkan organisointi ja järjestelyt)</li>
<li>sovittuja tapaamisia:</li>
  <ul>
    <li>Tukholman kaupunginkirjasto: teemana kuvailu Libris-työkalulla, tietueiden konvertointi Bibframe -> Marc, konvertoitujen tietueiden edelleenkäsittely, tulevaisuuden suunnitelmat</li>
    <li>Kungliga Biblioteket: tärkein teema KB:n rooli kuvailun ekosysteemissä, kehittämiseen liittyvät tavoitteet, yleisiin kirjastoihin liittyvät näkemykset</li>
    <li>Adlibris: teemana aineistotoimittajan näkökulma Libris-yhteistyöhön</li>
    <li>Nacka: teemana kuvailutietojen hankinta ostopalveluna ja BTJ:n rooli</li>
  </ul>
  <li>Olisiko ideoita, mihin kannattaisi kiinnittää huomiota tai mitä kannattaisi kysyä Kohan näkökulmasta ajateltuna tai ylipäänsä Ruotsin kuvailukäytäntöihin liittyen?</li>
  </ul>
</ul>

Antille toivotettiin hyvää matkaa. Helle-kirjastot toivat esiin Ruotsissa käytettävät Kohan kannalta tarpeettomat 800-alkuiset kentät, joita voi olla tietueessa kymmeniä, estäen Kohaa käyttäviltä kirjastoilta Libriksen täysimääräisen käytön. Asiasta käydyssä keskustelussa tuli ilmi että, asiaa on aikaisemminkin selvitetty, mutta johtopäätöksiä ei kukaan muistanut. Ylimääräisten kenttien poistoa niiden siirtyessä Kohaan päätettiin selvittää uudelleen. Antti lupautui selvitysmieheksi.

#### 8.	Melinda ####
Helmetin erätuonneissa oli tiistaina 10.1.2023 häiriöitä, joiden myötä oli ilmaantunut tuplatietueita. Näitä tuli myös TäTiin asti 26 kpl. Tuplat on poistettu, mutta joihinkin tietueisiin oli ilmestynyt kaksi 020-kenttää, joissa viivallinen ja viivaton ISBN tai sitten q-kentissä eroja, esim. pehmeäkantinen vs. nidottu.

#### 9.	Muita asioita ####
Vaara kyseli ovatko osakohteet valuneet oikein. Muut kimpat totesivat että, jos osakohdevalutus toimii jollakin, on se suoranainen ihme. Vie/tuo-nappi todettiin parhaimmaksi vaihtoehdoksi tuoda osakohteet paikalliskantaan. Tämän lisäksi keskusteltiin Kirjastopalvelun tietueiden viipyilystä. Todettiin että jos tietue viipyy useamman kuukauden, asiaa kannattaa tiedustella heiltä suoraan.

#### 10.	Ehdotuksia kevään kokousajoiksi ####
<ul>
<li>15.2.</li>
<li>22.3.</li>
<li>19.4.</li>
<li>24.5.</li>
</ul>

Ehdotuksesta poiketen päätettiin seuraava kokous järjestää 22.2.2023 klo 13.15–15.00


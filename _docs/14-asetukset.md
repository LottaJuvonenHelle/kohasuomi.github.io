---
title: 'Asetukset'
permalink: /dokumentaatio/asetukset/
redirect_from:
  - /theme-setup/
toc: true
---

## 1. Kirjastot

Tietokantaan pitää luoda kirjastot. Se onnistuu Ylläpito -> Kirjastot -> Uusi kirjasto

<img src="/assets/files/docs/Asetukset/kirjasto.png" title="Kirjaston lisäyslomake" alt="Kuvakaappaus kirjaston lisäyslomakkeesta" style="width:90.0%" />
<img src="/assets/files/docs/Asetukset/kirjasto2.png" title="Kirjaston lisäyslomake" alt="Kuvakaappaus kirjaston lisäyslomakkeesta jatkuu" style="width:90.0%" />

**Kirjaston tunnus**

Yksilöivä tunnus, jossa ei kannata käyttää erikoismerkkejä tai ääkkösiä. Tunnusta ei pysty muuttamaan jälkikäteen.

Perinteisesti tunnus on muodostettu niin, että se alkaa ns. kuntaosiolla ja päättyy toimipistetunnukseen. Esim. Oulun pääkirjasto OUPK, jossa OU-viittaa Ouluun ja PK pääkirjastoon. Tässä muodostustavassa on omat hyvät puolensa, pystyy esimerkiksi raporteilla hakemaan tietyn kunnan kirjastoja alun perusteella (OU%), mutta huonona puolena on se, että jos kirjastoyksikkö muuttaa nimensä tai siirtyy toisen kunnan alaisuuteen, niin lyhenne ei enää vastaa kunta tai nimitietoa.

Tällä hetkellä Finna muodostaa organisaatio-fasetissa kunta/kirjastotason kirjastolyhenteen perusteella.

**Nimi**

Kirjaston nimi. Tätä pystyy muokkaamaan myöhemminkin.

**Osoiterivit**

Kirjaston lähiosoite.

**Kunta**

Tähän kirjataan postitoimipaikka. Englanniksi sana on City, jota käytetään muussakin yhteydessä kuntaan viittaavana, joten sanaa ei ole voitu suomentamaan postitoimipaikaksi.

**Osavaltio**

Ei ole Suomessa tarpeellinen tieto.

**Postinumero**

Kirjaston postinumero.

**Maa**

Voi halutessaan kirjata, mutta ei välttämätön.

**Puh.**

Kirjaston puhelinnumero.

**Faksi**

Tähän voi kirjata faksin numeron tai käyttää luovasti ja kirjata esim. keskitetyn asiakaspalvelun numeron, jos se on eri kuin kirjastopisteen oma numero.

**Sähköposti**

Tähän laitetaan noreply@koha-suomi.fi, koska sähköpostiviestit lähetetään Koha-Suomen/Bittigurun sähköpostipalvelimelta Koha-Suomen nimissä.

**Vastausosoite**

Tähän voi kirjata kirjaston oman sähköpostiosoitteen, jolloin asiakkaan vastaus tulee kirjaston osoitteeseen.

**Palautusosoite**

Tämä jätetään joko tyhjäksi tai laitetaan noreply@koha-suomi.fi. Tässä olevan osoitteen domain (eli @-merkin jälkeinen tieto) pitää olla sama kuin Sähköposti-kentässä olevassa osoitteessa. Jos ne ovat erit, sähköpostipalvelut tulkitsevat herkästi viestin roskapostiksi tai huijaukseksi.

**SMTP-palvelin**

Annetaan olla oletus-vaihtoehto.

**URL**

Tähän voi kirjata kirjaston tai verkkokirjaston osoitteen halutessaan. Ei tule automaattisesti näkyviin mihinkään, mutta voi käyttää hyväksi mm. viestipohjissa.

**Verkkokirjaston tiedot**

Tämä kenttä koskee Kohan omaa verkkokirjastoa, joka ei ole käytössä. Ei tarvitse täyttää.

**IP-osoite**

Tällä voisi rajata pääsyn tähän kirjastoon tiettyyn ip-osoitteeseen tai aliverkkoon. Rajaus ei ole tarpeellinen.

**MARC-yhteisökoodi**

ISIL-tunnus. Ei tarvitse täyttää, koska kuvailu tehdään erilliseen TäTi-tietokantaan.

**Muuta**

Lisätietokenttä, ei tarpeellinen.

**Noutopaikka**

Tällä asetuksella valitaan, onko kirjastoyksikkö varausten noutopaikka vai ei. Asetus vaikuttaa sekä virkailijaliittymään että Finna-verkkokirjastoon. Jos kirjaston määrittää ei-noutopaikaksi, niin virkailijat eivät pysty ohittamaan asetusta.

**Julkinen**

Liittyy Kohan omaan verkkokirjastoon, joka ei ole käytössä. Ei tarpeellinen.


## 2. Kirjastoryhmät

Kirjastoryhmillä voi kirjastoja voi ryhmitellä eri tarpeiden mukaan esim. hakuryhmiin, kellutusryhmiin, yms. Kirjastoryhmät määritellään Ylläpito -> Kirjastoryhmät

OKM-tilastoja varten pitää perustaa ryhmä, jonka nimekkeessä mainitaan OKM. Esim. TUU_OKM. Tyypillisesti ryhmään lisätään yhden kunnan kirjastoyksiköt.

Uusi ryhmä tehdään Lisää ryhmä -painikkeella. Kun ryhmä on luotu, voi siihen lisätä kirjastoja Lisää kirjasto -nappulalla. Toiminnot-nappulan takaa voi lisätä alaryhmän, muokata ryhmän tietoja tai poistaa ryhmän. Alaryhmän tarvetta kannattaa harkita tarkkaan.

<img src="/assets/files/docs/Asetukset/ryhma.png" title="Kirjastoryhmän lisäyslomake" alt="Pop-up-ikkuna, jossa voi lisätä kirjastoryhmän" style="width:60.0%" />

**Nimeke**

Ryhmän nimi. Tieto on pakollinen, mutta sen voi muuttaa myöhemmin.

**Kuvaus**

Ryhmää voi kuvailla halutessaan, esim. mihin tarkoitukseen se on.

**Ominaisuudet**

- Rajoita muihin ryhmiin kuuluvien pääsyä tämä ryhmän asiakkaisiin -> Ei tarpeellinen.
- Käytä verkkokirjaston hakuryhmille -> koskee Kohan omaa verkkokirjastoa, ei tarpeellinen
- Käytä virkailijaliittymän hakuryhmille -> tällä ryhmän saa näkymään tiedonhaussa kirjasto-rajausten osiossa.
- Paikallinen varausryhmä -> tätä toimintoa ei ole vielä testattu.
- Paikallinen kellutusryhmä -> tällä voi määrittää ryhmään kuuluvien kirjastojen aineiston kellumaan ryhmään kuuluvissa kirjastoissa.

## 3. Nidetyypit

Jotta mitään voisi lainata, pitää määritellä nidetyypit, koska laina- ja maksusäännöt perustuvat niihin. Nidetypit kuvaavat teoksen laina-aikaa ja myöhästymismaksuja, jotka perustuvat kimpan/kirjaston käyttösääntöihin, joten jokaisella Koha-kimpalla on hieman erilaiset nidetyypit. Toki yhteneväisyyttäkin on. Yleisiä nidetyyppejä on mm. "28 vrk" tai "28 vrk lastenaineisto".

Laina- ja maksusääntöjä voi tehdä kirjaston, asiakastyypin ja nidetyypin mukaan. Nidetyyppejä luodessa kannattaa siis miettiä, minkälaisia laina-aikoja ja myöhästymismaksuja tarvitsee olla, kuinka monta lainaa saa olla kerralla, tarviiko automaatilla tehdä lajitteluja nidetyypin (joka mäpätään sip-materiaalityypiksi), tarvitseeko pystyä tekemään nidevarauksia.

**Alla esimerkkinä OUTI-kirjastojen nidetyypit:**

14 vrk - AV	: 14VRK (AV-aineistolle, joissa laina-aika on 14 vrk)

14 vrk - 2 lainaa :	14VRK2LA  (Konsolipeleille, joissa laina-aika on sama kuin muulla AV-aineistolla, mutta lainamäärä on rajoitettu kahteen)

14 vrk - 40 snt/pv :	14VRK40SNT (Lyhytlainoille, joilla laina-aika on 14 vrk, mutta päivittäinen myöhästymismaksu on korkeampi kuin AV-aineistolla)

14 vrk - LN - AV	: 14VRKLN  (Lasten AV-aineisto, jolla laina-aika 14 vrk. Lastenaineistosta ei mene päiväkohtaista myöhästymismaksua, joten sitä varten tarvitaan oma nidetyyppi)

14 vrk - LN - 2 lainaa :	14VRKLN2LA (Lasten konsolipeleille. Muuten sama kuin yllä oleva vastaava, mutta ei mene päiväkohtaista myöhästymismaksua)

28 vrk :	28VRK (Yleisin nidetyyppi, jolle on määritetty laina-ajaksi 28 vrk ja myöhästymismaksuksi 15 snt/pv. Nidevaraukset eivät sallittuja verkkokirjastossa.)

28 vrk - AV :	28VRKAV  (AV-aineistolle, joissa laina-aika on 28 vrk. Nämä pitää saada palautusautomaatilla lajiteltua muusta 28 vrk-materiaalista erilleen, minkä vuoksi oma nidetyyppi)

28 vrk - Lehti	: 28VRKLEHTI (Aikuisten lehdille. Näille pitää pystyä tekemään nidevarauksia verkkokirjastossa, minkä vuoksi oma nidetyyppi)

28 vrk - LN	: 28VRKLN (Lasten aineisto yleislaina-aika. Näistä ei saa mennä päiväkohtaista myöhästymismaksua, minkä vuoksi erillinen nidetyyppi 28 vrk:sta)

28 vrk - LN - AV	: 28VRKLNAV (Lasten aineiston 28 vrk:n AV-aineiston nidetyyppi, joista ei saa mennä päiväkohtaista myöhästymismaksua)

28 vrk - LN - Lehti	: 28VRKLNLEH (Lasten lehtiaineistolle oma nidetyyppi, koska ei saa mennä päiväkohtaista myöhästymismaksua ja pitää pystyä tekemään nidevarauksia verkkokirjastossa)

7 vrk - 1 laina	: 7VRK1LA (Pikalainat/Sarjakortit, joilla laina-aika 7 vrk, lainamäärä 1 kpl ja myöhästymismaksu 40 snt/pv)

Ei lainata	: EILAINATA (Ei lainattavan materiaalin nidetyyppi, joille määritetty lainamääräksi 0)

Oppimateriaalipalvelut : OPPIMATER (Oulun koulukirjaston Oppimateriaalipalvelujen tarvitsema nidetyyppi. Muuten koulukirjaston niteet ovat lasten aineiston nidetyypeillä)

## 4. Auktorisoidut arvot

Auktorisoituja arvoja voi käyttää Kohan eri osioissa esim. alasvetovalikoissa. Ne ovat siis valmiita "listoja", joita halutaan käytettävän vapaan tekstin sijaan. Kaikki arvot ovat pääsääntöisesti kaikille kirjastoille/asiakastyypeille käytettävissä, mutta ne voidaan rajoittaa myös käytettäväksi tietyillä kirjastoilla tai asiakastyyypeillä. Alla listattuna tärkeimmät:

**agelevel**

agelevel-luokalla ja sen arvoilla luodaan tiedonhakuun mahdollisuus rajata hakua elokuvan ikärajan mukaan. Luokan nimi on sama kuin ikäraja-indeksin nimi.

**AUTOMTYPE**

AUTOMTYPE-luokka on luotu asiakasmäärettä AUTOTYPE-varten, jolla taas voi määrittää SIP2-tunnuksiin, minkä tyyppinen automaatti on kysessä. Eli onko se lainausautomaatti, palautusautomaatti, lainaava ja palauttava vai ovikone. Tämä luokka on rajoitettu käytettäväksi vain asiakastyypille AUTOM/AUTOMAATTI

**BOR_NOTES**

BOR_NOTES-luokan arvoilla voi luoda valmiita viestipohjia, jotka näkyvät, kun asiakkaalle lisää viestin.

**CCODE**

CCODE eli kokoelmakoodi. Tämän arvon voi määrittää niteelle. Näistä ei ole tehty Koha-Suomen laajuista yhteistä päätöstä, mutta monestikin kokoelmat ovat esim. Jännitys, Fantasia, Romantiikka yms.

**DAMAGED**

DAMAGED-luokan arvot näkyvät niteen ylläpidossa Vahingoittunut/Varattavuus-rivin valikossa. Tätä arvoa käytetään hieman luovasti estämään niteiden jääminen kiinni varauksiin. Arvoina voi olla esim. "Saatavana, ei varattavissa" ja "Saatavana oppilaille, ei varattavissa". Vaikka jonkin nidetyypin määrittäisi "ei varattavaksi", niin Koha noudattaa sitä vain varatessa, ei silloin kun varaukset jäävät palautettaessa kiinni. Eli jos tietueella on osa niteistä varattavia ja osa ei-varattavia, pystyy tietueeseen tekemään varauksia ja ilman damaged-tilaa niteet myös jäävät kiinni varauksiin. Lisäksi pitää laittaa järjestelmäasetukseen *AllowHoldsOnDamagedItems* vaihtoehto "Älä salli".

**LOC**

LOC-luokkaan määritetään niteiden hyllypaikat (eli osastot). Hyllypaikoista ei ole Koha-Suomen kimppojen yhteistä päätöstä, mutta yleisiä ovat mm. Aikuiset, Lapset (tai Lapset ja nuoret), Musiikki, Lehdet, jne. Hyllypaikat ovat kaikille kirjastoyksiköille yhteiset, mutta kuten muutkin auktorisoidut arvot, ne voidaan tarvittaessa rajoittaa käytettäväksi vain tietyille kirjastoille.

**LOST**

LOST-luokassa on niteiden kadonnut-arvot.

**MTYPE**

MTYPE-luokassa on tietueiden aineistotyypit, jotka vastaavat Finnan materiaalityyppejä. Arvo on kytketty MARC-kenttä 942c.

**NOT_LOAN**

NOT_LOAN-luokassa on niteen Ei lainata -arvot. Arvot voivat olla miinus- tai plusmerkkisiä. *SkipHoldTrapOnNotForLoanValue*-järjestelmäasetuksella määritetään, mitkä ei-lainata-arvot estää varausten kiinni jäämisen. *TrapHoldsOnOrder*-järjestelmäasetuksessa määritetään, ovatko miinusmerkkiset arvot varattavissa.

**REPORT_GROUP ja REPORT_SUBGROUP**

REPORT_GROUP ja REPORT_SUBGROUP -luokissa määritetään, minkä nimisiä välilehtiä näkyy Tallennetuissa raporteissa. Näitä voi luoda myös suoraan raportti-osion kautta.

**SIP_MEDIA_TYPE**

SIP_MEDIA_TYPE-luokassa on lueteltuna SIP-mediatyypit, jotka välittyvät SIP2-viestissä automaatille. Näiden perusteella voidaan tehdä esim. lajitteluja automaatin ohjelmistossa. Standardi on vanha, joten vaihtoehtoja ei ole kovin kummoisia. Nämä on kytkettävissä Kohan nidetyyppeihin niiden ylläpidossa.

**SUBLOC**

SUBLOC-luokka eli niteen hyllytarkenne. Tämä on Koha-Suomen oma lisäys. Hyllytarkenteista ei ole Koha-Suomen kimppojen laajuista päätöstä ja niitä onkin käytetty hyvin eri tavoin. Niissä voi olla saman tyyppisiä arvoja kuin kokoelmissa tai esimerkiksi Koulukirjastojen kirjastoyksiköiden nimiä.

**TOIMITTAJAT**

TOIMITTAJAT-luokka on aisapari AUTOMTYPE-luokalle eli tällä voi määrittää SIP2-tunnukseen, mikä toimittajan automaatista on kyse. Tämä arvo on rajoitettu vain asiakastyypille AUTOM/AUTOMAATTI.

## 5. Asiakastyypit

Koha-asiantuntijaryhmä on päättänyt yhteiset asiakastyypit 27.3.2017.

|Lyhenne/Tunnus|Selite|Huomautus|
|-----------|-------------|-----------|
|HENKILO|Henkilöasiakas||
|LAPSI|Lapsiasiakas||
|YHTEISO|Yhteisöasiakas||
|VIRKAILIJA|Kirjaston työntekijä| Tätä käytetään vain käyttäjätunnuksena, ei käytetä kirjastokorttina. Henkilökunnalla pitää olla erikseen kirjastokortti-tunnus.|
|KAUKOLAINA|Kaukolainakirjasto||
|KOTIPALVEL|Kotipalveluasiakas||
|EITILASTO|Ei tilastoitavat lainat|Käytetään ns. työlainojen ja -varausten tekemiseen.|
|MUUHUOL|Huollettava, muu kuin lapsi|Aikuinen, jolle pitää merkitä huoltaja.|
|AUTOM|Z Automaatti Z|SIP2-automaattien/ovikoneiden/laitteiden käyttäjätunnukset. Selitteessä on Z-kirjaimet, jotta se asettuu valikossa loppuun.|
|API| Z API Z|Erilaisten rajapintoja käyttävien järjestelmien/toimintojen käyttäjätunnukset. Selitteessä on Z-kirjaimet, jotta se asettuu valikossa loppuun. Päätetty ottaa käyttöön [Koha-Suomen asiantuntijaryhmän kokouksessa 4/21](https://tiketti.koha-suomi.fi/projects/mls/wiki/Asiantuntijat_-_Vuosi_2021#Muistio-421).|
|LAOMATOIMI|Lapsi, omatoimi sallittu|Tarvitaan lapsiasiakkaille, joilla on huoltajan antama lupa päästä omatoimeen. Lapsi-asiakkaiden pääsy estetään. Päätetty ottaa käyttöön [Koha-Suomen asiantuntijaryhmän kokouksessa 5/21](https://tiketti.koha-suomi.fi/projects/mls/wiki/Asiantuntijat_-_Vuosi_2021#5-Asiakastyyppi-omatoimiestoille) |

### 5.1 Asiakastyyppien määritykset

**Tyyppikoodi**

Tyyppikoodiin tulee yllä luetellut tunnukset.

**Kuvaus**

Kuvausta voi muokata halutessaan muuksikin kuin yllä olevassa taulukossa.

**Voimassaoloaika**

Henkilöasikkaiden oletusvoimassaoloajaksi on sovittu Koha-Suomen asiantuntijaryhmän 9.5.2022 kokouksessa kymmenen vuotta.

Muilla asiakastyypeillä voi olla tarvittaessa lyhyempi voimassaoloaika.

**Vaadittu ikä ja Ikäraja**

Näillä asetuksilla määritetään asiakkaan minimi ja maksimi ikä. Lapsiasiakkaat muutetaan aikuiseksi tämän asetuksen perusteella, eli kun asiakas saavuttaa maksimi-iän, vaihdetaan hänen asiakastyyppi aikuisasiakkaaksi (henkilöasiakas).

Kun asiakasta lisätään, tarkistaa lomake, että asiakkaan ikä on asiakastyypille sallitussa ikähaarukassa.

**Rekisteröintimaksu**

Ei tarpeellinen Suomessa, merkitse 0.00.

**Myöhästymisilmoitus**

Tällä asetuksella määritetään, lähteekö asiakastyypin asiakkaille OVERDUE_NOTICE-tyyppisiä viestejä eli palautuskehotuksia. Esim. työkorteille (EITILASTO) ei kannata määrittää lähtemään myöhästymisilmoituksia.

**Näytetäänkö kadonneet niteet virkailijaliittymässä**

Valitse "Näytetään".

**Varausmaksu**

Ei sovellu suomalaiseen kirjastomaailmaan, koska varausmaksua ei saa lain mukaan periä. Laita 0.00.

**Luokkatyyppi**

Luokkatyyppi määrittelee, minkälainen "lomake" näytetään asiakasta lisätessä ja muokatessa. Esim. lapsiasiakas-tyypeille pitää määrittää "Huollettava", jotta lomakkeella näkyy huoltajan lisäysosio. Yhteisöasiakkailla taas näkyy vain yksi nimikenttä. 

Huom! Tilastoyksikkö-valinta aiheuttaa sen, että lainatessa lainat eivät mene asiakkaalle lainaan.

**Kirjastorajoitukset**

Asiakastyypin voi tarvittaessa rajoittaa myös tietyn kirjaston käyttöön, mutta pääsääntöisesti tämä ei ole tarpeen.

**Salasanan palautus verkkokirjastossa**

Valitse järjestelmäasetuksessa OpacResetPassword, että käyttäjät saavat palauttaa unohtuneen salasanansa verkkokirjastossa ja valitse tähän kohtaan, että Noudata järjestelmäasetusta OpacResetPassword.

**Salasanan vaihto verkkokirjastossa**

Valitse järjestelmäasetuksessa OpacPasswordChange, että sallitaan salasanan vaihto verkkokirjastossa ja valitse tähän kohtaan "Noudata järjestelmäasetusta OpacPasswordChange".

**Salasanan minimipituus**

Asiakkaiden asiakastyypeille tähän laitetaan numero 4, koska omatoimikirjautumisessa ei voi käyttää kuin neljänumeroista pin-koodia.

VIRKAILIJA/AUTOM/API-asiakastyypeille määritetään joko 15 (Kyberturvallisuuskeskuksen suositus) tai jätetään tyhjäksi, jolloin noudatetaan järjestelmäasetusta  minPasswordLength. Muista käydä määrittämässä kyseiseen järjestelmäasetukseen silloin tuo 15.

**Vaadi vahva salasana**

Asiakas-asiakastyypeille valitaan vaihtoehto "Ei". Asiakkailta ei voi vaatia vahvaa salasanaa, koska omatoimikirjautumisessa voi käyttää vain nelinumeroista pin-koodia.

VIRKAILIJA/AUTOM/API-asiakastyypeille määritetään "Kyllä". Tietoturvasyistä käyttäjätunnuksilta vaaditaan vahva salasana.

**Estä vanhentuneet asiakkaat**

Valitse vaihtoehto "Järjestelmäasetus BlockExpiredPatronOpacActions määrittää".

**Tarkasta edelliset lainat**

Kotipalvelu-asiakastyypille voi valita "Kyllä ja yritä ohittaa järjestelmäasetukset". Muille asiakastyypeille kannattaa valita "Ei ja yritä ohittaa järjestelmäasetukset.

Käytännössä järjestelmä tarkistaa lainatessa ja varatessa, onko saman tietueen nide ollut asiakkaalla jo lainassa. Jos asetus on päällä, pitää virkailijan kuitata huomautus. Lainaaminen ei onnistu automaateilla, jos teos on ollut jo asiakkaalla lainassa.

**Oletusarvo yksityisyydelle**

Tämä tarkoittaa lainahistorian säilytysaikaa. 

- Oletus tarkoittaa kirjaston määrittämän ajan. Koha-Suomen asiantuntijaryhmä on ehdottanut oletussäilytysajaksi kolme vuotta.
- Ei koskaan tarkoittaa, että lainahistoriaa ei tallenneta ja laina anonymisoidaan heti, kun nide palautetaan.
- Aina tarkoittaa, että lainahistoria säilyy aina, eikä sitä poisteta säännöllisissä poisto/anonymisointiajoissa.

**Jätä pois paikallisten varausten jonosta**

Valitse ei.

**Viestien oletusasetukset tälle asiakastyypille**

Asiakastyypille voi määritellä oletusasetukset viesteille. Nämä valinnat tulevat siis automaattisesti, kun luodaan kyseisen asiakastyypin asiakasta.

***

## 6. Laina- ja maksusäännöt

Laina- ja maksusäännöissä määritetään mm. laina-aika, sallittujen lainojen määrä, uusintojen määrä, varausten määrä, myöhästymismaksujen suuruus ja katto. Sääntöjä voi tehdä kirjaston, asiakastyypin ja nidetyypin mukaan. 

**Huomioitavaa:**

- Jos kirjastolle tekee yhdenkin oman säännön, oletussäännöt eivät enää koske kyseistä kirjastoa. Kirjastokohtaisiin sääntöihin pitää toistaa kaikki ne säännöt, jotka haluaa oletussäännöistä koskevan myös kirjastokohtaisesti.
- Vaikka olisi asettettu maksimi laina- ja varausmäärät asiakastyyppille, niin rajoitus koskee vain kirjastokohtaisesti. Eli jos lainojen maksimiksi on määritetty 50, saa asiakas lainata 50 kirjastosta A + 50 kirjastosta B + 50 kirjastosta C, jne.
- Jokainen lainasääntö sallii niin monta lainaa, kuin sille riville on määritetty. Käytännössä jos asiakas lainaa useampaan lainasääntöön kuuluvia niteitä, hän pystyy lainaamaan enemmän kuin yhden sääntörivin maksimissa määritetään.

Säännöt tarkistetaan tässä järjestyksessä, ja sääntönä käytetään ensimmäistä kirjaston, asiakastyypin ja nidetyypin mukaan osuvaa:

- sama kirjasto, sama asiakastyyppi, sama nidetyyppi
- sama kirjasto, sama asiakastyyppi, kaikki nidetyypit
- sama kirjasto, kaikki asiakastyypit, sama nidetyyppi
- sama kirjasto, kaikki asiakastyypit, kaikki nidetyypit
- oletus (kaikki kirjastot), sama asiakastyyppi, sama nidetyyppi
- oletus (kaikki kirjastot), sama asiakastyyppi, kaikki nidetyypit
- oletus (kaikki kirjastot), kaikki asiakastyypit, sama nidetyyppi
- oletus (kaikki kirjastot), kaikki asiakastyypit, kaikki nidetyypit

Kun nidetyypillä on emonidetyyppi, sääntö näytetään "Emo -> alatyyppi" ja sallittujen lainojen määrä rajoitetaan joko emon maksimiin (laskien mukaan "sisartyypit") tai nidetyypin erityissääntöön, siihen kummassa on pienempi luku.

Tarkentaaksesi sääntöä luo uusi sääntö, jolla on sama asiakastyyppi ja nidetyyppi.

### 6.1 Laina- ja maksusääntötaulukko

<img src="/assets/files/docs/Asetukset/lainasaannot.png" title="Laina- ja maksusäännöt" alt="Kuvakaappaus laina- ja maksusäännöt -sivulta. Näkymässä neljä sääntöriviä, joita voi muokata Muokkaa-napilla" style="width=100.0%" />

**Asiakastyyppi**

Valitse, mitä asiakastyyppiä sääntö koskee. Jos se koskee kaikkia, silloin ei valita asiakastyyppiä. Huomioitavaa on, että jos asiakastyypille tekee yhdenkin oman säännön, tällöin ei kaikkia asiakastyyppejä koskeva sääntö/säännöt koske enää kyseistä asiakastyyppiä.

**Nidetyyppi**

Niidetyypin mukaisia sääntöjä voi tehdä joko koskemaan kaikkia asiakastyyppejä tai tiettyjä asiakastyyppejä.

**Huomautus**

Tähän voi halutessaan laittaa jotain sääntöä kuvaavaa tietoa.

**Sallittu lainamäärä**

Jokainen lainasääntö sallii niin monta lainaa, kuin sille riville on määritetty. Käytännössä jos asiakas lainaa useampaan lainasääntöön kuuluvia niteitä, hän pystyy lainaamaan enemmän kuin yhden sääntörivin maksimissa määritetään.

**On-site lainoja sallittu**

On-site -lainat ovat tilastolainoja. Tätä voi käyttää esim. silloin, kun haluaa tilastoida mitä kirjoja on vinkattu. Nämä lainat eivät mene asiakkaan lainoihin.

**Laina-aika**

Määritä tähän laina-aika. Yksikkö eli onko laina-aika päivä/tunti-perusteinen määritetään omassa sarakkeessa.

**Päivätila**

Tällä asetuksella määritetään, käytetäänkö oletusta eli useDaysMode-järjestelmäasetuksessa määritettyä sääntöä vai jotain muuta valikossa ehdolla olevaa sääntöä. Pääsääntöisesti kimpassa kannattaa noudattaa yhteistä oletussääntöä.

**Yksikkö**

Tässä määritetään, onko laina-aika tunteja vai päiviä.

**Eräpäivä**

Tällä voi määrittää kiinteän eräpäivän. Tätä käytetään todennäköisesti lähinnä oppilaitoskirjastoissa, joissa halutaan, että eräpäivät eivät mene lukukauden loppumispäivän yli ja halutaan niteet takaisin ennen lukukauden loppua.

**Lyhennetty laina-aika paljon varatuille (päivinä)**

Kohassa on toiminnallisuus/järjestelmäasetus decreaseLoanHighHolds, jolla voi määrittää lyhyemmän laina-ajan sellaisille tietueille, joihin kohdistuu paljon varauksia. Laina-ajan voi määrittää oletuksena decreaseLoanHighHolds-järjestelmäasetukseen tai sääntökohtaisesti laina- ja maksussäännöissä, jolloin ohitetaan järjestelmäasetuksen sääntö.

Huomioitavaa: Tähän toiminnallisuuteen liittyy jonkin verran epäjohdonmukaisuuksia, joten kannattaa testata ennen käyttöönottoa huolella, että logiikka sopii omaan toimintaympäristöön.

<img src="/assets/files/docs/Asetukset/lainasaannot2.png" title="Laina- ja maksusäännöt keskiosa" alt="Laina- ja maksusäännöistä keskiosa" style="width:100.0%" />

**Maksun määrä**

Maksun määrä -kohtaan määritetään päivä/tuntikohtainen maksun määrä.

**Maksun veloitusväli**

Maksun veloitusväli -asetuksessa määritetään minkälaisella veloitusvälillä maksu veloitetaan, esim. 1 päivän välein, 5 päivän välein, 3 tunnin välein jne.

**Veloitusaika**

Veloitusaika-asetuksella määritetään, missä kohtaa veloitusväliä maksu lisätään asiakkaan maksuihin, alussa vai lopussa. Jos veloitusväli on yksi päivä, tällä ei ole juuri merkitystä, mutta jos veloitusväli on pidempi, esim. 7 päivää, on sillä jo merkitystä.

**Maksut anteeksi -aika (päivinä)**

Maksut anteeksi -aika (päivinä) on aika, jonka laina voi olla myöhässä ennen kuin aletaan veloittamaan myöhästymismaksuja. FinesIncludeGracePeriod-järjestelmäasetuksella määritetään, otetaanko Maksut anteeksi -aika huomioon, kun maksuja lasketaan.

Huom! Tämä asetus voidaan asettaa vain päiviksi, ei tunneiksi.

**Maksimi myöhästymismaksu**

Maksimi myöhästymismaksulla määritetään, kuinka paljon korkeintaan veloitetaan nidekohtaista myöhästymismaksua kyseiselle asiakastyyppi/nidetyyppiyhdistelmälle (lainasääntöriville).

Huom! Jos laina on useamman kerran myöhässä, niin lainasta voi kertyä yli maksimimäärän, koska jokaisesta myöhässä olevasta "lainakerrasta" (laina tai uusinta) kertyy oma maksurivi, joka kertyy maksimissaan sitten tässä asetettuun summaan.

**Korvaushinnan katto**

Tällä asetuksella voidaan estää se, että niteen korvaushinta ei ylitä maksimi myöhästymismaksua.

**Keskeytys (päivää)**

Jos asiakkaita "sakotetaan" jäädyttämällä heidän tilinsä/kirjasotkorttinsa, tähän määritetään, kuinka kauan päivissä jäädytys kestää.

Tätä ominaisuutta ei taideta Suomessa käyttää.

**Maksimikeskeytys (päivää)**

Tähän säädetään maksimimäärä päiviä, joita tilin/kirjastokortin jäädytys voi kestää.

**Keskeytyksen veloitusväli**

Keskeytyksen veloitusväli toimii kuten Veloitusaikaväli, mutta maksujen sijasta annetaan jäädytyspäiviä.

<img src="/assets/files/docs/Asetukset/lainasaannot3.png" title="Laina- ja maksusäännöt keskiosaa" alt="Laina- ja maksusääntöjen jatkoa" style="width:100.0%" />

**Sallitut uusintakerrat**

Asetuksella määritetään, kuinka monta kertaa asiakas voi uusia lainansa, mikäli siihen ei kohdistu varauksia, eikä asiakkaalla ole liikaa maksuja.

Huom! Jos tämän asetuksen muuttaa ns. lennossa pienemmäksi, voi asiakkailla olla uusintakertoja enemmän kuin sallitaan.

**Uusinta-aika**

Asetuksella määritetään, kuinka monta päivää lisää annetaan laina-aikaa. Tyypillisesti tässä on sama luku kuin laina-ajassa.

**Ei uusintaa ennen**

Asetuksella määritetään, koska lainan saa aikaisintaan uusia ennen eräpäivää. Tyypillisesti jos laina-aika on 28 vrk, niin tähän tulisi 27 vrk. Asetuksen tarkoituksena on estää asiakasta/virkailijaa uusimasta samaa lainaa monta kertaa saman päivän aikana ja kuluttamasta turhaan uusintakertojen määrää.

Huom! Jos tämä asetus on päällä ja asiakas vahingossa lukee automaatilla lainatessaan niteen uudelleen (kaksi kertaa peräkkäin, koitetaan nide silloin uusia. Jos tämä asetus on päällä, uusiminen ei onnistu ja asiakas saa automaatilta virheilmoituksen, että lainaaminen ei onnistunut. Nide on kuitenkin jo mennyt lainaan ensimmäisellä lukukerralla, mutta asiakas saa kuvan, että näin ei ole käynyt. Tämä on ongelmallista varsinkin omatoimiaikaan, jolloin asiakas ei voi tarkistaa tilannetta henkilökunnalta ja pahimmassa tapauksessa jättää itsellään lainassa olevan niteen automaatille/hyllyyn/tiskille.

Osalla kimpoista tämä asetus on käytössä, osassa siitä on luovuttu automaateilla tulevien ongelmien vuoksi.

**Automaattinen uusinta**

Asetuksella valitaan, onko kyseiselle lainasäännölle voimassa automaattinen uusinta vai ei. Tämä sääntö pelkästään ei riitä vaan lisäksi tarvitaan ajastettu ajo (cron job), joka tekee uusinnan lainasääntöjen mukaisesti.

Jos automaattinen uusinta on käytössä, pitää Ei uusintaa ennen -asetuksessa olla määritys. Muuten ajastettu ajo pyrkii uusimaan lainan joka päivä eräpäivän jälkeen. 

**Ei automaattista uusintaa tämän jälkeen**

Asetuksella voi määrittää päivien määrän, jonka jälkeen automaattista uusintaa ei tehdä. Esim. automaattisia uusintoja ei tehdä enää 80 päivää lainauspäivän jälkeen.

**Varauksia sallittu (yhteensä)**

Asetuksella määritetään, kuinka monta varausta voi tehdä yhteensä. Tässä on huomioitava, että jokainen lainasääntörivi sallii tässä määritetyn määrän varauksia. Jos jätetään tyhjäksi, asiakas voi tehdä rajoittamattoman määrän varauksia.

**Varauksia sallittu (päivittäin)**

Asetuksella määritetään, kuinka monta varausta asiakas voi tehdä päivittäin.

**Varauksia tietuetta kohti (määrä)**

Asetuksella määritetään, kuinka monta varausta asiakas voi tehdä tietuetta kohti. Lehtivarausten kohdalla on sallittava enemmän kuin yksi, koska numeroniteet ovat joko yhden tietueen tai vuositietueiden alla (riippuu kimpan koosta). Jos lehdillä varausmäärä rajataan esim. yksi/tietue, voi asiakas tehdä silloin vain yhteen lehtitietueen niteeseen varauksen.

Tämän käytössä on kimpoissa erilaisia käytäntöjä. Osa sallii tietueeseen saman verran varauksia kuin mitä on maksimimäärä, osa sallii vain yhden varauksen/tietue.

<img src="/assets/files/docs/Asetukset/lainasaannot4.png" title="Laina- ja maksusääntöjen loppuosa" alt="Laina- ja maksussääntöjen loppuosa" style="width:70.0%" />

**Hyllyvaraukset sallittu**

Tällä asetuksella säädetään, onko hyllyvarausten teko sallittua vai ei. Vaihtoehdot ovat Kyllä, Jos yhtään ei ole saatavilla ja Jos jokin ei ole saatavana.

Mikään ei suoraan ole vaihtoehtona "ei", mutta "Jos yhtään ei ole saatavilla" on teknisesti lähimpänä sitä.

**Verkkokirjaston nidevaraukset**

Asetuksella säädetään, voiko verkkokirjastossa (koskee myös Finnaa) tehdä nidevarauksia säännön piirissä oleviin niteisiin. Käytännössä kaikkiin muihin sääntöihin paitsi aikakauslehtiä koskeviin sääntöihin kannattaa laittaa _Älä salli_, jotta asiakkaat eivät tee turhaan yhteen tiettyyn niteeseen kohdistuvia varauksia. Lehtien osalta nidevaraukset taas ovat välttämättömiä, koska yksi nide on aina yksi lehden numero.

**Varausten noutoaika (päiviä)**

Asetuksella määritetään varausten noutoaika päivinä, jos pitää olla sääntörivi tai kirjastokohtainen. Noutoajan voi määrittää myös ReservesMaxPickUpDelay-järjestelmäasetukseen, jolloin se on oletusarvo, josta sitten poiketaan laina- ja maksusääntöjen säädöillä. Tyypillisesti tämä pitää lisätä esim. kirjastoautoille, joilla on tarve pidemmälle noutoajalle reittien vuoksi.

**Artikkelipyynnöt**

Asetuksella määritetään, onko asiakkaiden mahdollista tehdä Kohan verkkokirjastossa artikkelipyyntöjä. Ominaisuus ei ole käytössä yleisillä kirjastoilla.

**Lainausalennus (%)**

Asetuksellä määritetään lainausalennus prosentteina, mikäli käytössä on maksulliset lainaukset. Suomessa nämä ei taida olla edes laillisia, joten tähän ei tarvitse määrittää mitään.

**Toiminnot**

Sarakkeessa on Muokkaa- ja Poista-napit. Muokkaa-napista pääset muokkaamaan valitsemaasi riviä ja Poista-napilla rivin voi poistaa.

### 6.2 Oletussäännöt lainauksille, varauksille ja palautuksille

![](/assets/files/docs/Asetukset/lainasaannot5.png)

Voit asettaa lainojen sallitulle määrälle sekä varausten ja palautusten säännöille oletusarvot, joita käytetään, jos nidetyypille tai asiakastyypille ei ole määritelty tämän osion alla mitään arvoja. Näitä sääntöjä käytetään, jos mitään muuta sääntöä ei löydy.

**Sallittu lainamäärä**

Maksimimäärä lainoja. Tämä asetus ei ohita yläpuolella olevaa laina- ja maksusääntötaulukkoa.

**Yhteenlaskettu on-site-lainojen sallittu määrä**

On-site-lainojen maksimimäärä. Tämä asetus ei ohita yläpuolella olevaa laina- ja maksusääntötaulukkoa.

**Varauksia sallittu enintään (määrä)**

Varausten maksimimäärä. Tämä asetus ei ohita yläpuolella olevaa laina- ja maksusääntötaulukkoa.

**Varaussääntö**

Minkä kirjastojen niteitä/teoksia asiakas voi varata, perustuu asiakkaan kotikirjastoon. 

Vaihtoehdot: 
* Ei asetettu - oletus
* Mistä tahansa kirjastosta, eli minkä tahansa kirjaston asiakas voi tehdä kirjaston niteisiin varauksen.
* Paikallisesta varausryhmästä, eli vain ne asiakkaat, joiden kotikirjasto vastaa niteen kotikirjaston varausryhmää voi tehdä varauksen.
* Kotikirjastosta, eli vain asiakkaat, joiden kotikirjasto on sama kuin niteen kotikirjasto voi tehdä varauksen
* Ei varattavissa, eli kukaan asiakas ei voi varata.

Suositus: Mistä tahansa kirjastosta, kun käytössä on yhteinen varausjono. Muita vaihtoehtoja ei ole testattu ja ne perustuu asiakkaan kotikirjastoon, mikä ei käytännössä Suomen toimintaympäristössä tarkoita mitään.

**Varauksen noutokirjasto täsmää**

Asetuksella määritetään, mistä kirjastoista asiakas voi noutaa varauksensa.

Vaihtoehdot: 
* Ei asetettu, 
* mikä tahansa kirjasto, 
* niteen varausryhmä, 
* asiakkaan varausryhmä, 
* niteen kotikirjasto, 
* niteen sijaintikirjasto.

**Palautussääntö**

Asetuksella määritetään, mihin nide palaa, kun se palautetaan.

Vaihtoehdot:
* Ei asetettu
* Nide palaa kotikirjastoon
* Nide palaa lainaavaan kirjastoon
* Nide kelluu
* Nide kelluu kirjastoryhmän mukaan (KS-muutos). Tämä vaihtoehto pitää valita, jos haluaa käyttää kellutusryhmiä, jotka määritetään kirjastoryhmissä.

**Toiminnot**

Tallenna ja Pois päältä. Jälkimmäisellä voi tyhjentää asetetut asetukset.

### 6.3 Oletussääntö maksun hyvitykselle, kun palautetaan kadonnut nide

![](/assets/files/docs/Asetukset/lainasaannot6.png)

Asetuksessa voi määrittää oletussäännön maksun hyvityksille, kun kadonnut nide palautetaan. 

Vaihtoehdot:
* Hyvitä kadonneen aineiston korvausmaksu
* Hyvitä kadonneen aineiston korvausmaksu ja veloita uusi myöhästymismaksu
* Hyvitä kadonneen aineiston korvausmaksu ja palauta myöhästymismaksu
* Jätä kadonneen aineiston korvausmaksu

### 6.4 Oletusvaraussääntö nidetyypeittäin

![](/assets/files/docs/Asetukset/lainasaannot7.png)

Voit muokata tämän kirjaston sääntöjä nidetyypin mukaan, riippumatta asiakastyypistä. 

Varauksien määrityksillä on seuraavanlaisia vaikutuksia:

* Mistä tahansa kirjastosta: Asiakkaat mistä tahansa kirjastosta voivat varata tämän niteen. (käytetään oletusarvoa jos ei muutoin määritelty)
* Paikallisesta varausryhmästä: Niteen voivat varata vain asiakkaat, joiden kotikirjasto vastaa niteen kotikirjaston varausryhmää.
* Kotikirjastosta: Vain niteen kotikirjaston asiakkaat voivat varata niteen.
* Ei varattavissa: Asiakkaat eivät voi varata nidettä, eikä se jää varauksiin kiinni palautettaessa. Tällä säännöllä voi siis määrittää tietyn nidetyypin ei-varattavaksi.

Huom: Jos järjestelmäasetus 'AllowHoldPolicyOverride' on sallittu, lainauksen henkilökunta voi ohittaa nämä säännöt.
Tärkeä: Säännöt pohjautuvat ReservesControlBranch-järjestelmäasetukseen.

Voit määrittää, mistä asiakas voi noutaa varauksensa **Varauksen noutokirjasto täsmää** -sarakkeessa.

Vaihtoehdot:
* mikä tahansa kirjasto
* niteen varausryhmä
* asiakkaan varausryhmä
* niteen kotikirjasto
* niteen sijaintikirjasto

**Palautussääntö**-sarakkeessa voidaan määrittää, mitä tapahtuu, kun nide palautetaan.

Vaihtoehdot:
* Aineisto (Nide) palaa kotikirjastoon
  * jos käytössä on AutomaticItemReturn-järjestelmäasetus, käyttäjä ei saa ilmoitusta kuljetuksesta. 
* Aineisto (Nide) palaa lainaavaan kirjastoon
  * jos käytössä on AutomaticItemReturn-järjestelmäasetus, käyttäjä ei saa ilmoitusta kuljetuksesta.
* Aineisto (Nide) kelluu
* Aineisto (Nide) kelluu kellutusryhmän mukaan
  * Koha-Suomi-muutos

***

## 7. Asiakasmääreet

Asiakasmääreet ovat itse määritettäviä lisäkenttiä, jotka voi liittää asiakkaisiin. Jotta asiakasmääreitä voi lisätä, pitää järjestelmäasetus ExtendedPatronAttributes olla päällä.

![](/assets/files/docs/Asetukset/asiakasmaare.png)

Koha-Suomen kimpoilla on kolme kaikille yhteistä asiakasmäärettä: Automaattityyppi (AUTOTYPE), Sotu-avain (SSN) ja Automaatin toimittaja (TOIMITTAJA). Lisäksi voi olla kimppakohtaisia asiakasmääreitä, esim. OUTI-kirjastoissa on käytössä Y-tunnus-määre yhteisöasiakkaille.

Asiakasmääreet näkyvät asiakastiedoissa **Muut määreet ja tunnukset** -kohdassa.

![](/assets/files/docs/Asetukset/asiakasmaare1.png)

### 7.1 Uuden asiakasmääreen tekeminen

Uuden asiakasmääreen voi lisätä Uusi asiakasmääre -napista.

![](/assets/files/docs/Asetukset/asiakasmaare2.png)

**Asiakasmääreen tunnus** -kohtaan kirjoitetaan sopiva tunnus. Se kannattaa olla vähintään kolmemerkkinen, eikä se kannata olla sama kuin jokin muu tunnus (hyllypaikka, asiakastyyppi, nidetyyppi jne). Tunnus voi olla korkeintaan kymmenenmerkkinen.

**Kuvaus** -kohtaan voi antaa tunnukselle selkokielisen nimen.

**Toistettava** -kohtaan laitetaan rasti, jos määreen voi laittaa samalle asiakkaalle useamman kerran.

**Yksilöivä tunnus** -kohtaan laitetaan rasti, jos tunnus on yksilöivä eli uniikki. Samaa arvoa ei saa silloin laitettua kahdelle eri asiakkaalle. Esim. Sotu-avain on yksilöivä tunnus.

**Näytä verkkokirjastossa** -kohta tarkoittaa tällä hetkellä Kohan omaa opacia, mutta tähän kannattaa laittaa rasti tulevaisuutta ajatellen, jos sen halutaan näkyvän myös Finnassa.

**Muokattavissa verkkokirjastossa** -kohta tarkoittaa myös tällä hetkellä Kohan omaa opacia, mutta tähän kannattaa laittaa rasti tulevaisuutta ajatellen, jos sen halutaan näkyvän myös Finnassa.

**Haettavissa** -kohdassa määritetään, voiko määreellä hakea asiakkaita. Tähän kannattaa laittaa rasti ainakin Sotu-avaimen osalta.

**Pakollinen** -kohdassa määritetään, onko määre pakollinen.

**Näytä asiakkaan suppeissa tiedoissa** -kohdassa määritetään, näytetäänkö määre asiakastiedoissa vasemmalla olevassa tietoruudussa. Koha-Suomen kimpoissa tietoruutu on piilotettu css-määrityksellä.

**Säilytä pseudonymisointia varten** -kohdassa voi määrittää määreen tallennettavaksi pseudonymisoituihin tietoihin.

**Auktorisoidun arvon luokka** - kohtaan voi määrittää auktorisoidun arvon, jonka arvoja ehdotetaan vaihtoehdoiksi teksikentän sijaan. Esim. Automaattityyppi-määreelle on tähän valittu AUTOMTYPE-auktorisoitu arvo, jolloin määreelle annetaan alasvetovalikkoon vaihtoehdoiksi auktorisoidun arvon tunnukset.

![](/assets/files/docs/Asetukset/asiakasmaare3.png)

![](/assets/assets/files/docs/Asetukset/docs/Asetukset/asiakasmaare4.png)

**Kirjastorajoitus** - kohdassa asiakasmääreen voi rajoittaa koskevaksi vain tiettyä kirjastoa. Pääsääntöisesti määreet koskevat kaikkia kirjastoja.

**Tyyppi**-kohdassa asiakasmääreen voi rajata yhdelle asiakastyypille. Esim. OUTIssa Y-tunnus-määre on rajattu yhteisöasiakkaille. Kohta jätetään tyhjäksi, jos määreen haluaa koskevan kaikkia asiakastyyppejä.

**Luokka** -kohtaan voi valita PA_CLASS-auktorisoidun arvon luokan, jos sellaisia on määritetty. Näillä määreitä voidaan ryhmittää otsikoiden alle.

## 8. Aineistokuljetusten rajoitukset

Aineistokuljetusten rajoitukset -osiossa voi määrittää, kuinka niteitä voi kuljettaa perustuen lähettävään kirjastoon, vastaanottavaan kirjastoon ja kokoelmakoodiin/nidetyyppiin. Rajoitukset toimivat vain, jos UseBranchTransferLimits-järjestelmäasetus on päällä.  BranchTransferLimitsType-järjestelmäasetuksessa valitaan, perustuuko rajoitukset kokoelmakoodiin vai nidetyyppiin. 

Rajoitukset tehdään kirjastokohtaisesti eli ensin valitaan haluttu kirjasto. Sen jälkeen valitaan nidetyyppi/kokoelmakoodi-kohtaisesti, mihin kirjastoihin kuljetus sallitaan. Laita rasti niiden kirjastojen kohdalle, joihin kuljetus sallitaan.

![](/assets/files/docs/Asetukset/kuljetus.png)

Rajoituksia voi säätää myös **Kehittyneellä editorilla**, joka on matriisityyppinen taulukko. Siellä valitaan ensin nidetyyppi/kokoelmakoodi ja sen jälkeen pääsee säätämään koko kirjastoverkon rajoituksia kerralla. Isossa kimpassa tämä näkymä on hankala, mutta pienemmissä siedettävämpi.

![](/assets/files/docs/Asetukset/kuljetus1.png)

## 9. Kuljetusten painomatriisi

Kuljetusten painomatriisilla voi määritellä aineistojen kuljetuksille "kustannuksen" eri kirjastopisteiden välillä. Painomatriisi vaikuttaa vain Varausjono-raportin luomiseen, ei normaaliin varausjonon purkautumiseen. Järjestelmäasetus UseTransportCostMatrix pitää olla määritetty käyttöön, jotta määritettyjä arvoja käytetään.

Kustannukset voi merkitä haluamillaan minimi- ja maksimiarvoilla, esim. 1-100. Arvoja muokataan klikkaamalla haluttua kenttää ja kirjoitetaan arvo kenttään.

## 10. Nidekierron huomautukset

## 11. Kaupungit ja kunnat

## 12. Noutopalvelu

## 13. Asiakkaan rajoitukset

## 14. Maksutyypit

## 15. Credit-tyypit

## 16. Liitännäiset

## 17. Hallinoi taustatöitä

## 18. MARC-kuvailupohjat

## 19. Kohan MARC-määritykset

_Kohan MARC-määrityksissä_ määritetään, mitkä MARC-kentät yhdistetään Kohan tietokannan biblio, biblioitems ja items-taulujen sarakkeisiin. Kun kytkös on tehty, viedään MARC-kentän sisältö tietokannan tauluun, josta tiedon hakeminen on nopeampaa kuin marcxml:n sisältä.

Jos mäppäyksiä muutetaan, pitää tehdä täydellinen uudelleenindeksointi, jotta muuttuneet tiedot päivittyvät tietueista tietokannan tauluun. Uusille ja muokatuille tietueille sovelletaan uusia sääntöjä samantien.

Uusi määritys lisätään klikkaamalla halutun Koha-kentän kohdalla _Lisää_-nappia ja kirjoittamalla avautuvan popupiin lisättävän MARC-kentän numero ja osakenttä pilkulla erotettuna. Jos haluaa tehdä kytköksen kontrollikenttään, se lisätään kirjoittamalla '@'-merkki ja kontrollikentän numero.

![](/assets/files/docs/Asetukset/koha2marc.png)

Määrityksen voi poistaa klikkaamalla halutun Koha-kentän kohdalla _Poista_-nappia.

### Koha-kirjastojen 29.3.2022 yhdessä sopimat Koha2MARC-mäppäykset

| Sarake | MARC-kentät |
| --- | --- |
| Biblio.abstrac | 520 ‡a |
| Biblio.author | 100 ‡a, 110 ‡a, 111 ‡a |
| biblio.biblionumber | 999 ‡c |
| biblio.copyrightdate | (automaattisesti) |
| Biblio.datecreated | (automaattisesti) |
| Biblio.frameworkcode | 999 ‡b |
| biblio.medium | 245 ‡h |
| biblio.notes | 500 ‡a |
| biblio.part_name | 245 ‡p |
| biblio.part_number | 245 ‡n |
| biblio.serial | 942 ‡s |
| biblio.seriestitle | 830 ‡a 
| biblio.subtititle | 245 ‡b |
| biblio.timestamp | (automaattisesti) |
| biblio.title | 245 ‡a |
| biblio.unititle | 130 ‡a, 240 ‡a |
| biblioitems.agerestriction | 049 ‡c |
| biblioitems.biblioitemnumber | 999 ‡d |
| biblioitems.biblionumber | (automaattisesti) |
| biblioitems.cn_class | 084 ‡a |
| biblioitems.cn_item | 942 ‡i |
| biblioitems.cn_sort | 942 ‡6 |
| biblioitems.cn_source | 942 ‡2 |
| biblioitems.cn_suffix | 942 ‡m |
| biblioitems.collectionissn | 490 ‡x |
| biblioitems.collectiontitle | 490 ‡a |
| biblioitems.collectionvolume | 490 ‡v |
| biblioitems.ean | 024 ‡a |
| biblioitems.editionresponsibility | 028 ‡b |
| biblioitems.editionstatement | 250 ‡a |
| biblioitems.illus | 300 ‡b |
| biblioitems.isbn | 020 ‡a |
| biblioitems.issn | 022 ‡a |
| biblioitems.itemtype | 942 ‡c |
| biblioitems.lccn | (automaattisesti) |
| biblioitems.notes | (automaattisesti) |
| biblioitems.number | 830 ‡v |
| biblioitems.pages | 300 ‡a |
| biblioitems.place | 260 ‡a, 264 ‡a |
| biblioitems.publicationyear | 260 ‡c, 264 ‡c |
| biblioitems.publishercode | 028 ‡a |
| biblioitems.size | 300 ‡c |
| biblioitems.timestamp | (automaattisesti) |
| biblioitems.totalissues | 942 ‡0 |
| biblioitems.url | 856 ‡u |
| biblioitems.volume | 362 ‡a |
| biblioitems.volumedate | (automaattisesti) |
| biblioitems.volumedesc | (automaattisesti) |
| items.barcode | 952 ‡p |
| items.biblioitemnumber | (automaattisesti) |
| items.biblionumber | (automaattisesti) |
| items.booksellerid | 952 ‡e |
| items.ccode | 952 ‡8 |
| items.cn_sort | 952 ‡6 |
| items.cn_source | 952 ‡2 |
| items.coded_location_qualifier | 952 ‡f |
| items.copynumber | 952 ‡t |
| items.damaged | 952 ‡4 |
| items.damaged_on | (automaattisesti) |
| items.dateaccessioned | 952 ‡d |
| items.datelastborrowed | 952 ‡s |
| items.datelastseen | 952 ‡r |
| items.deleted_on | (automaattisesti) |
| items.enumchron | 952 ‡h |
| items.exclude_from_local_holds_priority | (automaattisesti) |
| items.holdingbranch | 952 ‡b |
| items.homebranch | 952 ‡a |
| items.issues | 952 ‡l |
| items.itemcallnumber | 952 ‡o |
| items.itemlost | 952 ‡1 |
| items.itemlost_on | (automaattisesti) |
| items.itemnotes | 952 ‡z |
| items.itemnotes_nonpublic | 952 ‡x |
| items.itemnumber | 952 ‡9 |
| items.itype | 952 ‡y |
| items.location | 952 ‡c |
| items.materials | 952 ‡3 |
| items.more_subfields_xml | (automaattisesti) |
| items.new_status | (automaattisesti) |
| items.notforloan | 952 ‡7 |
| items.onloan | 952 ‡q |
| items.permanent_location | (automaattisesti) |
| items.price | 952 ‡g |
| items.renewals | 952 ‡m |
| items.replacementprice | 952 ‡v |
| items.replacementpricedate | 952 ‡w |
| items.reserves | 952 ‡n |
| items.restricted | 952 ‡5 |
| items.stack | (automaattisesti) |
| items.stocknumber | 952 ‡i |
| items.sub_location | 952 ‡j |
| items.timestamp | (automaattisesti) |
| items.uri | 952 ‡u |
| items.withdrawn | 952 ‡0 |
| items.withdrawn_on | (automaattisesti) |

## 20. MARC-kuvailupohjan testaus

## 21. Auktoriteettityypit

## 22. Luokitusjärjestelmät

## 23. Tietueiden täsmäytyssäännöt

## 24. Tietueiden yhdistämisssäännöt

## 25. OAI-joukkojen asetukset

## 26. Nidehakukentät

## 27. Haun rajaukset

## 28. Hakukoneen asetukset (Elasticsearch)

## 29. Rahayksiköt ja vaihtokurssit

## 30. Budjetit

## 31. Tilit

## 32. EDI-tilit

## 33. Kirjasto-EANit

## 34. Tunnistustietojen tarjoajat

## 35. Z39.50/SRU-palvelimet

## 36. SMTP-palvelimet

## 37. Tarkoititko?

## 38. Taulujen asetukset

## 39. Äänihälytykset

## 40. Jaa käyttötilastojasi

## 41. Muut kentät

## 42. Pikanäppäimet

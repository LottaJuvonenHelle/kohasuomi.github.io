---
title: 'IntranetUserCSS'
permalink: /dokumentaatio/intranetusercss/
redirect_from:
  - /theme-setup/
toc: true
---

IntranetUserCSS-järjestelmäasetuksella pystyy "ohittamaan" Kohan CSS-määritykset ja esimerkiksi piilottamaan eri sivuilta elementtejä tai säätämään fontin kokoa ja väriä. Tämä on kevyempi tapa säätää näkymiä koskematta Kohan sivupohjiin.

Jokaisen kohdalle on merkitty, missä Koha-versiossa se toimii.


## Asiakkaat

### Piilota Asiakkaat-sivulla hausta osoite-hakuvaihtoehto

Versio: 17.05

> option[value='address'] { display:none; }


### Piilota asiakkaan kuva, jos asiakkaalla ei ole sellaista

Versio: 17.05

> /* Piilota asiakkaan kuva, jos asiakkaalla ei ole sellaista */
li#patronbasics img[src$="blank.png"] { display: none !important; }
li.email { background: none !important; }


### "Kirjoitussuojaa" sotu-avain-kenttä

Sotu-avain-kentän voi "kirjoitussuojata" niin, että siihen pystyy Lisää sotu -toiminnolla lisäämään sotu-avaimen, mutta käyttäjä ei pysty muokkaamaan kentässä olevaa tietoa. Käyttäjä pystyy poistamaan tiedon kentän vieressä olevalla "Tyhjennä"-linkillä.

Huomioi, että patron_attr_4-osiossa oleva numero riippuu siitä, kuinka monentena sotu-avain on näytöllä. Esim. OUTI-kirjastoissa numerona on 3 ja Hellessä 4. Voit tarkistaa numeron klikkaamalla asiakkaan muokkausnäytöllä hiiren oikealla sotu-avain-kenttää ja valitsemalla "Inspect Element (Q)" (toimii ainakin Firefoxilla).

Tarpeellisuus: Suositeltava
Versio: 21.11

> body#pat_memberentrygen.pat textarea#patron_attr_4 { pointer-events: none; }


### Käyttäjätunnus-osion piilottaminen asiakkaan muokkausnäytöltä

Käyttäjätunnus-osion piilottaminen asiakkaan muokkausnäytöltä.

Versio: 17.05

> /* Piilota Käyttäjätunnus-osio asiakkaan muokkausnäytöltä */
#pat_memberentrygen.pat fieldset#memberentry_userid { display:none; }


### Asiakasmääreen piilottaminen tiedot-näytöltä

Versio: 17.05

> /* Piilota asiakasmääre tiedot-näytöltä */
div#patron-extended-attributes ol li:nth-child(1) { display:none; }


### Piilota Luo hyvitys -välilehden sisältö

Versio: 21.11

> /* Piilota Luo hyvitys -välilehden sisältö asiakkaan maksuista */
form#mancredit { display: none; }


### Piilota asiakkaan ikä Tiedot-välilehdellä

Tarpeellisuus: Vapaaehtoinen
Versio: 21.11

> /* Piilota asiakkaan ikä tiedot-näytöllä */
body#pat_moremember.pat span.age_years { display: none; }


### Piilota Näytä aina lainat reaaliaikaisesti -valinta

Tarpeellisuus: Suositeltava, parantaa suorituskykyä.
Versio 21.11

Lainausnäytöltä piilotus:

> /* Piilota Näytä aina lainat reaaliaikaisesti / Always show checkouts immediately -täppä */
body#circ_circulation.circ input#issues-table-load-immediately { display: none; }
body#circ_circulation.circ div#checkouts.ui-tabs-panel.ui-widget-content.ui-corner-bottom label[for="issues-table-load-immediately"] { display: none; }


Tiedot-näytöltä piilotus:

> /* Piilota Näytä aina lainat reaaliaikaisesti / Always show checkouts immediately -täppä Tiedot-sivulta */
body#pat_moremember.pat input#issues-table-load-immediately { display: none; }
body#pat_moremember.pat div#checkouts.ui-tabs-panel.ui-widget-content.ui-corner-bottom label[for="issues-table-load-immediately"] { display: none; }


### Säädä Viesti asiakkaalle -viestin väriä

Versio 21.11

> /* Säädä Viesti asiakkaalle -viestin väriä */
#messages.circmessage span { color:#009900; font-weight: bold;}
#messages.circmessage span.circ-hlt { color:#cc0000; }


### Piilota Tiedot-sivulla Alternative contact / Vaihtoehtoinen yhteys -osio

Versio: 21.11

> /* Piilota Tiedot-sivulla Alternative contact / Vaihtoehtoinen yhteys -osio */ 
#patron-alternative-contact,
#patron-alternative-contact + div { display:none; }


### Piilota asiakkaan tiedot -sivulta Alternate address/ Vaihtoehtoinen osoite -osio

Versio: 21.11

> /* Piilota asiakkaan tiedot -sivulta Alternate address/ Vaihtoehtoinen osoite -osio */
#patron-alternate-address,
#patron-alternate-address + div { display:none; }


### Piilota asiakkaan muokkauksessa Yhteystiedot-boksista vihjeet näkyvistä

Versio: 21.11

> /* Piilota asiakkaan muokkauksessa Yhteystiedot-boksista vihjeet näkyvistä */ 
fieldset#memberentry_contact.rows div.hint { display: none; }


### Piilota maksujen mitätöintitäppä Asiakkaan tiedot- ja Lainaus-sivuilta

Versio: 21.11

> /* Asiakkaan lainat-taulu */
/* Piilota maksujen mitätöinti -täppä */
#circ_circulation #issues-table label[for="exemptfine"] { display:none; }
#circ_circulation #issues-table input#exemptfine { display:none; }

> /* Asiakkaan tiedot -sivulla lainat-taulu */
/* Piilota maksujen mitätöinti -täppä */
#pat_moremember #issues-table label[for="exemptfine"] { display:none; }
#pat_moremember #issues-table input#exemptfine { display:none; }


### Piilota asiakkaan tiedot -näytöltä muokkaa-linkit

Versio: 21.11

> /* Piilota asiakkaan tiedot -näytöltä muokkaa-linkit. Jatkossa muokkaus onnistuu vain yläreunan Muokkaa-napista */
body#pat_moremember a[href*="&step="] { display: none; }


### Piilota Ei asiakas -takaaja -kohta asiakkaan muokkauksesta

Versio: 21.11

> /* Piilota Ei asiakas -takaaja -kohta asiakkaan muokkauksesta */
body#pat_memberentrygen.pat fieldset#non_patron_guarantor.rows { display:none; }


### Piilota Tarkista edelliset lainat -kohta asiakkaan muokkauksesta

Versio: 21.11

> /* Piilota Tarkista edelliset lainat -kohta asiakkaan muokkauksesta */
body#pat_memberentrygen.pat label[for="checkprevcheckout"] { display:none; }
body#pat_memberentrygen.pat select#checkprevcheckout { display:none; }


### Piilota Tarkista edelliset lainat -kohta asiakkaan tiedot-sivulla

Versio: 21.11

> /* Piilota asiakkaan tiedot -sivulta "Tarkista edelliset lainat" -kohta */
body#pat_moremember.pat li#patron-checkprev { display:none; }


### Piilota ennakkoilmoituksen valinnasta 0 päivän keston

Versio: 21.11

> /* Piilota ennakkoilmoituksen valinnasta 0 päivän keston */
body#pat_memberentrygen.pat option[value='0'] { display:none; }


### Piilota Salli automaattinen uusinta -kohta

Asiakkaan lisäys/muokkausnäytöllä on kohta "Salli automaattinen uusinta", vaikka toiminto ei olisi sallittu laina- ja maksusäännöissä. Kohdan saa piiloon seuraavasti:

Versio: 21.11

> /* Piilota Salli automaattinen uusinta -kohta asiakkaan muokkauksesta */
body#pat_memberentrygen.pat li.radio { display:none; }


### Piilota Ei-asiakas-takaaja -osio

Lapsiasiakkaalle voi lisätä uudemmassa versiossa myös takaajan, jonka asiakastietoja ei tallenneta Kohaan. Kohdan saa piiloon seuraavasti:

Versio: 21.11

> /* Piilota Ei asiakas -takaaja -kohta asiakkaan muokkauksesta */
body#pat_memberentrygen.pat fieldset#non_patron_guarantor.rows { display:none; }


### Asiakkaan tietoruudun piilotus asiakastiedoista vasemmasta reunasta

Versio: 21.11

> /* Asiakkaan tietoruudun piilotus vasemmasta reunasta */
div.patroninfo { display: none; }


### Piilota Näytä takaajalle lainat ja Näytä takaajalle maksut -kohdat Tiedot-näytöltä

Versio: 21.11

> /* Piilota Näytä takaajalle lainat ja Näytä takaajalle maksut -tiedot */
#patron-privacyguarantor + li { display: none; }
#patron-privacyguarantor { display: none; }


### Säädä Lisää viesti -popparin alasvetovalikon leveyttä

Versio: 21.11

Säätö tehdään sekä lainaus- että tiedot-sivulle.

Ennen säätöä:
!{width:30%}ennenviesti.png!

Säädön jälkeen:
!{width:30%}jalkeenviesti.png!

> /* Säädä Lisää viesti -popupissa valikon leveys kapeammaksi lainaus- ja tiedot-näytöillä */
body#pat_moremember.pat.modal-open select#select_patron_messages { width: 556px;
}
body#circ_circulation.circ.modal-open select#select_patron_messages { width: 556px;
}


---

## Asiakkaat-sivu

### Säädä Selaa sukunimen mukaan -kohdan kirjaimet isommaksi ja harvemmaksi

Versio: 21.11

> /* Säädä Selaa sukunimen mukaan -kohdan kirjaimet isommaksi ja harvemmaksi */
#pcard_members_search .browse a,
#pat_member .browse a {
  padding:0 0.25em;
  font-size:larger;
}


### Säädä Selaa sukunimen mukaan -kohdan kirjaimien taustaväri toiseksi, kun hiiri viedään kirjaimen kohdalle

Versio: 21.11

> /* Säädä Selaa sukunimen mukaan -kohdan kirjaimien taustaväri toiseksi, kun hiiri viedään kirjaimen kohdalle */
#pcard_members_search .browse a:hover,
#pat_member .browse a:hover {
  background-color:#e8f0f8;
}


### Piilota asiakashaun "Kaikki"-vaihtoehto

Täällä pyritään estämään se, että virkailija ei vahingossa hae tietokannan kaikkia asiakastietoja listalle, jolloin kaikille listalla oleville tehdään muutoslokiin merkintä asiakastietojen katselusta.

Versio: 21.11

> /* Piilota asiakashaun "Kaikki"-vaihtoehto*/
#memberresultst_length select option:last-child { display: none; }


### Piilota Asiakkaan pikalisäys -painike

Rimpsu piilottaa Asiakkaan pikalisäys -painikkeen. Kyseisellä lomakkeella ei ole kaikkia tarvittavia kenttiä näkyvissä, joten se on ainakin osalle kimpoista turha.

> /* Piilota Asiakkaan pikalisäys -nappi */
body#pat_member.pat div#quick-add-new-patron-button.btn-group { display: none; }


### Piilota asiakashausta valikosta Lajittelu-vaihtoehdot

> /* Piilota asiakashausta valikosta Lajittelu-vaihtoehdot */
body#pat_member.pat select#searchfieldstype_filter option[value='sort1'] { display:none; }
body#pat_member.pat select#searchfieldstype_filter option[value='sort2'] { display:none; }


---

## Lainaus ja palautus

### Lainaus

### Piilota "Älä lainaa ja tulosta kuitti" -nappula lainauksessa

Jos lainattavaan teokseen on varaus, antaa Koha ilmoituksen, jossa ilmoitetaan  varauksesta ja pitää päättää, mitä tehdään. Yksi vaihtoehto on "Älä lainaa ja tulosta", joka tulostaa varauksen infokuitin (hold_slip). Varaus ei kuitenkaan jää kiinni eikä nide mene kuljetustilaan, joten kuitti on turha ja aiheuttaa ennemminkin hämmennystä, kun siihen tulostuu asiakkaan tiedot ja varauksen viimeinen voimassaolopäivä (yleensä parin vuoden päässä). Alla olevalla rimpsulla saa napin piiloon.

> /* Piilota Älä lainaa ja tulosta kuitti -nappula */
body#circ_circulation.circ button.print { display: none; }


Nappi näkyvissä
!alalainaaprint1.png!

Nappi piilossa
!alalainaaprint.png!

### Piilota Automatic renewal / Automaattinen uusinta -checkbox

Versio: 21.11

> /* Automatic renewal / Automaattinen uusinta -checkboxi piiloon */
body#circ_circulation #set-automatic-renewal { display: none; }


### Palautus

### Piilota palautus-näytön asetukset

Versio: 21.11

> /* Piilota Palautus-sivulla palautusasetukset. En saanut piilotettua blokkia, jossa asetukset on, mutta sisällön sain */
div#forgive-overdue-fines.circ-setting { display: none; }
div#book-drop-mode.circ-setting { display: none; }
div.forgive-manual-hold-fees.circ-setting { display: none; }
body#circ_returns.circ div#show-circ-settings a { display: none; }


### Piilota asiakkaan tiedot varaus-popupeista

Jotta turhia asiakastietojen katseluita saadaan vähennettyä, piilotetaan palautuksessa asiakkaan yhteystiedot varausten popupeista. Rimpsuista on kaksi eri versiota ja niitä käytetään riippuen siitä, onko käytössä varausten automaattinen kiinni jääminen vai ei.

Tarpeellisuus: Pakollinen
Versio: 21.11

Varausten automaattinen kiinnijääminen päällä. HUOM! Alimmainen rivi korjattu toisenlaiseksi, koska aiempi versio piilotti palautuksessa oikean yläreunan valikosta kirjastovalinnan. Uudella versiossa piilottuu sähköpostiosoite, mutta laatikkoon jää näkyville listapallero.

> /* Piilota varausruudusta asiakkaan yhteystiedot, kun käytössä automaattinen varauksen kiinni jääminen */
body#circ_returns.circ li.patronaddress1 { display: none; }
body#circ_returns.circ li.patroncity { display: none; }
body#circ_returns.circ a#boremail { display: none; }



Varausten automaattinen kiinnijääminen ei ole päällä

> /* Piilota varauksen popparista asiakkaan yhteystiedot */
body#circ_returns.circ.modal-open ul li:nth-child(4) { display: none; } /* Varaus palautuskirjastossa, puhelinnumero piiloon */
body#circ_returns.circ.modal-open ul li:nth-child(5) { display: none; }  /* Kuljetettava muualle, sähköpostiosoite piiloon */
body#circ_returns.circ.modal-open li.patronaddress1 { display: none; } /* Osoite piiloon */
body#circ_returns.circ.modal-open li.patroncity { display: none; } /* Osoite piiloon */
body#circ_returns.circ.modal-open a#boremail { display: none; } /* Varaus palautuskirjastossa, sähköpostiosoite piiloon */



### Laskutettu-merkintä palautuksessa isommaksi

Jos palautetaan laskutettu nide, siitä näkyvä ilmoitus on pieni. Alla olevalla css-säädöllä Laskutettu-ohjeistuksen kokoa saa säädettyä isommaksi.

Lisätty: 28.12.2022
Tekijä: Anni Rajala

> p.problem.ret_nflupdate { font-weight: 500; font-size: 26px; }


---

## Maksut

### Piilota Luo hyvitys -välilehden sisältö asiakkaan maksuista 

Tarpeellisuus: Hyvin suositeltava
Versio: 21.11

> /* Piilota Luo hyvitys -välilehden sisältö asiakkaan maksuista */
form#mancredit { display: none; }


### Piilota oletusmaksuja asiakkaan lisää maksu -toiminnosta

Tarpeellisuus: Suositeltava
Versio: 21.11

> /* Poistaa oletusmaksuja asiakkaan lisää maksu -toiminnosta */
body#pat_maninvoice.pat option[value='NEW_CARD'] { display:none; }
body#pat_maninvoice.pat option[value='LOST'] { display:none; }


### Piilota asiakkaan Maksut/Tapahtumat-välilehdeltä Luo hyvitys -painike

Tarpeellisuus: Suositeltava
Versio: 21.11

> /* Piilota asiakkaan Maksut/Tapahtumat-välilehdeltä Luo hyvitys -painike */
#table_account_fines button.refund-action{ display: none; }


---

## Tiedonhaku

### Tasaa otsikko ja tieto perustiedot-näytöllä samalle tasolle

Tarpeellisuus: Suositeltava (selkiyttää näkymää)
Versio: 21.11

> /* Tasaa otsikko ja tieto perustiedot-näytöllä samalle tasolle */
.label { vertical-align: inherit; }


!tasaus.png!

### Fonttikokojen säätö isommaksi koko perustiedot-näytöllä

Tarpeellisuus: Suositeltava
Versio: 21.11

> /* Säädä perustiedot-näytön fonttikokoja isommaksi*/
#catalogue_detail_biblio { font-size:larger; }


### Otsikkorivin fonttikoko suuremmaksi

Tarpeellisuus: Suositeltava
Versio: 21.11

> /* Otsikkorivin (nimeke ja tekijä) fonttikoko suuremmaksi */
#catalogue_detail_biblio h1 { font-size: 16pt; }


!nimeke.png!

### Seuraava- ja Edellinen -linkit pienemmiksi

Versio: 17.05, ei tarpeellinen versiossa 21.11, koska linkit muuttuneet nuoliksi

> /* Seuraava- ja edellinen-linkit pienemmiksi, jotta ne mahtuvat niille sallittuun tilaan */
body#catalog_detail div.browse-prev-next { font-size:8.5pt; background-color:#ffffff; }
body#catalog_MARCdetail div.browse-prev-next { font-size:8.5pt; background-color:#ffffff;}
body#catlaog_labeledMARCdetail div.browse-prev-next { font-size:8.5pt; background-color:#ffffff;}
body#catalog_moredetail div.browse-prev-next { font-size:8.5pt; background-color:#ffffff;}


!edellinen.png!

### Piilota kentät 336-338

Tarpeellisuus: Vapaaehtoinen
Versio: 21.11

> /* Piilota perustiedot-näytöltä kentät 336-338 */
body#catalog_detail #content_type.results_summary { display: none; }


!tyypit.png!

### Esityskokoonpanon järjestys näytöllä

Versio: 17.05

> /* Esityskokoonpanon järjestys näytöllä */
.performance-medium span[class^="sf-"] + span[class^="sf-"]:before {
  content: ", ";
}


### Otsikot boldattuna mustalla

Tarpeellisuus: Suositeltava
Versio: 21.11

> *Otsikot boldattuna mustalla*
.results_summary .label { color: #000000; font-weight: bold !important; }


!tasaus.png!

### Auktoriteettien MARC-näkymän säätöä

Versio: 17.05

> /* Auktoriteettien MARC */
#authoritiestabs div.tag p { font-weight: normal; display: inline; font-family: monospace; }
#authoritiestabs div.tag .labelsubfield,
#authoritiestabs div.tag .labelsubfield b { font-weight: normal; font-family: sans-serif; }
#authoritiestabs div.tag .labelsubfield span { display:none; }
#authoritiestabs div.tag p .labelsubfield:hover span,
#authoritiestabs div.tag p:hover .labelsubfield span {  display: inline; float:right; border: 1px solid black; background-color:#f0f0f0; position:relative; top: -1em; right: 0; padding:1em; }


### Muokka hakutulos-näytön värejä

Versio: 17.05

> /* Muokkaa hakutulos-näytön värejä */
.results_summary { color: #000111 !important; }
.results_summary span { color: #000000; font-weight: normal !important; }
.results_summary .label { color: #000000 !important; }


### Piilota Näytä kausijulkaisun tiedot -linkki

Versio: 17.05

> span.results_summary.analytics { display: none; }


### Piilota Huomautus toimenpiteistä

Piilota perustiedot-näytöltä huomautus toimenpiteestä eli MARC-kentän 583-tieto.

Tarpeellisuus: Vapaaehtoinen
Versio: 21.11

> /* Piilota Toimenpide-huomautus 583-kenttä perustiedot-näytöltä */
span.results_summary.actionnote { display: none; }


Ennen piilotusta:
!{width:40%}toimintaennen.png!

Piilotuksen jälkeen:
!{width:40%}toimintajalkeen.png!

### Piilota tuplakansikuvat

Joskus luettelointitiedoissa on syystä tai toisesta useampi kansikuvalinkki. Jos haluaa, että näkyvillä on vain yksi kansikuva, saa muut piiloon seuraavalla rimpsulla.

Versio: 17.05

> .cover_image_container ~ .cover_image_container {
   display:none;
}


### Säädä kansikuvan kokoa

Alla on kolme versiota, joilla voi säätää kansikuvien kokoa. Ensimmäinen versio vaikuttaa sekä hakutuloslista-sivulle että perustiedot-sivulle. Toinen vaikuttaa vain hakutulostilsta-sivulle ja kolmas perustiedot-näytölle. 

Tarpeellisuus: Suositeltava
Versio 21.11

Hakutuloslistalle ja perustiedot-näytölle:
> /* Säädä hakutuloslistan ja perustiedot-näytön kansikuva tietyn kokoiseksi. Muuta pikselikoko tarvittaessa toiseksi. */
.bookcoverimg {
  width: 150px;
}


Vain hakutuloslistalle:
> /* Säädä hakutuloslistan kansikuva tietyn kokoiseksi. Muuta pikselikoko tarvittaessa toiseksi. */
body#catalog_results.catalog .bookcoverimg {
  width: 150px;
}


Vain perustiedot-näytölle:
> /* Säädä perustiedotnäytön kansikuva tietyn kokoiseksi. Muuta pikselikoko tarvittaessa toiseksi. */
body#catalog_detail.catalog .bookcoverimg {
  width: 270px;
}


---

## Muita

### Muuta kaikissa taulukoissa rivin taustaväri, kun hiiri viedään rivin kohdalle

Versio: 21.11

> /* Muuta kaikissa taulukoissa rivin taustaväri, kun hiiri viedään rivin kohdalle. */
tr:hover td { background-color:#e8f0f8 !important; }


### Koha-logon piilotus virkailijaliittymän vasemmasta reunasta

Versio: 21.11
> /* Piilota Kohan logo vasemmasta reunasta */
#container-main {
    /* Contains the news + both columns of links + pending box + userblock box */
    background-image:none;
}

---

> /* Niteiden muokkaus -taulukko */
/* Piilota pois kierrosta -tila */
#cat_additem #itemst tr th:nth-child(2),
#cat_additem #itemst tr td:nth-child(2) { display:none; }


> /* SQL-raporttien tekstikenttä */
#rep_guided_reports_start textarea#sql { font-family: monospace; }

> /* Hankintaehdotustaulut */
table#ASKEDt,
table#CHECKEDt,
table#ORDEREDt,
table#REJECTEDt { width: 100%; }

### Testiympäristön ulkoasun muutokset

Versio: 21.11

> .gradient {
background-image: -webkit-gradient( linear, left top, left bottom, color-stop(0.1, rgb(255, 241, 186)), color-stop(0.99, rgb(255,255,255)) );
}

> #header.navbar-default {
background: rgb(255, 241, 186);
}

> #breadcrumbs {
background-color: #e3f2c8;
}

> #searchheader {
background-color: #e3f2c8;
}

> .navbar .nav > li > a {
color: #405b0e;
}

> #menu ul > li > a {
background: linear-gradient(180deg,#e3f2c8 0,#e3f2c8 96%,#c1c1c1);
}

> .ui-tabs .ui-tabs-nav li {
background: #e3f2c8 none;
}

> fieldset {
  background-color: #fafde9;
}

> ul.biglinks-list li a.icon_general {
border: solid 2px #b8ce97;
background-color: #fafbf4;
}

> body {
background-color: #fff2dd;
}

---
title: 'Järjestelmäasetukset'
permalink: /dokumentaatio/jarjestelmaasetukset/
redirect_from:
  - /theme-setup/
toc: true
---

## Ohjeita ja tietoja eri järjestelmäasetuksista

Koha-yhteisön suositus on, että auktorisoitujen arvojen koodeihin, esim. kirjastojen, hyllypaikkojen, yms. lyhenteisiin kannattaa käyttää vain kirjaimia a-z ja numeroita 0-9. Muut merkit voivat aiheuttaa ongelmia Kohan ja indeksoinnin kanssa.

Lisäksi koodeissa ei kannata olla myöskään alaviivoja, koska ne voivat aiheuttaa ongelmia indeksin kanssa.

Koska järjestelmäasetuksia on satoja, ei kaikista ole tällä sivulla tietoja. Järjestelmäasetuksia on käyty läpi pääkäyttäjien kanssa ja läpikäynneistä on tallenteet [Koha-Suomen Youtube-kanavalla](https://www.youtube.com/@koha-suomi/videos).

### BarcodePrefix

Asetuksella voi määrittää, millä merkkijonolla automaattisesti generoidut viivakoodit alkavat. Tämä vaatii kaveriksi autoBarcode-asetuksen toimiakseen. Asetus on YAMLia eli tieto pitää tallentaa tietyssä muodossa. Ensin kirjoitetaan kirjaston tunnus (minkä kirjaston niteestä kyse) - kaksoispiste - välilyönti - haluttu prefix. Eli siis näin:

LAPK: 111N<br />
TUPK: 123N<br />
RAPK: OUTI<br />

Eri kirjastopisteet laitetaan omille riveille.

### IntranetNav

IntranetNav-järjestelmäasetuksella saa lisättyä Kohan yläpalkkiin linkkejä. Alla viimeisin versio, jolla saa lisättyä Koha-Suomi-alasvetovalikon:

```
<li class="dropdown pull-right"><li class="nav navbar-nav pull-right"><a href="
<li id="kohasuomi-navlinkit" class="dropdown pull-right">
  <a href="/cgi-bin/koha/mainpage.pl" class="dropdown-toggle" data-toggle="dropdown">Koha-Suomi <b class="caret"></b></a>
  <ul class="dropdown-menu dropdown-menu-left">
    <li><a href="https://koha-suomi.fi/dokumentaatio/ohjeet/
" target="_ohjeet">Koha-ohje</a></li>
<li><a href="https://github.com/KohaSuomi/Koha/discussions
" target="_tiedotteet">Tiedotteet</a></li>
<li><a href="https://koha-suomi.fi/muistiot
" target="_muistiot">Muistiot</a></li>
<li><a href="https://github.com/orgs/KohaSuomi/projects/4
" target="_tiketit">Tiketit</a></li>
 </ul>
</li>
```

### IntranetReportsHomeHTML

Järjestelmäasetukseen voi lisätä omaa tekstiä Raporttien etusivulle. Sinne on päätetty siirtää Koha-Suomen MARC-virheraporttien linkit. Ne pystyy lisäämään alla olevan esimerkin mukaisesti. Muokkaa kimpan nimi osoitteisiin (huomaa, että kimpan nimi on osoitteessa kaksi kertaa eli yhteensä neljä muutosta)

```
<div class="col-md-10 col-md-offset-1 col-lg-8 col-lg-offset-2">
<h2>MARC-virheraportit</h2>
<ul>
<li><a href="https://helle.koha-suomi.fi/marc_virheet.helleprod.html" target="_blank" rel="noopener">Virheelliset tietueet </a></li>
<li><a href="https://helle.koha-suomi.fi/marc_virhemaara.helleprod.txt" target="_blank" rel="noopener">Virhem&auml;&auml;r&auml;t</a></li>
</ul>
</div>
```

### IntranetUserCSS

IntranetUserCSS-järjestelmäasetuksella voi "ohittaa" Kohan omia CSS-määrityksiä ja tehdä esimerkiksi erilaisia piilotuksia. Alla on linkki CSS-kirjastoon.

[IntranetUserCSS-kirjasto](/dokumentaatio/intranetusercss/)

### IntranetUserJS

IntranetUserJS-järjestelmäasetukseen voi lisätä JavaScript-koodeja, joille voi esim. lisätä tietoja eri näytöille kuten henkilötunnuksen lisäyskenttä asiakkaan muokkauksessa. Järjestelmäasetuksen muokkaamiseen tarvitaan kehittäjien apua, lue tarkemmat ohjeet alla olevasta JS-kirjastosta.

[IntranetUserJS-kirjasto](/dokumentaatio/intranetuserjs/)

### SCOUserCSS

SCOUserCSS-järjestelmäasetuksella voi säätää Kohan itsepalvelulainauksen ulkoasua.

Vaara-kirjastojen versio:

```
.navbar {
	display: none;
}

#opacheader {
	display: none;
}

.sco_entry.col-5 {
  background-color: rgb(81, 163, 226);
  margin: 25px 25px 55px 55px;
  padding: 25px 25px 25px 25px;
  -webkit-border-radius: 10px;
-moz-border-radius: 10px;
border-radius: 10px;
-webkit-box-shadow: 5px 5px 7px 0px rgba(0,0,0,0.35); 
box-shadow: 5px 5px 7px 0px rgba(0,0,0,0.35);
}

.sco_entry.col-5 h4 {
 font-size: 25px;
 color: darkslategrey;
}


.sco_entry.col {
  background-color: rgb(179, 222, 122);
  margin: 25px 25px 55px 55px;
  padding: 25px 25px 25px 25px;
  -webkit-border-radius: 10px;
-moz-border-radius: 10px;
border-radius: 10px;
-webkit-box-shadow: 5px 5px 7px 0px rgba(0,0,0,0.35); 
box-shadow: 5px 5px 7px 0px rgba(0,0,0,0.35);
}

.sco_entry.col h4 {
 font-size: 25px;
 color: darkslategrey;
}


#newcheckout {
  background-color: rgb(81, 163, 226);

  padding: 25px 25px 25px 25px;
  -webkit-border-radius: 5px;
-moz-border-radius: 5px;
border-radius: 5px;
-webkit-box-shadow: 5px 5px 7px 0px rgba(0,0,0,0.35); 
box-shadow: 5px 5px 7px 0px rgba(0,0,0,0.35);
}

.sco_entry h2 {
 font-size: 25px;
 color: darkslategrey;
}

#account {
 display: none;
}

label {

  white-space:nowrap;
}


#uibarcode {
  			
            width: 116%;
  
        }

.alert.alert-info {
  			background-color:rgb(0, 241, 111);

  
        }

/*  .alert.alert-info::after {content: "  Kirjautumisen jälkeen istunto katkaistaan 40 sekunnin kuluttua. Kirjaudu sisään uudelleen tarvittaessa.";}
*/
```

OUTI-kirjastojen versio:

```
a#account.nav-link { display: none; }

.navbar {
	display: none;
}

#opacheader {
	display: none;
}

.btn.btn-info.btn-sm.return{
  display: none;
}

.sco_entry.col-5 {
  max-width: 500px;
  background-color: skyblue;
  margin: 25px 25px 55px 55px;
  padding: 25px 25px 25px 25px;
  -webkit-border-radius: 10px;
-moz-border-radius: 10px;
border-radius: 10px;
-webkit-box-shadow: 5px 5px 7px 0px rgba(0,0,0,0.35); 
box-shadow: 5px 5px 7px 0px rgba(0,0,0,0.35);
}

.sco_entry.col-5 h4 {
 font-size: 25px;
 color: black;
}


.sco_entry.col {
  max-width: 500px;
  background-color: #8fe67e;
  margin: 25px 25px 55px 55px;
  padding: 25px 25px 25px 25px;
  -webkit-border-radius: 10px;
-moz-border-radius: 10px;
border-radius: 10px;
-webkit-box-shadow: 5px 5px 7px 0px rgba(0,0,0,0.35); 
box-shadow: 5px 5px 7px 0px rgba(0,0,0,0.35);

}

.sco_entry.col h4 {
 font-size: 25px;
 color: black;
}


#newcheckout {
  background-color: skyblue;
  max-width: 400px;
  padding: 25px 25px 25px 25px;
  -webkit-border-radius: 10px;
-moz-border-radius: 10px;
border-radius: 10px;
-webkit-box-shadow: 5px 5px 7px 0px rgba(0,0,0,0.35); 
box-shadow: 5px 5px 7px 0px rgba(0,0,0,0.35);
}

.sco_entry h2 {
 font-size: 25px;
 color: black;
}

#account {
 display: none;
}
```
### SCOUserJS

```
/* Viivakoodinlukijoita varten: */
/* Hitting "Enter" key in the username field will jump focus to the password field instead of submitting form  */
$(document).ready(function(){
    $('#patronlogin').keypress(function(e){
        if (e.keyCode == 13){
            $('#patronpw').focus();
            return false;
        }
    }); 
});
```

### Yksittäisiin asetuksiin suosituksia

Asetus|Suositus|Lisätietoja
---|---|---
SearchEngine| ElasticSearch|
PatronAutoComplete | Älä ehdota | Vältetään turhia tietojen katseluja
AgeRestrictionOverride | Älä salli | Esim. elokuvien ja pelien ikärajat ovat sitovia
ItemsDeniedRenewal | notforloan: [6] | Estää laskutetun niteen uusimisen
CalculateFinesOnReturn | Älä laske | Myöhästymismaksut lasketaan yöllä ajastetulla ajolla. Jos tämäkin on päällä, maksut voivat kirjautua asiakkaalle tietyissä tilanteissa uudelleen [maksut maksetaan ja sitten sen jälkeen palautetaan myöhässä olevia niteitä].
HidePersonalDetailOnCirculation | Piilota | Vältetään turhia tietojen katseluja
HoldsNeedProcessingSIP | Älä täytä | Omatoimiaikana automaattiin palautetuista varatuista niteistä ei lähde näin noutoilmoituksia
StoreLastBorrower | Säilytä | Säilytetään erillisessä taulussa niteen viimeisin lainaaja, vaikka lainat anonymisoidaan. Auttaa löytämään oikean asiakkaan ongelmatilanteissa.
TransfersBlockCirc | Estä | Kuljetukseen on reagoitava
TrapHoldsOnOrder | Ota kiinni | Saapunut/tilattu-tilaiset jäävät palautuksessa varauksiin kiinni
UpdateNotForLoanStatusOnCheckin | 6 : ONLYMESSAGE | Laskutetusta niteestä tulee ilmoitus palautettaessa





---
title: 'IntranetUserJS'
permalink: /dokumentaatio/intranetuserjs/
redirect_from:
  - /theme-setup/
toc: true
---

Seuraavia koodinpätkiä voi laittaa IntranetUserJS-järjestelmäasetukseen.

HUOM! Koha-Suomen kirjastojen pääkäyttäjät: Kohaan tehdyn tietoturva-auditoinnin perusteella IntranetUserJS-järjestelmäasetukseen on lisätty ominaisuus, että asetuksen sisällöstä lasketaan tarkistussumma, joka tallennetaan koha-confiin. Asetukseen tallennetut JavaScriptit ajetaan vain, jos tarkistussumma täsmää. Jos tarkistussumma ei täsmää, Kohan käyttöliittymän toiminta keskeytetään, jotta asetuksesta ei saa ajettua mahdollista haittakoodia. Jos asetukseen muuttaa yhdenkin merkin, tarkistussumma muuttuu. Jos teet muutoksia IntranetUserJS-järjestelmäasetukseen, huolehdi ennakkoon, että joku kehittäjistä on päivittämässä samaan aikaan tarkistussumman koha-confiin.

Kun Kohan käyttöliittymän toiminta pysäytetään IntranetUserJS-järjestelmäasetuksen tarkistussumman vuoksi, tulee ilmoitus: KOHA IS STOPPED DUE TO CHECKSUM MISMATCH IN SYSTEM PREFERENCES. PLEASE CONTACT YOUR SYSTEM ADMINISTRATOR.

[Muutokseen liittyvä tiketti](ttps://tiketti.koha-suomi.fi/issues/4343)



## Lainaus

### Alt+p tulostaa kuitin

Tämä ei tuntuisi toimivan.

``
/* When returning books, if there is an input with onclick handler that starts with "Dopop",
   allow pressing alt+p to click on that input. That should be a "print a slip" -type thing. */
``
``
$(document).ready(function () {
  $(document).bind('keypress', function(e) {
     var code = e.keyCode || e.which;
     if (code == 112 && e.altKey) { /* alt+p */
        e.preventDefault();
        $('body#circ_returns input.print[onclick^=Dopop]').trigger("click");
     }
  });
});
``

## Palautus

### "Maksuja ei peritä käsin peruutetuista varauksista" -täppä päälle

``
$(document).ready(function () {
  $("#forgivemanualholdsexpire").attr('checked', true);
});
``

### Palautusosion siivousta (Tritonia)

``
$( document ).ready(function() {
  $( '#circ_returns #return_date_override_fields' ).hide();
  $( '#circ_returns' ).on( 'click', '.show_circ_options_button', function(){
  $( '#return_date_override_fields, .show_circ_options_button' ).toggle();
  });
  $( '#circ_returns #checkin-form #return_date_override_fields' ).before( '<div class="show_circ_options_button"><i class="fa fa-caret-right"></i> Check in options</div><div class="show_circ_options_button" style="display: none;"><i class="fa fa-times"></i> Close check in options</div>');
  $( '#circ_returns #return_date_override_fields' ).prepend( '<h3>Check in options</h3>' );
  $( '#circ_returns #return_date_override_fields' ).append( $( '#circ_returns #checkin_options' ).parents( '.yui-u' ).html() );
  $( '#circ_returns .yui-u > #checkin_options' ).remove();
if( ( $( '#circ_returns #exemptcheck' ).prop("checked") == true ) || ( $( '#circ_returns #return_date_override_remember' ).prop("checked") == true ) || ( $( '#circ_returns #dropboxcheck' ).prop("checked") == true ) || ( $( '#circ_returns #forgivemanualholdsexpire' ).prop("checked") == true ) ) {
  $( '#return_date_override_fields, .show_circ_options_button' ).toggle();
}
});
``

### Kursorin kohdistus oikeaan paikkaan palautussivuilla (Tritonia)

``
$( document ).ready(function() {
  $( '#circ_returns #checkin-form #barcode' ).focus();
});
``

---

## Piilota Perheen lainat -välilehti

``
/* Piilota Perheen lainat -välilehti */
$(document).ready(function() { $("#relatives-issues-tab").parent().hide(); });
``

---

## Asiakkaan muokkausnäyttö

### Syntymäajan asettaminen automaattisesti henkilötunnuksesta

Asettaa automaattisesti syntymäajan kun sotu on laitettu, ja poistutaan sotu-kentästä. Tiketti #3796

``
/* Generoi syntymäaika henkilötunnuksesta */
$(document).ready(function() {
  $('body#pat_memberentrygen.pat input[name="ssn_ssn"]').blur(function() {
     var tmp = $(this).val().trim();
     var re = /^\d{6}[-A]\d{3}[0-9A-Z]$/i;
     if (re.test(tmp)) {
        var day = tmp.substr(0, 2);
        var month = tmp.substr(2, 2);
        var year = tmp.substr(4, 2);
        if (tmp.substr(6, 1) == "-") {
           year = "19" + year;
        } else {
           year = "20" + year;
        }
        $('#dateofbirth').datepicker('setDate', new Date(year+'-'+month+'-'+day));
     }
  });
});
``


### Poista asiakkaan muokkausnäytöllä kentistä ylimääräiset välilyönnit

Näillä kahdella JS:llä voi poistaa asiakkaan muokkausnäytöllä ylimääräiset välilyönnit kentistä. Näytöllä on kahta eriä kenttätyyppiä, minkä vuoksi JS:kin on kaksi. Funktiot poistaa kentistä välilyönnit alusta ja lopusta sekä useammat peräkkäiset välilyönnit välistä.

``
/* poista asiakkaan muokkausnäytön kentistä välilyönnit alusta, lopusta ja useammat peräkkäiset välilyönnit välistä*/
$(document).ready(function() {
  $('body#pat_memberentrygen.pat input').blur(function() {
     var tmp = $(this).val();
     tmp = tmp.replace(/^ +/, '');
     tmp = tmp.replace(/ +$/, '');
     tmp = tmp.replace(/  */g, ' ');     
     $(this).val(tmp);
  });
});
``
``
/* poista asiakkaan muokkausnäytön kentistä välilyönnit alusta, lopusta ja useammat peräkkäiset välilyönnit välistä*/
$(document).ready(function() {
  $('body#pat_memberentrygen.pat textarea').blur(function() {
     var tmp = $(this).val();
     tmp = tmp.replace(/^ +/, '');
     tmp = tmp.replace(/ +$/, '');
     tmp = tmp.replace(/  */g, ' ');     
     $(this).val(tmp);
  });
});
``

### Poista sukunimestä ja etunimestä välilyönnit alusta ja lopusta 

Näiden asemesta on ehkä järkevämpää käyttää yläpuolella olevaa skriptiä.

``
/* poista sukunimestä ja etunimestä välilyönnit alusta ja lopusta */
$(document).ready(function() {
  $('body#pat_memberentrygen.pat input#surname').blur(function() {
     var tmp = $(this).val();
     tmp = tmp.replace(/^ +/, '');
     tmp = tmp.replace(/ +$/, '');
     $(this).val(tmp);
  });
});
$(document).ready(function() {
  $('body#pat_memberentrygen.pat input#firstname').blur(function() {
     var tmp = $(this).val();
     tmp = tmp.replace(/^ +/, '');
     tmp = tmp.replace(/ +$/, '');
     $(this).val(tmp);
  });
});
``

### Aseta syntymäpäiväkalenterin alasvetovalikon vuodet

Raja on 50 edellistä vuotta

``
/* aseta syntymäpäivä-datepickerin dropdownin vuodet */
$(document).ready(function() {
  $("body#pat_memberentrygen.pat #dateofbirth").datepicker({yearRange: "c-50:c+1"});
});
``

### Kopioi matkapuhelinnumero SMS-tekstiviestinumerokenttään

``
$(document).ready(function() {
  $("body#pat_memberentrygen.pat input#mobile").blur(function() {
    var v = $(this).val().trim();
    var e = $("input#SMSnumber");
    if (e) {
       e.val(v);
       e.change();
    }
  });
});
``

### Siirretään Hetu ja tilastoryhmä toiseen paikkaan asiakkaan tietojen muokkaussivulla (Tritonia, päivitetty 2021 kv-Kohaa varten)

``
$( document ).ready(function() {
  $( '#memberentry_identity #othernames' ).parents( 'ol' ).append( '<li>' + $( '#memberentry_patron_attributes #patron_attr_3' ).parents( 'li' ).html() + '</li>' );
  $( '#memberentry_identity #othernames' ).parents( 'ol' ).append( '<li>' + $( '#memberentry_patron_attributes #patron_attr_5' ).parents( 'li' ).html() + '</li>' );
  $( '#pat_memberentrygen #memberentry_patron_attributes #patron_attr_3, #pat_memberentrygen #memberentry_patron_attributes #patron_attr_5' ).parents( 'li' ).remove();
});
``

### Kopioidaan kirjastokortin numero käyttäjätunnus-kenttään

Vaatii, että käyttäjän pitää klikata kirjastokortti-kentän ulkopuolelle (esim. tallentaa tiedot), jotta tieto kopioituu.

``
$(document).ready(function() {
  $("body#pat_memberentrygen.pat input#cardnumber").blur(function() {
    var v = $(this).val().trim();
    var e = $("input#userid");
    if (e) {
       e.val(v);
    }
  });
});
``

### Varaustunnuksen anonymisointi (Other name -kenttään)

Versioon 20.05 ja uudempaan.

``
// Varaustunnuksen automaattinen generointi/anonymisointi - Adapted from Koha-suomi patch for KD-1452 (commit 1c71b272885d9c510630 from https://github.com/KohaSuomi/Koha/ branch master) 
$(document).ready(function(){
    if (window.location.pathname == '/cgi-bin/koha/members/memberentry.pl' && window.location.search.includes("?op=add&") || window.location.search.includes("?op=duplicate&")) {
      var unixepoch = Math.round( (new Date()).getTime() / 10 ).toString();
      var epochdashed = unixepoch.replace( /(....)/g, '$1-').replace(/-$/,'' );
      $('input[id=othernames]').val(epochdashed);
      $("#othernames").focus(function() {
        unixepoch = Math.round( (new Date()).getTime() / 10 ).toString();
        epochdashed = unixepoch.replace( /(....)/g, '$1-').replace(/-$/,'' );
        $('input[id=othernames]').val(epochdashed);
      });
    }
      if (window.location.pathname == '/cgi-bin/koha/members/memberentry.pl' && window.location.search.includes("?op=modify")) {
      $("#othernames").focus(function() {
        unixepoch = Math.round( (new Date()).getTime() / 10 ).toString();
        epochdashed = unixepoch.replace( /(....)/g, '$1-').replace(/-$/,'' );
        $('input[id=othernames]').val(epochdashed);
      });
    }
});
``


### Varaustunnuksen automaattinen täyttö nimen perusteella 

Versioon 20.05 ja uudempaan.


// This file is part of Koha.
//
// Koha is free software; you can redistribute it and/or modify it
// under the terms of the GNU General Public License as published by
// the Free Software Foundation; either version 3 of the License, or
// (at your option) any later version.
//
// Koha is distributed in the hope that it will be useful, but
// WITHOUT ANY WARRANTY; without even the implied warranty of
// MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
// GNU General Public License for more details.
//
// You should have received a copy of the GNU General Public License
// along with Koha; if not, see <http://www.gnu.org/licenses>.
// Adapted from Koha-suomi patch for KD-1452 (commit 1c71b272885d9c510630 from https://github.com/KohaSuomi/Koha/ branch master) 
// Adapted from Koha-suomi patch for KD-205 (commit cd74805e73ead0569abfc158e8b7ac1fe2bedfbe from https://github.com/KohaSuomi/Koha/ branch master

``
$(document).ready(function(){
    if (window.location.pathname == '/cgi-bin/koha/members/memberentry.pl' && window.location.search.includes("?op=add&")) {
      var firstname = $("#entryform").find("#firstname");
      var surname = $("#entryform").find("#surname");
      $("#othernames").focus(function() {
        $("#othernames").val(  surname.val() + ", " + firstname.val()  );
      });
    }
});
``

### Asiakasmääreen piilotus

Asiakasmääreen saa piilotettua muokkausnäytöllä seuraavalla rimpsulla. "patron_attr_1"-kohtaan voi vaihtaa tarvittaessa toisen numeron ykkösen sijalle. Numero kertoo, monesko määre on listalla.

``
$( document ).ready(function() {
  $( '#pat_memberentrygen #memberentry_patron_attributes #patron_attr_1' ).parents( 'li' ).remove();
});
``

### Puhelinnumeron validointi

Versioon 20.05 ja uudempaan. Tarkoitettu korvaamaan järjestelmäasetus ValidatePhoneNumber (kts. #4650)

Uusi versio 19.5.2022

``
/* Puhelinnumeron muodon tarkistus */
// Add additional validation to member add/edit form
$(document).ready(function(){    
   // Replace forms "Save" button 
   // (otherwise form is sent regardless validation checks made here) 
   var language = $(".currentlanguage").text();
   var save_text; 
   if(language == "Suomi"){
     save_text = "Tallenna";
   }else if(language == "Svenska"){
     save_text = "Spara";
   }else {
     save_text = "Save";
   }
  $('#pat_memberentrygen #saverecord').replaceWith('<button class="btn btn-default" id="modified_saverecord"><i class="fa fa-save"></i> '+save_text+'</button>');
   var isvalid = 1;
   $('#phone').blur(function(){
      var error_mes = "";
      var phone = $('#phone').val();
      var phone_reg = /^[+]?([^-\s][0-9]+)+$/;
      if (phone && !phone_reg.test(phone)) {
        error_mes = error_mes + "\nPlease enter a valid phone number.\n";
        $('#phone').after('<label id="phone-error" class="error" for="phone">'+error_mes+'</label>');
        isvalid = 0;
      } else {
      	isvalid = 1;
      }
   });
   $('#mobile').blur(function(){
      var error_mes = "";
      var mobile = $('#mobile').val();
      var mobile_reg = /^[+]?([^-\s][0-9]+)+$/;
      if (mobile && !mobile_reg.test(mobile)) {
        error_mes = error_mes + "\nPlease enter a valid mobile number.\n";
        $('#mobile').after('<label id="mobile-error" class="error" for="mobile">'+error_mes+'</label>');
        isvalid = 0;
      } else {
      	isvalid = 1;
      }
   });
   $('#SMSnumber').blur(function(){
      var error_mes = "";
      var SMSnumber = $('#SMSnumber').val();
      var SMSnumber_reg = /^[+]?([^-\s][0-9]+)+$/;
      if (SMSnumber && !SMSnumber_reg.test(SMSnumber)) {
        error_mes = error_mes + "\nPlease enter a valid SMS number.\n";
        $('#SMSnumber').after('<label id="SMSnumber-error" class="error" for="SMSnumber">'+error_mes+'</label>');
        isvalid = 0;
      } else {
      	isvalid = 1;
      }
   });
   $('#modified_saverecord').click(function(e){
      if(isvalid == 1){
        if( check_form_borrowers() ){
          $("#entryform").submit();
        }
      }
   });
});
``

### Asiakkaan osoitteenmuutospyyntö- täppä oletuksena hyväksy

``
$(document).ready(function () {
if (window.location.pathname == '/cgi-bin/koha/members/members-update.pl') 
$('input:radio[value="approve"]').attr('checked', true); 
});
``

---

## Asiakkaan tiedot näyttö

### Piilota viestin tekijän nimi

``
$("#messages .circ-hlt a").remove();
$("#messages .circ-hlt").each(function( index ){
  var str = $(this).text().replace("(  )", "");
  $(this).text(str);
});
``

---

## Tarkka haku

### Aineistolajirajauksen tyhjennys

``
/* Aineistolajirajauksen tyhjennys tarkassa haussa */
function poista_itype_valinnat() {
 $('body#catalog_advsearch #advsearch-itemtypes input[id^="itypephr"]').each(function() { $(this).prop('checked', false)});
}
$(document).ready(function() {
  $('<a onclick="poista_itype_valinnat(); return false;" href="#">Tyhjennä</a>').insertAfter('body#catalog_advsearch #advsearch-itemtypes h4:first-of-type');
});
``

### Aseta hakukenttien oletukseksi nimeke, tekijä, ja sanahaku

Tiketti #494. Valikkojen oletus on asiasana, joten kolmannen arvoa ei tarvitse erikseen asettaa.

``
$(document).ready(function() {
  var elems = $("body#catalog_advsearch select[name='idx']");
  elems.eq(0).val('ti');
  elems.eq(1).val('au');
});
``

### Linkki Finna-näkymään

  Versioon 20.05 ja uudempaan.

  /* This file is part of Koha.
  /*
  /* Koha is free software; you can redistribute it and/or modify it
  /* under the terms of the GNU General Public License as published by
  /* the Free Software Foundation; either version 3 of the License, or
  /* (at your option) any later version.
  /*
  /* Koha is distributed in the hope that it will be useful, but
  /* WITHOUT ANY WARRANTY; without even the implied warranty of
  /* MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
  /* GNU General Public License for more details.
  /*
  /* You should have received a copy of the GNU General Public License
  /* along with Koha; if not, see <http://www.gnu.org/licenses>.


``
$(document).ready(function() {
	if (window.location.pathname == '/cgi-bin/koha/catalogue/detail.pl') {
		var details_elem = document.getElementById("catalogue_detail_biblio");
		var span_elem = document.createElement("span");
		span_elem.className = "results_summary";
		var link_elem = document.createElement("a");
		var params = new URLSearchParams(window.location.search);
		var biblionumber = parseInt(params.get("biblionumber"));
		link_elem.href = "https://kohatesti.finna-test.fi/kvkoha1/Record/kvkoha." + biblionumber;
                link_elem.target = "_blank";
		var link_text = document.createTextNode("Avaa Finnassa");
		link_elem.appendChild(link_text);
		span_elem.appendChild(link_elem);
		details_elem.appendChild(span_elem);
	}
});
``

### Linkki Finna-näkymään (nappula) (Tritonia 2020)

``
$( document ).ready(function() {
if (window.location.pathname == '/cgi-bin/koha/catalogue/detail.pl') {
        /*var details_elem = document.getElementById("catalogue_detail_biblio");
        var span_elem = document.createElement("span");
        span_elem.className = "results_summary";
        var link_elem = document.createElement("a");
        link_elem.href = "https://tritonia.finna.fi/Record/tria." + biblionumber;
        var link_text = document.createTextNode("Open in Finna");
        link_elem.appendChild(link_text);
        span_elem.appendChild(link_elem);
        details_elem.appendChild(span_elem);*/
  		var linktext = 'Avaa Finnassa';
        if( $( '#changelanguage .currentlanguage' ).text() == 'English' ) {
        	linktext = 'Open in Finna';
        } else if ( $( '#changelanguage .currentlanguage' ).text() == 'Svenska' ) {
        	linktext = 'Öppna i Finna';
        }
        var params = new URLSearchParams(window.location.search);
        var biblionumber = parseInt(params.get("biblionumber"));
  		$( '#catalog_detail #toolbar' ).prepend( '<a href="https://tritonia.finna.fi/Record/tria.' + biblionumber + '" class="btn" style="float: right;" target="_blank"><i class="fa fa-external-link"></i> ' + linktext + '</a>' );
}
});
``

### Indeksointityöryhmän tekemät tiedonhaun mukautukset

Indeksointityöryhmä ideoi mukautuksia tiedonhakun hakusivulle. Alla siitä syntyneet muutokset.

``
$(document).ready(function() {
    if ( $('html').attr('lang') == 'fi-FI') {
      $("#advsearch-tab-mtype a").text("Aineistotyyppi"); /* MTYPE auktorisoituarvo tarkassa haussa */
      $("#advsearch-tab-subloc a").text("Hyllytarkenne"); /* SUBLOC auktorisoituarvo tarkassa haussa */
      $("#advsearch-tab-agelevel a").text("Ikärajat"); /* AGELEVEL auktorisoituarvo tarkassa haussa */
      $("#searchterms select").append(new Option('YKL-luokitus', 'other-classification')); /* Lisää uuden valinnan YKL-luokitus */
      $("#searchterms select").append(new Option('UDC-luokitus', 'udc-classification')); /* Lisää uuden valinnan UDC-luokitus */
      $("#subtype select option[value='mus:i'").parent().append(new Option('Päivittyvä julkaisu', 'bib-level:i')); /*Lisää lisärajoitukset valikkoon uuden arvon */
      $("#subtype select option[value='mus:i'").parent().append(new Option('Kausijulkaisu', 'bib-level:s')); /*Lisää lisärajoitukset valikkoon uuden arvon */
    }
    else if ( $('html').attr('lang') == 'sv-SE') {
      $("#advsearch-tab-mtype a").text("Materialtyp");
      $("#advsearch-tab-subloc a").text("Underplats");
      $("#advsearch-tab-agelevel a").text("Åldersgränser");
      $("#searchterms select").append(new Option('YKL-klassification', 'other-classification'));
      $("#searchterms select").append(new Option('UDC-klassification', 'udc-classification'));
      $("#subtype select option[value='mus:i'").parent().append(new Option('Päivittyvä julkaisu', 'bib-level:i'));
      $("#subtype select option[value='mus:i'").parent().append(new Option('Kausijulkaisu', 'bib-level:s'));
    }
    else if ( $('html').attr('lang') == 'en') {
      $("#advsearch-tab-mtype a").text("Material type");
      $("#advsearch-tab-subloc a").text("Sub location"); 
      $("#advsearch-tab-agelevel a").text("Age levels");
      $("#searchterms select").append(new Option('Other classification', 'other-classification'));
      $("#searchterms select").append(new Option('UDC classification', 'udc-classification'));
      $("#subtype select option[value='mus:i'").parent().append(new Option('Integrating resource', 'bib-level:i'));
      $("#subtype select option[value='mus:i'").parent().append(new Option('Serial', 'bib-level:s'));
    }
    $("#searchterms select option[value='location']").val('loc'); /* Muuttaa location-arvon loc-arvoksi "Hakusanat"-valikossa */
});
``

---

## Luettelointi, niteiden muokkaus ja kausijulkaisut


### Luettelointinäkymässä highlight työstettävälle tagille (ja pois kun klikkaa taustaa) (Tritonia)

``
$( document ).ready(function() {
  $( '#cat_addholding .tag, #cat_addbiblio .tag' ).on( 'click', function( event ){
  $( '.tag' ).removeClass( 'new_active_tag' );
  $( this ).addClass( 'new_active_tag' );
event.stopPropagation();
});
  $( '#cat_addholding #doc, #cat_addbiblio #doc' ).on( 'click', function(event){
  $( '.tag' ).removeClass( 'new_active_tag' );
});
``

### Luettelointinäkymässä lisätään lukitulle tagi-inputille lukkoikoni (Tritonia)

``
$( '#cat_addbiblio .tag .subfield_line .input_marceditor.readonly' ).after( '<i class="fa fa-lock"></i>' );
``

### Valitaan cataloging-etusivulla "search the catalog" -haku "cataloging search" -haun sijasta (joka piilotetaan) (Tritonia)

``
$( document ).ready(function() {
$( '#cat_addbooks #header_search li[aria-controls="addbooks_search"]' ).hide();
$( '#cat_addbooks #header_search' ).tabs( { active: 4 } );
$( '#cat_addbooks #header_search #catalog_search #cat-search-block #search-form' ).focus();
});
``

### Lisätään holding id näkyville tietueen holdings-listaukseen (Tritonia)

``
$( document ).ready(function() {
  $( '#catalog_detail .summaryholdings_table thead tr' ).append( '<th>Holding ID</th>' );
  $( '#catalog_detail .summaryholdings_table tbody tr' ).each(function(){
  $( this ).append( '<td>' + $( this ).children( '.actions' ).children( '.delete' ).attr( 'href' ).split("holding_id=").pop() + '</td>' );
});
``


### Siirretään item-listaus sivun loppuun itemin muokkaussivulla (Tritonia, päivitetty 2020)

``
$( document ).ready(function() {
    $( '#cat_additem #cataloguing_additem_itemlist' ).after( $( '#cat_additem #cataloguing_additem_itemlist #itemst_wrapper' ).parents( 'div' ).html() );
	$( '#cat_additem #cataloguing_additem_itemlist #itemst_wrapper' ).parent( 'div' ).hide();*/
	$( '#cat_additem #cataloguing_additem_itemlist' ).prepend( $( '#cat_additem #cataloguing_additem_itemlist>.row' ) );
});
``

### Luettelointivalikon pysyminen sivun ylälaidassa MARC-näkymässä (Tritonia 2020)

``
$( document ).ready(function() {
$(window).bind('scroll', function () {
    if ($(window).scrollTop() > 150) {
        $('#cat_addbiblio #toolbar').addClass('fixed_cataloging_menu');
    } else {
        $('#cat_addbiblio #toolbar').removeClass('fixed_cataloging_menu');
    }
});
``

### Lisätään nidenäkymän tietojen otsikoihin rivivälejä (Tritonia 2020)

``
$( document ).ready(function() {
$( '#catalogue_detail_biblio .results_summary .label' ).before( '<div style="width: 100%; height: 1px;"></div>' );
});
``

### Poistetaan turhat hakaset "Edit item" -napista (Tritonia)

``
$( document ).ready(function() {
  $( '#catalog_moredetail #catalogue_detail_biblio .yui-g .listgroup h4 a' ).each( function() {
  $( this ).text( $( this ).text().replace('[', '') );
  $( this ).text( $( this ).text().replace(']', '') );
  });
});
``

### Poistetaan ylimääräiset välilyönnit niteen muokkausnäytöllä

``
/* poista niteen muokkausnäytön kentistä välilyönnit alusta, lopusta ja useammat peräkkäiset välilyönnit välistä*/
$(document).ready(function() {
  $('body#cat_additem.cat input').blur(function() {
     var tmp = $(this).val();
     tmp = tmp.replace(/^ +/, '');
     tmp = tmp.replace(/ +$/, '');
     tmp = tmp.replace(/  */g, ' ');
     $(this).val(tmp);
  });
});
``

### Poistetaan ylimääräiset välilyönnit kausijulkaisujen vastaantotossa

Skripti poistaa ylimääräiset välilyönnit sekä tarkistaa, että sarjanumero on muodossa "vuosi : numero". Jos vuoden jälkeen puuttuu välilyönti, käytännössä se lisätään sinne. Tarkistus tehdään kaikkiin nidekenttiin, mutta korjaus ei "tartu", jos kentän alussa ei ole vuosinumeroa.

``
/* poista kausijulkaisun vastaanottonäytön kentistä välilyönnit alusta, lopusta ja useammat peräkkäiset välilyönnit välistä*/
$(document).ready(function() {
  $('body#ser_serials-edit.ser input').blur(function() {
     var tmp = $(this).val();
     tmp = tmp.replace(/^ +/, '');
     tmp = tmp.replace(/ +$/, '');
     tmp = tmp.replace(/  */g, ' ');
     tmp = tmp.replace(/(^[1-2][0-9]{3}) *: */, '$1 : ');
     $(this).val(tmp);
  });
});
``

### Niteiden eräpoistossa täppä kohtaan "Poista tietueet.."

Skripti laittaa niteiden eräpoistossa valmiiksi täpän kohtaan "Poista tietueet, jos kaikki niteet poistettu". Näin todennäköisemmin tietokantaan ei jää roikkumaan niteettömiä tietueita.

Versio: 21.11

Tarpeellisuus: suositeltava

``
/* Laita niteiden eräpoistossa täppä kohtaan "Poista tietueet, jos kaikki niteet poistettu" */
$(document).ready(function () {
  $("#del_records").attr('checked', true);
});
``

---

## Yleiset

### Piilota Uusinta-välilehti yläosan hakukentästä

``
$(document).ready(function () {
  $( "li[aria-controls='renew_search']" ).hide();
});
``

### Koha logo ylävalikkoon (Tritonia)

``
$( document ).ready(function() {
  $( '#header #toplevelmenu' ).before( '<a href="/cgi-bin/koha/mainpage.pl" class="new_koha_toplogo" alt="Koha home"><img src="https://www.tritonia.fi/img/koha_logo_2019.png" alt="Koha home"></a>' );
});
``

### Kielivalinta ylävalikkoon ja piilotetaan apusivulinkki (Tritonia, päivitetty 2020)

``
$( document ).ready(function() {
$( '#changelanguage' ).hide();
var $langtext = 'Kieli';
if( $( '.currentlanguage' ).text() == 'English' ) {
$langtext = 'Language';
} else if ( $( '.currentlanguage' ).text() == 'Svenska' ) {
$langtext = 'Språk';
}
$( '#user-menu.nav.navbar-nav.navbar-right' ).append( '<li class="dropdown" id="new_lang_dropdown"><a href="#" id="drop99" role="button" class="dropdown-toggle" data-toggle="dropdown">' + $langtext + ' <b class="caret"></b></a><ul class="dropdown-menu" role="menu" aria-labelledby="drop99">' + $( '#changelanguage ul.navbar-nav' ).html() + '</ul>' );
$( '#user-menu .currentlanguage' ).append( ' <i class="fa fa-check"></i>' );  
});
``

### Etusivun ikonien parempi asettelu (Tritonia, pävitetty 2020)

``
$( document ).ready(function() {
$( '#main_intranet-main #container-main' ).append( '<div id="new_icon_container"></div>' );
$( '#main_intranet-main #container-main .row:first-child' ).hide();
$( '#main_intranet-main .biglinks-list li' ).each(function(){
	$( '#main_intranet-main #new_icon_container' ).append( $( this ).html() );
});
$( '#main_intranet-main #new_icon_container' ).prepend( $( '#main_intranet-main #area-pending' ).parent( 'div' ).html() );

});
``

### Tyhjennä Hae tietokannasta -hakukenttä

``
$(document).ready(function() {
      localStorage.removeItem("searchbox_value");
});
``

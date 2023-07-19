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

[Muutokseen liittyvä tiketti](https://tiketti.koha-suomi.fi/issues/4343)



## Lainaus

### Alt+p tulostaa kuitin

Tarpeellisuus: Suositeltava <br />
Versio: 22.11

```
/// ALKU ///
/* When returning books, if there is an input with onclick handler that starts with "Dopop",
   allow pressing alt+p to click on that input. That should be a "print a slip" -type thing. */

$(document).ready(function () {
  $(document).bind('keypress', function(e) {
     var code = e.keyCode || e.which;
     if (code == 112 && e.altKey) { /* alt+p */
        e.preventDefault();
        $('body#circ_returns input.print[onclick^=Dopop]').trigger("click");
     }
  });
});
/// LOPPU ///
```

## Palautus

### "Poista käsin poistettujen varausten maksut" -täppä päälle

Tarpeellisuus: Suositeltava<br />
Versio: 22.11

```
/// ALKU ///

/* Laita raksi "Poista käsin poistettujen varausten maksut" -kohtaa palautuksessa. Tällä estetään noutamattoman varauksen maksun syntyminen, kun varaus noudettavissa oleva varaus poistetaan palautuksen kautta. Huom! Ei toimi, jos palautus tehdään muualla kuin Palautus-sivulla. */
$(document).ready(function () {
  $("#forgivemanualholdsexpire").attr('checked', true);
});

/// LOPPU ///
```

### Palautusosion siivousta (Tritonia)

Tarpeellisuus: ?<br />
Versio: ?

```
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
```

### Kursorin kohdistus oikeaan paikkaan palautussivuilla (Tritonia)

Tarpeellisuus: ?<br />
Versio: ?

```
$( document ).ready(function() {
  $( '#circ_returns #checkin-form #barcode' ).focus();
});
```

---

## Piilota Perheen lainat -välilehti

Tarpeellisuus: Vapaaehtoinen<br />
Versio: 22.11

```
/// ALKU ///
/* Piilota Perheen lainat -välilehti */
$(document).ready(function() { $("#relatives-issues-tab").parent().hide(); });
/// LOPPU ///
```

---

## Asiakkaan muokkausnäyttö

### Henkilötunnuksen lisäys sotusiiloon ja syntymäajan asettaminen automaattisesti henkilötunnuksesta

Lisää asiakkaan muokkausnäytölle Henkilötunnus-kentän ja sen viennin sotusiiloon sekä asettaa automaattisesti syntymäajan henkilötunnuksen perusteella.

Tarpeellisuus: Suositeltava <br />
Versio: 22.11

```
/// ALKU ///
/// Lisätään asiakkaan lisäys/muokkausnäytölle hetun lisäysmahdollisuus. Rimpsu myös muodostaa syntymäaika-kenttään tiedon henkilötunnuksen perusteella. ///
$(document).ready(function() {
    $("#entryform #memberentry_identity ol").before('<ol><li><label>Lisää hetu:</label><input type="text" id="ssnvalue"></input><button onclick="addSSN(event)">Tallenna</button></li></ol><hr/>');
});
function addSSN(event) {
    event.preventDefault();
    $.ajax({
        url: "/api/v1/contrib/kohasuomi/ssn/add",
        type: "POST",
        dataType: "json",
        contentType: "application/json; charset=utf-8",
        data: JSON.stringify({
            token: 'yS390RiiReRhd2qXBmEIkD',
            ssn: $("#ssnvalue").val()
        }),
        success: function(result) {
            alert(result.msg);
            var entry = $("#ssnvalue").val().trim();
            var dateofbirth = ((entry.substr(6, 1) == "-" ? "19": "20") + entry.substr(4, 2) + "-" + entry.substr(2, 2) + "-" + entry.substr(0, 2));
            var fp = document.querySelector("#dateofbirth")._flatpickr;
            fp.setDate(dateofbirth);
            $("#patron_attr_5").val(result.ssnkey); //Tämä id on katsottava järjestelmäkohtaisesti
        },
        error: function(err) {
            var message = JSON.parse(err.responseText).message;
            if ($.isNumeric(message)) {
                if (window.confirm('Asiakas on jo olemassa! Paina OK siirtyäksesi tietoihin.')) {
                    window.open('/cgi-bin/koha/members/moremember.pl?borrowernumber=' + message, '_blank');
                }
            } else {
                alert(message);
            }
        }
    });
}
/// LOPPU ///
```


### Poista asiakkaan muokkausnäytöllä kentistä ylimääräiset välilyönnit

Näillä kahdella JS:llä voi poistaa asiakkaan muokkausnäytöllä ylimääräiset välilyönnit kentistä. Näytöllä on kahta eriä kenttätyyppiä, minkä vuoksi JS:kin on kaksi. Funktiot poistaa kentistä välilyönnit alusta ja lopusta sekä useammat peräkkäiset välilyönnit välistä.

Tarpeellisuus: Suositeltava<br />
Versio: 22.11

```
/// ALKU ///
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
/// LOPPU ///
```

```
/// ALKU ///
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
/// LOPPU ///
```


### Aseta syntymäpäiväkalenterin alasvetovalikon vuodet

Raja on 50 edellistä vuotta.

Tarpeellisuus: Ei tarpeellinen versiossa 22.11


```
/// ALKU ///
/* aseta syntymäpäivä-datepickerin dropdownin vuodet */
$(document).ready(function() {
  $("body#pat_memberentrygen.pat #dateofbirth").datepicker({yearRange: "c-50:c+1"});
});
/// LOPPU ///
```

### Kopioi matkapuhelinnumero SMS-tekstiviestinumerokenttään

Tämä on korvattu tietokannan triggerillä.

```
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
```

### Siirretään Hetu ja tilastoryhmä toiseen paikkaan asiakkaan tietojen muokkaussivulla (Tritonia, päivitetty 2021 kv-Kohaa varten)

Tarpeellisuus: ?<br />
Versio: ?

```
$( document ).ready(function() {
  $( '#memberentry_identity #othernames' ).parents( 'ol' ).append( '<li>' + $( '#memberentry_patron_attributes #patron_attr_3' ).parents( 'li' ).html() + '</li>' );
  $( '#memberentry_identity #othernames' ).parents( 'ol' ).append( '<li>' + $( '#memberentry_patron_attributes #patron_attr_5' ).parents( 'li' ).html() + '</li>' );
  $( '#pat_memberentrygen #memberentry_patron_attributes #patron_attr_3, #pat_memberentrygen #memberentry_patron_attributes #patron_attr_5' ).parents( 'li' ).remove();
});
```

### Kopioidaan kirjastokortin numero käyttäjätunnus-kenttään

Tämä on korvattu tietokantatriggerillä.

Vaatii, että käyttäjän pitää klikata kirjastokortti-kentän ulkopuolelle (esim. tallentaa tiedot), jotta tieto kopioituu.

```
$(document).ready(function() {
  $("body#pat_memberentrygen.pat input#cardnumber").blur(function() {
    var v = $(this).val().trim();
    var e = $("input#userid");
    if (e) {
       e.val(v);
    }
  });
});
```

### Varaustunnuksen generointi

Skripti generoi HOLDID-asiakasmääreeseen anonyymin varaustunnisteen, joka on käytännössä UNIX-aikaleima.

Tarpeellisuus: Suositeltava<br />
Versio: 22.11

```
/// ALKU ///

// Varaustunnuksen automaattinen generointi/anonymisointi - Adapted from Koha-suomi patch for KD-1452 (commit 1c71b272885d9c510630 from https://github.com/KohaSuomi/Koha/ branch master)
// Tämä generoi patron_attr_2-kenttään. Tarkista oikea attribuutti asiakkaan muokkaussivulta selaimen Tarkista-toiminnolla. Jos attribuutin arvo muuttuu, pitää se muuttaa jokaiseen kohtaan, jossa se mainitaan. //

$(document).ready(function(){
    if (window.location.pathname == '/cgi-bin/koha/members/memberentry.pl' && window.location.search.includes("?op=add&") || window.location.search.includes("?op=duplicate&")) {
      var unixepoch = Math.round( (new Date()).getTime() / 10 ).toString();
      var epochdashed = unixepoch.replace( /(....)/g, '$1-').replace(/-$/,'' );
      $('textarea#patron_attr_2').val(epochdashed);

      $("#patron_attr_2").focus(function() {
        unixepoch = Math.round( (new Date()).getTime() / 10 ).toString();
        epochdashed = unixepoch.replace( /(....)/g, '$1-').replace(/-$/,'' );
        $('textarea#patron_attr_2').val(epochdashed);
      });
    }

      if (window.location.pathname == '/cgi-bin/koha/members/memberentry.pl' && window.location.search.includes("?op=modify")) {
      $("#patron_attr_2").focus(function() {
        unixepoch = Math.round( (new Date()).getTime() / 10 ).toString();
        epochdashed = unixepoch.replace( /(....)/g, '$1-').replace(/-$/,'' );
        $('textarea#patron_attr_2').val(epochdashed);
      });
    }
});

/// LOPPU ///

```


### Varaustunnuksen automaattinen täyttö nimen perusteella 

Versioon 20.05 ja uudempaan.

```
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


$(document).ready(function(){
    if (window.location.pathname == '/cgi-bin/koha/members/memberentry.pl' && window.location.search.includes("?op=add&")) {
      var firstname = $("#entryform").find("#firstname");
      var surname = $("#entryform").find("#surname");
      $("#othernames").focus(function() {
        $("#othernames").val(  surname.val() + ", " + firstname.val()  );
      });
    }
});
```

### Asiakasmääreen piilotus

Asiakasmääreen saa piilotettua muokkausnäytöllä seuraavalla rimpsulla. "patron_attr_1"-kohtaan voi vaihtaa tarvittaessa toisen numeron ykkösen sijalle. Numero kertoo, monesko määre on listalla.

Tarpeellisuus: Vapaaehtoinen<br />
Versio: ?

```
/// ALKU ///
$( document ).ready(function() {
  $( '#pat_memberentrygen #memberentry_patron_attributes #patron_attr_1' ).parents( 'li' ).remove();
});
/// LOPPU ///
```

### Puhelinnumeron validointi ja viestitäppien poisto, jos puhelinnumero tai sähköpostiosoite puuttuu

Versioon 20.05 ja uudempaan. Tarkoitettu korvaamaan järjestelmäasetus ValidatePhoneNumber (kts. #4650).

Tässä on kaksi toiminnallisuutta yhdessä, koska ne ovat riippuvaisia toisistaan toiminnallisesti.

Tarpeellisuus: Suositeltava
Versio: 22.11

```
/// ALKU ///
/* Puhelinnumeron muodon tarkistus ja email/sms-viestitäpät*/
// Add additional validation to member add/edit form
$(document).ready(function () {
  if (window.location.href.indexOf("members/memberentry.pl") > -1) {
    // Replace forms "Save" button 
    // (otherwise form is sent regardless validation checks made here) 
    $('#pat_memberentrygen #saverecord').replaceWith('<button class="btn btn-default" id="modified_saverecord"><i class="fa fa-save"></i> Save</button>');

    var isvalid = 1;

    $('#phone').blur(function () {
      var error_mes = "";
      var phone = $('#phone').val();
      var phone_reg = /^((90[0-9]{3})?0|\+358)(?!(100|20(0|2(0|[2-3])|9[8-9])|300|600|700|708|75(00[0-3]|(1|2)\d{2}|30[0-2]|32[0-2]|75[0-2]|98[0-2])))(4|50|10[1-9]|20(1|2(1|[4-9])|[3-9])|29|30[1-9]|71|73|75(00[3-9]|30[3-9]|32[3-9]|53[3-9]|83[3-9])|2|3|5|6|8|9|1[3-9])(\d?){4,19}\d$/;

      if (phone && !phone_reg.test(phone)) {
        error_mes = error_mes + "\nPlease enter a valid phone number.\n";
        $('#phone').after('<label id="phone-error" class="error" for="phone">' + error_mes + '</label>');
        isvalid = 0;
      } else {
        isvalid = 1;
      }
    });

    $('#mobile').blur(function () {
      var error_mes = "";
      var mobile = $('#mobile').val();
      var mobile_reg = /^((90[0-9]{3})?0|\+358)(?!(100|20(0|2(0|[2-3])|9[8-9])|300|600|700|708|75(00[0-3]|(1|2)\d{2}|30[0-2]|32[0-2]|75[0-2]|98[0-2])))(4|50|10[1-9]|20(1|2(1|[4-9])|[3-9])|29|30[1-9]|71|73|75(00[3-9]|30[3-9]|32[3-9]|53[3-9]|83[3-9])|2|3|5|6|8|9|1[3-9])(\d?){4,19}\d$/;

      if (mobile && !mobile_reg.test(mobile)) {
        error_mes = error_mes + "\nPlease enter a valid mobile number.\n";
        $('#mobile').after('<label id="mobile-error" class="error" for="mobile">' + error_mes + '</label>');
        isvalid = 0;
      } else {
        isvalid = 1;
      }
    });

    $('#SMSnumber').blur(function () {
      var error_mes = "";
      var SMSnumber = $('#SMSnumber').val();
      var SMSnumber_reg = /^((90[0-9]{3})?0|\+358)(?!(100|20(0|2(0|[2-3])|9[8-9])|300|600|700|708|75(00[0-3]|(1|2)\d{2}|30[0-2]|32[0-2]|75[0-2]|98[0-2])))(4|50|10[1-9]|20(1|2(1|[4-9])|[3-9])|29|30[1-9]|71|73|75(00[3-9]|30[3-9]|32[3-9]|53[3-9]|83[3-9])|2|3|5|6|8|9|1[3-9])(\d?){4,19}\d$/;

      if (SMSnumber && !SMSnumber_reg.test(SMSnumber)) {
        error_mes = error_mes + "\nPlease enter a valid SMS number.\n";
        $('#SMSnumber').after('<label id="SMSnumber-error" class="error" for="SMSnumber">' + error_mes + '</label>');
        isvalid = 0;
      } else {
        isvalid = 1;
      }
    });

    $('#modified_saverecord').click(function (e) {
      var text = "";
      if (isvalid == 1) {
        //Vahvista viestitäppien poisto popupissa jos sähköposti/matkapuhelin puuttuu

        if (!$('#email').val()) {
          if ($('#email1').attr('checked') || $('#email2').attr('checked') || $('#email3').attr('checked') || $('#email4').attr('checked') || $('#email5').attr('checked') || $('#email6').attr('checked') || $('#email10').attr('checked')) {
            text = "Sähköpostiosoite puuttuu. Sähköposti-viestiasetukset poistetaan.\n";
            $('#email1').removeAttr('checked');
            $('#email1').attr('disabled', 'disabled');
            $('#email2').removeAttr('checked');
            $('#email2').attr('disabled', 'disabled');
            $('#email3').removeAttr('checked');
            $('#email3').attr('disabled', 'disabled');
            $('#email4').removeAttr('checked');
            $('#email4').attr('disabled', 'disabled');
            $('#email5').removeAttr('checked');
            $('#email5').attr('disabled', 'disabled');
            $('#email6').removeAttr('checked');
            $('#email6').attr('disabled', 'disabled');
            $('#email10').removeAttr('checked');
            $('#email10').attr('disabled', 'disabled');
          }
        }
        if (!$('#mobile').val()) {
          if ($('#sms1').attr('checked') || $('#sms4').attr('checked') || $('#sms10').attr('checked')) {
            text += "Matkapuhelinnumero puuttuu. Tekstiviesti-viestiasetukset poistetaan.";
            $('#sms1').removeAttr('checked');
            $('#sms1').attr('disabled', 'disabled');
            $('#sms4').removeAttr('checked');
            $('#sms4').attr('disabled', 'disabled');
            $('#sms10').removeAttr('checked');
            $('#sms10').attr('disabled', 'disabled');
          }
        }

        if (text.charAt(0)){
          alert(text);
        }
        
        $("#entryform").submit();
      }
    }
    );
  }
});
/// LOPPU ///
```

### Apuskripti puhelinnumeron tarkistus/viestitäppä -skriptille

Tämä skripti tarvitaan edellisen kaveriksi, jotta viestitäppien poisto onnistuu ensimmäisellä tallennuskerralla. [Liittyy tikettiin 538](https://github.com/KohaSuomi/Koha/issues/538).

Tarpeellisuus: Suositeltava
Versio: 22.11

```
///ALKU///
/* Tiketti 538 Lisää viestitäppiin checked-arvot jo ne laitettaessa, jolloin viestiasetusten tarkistus onnistuu ensimmäisellä asiakastietojen tallennuskerralla */
$(document).ready(function () {
    if (window.location.href.indexOf("members/memberentry.pl") > -1) {
var classA = Array.from(document.getElementsByClassName("pmp_sms"))
     ,classB = Array.from(document.getElementsByClassName("pmp_email"))
     ,result = Array.from(new Set(classA.concat(classB)));

for (var i = 0; i < result.length; i ++) {
      result[i].onclick = function(){
    var checkStatus = $(this).is(':checked');   

    if(checkStatus){
        $(this).attr('checked', 'checked');
    }
    else{
        $(this).removeAttr('checked');
    }
   };
  }
}});
///LOPPU///
```

### Asiakkaan osoitteenmuutospyyntö- täppä oletuksena hyväksy

Tarpeellisuus: Vapaaehtoinen<br />
Versio: ?

```
$(document).ready(function () {
if (window.location.pathname == '/cgi-bin/koha/members/members-update.pl') 
$('input:radio[value="approve"]').attr('checked', true); 
});
```

---

## Asiakkaan tiedot näyttö

### Piilota viestin tekijän nimi Tiedot-näytöllä

Tarpeellisuus: Vapaaehtoinen <br />
Versio: 22.11

```
/// ALKU ///

/* Piilota viestin tekijän nimi asiakkaan Tiedot-näytöllä */
$("#messages .circ-hlt a").remove();
$("#messages .circ-hlt").each(function( index ){
  var str = $(this).text().replace("(  )", "");
  $(this).text(str);
});

/// LOPPU ///
```

---

## Tarkka haku

### Aineistolajirajauksen tyhjennys

Tarpeellisuus: Vapaaehtoinen<br />
Versio: ?

```
/* Aineistolajirajauksen tyhjennys tarkassa haussa */
function poista_itype_valinnat() {
 $('body#catalog_advsearch #advsearch-itemtypes input[id^="itypephr"]').each(function() { $(this).prop('checked', false)});
}
$(document).ready(function() {
  $('<a onclick="poista_itype_valinnat(); return false;" href="#">Tyhjennä</a>').insertAfter('body#catalog_advsearch #advsearch-itemtypes h4:first-of-type');
});
```

### Aseta hakukenttien oletukseksi nimeke, tekijä, ja sanahaku

Tiketti #494. Valikkojen oletus on asiasana, joten kolmannen arvoa ei tarvitse erikseen asettaa.

Tarpeellisuus: Vapaaehtoinen<br />
Versio: 22.11

```
/// ALKU ///

/* Tarkka-haku ja Sanahaku-oletustermit korvataan Nimeke, Tekijä, Asiasana */
$(document).ready(function() {
  var elems = $("body#catalog_advsearch select[name='idx']");
  elems.eq(0).val('ti');
  elems.eq(1).val('au');
  elems.eq(2).val('su');
});

/// LOPPU ///
```

### Linkki Finna-näkymään

Tämä lisää tietueen perustiedot-näytölle valikkoriville viimeiseksi Avaa Finnassa -nappulan, joka vie oman kimpan Finnaan saman teoksen tietoihin.

Tarpeellisuus: Suositeltava<br />
Versio: 22.11

```
 /// ALKU ///
/// Lisää tietueen perustiedot-näytölle valikkoriville loppuun Avaa Finnassa -nappula. Muista vaihtaa osoitteisiin oman kimpan tunnisteet Vaaran tunnisteiden sijaan. ///

$( document ).ready(function() {
if (window.location.pathname == '/cgi-bin/koha/catalogue/detail.pl') {
        /*var details_elem = document.getElementById("catalogue_detail_biblio");
        var span_elem = document.createElement("span");
        span_elem.className = "results_summary";
        var link_elem = document.createElement("a");
        link_elem.href = "https://vaara.finna.fi/Record/vaarakirjastot." + biblionumber;
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
  		$( '#catalog_detail #toolbar' ).append( '<div class="btn-group"> <a href="https://vaara.finna.fi/Record/vaarakirjastot.' + biblionumber + '" class="btn btn-default" target="_blank"><i class="fa fa-external-link"></i> ' + linktext + '</a></div>' );
}
});

/// LOPPU ///
```

### Linkki Finna-näkymään (nappula) (Tritonia 2020)

```
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
```

### Indeksointityöryhmän tekemät tiedonhaun mukautukset

Indeksointityöryhmä ideoi mukautuksia tiedonhakun hakusivulle. Alla siitä syntyneet muutokset.

Tarpeellisuus: Suositelta<br />
Versio: 22.11

```
/// ALKU ///

/* Näillä rimpsuilla tehdään tiedonhakuun Indeksointi-työryhmän päättämät muutokset. Asetetaan otsikot eri kielillä aineistotyyppi-, hyllytarkenne- ja ikärajavälilehdille tiedonhaussa. Lisätään alasvetovalikoihin YKL, UDK, Päivittyvä julkaisu ja Kausijulkaisu */
$(document).ready(function() {

    if ( $('html').attr('lang') == 'fi-FI') {
      $("#advsearch-tab-mtype a").text("Aineistotyyppi"); /* MTYPE auktorisoituarvo tarkassa haussa */
      $("#advsearch-tab-subloc a").text("Hyllytarkenne"); /* SUBLOC auktorisoituarvo tarkassa haussa */
      $("#advsearch-tab-agelevel a").text("Ikärajat"); /* AGELEVEL auktorisoituarvo tarkassa haussa */
      $("#advsearch-tab-bib-level a").text("Emokohde/Osakohde"); /* bib-level auktorisoituarvo tarkassa haussa */
      $("#searchterms select").append(new Option('YKL-luokitus', 'other-classification')); /* Lisää uuden valinnan YKL-luokitus */
      $("#searchterms select").append(new Option('UDK-luokitus', 'udc-classification')); /* Lisää uuden valinnan UDK-luokitus */
      $("#subtype select option[value='mus:i'").parent().append(new Option('Päivittyvä julkaisu', 'bib-level:i')); /*Lisää lisärajoitukset valikkoon uuden arvon */
      $("#subtype select option[value='mus:i'").parent().append(new Option('Kausijulkaisu', 'bib-level:s')); /*Lisää lisärajoitukset valikkoon uuden arvon */
    }
    else if ( $('html').attr('lang') == 'sv-SE') {
      $("#advsearch-tab-mtype a").text("Materialtyp");
      $("#advsearch-tab-subloc a").text("Underplats");
      $("#advsearch-tab-agelevel a").text("Åldersgränser");
      $("#advsearch-tab-bib-level a").text("Huvudobjekt/Delobjekt");
      $("#searchterms select").append(new Option('YKL-klassification', 'other-classification'));
      $("#searchterms select").append(new Option('UDC-klassification', 'udc-classification'));
      $("#subtype select option[value='mus:i'").parent().append(new Option('Publikation som uppdateras', 'bib-level:i'));
      $("#subtype select option[value='mus:i'").parent().append(new Option('Seriell publikation', 'bib-level:s'));
    }
    else if ( $('html').attr('lang') == 'en') {
      $("#advsearch-tab-mtype a").text("Material type");
      $("#advsearch-tab-subloc a").text("Sub location"); 
      $("#advsearch-tab-agelevel a").text("Age levels");
      $("#advsearch-tab-bib-level a").text("Child/monographic record");
      $("#searchterms select").append(new Option('Other classification', 'other-classification'));
      $("#searchterms select").append(new Option('UDC classification', 'udc-classification'));
      $("#subtype select option[value='mus:i'").parent().append(new Option('Integrating resource', 'bib-level:i'));
      $("#subtype select option[value='mus:i'").parent().append(new Option('Serial', 'bib-level:s'));
    }

    $("#searchterms select option[value='location']").val('loc'); /* Muuttaa location-arvon loc-arvoksi "Hakusanat"-valikossa */
});

/// LOPPU ///
```

---

## Luettelointi, niteiden muokkaus ja kausijulkaisut


### Luettelointinäkymässä highlight työstettävälle tagille (ja pois kun klikkaa taustaa) (Tritonia)

```
$( document ).ready(function() {
  $( '#cat_addholding .tag, #cat_addbiblio .tag' ).on( 'click', function( event ){
  $( '.tag' ).removeClass( 'new_active_tag' );
  $( this ).addClass( 'new_active_tag' );
event.stopPropagation();
});
  $( '#cat_addholding #doc, #cat_addbiblio #doc' ).on( 'click', function(event){
  $( '.tag' ).removeClass( 'new_active_tag' );
});
```

### Luettelointinäkymässä lisätään lukitulle tagi-inputille lukkoikoni (Tritonia)

```
$( '#cat_addbiblio .tag .subfield_line .input_marceditor.readonly' ).after( '<i class="fa fa-lock"></i>' );
```

### Valitaan cataloging-etusivulla "search the catalog" -haku "cataloging search" -haun sijasta (joka piilotetaan) (Tritonia)

```
$( document ).ready(function() {
$( '#cat_addbooks #header_search li[aria-controls="addbooks_search"]' ).hide();
$( '#cat_addbooks #header_search' ).tabs( { active: 4 } );
$( '#cat_addbooks #header_search #catalog_search #cat-search-block #search-form' ).focus();
});
```

### Lisätään holding id näkyville tietueen holdings-listaukseen (Tritonia)

```
$( document ).ready(function() {
  $( '#catalog_detail .summaryholdings_table thead tr' ).append( '<th>Holding ID</th>' );
  $( '#catalog_detail .summaryholdings_table tbody tr' ).each(function(){
  $( this ).append( '<td>' + $( this ).children( '.actions' ).children( '.delete' ).attr( 'href' ).split("holding_id=").pop() + '</td>' );
});
```


### Siirretään item-listaus sivun loppuun itemin muokkaussivulla (Tritonia, päivitetty 2020)

```
$( document ).ready(function() {
    $( '#cat_additem #cataloguing_additem_itemlist' ).after( $( '#cat_additem #cataloguing_additem_itemlist #itemst_wrapper' ).parents( 'div' ).html() );
	$( '#cat_additem #cataloguing_additem_itemlist #itemst_wrapper' ).parent( 'div' ).hide();*/
	$( '#cat_additem #cataloguing_additem_itemlist' ).prepend( $( '#cat_additem #cataloguing_additem_itemlist>.row' ) );
});
```

### Luettelointivalikon pysyminen sivun ylälaidassa MARC-näkymässä (Tritonia 2020)

```
$( document ).ready(function() {
$(window).bind('scroll', function () {
    if ($(window).scrollTop() > 150) {
        $('#cat_addbiblio #toolbar').addClass('fixed_cataloging_menu');
    } else {
        $('#cat_addbiblio #toolbar').removeClass('fixed_cataloging_menu');
    }
});
```

### Lisätään nidenäkymän tietojen otsikoihin rivivälejä (Tritonia 2020)

```
$( document ).ready(function() {
$( '#catalogue_detail_biblio .results_summary .label' ).before( '<div style="width: 100%; height: 1px;"></div>' );
});
```

### Poistetaan turhat hakaset "Edit item" -napista (Tritonia)

```
$( document ).ready(function() {
  $( '#catalog_moredetail #catalogue_detail_biblio .yui-g .listgroup h4 a' ).each( function() {
  $( this ).text( $( this ).text().replace('[', '') );
  $( this ).text( $( this ).text().replace(']', '') );
  });
});
```

### Poistetaan ylimääräiset välilyönnit niteen muokkausnäytöllä

Tällä poistetaan ylimääräiset välilyönnit kentistä niteen muokkausnäytöllä. Välilyönnit poistetaan alusta, lopusta ja useammat peräkkäiset välilyönnit välistä.

Tarpeellisuus: Suositeltava<br />
Versio: 22.11

```
/// ALKU ///
/* Poista niteen muokkausnäytön kentistä välilyönnit alusta, lopusta ja useammat peräkkäiset välilyönnit välistä*/
$(document).ready(function() {
  $('body#cat_additem.cat input').blur(function() {
     var tmp = $(this).val();
     tmp = tmp.replace(/^ +/, '');
     tmp = tmp.replace(/ +$/, '');
     tmp = tmp.replace(/  */g, ' ');
     $(this).val(tmp);
  });
});
/// LOPPU ///
```

### Poistetaan ylimääräiset välilyönnit kausijulkaisujen vastaantotossa

Skripti poistaa ylimääräiset välilyönnit sekä tarkistaa, että sarjanumero on muodossa "vuosi : numero". Jos vuoden jälkeen puuttuu välilyönti, käytännössä se lisätään sinne. Tarkistus tehdään kaikkiin nidekenttiin, mutta korjaus ei "tartu", jos kentän alussa ei ole vuosinumeroa.

Tarpeellisuus: Suositeltava<br />
Versio: 22.11

```
/// ALKU ///
/* Poista kausijulkaisun vastaanottonäytön kentistä välilyönnit alusta, lopusta ja useammat peräkkäiset välilyönnit välistä. Tarkistetaan samalla, että numerointikaava on muodossa "vuosi : numero". */
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
/// LOPPU ///
```

### Niteiden eräpoistossa täppä kohtaan "Poista tietueet.."

Skripti laittaa niteiden eräpoistossa valmiiksi täpän kohtaan "Poista tietueet, jos kaikki niteet poistettu". Näin todennäköisemmin tietokantaan ei jää roikkumaan niteettömiä tietueita.

Tarpeellisuus: Suositeltava<br />
Versio: 22.11

```
/// ALKU ///

/* Laita niteiden eräpoistossa täppä kohtaan "Poista tietueet, jos kaikki niteet poistettu". Tällä varmistetaan, että tietokantaan ei jää niteettömiä tietueita. */
$(document).ready(function () {
  $("#del_records").attr('checked', true);
});

/// LOPPU ///
```

---

## Yleiset

### Piilota Uusinta-välilehti yläosan hakukentästä

```
$(document).ready(function () {
  $( "li[aria-controls='renew_search']" ).hide();
});
```

### Koha logo ylävalikkoon (Tritonia)

```
$( document ).ready(function() {
  $( '#header #toplevelmenu' ).before( '<a href="/cgi-bin/koha/mainpage.pl" class="new_koha_toplogo" alt="Koha home"><img src="https://www.tritonia.fi/img/koha_logo_2019.png" alt="Koha home"></a>' );
});
```

### Kielivalinta ylävalikkoon ja piilotetaan apusivulinkki (Tritonia, päivitetty 2020)

```
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
```

### Etusivun ikonien parempi asettelu (Tritonia, pävitetty 2020)

```
$( document ).ready(function() {
$( '#main_intranet-main #container-main' ).append( '<div id="new_icon_container"></div>' );
$( '#main_intranet-main #container-main .row:first-child' ).hide();
$( '#main_intranet-main .biglinks-list li' ).each(function(){
	$( '#main_intranet-main #new_icon_container' ).append( $( this ).html() );
});
$( '#main_intranet-main #new_icon_container' ).prepend( $( '#main_intranet-main #area-pending' ).parent( 'div' ).html() );
});
```

### Tyhjennä Hae tietokannasta -hakukenttä

```
$(document).ready(function() {
      localStorage.removeItem("searchbox_value");
});
```

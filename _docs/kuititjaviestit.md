---
title: 'Kuitit ja viestipohjat'
permalink: /dokumentaatio/kuititjaviestit/
redirect_from:
  - /theme-setup/
toc: true
---

Tälle sivulle on koottu esimerkit erilaisista kuitti- ja viestipohjista. Testattu toimivaksi Kohan versiossa 22.11.

## HOLD_SLIP eli varauksen info- ja kuljetuskuitti

Tieto lisätään email-pohjaan. HTML-täppä paikoilleen.

Suomi:
```
[% USE Branches %]

[% loggedinbranchname = Branches.GetName( Branches.GetLoggedInBranchcode() ) %]

[% IF loggedinbranchname == branch.branchname%]

<style type="text/css">
  h1 { font-family: arial; font-size: 20pt; }
  h2 { font-family: arial; font-size: 18pt; }
  p { font-family: arial; font-size: 12pt; }
</style>

<h1><<borrowers.othernames>></h1>
<h2>Viimeinen noutopäivä: <br />
<<reserves.expirationdate>></h2><br />
<h2 style="border: 2px solid; border-radius: 5px; padding-left: 5px; text-align: center; width: 198pt;">Muistathan lainata!</h2>
<br /><br />
<p>VARATTU NIDE</p>
<p><<biblio.author>><br />
<<biblio.title>> <<items.enumchron>><br />
<<items.barcode>><br />
Noutokirjasto: <<reserves.branchcode>></p>
```

Englanti:
```
[% USE Branches %]

[% loggedinbranchname = Branches.GetName( Branches.GetLoggedInBranchcode() ) %]

[% IF loggedinbranchname == branch.branchname%]

<style type="text/css">
  h1 { font-family: arial; font-size: 20pt; }
  h2 { font-family: arial; font-size: 18pt; }
  p { font-family: arial; font-size: 12pt; }
</style>

<h1><<borrowers.othernames>></h1>
<h2>Last pickup date: <br />
<<reserves.expirationdate>></h2><br />
<h2 style="border: 2px solid; border-radius: 5px; padding-left: 5px; text-align: center; width: 198pt;">Remember to<br /> check out!</h2>
<br /><br />
<p>Reserved item</p>
<p><<biblio.author>><br />
<<biblio.title>> <<items.enumchron>><br />
<<items.barcode>><br />
Pick up library:  <<reserves.branchcode>></p>

<p>Date: <<today>></p>
<br/>
<p>You can change your hold identifier<br/>
at the OUTI Web Library:
<br/> outi.finna.fi</p>
<br/><br/><br/><br/><br/><br/><br/><br/>.

[% ELSE %]

<style type="text/css">
  h1 { font-family: arial; font-size: 20pt; }
  h2 { font-family: arial; font-size: 18pt; }
  h3 { font-family: arial; font-size: 16pt; }
  h4 { font-family: arial; font-size: 14pt; }
  p { font-family: arial; font-size: 10pt; }
</style>

<h2>Transfer to:<br />
<<branches.branchname>></h2>
<h3>Date: <<today>></h3>
<br />
<p>Item<br />
<<biblio.author>><br />
<<biblio.title>> <<items.enumchron>><br />
<<items.barcode>></p>

[% END %]

<br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/>.

```

## MEMBERSHIP_EXPIRY eli sähköpostiviesti tilin voimassaoloajan loppumisesta

Tieto lisätään email-pohjaan.

Suomi:
```
Asiakas: <<borrowers.othernames>>

Kirjastokorttisi voimassoloaika on päättymässä <<borrowers.dateexpiry>>.

Ota yhteys kirjastoosi jatkaaksesi voimassaoloaikaa. Samalla tarkistamme yhteystietosi. Tarkistamme yhteystiedot kaikilta asiakkailtamme viiden vuoden välein. 

Ystävällisin terveisin

OUTI-kirjastot
www.outikirjastot.fi
```

Englanti:
```
Customer: <<borrowers.othernames>>

The validity period of your library card is ending <<borrowers.dateexpiry>>. 

Please contact your library to continue the validity period. At the same time we check your contact information. We will check the contact information from all our customers every five years. 

Sincerely

OUTI Libraries
www.outikirjastot.fi
```

Asiakaslajin mukaan valikoituva viestipohja (virkailijalle eri viesti kuin asiakkaille):
```
[% IF "<<borrowers.categorycode>>" == "VIRKAILIJA" %]
Hei,

Koha-tunnuksen <<borrowers.cardnumber>> voimassaolo päättyy 30 päivän kuluttua. Mikäli työsuhde jatkuu, on pyydäthän esihenkilöä huolehtimaan tunnuksen voimassaolon jatkamisesta ennen <<borrowers.dateexpiry>>.

[% ELSE %]

Hei <<borrowers.firstname>>,  
 
on aika tarkistaa kirjastokorttisi <<borrowers.cardnumber>> asiakastiedot. Käythän kirjastossa päivittämässä tietosi ennen <<borrowers.dateexpiry>>. Voit ottaa yhteyttä kirjastoon myös sähköpostilla tai puhelimitse. Vaski-kirjastojen yhteystiedot löydät verkkokirjastosta www.vaskikirjastot.fi.
  
Tähän viestiin ei voi vastata. Otathan tarvittaessa yhteyttä omaan kirjastoosi.

[% END %]
```

Myös syntaksi ```[% IF borrower.categorycode == "VIRKAILIJA" %]``` viestin alussa ajaa saman asian kuin ```[% IF "<<borrowers.categorycode>>" == "VIRKAILIJA" %]```

## FINESLIP eli asiakkaan maksut

Tieto lisätään Tuloste/Print-pohjaan. HTML-täppä pitää laittaa paikoilleen.

Suomi:
```
<style type="text/css">
  h1 { font-family: arial; font-size: 20pt; }
  h2 { font-family: arial; font-size: 18pt; }
  h3 { font-family: arial; font-size: 16pt; }
  h4 { font-family: arial; font-size: 14pt; }
  p { font-family: arial; font-size: 10pt; }
</style>
<h3><<branches.branchname>><br />
<<today>></h3>
<br /><br />
<h3>Kirjastomaksut:</h3>
<fines>
<p><<fines.date_due>> <<fines.description>>: <<fines.amount>> € </p>
</fines>
<p><b>Yhteensä:</b> <<total.amount>> €</p><br />
<p><<branches.branchfax>><br />
<<branches.branchphone>><br />
www.outikirjastot.fi</p>
```


Englanti:
```
<style type="text/css">
  h1 { font-family: arial; font-size: 20pt; }
  h2 { font-family: arial; font-size: 18pt; }
  h3 { font-family: arial; font-size: 16pt; }
  h4 { font-family: arial; font-size: 14pt; }
  p { font-family: arial; font-size: 10pt; }
</style>
<h3><<branches.branchname>><br />
<<today>></h3>
<br /><br />
<h3>Fines:</h3>
<fines>
<p><<fines.date_due>> <<fines.description>>: <<fines.amount>> € </p>
</fines>
<p><b>Total:</b> <<total.amount>> €</p><br />
<p><<branches.branchfax>><br />
<<branches.branchphone>><br />
www.outikirjastot.fi</p>
```

## DUEDGST eli Eräpäivämuistutus eräpäivänä

Email-pohjaan.

Suomi
```
Asiakastunnus: <<borrowers.cardnumber>>

Seuraavilla lainoilla on eräpäivä tänään: 

<<items.content>>


Lainat voi uusia osoitteessa https://outi.finna.fi/MyResearch/CheckedOut

Lainat voi uusia, jos niistä ei ole varauksia. Lainan voi uusia poikkeuksellisesti enintään kymmenen kertaa peräkkäin. Uusimiseen tarvitaan kirjastokortin numero ja pin-koodi.

Terveisin 
OUTI-kirjastot
<<branches.branchfax>>
http://www.outikirjastot.fi

ps. Verkkokirjastossa omaan kirjastokorttiin voi liittää myös muita kirjastokortteja, esimerkiksi lapsen tai muun perheenjäsenen kortin. Tämän toiminnon avulla liitetyn kortin tietoja pääsee tarkastelemaan ja muokkaamaan, uusimaan lainoja ja tekemään varauksia. Kortin liittämiseen tarvitsee tietää liitettävän kirjastokortin numero ja sen pin-koodi.
```

Englanti:
```
Library card number: <<borrowers.cardnumber>>

The following items are due today:

<<items.content>>

You can renew your loans at https://outi.finna.fi/MyResearch/CheckedOut

You need your library card number and PIN for renewing.

Best regards
OUTI Libraries
<<branches.branchfax>>
http://www.outikirjastot.fi
```

## ISSUESLIP eli lainakuitti kaikista lainoista

Email-pohjaan. HTML-täppä paikoilleen.

Suomi:
```
[% USE Price %]

<style type="text/css">
  h1 { font-family: arial; font-size: 20pt; }
  h2 { font-family: arial; font-size: 14pt; }
  h3 { font-family: arial; font-size: 18pt; }
  h4 { font-family: arial; font-size: 14pt; }
  p { font-family: arial; font-size: 10pt; }
</style>

<h3><<branches.branchname>><br />
<<today>></h3><br />

<h2>Kaikki lainassa olevat</h2>
<checkedout>
<p><<biblio.title>> <<items.enumchron>> / <<biblio.author>> <br />
Nidetunnus: <<items.barcode>><br />
Eräpäivä: <<issues.date_due | dateonly >><br />
Uusintakerrat: <<items.renewals>>
</p>
</checkedout>

<p>Yhteensä: [% checkouts.count %][% IF checkouts.count > 1 %]
      lainaa
[% ELSE %]
      laina
    [% END %] </p>
<br/>
<h4>Myöhässä olevat</h4>
<overdue>
<p>
<<biblio.title>> / <<biblio.author>>  <br />
Nidetunnus: <<items.barcode>><br />
Eräpäivä: <<issues.date_due | dateonly >> <br />
Uusintakerrat: <<items.renewals>>
</p>
<p>Yhteensä: [% overdues.count %][% IF overdues.count > 1 %]
      lainaa
[% ELSE %]
      laina
    [% END %] </p>
</overdue>
<br />
<p>Maksut: 
[% SET balance = borrower.account.balance %]
[% IF balance > 0 %]
[% balance | $Price %] €.
[% END %]
[% IF balance < 0 %]
Asiakkaalla on hyvityksiä [% balance | $Price %] €.
[% END %]
<br /></p>
<p><<branches.branchfax>><br />
<<branches.branchphone>><br />
www.outikirjastot.fi</p>
<br />
```

Englanti:
```
[% USE Price %]

<style type="text/css">
  h1 { font-family: arial; font-size: 20pt; }
  h2 { font-family: arial; font-size: 14pt; }
  h3 { font-family: arial; font-size: 18pt; }
  h4 { font-family: arial; font-size: 14pt; }
  p { font-family: arial; font-size: 10pt; }
</style>

<h3><<branches.branchname>><br />
<<today>></h3><br />

<h2>All check outs</h2>
<checkedout>
<p><<biblio.title>> <<items.enumchron>> / <<biblio.author>> <br />
Barcode: <<items.barcode>><br />
Due date: <<issues.date_due | dateonly >><br />
Renewals: <<items.renewals>>
</p>
</checkedout>

<p>Check outs: [% checkouts.count %][% IF checkouts.count > 1 %]
      check outs
[% ELSE %]
      check out
    [% END %] </p>
<br/>
<h4>Overdue</h4>
<overdue>
<p>
<<biblio.title>> / <<biblio.author>>  <br />
Barcode: <<items.barcode>><br />
Due date: <<issues.date_due | dateonly >> <br />
Renewals: <<items.renewals>>
</overdue>
</p>
<p>Check outs: [% overdues.count %][% IF overdues.count > 1 %]
      check outs
[% ELSE %]
      check out
    [% END %] </p>

<br />
<p>Fines: 
[% SET balance = borrower.account.balance %]
[% IF balance > 0 %]
[% balance | $Price %] €.
[% END %]
[% IF balance < 0 %]
Credit  [% balance | $Price %] €.
[% END %]
<br /></p>
<p><<branches.branchfax>><br />
<<branches.branchphone>><br />
www.outikirjastot.fi</p>
<br />
```

## ISSUEQLSLIP eli lainakuitti päivän lainoista

Email-pohjaan. HTML-täppä paikoilleen.

Suomi:
```
[% USE Price %]

<style type="text/css">
  h1 { font-family: arial; font-size: 20pt; }
  h2 { font-family: arial; font-size: 18pt; }
  h3 { font-family: arial; font-size: 16pt; }
  h4 { font-family: arial; font-size: 14pt; }
  p { font-family: arial; font-size: 10pt; }
</style>

<h3><<branches.branchname>><br />
<<today>></h3>
<br />
<h3>Lainattu tänään</h3>
<checkedout>
<p><<biblio.title>> <<items.enumchron>> / <<biblio.author>> <br />
Eräpäivä: <<issues.date_due | dateonly >>
</checkedout>
<br /><br />

<p>Yhteensä: [% checkouts.count %][% IF checkouts.count > 1 %]
      lainaa
[% ELSE %]
      laina
    [% END %] </p>
<p>Maksut:
[% SET balance = borrower.account.balance %]
[% IF balance > 0 %]
[% balance | $Price %] €.
[% END %]
[% IF balance < 0 %]
Asiakkaalla on hyvityksiä [% balance | $Price %] €.
[% END %]
</p>

<p><<branches.branchfax>>
<br /><<branches.branchphone>>
<br />www.outikirjastot.fi</p>
```

Englanti:
```
[% USE Price %]

<style type="text/css">
  h1 { font-family: arial; font-size: 20pt; }
  h2 { font-family: arial; font-size: 18pt; }
  h3 { font-family: arial; font-size: 16pt; }
  h4 { font-family: arial; font-size: 14pt; }
  p { font-family: arial; font-size: 10pt; }
</style>

<h3><<branches.branchname>><br />
<<today>></h3>
<br />
<h3>Check outs today</h3>
<checkedout>
<p><<biblio.title>> <<items.enumchron>> / <<biblio.author>> <br />
Du edate: <<issues.date_due | dateonly >>
</checkedout>
<br /><br />

<p>Checked out: [% checkouts.count %][% IF checkouts.count > 1 %]
      check outs
[% ELSE %]
      check out
    [% END %] </p>
<p>Fines:
[% SET balance = borrower.account.balance %]
[% IF balance > 0 %]
[% balance | $Price %] €.
[% END %]
[% IF balance < 0 %]
Credits [% balance | $Price %] €.
[% END %]
</p>

<p><<branches.branchfax>>
<br /><<branches.branchphone>>
<br />www.outikirjastot.fi</p>
```

## CHECKOUT eli Lainauskuitti sähköpostiin

Email-pohjaan.

Suomi:
```
Lainasitte tänään <<branches.branchname>>sta  seuraavat teokset:

----
<<biblio.title>> <<items.enumchron>> / <<biblio.author>>,  eräpäivä: <<issues.date_due | dateonly >>
----


Terveisin OUTI-kirjastot
www.outikirjastot.fi
```

Englanti:
```
You checked out from <<branches.branchname>> following items:

----
<<biblio.title>> <<items.enumchron>> / <<biblio.author>>,  due date: <<issues.date_due | dateonly >>
----


Best regards
OUTI Libraries
www.outikirjastot.fi
```

## HOLD eli Noutoilmoitus

### Email-pohjaan

Suomeksi:
```
NOUTOILMOITUS                                        
<<today>>

Varaustunnuksesi on <<borrowers.othernames>>.

Varaamasi teos <<biblio.title>> <<biblioitems.number>> <<items.enumchron>> / <<biblio.author>> (<<items.barcode>>) on noudettavissa <<branches.branchname>>sta.

Varauksen viimeinen noutopäivä on <<reserves.expirationdate>>. 

Muistathan ottaa kirjastokortin mukaan varausta noutaessasi. Noutamattomasta varauksesta perimme yhden euron.


Terveisin 
<<branches.branchname>>
<<branches.branchaddress1>>
<<branches.branchzip>>  <<branches.branchcity>>
<<branches.branchphone>>
<<branches.branchreplyto>>
www.outikirjastot.fi
```

Englanniksi:
```
Library pick-up notice 
<<today>>

Your library hold identifier is <<borrowers.othernames>>.

The item <<biblio.title>> <<biblioitems.number>> <<items.enumchron>> / <<biblio.author>> (nide <<items.barcode>>) is waiting for pickup at <<branches.branchname>>.

The last pick-up day is <<reserves.expirationdate>>. 

Please remember to take your library card with you when picking up your hold. If you do not pick up your hold, a fee of one euro will be charged.

Best regards
<<branches.branchname>>
<<branches.branchaddress1>>
<<branches.branchzip>>  <<branches.branchcity>>
<<branches.branchphone>>
<<branches.branchfax>>
<<branches.branchreplyto>>
www.outikirjastot.fi
```

### Tuloste/Print-pohjaan

E-kirjeeseen tulee osoitetiedot Paten toimintojen kautta, niitä ei määritetä viestipohjaan.

Suomi:
```
NOUTOILMOITUS                                        
<<today>>

Varaustunnuksesi on <<borrowers.othernames>>.

Varaamasi teos <<biblio.title>> <<biblioitems.number>> <<items.enumchron>> / <<biblio.author>> (<<items.barcode>>) on noudettavissa <<branches.branchname>>sta.

Varauksen viimeinen noutopäivä on <<reserves.expirationdate>>. 

Muistathan ottaa kirjastokortin mukaan varausta noutaessasi. Noutamattomasta varauksesta perimme yhden euron.


Terveisin 
<<branches.branchname>>
<<branches.branchaddress1>>
<<branches.branchzip>>  <<branches.branchcity>>
<<branches.branchphone>>
<<branches.branchreplyto>>
www.outikirjastot.fi
```

Englanti:
```
Your reservation is waiting for pickup. Your hold identifier is
<<borrowers.othernames>>.

Title: <<biblio.title>> <<biblioitems.number>> <<items.enumchron>> / <<biblio.author>> (<<items.barcode>>) is waiting at <<branches.branchname>>.
The last pick-up date is <<reserves.expirationdate>>.

Please remember to take your library card with you 
when picking up your hold. If you do not pick up your 
hold a fee of one euro will be charged.

Best regards 
OUTI Libraries
<<branches.branchphone>>
www.outikirjastot.fi
```

### SMS/Tekstiviesti-pohjaan

Suomi:
```
Varaustunnuksellasi <<borrowers.othernames>> on noudettavissa varaus <<biblio.title>> <<items.enumchron>> <<biblioitems.number>> (<<items.barcode>>)  <<branches.branchname>>sta <<reserves.expirationdate>> asti.
```

Englanti:
```
Your hold identifier is <<borrowers.othernames>>. Your hold <<biblio.title>> <<biblioitems.number>> <<items.enumchron>> (<<items.barcode>>) is waiting for you at <<branches.branchname>> until <<reserves.expirationdate>>. 
```

## CHECKINSLIP eli palautuskuitti

Tuloste/Print-pohjaan. HMTL-täppä pakoilleen.

Suomi:
```
<style type="text/css">
  h1 { font-family: arial; font-size: 20pt; }
  h2 { font-family: arial; font-size: 18pt; }
  h3 { font-family: arial; font-size: 16pt; }
  h4 { font-family: arial; font-size: 14pt; }
  p { font-family: arial; font-size: 10pt; }
</style>

<h3>[% branch.branchname %]<br />
[% today | $KohaDates %]<br /></h3><br /><br />

<h3>Palautetut lainat</h3>

[% FOREACH checkin IN old_checkouts %] [% SET item = checkin.item %] <p> [% item.biblio.title %] [% item.enumchron %] [% item.biblio.author %] <br />
Nide: [% item.barcode %] <br />
</p>
[% END %]

<p>
<br /><<branches.branchfax>>
<br /><<branches.branchphone>>
<br />www.outikirjastot.fi</p>
<br />
```

Englanti:
```
<style type="text/css">
  h1 { font-family: arial; font-size: 20pt; }
  h2 { font-family: arial; font-size: 18pt; }
  h3 { font-family: arial; font-size: 16pt; }
  h4 { font-family: arial; font-size: 14pt; }
  p { font-family: arial; font-size: 10pt; }
</style>

<h3>[% branch.branchname %]<br />
[% today | $KohaDates %]<br /></h3><br /><br />

<h3>Checkins</h3>

[% FOREACH checkin IN old_checkouts %] [% SET item = checkin.item %] <p> [% item.biblio.title %] [% item.enumchron %] [% item.biblio.author %] <br />
Barcode: [% item.barcode %] <br />
</p>
[% END %]

<p>
<br /><<branches.branchfax>>
<br /><<branches.branchphone>>
<br />www.outikirjastot.fi</p>
<br />
```

## CHECKIN eli palautuskuitti sähköpostiin

Email-pohjaan.

Suomi:
```
<<branches.branchname>>
<<today>>

Palautitte tänään seuraavat lainat:

----
<<biblio.title>> <<items.enumchron>> / <<biblio.author>> <<items.barcode>>
----

Terveisin OUTI-kirjastot
www.outikirjastot.fi
```

Englanti:
```
<<branches.branchname>>
<<today>>

You checked in today:

----
<<biblio.title>> <<items.enumchron>> / <<biblio.author>> <<items.barcode>>
----

Best regards
OUTI Libraries
www.outikirjastot.fi
```

## OVERDUES_SLIP eli myöhässä olevat lainat kuitille

Tuloste/Print-pohjalle. HMTL-täppä paikoilleen.

Suomi:
```
<style type="text/css">
  h1 { font-family: arial; font-size: 20pt; }
  h2 { font-family: arial; font-size: 18pt; }
  h3 { font-family: arial; font-size: 16pt; }
  h4 { font-family: arial; font-size: 14pt; }
  p { font-family: arial; font-size: 10pt; }
</style>

<h3>Myöhässä olevat lainat</h3>

<overdue>
<p><item>
<<biblio.title>> / <<biblio.author>>  <br />
Nidetunnus: <<items.barcode>><br />
Eräpäivä: <<issues.date_due>><br />
Uusintakerrat: <<issues.renewals>><br /><br /></item>
</p>
</overdue>

<p><<branches.branchfax>>
<br /><<branches.branchphone>>
<br />www.outikirjastot.fi</p>
```

Englanti:
```
<style type="text/css">
  h1 { font-family: arial; font-size: 20pt; }
  h2 { font-family: arial; font-size: 18pt; }
  h3 { font-family: arial; font-size: 16pt; }
  h4 { font-family: arial; font-size: 14pt; }
  p { font-family: arial; font-size: 10pt; }
</style>

<h3>Overdues</h3>

<overdue>
<p><item>
<<biblio.title>> / <<biblio.author>>  <br />
Barcode: <<items.barcode>><br />
Due date: <<issues.date_due>><br />
Renewals: <<issues.renewals>><br /><br /></item>
</p>
</overdue>

<p><<branches.branchfax>>
<br /><<branches.branchphone>>
<br />www.outikirjastot.fi</p>
```

## ODUE1 eli ensimmäinen palautuskehotus

### Email/sähköposti-pohjaan

Suomi:
```
Hyvä kirjaston asiakas 

Lainasi ovat myöhässä. 

Asiakastunnus: <<borrowers.cardnumber>>

Erääntyneet lainat:
----
<item>Nide: <<items.barcode>>, Aineistolaji: <<items.itype>>
Teos: <<biblio.title>> <<items.enumchron>> / <<biblio.author>>  
Eräpäivä: <<issues.date_due>>, Lainattu: <<issues.issuedate>>
</item>
----

Palautathan lainasi mahdollisimman pian. Voit uusia lainasi OUTI-verkkokirjastossa, jos niistä ei ole varauksia. Lainan voi uusia enintään 10 kertaa peräkkäin. OUTI-verkkokirjaston osoite: www.outikirjastot.fi

Myöhästymismaksut alkavat kertyä heti eräpäivän jälkeen. Lasten aineistosta ja lapsiasiakkaan lainoista ei mene myöhästymismaksua.

Perimme tämän muistutuksen lähettämisestä 1,50 euron huomautusmaksun.

Palauttamattomista lainoista lähetämme laskun.

Epäselvissä tapauksissa pyydämme ottamaan yhteyttä kirjastoon.


Ystävällisin terveisin

OUTI-kirjastot

<<branches.branchname>>
<<branches.branchfax>>
<<branches.branchphone>>
<<branches.branchreplyto>>
www.outikirjastot.fi
```

Englanti
```
Hyvä kirjaston asiakas 

Lainasi ovat myöhässä. 

Asiakastunnus: <<borrowers.cardnumber>>

Erääntyneet lainat:
----
<item>Nide: <<items.barcode>>, Aineistolaji: <<items.itype>>
Teos: <<biblio.title>> <<items.enumchron>> / <<biblio.author>>  
Eräpäivä: <<issues.date_due>>, Lainattu: <<issues.issuedate>>
</item>
----

Palautathan lainasi mahdollisimman pian. Voit uusia lainasi OUTI-verkkokirjastossa, jos niistä ei ole varauksia. Lainan voi uusia enintään 10 kertaa peräkkäin. OUTI-verkkokirjaston osoite: www.outikirjastot.fi

Myöhästymismaksut alkavat kertyä heti eräpäivän jälkeen. Lasten aineistosta ja lapsiasiakkaan lainoista ei mene myöhästymismaksua.

Perimme tämän muistutuksen lähettämisestä 1,50 euron huomautusmaksun.

Palauttamattomista lainoista lähetämme laskun.

Epäselvissä tapauksissa pyydämme ottamaan yhteyttä kirjastoon.


Ystävällisin terveisin

OUTI-kirjastot

<<branches.branchname>>
<<branches.branchfax>>
<<branches.branchphone>>
<<branches.branchreplyto>>
www.outikirjastot.fi
```

Englanti:
```
Dear library user

Your loans are overdue.

Customer number:  <<borrowers.cardnumber>>

Overdue items:
----
<item>Itemnumber: <<items.barcode>>
Title: <<biblio.title>> <<items.enumchron>> / <<biblio.author>>  
Due date: <<issues.date_due>>, Checked out on: <<issues.issuedate>>, Item type: <<items.itype>>
</item>
---- 

Please return your overdue items as soon as possible. You can also renew them at the OUTI Web Library if there are no reservations. Loans can be renewed up to ten times.

The overdue fine starts to accrue immediately after the due date. Materials for children and material borrowed by customers under the age of 18 years are not subject to overdue fines.

We also charge 1,50 euro for sending this notification.

If you have any questions about these loans, please contact the library where you checked them out.

Best regards
OUTI Libraries
<<branches.branchname>>
<<branches.branchfax>>
<<branches.branchphone>>
<<branches.branchreplyto>>
www.outikirjastot.fi
```

### Tuloste/Print-pohjaan

E-kirjeessä asiakkaan yhteystiedot tulee Paten kautta, niitä ei määritetä viestipohjaan.

Suomi:
```
Hyvä kirjaston asiakas. Lainasi ovat myöhässä. 

Erääntyneet lainat:
----
<item>Nide: <<items.barcode>>, Aineistolaji: <<biblioitems.itemtype>>
Teos: <<biblio.title>> <<items.enumchron>> / <<biblio.author>>  
Eräpäivä: <<issues.date_due>>, Lainattu: <<issues.issuedate>>
</item>
---- 

Palautathan lainasi mahdollisimman pian. Voit uusia lainasi 
OUTI-verkkokirjastossa osoitteessa www.outikirjastot.fi, 
jos niistä ei ole varauksia. Lainan voi uusia enintään 10
kertaa peräkkäin.

Myöhästymismaksut alkavat kertyä heti eräpäivän jälkeen.
Lasten aineistosta ja lapsiasiakkaiden lainoista ei mene
myöhästymismaksua.

Perimme tämän muistutuksen lähettämisestä 1,50 euron 
huomautusmaksun.

Epäselvissä tapauksissa pyydämme ottamaan yhteyttä kirjastoon.

Ystävällisin terveisin 
OUTI-kirjastot
<<branches.branchphone>>

Ilmoita kirjastoon sähköpostiosoitteesi tai lisää se OUTI-verkkokirjastossa,
niin saat tämän viestin nopeammin ja ekologisemmin.
```

Englanti:
```
Dear library user

Your loans are overdue.

Overdue items:
----
<item>Itemnumber: <<items.barcode>>,  Item type: <<biblioitems.itemtype>>
Title: <<biblio.title>> <<items.enumchron>> / <<biblio.author>>  
Due date: <<issues.date_due>>, Checked out on: <<issues.issuedate>>
</item>
---- 
 
Please return your overdue items as soon as possible.
You can also renew them at the OUTI Web Library if there are no 
reservations. Loans can be renewed up to ten times.

The overdue fine starts to accrue immediately after the due date.
Materials for children and material borrowed by customers under 
the age of 18 years are not subject to overdue fines.

We also charge 1,50 euro for sending this notification.

If you have questions about these loans, please contact the library
where you checked them out.

Best regards

OUTI Libraries
http://www.outikirjastot.fi
<<branches.branchphone>>
```

## ODUE2 eli toinen palautuskehotus

### Email/sähköposti-pohjaan

Suomi:
```
Hyvä kirjaston asiakas  

Seuraavat lainasi ovat edelleen palauttamatta. Tämä on toinen palautuskehotus.  

Asiakastunnus: <<borrowers.cardnumber>> 

Erääntyneet lainat: 

---- 

<item>Nide: <<items.barcode>>, Aineistolaji: <<items.itype>> 
Teos: <<biblio.title>> <<items.enumchron>> / <<biblio.author>>   
Eräpäivä: <<issues.date_due>>, Lainattu: <<issues.issuedate>> 
</item> 

---- 

Palautathan lainasi mahdollisimman pian. Voit uusia lainasi OUTI-verkkokirjastossa, jos niistä ei ole varauksia. Lainan voi uusia enintään 10 kertaa peräkkäin. OUTI-verkkokirjaston osoite: www.outikirjastot.fi 

Myöhästymismaksut alkavat kertyä heti eräpäivän jälkeen. Lasten aineistosta ja lapsiasiakkaan lainoista ei mene myöhästymismaksua.

Perimme tämän muistutuksen lähettämisestä 3 euron huomautusmaksun. 

Palauttamattomista lainoista lähetämme laskun. Laskun lähettäminen aiheuttaa lainauskiellon. Hoitamatta jäävä lasku voi johtaa perintään. 

Epäselvissä tapauksissa pyydämme ottamaan yhteyttä kirjastoon. 


Ystävällisin terveisin 

OUTI-kirjastot 

<<branches.branchname>> 
<<branches.branchfax>> 
<<branches.branchphone>> 
<<branches.branchreplyto>> 
www.outikirjastot.fi
```

Englanti:
```
Dear library user

Your loans are still overdue. This is a second overdue notice. 

Customer number:  <<borrowers.cardnumber>> 

Overdue items: 
---- 
<item>Itemnumber: <<items.barcode>> 
Title: <<biblio.title>> <<items.enumchron>> / <<biblio.author>>   
Due date: <<issues.date_due>>, Checked out on: <<issues.issuedate>>, Item type: <<items.itype>> 
</item> 
----  

Please return your overdue items as soon as possible. You can also renew them at the OUTI Web Library if there are no reservations. Loans can be renewed up to ten times. 

The overdue fine starts to accrue immediately after the due date. Materials for children and material borrowed by customers under the age of 18 years are not subject to overdue fines.

We also charge 3 euro for sending this notification. 

Unless you return the items, you will receive an invoice of the overdue loans. Your library card will be blocked when the invoice is sent. Not taking care of the invoice can lead to collection of your debt. 

If you have any questions about these loans, please contact the library where you checked them out. 
  

Best regards 

OUTI Libraries 

<<branches.branchname>> 
<<branches.branchfax>> 
<<branches.branchphone>> 
<<branches.branchreplyto>> 
www.outikirjastot.fi
```

### Tuloste/Print-pohjaan

E-kirjeissä asiakkaan yhteystiedot haetaan Paten kautta, niitä ei lisätä viestipohjaan.

Suomi:
```
Hyvä kirjaston asiakas 
 
Seuraavat lainasi ovat edelleen palauttamatta. Tämä on toinen palautuskehotus. 
 
Erääntyneet lainat: 
---- 
<item>Nide: <<items.barcode>>, Aineistolaji: <<biblioitems.itemtype>> 
Teos: <<biblio.title>> <<items.enumchron>> / <<biblio.author>>
Eräpäivä: <<issues.date_due>>, Lainattu: <<issues.issuedate>> 
</item> 
----  
 
Palautathan lainasi mahdollisimman pian. Voit uusia lainasi OUTI-verkkokirjastossa
osoitteessa www.outikirjastot.fi, jos niistä ei ole varauksia. Lainan voi uusia 
enintään 10 kertaa peräkkäin. 
 
Myöhästymismaksut alkavat kertyä heti eräpäivän jälkeen. Lasten aineistosta ja 
lapsiasiakkaan lainoista ei mene myöhästymismaksua.

Perimme tämän muistutuksen lähettämisestä 3 euron huomautusmaksun. 
 
Palauttamattomista lainoista lähetämme laskun. Laskun lähettäminen aiheuttaa lainauskiellon. Hoitamatta jäävä lasku voi johtaa perintään.    
 
Epäselvissä tapauksissa pyydämme ottamaan yhteyttä kirjastoon. 
 
Ystävällisin terveisin  
OUTI-kirjastot 
<<branches.branchphone>>

Ilmoita kirjastoon sähköpostiosoitteesi tai lisää se OUTI-verkkokirjastossa,
niin saat tämän viestin nopeammin ja ekologisemmin.
```

Englanti:
```
Dear library user
 
Your loans are overdue. 
 
Overdue items: 
---- 
<item>Itemnumber: <<items.barcode>>,  Item type: <<biblioitems.itemtype>> 
Title: <<biblio.title>> <<items.enumchron>> / <<biblio.author>>   
Due date: <<issues.date_due>>, Checked out on: <<issues.issuedate>> 
</item> 
----  
  
Please return your overdue items as soon as possible. 
You can also renew them at the OUTI Web Library if there are no  
reservations. Loans can be renewed up to ten times. 
 
The overdue fine starts to accrue immediately after the due date.
Materials for children and material borrowed by customers under 
the age of 18 years are not subject to overdue fines.

We also charge 3 euros for sending this notification. 
 
Unless you return the items, you will receive an invoice  
of the overdue loans. Your library card will be blocked  
when the invoice is sent. Not taking care of the invoice  
can lead to collection of your debt. 
 
If you have questions about these loans, please contact the library 
where you checked them out. 
 
Best regards 
 
OUTI Libraries 
http://www.outikirjastot.fi 
<<branches.branchphone>>
```

## ODUECLAIM eli lasku

Katso laskutustyökalun ohjeet.

## Tuloste/Print-pohjaan

Suomi:
```
Lainaaja: <<issueborname>>, <<issueborbarcode>>

Pyydämme viipymättä palauttamaan tai korvaamaan erääntyneet lainat. 

<item>
Eräpäivä: <<date_due>>
Teos: <<biblio.title>>  <<items.enumchron>> 
Tekijä: <<biblio.author>>
Aineistotyyppi: <<biblioitems.itemtype>> 
Viivakoodi: <<items.barcode>>
Luokka: <<items.itemcallnumber>>
Korvaushinta: <<items.replacementprice>> €
</item>


Maksettava yhteensä: <<totalfines>> €
ALV: 0 %

Saaja: <<grouplibrary>>
<<groupaddress>>, <<groupzipcode>> <<groupcity>>
Puhelin: <<groupphone>>
Y-tunnus: <<businessid>>

Tilinumero: <<accountnumber>>
BIC: <<biccode>>

Viitenumero: <<referencenumber>>
Laskun eräpäivä: <<invoice_duedate>>
Maksuehto: 14 pv netto
Huomautusaika: 8 päivää

Viivästyskorko: Korkolain mukainen
Laskunumero: <<invoicenumber>>
```

### PDF-pohjaan

```
<div class="header">
    <div class="sender">
        <div class="library">
            <p><ul class="info"><li><<branches.branchname>></li>
                <li><<branches.branchaddress1>></li>
                <li><<branches.branchzip>> <<branches.branchcity>></li>
                </ul></p>
        </div>
        <div class="billheader">
            <p><ul class="info"><li>Lasku</li>
                <li><<today>></li>
            </ul></p>
        </div>
    </div>
</div>
<div class="recipient">
    <p><ul class="info">
        <li><<borrowers.firstname>>  <<borrowers.surname>></li>
        <li><<borrowers.address>></li>
        <li><<borrowers.zipcode>> <<borrowers.city>></li>
    </ul></p>
</div>
<div class="content">
    <p><strong>Lainaajan nimi:</strong> <<issueborname>> <strong>Nro:</strong> <<issueborbarcode>></p>
    <p>Pyydämme teitä viipymättä palauttamaan tai korvaamaan erääntyneet lainat. Hoitamaton lasku siirtyy perintätoimiston hoidettavaksi.</p><br/>
    <table class="table">
        <thead>
            <tr>
            <th>Eräpäivä</th>
            <th>Teos</th>
            <th>Nidetiedot</th>
            <th>Korvaushinta</th>
            </tr>
        </thead>
        <tbody>
            <item>
                <tr>
                    <td><<date_due>></td>
                    <td><<biblio.title>>  <<items.enumchron>> / <<biblio.author>> </td>
                    <td><<biblioitems.itemtype>><br/><<items.barcode>><br/><<items.itemcallnumber>></td>
                    <td><<items.replacementprice>> €<br/></td>
                </tr>
            </item>
        </tbody>
    </table>
</div>
<div class="summary">
    <p><ul class="info">
    <li>MAKSETTAVA YHTEENSÄ: <<totalfines>> €</li>
    <li>ALV: 0 %</li>

    </ul></p>
</div>
<div class="ehdot">
<p>Saaja: <<grouplibrary>><br />
Osoite: <<groupaddress>>, <<groupzipcode>> <<groupcity>><br />
Puhelin: <<groupphone>><br />
Y-tunnus: <<businessid>>
<br />

Tilinumero: <<accountnumber>><br />
BIC: <<biccode>><br />
<br />
Viitenumero: <<referencenumber>><br />
Laskun eräpäivä: <<invoice_duedate>><br />
Maksuehto: 14 pv netto<br />
Huomautusaika: 8 päivää<br />
<br />
Viivästyskorko: Korkolain mukainen<br />
Laskunumero: <<invoicenumber>><br />
</p>
</div>
Laskunumero: <<invoicenumber>>
```
---
title: 'Kohan ohje suomeksi'
permalink: /dokumentaatio/tietoturvaohje/
redirect_from:
  - /theme-setup/
toc: true
---

# Koha-Suomen tietoturvaohje

Tällä sivulla on kirjastoille tarkoitettuja ohjeita ja hyviä käytäntöjä Koha-järjestelmän tietoturvasta ja turvallisuudesta huolehtimiseen.

## Yleistä

Koha-käyttöön suositeltava selain on Firefox ESR (Extended Support Release). Selainta on Kohaa käytettäessä hyvä käyttää yksityisen selauksen tilassa (Private Browsing). Kuten normaalia, linkkien seuraamisessa tulee noudattaa varovaisuutta eikä "epämääräisiä" linkkejä tule koskaan avata.

## Pääsy Kohaan

Virkailijaliittymiin pääsy on rajattu vuosittain uusittavin asiakasvarmentein. Koha-Suomi toimittaa varmenteet kimpan pääkäyttäjälle Matrixissa. Varmenne tulee asentaa sellaisten koneiden selaimiin joilla Kohaa halutaan käyttää. Varmennetta tai sellaisella varustettua selainta ei tule luovuttaa sellaisten henkilöiden käyttöön, joilla ei ole oikeutta käyttää Kohaa. Tästä voidaan huolehtia esimerkiksi erillisillä käyttäjäprofiileilla oikeudellisille ja oikeudettomille käyttäjille. Pääsääntöisesti Kohaa tulisi käyttää ainoastaan työnantajan toimittamilla laitteilla ja laitteiden tietoturvasta tulee huolehtia asianmukaisesti.

Kirjastokorttien ja virkailijatunnusten tulee lukittua jos salasana syötetään liian monta kertaa väärin. Tällä tavoin voidaan varsin tehokkaasti estää tunnuksiin tai kirjastokorttinumeroihin kohdistuva väsytyshyökkäys. Kohassa lukkiutumista säätää järjestelmäasetus _FailedLoginAttempts_, joka täytyy asettaa mielekkääseen arvoon (suosittelemme arvoa väliltä 3-5). Tunnuksen lukitus voidaan purkaa antamalla käyttäjälle uusi salasana tai PIN-koodi. Haluttaessa lukitus voidaan myös purkaa automaattisesti tietyn ajan kuluttua siitä kun tunnuksella on edellisen kerran yritetty kirjautua järjestelmään (resetFailedLogins.pl cronjob). Automaattisen lukituksen purkamisen käyttöönottoa voi pyytää kehittäjiltä. Emme kuitenkaan suosittele lukituksen purkua, koska se voi avata ylimääräisiä hyökkäysreittejä järjestelmään. Esimerkiksi asiakastunnusten lukittuessa on mahdollista, että kirjastokortin numero on päätynyt vääriin käsiin ja asiakkaan tietoja yritetään anastaa tai aiheuttaa muuta vahinkoa. Tällaisissa tapauksissa asiakkaalle tulisi mieluummin antaa kokonaan uusi kirjastokortti ja PIN-koodi.

Vanhentuneilla virkailijatunnuksila kirjautuminen järjestelmään tulee estää. Järjestelmänkehittäjä voi ottaa toiminnon (ManageExpiredUserAccounts.pl cronjob) käyttöön pyynnöstä. Tunnuksen voimassaoloajan jatkaminen Kohan liittymässä aktivoi tunnuksen pienellä viiveellä jälleen takaisin, salasana ei muutu.

## Tunnukset ja kirjautuminen

Virkailjatunnukset täytyy erottaa virkailijan lainaajatunnuksista. Lainaajatunnuksien kanssa ei ole kirjastoautomaatiosta johtuen mahdollista käyttää riittävän vahvoja salasanoja. Virkailijatunnusten salasanojen tulisi olla vähintään aakkosnumeerisia ja riittävän pitkiä, kyberturvallisuuskeskus suosittelee vähintään 15 merkkiä. Sama koskee myös automaattien käyttämiä SIP-tunnuksia.

Pääkäyttäjille kannattaa tehdä toinen matalammin käyttöoikeuksin varustettu tili perustyöskentelyyn. Pääkäyttäjätasoisin oikeuksin varustettua tiliä tulisi käyttää vain silloin kun sille on tarve.

Kohasta tulee aina ja ilman poikkeuksia kirjautua ulos jos virkailija poistuu koneen äärestä. Selain tai yksityisen selauksen ikkuna tulee sulkea Kohasta uloskirjautumisen jälkeen, tai vaihtoehtoisesti tyhjentää selaimen sivuhistoria ja evästeet. Tätä varten voi olla järkevää nostaa "Unohda" (engl. "Forget") nappi suoraan selaimen työkaluriville, josta se on helposti klikattavissa. Ohje tähän löytyy "täältä":https://support.mozilla.org/fi/kb/firefoxin-painikkeiden-tyokalupalkkien-muokkaaminen.

Erillisen käyttäjätunnuksen käyttö kirjastokorttinumeron rinnalla ei ole suositeltavaa. Kaksi rinnakkaista tunnusta voi aiheuttaa sekaannuksia ja avata ylimääräisiä hyökkäysreittejä järjestelmään. Asiakaskirjautumisen tulisi aina tapahtua kirjastokortin numerolla ja siihen liitetyllä PIN-koodilla. Virkailijakirjautumisen taas tunnuksella ja vahvalla salasanalla. Suosittelemme lukitsemaan käyttäjätunnuksen samaksi kuin kirjastokortin numero. Tämän voi pyytää kehittäjiltä.

Asiakkaiden varaustunnukseksi ei tulisi hyväksyä kirjautumiskelpoisia tunnuksia, esimerkiksi kirjastokortin numeroita. Varaustunnuksen ei ole tarkoitus avata pääsyä järjestelmään tai kirjaston palveluihin, vaan ainoastaan anonyymisti identifioida tietylle asiakkaalle menossa olevat varaukset noutohyllyssä.

## Käyttöoikeudet

Kullakin käyttäjällä tulisi olla ainoastaan juuri ne oikeudet, joita hänen työtehtäviensä hoitaminen edellyttää. Kimpan pääkäyttäjien täytyy huolehtia henkilöstön muuttuneiden työtehtävien aiheuttamista käyttöoikeuksien muutostarpeista Kohassa ja käyttöoikeuksien ja työtehtävien vastaavuus on hyvä kartoittaa koko henkilöstön laajuisesti säännöllisesti.

Erityisesti lokien katselu, asetusten muokkaus, uutisten julkaiseminen sekä tiedostojen lataaminen järjestelmään täytyy rajata ainoastaan niiden henkilöiden käyttöön, joilla on todellinen ja perusteltu tarve näille toiminnoille, esimerkiksi pääkäyttäjille. Huomionarvoisia, laajan pääsyn järjestelmään antavia oikeuksia ovat mm:

* management
* parameters_remaining_permissions
* batch_upload_patron_images
* stage_marc_import
* upload_general_files
* upload_local_cover_images
* upload_manage
* view_system_logs
* import_patron_data
* edit_news
* edit_quotes

Näiden kanssa on siis oltava erityisen tarkkana.

## Automaatit

Automaattien yhteys Koha-palvelimelle pitää salata. Ensisijainen ratkaisu tähän on SIP2oHTTPS (SIP2 over HTTPS) REST-endpoint. Vanhoja automaatteja varten voidaan tarvittaessa rakentaa salattuja tunneleita. Salaamaton liikennöinti SIP2-palvelimen ja automaattien välillä on ehdottomasti kielletty eikä ole teknisestikään mahdollista.

Lainausautomaateilla, omatoimijärjestelmissä ja Kohan itsepalvelulainauksessa tulisi kirjastoasiakkaiden oikeusturvan ja tietosuojan vuoksi käyttää PIN-koodin kyselyä.

## Miten toimia, jos huomaat tietoturvaan liittyvän ongelman

Jos huomaat tietoturvaan liittyvän ongelman, ole yhteydessä kimppasi pääkäyttäjään suojatusti (turvaposti, puhelu). Kimppojen pääkäyttäjät voivat laittaa Koha-Suomelle viestin ongelmasta turvapostilla osoitteeseen support(ät)koha-suomi.fi tai Matrixissa suojatussa huoneessa.

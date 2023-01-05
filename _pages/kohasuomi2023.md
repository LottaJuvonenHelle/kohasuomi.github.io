---
title: 'Koha-Suomen vuoden 2023 muistiot'
header:
  overlay_color: '#5e616c'
  overlay_image: /assets/images/cropped-pexels-photo-113850.jpeg
permalink: /kohasuomi2023
redirect_from:
  - /theme-setup/
toc: true
layout: single
hidden: true
---

Koha-Suomen henkilökunta kokoontuu kaksi kertaa viikossa. Uusin muistio on aina ylimmäisenä.

## Viikko 1 esityslista


### Maanantain palaveri

Aika: 2.1.2023 klo 10<br />
Läsnä: Anneli, Lasse, Pasi, Ari, Lari, Kodo

* Viikon 1 päivitys
  * [KohaSuomi/Koha #331](https://github.com/KohaSuomi/Koha/issues/331) Suojatut kentät näkyvät tyhjinä z39.50-haulla tietueita korvattaessa
  * [KohaSuomi/Koha #334](https://github.com/KohaSuomi/Koha/issues/334)
  * SQL-raportit hakemaan slave-kannasta masterin sijaan, jotta vältytään tietokannan taulujen lukkiutuminen raskaissa kyselyissä sekä master-kannan kuormaa saadaan kevennettyä.
  * [Koha #308](https://github.com/KohaSuomi/Koha/issues/308)

* Kodo ehdottaa tämän viikon Kirkes-palaverin ajankohdaksi ke 4.1.2023

* Versionvaihto
  * viedään ensin Vaski, jotta nähdään, kuinka kauan maksimissaan menee.
  * kaikille läksyksi miettiä torstain palaveriin mennessä, miten saadaan vähennettyä testikantaan vietävän datan määrää, jotta testikantojen luonti ei vie niin kauan.


### Torstain palaveri

Aika: 5.1.2023 klo 10<br />
Läsnä: Pasi, Lari, Kodo, Lasse

* Vanhentuneiden maksujen poistoajo - Vaski kysyi pääkäyttäjäpalaverissa, että mikä sen tilanne on?
  * Päätös [Tietojen säilytysajat -wikissä](https://tiketti.koha-suomi.fi/projects/koha-suomen-dokumentaatio/wiki/Tietojen_s%C3%A4ilytysajat)

* Viikon 2 päivitys
  * käännöksissä korjauksia 
  * Muutama XSLT-muutos, esim. hakutulosnäytön Sisältyy-linkki.

* Onko huoltokatkoa vkolla 2 keskiviikkona?
  * On, ja iso: Fujitsun muistikampojen vaihdot. Katko saattaa kestää enemmän kuin 2 tuntia, ja koskee kaikkia kimppoja.

* Pääkäyttäjien kanssa sovittiin, että jokainen kimppa käy omat Redmine-tikettinsä Palaute-projektissa läpi ja sulkee valmiit ja sellaiset, jotka eivät ole enää ajankohtaisia. Loput käydään läpi ja päätetään, mitkä siirretään uusina tiketteinä GitHubiin.

* Siirretään käännökset build-productionista omaan repoon, symlinkataan meidän omat po-tiedostot reposta Kohan ympäristöön.
 

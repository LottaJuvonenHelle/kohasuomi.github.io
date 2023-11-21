---
title: 'Käyttöönotto-ohjeita'
permalink: /dokumentaatio/kayttoonotto-ohjeita/
redirect_from:
  - /theme-setup/
toc: true
---

Tälle sivulle on kerätty erilaisia käyttöönotto-ohjeita.

## Asteri-liitännäinen

Asteri-liitännäisellä saa haettua Kansalliskirjaston KANTO-tietokannasta auktoriteettitietueita TäTiin.

[Asteri-liitännäisen käyttöönotto-ohje](/dokumentaatio/asteri/)

## EDItX-hankinta

[EDItX-hankinnan käyttöönotto-ohje](/dokumentaatio/editx/)

## Finto-liitännäiset

Finto-liitännäisiä voi hakea auktorisoituja muotoja käytettävistä termeistä Finton-rajapinnan kautta. Liitännäiset ovat käytössä TäTi-tietokannassa.

[Finto-liitännäisten määrittely](/dokumentaatio/finto/)

## Laskutustyökalu

Laskutustyökalu on toteutettu liitännäisenä.

[Laskutustyökalun käyttöönotto-ohje](https://github.com/KohaSuomi/koha-plugin-overdue-tool/wiki) Koha-Suomen GitHubissa.

## Palautuskehotukset ensisijaisesti sähköpostina


Kun halutaan lähettää palautuskehotukset ensisijaisesti sähköpostiin ja kirjeenä vain niille, joilla ei ole sähköpostiosoitetta, voidaan tämä toteuttaa seuraavasti:

Mene myöhästymisilmoitusten määrittelyyn ja laita täpät kohtiin _Sähköposti_ ja _Tuloste_.

![kuva](https://github.com/KohaSuomi/kohasuomi.github.io/assets/33121325/b32231fa-d72d-4208-95b4-fa3fbd3abd2b)


Lisäksi cron-ajoon pitää laittaa "vipu" _prefer email_. Tämän tekee kehittäjät.

## RDA ja poikkeava pääsana

Jos on tarve poiketa kuvailusääntöjen mukaisista pääsanoista, voi käyttää 942him-kenttiä ohittamaan normaalikäytännöt. Alla linkki ohjeeseen.

[RDA ja poikkeava pääsana](/dokumentaatio/rdanuotti/)

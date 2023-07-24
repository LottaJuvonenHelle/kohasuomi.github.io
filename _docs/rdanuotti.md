---
title: 'RDA ja poikkeava pääsana'
permalink: /dokumentaatio/rdanuotti/
redirect_from:
  - /theme-setup/
toc: true
---

Kun esim. nuottiin halutaan RDA-kuvailusäännöistä poikkeava pääsana signumiin ja tarralle, voi ottaa käyttöön sitä varten luodut liitännäiset. 
Lisäksi tarrapohjaan pitää tehdä lisäyksiä.

Tässä ratkaisussa tiedot poimitaan 942-kentästä normaalien sääntöjen sijaan, jolloin kuvailija pystyy itse määrittämään, mitä tietoja signumiin tulee.

Tähän liittyy seuraavat liitännäiset:
Liitännäinen|Liitetään kenttään
---|---
fi_signumbuilder_942k_branchloc_942hm.pl|952o
fi_signumbuilder_942k_loc_942hm.pl|952o
fi_signumbuilder_942k_loc_ccode_942hm.pl|952o
fi_signumbuilder_942khm_branch_loc.pl|952o
fi_signumbuilder_942khm_branchloc.pl|952o
fi_signumbuilder_942khm_branchloc_genre.pl|952o
fi_signumbuilder_942khm_loc.pl|952o
ykl_from_084a.pl|942h

## Muutokset kuvailupohjaan

RDA:sta poikkeavia säätöjä ei tarvitse tehdä kaikelle aineistolle, vaan esimerkiksi vain nuottiaineistolle siinä tapauksessa, 
että RDAn mukainen tekijätieto ei vastaa hyllytyskäytäntöjä.

Esim. Nightwishin musiikkia sisältävä nuotti halutaan hyllyyn Nightwishin mukaisesti eikä säveltäjä Tuomas Holopaisen mukaisesti.

1. Luo uusi kuvailupohja
2. Tuo siihen attachment:export_NUOP.csv -tiedostosta tiedot valitsemalla kuvailupohjan oikeasta reunasta Toiminnot -> Tuo
3. Tarkista, että 
* näkyvillä on 942him-kentät
* 942h-kentässä kiinni liitännäinen ykl_from_084a.pl
* 952o-kentässä oleva liitännäinen on omalle kimpalle sopiva. Jos ei ole, kokeile muita fi_signumbuilder-alkuisia liittännäisiä löytääksesi kimpallesi sopivan liitännäisen. Liitännäiset hakevat tiedot 942-kentistä, jolloin signumiin tulee poikkeuksen mukaiset tiedot.

Voit tehdä muutokset myös käsin ilman kuvailupohjan tuontia.

## Muutokset tarrapohjiin

Lisää haluamiisi tarrapohjiin sille riville, johon yleensä tulee tekijätieto, ensimmäiseksi määritys 942$i ||

Eli näin:

![](/assets/files/docs/Ohjeet/rda.png)

Käytännössä tuo määrittää, että "hae tieto 942i-kentästä, jos siitä ei löydy, niin 100a-kentästä, jos siitä ei löydy 110a-kentästä, jos siitä ei löydy, niin 111a-kentästä".

## Miten kenttiä käytetään

Yllä määritettyjä 942him-kenttiä tarvitaan, jotta tarralle saadaan tulostettua "normaalista" pääsanasta poikkeava tieto.

![](/assets/files/docs/Ohjeet/rda1.png)
* h-kenttään haetaan tietueen luokka klikkaamalla kentän perässä olevaa kuvaketta
* i-kenttään kirjoitetaan kuvailusäännöistä poikkeava pääsana
* m-kenttään kirjoitetaan poikkeavasta pääsanasta kolme ensimmäistä merkkiä.

Poikkeavat merkinnät pitää saada myös niteen signumiin.

![](/assets/files/docs/Ohjeet/rda2.png)
* klikkaa signumin vieressä olevaa kolmea pistettä, jolloin tiedot haetaan 942hm-kentistä normaalin pääsanasäännön sijaan.

Tarralla tieto näyttää sitten esim. OUTI-kirjastoissa tarrarullan pohjalla tältä:

![](/assets/files/docs/Ohjeet/rda3.png)

Ilman yllä mainittuja muutoksia tälle teokselle
![](/assets/files/docs/Ohjeet/rda4.png)

olisi tullut 

* Pääsanaksi: O'Connell, Finneas
* Pääasanan kolme ensimmäistä merkkiä O'C

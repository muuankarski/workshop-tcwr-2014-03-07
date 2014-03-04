---
title: rOpenGov - R ekosysteemi avoimelle julkishallinnon datalle ja laskennalliselle yhteiskuntatutkimukselle
author: Markus Kainu
date: Esitys TCWR-seminaarissa 7.3.2014 Turussa
---

Johdanto
==========================================

Tältä sivulta löydät materiaalit perjantaiseen esitykseeni. Kyseessä ei ole tavanomainen tutkimuksen ja sen tulosten esittely, vaan erään *laskennallisen yhteiskuntatutkimuksen* edistämiseen keskittyvän ohjelmistoprojektin esittely.

**Materiaalit**-kohdasta löydät esityksen diat sekä tammikuussa kirjoittamani johdannon avoimiin tutkimusmenetelmiin, jossa käyn pintapuolisesti läpi R-kieltä. Ko. teksti ei liity tähän esitykseen/projektiin kuin R-kielen kautta.

**Mikä rOpenGov**-kohdassa esittelen tiiviisti mistä projektissa on kyse ja ketkä sen tekemiseen tällä hetkellä osallistuvat.

*- Markus Kainu*


Materiaalit
==============================================


| linkki  | huom! |
| --- | --- |
| [slides.html](slides.html) | Esityksen diat .html-muodossa - (ei toimi vanhoilla Internet Explorer -selaimilla! Käytä Firefox, Chrome, Safari tms.) |
| [Fördjupning: Open research methods in computational social sciences and humanities: introducing R](http://digihist.se/5-metoder-inom-digital-historia/fordjupning-open-research-methods-in-computational-social-sciences-and-humanities-introducing-r/) | Kirjottamani "kevyt johdatus avoimiin tutkimusmenetelmiin ja R-kieleen" |


Mikä rOpenGov?
==============================================

[rOpenGov](http://ropengov.github.io) on *yhteisövetoinen ekosysteemi avoimen julkishallinnollisen datan ja laskennallisen yhteiskuntatutkimuksen R-paketeille*. 

Suomessa ja maailmalla nopeasti lisääntyvät hallinnollisen ja muun avoimen datan virrat ovat erityisen kiinnostavia yhteiskuntatieteiden, datajournaslimin ja kansalaisten osallistumisen näkökulmasta, mutta laskennalliset työkalut näiden datavirtojen hyödyntämiseen vielä ovat puutteellisia. rOpenGov-projektissa kehitetään yhteisövetoista skaalautuvaa ohjelmistoekosysteemiä tavoitteena valjastaa avoimen laskennallisen analyysin ja uusien datalähteiden potentiaali yhteiskuntatieteiden käyttöön. Projekti ottaa oppia biotieteiden menestyksekkäiden ekosysteemiprojektien kuten [Bioconductor](http://www.bioconductor.org/):in tai [rOpenSci](http://ropensci.org/):n kokemuksista.


rOpenGov-yhteisö
------------------------------------------------

rOpenGov on yhteisöllinen projekti, joka rakentuu **ydintiimistä**, **pakettien kehittäjistä** ja **pakettien käyttäjistä**.  

**Käyttäjäyhteisö** koostuu akateemisista tutkijoista, opiskelijoista, datajournalisteista, kansalaistieteilijöistä ja muista kiinnostuneista.

**Ydintiimin** palvelee kehittäjiä ja käyttäjiä ylläpitämällä infrastruktuuria, arvioimalla uusia paketteja ja laatimalla suosituksia pakettien toiminnalle. Ydintiimin jäsenillä on laskennallisten tieteiden koulutus:

- [Leo Lahti](http://www.iki.fi/Leo.Lahti) (Univ. Helsinki, Finland and Wageningen Univ., Netherlands)
- [Juuso Parkkinen](http://ouzor.github.io/) (Aalto Univ., Finland) 
- [Joona Lehtomäki](https://github.com/jlehtoma) (University of Helsinki, Finland).

**Pakettien kehittäjien** [projektit](http://ropengov.github.io/projects) helpottavat erilaisten lasennalliselle yhteiskuntatutkimukselle relevanttien datalähteiden ohjelmoinnillista hyödyntämistä. Mm. seuraavat eri tieteenalojen tutkijat ovat aktiivisesti mukana omien pakettiensa ja koko projektin kehitystyössä:

- [Przemyslaw Biecek](http://www.biecek.pl/) - [University of Warsaw](http://www.icm.edu.pl/web/guest/home)
- [François Briatte](http://f.briatte.org/) - [European School of Political and Social Sciences](http://espol-lille.eu/)
- [Scott Chamberlain](http://scottchamberlain.info/) - [Simon Fraser University in Vancouver](http://www.biology.sfu.ca/)
- [Manuel Eugster](http://users.ics.aalto.fi/meugster/) - [Helsinki Institute for Information Technology: Statistical Machine Learning and Bioinformatics Group](http://research.ics.aalto.fi/mi/)
- [Christopher Gandrud](http://christophergandrud.blogspot.fi/) - [Hertie School of Governance](http://www.hertie-school.org/)
- [Love Hansson](https://github.com/LCHansson) - [Swedish Pensions Agency](http://www.pensionsmyndigheten.se/)
- [Markus Kainu](http://markuskainu.fi/) - [Turun yliopisto](https://www.utu.fi/fi/yksikot/soc/yksikot/sosiaalitieteet/Sivut/home.aspx)
- [Stefan Kasberger](https://github.com/skasberger) - [openscienceASAP](http://openscienceasap.org/)
- [Thomas J. Leeper](http://thomasleeper.com/) - [Aarhus University](http://ps.au.dk/en/)
- [Måns Magnusson](https://github.com/MansMeg) - [Linköpings Universitet](http://www.liu.se/?l=en)



Projektin tavoitteet
-------------------------------------------------

**Tilastolliset ja graafiset menetelmät**. Projekti pyrkii tarjoamaan yhteiskuntatieteille relevantteja laskennallisia työkaluja R-kielen täydentämiseksi tältä osin. Erityisesti rOpenGov tarjoaa työkaluja uusien datalähteiden käyttöön.

**Dokumentaatio**. Projektissa uskotaan että korkealaatuinen dokumentaatio ei ole vain hyvä kehittämistrategia vaan myös ehdoton edellytys sille että uudet työkalut otetaan käyttöön. Jokainen rOpenGov-paketti sisältää vähintää yhden *vignetin* (ohjedokumentti R-projektissa), jossa esitellään tehtäväkältöisesti, läpinäkyvästi ja toistettavasti kuvaus paketin toiminnallisuudesta ja mahdollisuuksista. Pakettien ensisijaiset vignetit käännetään automaattisesti online-ohjeiksi rOpenGov:n verkkosivuille.

**Skaalautuvuus**. rOpenGov on jaettu ohjelmistoalusta joka mahdollistaa laajennettavien, skaalautuvien ja keskenään yhteensopivien ohjelmistojen ripeän kehittämisen. Yksittäinen tutkija ei kykene tuottamaan näin monipuolisia työkaluja kuin mitä on tarpellista uusien datalähteiden potentiaalin hyödyntämiseksi.

**Avoin lähdekoodi**. rOpenGov on ja tulee aina olemaan 100 % avoimen lähdekoodin projekti. Projektissa käytetään laajasti [git](http://git-scm.com/):iä ja [Github](https://github.com/):ia versionhallintaan and yhteistyöhön. Kaikki paketit julkaistaan avoimen lähdekoodin lisensseillä, jotta käyttäjillä ja kehittäjillä olisi pääsy algoritmeihin sekä niiden sovelluksiin, ja että kansainvälinen tiedeyhteisö voi omistaa tutkimuksen tekemiseen vaadittavat ohjelmistot.

**Toistettava tutkimus**. Projektissa pyritään edistämään tutkimuksen toistettavuutta tarjoamalla työkaluja ja työvirtoja, jotka ovat helposti sovitettavissa erilaisiin tutkimuskysymyksiin erilaisissa tutkimusasetelmissa. Yhdenmukaisen käyttöliitymän [äänestysdataan](https://github.com/rOpenGov/finpar) sekä [taloudellisiin ja sosiaalisiin indikaattoreihin](https://github.com/muuankarski/rqog) on yksi esimerkki tästä. Tämän kaltainen rakenne tekee analyyseistä suoraviivaisempia ja ymmärrettävämpi, kun dataa ei kerätä ja käsitellä erikseen jokaisella kertaa. Samoin läpinäkyvä dokumentaatio algoritmien yksityiskohtineen luo puitteet hyvälle tieteelliselle laskennalle ja tekee edistynyttä tieteellistä metodologiaa, työtapoja ja ymmärrystä tutuksi laajemmalle yleisölle.

**Avoin kehitystyö**. Projektissa käyttäjiä rohkaistaan astumaan kehittäjien rooliin, joko kehittämällä rOpenGov-yhteensopivia paketteja tai pakettien dokumentaatiota. Lisäksi rOpenGov tarjoaa foorumin ryhmien ja projektien yhteistyölle, joilla on yhteisiä tavoitteita ohjelmistojen kehityksessä. Tällainen yhteistyö voi myös auttaa tutkijoita oppimaan lisää laskennallisten ja tilastollisten menetelmien yhteiskuntatieteellisista sovelluksia. Tämän ohella projekti tarjoaa pakettien kehittäjille lisähyötyjä, kuten [TravisCI](https://travis-ci.org/) skriptit automaattisiin rakentumisraportteihin, automaattisesti generoituvat online-ohjeet paketeille, yhteisen pakettien jakamisen projektin verkkosivulla sekä näkyvyyttä ja tunnustettavuutta yksittäisille paketeille. Avoimen kehitystyön malli luo puitteet ohjelmistojen kehittämiselle virheiden korjaamisen ja laajennoksien rakentamisen kautta ja tarjoaa työkaluvalikoiman, joka mahdollistaa tutkijoiden perehtyä ja laajentaa metodeita. 


Kielipolitiikka
-------------------------------------

rOpenGov perustuu tilastolliseen R-ohjelmointikieleen. R on korkean tason tulkattava ohjelmointikieli, jolla on helppo testata uusia laskennallisia menetelmiä. Olioperusteinen rakenne mahdollistaa moninaisten ja kompleksisten yhteiskuntatieteellisten tutkimusongelmien mallintamisen ja ratkaisemisen.

Valtaosa projektin komponenteista jaetaan R-paketteina. Näin käyttäjillä on mahdollisuus käsitellä, analysoida ja raportoida datoja ja tutkimuksen tuloksia. Projektiin ovat tervetulleita myös tukipalveluja ja metadataa tarjoavat paketit. Yleisperiaate on että pakettien julkaisuversiot jaetaan [CRAN](http://cran.r-project.org/)-verkoston kautta ja kehitysversiot [rOpenGov:n Github-organisaation](https://github.com/rOpenGov) kautta. 

Projektin kieleksi on valittu R-kieli muuan muassa siksi että se tarjoaa:

1. vakiintuneen järjestelmän ohjelmistojen paketoimiselle,
2. monipuoliset mahdollisuudet automatisoituun dokumenttien luomiseen, 
3. verkossa olevan datan tehokkaaseen hyödyntämiseen sekä 
4. tuen moninaisten tilastollisten simulointien ja mallintamisten tekemiselle sekä 
5. tämänhetkistä huipputasoa edustavat graafiset graafiset ominaisuudet.

R:n puolesta puhuu lisäksi kielen ympärillä vaikuttava vahva ekosysteemi ja käyttäjäyhteisö. Lisäksi R on projektin tekijöille tutuin kieli ja sillä on vahvat näytöt samankaltaisista yhteisöllisistä projekteista muilta laskennallisten tieteiden aloilta. Samalla projektissa pidetään tarkkaa silmällä muiden ohjelmointikielien ja niiden ekosysteemien kehitystä, kuten [Python](http://www.python.org/)- ja [Julia](http://julialang.org/)-kielten, ja kielipolitiikkaa voidaan tulevaisuudessa laventaa.


Liity yhteisöön!
-----------------------------------------------

- [Google+](https://plus.google.com/u/0/communities/108289259916380218460)
- IRC (ropengov@Freenode)
- [rOpenGov blog](http://ropengov.github.io/)
- [Twitter](https://twitter.com/ropengov)
- Liity [ropengov-forum@googlegroups.com](https://groups.google.com/forum/#!forum/ropengov-forum) sähköpostilistalle


Linkkejä
===============================================

- [The intention of Open Science and Research initiative in Finland](http://www.tdata.fi/documents/47404/86137/The+intention+of+Open+Science+and+Research+initiative+in+Finland/d8558803-e050-45db-a6a5-90639fe62da9)
- [linkki](http://url.com)
- [linkki](http://url.com)
- [linkki](http://url.com)
- [linkki](http://url.com)
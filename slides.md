rOpenGov 
==============
css: slides.css
transition: fade
transition-speed: fast
*R-ekosysteemi avoimelle julkishallinnon datalle ja laskennalliselle yhteiskuntatutkimukselle*

[TCWR](https://www.utu.fi/fi/yksikot/soc/yksikot/sosiaalitieteet/tcwr/Sivut/home.aspx)-seminaari </br>
7.3.2014 Turussa

[Markus Kainu](http://markuskainu.fi)</br>
*tohtorikoulutettava* </br>
[Sosiaalitieteden laitos, Turun yliopisto](https://www.utu.fi/fi/yksikot/soc/yksikot/sosiaalitieteet/Sivut/home.aspx) </br>
[Aleksanteri-instituutti, Helsingin yliopisto](http://helsinki.fi/aleksanteri) </br>

<div class="github-fork-ribbon-wrapper right">
<div class="github-fork-ribbon">
<a href="https://github.com/muuankarski/" style="color:white;">Fork me on GitHub</a>
</div>
</div>



<!-- ---| notes begin |--------------------------------

Kyseessä ei ole tavanomainen tutkimuksen ja sen tulosten esittely, vaan erään *laskennallisen yhteiskuntatutkimuksen* edistämiseen keskittyvän ohjelmistoprojektin esittely.

Vaikka mä saatan kuulostaa myyntimieheltä, niin mä yritän olla kuulostamatta. Se tarve mihin tällä projektilla pyritään tähtäämään on mun parhaan tietämyksen mukaan todellinen ja olemassa, ja mä näen että nyt alkaa olla aika kiireesti tarttua siihen tai datanälköiset journalistit ottaa niskalenkin ainakin medianäkyvyyden mielessä.   

http://www.harvestmeat.com/wp-content/uploads/2010/09/underconstruction-Copy.jpg


-------------------------------------- -->


Mistä puhun
========================================================
incremental: true

1. Miksi?
2. Mikä rOpenGov?
3. Mitä rOpenGov:n avulla voi tehdä?
4. Miten osallistua projektiin?



========================================================
type:section


<h1>1. Miksi?</h1>


Muutos?
=======================================================


[*(Gary King (2014, p. 166), the director of the Institute for Quantitative Social Science at Harvard University)*](http://gking.harvard.edu/files/gking/files/king14.pdf)

>an important driver of the change sweeping the field is the enormous quantities of highly informative data inundating almost every area we study. 

>In the last half-century, the information base of social science research has primarily come from three sources: survey research, end-of-period government statistics, and one-off studies of particular people, places, or events. 

>In the next half-century, these sources will still be used and improved, but the number and diversity of other sources of information are increasing exponentially and are already many orders of magnitude more informative than ever before.


===================================================
</br>
</br>
</br>
- internet
- avoin lähdekoodi



Muutos!
====================================================
incremental: true

1. Paradigmaattinen käänne yhteiskuntatieteissä
-------------------------------------------

- Suljettu data ja räätälöidyt työkalut => 
- avoin data ja joustavat työkalut

2. Laskennallisten menetelmien kasvava merkitys
-------------------------------------------

- Uusia sovelluksia lainaamalla muiden tieteenalojen menetelmistä
    - sequence analysis (genomics) -> Social sequence analysis
    - networks analysis (computer science) -> Social network analysis
    - spatial inference (geography) -> Spatial econometrics 



====================================
title:false 
</br>
</br>
</br>
Yhteiskuntatieteissä on yhä enemmän **samankaltaisia datarakenteita** ja **samankaltaisia analyyttisiä ongelmia** kuin mitä muilla (laskennallisilla) tieteenaloilla
------------------------------------

Uudet työkalut, uudet mahdollisuudet
=======================
incremental: true

Tarve edistää yhteistyötä tietojenkäsittelytieteiden ja yhteiskuntatieteiden välillä, jonka myötä

- pääsy uusiin datalähteisiin ja datojen analysointi yksinkertaistuu
- työvaiheiden dokumentointi paranee ja avautuu
- läpinäkyvyys ja toistettavuus paranee (validiteetin ja reliabiliteetin näkökulma)
    - *For quantitatively oriented manuscripts that utilize real or simulated data, authors are strongly encouraged to offer their data and code online to other researchers.* [(Sociological Science)](http://www.sociologicalscience.com/for-authors/submission-guidelines/)
- otetaan käyttöön uusia julkaisuformaatteja ja saadaan lisänäkyvyyttä tutkimukselle
- laajempia vaikutuksia yhteiskuntaan, kuten päätöksentekoon, kansalaistieteeseen, datajournalismiin, opetukseen





========================================================
type:section

<h1>2. Mikä rOpenGov?</h1>



=======================================================
title:false

TCWR
------------------------------------------

>Turku Center for Welfare Research was founded in 1997 in a cooperative effort by the three universities in Turku (Åbo). **The Center is intended to more efficiently coordinate resources, both in teaching and research.**

rOpenGov
------------------------------------

>The rapidly emerging governmental and other open data streams provide novel opportunities for social sciences, data journalism, and citizen participation across the globe while computational tools to utilize these resources are lacking. **A community-driven software ecosystem provides a scalable solution and a potential to revolutionize the field, taking advantage of the lessons learned in similar initiatives in other fields such as [Bioconductor](http://www.bioconductor.org/) and [rOpenSci](http://ropensci.org/).**



rOpenGov
==============================================
incremental: true

[rOpenGov](http://ropengov.github.io) on *yhteisövetoinen ekosysteemi avoimen julkishallinnollisen datan ja laskennallisen yhteiskuntatutkimuksen R-paketeille*. 

Suomessa ja maailmalla nopeasti lisääntyvät hallinnollisen ja muun avoimen datan virrat ovat erityisen kiinnostavia yhteiskuntatieteiden, datajournaslimin ja kansalaisten osallistumisen näkökulmasta, mutta laskennalliset työkalut näiden datavirtojen hyödyntämiseen vielä ovat puutteellisia. 

rOpenGov-projektissa kehitetään yhteisövetoista skaalautuvaa ohjelmistoekosysteemiä tavoitteena valjastaa avoimen laskennallisen analyysin ja uusien datalähteiden potentiaali yhteiskuntatieteiden käyttöön. 

Projekti ottaa oppia biotieteiden menestyksekkäiden ekosysteemiprojektien kuten [Bioconductor](http://www.bioconductor.org/):in tai [rOpenSci](http://ropensci.org/):n kokemuksista.


rOpenGov-yhteisö
==============================================
incremental: true

rOpenGov on yhteisöllinen projekti, joka rakentuu **ydintiimistä**, **pakettien kehittäjistä** ja **pakettien käyttäjistä**.  

**Käyttäjäyhteisö** koostuu akateemisista tutkijoista, opiskelijoista, datajournalisteista, kansalaistieteilijöistä ja muista kiinnostuneista.

**Ydintiimin** palvelee kehittäjiä ja käyttäjiä ylläpitämällä infrastruktuuria, arvioimalla uusia paketteja ja laatimalla suosituksia pakettien toiminnalle. Ydintiimin jäsenillä on laskennallisten tai yhteiskuntatieteiden koulutus:

- [Leo Lahti](http://www.iki.fi/Leo.Lahti) (Univ. Helsinki, Finland and Wageningen Univ., Netherlands)
- [Juuso Parkkinen](http://ouzor.github.io/) (Aalto Univ., Finland) 
- [Joona Lehtomäki](https://github.com/jlehtoma) (University of Helsinki, Finland).
- [Markus Kainu](http://markuskainu.fi/) (University of Turku, Finland)



==============================================


**Pakettien kehittäjien** [projektit](http://ropengov.github.io/projects) helpottavat erilaisten lasennalliselle yhteiskuntatutkimukselle relevanttien datalähteiden ohjelmoinnillista hyödyntämistä. Mm. seuraavat eri tieteenalojen tutkijat ovat aktiivisesti mukana omien pakettiensa ja koko projektin kehitystyössä:

- [Vincent Arel-Bundock](https://www.lsa.umich.edu/polisci/people/graduatestudents/ci.arelbundockvincent_ci.detail) - [The University of Michigan’s Department of Political Science](https://www.lsa.umich.edu/polisci)
- [Przemyslaw Biecek](http://www.biecek.pl/) - [University of Warsaw](http://www.icm.edu.pl/web/guest/home)
- [François Briatte](http://f.briatte.org/) - [European School of Political and Social Sciences](http://espol-lille.eu/)
- [Scott Chamberlain](http://scottchamberlain.info/) - [Simon Fraser University in Vancouver](http://www.biology.sfu.ca/)
- [Manuel Eugster](http://users.ics.aalto.fi/meugster/) - [Helsinki Institute for Information Technology](http://research.ics.aalto.fi/mi/)
- [Christopher Gandrud](http://christophergandrud.blogspot.fi/) - [Hertie School of Governance](http://www.hertie-school.org/)
- [Love Hansson](https://github.com/LCHansson) - [Swedish Pensions Agency](http://www.pensionsmyndigheten.se/)
- [Stefan Kasberger](https://github.com/skasberger) - [openscienceASAP](http://openscienceasap.org/)
- [Thomas J. Leeper](http://thomasleeper.com/) - [Aarhus University](http://ps.au.dk/en/)
- [Måns Magnusson](https://github.com/MansMeg) - [Linköpings Universitet](http://www.liu.se/?l=en)



Projektin periaatteet ja tavoitteet 1
==============================================
incremental: true

**Tilastolliset ja graafiset menetelmät**. Projekti pyrkii tarjoamaan yhteiskuntatieteille relevantteja laskennallisia työkaluja R-kielen täydentämiseksi tältä osin. Erityisesti rOpenGov tarjoaa työkaluja uusien datalähteiden käyttöön.

**Dokumentaatio**. Projektissa uskotaan että korkealaatuinen dokumentaatio ei ole vain hyvä kehittämistrategia vaan myös ehdoton edellytys sille että uudet työkalut otetaan käyttöön. Jokainen rOpenGov-paketti sisältää vähintää yhden *vignetin* (ohjedokumentti R-projektissa), jossa esitellään tehtäväkältöisesti, läpinäkyvästi ja toistettavasti kuvaus paketin toiminnallisuudesta ja mahdollisuuksista. Pakettien ensisijaiset vignetit käännetään automaattisesti online-ohjeiksi rOpenGov:n verkkosivuille.

**Skaalautuvuus**. rOpenGov on jaettu ohjelmistoalusta joka mahdollistaa laajennettavien, skaalautuvien ja keskenään yhteensopivien ohjelmistojen ripeän kehittämisen. Yksittäinen tutkija ei kykene tuottamaan näin monipuolisia työkaluja kuin mitä on tarpellista uusien datalähteiden potentiaalin hyödyntämiseksi.

Projektin periaatteet ja tavoitteet 2
==============================================
incremental: true

**Avoin lähdekoodi**. rOpenGov on ja tulee aina olemaan 100 % avoimen lähdekoodin projekti. Projektissa käytetään laajasti [git](http://git-scm.com/):iä ja [Github](https://github.com/):ia versionhallintaan and yhteistyöhön. Kaikki paketit julkaistaan avoimen lähdekoodin lisensseillä, jotta käyttäjillä ja kehittäjillä olisi pääsy algoritmeihin sekä niiden sovelluksiin, ja että kansainvälinen tiedeyhteisö voi omistaa tutkimuksen tekemiseen vaadittavat ohjelmistot.

**Toistettava tutkimus**. Projektissa pyritään edistämään tutkimuksen toistettavuutta tarjoamalla työkaluja ja työvirtoja, jotka ovat helposti sovitettavissa erilaisiin tutkimuskysymyksiin erilaisissa tutkimusasetelmissa. Yhdenmukaisen käyttöliitymän [äänestysdataan](https://github.com/rOpenGov/finpar) sekä [taloudellisiin ja sosiaalisiin indikaattoreihin](https://github.com/muuankarski/rqog) on yksi esimerkki tästä. Tämän kaltainen rakenne tekee analyyseistä suoraviivaisempia ja ymmärrettävämpi, kun dataa ei kerätä ja käsitellä erikseen jokaisella kertaa.

**Avoin kehitystyö**. Projektissa käyttäjiä rohkaistaan astumaan kehittäjien rooliin, joko kehittämällä rOpenGov-yhteensopivia paketteja tai pakettien dokumentaatiota. Lisäksi rOpenGov tarjoaa foorumin ryhmien ja projektien yhteistyölle, joilla on yhteisiä tavoitteita ohjelmistojen kehityksessä. Tällainen yhteistyö voi myös auttaa tutkijoita oppimaan lisää laskennallisten ja tilastollisten menetelmien yhteiskuntatieteellisista sovelluksia. 

Tavoitteet tiivistettynä
============================================

1. Pääsy dataan
    - ohjelmoinnillinen pääsy datalähteisiin
    - läpinäkyvä ja valmiiksi tehty datojen prosessointi
    - datakatalogit
    - harmonisoidut datarakenteet
2. Datan analysoiminen
    - räätälöytyjä analyysialgoritmejä yhteiskuntatieteelliseen dataan
    - analyysitapojen standardisoiminen


Kielipolitiikka 1
==============================================
incremental: true

rOpenGov perustuu tilastolliseen R-ohjelmointikieleen. 

R on korkean tason tulkattava ohjelmointikieli, jolla on helppo testata uusia laskennallisia menetelmiä. 

Olioperusteinen rakenne mahdollistaa moninaisten ja kompleksisten yhteiskuntatieteellisten tutkimusongelmien mallintamisen ja ratkaisemisen.

Valtaosa projektin komponenteista jaetaan R-paketteina. Näin käyttäjillä on mahdollisuus käsitellä, analysoida ja raportoida datoja ja tutkimuksen tuloksia. 

Projektiin ovat tervetulleita myös tukipalveluja ja metadataa tarjoavat paketit. 

Yleisperiaate on että pakettien julkaisuversiot jaetaan [CRAN](http://cran.r-project.org/)-verkoston kautta ja kehitysversiot [rOpenGov:n Github-organisaation](https://github.com/rOpenGov) kautta. 

Kielipolitiikka 
==============================================
incremental: true

Projektin kieleksi on valittu R-kieli muuan muassa siksi että se tarjoaa:

1. vakiintuneen järjestelmän ohjelmistojen paketoimiselle,
2. monipuoliset mahdollisuudet automatisoituun dokumenttien luomiseen, 
3. verkossa olevan datan tehokkaaseen hyödyntämiseen sekä 
4. tuen moninaisten tilastollisten simulointien ja mallintamisten tekemiselle sekä 
5. tämänhetkistä huipputasoa edustavat graafiset graafiset ominaisuudet.

R:n puolesta puhuu lisäksi kielen ympärillä vaikuttava vahva ekosysteemi ja käyttäjäyhteisö. 

Lisäksi R on projektin tekijöille tutuin kieli ja sillä on vahvat näytöt samankaltaisista yhteisöllisistä projekteista muilta laskennallisten tieteiden aloilta. 

Samalla projektissa pidetään tarkkaa silmällä muiden ohjelmointikielien ja niiden ekosysteemien kehitystä, kuten [Python](http://www.python.org/)- ja [Julia](http://julialang.org/)-kielten, ja kielipolitiikkaa voidaan tulevaisuudessa laventaa.


Progress
============================================

| year  | happened |
| ----  | ------   |
| 2010  | Project starts | 
| 2011  | Data journalism workshops |
|       | Apps4Finland Data Opening Award |
| 2012  | SHARE-konferenssi (Belgrade) |
|  | Urban research seminar (Helsinki) |
|  | Collaboration with major Finnish media organizations (election data hackathon) |
|  | Sitra 14,000e funding for election data project | 
|  | Open Legislative Data-conference (Paris) |
|  | Open Knowledge Festival (Helsinki) |
|  | Apps4Finland Data Opening Award (Data elections & Datawiki) |
| 2013  | Open Knowledge Foundation; Open Science work group |
|  | CRAN |
|  | Russia, US, Poland, Austria, OpenStreetMap packages join rOpenGov |
|  | Open Knowledge Roadshow (Turku, Finland) |
|  | Apps4Finland award (collaboration with Demos Helsinki think tank) |
|  | NIPS Machine Learning Open Source Software workshop (Lake Tahoe, US) |
| 2014  | Political scientists rush in the project |
|   | Active development of guidelines and technical documentation |


========================================================
type:section

<h1>3. Mitä rOpenGov:n avulla voi tehdä?</h1>

Avoin hallinnollinen data
========================================================
incremental: true

- [Sotkanet](tutorials/Sotkanet_tutorial.html)
- [sorvi](tutorials/sorvi_tutorial.html)
- [datavaalit](tutorials/datavaalit_tutorial.html)
- [rustfare](tutorials/rustfare_tutorial.html)
- [SmarterPoland](tutorials/SmarterPoland_tutorial.html)


Avoin tutkimusdata & laskennallinen yhteiskuntatutkimus
========================================================
incremental: true

- [rqog](http://muuankarski.github.io/rqog/vignettes/rqog_tutorial.html)
- [r.eusilc](http://muuankarski.github.io/r.eusilc/vignettes/r.eusilc_tutorial.html)
- [psData](https://github.com/rOpenGov/psData)



========================================================
type:section

<h1>4. Miten osallistua projektiin?</h1>


Harkitse avointen analyysimenetelmien kuten R:n opettelemista!
========================================================

- [R-ohjelmointi.org](http://www.r-ohjelmointi.org/?page_id=11)
- [Cross Validated: Resources for learning R](http://stats.stackexchange.com/questions/138/resources-for-learning-r)
- [UCLA: Resources to help you learn and use R](http://www.ats.ucla.edu/stat/r/)
- [Johns Hopkins University: Data Science](https://www.coursera.org/specialization/jhudatascience/1?utm_medium=courseDescripTop)


Liity yhteisöön!
========================================================

- [Google+](https://plus.google.com/u/0/communities/108289259916380218460)
- IRC (ropengov@Freenode)
- [rOpenGov blog](http://ropengov.github.io/)
- [Twitter](https://twitter.com/ropengov)
- Liity [ropengov-forum@googlegroups.com](https://groups.google.com/forum/#!forum/ropengov-forum) sähköpostilistalle

Muutos?
=======================================================


[*Rufus Pollock 4.3.2014 in Al Jazeera*](http://www.aljazeera.com/indepth/opinion/2013/10/small-data-revolution-real-re-20131031111430442239.html)

>Big Data smacks of the centralization fads we've seen in each computing era. The notion that there's more data than we can process - something which has - no doubt - always been true, year on year, since computing began - has been dressed up as the latest trend, complete with associated technology must-haves.

>Meanwhile, a much more important story, the real revolution, is being overlooked: the mass democratisation of the means of access, storage, and processing of data. This story isn't about large organisations running parallel software on tens of thousands of servers, but about more people than ever being able to collaborate effectively around a distributed ecosystem of information, an ecosystem of Small Data.


========================================================
type: section
<h1>Kysymyksiä & kommentteja!</h1>

<center>

![](images/question.gif)

</center>

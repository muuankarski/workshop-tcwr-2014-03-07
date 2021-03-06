---
title: Sotkanet-tutorial
author: Louhos-team
---


Sotkanet API R tools
===========

This is the [sotkanet](http://ropengov.github.com/sotkanet) R package to access data from the [Sotkanet portal](http://uusi.sotkanet.fi/portal/page/portal/etusivu/hakusivu) that provides over 2000 demographic indicators across Finland and Europe, maintained by the National Institute for Health and Welfare (THL). For more information, see [Sotkanet indicator database](http://uusi.sotkanet.fi/portal/page/portal/etusivu/tietoa_palvelusta) and [API description](http://uusi.sotkanet.fi/portal/pls/portal/!PORTAL.wwpob_page.show?_docname=22001.PDF). This package is part of [rOpenGov](http://ropengov.github.com/).


### Installation

Release version for general users:


```r
install.packages("sotkanet")
library(sotkanet)
```


Development version for developers:


```r
install.packages("devtools")
library(devtools)
install_github("sotkanet", "ropengov")
library(sotkanet)
```


### Listing available indicators

List available Sotkanet indicators:


```r
library(sotkanet) 
sotkanet.indicators <- SotkanetIndicators(type = "table")
head(sotkanet.indicators)
```

```
##   indicator
## 1         4
## 2         5
## 3         6
## 4         7
## 5        74
## 6       127
##                                                                            indicator.title.fi
## 1  Mielenterveyden häiriöihin sairaalahoitoa saaneet 0 - 17-vuotiaat / 1 000 vastaavanikäistä
## 2                   Toimeentulotukea saaneet 25 - 64-vuotiaat, % vastaavanikäisestä väestöstä
## 3 Somaattisen erikoissairaanhoidon hoitopäivät 75 vuotta täyttäneillä / 1000 vastaavanikäistä
## 4                                                                 0 - 6-vuotiaat, % väestöstä
## 5                                                      Yksinhuoltajaperheet, % lapsiperheistä
## 6                                                                               Väestö 31.12.
##   indicator.organization        indicator.organization.title.fi
## 1                      2 Terveyden ja hyvinvoinnin laitos (THL)
## 2                      2 Terveyden ja hyvinvoinnin laitos (THL)
## 3                      2 Terveyden ja hyvinvoinnin laitos (THL)
## 4                      3                          Tilastokeskus
## 5                      3                          Tilastokeskus
## 6                      3                          Tilastokeskus
```


List geographical regions with available indicators:


```r
sotkanet.regions <- SotkanetRegions(type = "table")
head(sotkanet.regions)
```

```
##   region                 region.title.fi region.code     region.category
## 1    833          Etelä-Suomen AVIn alue           1 ALUEHALLINTOVIRASTO
## 2    834        Lounais-Suomen AVIn alue           2 ALUEHALLINTOVIRASTO
## 3    835            Itä-Suomen AVIn alue           3 ALUEHALLINTOVIRASTO
## 4    836 Länsi- ja Sisä-Suomen AVIn alue           4 ALUEHALLINTOVIRASTO
## 5    837        Pohjois-Suomen AVIn alue           5 ALUEHALLINTOVIRASTO
## 6    838                 Lapin AVIn alue           6 ALUEHALLINTOVIRASTO
##                           region.uri
## 1 http://www.yso.fi/onto/kunnat/ahv1
## 2 http://www.yso.fi/onto/kunnat/ahv2
## 3 http://www.yso.fi/onto/kunnat/ahv3
## 4 http://www.yso.fi/onto/kunnat/ahv4
## 5 http://www.yso.fi/onto/kunnat/ahv5
## 6 http://www.yso.fi/onto/kunnat/ahv6
```



### Querying SOTKAnet indicators

Get the [indicator 10013](http://uusi.sotkanet.fi/portal/page/portal/etusivu/hakusivu/metadata?type=I&indicator=10013) from Finland (Suomi) for 1990-2012 (Eurostat employment statistics youth unemployment), and plot a graph:


```r
# Get indicator data
dat <- GetDataSotkanet(indicators = 10013, years = 1990:2012, 
         	       genders = c('female', 'male', 'total'), 
		       region.category = "EUROOPPA", 
		       region = "Suomi")

# Investigate the first lines in the data
head(dat)
```

```
##            region region.title.fi region.code region.category indicator
## 10013.1139   1022           Suomi         246        EUROOPPA     10013
## 10013.1140   1022           Suomi         246        EUROOPPA     10013
## 10013.1141   1022           Suomi         246        EUROOPPA     10013
## 10013.1142   1022           Suomi         246        EUROOPPA     10013
## 10013.1143   1022           Suomi         246        EUROOPPA     10013
## 10013.1144   1022           Suomi         246        EUROOPPA     10013
##                    indicator.title.fi year gender primary.value
## 10013.1139 (EU) Nuorisotyöttömyysaste 1991  total          16.3
## 10013.1140 (EU) Nuorisotyöttömyysaste 2010   male          23.8
## 10013.1141 (EU) Nuorisotyöttömyysaste 1996   male          29.5
## 10013.1142 (EU) Nuorisotyöttömyysaste 2000  total          21.4
## 10013.1143 (EU) Nuorisotyöttömyysaste 1995  total          29.7
## 10013.1144 (EU) Nuorisotyöttömyysaste 1998   male          22.8
##            absolute.value                indicator.organization.title.fi
## 10013.1139             NA Euroopan yhteisöjen tilastotoimisto (Eurostat)
## 10013.1140             NA Euroopan yhteisöjen tilastotoimisto (Eurostat)
## 10013.1141             NA Euroopan yhteisöjen tilastotoimisto (Eurostat)
## 10013.1142             NA Euroopan yhteisöjen tilastotoimisto (Eurostat)
## 10013.1143             NA Euroopan yhteisöjen tilastotoimisto (Eurostat)
## 10013.1144             NA Euroopan yhteisöjen tilastotoimisto (Eurostat)
```

```r

# Pick indicator name
indicator.name <- as.character(unique(dat$indicator.title.fi))
indicator.source <- as.character(unique(dat$indicator.organization.title.fi))

# Visualize
library(ggplot2, quietly=TRUE)
theme_set(theme_bw(20)); 
p <- ggplot(dat, aes(x = year, y = primary.value, group = gender, color = gender)) 
p <- p + geom_line() + ggtitle(paste(indicator.name, indicator.source, sep = " / ")) 
p <- p + xlab("Year") + ylab("Value") 
p <- p + theme(title = element_text(size = 10))
p <- p + theme(axis.title.x = element_text(size = 20))
p <- p + theme(axis.title.y = element_text(size = 20))
p <- p + theme(legend.title = element_text(size = 15))
print(p)
```

![plot of chunk sotkanetData](figure/sotkanetData.png) 



### Effect of municipality size

Smaller municipalities have more random variation.


```r
selected.inds <- c(127, 178)
dat <- GetDataSotkanet(indicators = selected.inds, years = 2011, genders = c('total'))
datf <- dat[, c("region.title.fi", "indicator.title.fi", "primary.value")]
dw <- reshape(datf, idvar = "region.title.fi", timevar = "indicator.title.fi", direction = "wide")
names(dw) <- c("Municipality", "Population", "Migration")
p <- ggplot(dw, aes(x = log10(Population), y = Migration)) + geom_point(size = 3)
p <- p + ggtitle("Migration vs. population size") 
p <- p + theme(title = element_text(size = 15))
p <- p + theme(axis.title.x = element_text(size = 20))
p <- p + theme(axis.title.y = element_text(size = 20))
p <- p + theme(legend.title = element_text(size = 15))
print(p)
```

![plot of chunk sotkanetVisu3](figure/sotkanetVisu3.png) 




### Fetch all SOTKAnet indicators

This takes for a long time and is not recommended for regular
use. Save the data on your local disk for further work.



```r
# These indicators have problems with R routines:
probematic.indicators <- c(1575, 1743, 1826, 1861, 1882, 1924, 1952, 2000, 2001, 2033, 2050, 3386, 3443)

# Get data for all indicators
datlist <- list()
for (ind in setdiff(sotkanet.indicators$indicator, probematic.indicators)) {
  datlist[[as.character(ind)]] <- GetDataSotkanet(indicators = ind, years = 1990:2013, genders = c('female', 'male', 'total'))
}

# Combine tables (this may require considerable time and memory 
# for the full data set)
dat <- do.call("rbind", datlist)
```


For further usage examples, see
[Louhos-blog](http://louhos.wordpress.com), and
[takomo](https://github.com/louhos/takomo/tree/master/Sotkanet).


# Licensing and Citations

### SOTKAnet data

Cite SOTKAnet and link to [http://www.sotkanet.fi](http://www.sotkanet.fi/). Also mention indicator provider. 

 * [Full license and terms of use](http://uusi.sotkanet.fi/portal/page/portal/etusivu/tietoa_palvelusta). 

Central points:

 * SOTKAnet REST API is meant for non-regular data queries. Avoid regular and repeated downloads.
 * SOTKAnet API can be used as the basis for other systems
 * Metadata for regions and indicators are under [CC-BY 3.0](http://creativecommons.org/licenses/by/3.0/) 
 * THL indicators are under [CC-BY 3.0](http://creativecommons.org/licenses/by/3.0/) 
 * Indicators provided by third parties can be used only by separate agreement!


### SOTKAnet R package

This work can be freely used, modified and distributed under the
[Two-clause FreeBSD
license](http://en.wikipedia.org/wiki/BSD\_licenses). Kindly cite the
R package as 'Leo Lahti, Einari Happonen, Juuso Parkkinen ja Joona
Lehtomaki (2013). sotkanet R package. URL:
http://www.github.com/ropengov/sotkanet'.


### Session info


This vignette was created with


```r
sessionInfo()
```

```
## R version 3.0.2 (2013-09-25)
## Platform: x86_64-pc-linux-gnu (64-bit)
## 
## locale:
##  [1] LC_CTYPE=fi_FI.UTF-8       LC_NUMERIC=C              
##  [3] LC_TIME=fi_FI.UTF-8        LC_COLLATE=fi_FI.UTF-8    
##  [5] LC_MONETARY=fi_FI.UTF-8    LC_MESSAGES=fi_FI.UTF-8   
##  [7] LC_PAPER=fi_FI.UTF-8       LC_NAME=C                 
##  [9] LC_ADDRESS=C               LC_TELEPHONE=C            
## [11] LC_MEASUREMENT=fi_FI.UTF-8 LC_IDENTIFICATION=C       
## 
## attached base packages:
## [1] stats     graphics  grDevices utils     datasets  methods   base     
## 
## other attached packages:
##  [1] sotkanet_0.9.01   rgdal_0.8-16      SmarterPoland_1.2
##  [4] rjson_0.2.13      reshape_0.8.4     plyr_1.8.1       
##  [7] mapproj_1.2-2     maps_2.3-6        rgeos_0.3-3      
## [10] maptools_0.8-29   sp_1.0-14         ggplot2_0.9.3.1  
## [13] stringr_0.6.2     reshape2_1.2.2    XML_3.98-1.1     
## [16] rustfare_0.1.1    knitr_1.5.22     
## 
## loaded via a namespace (and not attached):
##  [1] codetools_0.2-8    colorspace_1.2-4   dichromat_2.0-0   
##  [4] digest_0.6.4       evaluate_0.5.1     foreign_0.8-59    
##  [7] formatR_0.10       grid_3.0.2         gtable_0.1.2      
## [10] labeling_0.2       lattice_0.20-27    MASS_7.3-29       
## [13] munsell_0.4.2      proto_0.3-10       RColorBrewer_1.0-5
## [16] Rcpp_0.11.0        scales_0.2.3       tools_3.0.2
```


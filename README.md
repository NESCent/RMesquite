# RMesquite - an R package for interoperating with Mesquite

[![RMesquite Logo](https://nescent.github.io/RMesquite/images/mesquiteR-logo.gif)](https://nescent.github.io/RMesquite)

The R package RMesquite provides basic services for R to make use of functions in the evolutionary analysis system [Mesquite]. With RMesquite, R users can have access to the interactive interface of Mesquite as well as a broad array of computations in Mesquite. (A companion package, [Mesquite.R], provides access in the reverse direction, for Mesquite to access functions in R.)

## Installation

To use RMesquite you must:
* In R, install **RMesquite**. Until the package appears on CRAN (at which point you can install from CRAN as you normally would install R packages), you can install from Github, using `install.github()` (from the devtools package) from within R. RMesquite depends on the packages rJava and ape.
* Install [Mesquite] 2.72 or later

## Starting Mesquite</h3>

Before using functions of Mesquite, start it using `startMesquite()`:
```R
library(RMesquite) 
startMesquite()
```

This simple style of starting Mesquite will work only if you have previously started your copy of Mesquite. If you have, then Mesquite will have recorded its location in its preferences file, and RMesquite will look there to discover where Mesquite is. If you haven't started Mesquite previously, then you will need to indicate the location of the Mesquite copy you want to run:
```R
library(RMesquite) 
startMesquite("/Applications/Mesquite_Folder")
```

If you want to run a headless version of Mesquite (see below), you need to either specify its location, or you need to have previously run the headless version and then indicate RMesquite is to look for it by setting `headless` to `TRUE`:
```R
library(RMesquite) 
startMesquite(headless = TRUE)
```

See the R help page for `startMesquite()` for more details.

### More information

More information can be found on the [RMesquite project page], including a few commonly encountered troubles, and some examples.

## Terms of reuse and credits

If you make use of Mesquite for the analysis of results, such as to estimate ancestral states, then you should cite the functions in Mesquite. Thus, we suggest a citation like this: &quot;The &lt;insert analysis name here&gt; analysis was performed by Mesquite 2.72 (Maddison &amp; Maddison, 2009), run via the RMesquite package (Lapp &amp; Maddison, 2009) from R version 2.10.0.&quot;

Lapp, H. &amp; Maddison, W.P. 2009. RMesquite, an R package for transparent access to Mesquite functions. http://nescent.github.io/RMesquite

RMesquite and Mesquite.R were stimulated by the [Comparative Methods in R Hackathon] at NESCent in Dec 2007, and supported by the National Evolutionary Synthesis Center (NESCent), NSF #EF-0423641.

RMesquite is distributed under a GPL version 2 license. See the file LICENSE.

[Mesquite.R]: http://mesquiteproject.org/packages/Mesquite.R
[Mesquite]: http://mesquiteproject.org
[JGR]: http://jgr.markushelbig.org/JGR.html
[RMesquite project page]: https://nescent.github.io/RMesquite
[Comparative Methods in R Hackathon]: http://informatics.nescent.org/wiki/R_Hackathon_1

Exploring and visualising spatial proteomics data
=================================================

## Introduction

The
[`pRolocGUI`](http://www.bioconductor.org/packages/devel/bioc/html/pRolocGUI.html)
package is an interactive interface to explore and visualise
experimental mass spectrometry-based spatial proteomics data. It
relies on the [`shiny`](http://shiny.rstudio.com/) framework for
interactive visualisation, the
[`MSnbase`](http://www.bioconductor.org/packages/release/bioc/html/MSnbase.html)
package to handle data and metadata and the
[`pRoloc`](http://www.bioconductor.org/packages/release/bioc/html/pRoloc.html)
software for spatial proteomics specific data matters. Example spatial
data is available in the
[`pRolocdata`](http://bioconductor.org/packages/release/data/experiment/html/pRolocdata.html)
experiment package.


The `pRoloc` suite set of software are distributed as part of the
`R`/[Bioconductor](http://bioconductor.org/) project and are developed
at the [Computational Proteomics Unit](http://cpu.sysbiol.cam.ac.uk/)
at the
[Cambridge Centre for Proteomics](http://proteomics.bio.cam.ac.uk)
labs, at the University of Cambridge.

This document describes the installation of the software, followed by
a basic quick start guide for using `pRolocGUI` to search and
visualise the organelle map. Please refer to the respective
documentation and vignettes for full details about the software.

If you use these open-source software for your research, please cite:

>  Gatto L, Breckels LM, Wieczorek S, Burger T, Lilley KS.
>  Mass-spectrometry-based spatial proteomics data analysis using pRoloc
>  and pRolocdata. Bioinformatics. 2014 May 1;30(9):1322-4.
>  doi:10.1093/bioinformatics/btu013. Epub 2014 Jan 11. PubMed PMID:
>  24413670; PubMed Central PMCID: PMC3998135.
>
>  Breckels LM, Gatto L, Christoforou A, Groen AJ, Lilley KS, Trotter
>  MW. The effect of organelle discovery upon sub-cellular protein
>  localisation. J Proteomics. 2013 Mar 21. doi:pii:
>  S1874-3919(13)00094-8. 10.1016/j.jprot.2013.02.019. [Epub ahead of
>  print] PubMed PMID: 23523639.
>
>  Gatto L., Breckels L.M., Burger T, Nightingale D.J.H., Groen A.J.,
>  Campbell C., Mulvey C.M., Christoforou A., Ferro M., Lilley K.S. 'A
>  foundation for reliable spatial proteomics data analysis' Mol Cell
>  Proteomics. 2014 May 20. 


## Installation

`pRolocGUI` is written in the [`R`](http://www.r-project.org/)
programming language. Before installing the software you need to
download `R` and also preferably `RStudio`.

1) Download `R` version >= 3.1.1 for your operating system from the (R
website)[http://www.r-project.org/] and install it.

2) Optional, but
recommended. [Download](http://www.rstudio.com/products/rstudio/download/)
and install the RStudio IDE. `RStudio` provides a good code editor and
excellent integration with the `R` terminal.

3) Start `R` or `RStudio`. 

4) Install the Bioconductor packages `pRoloc`, `pRolocdata` and
`pRolocGUI`:

`pRolocGUI` requires `R >= 3.1.1` and Bioconductor version `>=
3.0`. If you are using version is 3.1.x, type in to the console

```{r dev, eval=FALSE}
source("http://www.bioconductor.org/biocLite.R")
useDevel(TRUE) ## to use Bioc 3.0 with R 3.1.1
biocLite(c("pRoloc", "pRolocdata", "pRolocGUI"))
```

For any later version >= 3.2:

```{r install, eval=FALSE}
source("http://www.bioconductor.org/biocLite.R")
biocLite(c("pRoloc", "pRolocdata", "pRolocGUI"))
```

To check the version of your `R` installation, check your session
information:

```{r version}
sessionInfo()
```


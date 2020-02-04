# SampleSize4ClinicalTrials: Sample Size Calculation for the Comparison of Means or Proportions in Phase III Clinical Trials

[![CRAN status](http://www.r-pkg.org/badges/version/SampleSize4ClinicalTrials)](https://cran.r-project.org/package=SampleSize4ClinicalTrials) 
[![](https://cranlogs.r-pkg.org/badges/grand-total/SampleSize4ClinicalTrials)](https://CRAN.R-project.org/package=SampleSize4ClinicalTrials)
[![Download counter](http://cranlogs.r-pkg.org/badges/SampleSize4ClinicalTrials)](https://cran.r-project.org/package=SampleSize4ClinicalTrials) 
[![Rdoc](http://www.rdocumentation.org/badges/version/SampleSize4ClinicalTrials)](https://cran.r-project.org/package=SampleSize4ClinicalTrials) 

<img src="man/logo/logo.png" height = "200" align = "right"/>

Description
------------

The package **SampleSize4ClinicalTrials** aims to calculate the sample size for both the treatment and control arm in the comparison of means and proportions in phase III clinical trials.

There are four categories of Phase III clinical trials according to different research goals, including (1) Testing for equality, (2) Superiority trial, (3) Non-inferiority trial, and (4) Equivalence trial. The **ssc_meancomp** and **ssc_propcomp** function in the package allow for the calculation of sample size in the comparison of means and proprtions respectively in the above four study designs.

Installation
------------
The package can be installed from CRAN:
```r
install.packages("SampleSize4ClinicalTrials")
```

It can also be installed from GitHub using the **devtools** package:
```r
devtools::install_github("QiHongchao/SampleSize4ClinicalTrials")
```

Usage
------------
```r
library(SampleSize4ClinicalTrials)

##The comparison of means, a non-inferiority trial and the non-inferiority margin is -0.05
ssc_meancomp(design=3L, ratio=1, alpha=0.05, power=0.8, sigma=0.01, theta=0, delta=-0.05)

##The comparison of proportions, equivalence trial and the equivalence margin is 0.2
ssc_propcomp(design=4L, ratio=1, alpha = 0.05, power=0.8, p1=0.75, p2=0.80, delta = 0.2)

```

Reference
------------

Chow S, Shao J, Wang H. 2008. Sample Size Calculations in Clinical Research. 2nd Ed. Chapman & Hall/CRC Biostatistics Series.

Yin, G. 2012. Clinical Trial Design: Bayesian and Frequentist Adaptive Methods. John Wiley & Sons.

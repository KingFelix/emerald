---
title: "Blog Post example"
author: "IngaPa"
tags: [ r-bloggers, shiny, tutorial, R-package]
date: "9/7/2019"
lastupdated: 2019-09-09
published: true
---

 Each blog post should contain following categories:
  
  __1. IDEA__ (1-2 sentance about the idea of the post)
  
  __2. Introduction:__
      2.a. What is [phenotype of interest]?
      2.b. Genetic background of the [phenotype of interest]
      
  __3. How can I identify risk variants in my genome that are associated with [phenotype of interest] using myDNA R package?__
  
  __4. Limitations of the myDNA analysis__
  
  __5. Possible suggestions/Other approaches__

  __6.Where can I find more info about lactose intolerance?__


# IDEA

(1-2 sentance about the idea of the post)
  
## What is [phenotype of interest]?
[....]

## Genetic background of the [phenotype of interest]
 [....]
 
##How can I identify risk variants in my genome that are associated with [phenotype of interest] using myDNA R package?__



__Step 1. Genotype your genome.__ 

At the moment, the easiest way to do it is to buy a [direct-to-consumer](https://www.fda.gov/medical-devices/vitro-diagnostics/direct-consumer-tests) test by one of the [DNA testing companies](https://isogg.org/wiki/List_of_DNA_testing_companies). 



__Step 2. Download your genotypes__ and store them on your computer

__Step 3. Install R, RStudio and myDNA R package__

*  Install R from: [here](https://cloud.r-project.org/)
*  Install RStudio from: [here](https://download1.rstudio.org/desktop/windows/RStudio-1.2.1335.exe)
*  Learn about R and RStudio by watching [this youtube video](https://www.youtube.com/watch?v=lVKMsaWju8w)

*  Open RStudio and open new RScript ( click on File -> Rscript) 
*  Install myDNA R package from my GitHub account by running:


```{r}
install.packages("BiocManager") 
BiocManager::install("IngaPa/myDNAS")

```

* 	And import myDNA library by running:

```{r}
library(myDNA)	
```
Your R session should look as follows:
 
[add figure here] 
  
  
__Step 4. Import your genome in R by running:__  
  
  
```{r}
importDNA("write-full-path-here") 
```
In your R script you should type something like:

[add figure here]

Now, my genome appeared as a variable in the R environment.
Notice, it has __[add number]__ rows and __[add number]__ columns.
  
  
  
It means that __[add number]__ positions (SNPs) in my genome are genotyped.



For each position, I received the following info:

    1) unique identifier for each SNP (rsid), 
    2) chromosome where each SNP is located,
    3) location on the chromosome,
    4) your genotype;

This corresponds to four reported columns.

If you wish to observe imported file, you can run head() function. For example, 

```{r}
head(myGenome) 
```
returns: 
  
[add figure here]
  

The first row of myGenome data table can read as follows:

[....]



__Step 5. Perform myDNA [phenotype of interest] analysis__
myDNA R package contains the __[add name]__ function that for __[add here]__ SNP extracts info about your genotype. 



By running
```{r}
functionName(myGenome)
```
 I got the following results:
 
[add figure here]


__Step 6. Results interpretation__

[....]


## Limitations of the myDNA analysis
[....]


## Possible suggestions/Other approaches
[....]


## 7. Where can I find more info about lactose intolerance?


## Appendix I: my full R code:
[add figure here]

## Appendix II: Details (sessionInfo) about analysis:
[add figure here]



## 8. About author

## 9. Disclaimer

Information shared in this post is for educational purposes only. We do not diagnose or prevent any illness or disease. This post has not been evaluated by the Food & Drug Administration or any other medical body. You must consult your doctor before acting on any content on this post.

In addition,  most human traits and diseases are products of interactions of hundreds of genes and variants influenced by many non genetic factors. Thus, SNPs presented in this post are likely only a very small puzzle piece in a large picture of genetic, epigenetic and environmental influences on the development of trait. 


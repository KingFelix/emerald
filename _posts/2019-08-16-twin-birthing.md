---
published: true
title: How likely you are of having twins?
---

### Here is a step-by-step guide to find it out

## Info: Make sure to have your genotyped genome saved in a folder onto your computer.

The likelihood of conceiving twins is a complex trait. It is probably affected by multiple genetic and environmental factors, depending on the type of twins. The two types of twins are classified as monozygotic and dizygotic.

Monozygotic (MZ) twins, also called identical twins, occur when a single egg cell is fertilized by a single sperm cell. The resulting zygote splits into two very early in development, leading to the formation of two separate embryos. MZ twins occur in 3 to 4 per 1,000 births worldwide. Research suggests that most cases of MZ twinning are not caused by genetic factors. However, a few families with a larger-than-expected number of MZ twins have been reported, which indicates that genetics may play a role. It is possible that genes involved in sticking cells together (cell adhesion) may contribute to MZ twinning, although this hypothesis has not been confirmed. Most of the time, the cause of MZ twinning is unknown.

Dizygotic (DZ) or fraternal twins happen when two eggs are simultaneously fertilized instead of just one. Usually, a woman only releases a single egg at a time. Fraternal twins can only happen if a mother releases two eggs in one cycle. This is called hyperovulation. Some women have versions (called alleles) of these genes that make them more likely to hyperovulate. This means there is a higher chance that two eggs could get fertilized at once, leading to fraternal twins. However, only women ovulate. So, the mother’s genes control this and the fathers don’t. Scientists have found two genes that increase a woman’s chance of having twins—one that affects follicle-stimulating hormone levels and another that may alter how ovaries respond to them. The second of these may also have implications for why some women respond better than others to in vitro fertilization.


Genome-wide association study(GWAS) is an observational study of a genome-wide set of genetic variants in different individuals to see if any variant is associated with a trait. GWASs typically focus on associations between single-nucleotide polymorphisms (SNPs) and traits like major human diseases, but can equally be applied to any other genetic variants and any other organisms.
There are SNPs in GWAS asocciated with dizygotic twin birthing:
rs11031006-G, rs17293443-C, rs12064669-C,  rs428022-A, rs11031006-G
![Aug14_2018_AtlasOfScience_SNPs1891704823.jpg](/myDNA/img/Aug14_2018_AtlasOfScience_SNPs1891704823.jpg)


With our programme represented down below you can easily find out if you have these risk alleles and so the posibility of having twins.
Also you can learn more about genetics and programming doing so. For this programme we have used R programming language which is used for analyzing scientific data.

###### Step 1: Download R and RStudio

R: [https://cloud.r-project.org/](https://cloud.r-project.org/)
RStudio: [https://download1.rstudio.org/desktop/windows/RStudio-1.2.1335.exe](https://download1.rstudio.org/desktop/windows/RStudio-1.2.1335.exe)

                      
Sources: [https://genetics.thetech.org/ask-a-geneticist/twin-genetics](https://genetics.thetech.org/ask-a-geneticist/twin-genetics)
		              [https://ghr.nlm.nih.gov/primer/traits/twins](https://ghr.nlm.nih.gov/primer/traits/twins)
		 			  [https://www.sciencemag.org/news/2016/04/having-fraternal-twins-your-genes-and-your-hormonesfound](https://www.sciencemag.org/news/2016/04/having-fraternal-twins-your-genes-and-your-hormonesfound)
gwastwin <- gwas[grep("twin", gwas$`DISEASE/TRAIT`), ]

---
published: true
---
### Step-by-step guide to check whether risk allele for lactose intolerance can be found in your genome
Info: Lactose Intolerance is primarily linked to 2 SNPs found in the introns of the MCM6 gene, which is associated with the LCT gene located thousands of base pairs away. 
- In 77% of Europeans: rs4988235 and rs182549, for which the (T) and (A) alleles, respectively, form a haplotype predicting lactase persistence (thus avoiding lactose intolerance).
- A different SNP, rs145946881, known as "G/C-14010", appears to be associated with lactase persistence in sub-Saharan African populations. 
- Two other nearby SNPs, rs41380347 "T/G(-13915)" and rs41525747 "C/G(-13907)", are also associated to a lesser degree.

Source: [Lactose intolerance SNPedia](https://www.snpedia.com/index.php/Lactose_intolerance)

Alleles: 
- GG - likely to be lactose intolerant
- CG/CC - likely to not be lactose intolerant

Note: Make sure to have your sequenced/genotyped genome saved in a folder onto your computer. 


**Step 1:** Download R and RStudio
- R: [https://cloud.r-project.org/](https://cloud.r-project.org/)
- RStudio: [https://download1.rstudio.org/desktop/windows/RStudio-1.2.1335.exe](https://download1.rstudio.org/desktop/windows/RStudio-1.2.1335.exe)

**Step 2:** Open RStudio and open a project.
- Go to "File" and then click on "Open Project..."
- Select the folder containing your DNA and click "Open" in botton right corner. 
Now you should be able to see the files your folder contains in the buttom-right window of your screen:
![files_in_rstudio](/emerald/img/IngaDNAonRstudio.PNG)

**Step 3:** Write a function to screen for lactose intolerance.

- @param [insert name of ]
- @import "stringr"
![import_code](/emerald/img/lactose_import.PNG)
![function_code](/emerald/img/lactose_function.PNG)

**Step 4:** Write the code to screen for the "G-allele"

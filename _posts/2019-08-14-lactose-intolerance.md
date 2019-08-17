---
published: true
---
### Step-by-step guide to check whether risk allele for lactose intolerance can be found in your genome
Info: Lactose Intolerance is primarily linked to SNPs found in the introns of the MCM6 gene, which is associated with the LCT gene located thousands of base pairs away. 
- In 77% of Europeans: rs4988235 and rs182549, for which the (T) and (A) alleles, respectively are associated with lactase persistence (thus avoiding lactose intolerance).
- A different SNP, rs145946881 is found to be associated with lactase persistence in sub-Saharan African populations. 
- SNPs rs41380347 and rs41525747, are also associated to a lesser degree.

Source: [Lactose intolerance SNPedia](https://www.snpedia.com/index.php/Lactose_intolerance)

Note: Make sure to have your genotyped genome saved in a folder onto your computer. 


**Step 1:** Download R and RStudio
- R: [https://cloud.r-project.org/](https://cloud.r-project.org/)
- RStudio: [https://download1.rstudio.org/desktop/windows/RStudio-1.2.1335.exe](https://download1.rstudio.org/desktop/windows/RStudio-1.2.1335.exe)

**Step 2:** Open RStudio and open a project.
- Go to "File" in the top left corner of your laptop screen and then click on "New Project..."

**Step 3:** Type the following code to download the myDNA package to analyze your DNA: 
- install.packages("BiocManager")
- BiocManager::install("IngaPa/myDNAS")
Your code should look like this: 
![install_code](/myDNA/img/code4lactose.PNG)
Now you can run your code by clicking the "Run" button or by using the [ctrl][shift][enter] keys on your keyboard. 

**Step 4:** IMPORTANT: If you are a Windows user, make sure to install Rtools before installing myDNA package. 
To do this write the following code and then run it:
- install.packages('installr')
- library(installr)
- installr:install.Rtools()
Compare your code with the code displayed below:
![install_code](/myDNA/img/allcode.PNG)

**Step 5:** Now you can screen your DNA for lactose intolerance :)

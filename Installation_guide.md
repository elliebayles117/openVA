This guide presents an overview for installing **openVA** package, with some common error reports and solutions at the end.

## 1. Overview of openVA package structure
Whenever the **openVA** package is loaded to R, it also requires four other core packages on CRAN for each of the VA coding methods, namely, **InSilicoVA**, **InterVA4**, **Tariff**, and **nbc4va**, and **ggplot2** for visualization. Additionally, the **InSilicoVA** package further requires the dependency of **coda** and **rJava** for its computation. 

Users typically need to take no specific action regarding the dependencies, since R takes care of them automatically. However, sometimes issues with installing **openVA** package can arise because of some of the dependencies, which may require additional configurations and re-installing the package. I find that most of the times, the errors stem from loading **rJava**, and thus is the main focus of this guide.

## 2. Pre-requisites
As the name suggests, to properly load the package **rJava**, you will need two key ingradients: _R_, and _Java_. Here is how you can make sure you have the right combination of the two:
 
### Check R environment 
1. If you do not aleady have it, install from [CRAN](http://cran.r-project.org/). Follow the instructions at the link to choose a mirror that will take you to the download page. After download, double click the file to install.
2. Open R. On the welcome message, there is a line starting with “Platform” and ending with “(32-bit)” or “(64-bit)”. It is very important to know which version (32-bit or 64-bit) of R you use, since the Java JDK should have the same version. 
3. Sometimes multiple versions of R could be installed on the same machine, so you should check the version you wish to use for data analysis. For example, if you prefer using RStudio to run the codes, you should check the default R version of RStudio by reading the welcome message for RStudio, instead of, say, the R version when opening from command line.

### Check Java installation
1. To check if Java in installed on your machine, open terminal if you use Mac or Linux, or Command Prompt if Windows, and type in ```java -version```. If Java is installed, it will show the Java version number. Version number at least 1.7.x should be sufficient.
2. If no Java is installed, or version too low, you should download and install a newer Java JDK by following the instructions at http://www.oracle.com/technetwork/java/javase/downloads/index.html. On that page, there are downloads for both “Java SE 8uXX” and “Java SE 7uXX” (XX is the specific most recent re- leased subversion number), which stands for Standard Edition Java 8 and 7. The required download is JDK (Java Development Kit). Click on download link for JDK and choose the appropriate version. You should choose “x86” version if your R version is 32-bit, and “x64” if R is 64-bit. Then follow the instructions to finish download and install Java.
3. After successfully installing Java, try again typing ```java -version``` on terminal or Command Prompt. It should show the correct version number just installed.

## 3. Misc suggestions
1. For users not familiar with R envrionment, see [the official introduction](https://www.r-project.org/about.html).
2. Many people find using R from Rstudio to be most convenient. Rstudio could be downloaded from [its website](https://www.rstudio.com/products/rstudio/download3/). 


## 4. Errors and solutions
If you encounter other errors not listed here, or could not resolve the errors following the steps listed, or would like to propose new solutions, you are more than welcome to contact me (Richard Li, lizehang@uw.edu) or submit issue reports to [this Github repository](https://github.com/richardli/openVA/issues).

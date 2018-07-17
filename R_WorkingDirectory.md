
# Working directory

## Get working directory

```r
wd <- getwd()
```

## Set working directory

```r
setwd('/my/new/working/directory')
```


### at current script parent path

Why? To be able to source other script file near the current one without passing the full path.

#### rstudio

```r
wd <- dirname(rstudioapi::getActiveDocumentContext()$path) # or dirname(sys.frame(1)$ofile)
setwd(wd)
```

#### universal solution by installing package `here`

```r
install.packages("here")
library(here)

wd <- here()
setwd(wd)
```

https://github.com/jennybc/here_here


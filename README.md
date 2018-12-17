---
---
title: "BAHCS-10 Prelim Results"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```
Library packages
```{r}
library(lavaan)
library(psych)
library(semTools)
library(dplyr)
library(ltm)
library(prettyR)
library(semTools)
library(GPArotation)
library(lavaan)
library(psych)
library(semTools)
library(dplyr)
library(ltm)
library(lordif)
library(Amelia)
library(plyr)
library(paran)
library(caret)
library(prettyR)
library(lme4)
#library(lmerTest)
library(MuMIn)
library(HLMdiag)
library(nlme)
library(MASS)
library(descr)
library(brms)
library(future)
```
Get data
```{r}
setwd("C:/Users/Matthew.Hanauer/Desktop")
GPRAAll = read.csv("ConnGPRA.csv", header = TRUE) 

# subet the data based on 1's for baseline and 2's for six-month.  Then write as CSV's, then merge together.
GPRAConBase = subset(GPRAAll, InterviewType ==1)
dim(GPRAConBase)

### Demographics
sum(GPRAConBase$RaceBlack, na.rm = TRUE)
sum(GPRAConBase$RaceWhite, na.rm = TRUE)
describe.factor(GPRAConBase$HispanicLatino)
sum(GPRAConBase$RaceOther, na.rm = TRUE)
describe.factor(GPRAConBase$Gender)

```


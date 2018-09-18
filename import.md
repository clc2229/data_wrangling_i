---
title: "Import"
author: "Christopher Crowe"
date: "September 18, 2018"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)

library(tidyverse)
```

## Import FAS csv files

```{r litters}
litters_data = read_csv(file = "./data/FAS_litters.csv")
litters_data = janitor::clean_names(litters_data)
```

```{r pups}
pups_data = read_csv(file = "./data/FAS_pups.csv")
pups_data = janitor::clean_names(pups_data)
```


## Look at data

Looks at the data

```{r}

## top of data
head(litters_data)

## bottom of data
tail(litters_data)

## summary of data
skimr::skim(litters_data)
```


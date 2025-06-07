---
layout: post
title: "Conversation piece"
date: 2025-06-07
tags: [depmap, data]
excerpt: "A look at DepMap data."
---

# Conversation piece

A look at DepMap data.

## The data

DepMap contains CRISPR knockout screening data across cancer cell lines. Gene dependency scores indicate how much each cell line relies on each gene for survival.

```r
library(tidyverse)
library(ggplot2)

# Load datasets
gene_effect <- read_csv("CRISPR_gene_effect.csv")
sample_info <- read_csv("sample_info.csv") 
gene_info <- read_csv("CRISPR_gene_dependency.csv")

dim(gene_effect)

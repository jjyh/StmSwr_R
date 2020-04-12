---
title: "Data Sourcing"
teaching: 10
exercises: 10
questions:
- "What does the available data look like?"
- "What clean-up is required?"
objectives:
- "Understand data format"
- "Perform clean-up"
keypoints:
- "Thinking where data may be messy"
- "Identify gap between current state of data and the way we need it for manipulation"
---
## CMMS data retrieval
Stormwater assets are registered within the CMMS database.  
```
{r, echo=FALSE}
cmmsdata<-read_excel('stormwater survey data.xlsx')
#explore created dataframe
str(cmmsdata) 
```
Reviewing the structure of data table prior to processing:
1. Only several fields are of known acceptable quality/recent updates
1. Typos prevalent
1. Unclear abbreviations also prevalent
1. Field/column headers are messy (spaces, special characters)
1. some information recorded, e.g. "depths", are erroneous in principle, and should not be processed/further used

Coordinate information exists but embedded with general description and misc. text in a single field.  Some assets have multiple coordinates (e.g. two ends of a ditch).

{% include links.md %}


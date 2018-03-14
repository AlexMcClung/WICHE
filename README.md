## Working with WICHE projections of high school graduates

https://knocking.wiche.edu/data

Direct link to raw data download (xlsx):

https://knocking.wiche.edu/s/All-Enrollment-and-Graduate-Projections-zlxg.xlsx

```r
# Read the excel data into R

require('readxl')

excel_sheets('All+Enrollment+and+Graduate+Projections.xlsx')

df <- read_excel('All+Enrollment+and+Graduate+Projections.xlsx', sheet = 'Projections')

```
The `Data Notes` sheet serves as the codebook

```r
# Get estimated graduates for your state

df %>% filter(STABR == 'NJ' & TYPE %in% c('G','NP')) %>% # G = public, NP = Private
  group_by(SURVYEAR) %>% 
  summarize(grads = sum(DPL))
```

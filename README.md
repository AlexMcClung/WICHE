## Working with WICHE projections of high school graduates

https://knocking.wiche.edu/data

Direct link to raw data download (xlsx):

https://knocking.wiche.edu/s/All-Enrollment-and-Graduate-Projections-zlxg.xlsx

```r
require('readxl')

excel_sheets('All+Enrollment+and+Graduate+Projections.xlsx')

df <- read_excel('All+Enrollment+and+Graduate+Projections.xlsx', sheet = 'Projections')

```
The `Data Notes` sheet serves as the codebook

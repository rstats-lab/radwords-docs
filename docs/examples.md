### Installation
```R
install.packages("RAdwords")
library(RAdwords)
```
### Authentication
```R
library(RAdwords)
google_auth <- doAuth()
```

### Create Statement
```R
body <- statement(select=c('Clicks','AveragePosition','Cost','Ctr'),
					report="ACCOUNT_PERFORMANCE_REPORT",
					start="2014-03-20",
					end="2014-03-21")
```

### Query Adwords API and load data as dataframe

```R
# make sure to use the Adwords Account Id (MCC Id will not work)
data <- getData(clientCustomerId='xxx-xxx-xxxx',
                google_auth=google_auth,
                statement=body)
```

### List available report types

```R
reports()
```

### List available metrics/attributes of specific report type

```R
metrics(report='ACCOUNT_PERFORMANCE_REPORT')
```
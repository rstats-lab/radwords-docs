### NAs introduced by coercion
```getData()``` prints a warning message:  

```R
Warning message:
NAs introduced by coercion 
```

Most likley you query data which are not available by the AdWords API. 

There are specific metrics like ```SearchRankLostImpressionShare, SearchExactMatchImpressionShare, SearchImpressionShare, SearchPredictedCtr``` which do not have data on certain AdWords segments (e.g. the content network).  

A commen case of this issue occures when you query competition metrics (```SearchRankLostImpressionShare```) which are only available for the google search. However your keywords are running in the google search and in the google content network at the same time.

### Cannot get keywords

Since AdWords API version 201601 the attribute name ```KeywordText```is no longer valid. Use ```Criteria```instead.

### Send mutate jobs

Is it possible to send mutate jobs wo the API?  

No it´s not. RAdwords uses the reporting service of the AdWords API which only allows to retrieve data. Changing campaigns, keywords, AdWords settings, etc. is not possible with the package.

### List account IDs

How to list all AdWords account IDs which are in my MCC?

We would love to implement this feature! Unfortunately the Adwords API reporting service does not allow to query the account information on client center level.  

However the good is, you only need to authenticate once in order to access all accounts within your MCC. Best practice is to create a vector containing the account IDs and loop over the vector.

Example:

```R
# authentication, once done you can access all accounts in your MCC
google_auth <- doAuth()
# specify date range, i.e. last two weeks until yesterday
yesterday <- Sys.Date()-1
twoWeeks <- Sys.Date()-14
# create statement
body <- statement(select=c'Date','AccountDescriptiveName','CampaignName','Impressions','Clicks','Cost','Conversions'),
                  report="CAMPAIGN_PERFORMANCE_REPORT",
                  start=twoWeeks,
                  end=yesterday)
#vector of account IDs
accounts <- c("xxx-xxx-xxxx",#Account 1
              "xxx-xxx-xxxx",#Account 2
              "xxx-xxx-xxxx")#Account 3
#loop over accounts and rbind data to dataframe
dataList <- list()
for(account in accounts){
	dataList[account] <- getData(clientCustomerId=account,statement=body,google_auth = google_auth)
}
data <- do.call(rbind, dataList)
```




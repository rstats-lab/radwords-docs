### Build a query

With ```statement()``` function you can build a statement for querying the Adwords API. For possible reports and metrics see the [reports section](reports.md). 

### Examples
```R
#Example 1
body <- statement(select=c('Clicks','AveragePosition','Cost','Ctr'),
					report="ACCOUNT_PERFORMANCE_REPORT",
					start="2014-03-20",
					end="2014-03-21")
#Example 2
body <- statement(select=c('CampaignName','Clicks','Cost','Ctr'),
                  report="CAMPAIGN_PERFORMANCE_REPORT",
                  where="CampaignName STARTS_WITH 'A' AND Clicks > 100",
                  start="2014-03-20",
                  end="2014-03-21")
#Example 3
body <- statement(select=c('Criteria','Clicks','Cost','Ctr'),
                  report="KEYWORDS_PERFORMANCE_REPORT",
                  where="Clicks > 100",
                  start="2014-03-20",
                  end="2014-03-21")  					
```

### Details

RAdwords uses the AdHoc reporting services of the AdWords API. This service supports statements of the [Adwords Query Language (AWQL)](https://developers.google.com/adwords/api/docs/guides/awql).
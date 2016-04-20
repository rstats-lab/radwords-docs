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
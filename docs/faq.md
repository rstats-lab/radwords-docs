### NAs introduced by coercion
```getData()``` prints a warning message:  

```R
Warning message:
NAs introduced by coercion 
```

Most likley you query data which are not available by the AdWords API. 

There are specific metrics like ```SearchRankLostImpressionShare, SearchExactMatchImpressionShare, SearchImpressionShare, SearchPredictedCtr``` which do not have data on certain AdWords segments (e.g the content network).  

A commen case of this issue occures when you query competition metrics (```SearchRankLostImpressionShare```) which are only available for the google search. However your keywords are running in the google search and in the google content network at the same time.
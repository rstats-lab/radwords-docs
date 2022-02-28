# RAdwords User Manual 

Welcome to the official documentation of the R Adwords package for Google Adwords. RAdwords enables users of the R Language for Statistical Computing to directly access their Google Adwords account in order to consume and analyze information provided by the Adwords API.

## :exclamation::exclamation: Google AdWords API Sunset :exclamation::exclamation:

> **The Google AdWords API will [sunset on April 27, 2022](https://ads-developers.googleblog.com/2021/04/upgrade-to-google-ads-api-from-adwords.html).  
> Upgrade to the Google Ads API with our new R package [{r4googleads}](https://github.com/banboo-data/r4googleads).
> Follow our [RAdwords Migration Guide](https://banboo-data.github.io/r4googleads/articles/radwords-migration-guide.html).**

Is our work helpful for you and you want to support us? We`ll be happy to have some coffee(s) from you!
<a href="https://www.buymeacoffee.com/banboo" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/default-orange.png" alt="Buy Me A Coffee" height="41" width="174"></a>

## General

RAdwords is a license cost free open source project by [@jburkhardt](https://github.com/jburkhardt) and [@mbannert](https://github.com/mbannert).
Our package implements three main features:

**First**, the package provides OAUTH2 authentication for R with an user's Google Adwords account. 

**Second**, the package offers an R interface to apply the Adwords Query Language from within R. The Adwords API can be used to obtain adhoc reports. 

**Third**, the received data is transformed to standard R data objects that can be easily analyzed from within R or export to standard file formats.


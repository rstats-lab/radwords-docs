### Retrieve Data

```getData()``` posts the Adwords Query Language Statement (AWQL) which you created with the [statement() function](query.md). The function retrieves data from the Adwords API and returns the data as a dataframe if ```transformation=T```.


### Example
```R
# make sure to use the Adwords Account Id (MCC Id will not work)
data <- getData(clientCustomerId='xxx-xxx-xxxx',
                google_auth=google_auth,
                statement=body, #object created with statement()
                transformation = T, #data are transformed from xml text to R dataframe
                changeNames = T) #column names are changed to more useful expressions
```


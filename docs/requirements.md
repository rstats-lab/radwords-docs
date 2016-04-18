### Requirements

In order to access the AdWords API you need to satisfy the following:  

- Google API project (client ID, client secret)
- AdWords MCC (my client center)
- AdWords API Developer Token


Missing one of the above mentioned items you cannot access the AdWords API. 

We recommend to use the same email (user account) for the Google API project and the AdWords MCC.

### Google API Project

Set up a [Google API project](https://console.developers.google.com) for **native apps**. The Google API project provides a **Client Id** and **Client Secret** which is necessary for the authentication.

1. Create credentials

	Click Credentials > Create Credentials > OAuth client ID

	![Google API Project](images/googleAPIProject1.png)

2. Select Application Type: Other

	![Google API Project Type](images/googleAPIProject2.png)

3. Copy client ID and client secret

	![Google API Project OAuth Client](images/googleAPIProject3.png)

### Adwords MCC

Moreover you need to set up an [AdWords My Client Center](https://www.google.com/adwords/manager-accounts/). A single AdWords account is not sufficient.

### AdWords Developer Token

Once your AdWords MCC is set up you have to apply for an AdWords developer token. You can do this within the settings of the AdWords MCC account.  

Navigate to:

Adwords MCC > Account settings > AdWords API Center > Developer Token Details > Apply for Standard Access

**Important:**  An AdWords API Test Account will not allow you to load data. You need to have **Basic access** level at least.


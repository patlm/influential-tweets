# Influential Tweets

[Goal](#Goal)

[Getting Started](#Getting-Started)

[Indexes](#Indexes)

[Todo](#Todo)

## Goal

The goal of this project is to determine "Influential Tweets" on the Twitter platform by finding tweets with the highest number of interactions from individuals within "indexes" over a set time period. These "indexes" consists of groups of Twitter users considered influential within certain areas. Indexes included with this project consist of the top followed accounts, accounts within the space field, and finance field accounts. Currently, interactions consist of retweets, replies to tweets, and quote tweets. All interactions are currently considered equal in terms of their influence.

## Getting Started

To start running this project on your local machine, follow these steps:

1. Apply for a [Twitter Developer Account](https://developer.twitter.com/en/apply-for-access).

2. Create an App on the [App Page](https://developer.twitter.com/en/apps) of your developer account.  Enter all of the required information into the form to provide information about your use case for the app.

3. Once the app is created, you can go to the `Permissions` tab at the top of the app's page and change access permission to `Read-only` if you want.  The tweet analyzer does not do any writing to Twitter so write permissions are not needed.

4. Look under `Keys and tokens` tab at the top of the app's page to find an `API key` and `API secret key`. They should both be listed under the Consumer API keys section of the page.  These keys will be used in the next step.

5. Create a file named `.env` in the root directory of this repository. The format of the file should be the same as `example.env` except replacing `{key_here}` with the API key and replacing `{secret_here}` with the API secret key you found in the previous step.  Your file should similar to this once finished (except with your own valid keys):

   ```
   CONSUMER_KEY=aBcDef1234gHijkLm
   CONSUMER_SECRET=fghijK9876abcdEfgHiJJK
   ```

6. Next, open `influential-tweets.ipynb` in Jupyter Notebook.

7. The top section of the notebook contains variables that you can configure when completing the analysis.

8. You are now set up and ready to run the project using Jupyter Notebook! Feel free to experiment and make your own modifications to the program!

## Indexes

Indexes currently included within the project all contain 100 accounts considered influential within the topic. Accounts can be added to the current indexes and new indexes can be created using a simliar format to the current indexes available.

- Top 100 Followed Accounts [`data/top-100.json`]
  - Source: https://friendorfollow.com/twitter/most-followers/
- Space [`data/space-100.json`]
  - To compile this list, I used a combination of sources and added well-known accounts relating to space
  - Sources:
    - https://www.siliconrepublic.com/innovation/10-top-twitter-accounts-for-space
    - https://www.mentalfloss.com/article/58017/15-twitter-accounts-space-nerds
    - https://mashable.com/2011/07/08/twitter-astronomy/
    - https://mashable.com/2012/10/06/space-twitter-accounts/
    - https://www.nationalgeographic.com/news/2013/5/130516-space-science-social-media-twitter-nasa-astronaut-hadfield/
- Finance [`data/finance-100.json`]
  - Compiled the list using the two sources linked below
  - Sources: 
    - https://www.forbes.com/sites/alapshah/2017/11/16/the-100-best-twitter-accounts-for-finance/#73cbbfbe7ea0 
    - https://www.marketwatch.com/story/finance-twitter-the-50-most-important-people-for-investors-to-follow-2018-12-13

## Todo

[ ] Verify replies that are part of threads do not count towards tweet interactions

<br>

<br>

<br>

Note: When using the Twitter API and developer tools, always ensure you are using it within the bounds of their [Developer terms](https://developer.twitter.com/en/developer-terms).
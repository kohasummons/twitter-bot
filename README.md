<h1 align ="center">Twitter Bot</h1>

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/Pradumnasaraf/Twitter_Bot.git)

This repo contains the source for the **Twitter bot** which Tweet out the latest Ticket price after a fixed interval of time.

All the bots are made with the help of [`tweepy`](https://github.com/tweepy/tweepy) library for accessing the Twitter API, and [`CoinMarketCap`](https://coinmarketcap.com/api/documentation/v1/) API for accessing the latest financial market data, and [`Railway`](https://railway.app/) for the deployment.

<p align="center"><img src="https://user-images.githubusercontent.com/51878265/150635263-e2c0e19b-2dcb-434c-a2a1-39a5f79e40d2.png"></p>

## ✔️ Prerequisite

- **Twitter Developer Account**

  - We need to get a developer account for getting private keys and secrets. we can apply from it [here](https://developer.twitter.com/en/portal/petition/essential/basic-info), it will take 5-10 min for setting up a Dev account.

- **CoinMaerketCap API Keys** (Optional if we don't need any financial market data)

  - We can use any financial market API for getting the latest quote of the assets, but here we are using the `CoinMarketCap API` free plan. we can get API access from [here](https://coinmarketcap.com/api/).

- **Railway Account** (Only necessary if we want to host the bot, not for running locally)
  - For deploying and running we will use [Railway](https://railway.app/). Here we are using Railway because it's free and can run the bot for 24X7 without any refreshment.

## 🖱️ Using and quick set-up guide:

- Fork this repository

- Install all the dependencies from [`requirements.txt`](requirements.txt) file. We can also use the command to install all the dependencies at once.

```sh
pip3 install -r requirements.txt
```

- Create a `.env` file in the root folder and add in our API keys and like so :

```
Note: Here I have included 2 sets of keys because I am running 2 different bots from the same repo,
we can also use one of them, either BTC or Doge

BTC_CON_KEY = XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX     (TWITTER_CONSUMER_KEY)
BTC_CON_SECRET = XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX  (TWITTER_CONSUMER_SECRET)
BTC_KEY = XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX         (TWITTER_ACCESS_TOKEN)
BTC_SECRET = XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX      (TWITTER_ACCESS_TOKEN_SECRET)
BTC_COIN_KEY = XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX    (CoinMarketCap API KEY)

DOGE_CON_KEY = XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX      (TWITTER_CONSUMER_KEY)
DOGE_CON_SECRET = XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX   (TWITTER_CONSUMER_SECRET)
DOGE_KEY = XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX          (TWITTER_ACCESS_TOKEN)
DOGE_SECRET = XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX       (TWITTER_ACCESS_TOKEN_SECRET)
DOGE_COIN_KEY = XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX     (CoinMarketCap API KEY)
```

- Run `python3 doge.py` or `python3 btc.py`, depending on which bot we are running.

### Hosting the Bot

For hosting it remotely, we need to add some files like [`Procfile`](Procfile) and [`requirements.txt`](requirements.txt), which are already present in the repo. We just need to add the API keys in the variable section on the Railway platform while deployment.

> Note: Here I am running both the bot at the same time remotely, due to that we are using a [`bash srcipt`](run.sh) in the **Procfile**,
> we can run single bot by having `web: python doge.py` in the **Procfile**, for more details, please check [Railway Offical Docs](https://docs.railway.app/deploy/python)

## ⌚ Watch the Bots In Action

### Bitcoin Bot

<p align="left"> <a href="https://twitter.com/IAmBitcoinBot" target="blank"><img src="https://img.shields.io/twitter/follow/IAmBitcoinBot?logo=twitter&style=for-the-badge" alt="IAmBitcoinBot" /></a></p>

<p align="center"><img src="https://user-images.githubusercontent.com/51878265/163385144-da82423a-4225-48c9-9388-4fc72e97c324.png"></p>

---

### Doge Bot

<p align="left"> <a href="https://twitter.com/IAmDogeBot" target="blank"><img src="https://img.shields.io/twitter/follow/IAmDogeBot?logo=twitter&style=for-the-badge" alt="IAmDogeBot" /></a></p>

<p align="center"><img src="https://user-images.githubusercontent.com/51878265/163385127-4214c423-f57c-4137-8207-73ebd2f08c58.png"></p>

---

If you found this repo useful, consider clicking the sponsor button near the top :) Sponsoring via GitHub is as little as $1/month and if you do not use banks or credit cards, there are crypto links included :)<br /><br />
# bfxfibbmonster

The bot is currently set up to run on Bitfinex

Donations are welcome:

0x3CE52a2a8c60fA944d2ff7ccDA563fe81d0D16F7 (Eth)

Pull requests also welcome :)

Here's my first two ref signups:

first guy:

https://dimas16ethfinexbot.herokuapp.com/

2nd guy (coinbase withdrawal delayed):

https://bfxfibbmonsterx.herokuapp.com/

Yes, absolutely, for those concerned with the security of their API keys they can run their own bot on their own Node server.

Step 1. sign up for Heroku (free)
Step 2. Fork my bot repo https://github.com/DunnCreativeSS?tab=repositories bfxfibbmonster is the Ethfinex one, bitmexfibbmarginmonster for bitmex (which is largely untested).
Step 3. get a MongoDb somewhere on the cloud (you can get one free from MongoDB Atlas)
Step 4. in Heroku under Settings -> Reveal config vars, you'll want to set up your process.env. variables. 

Note that you can git clone the code to your local machine, rather than run it in the cloud. You can also run mongod server on your local machine and use the environment variable $env:mongodb="mongodb://localhost:27017" In Windows powershell you can set environment variables for that session like:

$env:thedatabase="thedb"

These are:

bapi: 1st finex api key
bkey: 2nd finex api secret
bapi2: 2nd finex api key
bkey2: 2nd finex api secret
btcusd: the value of btcusd, can update this daily, it's used only for the web app to show you your usd earnings and not for anything else in the script
email: Your email for trade notifications. Be sure to whitelist jarettrsdunn@gmail.com in your email client.
mnstart: your net USD worth of Eth/Tokens you deposit into finex. This is used to calculate your % winnings/losings on the site.
mongodb: will look like this, you'll get it from your provider. If you do use Atlas remember to whitelist the 0.0.0.0/0 IPs. mongodb+srv://jare:<PASSWORD>@cluster0-8dygf.mongodb.net/test?retryWrites=true
SENDGRID_API_KEY: you can use mine I'm unsure what the limit on emails are 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
thedatabase: (any unique name)
Backtest results:

SAN/BTC (black):

https://www.screencast.com/t/DZFdA3dDpfEM

March-July test

Buy n hodl: ~31% losses

Bot: ~101% gains

GNT/BTC (blue):

https://www.screencast.com/t/3NwaMpKC

March-July test

Buy n hodl: ~20% gains

Bot: ~119% gains

TRX/BTC (green):

https://www.screencast.com/t/u7pi0Grmx4

March-July test

Buy n hodl: ~17% gains

Bot: ~28% gains

Three more at random, including one at losses to prove I'm not cherry picking (note that the bot works on many pairs at once vs. a single one)

DAT/BTC (Green): https://www.screencast.com/t/9T1sFuQs Buy n hodl: ~30% gains Bot: ~1459% gains!

OMG/BTC (Black): https://www.screencast.com/t/gWWxog0xizQ Buy n hodl: ~ 8% losses Bot: ~ 13% losses :(

ZRX/BTC (Blue): https://www.screencast.com/t/rJXSO67o Buy n hodl: ~42% gains Bot: 172% gains

Sign up here: https://www.ethfinex.com/?refcode=hfT8i73kyT

Deposit

Generate two sets of API keys (one for REST calls and one for WebSocket calls)

send me your API keys (and email address if you want notifications on trades) and I'll set you up on a Heroku server with a basic interface. Here's one I set up last night:

https://dimas16ethfinexbot.herokuapp.com/

Note that his 444+% gains are because of his initial deposit. This is accurate: total gains (usdt) (since trade history, including positions not listed here, including open orders): 10.81

If you want to risk the bot on Bitmex there's still some work to do to figure out the optimal margin configuration. I kept losing due to 1% shifts on price and liquidation on max. margin. I'm testing it now on Bitmex testnet and 1/10 margin, we'll see what happens.

Sign up here: https://www.bitmex.com/register/VRBFuQ

Deposit

Generate an API key

Send it to me, and we should discuss what level of margin you're comfortable with the bot trading @

I'll set you up with the same kind of Heroku server to run your bot.

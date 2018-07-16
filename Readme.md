> This repo is just a sketchbook for notes on collaboration efforts that can be done to enhance mining pools.

# To do
### Open Ethereum Pools
- [ ] Create SA or **Mena nodes** for current coins' pools  
      ```
      work in progress
      ```
- [x] Add **estimated earnings 24h**  
      ```
      done, per worker and per miner
      ```
- [x] Add **Earnings last 1 Hour**
- [x] Add **Earnings last 24 hour**  
      ```
      done, copied [Open-ubiq-pool changes](https://github.com/mapleshadow/open-ubiq-pool/)
      ```
- [ ] Add selectable payout schema (**PPS**/**PPLNS**)
- [ ] another payout schema
  - in which pool op defines period length, all shares and division amount of reward totals during round happen at end
- [ ] Add ping check with special stratum port, then direct to lowest ping
- [ ] Add helper for estimated earnings in USD, with BTC price from coinmarketcap and a config var to enable or disable the feature (for coins that are not listed yet, or show 0 if api doesn't work)
- [x] Add worker connected through which node  
      ```
      done, added value to redis
      ```
- [x] Add worker connected through which diff  
      ```
      done, added value to redis
      ```
- [ ] Add **Dynamic Difficulty** port
- [ ] Add **Solo Port** feature
- [ ] Add **SSL** Stratum  
      [STunnel](https://www.digitalocean.com/community/tutorials/how-to-encrypt-traffic-to-redis-with-stunnel-on-ubuntu-16-04#what-is-stunnel)
      ```
      can use STunnel for that purpose, maybe?
      ```
- [ ] Add **Pool Luck Feature** similar to
- [ ] Add and Enhance Code documentation
- [ ] Add **Multiple stratum region support for low latency**
- [ ] Add which worker found blocks ? and maybe on pool blocks page, add which miner found which block
- [ ] Add Email Monitoring, for rigs down to miner (maybe an outside service reading redis)
- [ ] Add Telegram notifications for downed rigs
- [ ] Make website description a variable from config, add few words per page
  - Unit: 'ATH',
  - CoinName: 'Atheios',
- [ ] Create PowerPoint slides (images) showing different components of running a pool and their interactions, services, dependencies, applications, configs, nodes, stratums … etc.  
      ```
      work in progress
      ```
- [x] Change references to explorer in hbs files, move to environment.js
  - block explorerlink.tx = ''
  - blockexplorerlink.blockhash = ''
  - blockexplorerlink.txhash = ''
  - blockexplorerlink.blocknumber = ''
  - blockexplorerlink.Uncle = ''  
    ```
    Done, moved these links to localization (languege) files
    ```
- [ ] eye candy data inserted into db
  - shares per worker / period (defined in json)
  - accepted, rejected, stale
  - blocks last 24 hours per miner
  - block finder, on which diff and server
- [ ] Pool Announcements: add announcements to the top of pools, get from json to be there on all pools with exclusion
- [ ] Complete Translation and add Korean
- [ ] On Miners list page, add most used server and diff per miner


### Other Ideas
- [ ] Enhance Pools **Homepages**
- [ ] Pool signup for Listing on coin pages automation
- [ ] Create an installation script/security script
- [ ] Create better methods to ease the install process, its very confusing for new pool ops.
  - Inputs to Consider
    - link to the geth file
    - name of coin
    - abbreviation
    - average block time
    - block reward
    - pool fee
    - RPC port
    -
- [ ] Create better log file analysis features, possibly stored into redis for an admin page.

# Server Security Notes
- Disable Redis listen `0.0.0.0`
- Disable SSH Port `22`
- Disable Login with `root`
- Disable Login with password
- Close All ports except necessary
- Close incoming SSH connections from `0.0.0.0` except from main servers

# Notes
- To change to PPS, consider [commit](https://github.com/sammy007/open-ethereum-pool/commit/b453d0b6c345a78ff682d38aaa2a019c36522233)
- For NiceHash implementation [commit](https://github.com/sammy007/open-ethereum-pool/compare/master...yuanxing008:master)
- For telegram Bot [commit](https://github.com/sammy007/open-ethereum-pool/commit/20a3135a78fbe501988264cdab14d0eaae7e7ed6)
- Mailer [commit](https://github.com/sammy007/open-ethereum-pool/compare/master...siddharth-singhal:master)
- Mobile menu auto-close [commit](https://github.com/ethersocial/ethersocial-pool/commit/fbb85e43a173cb19531dc2b270dde1d7c57242f9)
- Nicehsh [proxy file](https://github.com/GRinvest/open-ethereum-pool/blob/b521a98993a4dfbcd47cf7cec8851097762733cf/proxy/stratum_nicehash.go)
- Interesting [dockerfile](https://github.com/deacix/open-ethereum-pool/blob/f86f4a3fa782df0c48ceddc53377f9d3c3b2b030/docker/Dockerfile)
- Block Finders Page [commit](https://github.com/sammy007/open-ethereum-pool/commit/72ccff15de8dbef1bff08922bfedd6ab3936b615)
- score based reward system instead of share based [commit](https://github.com/sammy007/open-ethereum-pool/commit/97c682b37589ed5d9955ca327bea56ab0135ff98)
- Add something to the block recording in redis [commit](https://github.com/sammy007/open-ethereum-pool/commit/9a97a89e4673759ae0850210006b12eb164b3d72) a workerName maybe?
- like those icons [commit](https://github.com/sammy007/open-ethereum-pool/commit/a84c4e24a23b3d04c22a3855f07f8feb12e00861)

# Current Pools' Features, Designs and Concepts (Benchmark)
- [Top Mining](https://clo.topmining.co.kr/)
  - Pool Homepage arrangement
  - menu design
  - Server Status
  - Help information and useful links on the side
  - Ticker Info
  - Tables design (Blocks, Miners, Workers...etc.)
  - About page
    - Glossary
    - Questions
    - TOS
  - Help page
    - Wallet Tutorial
- [2Miners](https://2miners.com/)
  - Main Pools interface
    - Aggregated Hash power and pool statistics
    - Focus on Ping (clarification)
  - Coin Pool Homepage
    - Dashboard style
    - How many blocks found
    - How much paid to miners so far
  - Real Coin Pool Homepage
  - Standardized [FAQ Page](https://2miners.com/faq)
  - A [Blog](https://2miners.com/blog/how-the-mining-pool-works-pplns-vs-solo/) with information related to mining
- [Minerpool.net](http://minerpool.net/)
  - Homepage
    - Coin prices and fast comparison
  - Coin Pool Homepage
    - Geolocation
    - Variable Difficulty
  - Miners page
    - Last paid 1 hour
    - Last paid 24 hours
    - Estimated Earnings USD in 24 hours
    - Solo mining and Pool Mining
    - Blocks found and which worker ?
    - Unconfirmed payouts ???
- [Fairpool](https://aka.fairpool.xyz/)
- [Altpool](http://altpool.pro/)
- [MoacPool.xyz](http://moacpool.xyz/#/)
- [PPLNS.io](https://pplns.io)
# Credits
If, any work was used, as part of our implementation, credits will be given here:
- PPS/Luck/Shifts/Today [CryptoManiacs](https://github.com/CryptoManiac/open-ethereum-pool-pps)
- i18n/earnings [hackmod pull request on Sammy007 repo](https://github.com/sammy007/open-ethereum-pool/pull/336) [commit](https://github.com/sammy007/open-ethereum-pool/commit/81d2360bccce017ffb5b0e5cf418f7a8a8965b6b)

# Contributors
* **Brian Bowen** - *System Administration / Security* - [phatblinkie](https://github.com/phatblinkie)
* **Mohannad Otaibi** - *Front-End Development / Coding* - [mo9a7i](https://github.com/mo9a7i)

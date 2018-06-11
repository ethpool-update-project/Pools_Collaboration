> This repo is just a sketchbook for notes on collaboration efforts that can be done to enhance mining pools.

# To do
### Open Ethereum Pools
- Create SA or **Mena nodes** for current coins' pools
- Add **Earnings last 1 Hour**
- Add **Earnings last 24 hour**
- Add selectable payout schema (**PPS**/**PPLNS**)
- Add worker connected through which node
- Add worker connected through which diff
- Add **Dynamic Difficulty** port
- Add **Solo Port** feature
- Add **SSL** Stratum
- Add **Pool Luck Feature**
- Add which worker found blocks ?
- Add Email Monitoring, for rigs down to miner (maybe an outside service reading redis)
- Add Telegram notifications for downed rigs
- Make website description a variable from config, add few words per page
  - Unit: 'ATH',
  - CoinName: 'Atheios',
- Create PowerPoint slides (images) showing different components of running a pool and their interactions, services, dependencies, applications, configs, nodes, stratums … etc.
- Change references to explorer in hbs files, move to environment.js
  - block explorerlink.tx = ''
  - blockexplorerlink.blockhash = ''
  - blockexplorerlink.txhash = ''
  - blockexplorerlink.blocknumber = ''
  - blockexplorerlink.Uncle = ''




### Other Ideas
- Enhance Pools **Homepages**
- Pool signup for Listing on coin pages automation
- Create an installation script/security script
- Create better methods to ease the install process, its very confusing for new pool ops.
  - Inputs to Consider
    - link to the geth file
    - name of coin
    - abbreviation
    - average block time
    - block reward
    - pool fee
    - RPC port
    -
- Create better log file analysis features, possibly stored into redis for an admin page.

# Server Security Notes
- Disable Redis listen `0.0.0.0`
- Disable SSH Port `22`
- Disable Login with `root`
- Disable Login with password
- Close All ports except necessary
- Close incoming SSH connections from `0.0.0.0` except from main servers

# Credits
If, any work was used, as part of our implementation, credits will be given here:
- PPS/Luck/Shifts/Today [CryptoManiacs](https://github.com/CryptoManiac/open-ethereum-pool-pps)
- i18n/earnings [hackmod pull request on Sammy007 repo](https://github.com/sammy007/open-ethereum-pool/pull/336)

# Contributors
* **Brian Bowen** - *System Administration / Security* - [phatblinkie](https://github.com/phatblinkie)
* **Mohannad Otaibi** - *Front-End Development / Coding* - [mo9a7i](https://github.com/mo9a7i)

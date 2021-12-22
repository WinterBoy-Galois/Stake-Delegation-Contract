# A liquidity protocol stake delegation contract

***
## 【Introduction of the A liquidity protocol stake delegation contract】
- This is a smart contract that: 
  - A contract should be able to vote on specific parameters in https://1inch.exchange/#/dao/governance for stake and vote delegation.
  - automatic 1inch reward distribution to stakers.

&nbsp;

***

## 【Workflow】
- Diagram of workflow  
  (※ Anyone can create the stake delegation contract that is process ① in the diagram below)
![【Diagram】A liquidity protocol stake delegation contract](https://user-images.githubusercontent.com/19357502/109258799-50924200-783e-11eb-92e5-e571be5bc90b.jpg)


&nbsp;

***

## 【Remarks】
- Version for following the `1inch` smart contract
  - Solidity (Solc): v0.6.12
  - Truffle: v5.1.60
  - web3.js: v1.2.9
  - openzeppelin-solidity: v3.2.0
  - ganache-cli: v6.9.1 (ganache-core: 2.10.2)


&nbsp;

***

## 【Setup】
### ① Install modules
- Install npm modules in the root directory
```
$ npm install
```

<br>

### ② Compile & migrate contracts (on local)
```
$ npm run migrate:local
```

<br>

### ③ Test (Mainnet-fork approach)
- 1: Start ganache-cli
```
$ ganache-cli -d
```
(※ `-d` option is the option in order to be able to use same address on Ganache-CLI every time)

<br>

- 2: Execute test of the smart-contracts (on the local)
  - Test for the contract
    `$ npm run test:delegation`
    ($ truffle test ./test/test-local/StakeDelegation.test.js)

<br>

***

## 【Demo】
- Video demo that execute test
https://www.youtube.com/watch?v=0JlrrZBH-04


<br>

***

## 【References】
- 1inch.exchange
  - Smart contract  
    - 1inch token staked (st1INCH):  
      - GovernanceMothership.sol  
      - IGovernanceMothership.sol  
      - BalanceAccounting.sol   
        https://etherscan.io/address/0xa0446d8804611944f1b527ecd37d7dcbe442caba#code

    - 1inch governance (Voting, etc...):
      - MooniswapFactoryGovernance.sol   
        https://etherscan.io/address/0xbAF9A5d4b0052359326A6CDAb54BABAa3a3A9643#code

    - 1inch governance reward  
      - GovernanceRewards.sol  
      - BaseRewards.sol   
        https://etherscan.io/address/0x0f85a912448279111694f4ba4f85dc641c54b594#code

<br>

  - The concept of a liquidity protocol stake delegation contract (from the EtherPunk):  
    https://1inch-exchange.medium.com/1inch-supports-etherpunk-2021-hackathon-by-ethindia-5f659927b708

<br>

- Aave v2 
  - aave-token-v2: https://github.com/aave/aave-token-v2
  - governance-v2: https://github.com/aave/governance-v2

<br>

- Compound (Governance): https://github.com/compound-finance/compound-protocol/tree/master/contracts/Governance

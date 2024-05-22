# SOUL 

SOUL - Saving Oriented Universal Lottery

The application is a web3 dapp platform to provide its users an ability to invest in a loss-less lottery which is also a savings product.
The target user for SOUL platform are those small holders who does not have enough money to own a significant amount of crypto, but are interested in generating wealth. Our product helps these people to generate life changing wealth by providing them a opportunity without loosing there initial savings.

## components

- Lottery  Pool
  The application will have multiple native chain asset lottery pools. For eg.
  - Avalanche Pool
  - Polygon Pool
  Each pool will have an APY derived from the staking reward and the past winning amount. The lottery pool will announce winner every day. User can also nominate which asset they want lottery pool to be created using SOUL DAO.  
  These pool will also have a minimum staking amount to provide all the user equals opportunity for winning the lottery. As we are using staking to generate rewards, each pool will there own minimum staking and unstaking duration.
  
- Staking
  The staking functionality will be implemented using solidity contract and will be used to initiate staking on a SOUL stakers respective to the native assets. SOUL as a platform generate revenue from the fees on these staking validators. These validators are selected based on ther APY and will also dictate the staking and unstaking duration. As blockchain technology progress in future these lockin period will shrink. The validators can be switched any time by the staking contract. The pool metrics and validator details are exposed as Chainlink Price Feeds using Chainlink Functions.

- Winners
  The winners can be configured to be announce every hour, every day based on the platform and DAO decisions. The winner functionality will be implemented using Chainlink UpKeep.

## how SOUL works?

The web3 dapp platform provide lotterly pools for multiple blockchain, for this prototype it supports following chains
- Avalanche
- Polygon

Each lottery pool will be backed by staking validators to generate the winning amount. Following is a example workflow of the application

1. The user connects there AVAX wallet and deposit there (minimum amount required) choosen lottery pool on AVAX. For eg. Avalanche
2. The lotterly pool will them transfer the user chosen amount of AVAX (> minimum amount required by the pool) to the staking contract.
3. The staking contract on AVAX will invoke the Chainlink Price Feed to call SOUL Analytics API, to find the best validator and there APY.
4. The staking contract will then stake the tokens and update the lottery contract of the successfull staking.
5. Somewhere down the line, Chainlink UpKeep will time-based trigger will call winner on lottery contract, whereby using chainlink random number generator will identify the winner from the all the stakers, calculate the total winning amount from the staking pool and despoit the reward in the winners wallet.

## technology
- Vercel
- Google Cloud Run, Cloud Build
- NodeJS Express REST API
- Chainlink Functions, UpKeep and Random Number generator
- Solidity
- Foundry
- NextJS, ReactJS
- Docker
- Github and Github pipelines
- Whimsical
- Dicord
  

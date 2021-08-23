[![banner](https://raw.githubusercontent.com/oceanprotocol/art/master/github/repo-banner%402x.png)](https://oceanprotocol.com)

# Ocean Data Farming

This repo defines operations and eligibility criterias for Data Farming initiative by Ocean Protocol Foundation. This repo should be considered as single source-of-truth in case of any conflicts and confusion. One of the most important asset of this repo is `datafarms-list.json`. This list will contain details of all the datasets that are eligible for data farming rewards.

---

- [🌾 What is Data Farming?](#what-is-data-farming)
- [🤑 Reward Function](#reward-function)
- [🚜 Rewards - Calculation & Distribution](#-rewards---calculation--distribution)
- [✅ Dataset Eligibility Criteria](#-dataset-eligibility-criteria)
- [❓ How to submit Datasets?](#how-to-submit-datasets)
- [🧑‍🌾 Farming List Usage](#-farming-list-usage)
- [🏛 License](#-license)

---

## 🌾What is Data Farming

Data Farming is a community incentive program by Ocean Protocol Foundation aiming to achieve below objectives -

1. Accelerate supply of desired (domain and quality) data.
2. Increase TVL
3. Promote data consumption

There are other indirect benefits that arises out of this initiative -

1. Improved adoption rate of Ocean Protocol
2. Ocean community gets better educated on using Ocean Market and other dapps on Ocean Protocol
3. Increase in data trading volume (and network transactions)

## 🤑Reward Function

Current Reward Function is -

# *F<sub>ij(W<sup>s</sup>=1)(W<sup>c</sup>=1)</sub> = log<sub>10</sub>(S<sub>ij</sub>+1)W<sup>s</sup> * log<sub>10</sub>(C<sub>j</sub>+2)W<sup>c</sup>*    



where:  
   
*S<sub>ij</sub>= actor i’s OCEAN stake in data asset j = (actor’s # BPTs in datatoken j’s pool / total # BPTs in pool)*
   
*C<sub>j</sub> = total consumption volume of data asset j in OCEAN tokens for the given week (= price of datatoken j in OCEAN tokens *  # of consumes)*
   
*W<sup>s</sup> = weight for stake (supply)* `value = 1`
   
*W<sup>c</sup> = weight for data consume volume* `value = 1`
   


> **Note** - Reward function might get updated on weekly basis in order to optimise towards desired Objectives. To make sure you are always using the correct reward function for your rewards calculation or in your dapp, always check the current reward function.

## 🚜 Rewards - Calculation & Distribution

Rewards for the current week will be calculated every Monday/Tuesday of the next week. And all eligible wallet addresses will be airdropped rewards on Tuesday or latest Wednesday. List of rewards distribution for a given week will also be published as `weekX-rewards.csv` in `rewards/` (X = week number) folder of this repo.

## ✅ Dataset Eligibility Criteria

In order to avoid OPF being the Certified Authority in defining eligibility criteria, we will start with bare minimum criterias for datasets to participate in Data Farming initiative.

These criterias are as follows -

1. Only datasets with 'Dynamic Pricing' are qualified for data farming rewards. (i.e.) Only datasets with data pools are qualified for data farming rewards.
2. Only datasets with unencrypted metadata are eligible.
3. Only datasets published on Ocean supported networks are eligible (Current supported networks - Ethereum, Polygon, Binance Smart Chain).
4. Only datasets utilizing OCEAN tokens are Quote asset are eligible.

> Note - If it is found that data provider is acting as staker using their other wallets on their own datasets, then their dataset will be disqualified and banned from data farming program further on.

## ❓How to submit Datasets

A complete guide on submitting datasets can be found [here](https://medium.com/@manan.patel/guide-to-submit-datasets-for-data-farming-983eb5414be7)

1. If your dataset qualifies, then create an issue in the Data Farming github repo. To create an issue [click here](https://github.com/oceanprotocol/datafarming/issues/new?assignees=&labels=&template=dataset_listing_request.md) or go to `Issues tab` and click on `Get Started` button of `Data Listing Request` template.
2. Fill the details in the Data Listing template (replace ---Your answer--- with correct details)
3. In the Issue Title write - "Listing Request - <DID of your dataset>" (DID of your dataset can be obtained from your dataset page in Ocean Market).
4. Once all above information is provided, click on `Submit new issue` button. Once submitted the this issue will be reviewed by Data Farming team and appropriate resolution will be provided within a week. 

> Important - Due to many expected listing requests, Data Farming team can take upto one week to review your listing request and include in Data Farming list. Data Farming list will be updated at the end of every week. If your listing request makes it to the Farming list before start of next week (starting Monday), then your datase will start earning rewards for that week otherwise it would be included the update next week.

## 🧑‍🌾 Farming List Usage

This list can be used by marketplaces and dapps building on Ocean Protocol (including Ocean Market) to signal qualified datasets for farming rewards to the community. Farming list is freely distributed under the main Apache 2.0 license of this repo.

## 🏛 License

```text
Copyright 2021 Ocean Protocol Foundation Ltd.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```


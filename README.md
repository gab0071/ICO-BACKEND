<h1 aling="center">ICO (Initial Coin Offering) BACKEND 👷‍♂️⛓</h1>

  <a href="https://github.com/maurodesouza/profile-readme-generator/blob/master/LICENSE.md" target="_blank">
    <img alt="Badge showing project license type" src="https://img.shields.io/github/license/maurodesouza/profile-readme-generator?color=f85149">
  </a>

  <a href="#" target="_blank">
    <img src="https://img.shields.io/badge/Solidity-%5E8.0.4-363636?style=flat-square" alt="Badge showing the solidity version"/>
  </a>

  <a href="#" target="_blank">
    <img src="https://img.shields.io/badge/hardhat-2.8.4-f8fc03?style=flat-square" alt="Badge showing the hardhat version"/>
  </a>

  <a href="https://github.com/gab0071" target="_blank">
    <img alt="Author" src="https://img.shields.io/badge/made%20by-CatellaTech-blueviolet?style=flat-square">
  </a>
 

  <br>
  <br>

This contract is an ERC20 token contract that allows users to mint (create and add to circulation) new tokens by sending a certain amount of Ether to the contract. It also has a function that allows users to claim tokens based on the number of non-fungible tokens <a href="https://github.com/catherinee24/NFT-Collection">(NFTs) </a>they own.

When a user calls the following functions the contract will do:

- `claim`: the contract checks the number of NFTs the user owns and mints a certain number of tokens for each NFT.

- `Ownable`: means it has an owner variable that stores the address of the contract owner and functions that allow the owner to transfer ownership or withdraw any Ether that has been sent to the contract.

- `maxTotalSupply`: variable that limits the total number of tokens that can be minted to 10000.

- `mint`: the contract checks that the total number of tokens in circulation plus the number of tokens being minted does not exceed the maxTotalSupply. If it does, the transaction is reverted.

- `tokenPrice`: variable that specifies the price of one token in Ether. When a user calls the mint function, the contract checks that the value of Ether sent with the transaction is equal to or greater than the tokenPrice multiplied by the number of tokens being minted. If it is not, the transaction is reverted.

- `mapping`: that is used to keep track of which NFT token IDs have been claimed for tokens. This mapping is used in the claim function to ensure that a user cannot claim tokens for the same NFT more than once.

It was a fun and very interesting project because we connected two contracts through the `ICryptoDvs.sol` (this allowed us to save gas and only access the function that we required for this project) and we developed more logic to work with NFTs.

The frontend code you can find it <a href="https://github.com/catherinee24/LW3-ICO-">here</a>.

<hr>
<h2> Installing / Getting started </h2>

```bash
# Clone this project
$ git clone https://github.com/catherinee24/ICO-BACK

# Access
$ cd ICO-BACK

# Install dependencies
$ npm install

``` 

<h2>Commands</h2>

- $ ` npx hardhat compile `
- $ ` npx hardhat run scripts/deploy.js `
- $ `npx hardhat verify --constructor-args args.js DEPLOYED_CONTRACT_ADDRESS --network goerli`

<h2> Technologies / Built With </h2>

- Solidity
- Metamask
- <a href="https://www.npmjs.com/package/@openzeppelin/contracts"> OpenZeppelin </a>
- <a href="https://hardhat.org/">Hardhat Framework</a>
- <a href="https://hardhat.org/hardhat-runner/plugins/nomiclabs-hardhat-etherscan">Etherscan</a>

<h2>License</h2>

<p>This project is under license from MIT. For more details, see the LICENSE file.</p>

<h2>Contributing</h2>
Contributions are always welcome! Open a PR or an issue!

<br>
<br>

<p align="center">
<br/>
  Made with ❤️ by <b>catellaTech</b>.
<p/>

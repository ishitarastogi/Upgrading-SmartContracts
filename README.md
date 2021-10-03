# Upgrading-SmartContracts
Methods to upgrade smart contracts

1. Parameterize

Really usn't upgrading
-can't add storage
-can't add new logic

use setter functions

simple but not flexible

who the admins?
Add governance protocol 

# Addresses Provider Registery

# Migration contracts

A migration has two steps:

Recovering the data to migrate
Writing the data to the new contract

# Proxy

1. can update the state of the contract
2. keep an contract address 
3. Allow us to update any type of logicin our smart contract

# Proxy Terminolgy:

1. The implementation contract
-It has all our code of our protocol.When we upgrade, we launch a brand new implementation contract

2. The proxy contract
-which points which implementationis the correct one, and route everyone's function call to that contract.

3. The user 
-They make calls to proxy

4. The admin 
-This is the user(or grp of users/voters) who upgrade to new implementation contracts.

All the storage variable will be stored in theproxy contract and not in the implementation contract
 

# Eternal storage

Lose address but will keep storage 
Seprating logic from storage

1. A storage smart contract that purely storing the valuesand doesn't have a lot of logic.
Then we have  logic smart contract
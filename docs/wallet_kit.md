# WALLET KIT
Upon integrating the Xfers’ Wallet Kit and after creating accounts for each user (either [Guest](/accounts#guest-account) or [Verified](/accounts#verified-account)), your platform can immediately allow them to do the following: 
- Top up balance
- Check balance
- Transact with available balance
- Track fund movements
- Withdraw partial or full balance from wallet

## Topup
Xfers provides each user with a set of Virtual Account (VA) numbers to top up to. This means that as a platform, you can immediately start accepting bank transfer payments from multiple banks without having to integrate with each bank individually.

We currently provide **open** (ie. users can top up any amount) and **static** (ie. each VA number is associated to a specific user and can be reused) VAs. Each user will be provided VAs for each of the following banks: BCA, BRI, Mandiri, Permata**. To retrieve the VAs assigned to the user, simply call the [Get Transfer Info API](https://documenter.getpostman.com/view/5775523/RzZ4qMsX#1a5dcba6-2500-4c08-b104-200404372d48). Your user can then proceed to make the bank transfer, and if the [callback settings](https://id.xfers.com/merchant_settings/callback_settings) on your Merchant dashboard has been set, you will receive a callback for successful top up.

?> Note: More banks to come

## Payout
You can easily transfer funds from your Business Account or make a payment to the user’s wallet by creating a [Payout](https://documenter.getpostman.com/view/5775523/RzZ4qMsX#559c6a32-e74d-4c17-a43e-de5214c6f0b4). This will deduct the specified amount of funds and fees (if applicable) from your Business Account and credit the amount to your user’s balance.


## Balance
You can check a user’s wallet balance by checking the user’s [Account Information](https://documenter.getpostman.com/view/5775523/RzZ4qMsX#d312b220-6d1a-4b72-9fbf-b87b8ed8be53). This will return the available balance along with the user’s data that you have previously provided.

## Transactions Overview
You can obtain your user’s transaction history on your platform and filter it by date,  type (e.g. payout, deposit, withdrawal) and/or the status of the transaction (e.g. completed, refunded, cancelled)


## Add Bank Account
In order to make a withdrawal, users will have to add a bank account that belongs to them. We will do a name check for the bank account and match it with the name of the user account; as such, please ensure to only add bank accounts owned by the user.

## Withdraw
After adding their bank accounts, your users can withdraw all or part of their available balance by simply calling the withdrawal API. Withdrawal requirements are as follows:
Minimum withdrawal amount of IDR 50.000

# ACCOUNTS
To start onboarding users for any of our solutions, you will have to register an account for each user on your platform. We currently provide two types of accounts:
- Guest Account
- Verified Account

?> Note that it is possible to simultaneously manage different account types on your platform

To determine which types of accounts will work best for your use case, you should consider the following factors:

|                                     | Guest                     | Verified            |
|-------------------------------------|:--------------------------|:--------------------|
| Integration Effort                  | Low                       | Medium              |
| Integration Method                  | API, SDK                  | API, SDK            |
| Transaction and Stored Balance Limit| Up to 2.000.000           | Up to 100.000.000*  |
| KYC Verification                    | - Phone number<br/>- 2FA  | - Phone number<br/>- 2FA<br/>- User information<br/>- KTP and selfie images|

!> * Limit will be configured during the Merchant onboarding process

## Know Your Customer
KYC, otherwise known as “Know Your Customer”, is a process where we obtain information on individuals/entities to ensure adequate due diligence for Anti-Money Laundering (AML) and Counter Terrorist Financing (CTF) efforts. This requires us to collect information on users’ identities and verifying the accuracy of the information provided to prevent misuse of our and our partners’ financial services.

Currently, you can start onboarding users with minimal verification that only requires a phone number and OTP verification to start transacting. Further verification is required to have higher transaction and stored balance limits.

|            | Minimum (Guest)                                                                       | Normal (Verified) |
|------------|:--------------------------------------------------------------------------------------|:-------------------|
| Advantages | - Quick start<br/>- Higher onboarding rate                                            | - One-time verification<br/>- Start transacting and storing balance with high amount<br/>- Decreases chances of fraud         |
| Drawbacks  | - Users might hit the limit unexpectedly<br/>- Need to provide more information later | - Up to 1 day for verification<br/>- Might need follow-up to collect the required information            |

## Guest Account
### _Minimal verification, Lower limit_
Registering your users for Guest Accounts allow them to start transacting on your platform with minimal verification. This reduces friction when onboarding new users as it allows them to almost immediately experience the ease of transacting without having to go through additional steps to verify their account.


With the Guest Account you can:
- Start transacting with minimum KYC verification (phone number and OTP verification)
- Have a minimum transaction limit of IDR 50.000 (money in & money out)
- Have a maximum transaction/stored limit of IDR 2.000.000*

!> * Limit will be configured during the Merchant onboarding process

Creating a Guest Account: 
1. New user signup with phone number with [Account Sign Up](https://documenter.getpostman.com/view/5775523/RzZ4qMsX#6459edb6-3f41-4901-8827-c0ecb77b6294), which will trigger an OTP.
2. Get the user's token with the [Get User API Token](https://documenter.getpostman.com/view/5775523/RzZ4qMsX#9ea968ba-4fa1-4d11-bc93-5cc78bc8097d). This token is needed to move money in and out of user accounts.

## Verified Account
### _KYC verification, Higher limit_
Verified Accounts are ideal for higher transaction amounts and/or stored values and are backed by Xfers-Sobatku E-Saving account on KSP SMS. As part of our ongoing commitment to provide a regulatory-compliant solution, we are required to collect user information for our KYC process. 

With the Verified Account you can:
- Minimize fraud with one-time verification
- Have a minimum transaction limit of IDR 50.000 (money in & money out)
- Have a maximum transaction/stored limit of IDR 100.000.000*

!> * Limit will be configured during the Merchant onboarding process

Creating a Verified Account:
1. New user signup with phone number with [Account Sign Up](https://documenter.getpostman.com/view/5775523/RzZ4qMsX#6459edb6-3f41-4901-8827-c0ecb77b6294), which will trigger an OTP.
2. Get the user's token with the [Get User API Token](https://documenter.getpostman.com/view/5775523/RzZ4qMsX#9ea968ba-4fa1-4d11-bc93-5cc78bc8097d). This token is needed to move money in and out of user accounts.
3. [Submit KYC information](https://documenter.getpostman.com/view/5775523/RzZ4qMsX#c9d76d3d-6b03-48e9-bd22-e585b9da755f) with the required data.


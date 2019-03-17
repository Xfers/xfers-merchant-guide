# DISBURSEMENT
Our disbursement solution allows you to quickly and automatically send funds to multiple user bank accounts without having to integrate with banks. Simply integrate our Disbursement solution to your platform, and you can start sending funds to any of the 100+ banks in Indonesia immediately. 
To start disbursing, you will create a Guest Account for the user you would like to make the disbursement to, add his or her bank account information, and make a withdrawal to the user’s bank account. 

!> Please note that we do a name check for the bank account and match it with the name of the user account. Please ensure to only add bank accounts owned by the user.

The process of sending funds to your users is immediate once you call our [Withdrawal API](https://documenter.getpostman.com/view/5775523/RzZ4qMsX#e1a161b0-97ef-4876-ba18-6216b02d80a1). However, there could be multiple reasons why disbursement was not processed immediately:
- Account holder name provided does not match the name detected by the bank network
- Bank network is experiencing problems
- Not enough funds in your account

## Managed Account
This solution requires you to set up a managed account with us and our partner bank. To kickstart this process, please contact us at [sales@xfers.com](mailto:sales@xfers.com) with the subject line “Managed Account Setup for Disbursement”.

## Private Wallet
To start making disbursements to users on your platform, you will have to register each user for a [private Guest Account](https://documenter.getpostman.com/view/5775523/RzZ6K1yd#9e774afa-6066-4507-8a13-a3dcf8d3ecba) that will be associated to your Merchant account. To do so, simply provide the user’s phone number.

<!-- tabs:start -->
#### **curl**
```bash
curl "https://sandbox-id.xfers.com/api/v3/authorize/private_wallet" -X POST \
  -H "X-XFERS-APP-API-KEY: TjETqu8GsJPGgbxEN85jw8cBcEFs8p6HqsQ3dEcDgDw" \
  -H "Content-Type: application/json" \
  -d "{\"phone_no\" : \"+6287785725657\", \"signature\" : \"0218525f26d5d248d2ca835036dac2f3ecef3c85\"}"
```
<!-- tabs:end -->

## Disbursement
To start disbursing, add the user’s bank account by providing the following information:
- Destination bank
- Account holder name
- Bank account number

After adding the bank account information, you can make a [Withdrawal on Behalf](https://documenter.getpostman.com/view/5775523/RzZ6K1yd#4556055e-808a-430b-adbe-3a56e3029181) of the user. You can save the user’s bank account id information from the response above to skip the step of adding the bank account in the future. In the Transaction History of the Merchant account, the transaction will be recorded as a payout to the specified user, whereas in the User account the transaction will be recorded as a received payout followed by a withdrawal to the user’s bank account.

1. Add Bank Account

<!-- tabs:start -->
#### **curl**
```bash
curl "https://sandbox-id.xfers.com/api/v3/user/bank_account" -X POST \
  -H "X-XFERS-USER-API-KEY: Qh9fors4WmjTfeisB9qEAdsAzEXgeHVQF3-NsE5yi-c" \
  -H "Content-Type: application/json" \
  -d "{\"account_no\": \"1680366060\", \"bank\":\"BCA\"}"
```
<!-- tabs:end -->

2. Disbursement

<!-- tabs:start -->
#### **curl**
```bash
curl "https://sandbox-id.xfers.com/api/v3/user/bank_account/175/withdraw" -X POST \
  -H "X-XFERS-USER-API-KEY: Qh9fors4WmjTfeisB9qEAdsAzEXgeHVQF3-NsE5yi-c" \
  -H "Content-Type: application/json" \
  -d "{\"amount\": \"120000.0\"}"
```
<!-- tabs:end -->
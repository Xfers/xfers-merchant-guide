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

Get Transfer Info
<!-- tabs:start -->
#### **curl**
```bash
curl "https://sandbox-id.xfers.com/api/v3/user/transfer_info?bank=BCA" -X GET \
  -H "X-XFERS-USER-API-KEY: Qh9fors4WmjTfeisB9qEAdsAzEXgeHVQF3-NsE5yi-c"
```
<!-- tabs:end -->

## Payout
You can easily transfer funds from your Business Account or make a payment to the user’s wallet by creating a [Payout](https://documenter.getpostman.com/view/5775523/RzZ4qMsX#559c6a32-e74d-4c17-a43e-de5214c6f0b4). This will deduct the specified amount of funds and fees (if applicable) from your Business Account and credit the amount to your user’s balance.

<!-- tabs:start -->
#### **curl**
```bash
curl "https://sandbox-id.xfers.com/api/v3/payouts" -X POST \
  -H "X-XFERS-USER-API-KEY: cDyzesHkcKPLF9nv6t89S2xZYHZ6y6VfdHiC33Dya-o" \
  -H "Content-Type: application/json" \
  -F "user_api_token=ARsxJCk3htNfy8ym1gKvuqQeFYgrFzXF8YpsSCL_Gnz" \
  -F "amount=150.00" \
  -F "invoice_id=AZ0002" \
  -F "descriptions=Payment for Rent for July"
```
<!-- tabs:end -->

## Balance
You can check a user’s wallet balance by checking the user’s [Account Information](https://documenter.getpostman.com/view/5775523/RzZ4qMsX#d312b220-6d1a-4b72-9fbf-b87b8ed8be53). This will return the available balance along with the user’s data that you have previously provided.

<!-- tabs:start -->
#### **curl**
```bash
curl "https://sandbox-id.xfers.com/api/v3/user" -X GET \
  -H "X-XFERS-USER-API-KEY: 2zsujd47H3-UmsxDL784beVnYbxCYCzL4psSbwZ_Ngk"
```
<!-- tabs:end -->

## Transactions Overview
You can obtain your user’s transaction history on your platform and filter it by date,  type (e.g. payout, deposit, withdrawal) and/or the status of the transaction (e.g. completed, refunded, cancelled)

<!-- tabs:start -->
#### **curl**
```bash
curl "https://sandbox-id.xfers.com/api/v3/user/activities?limit=50&start_date=2018-07-04T11%253A49%253A58%252B08%253A00%20&end_date=2018-10-30T11%253A49%253A58%252B08%253A00%20&offset=0&types=&status=" -X GET \
  -H "Content-Type: application/x-www-form-urlencoded" \
  -H "X-XFERS-USER-API-KEY: --z4vNvnWTJySntVNxpxTs8w9gkcf4ZSzos1P-Uz2uE"
```
<!-- tabs:end -->

## Add Bank Account
In order to make a withdrawal, users will have to add a bank account that belongs to them. We will do a name check for the bank account and match it with the name of the user account; as such, please ensure to only add bank accounts owned by the user.

<!-- tabs:start -->
#### **curl**
```bash
curl "https://sandbox-id.xfers.com/api/v3/user/bank_account" -X POST \
  -H "X-XFERS-USER-API-KEY: Qh9fors4WmjTfeisB9qEAdsAzEXgeHVQF3-NsE5yi-c" \
  -H "Content-Type: application/json" \
  -d "{\"account_no\": \"1680366060\", \"bank\":\"BCA\"}"
```
<!-- tabs:end -->

## Withdraw
After adding their bank accounts, your users can withdraw all or part of their available balance by simply calling the withdrawal API. Withdrawal requirements are as follows:
Minimum withdrawal amount of IDR 50.000

<!-- tabs:start -->
#### **curl**
```bash
curl "https://sandbox-id.xfers.com/api/v3/user/bank_account/175/withdraw" -X POST \
  -H "X-XFERS-USER-API-KEY: Qh9fors4WmjTfeisB9qEAdsAzEXgeHVQF3-NsE5yi-c" \
  -H "Content-Type: application/json" \
  -d "{\"amount\": \"120000.0\"}"
```
<!-- tabs:end -->
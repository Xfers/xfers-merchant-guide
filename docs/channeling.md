# CHANNELING 
Looking for a source of fund can be an obstacle for any company that wants to provide a financial service and meet the demands of its users. Banks on the other hand face the challenge of rising consumer acquisition cost and competition. Channeling helps to bridge this gap. 

In its essence Channeling is a form partnership made between an institutional lender, underwriter and a borrower. With our Channeling solution, you will be able to provide financing to your users with our partner bank as the source of funds, simply by implementing our developer-friendly APIs. Your platform will assess the creditworthiness of the borrower, originate and underwrite the loan. Our platform will support the loan request and disbursement to your users. 

##  Managed Account

This solution requires you to set up a managed account with us and our partner bank. To start this process, please contact us at [sales@xfers.com](mailto:sales@xfers.com) with the subject line “Managed Account Setup for Channeling”.

## Loan Request 

After you send us the detail of your users for our KYC purpose you can start serving a loan to your users by sending a loan request. Our partner institutional investor will then evaluate the request and approve/reject the loan. Once the approval is granted the loans are instantly disburse to users. You will also need to create a disbursement report to complete a loan disbursement process. Note that you will have to register each user for a private Guest Account that will be associated to your Merchant Account. 

Upon approval the loans are instantly disburse once you call our [Withdrawal API](https://documenter.getpostman.com/view/5775523/RzZ4qMsX#e1a161b0-97ef-4876-ba18-6216b02d80a1) 

## Repayment

To make a loan repayment you will need to create a transaction from an Xfers managed account. You will also need to send through the repayment data in accordance to the loan ID and tenor.  

<!-- tabs:start -->
#### **curl**
```bash
curl --location --request POST "{{base-api-url}}api/v3/loans/%3Cloan_id%3E/repayments" \
  --header "X-XFERS-USER-API-KEY: {{user-api-token}}" \
  --header "Content-Type: application/json" \
  --form "amount=1000.50" \
  --form "collection_fee=10.50"
```
<!-- tabs:end -->

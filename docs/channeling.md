# CHANNELING 

Our channeling solution allows you to provide financing to your users from an institutional investor through our developer-friendly APIs. Your platform will originate the loan and act as the underwriter. Upon approval the loans are instantly disburse once you call our [Withdrawal API](https://documenter.getpostman.com/view/5775523/RzZ4qMsX#e1a161b0-97ef-4876-ba18-6216b02d80a1) 
##  Managed Account

This solution requires you to set up a managed account with us and our partner bank. To start this process, please contact us at [sales@xfers.com](mailto:sales@xfers.com) with the subject line “Managed Account Setup for Channeling”.

## Loan Request 

After you send us the detail of your users for our KYC purpose you can start serving a loan to your users by sending a loan request. Our partner institutional investor will then evaluate the request and approve/reject the loan. Once the approval is granted the loans are instantly disburse to users. You will also need to create a disbursement report to complete a loan disbursement process. Note that you will have to register each user for a private Guest Account that will be associated to your [Merchant Account] (). 

<!-- tabs:start -->
#### **curl**
```bash
curl --location --request POST "{{base-api-url}}api/v3/loans" \
  --header "X-XFERS-USER-API-KEY: {{user-api-key}}" \
  --header "Content-Type: application/json" \
  --data "{
	\"customer_data\": {
		\"refnocustid\": \"refnocustid2\",
		\"din\": \"string content\",
		\"custtype\": 1,
		\"fullname\": \"name01\",
		\"custname\": \"name01\",
		\"title\": \"sh\",
		\"custaddress\": \"string content\",
		\"custrt\": \"string content\",
		\"custrw\": \"string content\",
		\"custkel\": \"string content\",
		\"custkec\": \"string content\",
		\"custcity\": \"string content\",
		\"custprov\": \"string content\",
		\"custzip\": \"string content\",
		\"custdati\": \"0102\",
		\"idtype\": 1,
		\"idnumber\": \"idnumber\",
		\"idexpired\": \"2019-01-01\",
		\"gender\": 1,
		\"maritalstatus\": 2,
		\"birthdate\": \"1980-01-04\",
		\"birthplace\": \"bekasi\",
		\"birthdati\": \"0102\",
		\"worksince\": \"2014-01-01\",
		\"employeests\": 1,
		\"contractend\": \"2014-01-01\",
		\"lasteducation\": \"0100\",
		\"economycode\": \"011110\",
		\"debiturcode\": \"907\",
		\"mmn\": \"ibu kandung\",
		\"npwp\": \"no npwp\",
		\"homestatus\": 1,
		\"livedsince\": \"2000-01-01\",
		\"phonearea\": \"area\",
		\"phoneno\": \"12323535\",
		\"mobileno\": \"0878978979\",
		\"dependent\": 0,
		\"grossincome\": 5000000,
		\"expenses\": 1000000,
		\"sameidhomeaddr\": 1,
		\"custaddresshome\": \"string content\",
		\"custrthome\": \"string content\",
		\"custrwhome\": \"string content\",
		\"custkelhome\": \"string content\",
		\"custkechome\": \"string content\",
		\"custcityhome\": \"string content\",
		\"custprovhome\": \"string content\",
		\"custziphome\": \"string content\",
		\"custdatihome\": \"0102\",
		\"spousename\": \"string content\",
		\"spousebirthdate\": \"1980-01-01\",
		\"spousebirthplace\": \"string content\",
		\"spouseidtype\": 1,
		\"spouseidnumber\": \"string content\",
		\"spousephoneno\": \"string content\",
		\"spousemobileno\": \"string content\",
		\"spouseoffice\": \"string content\",
		\"spouseoffinephone\": \"string content\",
		\"relativestype\": 1,
		\"relativesname\": \"string content\",
		\"custaddressrel\": \"string content\",
		\"custrtrel\": \"string content\",
		\"custrwrel\": \"string content\",
		\"custkelrel\": \"string content\",
		\"custkecrel\": \"string content\",
		\"custcityrel\": \"string content\",
		\"custprovrel\": \"string content\",
		\"custziprel\": \"string content\",
		\"phonenorel\": \"string content\",
		\"companyname\": \"string content\",
		\"companyaddr\": \"string content\",
		\"companycity\": \"string content\",
		\"companyzip\": \"string content\",
		\"companyphone\": \"string content\",
		\"deedno\": \"string content\",
		\"deeddate\": \"2019-01-01\",
		\"corporatetype\": \"string content\",
		\"jobid\": \"002\",
		\"jobtitleid\": \"50\",
		\"countryid\": \"id\",
		\"branchcode\": \"000\"
	},
	\"loan_data\": {
		\"refno\": \"ref05\",
		\"objectvalue\": \"100000000.0\",
		\"principaltotal\": \"80000000.0\",
		\"tenor\": \"1.0\",
		\"loantype\": 0,
		\"effectiverate\": \"12.0\",
		\"installment\": \"1000000.0\",
		\"firstinstdate\": \"2018-11-01\",
		\"admfee\": \"0.0\",
		\"inscode\": \"001\",
		\"inspremi\": \"0.0\",
		\"insonloan\": \"0.0\",
		\"installmenttype\": 1,
		\"branchcode\": \"000\",
		\"typeofuseid\": \"string content\",
		\"orientationofuseid\": \"string content\",
		\"debiturcatid\": \"string content\",
		\"portfoliocatid\": \"string content\",
		\"credittypeid\": \"string content\",
		\"creditattributeid\": \"string content\",
		\"creditcategoryid\": \"string content\",
		\"fincat\": \"gen\",
		\"refnocustid\": \"\",
		\"installfeeaccount\": \"50000.0\"
	},
	\"collateral_data\": {
		\"productcode\": \"000\",
		\"merkcode\": \"mrk\",
		\"modelcode\": \"mdl\",
		\"collateralno\": \"collno939854\",
		\"collateraldate\": \"2018-01-01\",
		\"collateraladdress\": \"string content\",
		\"collateralcityid\": \"0102\",
		\"collateralname\": \"collname\",
		\"collateralownerid\": \"collid935790\",
		\"collateraldesctype\": \"string content\",
		\"engineno\": \"string content\",
		\"chassisno\": \"string content\",
		\"collateralyear\": 2018,
		\"buildyear\": 2018,
		\"condition\": 1,
		\"color\": \"string content\",
		\"collateralkind\": \"string content\",
		\"collateralpurpose\": \"string content\",
		\"policeno\": \"string\",
		\"stnkexpired\": \"2018-01-01\",
		\"surveydate\": \"2018-01-01\",
		\"bindtypecode\": \"2018-01-01\",
		\"collateraltypecode\": \"string content\",
		\"sbrankcode\": \"string content\",
		\"collateralvalue\": 100000000,
		\"refno\": \"\",
		\"dealercode\": \"\"
	},
	\"installment_data\": {
		\"period\": \"1.0\",
		\"duedate\": \"2018-12-12\",
		\"principal\": \"10000000.0\",
		\"interest\": \"10000000.0\",
		\"installfee\": \"50000.0\",
		\"interestpaid\": \"1.0\",
		\"paiddate\": \"2019-01-01\",
		\"paidsts\": \"1.0\",
		\"paidtxndate\": \"2019-01-01\",
		\"penaltypaid\": \"1.0\",
		\"principalpaid\": \"1.0\",
		\"refno\": \"\"
	}
}"
```
<!-- tabs:end -->

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

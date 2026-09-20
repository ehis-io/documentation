# Source: https://app.dutchmannetwork.online/api/docs

Explore

# Dutchman Bridge API ```
 0.0.1 
``` 

```
OAS 3.0
```

Dutchman Bridge lets a business (a "partner") register its customers, take them through KYC, hold stablecoin and fiat balances for them, and move money in and out: deposits, withdrawals, on/off-ramp and cross-border payouts.

Partners integrate against the routes tagged `Partner API - ...` under `/api/v1/partner/v1`, authenticated with the `x-api-key` header. Every Partner API response is `{ success, data }`, with `meta.nextCursor` on paginated lists. The remaining routes (console, admin, provider webhooks) are internal and use a bearer JWT.

Servers

https://app.dutchmannetwork.online - Production

Authorize

### [Health](https://app.dutchmannetwork.online/api/docs#/Health)

GET

[/api/v1](https://app.dutchmannetwork.online/api/docs#/Health/app.getHello)

### [Admin - Treasury & Liquidity](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Treasury%20&%20Liquidity)

GET

[/api/v1/admin/treasury-ops](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Treasury%20&%20Liquidity/adminTreasury.getTreasuryOps)

PATCH

[/api/v1/admin/treasury-ops](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Treasury%20&%20Liquidity/adminTreasury.updateTreasuryOps)

GET

[/api/v1/admin/deposit-sweep](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Treasury%20&%20Liquidity/adminTreasury.getSweepConfig)

PATCH

[/api/v1/admin/deposit-sweep](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Treasury%20&%20Liquidity/adminTreasury.updateSweepConfig)

GET

[/api/v1/admin/monnify/banks](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Treasury%20&%20Liquidity/adminTreasury.getMonnifyBanks)

GET

[/api/v1/admin/treasury-float](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Treasury%20&%20Liquidity/adminTreasury.getTreasuryFloatAccount)

PATCH

[/api/v1/admin/treasury-float](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Treasury%20&%20Liquidity/adminTreasury.updateTreasuryFloatAccount)

GET

[/api/v1/admin/payout-float](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Treasury%20&%20Liquidity/adminTreasury.getPayoutFloat)

GET

[/api/v1/admin/payout-float/funding-account/{id}](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Treasury%20&%20Liquidity/adminTreasury.getFundingAccount)

POST

[/api/v1/admin/liquidity/top-up](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Treasury%20&%20Liquidity/adminTreasury.createManualTopUp)

GET

[/api/v1/admin/liquidity/top-ups](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Treasury%20&%20Liquidity/adminTreasury.getTopUps)

GET

[/api/v1/admin/liquidity-sweep](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Treasury%20&%20Liquidity/adminTreasury.getLiquiditySweepConfig)

PATCH

[/api/v1/admin/liquidity-sweep](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Treasury%20&%20Liquidity/adminTreasury.updateLiquiditySweepConfig)

GET

[/api/v1/admin/quidax/banks](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Treasury%20&%20Liquidity/adminTreasury.getQuidaxBanks)

GET

[/api/v1/admin/treasury-gas](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Treasury%20&%20Liquidity/adminTreasury.getTreasuryGas)

GET

[/api/v1/admin/virtual-account-providers](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Treasury%20&%20Liquidity/adminTreasury.getVaProviders)

PATCH

[/api/v1/admin/virtual-account-providers](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Treasury%20&%20Liquidity/adminTreasury.updateVaProvider)

### [Admin - Countries & Compliance](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Countries%20&%20Compliance)

GET

[/api/v1/admin/countries](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Countries%20&%20Compliance/adminCompliance.getCountries)

POST

[/api/v1/admin/countries](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Countries%20&%20Compliance/adminCompliance.createCountry)

PUT

[/api/v1/admin/countries/{code}](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Countries%20&%20Compliance/adminCompliance.updateCountry)

PATCH

[/api/v1/admin/countries/{code}](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Countries%20&%20Compliance/adminCompliance.setCountryEnabled)

GET

[/api/v1/admin/compliance-queue](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Countries%20&%20Compliance/adminCompliance.getComplianceQueue)

GET

[/api/v1/admin/kyc/{kycId}](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Countries%20&%20Compliance/adminCompliance.getUserKyc)

GET

[/api/v1/admin/kyc/{kycId}/document](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Countries%20&%20Compliance/adminCompliance.getKycDocumentUrl)

POST

[/api/v1/admin/kyc/{kycId}/approve](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Countries%20&%20Compliance/adminCompliance.approveUserKyc)

POST

[/api/v1/admin/kyc/{kycId}/reject](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Countries%20&%20Compliance/adminCompliance.rejectUserKyc)

GET

[/api/v1/admin/kyc](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Countries%20&%20Compliance/adminCompliance.listUserKyc)

### [Admin - Pricing & Assets](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Pricing%20&%20Assets)

GET

[/api/v1/admin/pricing](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Pricing%20&%20Assets/adminPricing.getPricing)

PATCH

[/api/v1/admin/pricing](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Pricing%20&%20Assets/adminPricing.updatePricing)

GET

[/api/v1/admin/send-assets](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Pricing%20&%20Assets/adminPricing.getSendAssets)

PATCH

[/api/v1/admin/send-assets](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Pricing%20&%20Assets/adminPricing.updateSendAsset)

GET

[/api/v1/admin/send-networks](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Pricing%20&%20Assets/adminPricing.getSendNetworks)

PATCH

[/api/v1/admin/send-networks](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Pricing%20&%20Assets/adminPricing.updateSendNetwork)

GET

[/api/v1/admin/corridors](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Pricing%20&%20Assets/adminPricing.getCorridors)

PATCH

[/api/v1/admin/corridors](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Pricing%20&%20Assets/adminPricing.updateCorridor)

### [Admin - Partners](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Partners)

GET

[/api/v1/admin/partners](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Partners/adminPartners.getAllPartners)

GET

[/api/v1/admin/partners/{partnerId}](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Partners/adminPartners.getPartner)

POST

[/api/v1/admin/partners/{partnerId}/approve](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Partners/adminPartners.approvePartnerKyc)

POST

[/api/v1/admin/partners/{partnerId}/reject](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Partners/adminPartners.rejectPartnerKyc)

POST

[/api/v1/admin/partners/{partnerId}/request-resubmission](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Partners/adminPartners.requestPartnerResubmission)

POST

[/api/v1/admin/addresses/regenerate](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Partners/adminPartners.regenerateAddresses)

POST

[/api/v1/admin/addresses/regenerate-partners](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Partners/adminPartners.regeneratePartnerAddresses)

PATCH

[/api/v1/admin/partners/{partnerId}/deposit-policy](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Partners/adminPartners.updatePartnerDepositPolicy)

### [Admin - Payouts & Withdrawals](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Payouts%20&%20Withdrawals)

GET

[/api/v1/admin/transactions/stats](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Payouts%20&%20Withdrawals/adminPayouts.getTransactionStats)

GET

[/api/v1/admin/cross-border-payouts](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Payouts%20&%20Withdrawals/adminPayouts.getCrossBorderPayouts)

POST

[/api/v1/admin/cross-border-payouts/{id}/submit](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Payouts%20&%20Withdrawals/adminPayouts.submitCrossBorderPayout)

POST

[/api/v1/admin/cross-border-payouts/{id}/resolve](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Payouts%20&%20Withdrawals/adminPayouts.resolveCrossBorderPayout)

GET

[/api/v1/admin/withdrawals](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Payouts%20&%20Withdrawals/adminPayouts.getAdminWithdrawals)

POST

[/api/v1/admin/withdrawals/{id}/confirm](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Payouts%20&%20Withdrawals/adminPayouts.confirmWithdrawal)

POST

[/api/v1/admin/withdrawals/{id}/reverse](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Payouts%20&%20Withdrawals/adminPayouts.reverseWithdrawal)

### [Admin - Users](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Users)

GET

[/api/v1/admin/users](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Users/adminUsers.getAllUsers)

POST

[/api/v1/admin/users/{userId}/request-reverification](https://app.dutchmannetwork.online/api/docs#/Admin%20-%20Users/adminUsers.requestUserReverification)

### [Users](https://app.dutchmannetwork.online/api/docs#/Users)

POST

[/api/v1/user/create](https://app.dutchmannetwork.online/api/docs#/Users/user.createUser)

GET

[/api/v1/user/me](https://app.dutchmannetwork.online/api/docs#/Users/user.me)

### [KYC](https://app.dutchmannetwork.online/api/docs#/KYC)

GET

[/api/v1/kyc/verify](https://app.dutchmannetwork.online/api/docs#/KYC/kyc.verifyKycToken)

GET

[/api/v1/kyc/status](https://app.dutchmannetwork.online/api/docs#/KYC/kyc.getStatus)

### [Uploads](https://app.dutchmannetwork.online/api/docs#/Uploads)

POST

[/api/v1/uploads/kyb-document](https://app.dutchmannetwork.online/api/docs#/Uploads/uploads.uploadKybDocument)

Upload a KYB supporting document (CAC certificate, director IDs, etc.)

### [Signer](https://app.dutchmannetwork.online/api/docs#/Signer)

POST

[/api/v1/internal/signer/send](https://app.dutchmannetwork.online/api/docs#/Signer/signer.send)

POST

[/api/v1/internal/signer/fund-gas](https://app.dutchmannetwork.online/api/docs#/Signer/signer.fundGas)

POST

[/api/v1/internal/signer/sweep](https://app.dutchmannetwork.online/api/docs#/Signer/signer.sweep)

POST

[/api/v1/internal/signer/refund](https://app.dutchmannetwork.online/api/docs#/Signer/signer.refund)

### [Partner Management](https://app.dutchmannetwork.online/api/docs#/Partner%20Management)

POST

[/api/v1/partner/update-company-details](https://app.dutchmannetwork.online/api/docs#/Partner%20Management/partner.updateCompanyDetails)

GET

[/api/v1/partner/get-api-key](https://app.dutchmannetwork.online/api/docs#/Partner%20Management/partner.getNewApiKey)

POST

[/api/v1/partner/kyc/business](https://app.dutchmannetwork.online/api/docs#/Partner%20Management/partner.submitBusinessKyc)

PATCH

[/api/v1/partner/kyb-draft](https://app.dutchmannetwork.online/api/docs#/Partner%20Management/partner.saveKybDraft)

GET

[/api/v1/partner/customers](https://app.dutchmannetwork.online/api/docs#/Partner%20Management/partner.getCustomers)

GET

[/api/v1/partner/customers/{userId}/kyc-link](https://app.dutchmannetwork.online/api/docs#/Partner%20Management/partner.getCustomerKycLink)

GET

[/api/v1/partner/customers/{userId}/kyc](https://app.dutchmannetwork.online/api/docs#/Partner%20Management/partner.getCustomerKycStatus)

POST

[/api/v1/partner/rotate-api-key](https://app.dutchmannetwork.online/api/docs#/Partner%20Management/partner.rotateApiKey)

POST

[/api/v1/partner/update-webhook](https://app.dutchmannetwork.online/api/docs#/Partner%20Management/partner.updateWebhook)

GET

[/api/v1/partner/addresses](https://app.dutchmannetwork.online/api/docs#/Partner%20Management/partner.getAddresses)

GET

[/api/v1/partner/profile](https://app.dutchmannetwork.online/api/docs#/Partner%20Management/partner.getProfile)

### [Partner API - Customers](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Customers)

POST

[/api/v1/partner/v1/customers](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Customers/customers.register)

Register a customer under your account

GET

[/api/v1/partner/v1/customers/{customerId}](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Customers/customers.get)

Read one of your customer's profile

GET

[/api/v1/partner/v1/customers/{customerId}/full](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Customers/customers.full)

A customer's full snapshot -- profile, KYC, and wallet -- in one call

### [Partner API - Profile](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Profile)

DELETE

[/api/v1/partner/v1/customers/{customerId}](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Profile/profile.deleteAccount)

Delete the customer's account

GET

[/api/v1/partner/v1/customers/{customerId}/profile](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Profile/profile.profile)

The customer's profile

PATCH

[/api/v1/partner/v1/customers/{customerId}/profile](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Profile/profile.updateProfile)

Update the customer's profile

PATCH

[/api/v1/partner/v1/customers/{customerId}/change-password](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Profile/profile.changePassword)

Change the customer's password

GET

[/api/v1/partner/v1/customers/{customerId}/withdrawals](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Profile/profile.withdrawals)

The customer's withdrawal / global payout history, newest first

### [Partner API - Invoices](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Invoices)

POST

[/api/v1/partner/v1/customers/{customerId}/invoices](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Invoices/invoices.upload)

Upload an invoice for a business customer

GET

[/api/v1/partner/v1/customers/{customerId}/invoices](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Invoices/invoices.list)

A customer's invoices, newest first

### [Partner API - KYC](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20KYC)

GET

[/api/v1/partner/v1/customers/{customerId}/verification](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20KYC/kyc.summary)

Where the customer stands, and what to submit next

GET

[/api/v1/partner/v1/customers/{customerId}/kyc](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20KYC/kyc.status)

A customer's KYC records, newest first

GET

[/api/v1/partner/v1/customers/{customerId}/kyc/reverification](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20KYC/kyc.reverification)

Any open re-verification request an admin has raised for the customer

POST

[/api/v1/partner/v1/customers/{customerId}/kyc/tier1](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20KYC/kyc.tier1)

Submit Tier 1 (BVN + NIN)

POST

[/api/v1/partner/v1/customers/{customerId}/kyc/tier2](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20KYC/kyc.tier2)

Submit Tier 2 (ID document, from a prior /kyc/documents upload)

POST

[/api/v1/partner/v1/customers/{customerId}/kyc/tier3](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20KYC/kyc.tier3)

Submit Tier 3 (date of birth + address, for cross-border corridors)

POST

[/api/v1/partner/v1/customers/{customerId}/kyc/selfie-check](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20KYC/kyc.selfieCheckRoute)

Check a customer's selfie before submitting it

POST

[/api/v1/partner/v1/customers/{customerId}/kyc/documents](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20KYC/kyc.document)

Upload a customer's ID document or selfie ahead of Tier 2

### [Partner API - Wallet](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Wallet)

GET

[/api/v1/partner/v1/customers/{customerId}/balance](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Wallet/wallet.balance)

USDT + local fiat balance

GET

[/api/v1/partner/v1/customers/{customerId}/balance/stream](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Wallet/wallet.streamBalance)

Live updates: re-emits the customer's balance on every credit/debit

GET

[/api/v1/partner/v1/customers/{customerId}/transactions](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Wallet/wallet.transactions)

Recent balance movements, cursor-paginated

GET

[/api/v1/partner/v1/customers/{customerId}/addresses](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Wallet/wallet.addresses)

The customer's per-network USDT deposit addresses

GET

[/api/v1/partner/v1/customers/{customerId}/virtual-account](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Wallet/wallet.virtualAccountFor)

Local-currency virtual account for fiat funding

GET

[/api/v1/partner/v1/customers/{customerId}/withdraw/quote](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Wallet/wallet.withdrawalQuote)

Price a withdrawal before submitting it

POST

[/api/v1/partner/v1/customers/{customerId}/withdraw](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Wallet/wallet.withdraw)

Pay a held balance out to the customer's default bank account

POST

[/api/v1/partner/v1/customers/{customerId}/funding/charge](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Wallet/wallet.initiateFundingCharge)

Start a fund-by-charge: a one-off bank account (bank\_transfer) or a redirect URL to authorise (eft, ZAR)

GET

[/api/v1/partner/v1/customers/{customerId}/funding/charges](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Wallet/wallet.fundingCharges)

The customer's funding charges, newest first

### [Partner API - Send](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Send)

GET

[/api/v1/partner/v1/customers/{customerId}/send/networks](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Send/send.networks)

Networks the customer can send USDT/USDC on, with fee and minimum

POST

[/api/v1/partner/v1/customers/{customerId}/send/quote](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Send/send.quote)

Quote a send before submitting it

POST

[/api/v1/partner/v1/customers/{customerId}/send](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Send/send.submit)

Send USDT on-chain to the given address

### [Partner API - Global Send](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Global%20Send)

GET

[/api/v1/partner/v1/customers/{customerId}/global-send/verification](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Global%20Send/globalSend.verificationStatus)

Re-check the customer's level 3 verification status with the partner

GET

[/api/v1/partner/v1/customers/{customerId}/global-send/corridors](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Global%20Send/globalSend.corridors)

Countries the customer can send to, with their currency and rails

POST

[/api/v1/partner/v1/customers/{customerId}/global-send/quote](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Global%20Send/globalSend.quote)

Price a cross-border send for the customer

POST

[/api/v1/partner/v1/customers/{customerId}/global-send/initiate](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Global%20Send/globalSend.initiate)

Initiate a cross-border send for the customer

### [Partner API - Ramp](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Ramp)

POST

[/api/v1/partner/v1/customers/{customerId}/buy/quote](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Ramp/ramp.buyQuote)

Price a buy (fiat -> stablecoin) against the customer's fiat balance

POST

[/api/v1/partner/v1/customers/{customerId}/buy/execute](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Ramp/ramp.buy)

Execute a buy from the customer's fiat balance

GET

[/api/v1/partner/v1/customers/{customerId}/sell/networks](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Ramp/ramp.sellNetworks)

Networks the customer can deposit stablecoins on

GET

[/api/v1/partner/v1/customers/{customerId}/rate](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Ramp/ramp.rate)

Live all-in stablecoin rates in the customer's local fiat, for previewing a conversion

POST

[/api/v1/partner/v1/customers/{customerId}/sell/quote](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Ramp/ramp.sellQuote)

Price a sell (stablecoin -> fiat) against the customer's balance

POST

[/api/v1/partner/v1/customers/{customerId}/sell/execute](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Ramp/ramp.sell)

Execute a sell from the customer's stablecoin balance

### [Partner API - Banks](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Banks)

GET

[/api/v1/partner/v1/customers/{customerId}/banks](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Banks/bank.banks)

Banks for the given (or the customer's own) country/currency

POST

[/api/v1/partner/v1/customers/{customerId}/bank/verify-account](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Banks/bank.verifyAccount)

Resolve an account number to its account name

POST

[/api/v1/partner/v1/customers/{customerId}/accounts](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Banks/bank.addAccount)

Link a payout bank account to the customer

GET

[/api/v1/partner/v1/customers/{customerId}/accounts](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Banks/bank.getAccounts)

List the customer's linked payout accounts, default first

PATCH

[/api/v1/partner/v1/customers/{customerId}/accounts/{accountId}/default](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Banks/bank.setDefaultAccount)

Make a linked account the customer's default payout destination

DELETE

[/api/v1/partner/v1/customers/{customerId}/accounts/{accountId}](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Banks/bank.deleteAccount)

Remove a customer's linked payout account

### [Partner API - Receiving](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Receiving)

GET

[/api/v1/partner/v1/customers/{customerId}/receiving-accounts/currencies](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Receiving/receiving.currencies)

Foreign currencies the customer can be paid in

GET

[/api/v1/partner/v1/customers/{customerId}/receiving-accounts](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Receiving/receiving.list)

Every foreign-currency account the customer holds

GET

[/api/v1/partner/v1/customers/{customerId}/receiving-accounts/activity](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Receiving/receiving.activity)

Payments seen on the customer's receiving accounts, including ones still in flight

POST

[/api/v1/partner/v1/customers/{customerId}/receiving-accounts/{currency}](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Receiving/receiving.open)

Open (or return) the customer's account for one currency

POST

[/api/v1/partner/v1/customers/{customerId}/receiving-accounts/{currency}/refresh](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Receiving/receiving.refresh)

Re-read one of the customer's accounts from the partner

### [Partner API - Countries](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Countries)

GET

[/api/v1/partner/v1/countries](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Countries/countries.list)

Countries currently enabled for onboarding

### [Partner API - Features](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Features)

GET

[/api/v1/partner/v1/features](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Features/features.list)

Every switchable capability and its current state

### [Partner API - Webhooks](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Webhooks)

GET

[/api/v1/partner/v1/webhook](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Webhooks/webhook.config)

Your current webhook URL and whether a secret is set

PUT

[/api/v1/partner/v1/webhook](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Webhooks/webhook.setUrl)

Set your webhook URL and receive a new signing secret

POST

[/api/v1/partner/v1/webhook/rotate-secret](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Webhooks/webhook.rotateSecret)

Rotate the signing secret

GET

[/api/v1/partner/v1/webhook/deliveries](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Webhooks/webhook.deliveries)

Your delivery log, newest first

GET

[/api/v1/partner/v1/webhook/deliveries/{id}](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Webhooks/webhook.delivery)

One delivery, including the payload that was sent

POST

[/api/v1/partner/v1/webhook/deliveries/{id}/replay](https://app.dutchmannetwork.online/api/docs#/Partner%20API%20-%20Webhooks/webhook.replay)

Send a delivery again

### [Authentication](https://app.dutchmannetwork.online/api/docs#/Authentication)

POST

[/api/v1/authentication/login](https://app.dutchmannetwork.online/api/docs#/Authentication/auth.login)

Sign in a user

POST

[/api/v1/authentication/refresh](https://app.dutchmannetwork.online/api/docs#/Authentication/auth.refresh)

Refresh access token

POST

[/api/v1/authentication/forgot-password](https://app.dutchmannetwork.online/api/docs#/Authentication/auth.forgotPassword)

Request password reset

POST

[/api/v1/authentication/reset-password](https://app.dutchmannetwork.online/api/docs#/Authentication/auth.resetPassword)

Reset password

### [Webhooks](https://app.dutchmannetwork.online/api/docs#/Webhooks)

POST

[/api/v1/webhooks/alchemy](https://app.dutchmannetwork.online/api/docs#/Webhooks/webhook.handleAlchemyEvent)

POST

[/api/v1/webhooks/fincra](https://app.dutchmannetwork.online/api/docs#/Webhooks/webhook.handleFincraEvent)

POST

[/api/v1/webhooks/monnify](https://app.dutchmannetwork.online/api/docs#/Webhooks/webhook.handleMonnifyEvent)

POST

[/api/v1/webhooks/busha](https://app.dutchmannetwork.online/api/docs#/Webhooks/webhook.handleBushaEvent)

POST

[/api/v1/webhooks/quidax](https://app.dutchmannetwork.online/api/docs#/Webhooks/webhook.handleQuidaxEvent)

POST

[/api/v1/webhooks/bridge](https://app.dutchmannetwork.online/api/docs#/Webhooks/webhook.handleBridgeEvent)

### [Compliance](https://app.dutchmannetwork.online/api/docs#/Compliance)

GET

[/api/v1/compliance/policies](https://app.dutchmannetwork.online/api/docs#/Compliance/policies.getPolicies)

POST

[/api/v1/compliance/policies](https://app.dutchmannetwork.online/api/docs#/Compliance/policies.updatePolicy)

GET

[/api/v1/compliance/policies/{type}](https://app.dutchmannetwork.online/api/docs#/Compliance/policies.getPolicyByType)

### [Admin](https://app.dutchmannetwork.online/api/docs#/Admin)

GET

[/api/v1/admin/features](https://app.dutchmannetwork.online/api/docs#/Admin/featureAdmin.list)

Every switchable capability and its current state

PATCH

[/api/v1/admin/features/{key}](https://app.dutchmannetwork.online/api/docs#/Admin/featureAdmin.update)

Set a capability to LIVE, COMING\_SOON or OFF

### [Liquidity Providers](https://app.dutchmannetwork.online/api/docs#/Liquidity%20Providers)

GET

[/api/v1/liquidity-provider/me](https://app.dutchmannetwork.online/api/docs#/Liquidity%20Providers/liquidityProvider.getMine)

POST

[/api/v1/liquidity-provider/register](https://app.dutchmannetwork.online/api/docs#/Liquidity%20Providers/liquidityProvider.register)

GET

[/api/v1/liquidity-provider/balances](https://app.dutchmannetwork.online/api/docs#/Liquidity%20Providers/liquidityProvider.getBalances)

GET

[/api/v1/liquidity-provider/rewards](https://app.dutchmannetwork.online/api/docs#/Liquidity%20Providers/liquidityProvider.getRewards)

POST

[/api/v1/liquidity-provider/deposit](https://app.dutchmannetwork.online/api/docs#/Liquidity%20Providers/liquidityProvider.deposit)

POST

[/api/v1/liquidity-provider/withdraw](https://app.dutchmannetwork.online/api/docs#/Liquidity%20Providers/liquidityProvider.withdraw)

#### Schemas

UpdateTreasuryOpsDto

UpdateSweepConfigDto

UpdateTreasuryFloatDto

ManualTopUpDto

UpdateLiquiditySweepDto

UpdateVaProviderDto

CreateCountryDto

UpdateCountryDto

SetCountryEnabledDto

RejectKycDto

NetworkGasFeesDto

UpdatePricingDto

UpdateSendAssetDto

UpdateSendNetworkDto

UpdateCorridorDto

RegenerateAddressesDto

RegeneratePartnerAddressesDto

UpdatePartnerDepositPolicyDto

SubmitCrossBorderPayoutDto

ResolveCrossBorderPayoutDto

ReverseWithdrawalDto

RequestReverificationDto

CreateUserDto

CreateCompanyDto

BusinessKycDto

KybDraftDto

UpdateWebhookDto

PartnerBusinessDto

PartnerCustomerDto

BusinessDetailsDto

RegisterCustomerDto

KycStatus

PartnerKycRecordDto

ReverificationItem

ReverificationStatus

PartnerReverificationRequestDto

PartnerCustomerKycSnapshotDto

PartnerBalanceDto

PartnerDepositAddressDto

PartnerVirtualAccountDto

PartnerCustomerWalletSnapshotDto

PartnerCustomerSnapshotDto

PartnerInvoiceDto

PartnerTierStatus

PartnerTierStateDto

PartnerVerificationTiersDto

PartnerVerificationInput

PartnerVerificationSummaryDto

PartnerKycSubmissionDto

Tier1KycDto

Tier2KycDto

PartnerVerificationRecordDto

SubmitTier3Dto

PartnerSelfieCheckDto

CheckSelfieDto

PartnerUploadedDocumentDto

LedgerEntryType

PartnerLedgerEntryDto

PartnerWithdrawalQuoteDto

WithdrawalStatus

PartnerWithdrawalBankAccountDto

PartnerWithdrawalDto

WithdrawDto

FundingChargeStatus

PartnerFundingChargeDto

InitiateFundingChargeDto

BlockchainNetwork

PartnerSendNetworkDto

PartnerSendQuoteDto

QuoteSendDto

PartnerSendResultDto

SendDto

PartnerCorridorDto

PartnerGlobalSendQuoteDto

GlobalSendQuoteDto

PartnerGlobalSendResultDto

GlobalSendBeneficiaryDto

InitiateGlobalSendDto

PartnerRampQuoteDto

GetQuoteDto

PartnerBuyResultDto

CustomerSellDto

PartnerNetworkDto

PartnerRateDto

PartnerSellResultDto

PartnerBankDto

PartnerAccountVerificationDto

VerifyAccountNumberInput

PartnerBankAccountDto

AddAccountDto

UpdateCustomerProfileDto

ResetPassword

PartnerReceivingAccountDto

PartnerReceivingActivityDto

PartnerCountryDto

FeatureStatus

PartnerFeatureDto

PartnerWebhookConfigDto

PartnerWebhookTestDto

PartnerWebhookSecretDto

SetWebhookUrlDto

WebhookDeliveryStatus

PartnerWebhookDeliveryDto

PartnerWebhookDeliveryDetailDto

SignInUserDto

RefreshTokenDto

ForgotPasswordDto

ResetPasswordDto

ComplianceDocumentDto

UpdateFeatureDto

RegisterLiquidityProviderDto

LiquidityMovementDto
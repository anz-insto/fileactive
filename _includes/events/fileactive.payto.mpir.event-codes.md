### PayTo MPIR Event Codes

Validation failures relating to MPIR submissions. 

The transaction status and transaction reason codes are returned in the [PayTo API Webhook **MPIR Processing Outcomes**]({{ site.baseurl }}/fileactive/api/payto-api-webhook).

Transaction reason codes can be generated by both ANZ and the other finiancial institution (OFI) involved in processing the MPIR. Where ANZ is also the debtor then ANZ can generate the "OFI" transaction reason codes below.

| transaction_status | transaction_status_reason_code | transaction_status_additional_information | Description | Source of Reason Code |
|:---:|:---:|---|---|:---:|
| RJCT | AB01 | AbortedClearingTimeout | Clearing process aborted due to timeout | OFI |
| RJCT | AB02 | AbortedClearingFatalError | Clearing process aborted due to a fatal error | OFI |
| RJCT | AB03 | AbortedSettlementTimeout | Settlement aborted due to timeout | OFI |
| RJCT | AB04 | AbortedSettlementFatalError | Settlement process aborted due to a fatal error | OFI |
| RJCT | AB08 | OfflineCreditorAgent | Creditor Agent is not online | OFI |
| RJCT | AC02 | InvalidDebtorAccountNumber | Debtor account number invalid or missing | OFI |
| RJCT | AC02 | Invalid Debtor Account | Debtor name on mandate is not matching debtor name returned from  alias resolution service | ANZ |
| RJCT | AC03 | Creditor Account number invalid or missing | Creditor account number invalid or missing | ANZ |
| RJCT | AC03 | InvalidCreditorAccountNumber | Creditor account number invalid or missing | OFI |
| RJCT | AC05 | ClosedDebtorAccountNumber | Debtor account number closed | OFI |
| RJCT | AC06 | BlockedAccount | Account specified is blocked, prohibiting posting of transactions against it | OFI |
| RJCT | AC06 | Creditor account blocked | Account specified is blocked, prohibiting posting of transactions against it | ANZ |
| RJCT | AC07 | ClosedCreditorAccountNumber | Creditor account number closed | OFI |
| RJCT | AC07 | Closed Creditor Account number | Creditor account number closed | ANZ |
| RJCT | AC13 | InvalidDebtorAccountType | Debtor account type missing or invalid | OFI |
| RJCT | AC14 | InvalidCreditorAccountType | Creditor account type missing or invalid | OFI |
| RJCT | AC15 | AccountDetailsChanged | The account details for the counterparty have changed | OFI |
| RJCT | AG01 | TransactionForbidden | Transaction forbidden on this type of account | OFI |
| RJCT | AG03 | TransactionNotSupported | Transaction type not supported/authorized on this account | OFI |
| RJCT | AG07 | UnsuccesfulDirectDebit | Debtor account cannot be debited for a generic reason | OFI |
| RJCT | AGNT | IncorrectAgent | Agent in the payment workflow is incorrect | OFI |
| RJCT | AM01 | Specified message amount is equal to zero | Instructed Amount is invalid | ANZ |
| RJCT | AM01 | ZeroAmount | Specified message amount is equal to zero | OFI |
| RJCT | AM02 | NotAllowedAmount | Specific transaction/message amount is greater than allowed maximum | OFI |
| RJCT | AM03 | Not Allowed Currency | Instructed Currency is not AUD | ANZ |
| RJCT | AM03 | NotAllowedCurrency | Specified message amount is an non processable currency outside of existing agreement | OFI |
| RJCT | AM04 | InsufficientFunds | Amount of funds available to cover specified message amount is insufficient | OFI |
| RJCT | AM06 | TooLowAmount | Specified transaction amount is less than agreed minimum | OFI |
| RJCT | AM09 | Wrong Amount | Amount received is not the amount agreed or expected | ANZ |
| RJCT | AM09 | WrongAmount | Amount received is not the amount agreed or expected | OFI |
| RJCT | AM12 | InvalidAmount | Amount is invalid or missing | OFI |
| RJCT | AM19 | InvalidGroupNumberOfTransactions | Number of transactions at the Group level is invalid or missing | OFI |
| RJCT | AM21 | Daily MPIR pay away limit exceeded. Your daily limit is AUD XXX,XXX.XX. Available limit (as at "Time in HH:MM:SS in Melbourne/Sydney Time"" on ""MPIR Date""): AUD XXX,XXX.XX | Daily MPIR limit has been exceeded | ANZ |
| RJCT | AM21 | LimitExceeded | Transaction amount exceeds limits agreed between bank and client | OFI |
| RJCT | AVED | AfterValidityEndDate | Mandate Validity end date has been passed | ANZ |
| RJCT | BE05 | UnrecognisedInitiatingParty | Party who initiated the message is not recognised by the end customer | OFI |
| RJCT | BE06 | UnknownEndCustomer | End customer specified is not known at associated Sort/National Bank Code or does no longer exist in the books | OFI |
| RJCT | BE08 | MissingDebtorName | Debtor name is missing | OFI |
| RJCT | BE22 | Creditor name is missing | Creditor Name or Ultimate Creditor Name or both are missing | ANZ |
| RJCT | BE22 | MissingCreditorName | Creditor name is missing | OFI |
| RJCT | BVSD | BeforeValidityStartDate | Mandate validity start date has not been reached | ANZ |
| RJCT | CH03 | Payment Date is in future and invalid. | requested_execution_date is too far in the future | ANZ |
| RJCT | CH03 | Requested Execution Time is too far in the future | payment_execute_not_before_time  too far into the futureNote future dated MPIRs are released at 00:01  on the requested_execution_date | ANZ |
| RJCT | CH04 | Payment Date is in past and invalid. | requested_execution_date is too far in the past | ANZ |
| RJCT | CH20 | DecimalPointsNotCompatibleWithCurrency | Number of decimal points not compatible with the currency | OFI |
| RJCT | CH21 | RequiredCompulsoryElementMissing | Mandatory element is missing | OFI |
| RJCT | CURR | IncorrectCurrency | Currency of the payment is incorrect | OFI |
| RJCT | CUST | RequestedByCustomer | Cancellation requested by the Debtor | OFI |
| RJCT | DS09 | EC004_403 Failed to decrypt and verify the message | ANZ is unable to decrypt MPIR | ANZ |
| RJCT | DT02 | InvalidCreationDate | Invalid creation date and time in Group Header (eg, historic date) | OFI |
| RJCT | DT04 | FutureDateNotSupported | Future date not supported | OFI |
| RJCT | DU05 | Duplicate Instruction ID | instruction_identification needs to be unique for each MPS User Id | ANZ |
| RJCT | ED05 | SettlementFailed | Settlement of the transaction has failed | OFI |
| RJCT | ED06 | SettlementSystemNotAvailable | Interbank settlement system not available | OFI |
| RJCT | FF04 | InvalidServiceLevelCode | Service Level code is missing or invalid | OFI |
| RJCT | FF08 | InvalidEndToEndId | End to End Id missing or invalid | OFI |
| RJCT | FF10 | EC004_409 MPIR processing failed due to a technical issue | Generic error for any technical issues processing a MPIR where no reason code is available | ANZ |
| RJCT | FF10 | Unexpected error. Please try again and contact the ANZ Customer Service Centre if the issue persists | Technical error reported by downstream system | ANZ |
| RJCT | FF10 | BankSystemProcessingError | File or transaction cannot be processed due to technical issues at the bank side | OFI |
| RJCT | FF11 | ClearingRequestAborted | Clearing request rejected due it being subject to an abort operation | OFI |
| RJCT | G005 | DeliveredWithServiceLevel | Payment has been delivered to creditor agent with service level | OFI |
| RJCT | G006 | DeliveredWIthoutServiceLevel | Payment has been delivered to creditor agent without service level | OFI |
| RJCT | MCGP | MGCRInGracePeriod | A mandate with establishment scheme MGCR will only be valid for payment after a grace period of 5 calendar days from the registration of the mandate | ANZ |
| RJCT | MD01 | No mandate | mandate_identification is not found in MMS | ANZ |
| RJCT | MD01 | NoMandate | No Mandate | OFI |
| RJCT | MD02 | MissingMandatoryInformationInMandate | Mandate related information data required by the scheme is missing | OFI |
| RJCT | MD20 | MandateExpired | Mandate cancellation following validity expiration | OFI |
| RJCT | MS02 | NotSpecifiedReasonCustomerGenerated | Reason has not been specified by end customer | OFI |
| RJCT | MS03 | NotSpecifiedReasonAgentGenerated | Reason has not been specified by agent | OFI |
| RJCT | NACT | NotActive | Mandate status is not active | ANZ |
| RJCT | NARR | EC004_405 MPS User Id value: [mpsUserId] is invalid | MPS User Id Is Invalid | ANZ |
| RJCT | NARR | 4001 Division is invalid. Contact the ANZ Customer Service Centre | Invalid Division | ANZ |
| RJCT | NARR | 4002 Product is not entitled. Contact the ANZ Customer Service Centre | MPS User not entitled to submit MPIR | ANZ |
| RJCT | NARR | 4003 MPS User is invalid. Contact the ANZ Customer Service Centre | MPS User Id Is Invalid in downstream system | ANZ |
| RJCT | NARR | [{errorDetail}] | Reason is provided as narrative information | OFI |
| RJCT | NAUT | Unauthorised Mandate | MPS User Id not authorised to mandate | ANZ |
| RJCT | NAUT | Unauthorised Mandate | Permission to be processed is not granted | OFI |
| RJCT | RC05 | InvalidBICIdentifier | BIC identifier is invalid or missing | OFI |
| RJCT | RR02 | MissingDebtorNameOrAddress | Specification of the debtor’s name and/or address needed for regulatory requirements is insufficient or missing | OFI |
| RJCT | RR03 | MissingCreditorNameOrAddress | Specification of the creditor’s name and/or address needed for regulatory requirements is insufficient or missing | OFI |
| RJCT | SL01 | SpecificServiceOfferedByDebtorAgent | Due to specific service offered by the Debtor Agent | OFI |
| RJCT | SL11 | CreditorNotOnWhitelistOfDebtor | Whitelisting service offered by the Debtor Agent; Debtor has not included the Creditor on its “Whitelist” (yet). In the Whitelist the Debtor may list all allowed Creditors to debit Debtor bank account | OFI |
| RJCT | SL13 | MaximumNumberOfDirectDebitTransactionsExceeded | Due to Maximum allowed Direct Debit Transactions per period service offered by the Debtor Agent | OFI |
| RJCT | SL14 | MaximumDirectDebitTransactionAmountExceeded | Due to Maximum allowed Direct Debit Transaction amount service offered by the Debtor Agent | OFI |
| RJCT | TD03 | EC004_404 Schema validation failed against the unencrypted PayTo Request schema, error details [{errorDetail}] | MPIR invalid schema | ANZ |
| RJCT | TD03 | IncorrectFileStructure | The file format is incomplete or invalid | OFI |
| RJCT | TM01 | InvalidCutOffTime | Associated message, payment information block, or transaction was received after agreed processing cut-off time | OFI |
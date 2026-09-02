# Org.OpenAPITools.Model.Invoice

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Attachments** | **Object** |  | [optional] 
**BillingPeriodEnd** | **DateOnly?** |  | [optional] 
**BillingPeriodStart** | **DateOnly?** |  | [optional] 
**CancellationDate** | **DateOnly?** |  | [optional] 
**CancellationInvoiceId** | **string** | References the invoice entity. | [optional] 
**CancellationReason** | **string** |  | [optional] 
**ContractId** | **Guid?** | References the contract entity. | [optional] 
**Currency** | **CurrencyCode** |  | 
**CustomerId** | **string** | References the customer entity. | [optional] 
**DiscountAmount** | **string** |  | [optional] 
**DiscountDays** | **int?** |  | [optional] 
**DiscountPercentage** | **string** |  | [optional] 
**DocumentType** | **DocumentType** |  | [optional] 
**DunningLevel** | **int** |  | [optional] 
**InputVatAmount** | **string** |  | [optional] 
**InputVatDeductible** | **bool** |  | [optional] 
**InputVatPercentage** | **string** |  | [optional] 
**IntroductionText** | **string** |  | [optional] 
**InvoiceType** | **InvoiceType** |  | 
**IsCancelled** | **bool** |  | [optional] 
**IsDraft** | **bool** |  | [optional] 
**IsEuAcquisition** | **bool** |  | [optional] 
**IsEuDelivery** | **bool** |  | [optional] 
**IsIntraCommunityAcquisition** | **bool** |  | [optional] 
**IsReverseCharge** | **bool** |  | [optional] 
**IssueDate** | **DateOnly** |  | 
**LedgerAccount** | **string** |  | [optional] 
**LineItems** | **Object** |  | 
**Margin25a** | **bool** |  | [optional] 
**Margin25aGross** | **string** |  | [optional] 
**Margin25aPurchasePrice** | **string** |  | [optional] 
**Notes** | **string** |  | [optional] 
**OrderNumber** | **string** |  | [optional] 
**OriginalPdfPath** | **string** |  | [optional] 
**PaidAmount** | **string** |  | [optional] 
**PaymentDueDate** | **DateOnly?** |  | [optional] 
**PaymentStatus** | **PaymentStatus** |  | [optional] 
**PaymentTermsText** | **string** |  | [optional] 
**PrecedingSalesVoucherId** | **string** | References the preceding sales voucher entity. | [optional] 
**PrecedingSalesVoucherType** | **PrecedingSalesVoucherType** |  | [optional] 
**ReceiptConfirmationAvailable** | **bool** |  | [optional] 
**RelatedInvoiceId** | **Guid?** | References the invoice entity. | [optional] 
**RelationshipType** | **string** |  | [optional] 
**SenderSnapshot** | **Object** |  | [optional] 
**SentAt** | **DateTime?** |  | [optional] 
**ServicePeriodEnd** | **DateOnly?** |  | [optional] 
**ServicePeriodStart** | **DateOnly?** |  | [optional] 
**Status** | **InvoiceStatus** |  | 
**Subtotal** | **string** |  | 
**SupplierId** | **string** | References the supplier entity. | [optional] 
**TaxExemptionReason** | **string** |  | [optional] 
**TotalAmount** | **string** |  | 
**TotalTax** | **string** |  | 
**VatCountry** | **CountryCode** |  | [optional] 
**VatSpecialCase** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


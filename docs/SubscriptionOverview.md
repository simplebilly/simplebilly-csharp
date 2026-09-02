# Org.OpenAPITools.Model.SubscriptionOverview
Tenant subscription overview for the billing page: current plan, status, period end, trial state, effective limits, current usage and feature flags. Backed by Paddle Billing webhook data written into `billing_info` + `tenants.plan`, and by the canonical plans in `crate::saasy::plans`.  JSON contract (camelCase, matches the frontend): `plan`, `planName`, `priceEur`, `status`, `currentPeriodEnd`, `manageUrl`, `trialEndsAt`, `isTrialing`, `limits:{maxUsers,maxInvoicesPerMonth,maxConnectors}`, `usage:{users,invoicesThisMonth,connectors,overageSeats}`, `features:{taxAutomations,fancyReports,erp}`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CurrentPeriodEnd** | **DateTime?** |  | [optional] 
**Features** | [**PlanFeatures**](PlanFeatures.md) |  | 
**IsTrialing** | **bool** |  | 
**Limits** | [**PlanLimits**](PlanLimits.md) |  | 
**ManageUrl** | **string** |  | [optional] 
**Plan** | **string** | Resolved plan id (free/starter/business/enterprise, or a custom override id). | 
**PlanName** | **string** |  | 
**PriceEur** | **double** | Monthly price in EUR; &#x60;-1.0&#x60; &#x3D; custom pricing (enterprise). | 
**Quantity** | **int?** |  | [optional] 
**Status** | **string** |  | [optional] 
**SubscriptionId** | **string** |  | [optional] 
**TrialEndsAt** | **DateTime?** |  | [optional] 
**Usage** | [**UsageSnapshot**](UsageSnapshot.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


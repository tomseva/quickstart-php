# PUTSubscriptionSuspendType

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**apply_credit_balance** | **bool** | Applies a credit balance to an invoice.  If the value is &#x60;true&#x60;, the credit balance is applied to the invoice. If the value is &#x60;false&#x60;, no action is taken.  Prerequisite: &#x60;invoice&#x60; must be &#x60;true&#x60;.   To view the credit balance adjustment, retrieve the details of the invoice using the Get Invoices method. | [optional] 
**collect** | **bool** | Collects an automatic payment for a subscription. The collection generated in this operation is only for this subscription, not for the entire customer account.  If the value is &#x60;true&#x60;, the automatic payment is collected. If the value is &#x60;false&#x60;, no action is taken.  The default value is &#x60;false&#x60;.  Prerequisite: &#x60;invoice&#x60; must be &#x60;true&#x60;.   **Note:** This field is in Zuora REST API version control. Supported minor versions are 196.0 or later. To use this field in the method, you must set the &#x60;zuora-version&#x60; field to the minor version number in the request header. See [Zuora REST API Versions](https://knowledgecenter.zuora.com/DC_Developers/REST_API/A_REST_basics#Zuora_REST_API_Versions) for more information. | [optional] 
**contract_effective_date** | [**\DateTime**](Date.md) | The date when the customer notifies you that they want to amend their subscription. | [optional] 
**extends_term** | **bool** | Whether to extend the subscription term by the length of time the suspension is in effect. Values: &#x60;true&#x60;, &#x60;false&#x60;. | [optional] 
**invoice** | **bool** | Creates an invoice for a subscription. The invoice generated in this operation is only for this subscription, not for the entire customer account.  If the value is &#x60;true&#x60;, an invoice is created. If the value is &#x60;false&#x60;, no action is taken. The default value is &#x60;false&#x60;.   **Note:** This field is in Zuora REST API version control. Supported minor versions are 196.0 or later. To use this field in the method, you must set the &#x60;zuora-version&#x60; field to the minor version number in the request header. See [Zuora REST API Versions](https://knowledgecenter.zuora.com/DC_Developers/REST_API/A_REST_basics#Zuora_REST_API_Versions) for more information. | [optional] 
**invoice_collect** | **bool** | **Note:** This field has been replaced by the &#x60;invoice&#x60; field and the &#x60;collect&#x60; field. &#x60;invoiceCollect&#x60; is available only for backward compatibility.  This field is in Zuora REST API version control. Supported minor versions are 186.0, 187.0, 188.0, 189.0, and 196.0. See [Zuora REST API Versions](https://knowledgecenter.zuora.com/DC_Developers/REST_API/A_REST_basics#Zuora_REST_API_Versions) for more information. | [optional] 
**invoice_target_date** | [**\DateTime**](Date.md) | If an invoice is to be generated, the date through which to calculate the charges, as yyyy-mm-dd. | [optional] 
**resume** | **bool** | Whether to set when to resume a subscription when creating a suspend amendment. Values: &#x60;true&#x60;, &#x60;false&#x60;. | [optional] 
**resume_periods** | **string** | The length of the period used to specify when the subscription is resumed. The subscription resumption takes effect after a specified period based on the suspend date or today&#39;s date. You must use this field together with the &#x60;resumePeriodsType&#x60; field to specify the period.  **Note:** This field is only applicable when the &#x60;suspendPolicy&#x60; field is set to &#x60;FixedPeriodsFromToday&#x60; or &#x60;FixedPeriodsFromSuspendDate&#x60;. | [optional] 
**resume_periods_type** | **string** | The period type used to define when the subscription resumption takes effect. The subscription resumption takes effect after a specified period based on the suspend date or today&#39;s date. You must use this field together with the resumePeriods field to specify the period.  Values: &#x60;Day&#x60;, &#x60;Week&#x60;, &#x60;Month&#x60;, &#x60;Year&#x60;  **Note:** This field is only applicable when the &#x60;suspendPolicy&#x60; field is set to &#x60;FixedPeriodsFromToday&#x60; or &#x60;FixedPeriodsFromSuspendDate&#x60;. | [optional] 
**resume_policy** | **string** | Resume methods. Specify a way to resume a subscription. See [Resume Date](https://knowledgecenter.zuora.com/BC_Subscription_Management/Subscriptions/Resume_a_Subscription#Resume_Date) for more information.  Values:  * &#x60;Today&#x60;: The subscription resumption takes effect on today&#39;s date.  * &#x60;FixedPeriodsFromSuspendDate&#x60;: The subscription resumption takes effect after a specified period based on the suspend date. You must specify the &#x60;resumePeriods&#x60; and &#x60;resumePeriodsType&#x60; fields to define the period.  * &#x60;SpecificDate&#x60;: The subscription resumption takes effect on a specific date. You must define the specific date in the &#x60;resumeSpecificDate&#x60; field.  * &#x60;FixedPeriodsFromToday&#x60;: The subscription resumption takes effect after a specified period based on the today&#39;s date. You must specify the &#x60;resumePeriods&#x60; and &#x60;resumePeriodsType&#x60; fields to define the period. | [optional] 
**resume_specific_date** | [**\DateTime**](Date.md) | A specific date when the subscription resumption takes effect, in the format yyyy-mm-dd.  **Note:** This field is only applicable only when the &#x60;resumePolicy&#x60; field is set to &#x60;SpecificDate&#x60;.  The value should not be earlier than the subscription suspension date. | [optional] 
**suspend_periods** | **string** | The length of the period used to specify when the subscription suspension takes effect. The subscription suspension takes effect after a specified period based on today&#39;s date. You must use this field together with the &#x60;suspendPeriodsType&#x60; field to specify the period.  **Note:** This field is only applicable only when the suspendPolicy field is set to FixedPeriodsFromToday. | [optional] 
**suspend_periods_type** | **string** | The period type used to define when the subscription suspension takes effect. The subscription suspension takes effect after a specified period based on today&#39;s date. You must use this field together with the suspendPeriods field to specify the period.  Type: string (enum)  Values: &#x60;Day&#x60;, &#x60;Week&#x60;, &#x60;Month&#x60;, &#x60;Year&#x60;  **Note:** This field is only applicable only when the suspendPolicy field is set to FixedPeriodsFromToday. | [optional] 
**suspend_policy** | **string** | Suspend methods. Specify a way to suspend a subscription. See [Suspend Date](https://knowledgecenter.zuora.com/BC_Subscription_Management/Subscriptions/Suspend_a_Subscription#Suspend_Date) for more information.  Value:  * &#x60;Today&#x60;: The subscription suspension takes effect on today&#39;s date. * &#x60;EndOfLastInvoicePeriod&#x60;: The subscription suspension takes effect at the end of the last invoice period. The suspend date defaults to a date that is one day after the last invoiced period. You can choose this option to avoid any negative invoices (credits) issued back to the customer after the subscription suspension.  * &#x60;SpecificDate&#x60;: The subscription suspension takes effect on a specific date. You must define the specific date in the &#x60;suspendSpecificDate&#x60; field. * &#x60;FixedPeriodsFromToday&#x60;: The subscription suspension takes effect after a specified period based on today&#39;s date. You must specify the &#x60;suspendPeriods&#x60; and &#x60;suspendPeriodsType&#x60; fields to define the period. | 
**suspend_specific_date** | [**\DateTime**](Date.md) | A specific date when the subscription suspension takes effect, in the format yyyy-mm-dd.  **Note:** This field is only applicable only when the suspendPolicy field is set to SpecificDate.  The value should not be earlier than the subscription contract effective date, later than the subscription term end date, or within a period for which the customer has been invoiced. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


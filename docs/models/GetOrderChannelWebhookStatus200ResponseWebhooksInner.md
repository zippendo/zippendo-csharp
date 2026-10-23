# Zippendo.Model.GetOrderChannelWebhookStatus200ResponseWebhooksInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **decimal** | Platform webhook ID. | 
**Topic** | **string** | Webhook event topic. | 
**Address** | **string** | Registered callback address. | 
**CreatedAt** | **string** | Webhook creation timestamp. | 
**DeliveryUrl** | **string** | WooCommerce delivery URL (same as &#x60;address&#x60;; present for WooCommerce channels). | [optional] 
**Status** | **string** | WooCommerce webhook status. A value other than &#x60;active&#x60; means WooCommerce disabled the webhook (e.g. after repeated delivery failures). | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)


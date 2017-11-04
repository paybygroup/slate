---
title: Pay By Group Merchant API v1.0
language_tabs: []
toc_footers: []
includes: []
search: true
highlight_theme: darkula
headingLevel: 2
---

# Pay By Group Merchant API v1.0

> Scroll down for example requests and responses.

This is the Pay By Group API for merchant integrations

Base URLs:

* <a href="https://api.paybygroup.com/">https://api.paybygroup.com/</a>

* <a href="https://api-test.paybygroup.com/">https://api-test.paybygroup.com/</a>



Email: <a href="mailto:dev@paybygroup.com">Pay By Group</a> 

# Authentication





# purchases

Operations on Purchase objects.

## RetrieveMerchantPurchases

`GET /purchases`

*Retrieve list of all purchases under a merchant*

> Example responses

```json
[
  {
    "id": "string",
    "slug": "string",
    "merchant": {
      "id": "string",
      "unique_name": "string",
      "display_name": "string",
      "support_email": "user@example.com",
      "support_phone": "string",
      "logo_url": "string",
      "defaults": {
        "currency_code": "string",
        "language_code": "string",
        "timezone_code": "string",
        "product_image_url": "string"
      }
    },
    "status": "created",
    "refund_status": "none",
    "processing_refund": true,
    "tipped": true,
    "auto_pilot_enabled": true,
    "auto_pilot_trigger_slots": 0,
    "consumer_fields": [
      {
        "name": "string",
        "label": "string",
        "description": "string",
        "type": "text",
        "settings": {},
        "scope": "member",
        "default_value": "string"
      }
    ],
    "consumer_field_values": [
      {
        "name": "string",
        "scope": "member",
        "required": true
      }
    ],
    "consumer_field_schemas": [
      {
        "id": "string",
        "name": "string",
        "label": "string",
        "scope": "member",
        "required": true,
        "type": "text"
      }
    ],
    "has_consumer_field_schemas": true,
    "currency_code": "string",
    "payment_destination_id": "string",
    "currency_config": {
      "supported_payment_sources": [
        {
          "type": "credit_card",
          "unsupported_cards": [
            "string"
          ]
        }
      ]
    },
    "payments": [
      {
        "id": "string",
        "status": "pending",
        "number": 0,
        "percentage": 1,
        "due_deadline": "2017-11-03T23:44:19Z",
        "paid_at": "2017-11-03T23:44:19Z",
        "accepted_at": "2017-11-03T23:44:19Z",
        "submitted_at": "2017-11-03T23:44:19Z",
        "amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "conversion_rate": 0,
        "processing_currency": "string",
        "failed": true,
        "payout_failed": true
      }
    ],
    "current_payment": {
      "id": "string",
      "status": "pending",
      "number": 0,
      "percentage": 1,
      "due_deadline": "2017-11-03T23:44:19Z",
      "paid_at": "2017-11-03T23:44:19Z",
      "accepted_at": "2017-11-03T23:44:19Z",
      "submitted_at": "2017-11-03T23:44:19Z",
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "conversion_rate": 0,
      "processing_currency": "string",
      "failed": true,
      "payout_failed": true
    },
    "next_payment_due_deadline": "2017-11-03T23:44:19Z",
    "cost_range": [
      {
        "amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "min_slots": 0,
        "max_slots": 0
      }
    ],
    "current_product_cost_amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "current_total_cost_amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "max_product_cost_by_slots": {
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "min_slots": 0,
      "max_slots": 0
    },
    "min_product_cost_by_slots": {
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "min_slots": 0,
      "max_slots": 0
    },
    "max_product_cost_by_amount": {
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "min_slots": 0,
      "max_slots": 0
    },
    "fees_structure": {
      "currency_code": "string",
      "payment_destination_type": "bank_account",
      "consumer_fees": {
        "per_share": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "per_share_max": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "per_share_min": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "percentage": 1
      },
      "merchant_service_fees": {
        "per_share": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "per_purchase_max": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "percentage": 1
      },
      "merchant_processing_fees": {
        "per_transaction": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "percentage": 1
      }
    },
    "apply_consumer_fee_to_organizer": true,
    "product": {
      "images": [
        {
          "name": "string",
          "version": "string",
          "url": "string"
        }
      ],
      "default_image_url": "string",
      "allowed_split_types": "even_split",
      "cost_type": "total",
      "costs": [
        {
          "amount": {
            "amount_cents": 0,
            "currency_code": "string"
          },
          "min_slots": 0,
          "max_slots": 0
        }
      ],
      "description": "string",
      "name": "string",
      "end_datetime": "2017-11-03T23:44:19Z",
      "start_datetime": "2017-11-03T23:44:19Z",
      "external_purchase_id": "string",
      "inventory_id": "string",
      "link": "string",
      "max_slots": 0,
      "min_slots": 0,
      "legal_documents": [
        {
          "id": "string",
          "type": "tos",
          "title": "string",
          "content": "string",
          "created_at": "2017-11-03T23:44:19Z",
          "updated_at": "2017-11-03T23:44:19Z"
        }
      ]
    },
    "group": {
      "commit_deadline": "2017-11-03T23:44:19Z",
      "max_slots": 0,
      "min_slots": 0,
      "min_contribution": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "organizer_email": "user@example.com",
      "organizer_full_name": "string",
      "legal_document_ids": [
        "string"
      ],
      "split_type": "even_split"
    },
    "memberships": [
      {
        "id": "string",
        "status": "holdout",
        "refund_status": "none",
        "failed": true,
        "short": true,
        "role": "organizer",
        "claimed_slots": 0,
        "opt_in_marketing": true,
        "amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "share_amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "fees": {
          "consumer_fee": {
            "amount_cents": 0,
            "currency_code": "string"
          },
          "merchant_service_fee": {
            "amount_cents": 0,
            "currency_code": "string"
          }
        },
        "consumer_field_values": {
          "name": "string",
          "scope": "member",
          "required": true
        },
        "allowed_amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "allowed_share_amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "allowed_fees": {
          "consumer_fee": {
            "amount_cents": 0,
            "currency_code": "string"
          },
          "merchant_service_fee": {
            "amount_cents": 0,
            "currency_code": "string"
          }
        },
        "max_amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "max_share_amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "max_fees": {
          "consumer_fee": {
            "amount_cents": 0,
            "currency_code": "string"
          },
          "merchant_service_fee": {
            "amount_cents": 0,
            "currency_code": "string"
          }
        },
        "collected_amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "collected_share_amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "current_contribution": {
          "id": "string",
          "status": "created",
          "refund_status": "none",
          "amount": {
            "amount_cents": 0,
            "currency_code": "string"
          },
          "share_amount": {
            "amount_cents": 0,
            "currency_code": "string"
          },
          "fees": {
            "consumer_fee": {
              "amount_cents": 0,
              "currency_code": "string"
            },
            "merchant_service_fee": {
              "amount_cents": 0,
              "currency_code": "string"
            }
          },
          "charged_at": "2017-11-03T23:44:19Z",
          "failed_at": "2017-11-03T23:44:19Z",
          "created_at": "string"
        },
        "user": {
          "id": "string",
          "email": "user@example.com",
          "full_name": "string",
          "first_name": "string",
          "last_name": "string",
          "avatar_url": "string",
          "language_code": "string",
          "created_at": "string"
        },
        "purchase_id": "string",
        "payment_source": {
          "id": "string",
          "name": "string",
          "type": "string",
          "info": {
            "account_name": "string",
            "account_number": "string",
            "account_holder_type": "string"
          },
          "created_at": "2017-11-03T23:44:19Z"
        },
        "committed_at": "2017-11-03T23:44:19Z",
        "created_at": "2017-11-03T23:44:19Z"
      }
    ],
    "collected_shares_amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "committed_shares_amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "committed_slots": 0,
    "needed_amount_to_current_payment": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "needed_slots_to_min": 0,
    "product_or_group_max_slots": 0,
    "product_or_group_min_slots": 0,
    "language_code": "string",
    "created_at": "2017-11-03T23:44:19Z"
  }
]
```
<h3 id="RetrieveMerchantPurchases-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success response.|Inline

<h3 id="RetrieveMerchantPurchases-responseschema">Response Schema</h3>

Status Code **200**

Name|Type|Required|Description
---|---|---|---|---|
anonymous|[[Purchase](#schemapurchase)]|false|No description
» id|string(uuid)|false|Pay By Group UUID for this Purchase used for API calls
» slug|string|false|Short, unique identifier of this Purchase for easy reference in the Business Portal and with end users 
» merchant|[Merchant](#schemamerchant)|false|No description
»» id|string(uuid)|false|Unique ID for the merchant.
»» unique_name|string|false|Unique Pay By Group-assigned slug to identify this merchant
»» display_name|string|false|Display name chosen by merchant for end users to see
»» support_email|string(email)|false|Email provided for end users to contant the merchant
»» support_phone|string|false|Phone provided for end users to contant the merchant
»» logo_url|string|false|Logo provided by the merchant for display to end users
»» defaults|[MerchantDefaults](#schemamerchantdefaults)|false|No description
»»» currency_code|string|false|Default currency code for this merchant, which applies to new purchases where a currency is not specified 
»»» language_code|string|false|Default language for this merchant, which applies to new purchases where a default language is not specified 
»»» timezone_code|string|false|Default timezone code for this merchant, which applies to new datetimes created under the merchant's purchases where a time is not specified. 
»»» product_image_url|string|false|URL of the default image for this merchant, which applies to new purchases where a purchase image is not specified. 
» status|string|false|Current status of the purchase. One of: - created Purchase has been created by the Merchant. - active Purchase has been claimed by an organizer and is in process. - completed All payments have been successfully paid out to the Merchant for this Purchase. - canceled The Purchase has been canceled by the merchant or organizer and is not recoverable. 
» refund_status|string|false|Status that determines whether the Purchase is partially or fully refunded. One of: - none None of the Purchase's Memberships were refunded. - partial Some of the Purchase's Memberships were partially or fully refunded. - full All of the Purchase's Memberships were fully refunded. 
» processing_refund|boolean|false|Determines whether or not a refund is being processed for the purchase.
» tipped|boolean|false|The minimum required slots have been claimed for the organizer to submit payment
» auto_pilot_enabled|boolean|false|The organizer has chosen to have payments triggered automatically as soon as the trigger_slots level they set is reached 
» auto_pilot_trigger_slots|integer(int32)|false|The number of slots set by the organizer, which when reached, will automatically trigger payment submission 
» has_consumer_field_schemas|boolean|false|Whether or not this purchase has any consumer field schema declared.
» currency_code|string|false|3-letter currency code for all money values related to the Purchase
» payment_destination_id|string(uuid)|false|ID of the payment destination that will receive all future payments made under this Purchase.
» currency_config|object|false|All unsupported payment source types by this Purchase's payment destination, which members cannot use for their contributions 
»» supported_payment_sources|[object]|false|List of supported payment sources based on the currency of this Purchase
»»» type|string|false|Type of the supported payment source
»»» unsupported_cards|[string]|false|List of unsupported credit cards for this particular payment source.
» current_payment|[Payment](#schemapayment)|false|No description
»» id|string(uuid)|false|Pay By Group UUID for this payment
»» status|string|false|One of: - pending A planned future payment on the purchase. - active The currently active, next payment to be paid on the purchase - authorizing The constituent contributions that comprise this   payment are in the process of having their funds verified. - authorized All funds have been verified for this payment and it   awaits acceptance by the merchant. - captured All funds have been taken from group members for the   purchase and are awaiting payout to the merchant. - processing_payout The payout to the merchant is in process. - canceled This payment has been canceled. - paid All funds are paid out to the Payout Account. 
»» number|integer(int32)|false|Number of this payment in the overall sequence of the purchase. It is 0 if the purchase has only 1 payment. 
»» percentage|integer(int32)|false|Percent of the total purchase cost due for this payment, which must be an integer. All payments on a purchase must sum to 100. 
»» due_deadline|string(date-time)|false|Datetime by when this payment must be submitted to the merchant for the purchase to be valid. It is required for all payments after the first payment but may be passed for the first, or only, payment as well. 
»» paid_at|string(date-time)|false|Timestamp when the payment is paid out to the merchant
»» accepted_at|string(date-time)|false|Timestamp when the payment is accepted by the merchant
»» submitted_at|string(date-time)|false|Timestamp when the payment is originally submitted by the organizer
»» amount|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» conversion_rate|number(float)|false|If the currency of the purchase differs from the required currency of the payment destination then this is the conversion rate used to determine the transacted amount. 
»» processing_currency|string|false|The required currency of the payment destination, which is the currency in which all transactions related to this payment occur 
»» failed|boolean|false|true if any of the contributions under this payment are currently in a failed state
»» payout_failed|boolean|false|true if the last attempt to perform a payout failed
» next_payment_due_deadline|string(date-time)|false|This is the next due deadline set by the merchant for an upcoming payment
» current_product_cost_amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» current_total_cost_amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» max_product_cost_by_slots|[ProductCost](#schemaproductcost)|false|No description
»» amount|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» min_slots|integer(int32)|false|Minimum number of slots that must be claimed by group members before the Purchase can be made at the amount specified for this range. 
»» max_slots|integer(int32)|false|Maximum allowed number of slots that may be claimed by group members at the amount specified for this range. 
» min_product_cost_by_slots|[ProductCost](#schemaproductcost)|false|No description
»» amount|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» min_slots|integer(int32)|false|Minimum number of slots that must be claimed by group members before the Purchase can be made at the amount specified for this range. 
»» max_slots|integer(int32)|false|Maximum allowed number of slots that may be claimed by group members at the amount specified for this range. 
» max_product_cost_by_amount|[ProductCost](#schemaproductcost)|false|No description
»» amount|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» min_slots|integer(int32)|false|Minimum number of slots that must be claimed by group members before the Purchase can be made at the amount specified for this range. 
»» max_slots|integer(int32)|false|Maximum allowed number of slots that may be claimed by group members at the amount specified for this range. 
» fees_structure|[PurchaseFeesStructure](#schemapurchasefeesstructure)|false|No description
»» currency_code|string|false|3-letter currency code for which this fee structure applies
»» payment_destination_type|string|false|Payment destination identifier for which this fee structure applies
»» consumer_fees|[ConsumerFeesStructure](#schemaconsumerfeesstructure)|false|No description
»»» per_share|[Money](#schemamoney)|false|No description
»»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»»» currency_code|string|false|3-letter currency code attached to every money value
»»» per_share_max|[Money](#schemamoney)|false|No description
»»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»»» currency_code|string|false|3-letter currency code attached to every money value
»»» per_share_min|[Money](#schemamoney)|false|No description
»»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»»» currency_code|string|false|3-letter currency code attached to every money value
»»» percentage|integer(int32)|false|Percentage applied to member's total share to determine fee
»» merchant_service_fees|[MerchantServiceFeesStructure](#schemamerchantservicefeesstructure)|false|No description
»»» per_share|[Money](#schemamoney)|false|No description
»»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»»» currency_code|string|false|3-letter currency code attached to every money value
»»» per_purchase_max|[Money](#schemamoney)|false|No description
»»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»»» currency_code|string|false|3-letter currency code attached to every money value
»»» percentage|integer(int32)|false|Percentage fee applied to each member's share
»» merchant_processing_fees|[MerchantProcessingFeesStructure](#schemamerchantprocessingfeesstructure)|false|No description
»»» per_transaction|[Money](#schemamoney)|false|No description
»»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»»» currency_code|string|false|3-letter currency code attached to every money value
»»» percentage|integer(int32)|false|Percentage fee for each successful transaction sent through Pay By Group
» apply_consumer_fee_to_organizer|boolean|false|Tells if consumer fee applies to the purchase's organizer
» product|[Product](#schemaproduct)|false|No description
»» default_image_url|string|false|The primary or default image for this product
»» cost_type|string|false|Cost type that determines whether the product_costs amount(s) are: - per_slot The amount is per slot claimed in the Purchase so the   total amount paid to the merchant is a function of the number of   slots claimed by group members. - total A single total amount so long as the number of slots claimed   is in the allowed range for that amount. 
»» description|string|false|Description of the product for this Purchase
»» name|string|false|Name of the product being purchased as it should be shown to end users
»» end_datetime|string(date-time)|false|End date time for the product being purchased (e.g. check-out date time, flight arrival date time, or activity ending time) 
»» start_datetime|string(date-time)|false|Start date time for the product being purchased (e.g. check-in date time, flight departure date time, or event starting time) 
»» external_purchase_id|string|false|ID supplied by the merchant that identifies this Purchase (e.g. order or booking) in the merchant's system 
»» inventory_id|string|false|Inventory ID supplied by the merchant that identifies the product being bought in this Purchase (e.g. SKU or property ID) 
»» link|string|false|Link to the product being purchased on the merchant's (or other third party's) website
»» max_slots|integer(int32)|false|The maximum possible slots allowed by the merchant based on product_costs
»» min_slots|integer(int32)|false|The minimum possible slots allowed by the merchant based on product_costs
»» images|[[Image](#schemaimage)]|false|The set of images for this product
»»» name|string|false|Filename of the image as provided by the merchant
»»» version|string|false|Version of the image generated by PBG
»»» url|string|false|No description
»» allowed_split_types|[string]|false|Array of allowed split types
»» costs|[[ProductCost](#schemaproductcost)]|false|The set of product_costs and the optional allowed range(s) of slots for each provided by the merchant 
»»» amount|[Money](#schemamoney)|false|No description
»»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»»» currency_code|string|false|3-letter currency code attached to every money value
»»» min_slots|integer(int32)|false|Minimum number of slots that must be claimed by group members before the Purchase can be made at the amount specified for this range. 
»»» max_slots|integer(int32)|false|Maximum allowed number of slots that may be claimed by group members at the amount specified for this range. 
»» legal_documents|[[LegalDocument](#schemalegaldocument)]|false|All legal documents attached to this purchase that must be agreed to by the group members
»»» id|string(uuid)|false|Pay By Group UUID of this legal document
»»» type|string|false|Specified by the merchant as either cancellation policy for cancellation and refund terms or tos for all other legal documents. 
»»» title|string|false|Mechant's title for this legal document
»»» content|string|false|Full content as provided by the merchant, either in plain text or as a URL
»»» created_at|string(date-time)|false|When this legal document was added by the merchant
»»» updated_at|string(date-time)|false|When this legal document was last updated by the merchant
» group|[Group](#schemagroup)|false|No description
»» commit_deadline|string(date-time)|false|Pay By Group-generated deadline that encourages invitees to commit to the group quickly. It auto-extends unless overriden by the merchant or organizer 
»» max_slots|integer(int32)|false|The organizer-specified value for the maximum number of slots they will allow to be claimed. It must be within the bounds allowed by the merchant. 
»» min_slots|integer(int32)|false|The organizer-specified value for the minimum number of slots they require to be claimed. It must be within the bounds allowed by the merchant. 
»» min_contribution|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» organizer_email|string(email)|false|Email of the expected organizer as provided by the merchant
»» organizer_full_name|string|false|Full name of the expected organizer as provided by the merchant
»» split_type|string|false|Splitting type chosen by the organizer for how to divide the cost among group members. One of: - even_split Only compatible with total cost_type and means the   Purchase amount is split evenly across each slot claimed. - specified_per_person Only compatible with total cost_type and   means each member may pay a different amount. - fixed_per_person Only compatible with per_slot cost_type and means   each group member pays a fixed amount per slot they claim. 
»» legal_document_ids|[string]|false|Array of legal document IDs that must be accepted by the members in this purchase
» collected_shares_amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» committed_shares_amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» committed_slots|integer(int32)|false|Sum of all slots group members have claimed in the Purchase at this point
» needed_amount_to_current_payment|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» needed_slots_to_min|integer(int32)|false|Number of slots group members must claim in order to meet the minimum required to submit the current payment 
» product_or_group_max_slots|integer(int32)|false|The active minimum number of slots that must be claimed based on the parameters set by the merchant and organizer 
» product_or_group_min_slots|integer(int32)|false|The active maximum number of slots that are allowed to be claimed based on the parameters set by the merchant and organizer 
» language_code|string|false|Default language for this purchase. It is going to be used in the claim and commit steps; and as one of the fallbacks when detecting what language to show to the user 
» created_at|string(date-time)|false|Timestamp of when the Purchase was first created by the merchant
» consumer_fields|[[ConsumerField](#schemaconsumerfield)]|false|Array of consumer fields for this Purchase
»» name|string|false|No description
»» label|string|false|No description
»» description|string|false|No description
»» type|string|false|No description
»» settings|object|false|No description
»» scope|string|false|No description
»» default_value|string|false|No description
» consumer_field_values|[[ConsumerFieldValue](#schemaconsumerfieldvalue)]|false|Array of values for each of the consumer fields defined.
»» name|string|false|Name of the schema
»» scope|string|false|One of member or purchase.
»» required|boolean|false|Whether the schema field should be required or not.
» consumer_field_schemas|[[ConsumerFieldSchema](#schemaconsumerfieldschema)]|false|List of consumer field schemas to use for the purchase
»» id|string(uuid)|false|No description
»» name|string|false|No description
»» label|string|false|No description
»» scope|string|false|Any of member or purchase.
»» required|boolean|false|Whether the field for this schema should be required or not.
»» type|string|false|No description
» payments|[[Payment](#schemapayment)]|false|Full payment schedule as set by the merchant for this Purchase
»» id|string(uuid)|false|Pay By Group UUID for this payment
»» status|string|false|One of: - pending A planned future payment on the purchase. - active The currently active, next payment to be paid on the purchase - authorizing The constituent contributions that comprise this   payment are in the process of having their funds verified. - authorized All funds have been verified for this payment and it   awaits acceptance by the merchant. - captured All funds have been taken from group members for the   purchase and are awaiting payout to the merchant. - processing_payout The payout to the merchant is in process. - canceled This payment has been canceled. - paid All funds are paid out to the Payout Account. 
»» number|integer(int32)|false|Number of this payment in the overall sequence of the purchase. It is 0 if the purchase has only 1 payment. 
»» percentage|integer(int32)|false|Percent of the total purchase cost due for this payment, which must be an integer. All payments on a purchase must sum to 100. 
»» due_deadline|string(date-time)|false|Datetime by when this payment must be submitted to the merchant for the purchase to be valid. It is required for all payments after the first payment but may be passed for the first, or only, payment as well. 
»» paid_at|string(date-time)|false|Timestamp when the payment is paid out to the merchant
»» accepted_at|string(date-time)|false|Timestamp when the payment is accepted by the merchant
»» submitted_at|string(date-time)|false|Timestamp when the payment is originally submitted by the organizer
»» amount|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» conversion_rate|number(float)|false|If the currency of the purchase differs from the required currency of the payment destination then this is the conversion rate used to determine the transacted amount. 
»» processing_currency|string|false|The required currency of the payment destination, which is the currency in which all transactions related to this payment occur 
»» failed|boolean|false|true if any of the contributions under this payment are currently in a failed state
»» payout_failed|boolean|false|true if the last attempt to perform a payout failed
» cost_range|[[ProductCost](#schemaproductcost)]|false|The range of possible costs for this product based on the product_costs merchant provides
»» amount|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» min_slots|integer(int32)|false|Minimum number of slots that must be claimed by group members before the Purchase can be made at the amount specified for this range. 
»» max_slots|integer(int32)|false|Maximum allowed number of slots that may be claimed by group members at the amount specified for this range. 
» memberships|[[Membership](#schemamembership)]|false|Array that includes all members in this Purchase without their contributions.
»» id|string|false|Pay By Group UUID for this membership
»» status|string|false|One of: - holdout (user has been invited but not joined the group); - committed (user has joined the group and whether they have been charged is in the contribution object); 
»» refund_status|string|false|Status that determines whether the Membership is partially or fully refunded. One of: - none (none of the Membership's Contributions were refunded). - partial (some of the Membership's Contributions were partially   or fully refunded). - full (all of the Membership's Contributions were fully refunded). 
»» failed|boolean|false|User is currently in the group with a failed payment method, which is preventing the purchase from completing 
»» short|boolean|false|The user is currently in the group but has not agreed to pay their new required share amount due to updates to the purchase. 
»» role|string|false|Either organizer or invitee
»» claimed_slots|integer(int32)|false|Number of slots the member has claimed in the group. Defaults to 1 if none is selected by the user.
»» opt_in_marketing|boolean|false|true if the user has opted in to receive marketing communication from the merchant. Otherwise false.
»» amount|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» share_amount|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» fees|[Fees](#schemafees)|false|No description
»»» consumer_fee|[Money](#schemamoney)|false|No description
»»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»»» currency_code|string|false|3-letter currency code attached to every money value
»»» merchant_service_fee|[Money](#schemamoney)|false|No description
»»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»»» currency_code|string|false|3-letter currency code attached to every money value
»» consumer_field_values|[ConsumerFieldValue](#schemaconsumerfieldvalue)|false|No description
»»» name|string|false|Name of the schema
»»» scope|string|false|One of member or purchase.
»»» required|boolean|false|Whether the schema field should be required or not.
»» allowed_amount|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» allowed_share_amount|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» allowed_fees|[Fees](#schemafees)|false|No description
»»» consumer_fee|[Money](#schemamoney)|false|No description
»»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»»» currency_code|string|false|3-letter currency code attached to every money value
»»» merchant_service_fee|[Money](#schemamoney)|false|No description
»»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»»» currency_code|string|false|3-letter currency code attached to every money value
»» max_amount|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» max_share_amount|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» max_fees|[Fees](#schemafees)|false|No description
»»» consumer_fee|[Money](#schemamoney)|false|No description
»»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»»» currency_code|string|false|3-letter currency code attached to every money value
»»» merchant_service_fee|[Money](#schemamoney)|false|No description
»»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»»» currency_code|string|false|3-letter currency code attached to every money value
»» collected_amount|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» collected_share_amount|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» current_contribution|[Contribution](#schemacontribution)|false|No description
»»» id|string|false|UUID of this contribution
»»» status|string|false|Current status of the contribution, any of created, authorized, captured, holdout or failed
»»» refund_status|string|false|Status that determines whether the Contribution is partially or fully refunded. One of: - none (none of the Contribution's Transactions were refunded). - partial (some of the Contribution's Transactions were partially   or fully refunded). - full (all of the Contribution's Transactions were fully refunded). 
»»» amount|[Money](#schemamoney)|false|No description
»»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»»» currency_code|string|false|3-letter currency code attached to every money value
»»» share_amount|[Money](#schemamoney)|false|No description
»»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»»» currency_code|string|false|3-letter currency code attached to every money value
»»» fees|[Fees](#schemafees)|false|No description
»»»» consumer_fee|[Money](#schemamoney)|false|No description
»»»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»»»» currency_code|string|false|3-letter currency code attached to every money value
»»»» merchant_service_fee|[Money](#schemamoney)|false|No description
»»»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»»»» currency_code|string|false|3-letter currency code attached to every money value
»»» charged_at|string(date-time)|false|Timestamp of when this contibution was charged
»»» failed_at|string(date-time)|false|Timestamp of when this contribution most recently failed
»»» created_at|string|false|Timestamp when the record of this contribution was first created, which is not necessarily when it was charged 
»» user|[User](#schemauser)|false|No description
»»» id|string(uuid)|false|Pay By Group UUID for this user
»»» email|string(email)|false|User's email address
»»» full_name|string|false|User's full name
»»» first_name|string|false|User's first name
»»» last_name|string|false|User's last name
»»» avatar_url|string|false|URL of the User's avatar
»»» language_code|string|false|The preferred language selected by this user
»»» created_at|string(uuid)|false|No description
»» purchase_id|string(uuid)|false|Pay By Group slug of the purchase to which this membership is tied
»» payment_source|[PaymentSource](#schemapaymentsource)|false|No description
»»» id|string(uuid)|false|Pay By Group UUID of this payment source
»»» name|string|false|Full name of this payment source's owner
»»» type|string|false|Describes the type of payment source, any of credit_card or bank_account
»»» info|object|false|Bank account information of this payment source
»»»» account_name|string|false|Listed name of the account holder
»»»» account_number|string|false|Account number
»»»» account_holder_type|string|false|Either a business or individual
»»» created_at|string(date-time)|false|Timestamp when the payment source was first added to the system
»» committed_at|string(date-time)|false|Timestamp of when the member agreed to pay into the purchase
»» created_at|string(date-time)|false|When the membership was first created



<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
http
</aside>

## CreatePurchase

`POST /purchases`

*Create a purchase*

Creates a new purchase and returns a slug, which you can use to redirect an end user to their group's hub page, or you can proceed to use PATCH /purchases/:id/claim if you want to fully embed the experience.

> Body parameter

```json
{
  "product": {
    "name": "Trip to Las Vegas!",
    "cost_type": "total",
    "description": "We're going to Las Vegas.",
    "default_image_url": "https://example.com/image.jpg",
    "inventory_id": "SKU-1234",
    "link": "https://mycompany.com/product/sku-1234/details",
    "start_datetime": "2018-11-03T14:57:54Z",
    "end_datetime": "2018-12-03T14:57:54Z",
    "external_purchase_id": "https://mycompany.com/order/1234",
    "costs": [
      {
        "amount": {
          "amount_cents": 10000,
          "currency_code": "USD"
        },
        "min_slots": 1,
        "max_slots": 3
      },
      {
        "amount": {
          "amount_cents": 20000,
          "currency_code": "USD"
        },
        "min_slots": 4
      }
    ]
  },
  "group": {
    "organizer_full_name": "John Doe",
    "organizer_email": "john@example.com",
    "legal_document_ids": [
      "03DEFD52-E46C-42CF-BD88-A61EB5A61BB5"
    ]
  },
  "payments": [
    {
      "percentage": 30
    },
    {
      "percentage": 70,
      "due_deadline": "2018-10-03T14:57:54Z"
    }
  ],
  "language_code": "es"
}
```
<h3 id="CreatePurchase-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
body|body|object|true|No description
» product|body|object|false|No description
»» name|body|string|false|Name of the product being purchased as it should be shown to end users
»» cost_type|body|string|false|Cost type that determines whether the product_costs amount(s) are:
»» description|body|string|false|Description of the product for this Purchase
»» default_image_url|body|string|false|The primary or default image for this product
»» inventory_id|body|string|false|Inventory ID supplied by the merchant that identifies the product
»» link|body|string|false|Link to the product being purchased on the merchant's (or other third party's) website
»» start_datetime|body|string(date-time)|false|Start date time for the product being purchased
»» end_datetime|body|string(date-time)|false|End date time for the product being purchased
»» external_purchase_id|body|string|false|ID supplied by the merchant that identifies this Purchase
»» costs|body|[[ProductCost](#schemaproductcost)]|false|The set of product_costs and the optional allowed range(s) of slots
» group|body|object|false|No description
»» organizer_full_name|body|string|false|Full name of the expected organizer as provided by the merchant
»» organizer_email|body|string(email)|false|Email of the expected organizer as provided by the merchant
»» legal_document_ids|body|[string]|false|Array of legal document IDs that must be accepted by the members in this purchase
» language_code|body|string|false|Default language for this purchase. It is going to be used in the
» payment_destination_id|body|string(uuid)|false|ID of the payment destination that will receive all future payments
» payments|body|[object]|false|No description
»» percentage|body|integer(int32)|true|Percent of the total purchase cost due for this payment, which must
»» due_deadline|body|string(date-time)|false|Datetime by when this payment must be submitted to the merchant for
» consumer_field_schemas|body|[object]|false|No description
»» name|body|string|false|No description
»» scope|body|string|false|Any of member or purchase.
»» required|body|boolean|false|Whether the field for this schema should be required or not.


#### Enumerated Values

|Parameter|Value|
|---|---|
»» cost_type|total|
»» cost_type|per_slot|
»» scope|member|
»» scope|purchase|

##### »» cost_type
Cost type that determines whether the product_costs amount(s) are:
- per_slot The amount is per slot claimed in the Purchase so the
  total amount paid to the merchant is a function of the number of
  slots claimed by group members.
- total A single total amount so long as the number of slots claimed
  is in the allowed range for that amount.

##### »» inventory_id
Inventory ID supplied by the merchant that identifies the product
being bought in this Purchase (e.g. SKU or property ID)

##### »» start_datetime
Start date time for the product being purchased
(e.g. check-in date time, flight departure date time, or event
starting time)

##### »» end_datetime
End date time for the product being purchased
(e.g. check-out date time, flight arrival date time, or activity
ending time)

##### »» external_purchase_id
ID supplied by the merchant that identifies this Purchase
(e.g. order or booking) in the merchant's system

##### »» costs
The set of product_costs and the optional allowed range(s) of slots
for each provided by the merchant

##### » language_code
Default language for this purchase. It is going to be used in the
claim and commit steps; and as one of the fallbacks when detecting
what language to show to the user

##### » payment_destination_id
ID of the payment destination that will receive all future payments
made under this Purchase.

##### »» percentage
Percent of the total purchase cost due for this payment, which must
be an integer. All payments on a purchase must sum to 100.

##### »» due_deadline
Datetime by when this payment must be submitted to the merchant for
the purchase to be valid.
It is required for all payments after the first payment but may be
passed for the first, or only, payment as well.

> Example responses

```json
{
  "id": "string",
  "slug": "string",
  "merchant": {
    "id": "string",
    "unique_name": "string",
    "display_name": "string",
    "support_email": "user@example.com",
    "support_phone": "string",
    "logo_url": "string",
    "defaults": {
      "currency_code": "string",
      "language_code": "string",
      "timezone_code": "string",
      "product_image_url": "string"
    }
  },
  "status": "created",
  "refund_status": "none",
  "processing_refund": true,
  "tipped": true,
  "auto_pilot_enabled": true,
  "auto_pilot_trigger_slots": 0,
  "consumer_fields": [
    {
      "name": "string",
      "label": "string",
      "description": "string",
      "type": "text",
      "settings": {},
      "scope": "member",
      "default_value": "string"
    }
  ],
  "consumer_field_values": [
    {
      "name": "string",
      "scope": "member",
      "required": true
    }
  ],
  "consumer_field_schemas": [
    {
      "id": "string",
      "name": "string",
      "label": "string",
      "scope": "member",
      "required": true,
      "type": "text"
    }
  ],
  "has_consumer_field_schemas": true,
  "currency_code": "string",
  "payment_destination_id": "string",
  "currency_config": {
    "supported_payment_sources": [
      {
        "type": "credit_card",
        "unsupported_cards": [
          "string"
        ]
      }
    ]
  },
  "payments": [
    {
      "id": "string",
      "status": "pending",
      "number": 0,
      "percentage": 1,
      "due_deadline": "2017-11-03T23:44:19Z",
      "paid_at": "2017-11-03T23:44:19Z",
      "accepted_at": "2017-11-03T23:44:19Z",
      "submitted_at": "2017-11-03T23:44:19Z",
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "conversion_rate": 0,
      "processing_currency": "string",
      "failed": true,
      "payout_failed": true
    }
  ],
  "current_payment": {
    "id": "string",
    "status": "pending",
    "number": 0,
    "percentage": 1,
    "due_deadline": "2017-11-03T23:44:19Z",
    "paid_at": "2017-11-03T23:44:19Z",
    "accepted_at": "2017-11-03T23:44:19Z",
    "submitted_at": "2017-11-03T23:44:19Z",
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "conversion_rate": 0,
    "processing_currency": "string",
    "failed": true,
    "payout_failed": true
  },
  "next_payment_due_deadline": "2017-11-03T23:44:19Z",
  "cost_range": [
    {
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "min_slots": 0,
      "max_slots": 0
    }
  ],
  "current_product_cost_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "current_total_cost_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "max_product_cost_by_slots": {
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "min_slots": 0,
    "max_slots": 0
  },
  "min_product_cost_by_slots": {
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "min_slots": 0,
    "max_slots": 0
  },
  "max_product_cost_by_amount": {
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "min_slots": 0,
    "max_slots": 0
  },
  "fees_structure": {
    "currency_code": "string",
    "payment_destination_type": "bank_account",
    "consumer_fees": {
      "per_share": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "per_share_max": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "per_share_min": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "percentage": 1
    },
    "merchant_service_fees": {
      "per_share": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "per_purchase_max": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "percentage": 1
    },
    "merchant_processing_fees": {
      "per_transaction": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "percentage": 1
    }
  },
  "apply_consumer_fee_to_organizer": true,
  "product": {
    "images": [
      {
        "name": "string",
        "version": "string",
        "url": "string"
      }
    ],
    "default_image_url": "string",
    "allowed_split_types": "even_split",
    "cost_type": "total",
    "costs": [
      {
        "amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "min_slots": 0,
        "max_slots": 0
      }
    ],
    "description": "string",
    "name": "string",
    "end_datetime": "2017-11-03T23:44:19Z",
    "start_datetime": "2017-11-03T23:44:19Z",
    "external_purchase_id": "string",
    "inventory_id": "string",
    "link": "string",
    "max_slots": 0,
    "min_slots": 0,
    "legal_documents": [
      {
        "id": "string",
        "type": "tos",
        "title": "string",
        "content": "string",
        "created_at": "2017-11-03T23:44:19Z",
        "updated_at": "2017-11-03T23:44:19Z"
      }
    ]
  },
  "group": {
    "commit_deadline": "2017-11-03T23:44:19Z",
    "max_slots": 0,
    "min_slots": 0,
    "min_contribution": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "organizer_email": "user@example.com",
    "organizer_full_name": "string",
    "legal_document_ids": [
      "string"
    ],
    "split_type": "even_split"
  },
  "memberships": [
    {
      "id": "string",
      "status": "holdout",
      "refund_status": "none",
      "failed": true,
      "short": true,
      "role": "organizer",
      "claimed_slots": 0,
      "opt_in_marketing": true,
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "share_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "fees": {
        "consumer_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "merchant_service_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        }
      },
      "consumer_field_values": {
        "name": "string",
        "scope": "member",
        "required": true
      },
      "allowed_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "allowed_share_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "allowed_fees": {
        "consumer_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "merchant_service_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        }
      },
      "max_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "max_share_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "max_fees": {
        "consumer_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "merchant_service_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        }
      },
      "collected_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "collected_share_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "current_contribution": {
        "id": "string",
        "status": "created",
        "refund_status": "none",
        "amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "share_amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "fees": {
          "consumer_fee": {
            "amount_cents": 0,
            "currency_code": "string"
          },
          "merchant_service_fee": {
            "amount_cents": 0,
            "currency_code": "string"
          }
        },
        "charged_at": "2017-11-03T23:44:19Z",
        "failed_at": "2017-11-03T23:44:19Z",
        "created_at": "string"
      },
      "user": {
        "id": "string",
        "email": "user@example.com",
        "full_name": "string",
        "first_name": "string",
        "last_name": "string",
        "avatar_url": "string",
        "language_code": "string",
        "created_at": "string"
      },
      "purchase_id": "string",
      "payment_source": {
        "id": "string",
        "name": "string",
        "type": "string",
        "info": {
          "account_name": "string",
          "account_number": "string",
          "account_holder_type": "string"
        },
        "created_at": "2017-11-03T23:44:19Z"
      },
      "committed_at": "2017-11-03T23:44:19Z",
      "created_at": "2017-11-03T23:44:19Z"
    }
  ],
  "collected_shares_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "committed_shares_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "committed_slots": 0,
  "needed_amount_to_current_payment": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "needed_slots_to_min": 0,
  "product_or_group_max_slots": 0,
  "product_or_group_min_slots": 0,
  "language_code": "string",
  "created_at": "2017-11-03T23:44:19Z"
}
```
<h3 id="CreatePurchase-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created response.|[Purchase](#schemapurchase)

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
http
</aside>

## RetrievePurchase

`GET /purchases/{id}`

*Retrieve info for a single purchase*

You can get the current status and all details of a purchase with this endpoint.

<h3 id="RetrievePurchase-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|string(uuid)|true|Purchase ID to fetch


> Example responses

```json
{
  "id": "string",
  "slug": "string",
  "merchant": {
    "id": "string",
    "unique_name": "string",
    "display_name": "string",
    "support_email": "user@example.com",
    "support_phone": "string",
    "logo_url": "string",
    "defaults": {
      "currency_code": "string",
      "language_code": "string",
      "timezone_code": "string",
      "product_image_url": "string"
    }
  },
  "status": "created",
  "refund_status": "none",
  "processing_refund": true,
  "tipped": true,
  "auto_pilot_enabled": true,
  "auto_pilot_trigger_slots": 0,
  "consumer_fields": [
    {
      "name": "string",
      "label": "string",
      "description": "string",
      "type": "text",
      "settings": {},
      "scope": "member",
      "default_value": "string"
    }
  ],
  "consumer_field_values": [
    {
      "name": "string",
      "scope": "member",
      "required": true
    }
  ],
  "consumer_field_schemas": [
    {
      "id": "string",
      "name": "string",
      "label": "string",
      "scope": "member",
      "required": true,
      "type": "text"
    }
  ],
  "has_consumer_field_schemas": true,
  "currency_code": "string",
  "payment_destination_id": "string",
  "currency_config": {
    "supported_payment_sources": [
      {
        "type": "credit_card",
        "unsupported_cards": [
          "string"
        ]
      }
    ]
  },
  "payments": [
    {
      "id": "string",
      "status": "pending",
      "number": 0,
      "percentage": 1,
      "due_deadline": "2017-11-03T23:44:19Z",
      "paid_at": "2017-11-03T23:44:19Z",
      "accepted_at": "2017-11-03T23:44:19Z",
      "submitted_at": "2017-11-03T23:44:19Z",
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "conversion_rate": 0,
      "processing_currency": "string",
      "failed": true,
      "payout_failed": true
    }
  ],
  "current_payment": {
    "id": "string",
    "status": "pending",
    "number": 0,
    "percentage": 1,
    "due_deadline": "2017-11-03T23:44:19Z",
    "paid_at": "2017-11-03T23:44:19Z",
    "accepted_at": "2017-11-03T23:44:19Z",
    "submitted_at": "2017-11-03T23:44:19Z",
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "conversion_rate": 0,
    "processing_currency": "string",
    "failed": true,
    "payout_failed": true
  },
  "next_payment_due_deadline": "2017-11-03T23:44:19Z",
  "cost_range": [
    {
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "min_slots": 0,
      "max_slots": 0
    }
  ],
  "current_product_cost_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "current_total_cost_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "max_product_cost_by_slots": {
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "min_slots": 0,
    "max_slots": 0
  },
  "min_product_cost_by_slots": {
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "min_slots": 0,
    "max_slots": 0
  },
  "max_product_cost_by_amount": {
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "min_slots": 0,
    "max_slots": 0
  },
  "fees_structure": {
    "currency_code": "string",
    "payment_destination_type": "bank_account",
    "consumer_fees": {
      "per_share": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "per_share_max": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "per_share_min": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "percentage": 1
    },
    "merchant_service_fees": {
      "per_share": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "per_purchase_max": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "percentage": 1
    },
    "merchant_processing_fees": {
      "per_transaction": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "percentage": 1
    }
  },
  "apply_consumer_fee_to_organizer": true,
  "product": {
    "images": [
      {
        "name": "string",
        "version": "string",
        "url": "string"
      }
    ],
    "default_image_url": "string",
    "allowed_split_types": "even_split",
    "cost_type": "total",
    "costs": [
      {
        "amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "min_slots": 0,
        "max_slots": 0
      }
    ],
    "description": "string",
    "name": "string",
    "end_datetime": "2017-11-03T23:44:19Z",
    "start_datetime": "2017-11-03T23:44:19Z",
    "external_purchase_id": "string",
    "inventory_id": "string",
    "link": "string",
    "max_slots": 0,
    "min_slots": 0,
    "legal_documents": [
      {
        "id": "string",
        "type": "tos",
        "title": "string",
        "content": "string",
        "created_at": "2017-11-03T23:44:19Z",
        "updated_at": "2017-11-03T23:44:19Z"
      }
    ]
  },
  "group": {
    "commit_deadline": "2017-11-03T23:44:19Z",
    "max_slots": 0,
    "min_slots": 0,
    "min_contribution": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "organizer_email": "user@example.com",
    "organizer_full_name": "string",
    "legal_document_ids": [
      "string"
    ],
    "split_type": "even_split"
  },
  "memberships": [
    {
      "id": "string",
      "status": "holdout",
      "refund_status": "none",
      "failed": true,
      "short": true,
      "role": "organizer",
      "claimed_slots": 0,
      "opt_in_marketing": true,
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "share_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "fees": {
        "consumer_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "merchant_service_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        }
      },
      "consumer_field_values": {
        "name": "string",
        "scope": "member",
        "required": true
      },
      "allowed_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "allowed_share_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "allowed_fees": {
        "consumer_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "merchant_service_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        }
      },
      "max_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "max_share_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "max_fees": {
        "consumer_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "merchant_service_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        }
      },
      "collected_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "collected_share_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "current_contribution": {
        "id": "string",
        "status": "created",
        "refund_status": "none",
        "amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "share_amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "fees": {
          "consumer_fee": {
            "amount_cents": 0,
            "currency_code": "string"
          },
          "merchant_service_fee": {
            "amount_cents": 0,
            "currency_code": "string"
          }
        },
        "charged_at": "2017-11-03T23:44:19Z",
        "failed_at": "2017-11-03T23:44:19Z",
        "created_at": "string"
      },
      "user": {
        "id": "string",
        "email": "user@example.com",
        "full_name": "string",
        "first_name": "string",
        "last_name": "string",
        "avatar_url": "string",
        "language_code": "string",
        "created_at": "string"
      },
      "purchase_id": "string",
      "payment_source": {
        "id": "string",
        "name": "string",
        "type": "string",
        "info": {
          "account_name": "string",
          "account_number": "string",
          "account_holder_type": "string"
        },
        "created_at": "2017-11-03T23:44:19Z"
      },
      "committed_at": "2017-11-03T23:44:19Z",
      "created_at": "2017-11-03T23:44:19Z"
    }
  ],
  "collected_shares_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "committed_shares_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "committed_slots": 0,
  "needed_amount_to_current_payment": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "needed_slots_to_min": 0,
  "product_or_group_max_slots": 0,
  "product_or_group_min_slots": 0,
  "language_code": "string",
  "created_at": "2017-11-03T23:44:19Z"
}
```
```json
{
  "errors": [
    {
      "code": 0,
      "message": "string"
    }
  ]
}
```
<h3 id="RetrievePurchase-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Sucecss response.|[Purchase](#schemapurchase)
404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|[Error](#schemaerror)

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
http
</aside>

## UpdatePurchase

`PATCH /purchases/{id}`

*Update an existing purchase*

To update a purchase where the inventory is unavailable to apply to different inventory
that is available, you should change details of the in-progress group. You should also
update the purchase if other details change before it completes such as the the price,
start datetime, due deadline, etc. You can update a purchsae at any time until you accept
the last (or only) payment for that purchase. NOTE: you can never update the `cost_type`.
You can not update `payments` after you have accepted at least 1 payment, but you may still
update the `costs`.

> Body parameter

```json
{
  "language_code": "string",
  "payment_destination_id": "string",
  "product": {
    "name": "string",
    "description": "string",
    "default_image_url": "string",
    "inventory_id": "string",
    "link": "string",
    "start_datetime": "2017-11-03T23:44:19Z",
    "end_datetime": "2017-11-03T23:44:19Z",
    "external_purchase_id": "string",
    "costs": [
      {
        "amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "min_slots": 0,
        "max_slots": 0
      }
    ]
  },
  "group": {
    "organizer_full_name": "string",
    "organizer_email": "user@example.com",
    "legal_document_ids": [
      "string"
    ],
    "split_type": "even_split",
    "max_slots": 0,
    "min_slots": 0
  },
  "payments": [
    {
      "percentage": 1,
      "due_deadline": "2017-11-03T23:44:19Z"
    }
  ]
}
```
<h3 id="UpdatePurchase-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|string(uuid)|true|ID of the Purchase to update.
body|body|object|true|No description
» language_code|body|string|false|Default language for this purchase. It is going to be used in the
» payment_destination_id|body|string(uuid)|false|ID of the payment destination that will receive all future payments
» product|body|object|false|No description
»» name|body|string|false|Name of the product being purchased as it should be shown to end users
»» description|body|string|false|Description of the product for this Purchase
»» default_image_url|body|string|false|The primary or default image for this product
»» inventory_id|body|string|false|Inventory ID supplied by the merchant that identifies the product
»» link|body|string|false|Link to the product being purchased on the merchant's (or other third party's) website
»» start_datetime|body|string(date-time)|false|Start date time for the product being purchased
»» end_datetime|body|string(date-time)|false|End date time for the product being purchased
»» external_purchase_id|body|string|false|ID supplied by the merchant that identifies this Purchase
»» costs|body|[[ProductCost](#schemaproductcost)]|false|The set of product_costs and the optional allowed range(s) of slots
» group|body|object|false|No description
»» organizer_full_name|body|string|false|Full name of the expected organizer as provided by the merchant
»» organizer_email|body|string(email)|false|Email of the expected organizer as provided by the merchant
»» split_type|body|string|false|Splitting type chosen by the organizer for how to divide the cost
»» max_slots|body|integer(int32)|false|The organizer-specified value for the maximum number of slots they
»» min_slots|body|integer(int32)|false|The organizer-specified value for the minimum number of slots they
»» legal_document_ids|body|[string]|false|Array of legal document IDs that must be accepted by the members in this purchase
» payments|body|[object]|false|No description
»» percentage|body|integer(int32)|true|Percent of the total purchase cost due for this payment, which must
»» due_deadline|body|string(date-time)|false|Datetime by when this payment must be submitted to the merchant for


#### Enumerated Values

|Parameter|Value|
|---|---|
»» split_type|even_split|
»» split_type|specified_per_person|
»» split_type|fixed_per_person|

##### » language_code
Default language for this purchase. It is going to be used in the
claim and commit steps; and as one of the fallbacks when detecting
what language to show to the user

##### » payment_destination_id
ID of the payment destination that will receive all future payments
made under this Purchase.

##### »» inventory_id
Inventory ID supplied by the merchant that identifies the product
being bought in this Purchase (e.g. SKU or property ID)

##### »» start_datetime
Start date time for the product being purchased
(e.g. check-in date time, flight departure date time, or event
starting time)

##### »» end_datetime
End date time for the product being purchased
(e.g. check-out date time, flight arrival date time, or activity
ending time)

##### »» external_purchase_id
ID supplied by the merchant that identifies this Purchase
(e.g. order or booking) in the merchant's system

##### »» costs
The set of product_costs and the optional allowed range(s) of slots
for each provided by the merchant

##### »» split_type
Splitting type chosen by the organizer for how to divide the cost
among group members.
One of:
- even_split Only compatible with total cost_type and means the
  Purchase amount is split evenly across each slot claimed.
- specified_per_person Only compatible with total cost_type and
  means each member may pay a different amount.
- fixed_per_person Only compatible with per_slot cost_type and means
  each group member pays a fixed amount per slot they claim.

##### »» max_slots
The organizer-specified value for the maximum number of slots they
will allow to be claimed.
It must be within the bounds allowed by the merchant.

##### »» min_slots
The organizer-specified value for the minimum number of slots they
require to be claimed.
It must be within the bounds allowed by the merchant.

##### »» percentage
Percent of the total purchase cost due for this payment, which must
be an integer. All payments on a purchase must sum to 100.

##### »» due_deadline
Datetime by when this payment must be submitted to the merchant for
the purchase to be valid.
It is required for all payments after the first payment but may be
passed for the first, or only, payment as well.

> Example responses

```json
{
  "id": "string",
  "slug": "string",
  "merchant": {
    "id": "string",
    "unique_name": "string",
    "display_name": "string",
    "support_email": "user@example.com",
    "support_phone": "string",
    "logo_url": "string",
    "defaults": {
      "currency_code": "string",
      "language_code": "string",
      "timezone_code": "string",
      "product_image_url": "string"
    }
  },
  "status": "created",
  "refund_status": "none",
  "processing_refund": true,
  "tipped": true,
  "auto_pilot_enabled": true,
  "auto_pilot_trigger_slots": 0,
  "consumer_fields": [
    {
      "name": "string",
      "label": "string",
      "description": "string",
      "type": "text",
      "settings": {},
      "scope": "member",
      "default_value": "string"
    }
  ],
  "consumer_field_values": [
    {
      "name": "string",
      "scope": "member",
      "required": true
    }
  ],
  "consumer_field_schemas": [
    {
      "id": "string",
      "name": "string",
      "label": "string",
      "scope": "member",
      "required": true,
      "type": "text"
    }
  ],
  "has_consumer_field_schemas": true,
  "currency_code": "string",
  "payment_destination_id": "string",
  "currency_config": {
    "supported_payment_sources": [
      {
        "type": "credit_card",
        "unsupported_cards": [
          "string"
        ]
      }
    ]
  },
  "payments": [
    {
      "id": "string",
      "status": "pending",
      "number": 0,
      "percentage": 1,
      "due_deadline": "2017-11-03T23:44:19Z",
      "paid_at": "2017-11-03T23:44:19Z",
      "accepted_at": "2017-11-03T23:44:19Z",
      "submitted_at": "2017-11-03T23:44:19Z",
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "conversion_rate": 0,
      "processing_currency": "string",
      "failed": true,
      "payout_failed": true
    }
  ],
  "current_payment": {
    "id": "string",
    "status": "pending",
    "number": 0,
    "percentage": 1,
    "due_deadline": "2017-11-03T23:44:19Z",
    "paid_at": "2017-11-03T23:44:19Z",
    "accepted_at": "2017-11-03T23:44:19Z",
    "submitted_at": "2017-11-03T23:44:19Z",
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "conversion_rate": 0,
    "processing_currency": "string",
    "failed": true,
    "payout_failed": true
  },
  "next_payment_due_deadline": "2017-11-03T23:44:19Z",
  "cost_range": [
    {
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "min_slots": 0,
      "max_slots": 0
    }
  ],
  "current_product_cost_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "current_total_cost_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "max_product_cost_by_slots": {
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "min_slots": 0,
    "max_slots": 0
  },
  "min_product_cost_by_slots": {
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "min_slots": 0,
    "max_slots": 0
  },
  "max_product_cost_by_amount": {
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "min_slots": 0,
    "max_slots": 0
  },
  "fees_structure": {
    "currency_code": "string",
    "payment_destination_type": "bank_account",
    "consumer_fees": {
      "per_share": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "per_share_max": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "per_share_min": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "percentage": 1
    },
    "merchant_service_fees": {
      "per_share": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "per_purchase_max": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "percentage": 1
    },
    "merchant_processing_fees": {
      "per_transaction": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "percentage": 1
    }
  },
  "apply_consumer_fee_to_organizer": true,
  "product": {
    "images": [
      {
        "name": "string",
        "version": "string",
        "url": "string"
      }
    ],
    "default_image_url": "string",
    "allowed_split_types": "even_split",
    "cost_type": "total",
    "costs": [
      {
        "amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "min_slots": 0,
        "max_slots": 0
      }
    ],
    "description": "string",
    "name": "string",
    "end_datetime": "2017-11-03T23:44:19Z",
    "start_datetime": "2017-11-03T23:44:19Z",
    "external_purchase_id": "string",
    "inventory_id": "string",
    "link": "string",
    "max_slots": 0,
    "min_slots": 0,
    "legal_documents": [
      {
        "id": "string",
        "type": "tos",
        "title": "string",
        "content": "string",
        "created_at": "2017-11-03T23:44:19Z",
        "updated_at": "2017-11-03T23:44:19Z"
      }
    ]
  },
  "group": {
    "commit_deadline": "2017-11-03T23:44:19Z",
    "max_slots": 0,
    "min_slots": 0,
    "min_contribution": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "organizer_email": "user@example.com",
    "organizer_full_name": "string",
    "legal_document_ids": [
      "string"
    ],
    "split_type": "even_split"
  },
  "memberships": [
    {
      "id": "string",
      "status": "holdout",
      "refund_status": "none",
      "failed": true,
      "short": true,
      "role": "organizer",
      "claimed_slots": 0,
      "opt_in_marketing": true,
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "share_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "fees": {
        "consumer_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "merchant_service_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        }
      },
      "consumer_field_values": {
        "name": "string",
        "scope": "member",
        "required": true
      },
      "allowed_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "allowed_share_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "allowed_fees": {
        "consumer_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "merchant_service_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        }
      },
      "max_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "max_share_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "max_fees": {
        "consumer_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "merchant_service_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        }
      },
      "collected_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "collected_share_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "current_contribution": {
        "id": "string",
        "status": "created",
        "refund_status": "none",
        "amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "share_amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "fees": {
          "consumer_fee": {
            "amount_cents": 0,
            "currency_code": "string"
          },
          "merchant_service_fee": {
            "amount_cents": 0,
            "currency_code": "string"
          }
        },
        "charged_at": "2017-11-03T23:44:19Z",
        "failed_at": "2017-11-03T23:44:19Z",
        "created_at": "string"
      },
      "user": {
        "id": "string",
        "email": "user@example.com",
        "full_name": "string",
        "first_name": "string",
        "last_name": "string",
        "avatar_url": "string",
        "language_code": "string",
        "created_at": "string"
      },
      "purchase_id": "string",
      "payment_source": {
        "id": "string",
        "name": "string",
        "type": "string",
        "info": {
          "account_name": "string",
          "account_number": "string",
          "account_holder_type": "string"
        },
        "created_at": "2017-11-03T23:44:19Z"
      },
      "committed_at": "2017-11-03T23:44:19Z",
      "created_at": "2017-11-03T23:44:19Z"
    }
  ],
  "collected_shares_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "committed_shares_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "committed_slots": 0,
  "needed_amount_to_current_payment": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "needed_slots_to_min": 0,
  "product_or_group_max_slots": 0,
  "product_or_group_min_slots": 0,
  "language_code": "string",
  "created_at": "2017-11-03T23:44:19Z"
}
```
```json
{
  "errors": [
    {
      "code": 0,
      "message": "string"
    }
  ]
}
```
```json
{
  "errors": [
    {
      "code": 0,
      "message": "string"
    }
  ]
}
```
<h3 id="UpdatePurchase-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success response.|[Purchase](#schemapurchase)
404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found.|[Error](#schemaerror)
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Unprocessable entity.|[Error](#schemaerror)

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
http
</aside>

## ClaimPurchase

`POST /purchases/{id}/claim`

*Claim purchase as organizer*

This officially attaches a user to a purchase as its organizer.
Its parameters correspond to selections the organizer can make (or the merchant makes on their behalf)
for how to split the cost amoung their group. Pay By Group will handle this step for any purchase
a merchant creates if they redirect the user to Pay By Group, but merchants may also call this
method before redirecting the user, either building this part of the experience into their site or
supplying defaults for the required parameters.

> Body parameter

```json
{
  "organizer_name": "string",
  "organizer_email": "string",
  "organizer_allowed_share_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "min_contribution": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "group": {
    "split_type": "even_split",
    "max_slots": 0,
    "min_slots": 0
  }
}
```
<h3 id="ClaimPurchase-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|string(uuid)|true|ID of the Purchase to claim
body|body|object|true|No description
» organizer_name|body|string|false|Name of the organizer
» organizer_email|body|string|false|Email of the organizer
» organizer_allowed_share_amount|body|[Money](#schemamoney)|false|Allowed share of the organizer
» min_contribution|body|[Money](#schemamoney)|false|Min contribution amount
» group|body|object|false|No description
»» split_type|body|string|false|Splitting type chosen by the organizer for how to divide the cost
»» max_slots|body|integer(int32)|false|The organizer-specified value for the maximum number of slots they
»» min_slots|body|integer(int32)|false|The organizer-specified value for the minimum number of slots they


#### Enumerated Values

|Parameter|Value|
|---|---|
»» split_type|even_split|
»» split_type|specified_per_person|
»» split_type|fixed_per_person|

##### »» split_type
Splitting type chosen by the organizer for how to divide the cost
among group members.
One of:
- even_split Only compatible with total cost_type and means the
  Purchase amount is split evenly across each slot claimed.
- specified_per_person Only compatible with total cost_type and
  means each member may pay a different amount.
- fixed_per_person Only compatible with per_slot cost_type and means
  each group member pays a fixed amount per slot they claim.

##### »» max_slots
The organizer-specified value for the maximum number of slots they
will allow to be claimed.
It must be within the bounds allowed by the merchant.

##### »» min_slots
The organizer-specified value for the minimum number of slots they
require to be claimed.
It must be within the bounds allowed by the merchant.

> Example responses

```json
{
  "id": "string",
  "slug": "string",
  "merchant": {
    "id": "string",
    "unique_name": "string",
    "display_name": "string",
    "support_email": "user@example.com",
    "support_phone": "string",
    "logo_url": "string",
    "defaults": {
      "currency_code": "string",
      "language_code": "string",
      "timezone_code": "string",
      "product_image_url": "string"
    }
  },
  "status": "created",
  "refund_status": "none",
  "processing_refund": true,
  "tipped": true,
  "auto_pilot_enabled": true,
  "auto_pilot_trigger_slots": 0,
  "consumer_fields": [
    {
      "name": "string",
      "label": "string",
      "description": "string",
      "type": "text",
      "settings": {},
      "scope": "member",
      "default_value": "string"
    }
  ],
  "consumer_field_values": [
    {
      "name": "string",
      "scope": "member",
      "required": true
    }
  ],
  "consumer_field_schemas": [
    {
      "id": "string",
      "name": "string",
      "label": "string",
      "scope": "member",
      "required": true,
      "type": "text"
    }
  ],
  "has_consumer_field_schemas": true,
  "currency_code": "string",
  "payment_destination_id": "string",
  "currency_config": {
    "supported_payment_sources": [
      {
        "type": "credit_card",
        "unsupported_cards": [
          "string"
        ]
      }
    ]
  },
  "payments": [
    {
      "id": "string",
      "status": "pending",
      "number": 0,
      "percentage": 1,
      "due_deadline": "2017-11-03T23:44:19Z",
      "paid_at": "2017-11-03T23:44:19Z",
      "accepted_at": "2017-11-03T23:44:19Z",
      "submitted_at": "2017-11-03T23:44:19Z",
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "conversion_rate": 0,
      "processing_currency": "string",
      "failed": true,
      "payout_failed": true
    }
  ],
  "current_payment": {
    "id": "string",
    "status": "pending",
    "number": 0,
    "percentage": 1,
    "due_deadline": "2017-11-03T23:44:19Z",
    "paid_at": "2017-11-03T23:44:19Z",
    "accepted_at": "2017-11-03T23:44:19Z",
    "submitted_at": "2017-11-03T23:44:19Z",
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "conversion_rate": 0,
    "processing_currency": "string",
    "failed": true,
    "payout_failed": true
  },
  "next_payment_due_deadline": "2017-11-03T23:44:19Z",
  "cost_range": [
    {
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "min_slots": 0,
      "max_slots": 0
    }
  ],
  "current_product_cost_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "current_total_cost_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "max_product_cost_by_slots": {
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "min_slots": 0,
    "max_slots": 0
  },
  "min_product_cost_by_slots": {
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "min_slots": 0,
    "max_slots": 0
  },
  "max_product_cost_by_amount": {
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "min_slots": 0,
    "max_slots": 0
  },
  "fees_structure": {
    "currency_code": "string",
    "payment_destination_type": "bank_account",
    "consumer_fees": {
      "per_share": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "per_share_max": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "per_share_min": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "percentage": 1
    },
    "merchant_service_fees": {
      "per_share": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "per_purchase_max": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "percentage": 1
    },
    "merchant_processing_fees": {
      "per_transaction": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "percentage": 1
    }
  },
  "apply_consumer_fee_to_organizer": true,
  "product": {
    "images": [
      {
        "name": "string",
        "version": "string",
        "url": "string"
      }
    ],
    "default_image_url": "string",
    "allowed_split_types": "even_split",
    "cost_type": "total",
    "costs": [
      {
        "amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "min_slots": 0,
        "max_slots": 0
      }
    ],
    "description": "string",
    "name": "string",
    "end_datetime": "2017-11-03T23:44:19Z",
    "start_datetime": "2017-11-03T23:44:19Z",
    "external_purchase_id": "string",
    "inventory_id": "string",
    "link": "string",
    "max_slots": 0,
    "min_slots": 0,
    "legal_documents": [
      {
        "id": "string",
        "type": "tos",
        "title": "string",
        "content": "string",
        "created_at": "2017-11-03T23:44:19Z",
        "updated_at": "2017-11-03T23:44:19Z"
      }
    ]
  },
  "group": {
    "commit_deadline": "2017-11-03T23:44:19Z",
    "max_slots": 0,
    "min_slots": 0,
    "min_contribution": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "organizer_email": "user@example.com",
    "organizer_full_name": "string",
    "legal_document_ids": [
      "string"
    ],
    "split_type": "even_split"
  },
  "memberships": [
    {
      "id": "string",
      "status": "holdout",
      "refund_status": "none",
      "failed": true,
      "short": true,
      "role": "organizer",
      "claimed_slots": 0,
      "opt_in_marketing": true,
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "share_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "fees": {
        "consumer_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "merchant_service_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        }
      },
      "consumer_field_values": {
        "name": "string",
        "scope": "member",
        "required": true
      },
      "allowed_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "allowed_share_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "allowed_fees": {
        "consumer_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "merchant_service_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        }
      },
      "max_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "max_share_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "max_fees": {
        "consumer_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "merchant_service_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        }
      },
      "collected_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "collected_share_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "current_contribution": {
        "id": "string",
        "status": "created",
        "refund_status": "none",
        "amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "share_amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "fees": {
          "consumer_fee": {
            "amount_cents": 0,
            "currency_code": "string"
          },
          "merchant_service_fee": {
            "amount_cents": 0,
            "currency_code": "string"
          }
        },
        "charged_at": "2017-11-03T23:44:19Z",
        "failed_at": "2017-11-03T23:44:19Z",
        "created_at": "string"
      },
      "user": {
        "id": "string",
        "email": "user@example.com",
        "full_name": "string",
        "first_name": "string",
        "last_name": "string",
        "avatar_url": "string",
        "language_code": "string",
        "created_at": "string"
      },
      "purchase_id": "string",
      "payment_source": {
        "id": "string",
        "name": "string",
        "type": "string",
        "info": {
          "account_name": "string",
          "account_number": "string",
          "account_holder_type": "string"
        },
        "created_at": "2017-11-03T23:44:19Z"
      },
      "committed_at": "2017-11-03T23:44:19Z",
      "created_at": "2017-11-03T23:44:19Z"
    }
  ],
  "collected_shares_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "committed_shares_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "committed_slots": 0,
  "needed_amount_to_current_payment": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "needed_slots_to_min": 0,
  "product_or_group_max_slots": 0,
  "product_or_group_min_slots": 0,
  "language_code": "string",
  "created_at": "2017-11-03T23:44:19Z"
}
```
```json
{
  "errors": [
    {
      "code": 0,
      "message": "string"
    }
  ]
}
```
```json
{
  "errors": [
    {
      "code": 0,
      "message": "string"
    }
  ]
}
```
<h3 id="ClaimPurchase-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success response|[Purchase](#schemapurchase)
404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|[Error](#schemaerror)
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Unprocessable entity|[Error](#schemaerror)

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
http
</aside>

## InviteMembersToPurchase

`POST /purchases/{id}/invite`

*Invite users to join a purchase*

Sends invitations to join the purchase and creates memberships in `holdout` state.
They will receive reminders to join until the purchase completes, expires, or is canceled.

> Body parameter

```json
{
  "invitees": [
    {
      "email": "user@example.com",
      "full_name": "string",
      "allowed_share_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      }
    }
  ],
  "message": "string",
  "subject": "string"
}
```
<h3 id="InviteMembersToPurchase-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|string(uuid)|true|ID of the Purchase to invite to.
body|body|object|true|No description
» message|body|string|false|Message to attach to the invite notification.
» subject|body|string|false|Subject of the notification.
» invitees|body|[object]|false|No description
»» email|body|string(email)|false|Email to send the invite to.
»» full_name|body|string|false|Name of the invitee.
»» allowed_share_amount|body|[Money](#schemamoney)|false|Suggested contribution for the invitee.


<h3 id="InviteMembersToPurchase-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|Success response|None
404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|None
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Unprocessable entity|None

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
http
</aside>

## RequestPurchaseRefund

`POST /purchases/{id}/refund`

*Refund purchase*

Refund the money collected for a purchase, either in whole or in part.
The refund will be allocated proportionally across all group members relative to their
percentages of all payments completed thus far. If you try to refund an amount larger than
the sum of all payments on the purchase, you will get an error response.

> Body parameter

```json
{
  "reason": "string",
  "amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "memberships_shares": [
    {
      "membership_id": "string",
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      }
    }
  ],
  "funding_source_id": "string"
}
```
<h3 id="RequestPurchaseRefund-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|string(uuid)|true|ID of the purchase to refund
body|body|object|true|No description
» reason|body|string|false|Reason why this amount is being refunded
» amount|body|[Money](#schemamoney)|false|Amount to be refunded. It may not be greater than the current
» funding_source_id|body|string(uuid)|false|UUID of the merchant's payment source for funding refunds
» memberships_shares|body|[object]|false|No description
»» membership_id|body|string|false|ID of the membership to refund.
»» amount|body|[Money](#schemamoney)|false|Amount to refund to this member.


##### » amount
Amount to be refunded. It may not be greater than the current
collected amount of the purchase, which is the total purchase
amount net of any previous refunds. If the memberships_shares
are provided, this value must equal the sum of those shares.

> Example responses

```json
{
  "id": "string",
  "slug": "string",
  "merchant": {
    "id": "string",
    "unique_name": "string",
    "display_name": "string",
    "support_email": "user@example.com",
    "support_phone": "string",
    "logo_url": "string",
    "defaults": {
      "currency_code": "string",
      "language_code": "string",
      "timezone_code": "string",
      "product_image_url": "string"
    }
  },
  "status": "created",
  "refund_status": "none",
  "processing_refund": true,
  "tipped": true,
  "auto_pilot_enabled": true,
  "auto_pilot_trigger_slots": 0,
  "consumer_fields": [
    {
      "name": "string",
      "label": "string",
      "description": "string",
      "type": "text",
      "settings": {},
      "scope": "member",
      "default_value": "string"
    }
  ],
  "consumer_field_values": [
    {
      "name": "string",
      "scope": "member",
      "required": true
    }
  ],
  "consumer_field_schemas": [
    {
      "id": "string",
      "name": "string",
      "label": "string",
      "scope": "member",
      "required": true,
      "type": "text"
    }
  ],
  "has_consumer_field_schemas": true,
  "currency_code": "string",
  "payment_destination_id": "string",
  "currency_config": {
    "supported_payment_sources": [
      {
        "type": "credit_card",
        "unsupported_cards": [
          "string"
        ]
      }
    ]
  },
  "payments": [
    {
      "id": "string",
      "status": "pending",
      "number": 0,
      "percentage": 1,
      "due_deadline": "2017-11-03T23:44:19Z",
      "paid_at": "2017-11-03T23:44:19Z",
      "accepted_at": "2017-11-03T23:44:19Z",
      "submitted_at": "2017-11-03T23:44:19Z",
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "conversion_rate": 0,
      "processing_currency": "string",
      "failed": true,
      "payout_failed": true
    }
  ],
  "current_payment": {
    "id": "string",
    "status": "pending",
    "number": 0,
    "percentage": 1,
    "due_deadline": "2017-11-03T23:44:19Z",
    "paid_at": "2017-11-03T23:44:19Z",
    "accepted_at": "2017-11-03T23:44:19Z",
    "submitted_at": "2017-11-03T23:44:19Z",
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "conversion_rate": 0,
    "processing_currency": "string",
    "failed": true,
    "payout_failed": true
  },
  "next_payment_due_deadline": "2017-11-03T23:44:19Z",
  "cost_range": [
    {
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "min_slots": 0,
      "max_slots": 0
    }
  ],
  "current_product_cost_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "current_total_cost_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "max_product_cost_by_slots": {
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "min_slots": 0,
    "max_slots": 0
  },
  "min_product_cost_by_slots": {
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "min_slots": 0,
    "max_slots": 0
  },
  "max_product_cost_by_amount": {
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "min_slots": 0,
    "max_slots": 0
  },
  "fees_structure": {
    "currency_code": "string",
    "payment_destination_type": "bank_account",
    "consumer_fees": {
      "per_share": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "per_share_max": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "per_share_min": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "percentage": 1
    },
    "merchant_service_fees": {
      "per_share": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "per_purchase_max": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "percentage": 1
    },
    "merchant_processing_fees": {
      "per_transaction": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "percentage": 1
    }
  },
  "apply_consumer_fee_to_organizer": true,
  "product": {
    "images": [
      {
        "name": "string",
        "version": "string",
        "url": "string"
      }
    ],
    "default_image_url": "string",
    "allowed_split_types": "even_split",
    "cost_type": "total",
    "costs": [
      {
        "amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "min_slots": 0,
        "max_slots": 0
      }
    ],
    "description": "string",
    "name": "string",
    "end_datetime": "2017-11-03T23:44:19Z",
    "start_datetime": "2017-11-03T23:44:19Z",
    "external_purchase_id": "string",
    "inventory_id": "string",
    "link": "string",
    "max_slots": 0,
    "min_slots": 0,
    "legal_documents": [
      {
        "id": "string",
        "type": "tos",
        "title": "string",
        "content": "string",
        "created_at": "2017-11-03T23:44:19Z",
        "updated_at": "2017-11-03T23:44:19Z"
      }
    ]
  },
  "group": {
    "commit_deadline": "2017-11-03T23:44:19Z",
    "max_slots": 0,
    "min_slots": 0,
    "min_contribution": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "organizer_email": "user@example.com",
    "organizer_full_name": "string",
    "legal_document_ids": [
      "string"
    ],
    "split_type": "even_split"
  },
  "memberships": [
    {
      "id": "string",
      "status": "holdout",
      "refund_status": "none",
      "failed": true,
      "short": true,
      "role": "organizer",
      "claimed_slots": 0,
      "opt_in_marketing": true,
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "share_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "fees": {
        "consumer_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "merchant_service_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        }
      },
      "consumer_field_values": {
        "name": "string",
        "scope": "member",
        "required": true
      },
      "allowed_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "allowed_share_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "allowed_fees": {
        "consumer_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "merchant_service_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        }
      },
      "max_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "max_share_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "max_fees": {
        "consumer_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "merchant_service_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        }
      },
      "collected_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "collected_share_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "current_contribution": {
        "id": "string",
        "status": "created",
        "refund_status": "none",
        "amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "share_amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "fees": {
          "consumer_fee": {
            "amount_cents": 0,
            "currency_code": "string"
          },
          "merchant_service_fee": {
            "amount_cents": 0,
            "currency_code": "string"
          }
        },
        "charged_at": "2017-11-03T23:44:19Z",
        "failed_at": "2017-11-03T23:44:19Z",
        "created_at": "string"
      },
      "user": {
        "id": "string",
        "email": "user@example.com",
        "full_name": "string",
        "first_name": "string",
        "last_name": "string",
        "avatar_url": "string",
        "language_code": "string",
        "created_at": "string"
      },
      "purchase_id": "string",
      "payment_source": {
        "id": "string",
        "name": "string",
        "type": "string",
        "info": {
          "account_name": "string",
          "account_number": "string",
          "account_holder_type": "string"
        },
        "created_at": "2017-11-03T23:44:19Z"
      },
      "committed_at": "2017-11-03T23:44:19Z",
      "created_at": "2017-11-03T23:44:19Z"
    }
  ],
  "collected_shares_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "committed_shares_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "committed_slots": 0,
  "needed_amount_to_current_payment": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "needed_slots_to_min": 0,
  "product_or_group_max_slots": 0,
  "product_or_group_min_slots": 0,
  "language_code": "string",
  "created_at": "2017-11-03T23:44:19Z"
}
```
```json
{
  "errors": [
    {
      "code": 0,
      "message": "string"
    }
  ]
}
```
```json
{
  "errors": [
    {
      "code": 0,
      "message": "string"
    }
  ]
}
```
<h3 id="RequestPurchaseRefund-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
202|[Accepted](https://tools.ietf.org/html/rfc7231#section-6.3.3)|Success response|[Purchase](#schemapurchase)
404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|[Error](#schemaerror)
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Unprocessable entity|[Error](#schemaerror)

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
http
</aside>

## CancelPurchase

`POST /purchases/{id}/cancel`

*Cancel purchase*

Cancels this purchase so that it may not complete under any circumstances.
If any payment is in `authorized` state, all auths will be voided.

> Body parameter

```json
{
  "reason": "string"
}
```
<h3 id="CancelPurchase-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|string(uuid)|true|ID of the Purchase to cancel
body|body|object|true|No description
» reason|body|string|false|Description to be provided to the group's organizer


##### » reason
Description to be provided to the group's organizer
explaining why the group was canceled

<h3 id="CancelPurchase-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|Success response|None
404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|None
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Unprocessable entity|None

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
http
</aside>

## CreatePurchaseImages

`POST /purchases/{id}/images`

*Create purchase image*

Attaches an image of the product to the purchase specified in the
request. The most recent image uploaded will be the primary image
for the purchase.

> Body parameter

```yaml
url: string
file: string

```
<h3 id="CreatePurchaseImages-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|string(uuid)|true|ID of the Image
body|body|object|false|No description
» url|body|string|false|No description
» file|body|string(binary)|false|Image file provided by the merchant


> Example responses

```json
{
  "name": "string",
  "version": "string",
  "url": "string"
}
```
```json
{
  "errors": [
    {
      "code": 0,
      "message": "string"
    }
  ]
}
```
```json
{
  "errors": [
    {
      "code": 0,
      "message": "string"
    }
  ]
}
```
<h3 id="CreatePurchaseImages-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success response|[Image](#schemaimage)
404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|[Error](#schemaerror)
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Unprocessable entity|[Error](#schemaerror)

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
http
</aside>

## RetrievePurchaseMemberships

`GET /purchases/{id}/memberships`

*Retrieve list of all memberships for a purchase*

Returns a paginated list of all memberships associated with the specified purchase.

<h3 id="RetrievePurchaseMemberships-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|string(uuid)|true|Purchase ID.


> Example responses

```json
[
  {
    "id": "string",
    "status": "holdout",
    "refund_status": "none",
    "failed": true,
    "short": true,
    "role": "organizer",
    "claimed_slots": 0,
    "opt_in_marketing": true,
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "share_amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "fees": {
      "consumer_fee": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "merchant_service_fee": {
        "amount_cents": 0,
        "currency_code": "string"
      }
    },
    "consumer_field_values": {
      "name": "string",
      "scope": "member",
      "required": true
    },
    "allowed_amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "allowed_share_amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "allowed_fees": {
      "consumer_fee": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "merchant_service_fee": {
        "amount_cents": 0,
        "currency_code": "string"
      }
    },
    "max_amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "max_share_amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "max_fees": {
      "consumer_fee": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "merchant_service_fee": {
        "amount_cents": 0,
        "currency_code": "string"
      }
    },
    "collected_amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "collected_share_amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "current_contribution": {
      "id": "string",
      "status": "created",
      "refund_status": "none",
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "share_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "fees": {
        "consumer_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "merchant_service_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        }
      },
      "charged_at": "2017-11-03T23:44:19Z",
      "failed_at": "2017-11-03T23:44:19Z",
      "created_at": "string"
    },
    "user": {
      "id": "string",
      "email": "user@example.com",
      "full_name": "string",
      "first_name": "string",
      "last_name": "string",
      "avatar_url": "string",
      "language_code": "string",
      "created_at": "string"
    },
    "purchase_id": "string",
    "payment_source": {
      "id": "string",
      "name": "string",
      "type": "string",
      "info": {
        "account_name": "string",
        "account_number": "string",
        "account_holder_type": "string"
      },
      "created_at": "2017-11-03T23:44:19Z"
    },
    "committed_at": "2017-11-03T23:44:19Z",
    "created_at": "2017-11-03T23:44:19Z"
  }
]
```
```json
{
  "errors": [
    {
      "code": 0,
      "message": "string"
    }
  ]
}
```
<h3 id="RetrievePurchaseMemberships-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success response|Inline
404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|[Error](#schemaerror)

<h3 id="RetrievePurchaseMemberships-responseschema">Response Schema</h3>

Status Code **200**

Name|Type|Required|Description
---|---|---|---|---|
anonymous|[[Membership](#schemamembership)]|false|No description
» id|string|false|Pay By Group UUID for this membership
» status|string|false|One of: - holdout (user has been invited but not joined the group); - committed (user has joined the group and whether they have been charged is in the contribution object); 
» refund_status|string|false|Status that determines whether the Membership is partially or fully refunded. One of: - none (none of the Membership's Contributions were refunded). - partial (some of the Membership's Contributions were partially   or fully refunded). - full (all of the Membership's Contributions were fully refunded). 
» failed|boolean|false|User is currently in the group with a failed payment method, which is preventing the purchase from completing 
» short|boolean|false|The user is currently in the group but has not agreed to pay their new required share amount due to updates to the purchase. 
» role|string|false|Either organizer or invitee
» claimed_slots|integer(int32)|false|Number of slots the member has claimed in the group. Defaults to 1 if none is selected by the user.
» opt_in_marketing|boolean|false|true if the user has opted in to receive marketing communication from the merchant. Otherwise false.
» amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» share_amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» fees|[Fees](#schemafees)|false|No description
»» consumer_fee|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» merchant_service_fee|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
» consumer_field_values|[ConsumerFieldValue](#schemaconsumerfieldvalue)|false|No description
»» name|string|false|Name of the schema
»» scope|string|false|One of member or purchase.
»» required|boolean|false|Whether the schema field should be required or not.
» allowed_amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» allowed_share_amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» allowed_fees|[Fees](#schemafees)|false|No description
»» consumer_fee|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» merchant_service_fee|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
» max_amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» max_share_amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» max_fees|[Fees](#schemafees)|false|No description
»» consumer_fee|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» merchant_service_fee|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
» collected_amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» collected_share_amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» current_contribution|[Contribution](#schemacontribution)|false|No description
»» id|string|false|UUID of this contribution
»» status|string|false|Current status of the contribution, any of created, authorized, captured, holdout or failed
»» refund_status|string|false|Status that determines whether the Contribution is partially or fully refunded. One of: - none (none of the Contribution's Transactions were refunded). - partial (some of the Contribution's Transactions were partially   or fully refunded). - full (all of the Contribution's Transactions were fully refunded). 
»» amount|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» share_amount|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» fees|[Fees](#schemafees)|false|No description
»»» consumer_fee|[Money](#schemamoney)|false|No description
»»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»»» currency_code|string|false|3-letter currency code attached to every money value
»»» merchant_service_fee|[Money](#schemamoney)|false|No description
»»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»»» currency_code|string|false|3-letter currency code attached to every money value
»» charged_at|string(date-time)|false|Timestamp of when this contibution was charged
»» failed_at|string(date-time)|false|Timestamp of when this contribution most recently failed
»» created_at|string|false|Timestamp when the record of this contribution was first created, which is not necessarily when it was charged 
» user|[User](#schemauser)|false|No description
»» id|string(uuid)|false|Pay By Group UUID for this user
»» email|string(email)|false|User's email address
»» full_name|string|false|User's full name
»» first_name|string|false|User's first name
»» last_name|string|false|User's last name
»» avatar_url|string|false|URL of the User's avatar
»» language_code|string|false|The preferred language selected by this user
»» created_at|string(uuid)|false|No description
» purchase_id|string(uuid)|false|Pay By Group slug of the purchase to which this membership is tied
» payment_source|[PaymentSource](#schemapaymentsource)|false|No description
»» id|string(uuid)|false|Pay By Group UUID of this payment source
»» name|string|false|Full name of this payment source's owner
»» type|string|false|Describes the type of payment source, any of credit_card or bank_account
»» info|object|false|Bank account information of this payment source
»»» account_name|string|false|Listed name of the account holder
»»» account_number|string|false|Account number
»»» account_holder_type|string|false|Either a business or individual
»» created_at|string(date-time)|false|Timestamp when the payment source was first added to the system
» committed_at|string(date-time)|false|Timestamp of when the member agreed to pay into the purchase
» created_at|string(date-time)|false|When the membership was first created



<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
http
</aside>

## RetrievePurchasePaymentTransactions

`GET /purchases/{id}/transactions`

*Retrieve list of all transactions*

Returns a paginated list of all transactions that have been attempted or
completed for payments related to a specific purchase.

<h3 id="RetrievePurchasePaymentTransactions-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|string(uuid)|true|Purchase ID


> Example responses

```json
[
  {
    "id": "string",
    "short_id": "string",
    "parent_id": "string",
    "chargable_type": "string",
    "action": "auth",
    "status": "pending",
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "fees": {
      "consumer_fee": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "merchant_service_fee": {
        "amount_cents": 0,
        "currency_code": "string"
      }
    },
    "payout_account": {
      "id": "string",
      "name": "string",
      "status": "verified",
      "user_id": "string",
      "merchant_id": "string",
      "supported_currency_codes": [
        "string"
      ],
      "currency_configs": "string"
    },
    "payment_gateway": {
      "id": "string",
      "name": "string",
      "merchant_id": "string",
      "supported_currency_codes": [
        "string"
      ]
    },
    "payment_source": {
      "id": "string",
      "name": "string",
      "type": "string",
      "info": {
        "account_name": "string",
        "account_number": "string",
        "account_holder_type": "string"
      },
      "created_at": "2017-11-03T23:44:19Z"
    },
    "created_at": "2017-11-03T23:44:19Z",
    "processing_currency": "string",
    "conversion_rate": 0
  }
]
```
```json
{
  "errors": [
    {
      "code": 0,
      "message": "string"
    }
  ]
}
```
<h3 id="RetrievePurchasePaymentTransactions-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success response|Inline
404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|[Error](#schemaerror)

<h3 id="RetrievePurchasePaymentTransactions-responseschema">Response Schema</h3>

Status Code **200**

Name|Type|Required|Description
---|---|---|---|---|
anonymous|[[PaymentTransaction](#schemapaymenttransaction)]|false|No description
» id|string(uuid)|false|Pay By Group UUID for this transaction
» short_id|string|false|Unique ID of this transaction for easy reference
» parent_id|string|false|Another transaction related to and replaced by this one - e.g. the credit card authorization for which this transaction is the capture or the capture for which this is the refund. 
» chargable_type|string|false|No description
» action|string|false|One of: - auth (holds funds or the specified amount on the user's payment   method for later capture). - capture (captures funds that were previously authorized at an   amount = or < the authorized amount). - charge (instantly charges an amount without first making an   authorization). - void (voids a previously created authorization). - refund (refunds a previously created capture or charge). - payout (sends funds to a bank account). 
» status|string|false|Oneo of pending, completed or failed
» amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» fees|[Fees](#schemafees)|false|No description
»» consumer_fee|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» merchant_service_fee|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
» payout_account|[BankAccount](#schemabankaccount)|false|No description
»» id|string(uuid)|false|Pay By Group UUID for this bank account
»» name|string|false|Displayed name of bank account with last 4 of account number
»» status|string|false|verified or unverified depending on whether micro-deposit amounts have confirmed account ownership
»» user_id|string(uuid)|false|User that added the bank account
»» merchant_id|string(uuid)|false|Merchant this bank account belongs to
»» currency_configs|string|false|Set of payment sources supported across all currencies for this bank account. Not all currencies support all payment sources. 
»» supported_currency_codes|[string]|false|3-letter currency codes that can be used for credits and debits with this account
» payment_gateway|[PaymentGateway](#schemapaymentgateway)|false|No description
»» id|string|false|Pay By Group UUID for this payment gateway
»» name|string|false|Displayed name of the gateway
»» merchant_id|string|false|Merchant this gateway belongs to
»» supported_currency_codes|[string]|false|3-letter currency codes that can be used for payments to this gateway
» payment_source|[PaymentSource](#schemapaymentsource)|false|No description
»» id|string(uuid)|false|Pay By Group UUID of this payment source
»» name|string|false|Full name of this payment source's owner
»» type|string|false|Describes the type of payment source, any of credit_card or bank_account
»» info|object|false|Bank account information of this payment source
»»» account_name|string|false|Listed name of the account holder
»»» account_number|string|false|Account number
»»» account_holder_type|string|false|Either a business or individual
»» created_at|string(date-time)|false|Timestamp when the payment source was first added to the system
» created_at|string(date-time)|false|Timestamp when the transaction was created
» processing_currency|string|false|The currency in which this transaction occurred
» conversion_rate|number(float)|false|If the currency of the purchase differs from the required currency of the payout account then this is the conversion rate used to determine the transaction amount. 



<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
http
</aside>

## RetrievePurchaseLegalDocuments

`GET /purchases/{id}/legal_documents`

*List legal documents attached to purchase*

Returns a paginated list of all legal documents currently
attached to this purchase that must be accepted by its members

<h3 id="RetrievePurchaseLegalDocuments-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|string(uuid)|true|Purchase ID


> Example responses

```json
[
  {
    "id": "string",
    "type": "tos",
    "title": "string",
    "content": "string",
    "created_at": "2017-11-03T23:44:19Z",
    "updated_at": "2017-11-03T23:44:19Z"
  }
]
```
```json
{
  "errors": [
    {
      "code": 0,
      "message": "string"
    }
  ]
}
```
<h3 id="RetrievePurchaseLegalDocuments-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success response|Inline
404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|[Error](#schemaerror)

<h3 id="RetrievePurchaseLegalDocuments-responseschema">Response Schema</h3>

Status Code **200**

Name|Type|Required|Description
---|---|---|---|---|
anonymous|[[LegalDocument](#schemalegaldocument)]|false|No description
» id|string(uuid)|false|Pay By Group UUID of this legal document
» type|string|false|Specified by the merchant as either cancellation policy for cancellation and refund terms or tos for all other legal documents. 
» title|string|false|Mechant's title for this legal document
» content|string|false|Full content as provided by the merchant, either in plain text or as a URL
» created_at|string(date-time)|false|When this legal document was added by the merchant
» updated_at|string(date-time)|false|When this legal document was last updated by the merchant



<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
http
</aside>

## RetrievePurchaseLegalBindings

`GET /purchases/{id}/legal_documents/acceptances`

*List legal term acceptance records for all members*

Returns a paginated list of all legal bindings, which
represent each individual acceptance of a legal document
for this purchase by a group member

<h3 id="RetrievePurchaseLegalBindings-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|string(uuid)|true|Purchase ID


> Example responses

```json
[
  {
    "id": "string",
    "type": "string",
    "title": "string",
    "content": "string",
    "created_at": "string",
    "remote_ip": "string",
    "user_id": "string",
    "purchase_id": "string"
  }
]
```
```json
{
  "errors": [
    {
      "code": 0,
      "message": "string"
    }
  ]
}
```
<h3 id="RetrievePurchaseLegalBindings-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success response|Inline
404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|[Error](#schemaerror)

<h3 id="RetrievePurchaseLegalBindings-responseschema">Response Schema</h3>

Status Code **200**

Name|Type|Required|Description
---|---|---|---|---|
anonymous|[[LegalBinding](#schemalegalbinding)]|false|No description
» id|string(uuid)|false|Pay By Group UUID of this specific record of acceptance by the user
» type|string|false|Either cancellation policy for cancellation and refund terms or tos for all other legal documents provided by merchant. 
» title|string|false|Mechant's title for this legal document as accepted by the user
» content|string|false|Full content as accepted by the user at the moment they agreed to this legal document
» created_at|string|false|Verifiable timestamp when the user accepted this legal document
» remote_ip|string|false|User's IP address at the moment they accepted this legal document
» user_id|string|false|ID of the user that accepted the document, which includes their name and email
» purchase_id|string|false|The purchase for which this document was accepted by the user



<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
http
</aside>

# payments

Operations on Payment objects.

## AcceptPayment

`POST /payments/{id}/accept`

*Accept a payment*

Merchants must make this call to receive a payout for any payment
that is in authorized status unless the merchant is  configured to auto-accept
all payments automatically

<h3 id="AcceptPayment-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|string(uuid)|true|ID of the Purchase to accept


> Example responses

```json
{
  "errors": [
    {
      "code": 0,
      "message": "string"
    }
  ]
}
```
```json
{
  "errors": [
    {
      "code": 0,
      "message": "string"
    }
  ]
}
```
<h3 id="AcceptPayment-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
202|[Accepted](https://tools.ietf.org/html/rfc7231#section-6.3.3)|Success response|None
404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|[Error](#schemaerror)
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Unprocessable entity|[Error](#schemaerror)

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
http
</aside>

# legal_documents

Operations on LegalDocument objects.

## RetrieveMerchantLegalDocuments

`GET /legal_documents`

*Retrieve list of legal documents*

Returns a paginated list of all legal documents that currently exist under this merchant

> Example responses

```json
[
  {
    "id": "string",
    "type": "tos",
    "title": "string",
    "content": "string",
    "created_at": "2017-11-03T23:44:19Z",
    "updated_at": "2017-11-03T23:44:19Z"
  }
]
```
```json
{
  "errors": [
    {
      "code": 0,
      "message": "string"
    }
  ]
}
```
<h3 id="RetrieveMerchantLegalDocuments-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success response|Inline
404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|[Error](#schemaerror)

<h3 id="RetrieveMerchantLegalDocuments-responseschema">Response Schema</h3>

Status Code **200**

Name|Type|Required|Description
---|---|---|---|---|
anonymous|[[LegalDocument](#schemalegaldocument)]|false|No description
» id|string(uuid)|false|Pay By Group UUID of this legal document
» type|string|false|Specified by the merchant as either cancellation policy for cancellation and refund terms or tos for all other legal documents. 
» title|string|false|Mechant's title for this legal document
» content|string|false|Full content as provided by the merchant, either in plain text or as a URL
» created_at|string(date-time)|false|When this legal document was added by the merchant
» updated_at|string(date-time)|false|When this legal document was last updated by the merchant



<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
http
</aside>

## CreateMerchantLegalDocument

`POST /legal_documents`

*Add new legal document*

Add a new legal document, which can be attached to any purchase to require its members' acceptances

> Body parameter

```json
{
  "type": "tos",
  "title": "string",
  "content": "string"
}
```
<h3 id="CreateMerchantLegalDocument-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
body|body|object|true|No description
» type|body|string|false|Specified by the merchant as either cancellation policy for cancellation and refund terms
» title|body|string|false|Mechant's title for this legal document
» content|body|string|false|Full content as provided by the merchant, either in plain text or as a URL


#### Enumerated Values

|Parameter|Value|
|---|---|
» type|tos|
» type|cancelation_policy|

##### » type
Specified by the merchant as either cancellation policy for cancellation and refund terms
or tos for all other legal documents

> Example responses

```json
{
  "id": "string",
  "type": "tos",
  "title": "string",
  "content": "string",
  "created_at": "2017-11-03T23:44:19Z",
  "updated_at": "2017-11-03T23:44:19Z"
}
```
```json
{
  "errors": [
    {
      "code": 0,
      "message": "string"
    }
  ]
}
```
<h3 id="CreateMerchantLegalDocument-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Add new legal document|[LegalDocument](#schemalegaldocument)
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Unprocessable entity|[Error](#schemaerror)

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
http
</aside>

## RetrieveMerchantLegalDocument

`GET /legal_documents/{id}`

*Retrieve legal document*

Retrieves the details of a specific legal document

<h3 id="RetrieveMerchantLegalDocument-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|string(uuid)|true|ID of the Legal Document to retrieve


> Example responses

```json
{
  "id": "string",
  "type": "tos",
  "title": "string",
  "content": "string",
  "created_at": "2017-11-03T23:44:19Z",
  "updated_at": "2017-11-03T23:44:19Z"
}
```
```json
{
  "errors": [
    {
      "code": 0,
      "message": "string"
    }
  ]
}
```
<h3 id="RetrieveMerchantLegalDocument-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Retrieve legal document|[LegalDocument](#schemalegaldocument)
404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|[Error](#schemaerror)

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
http
</aside>

## patchLegalDocumentsId

`PATCH /legal_documents/{id}`

*Update a legal document*

Makes changes to a legal document, which will apply to all
future acceptances by members where that document is attached
to a purchase. It will not apply retroactively.

> Body parameter

```json
{
  "type": "tos",
  "title": "string",
  "content": "string"
}
```
<h3 id="patchLegalDocumentsId-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|string(uuid)|true|ID of the Legal Document to update.
body|body|object|true|No description
» type|body|string|false|Specified by the merchant as either cancellation policy for cancellation
» title|body|string|false|Mechant's title for this legal document
» content|body|string|false|Full content as provided by the merchant, either in plain text or as a URL


#### Enumerated Values

|Parameter|Value|
|---|---|
» type|tos|
» type|cancelation_policy|

##### » type
Specified by the merchant as either cancellation policy for cancellation
and refund terms or tos for all other legal documents

> Example responses

```json
{
  "id": "string",
  "type": "tos",
  "title": "string",
  "content": "string",
  "created_at": "2017-11-03T23:44:19Z",
  "updated_at": "2017-11-03T23:44:19Z"
}
```
```json
{
  "errors": [
    {
      "code": 0,
      "message": "string"
    }
  ]
}
```
```json
{
  "errors": [
    {
      "code": 0,
      "message": "string"
    }
  ]
}
```
<h3 id="patchLegalDocumentsId-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Update a legal document|[LegalDocument](#schemalegaldocument)
404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|[Error](#schemaerror)
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Unprocessable entity|[Error](#schemaerror)

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
http
</aside>

# consumer_field_templates

Operations on ConsumerFieldTemplate objects.

## CreateConsumerFieldTemplate

`POST /consumer_field_templates`

*Creates a new consumer field template*

Creates a new consumer field template

> Body parameter

```json
{
  "options": [
    {
      "type": "string",
      "value": "string"
    }
  ],
  "name": "string",
  "label": "string",
  "description": "string",
  "type": "text",
  "order": 0,
  "scope": "member",
  "default_value": "string",
  "default": true,
  "required": true
}
```
<h3 id="CreateConsumerFieldTemplate-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
body|body|object|true|No description
» name|body|string|false|A unique name for the template.
» label|body|string|false|Text to display as the field label.
» description|body|string|false|A description for the template
» type|body|string|false|Type of field to display for this template.
» order|body|integer(int32)|false|Order in which the template should be displayed.
» scope|body|string|false|Whether the template is at the member level, or purchase level.
» default_value|body|string|false|Default value to use for the template.
» default|body|boolean|false|Whether the template should be default or not.
» required|body|boolean|false|Whether the template is required or not.
» options|body|[object]|false|Array of options to use for a list template.
»» type|body|string|false|Option type
»» value|body|string|false|Option value


#### Enumerated Values

|Parameter|Value|
|---|---|
» type|text|
» type|textarea|
» type|datetime|
» type|address|
» type|single_select|
» type|multi_select|
» scope|member|
» scope|purchase|

> Example responses

```json
{
  "id": "string",
  "name": "string",
  "label": "string",
  "description": "string",
  "type": "text",
  "default_value": "string",
  "options": [
    {
      "type": "text",
      "value": "string"
    }
  ],
  "order": 0,
  "scope": "member",
  "default": true,
  "special": true,
  "required": true
}
```
```json
{
  "errors": [
    {
      "code": 0,
      "message": "string"
    }
  ]
}
```
<h3 id="CreateConsumerFieldTemplate-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success response|[ConsumerFieldTemplate](#schemaconsumerfieldtemplate)
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Unprocessable entity|[Error](#schemaerror)

<aside class="warning">
To perform this operation, you must be authenticated by means of one of the following methods:
http
</aside>

# Schemas

## Purchase

<a name="schemapurchase"></a>

```json
{
  "id": "string",
  "slug": "string",
  "merchant": {
    "id": "string",
    "unique_name": "string",
    "display_name": "string",
    "support_email": "user@example.com",
    "support_phone": "string",
    "logo_url": "string",
    "defaults": {
      "currency_code": "string",
      "language_code": "string",
      "timezone_code": "string",
      "product_image_url": "string"
    }
  },
  "status": "created",
  "refund_status": "none",
  "processing_refund": true,
  "tipped": true,
  "auto_pilot_enabled": true,
  "auto_pilot_trigger_slots": 0,
  "consumer_fields": [
    {
      "name": "string",
      "label": "string",
      "description": "string",
      "type": "text",
      "settings": {},
      "scope": "member",
      "default_value": "string"
    }
  ],
  "consumer_field_values": [
    {
      "name": "string",
      "scope": "member",
      "required": true
    }
  ],
  "consumer_field_schemas": [
    {
      "id": "string",
      "name": "string",
      "label": "string",
      "scope": "member",
      "required": true,
      "type": "text"
    }
  ],
  "has_consumer_field_schemas": true,
  "currency_code": "string",
  "payment_destination_id": "string",
  "currency_config": {
    "supported_payment_sources": [
      {
        "type": "credit_card",
        "unsupported_cards": [
          "string"
        ]
      }
    ]
  },
  "payments": [
    {
      "id": "string",
      "status": "pending",
      "number": 0,
      "percentage": 1,
      "due_deadline": "2017-11-03T23:44:19Z",
      "paid_at": "2017-11-03T23:44:19Z",
      "accepted_at": "2017-11-03T23:44:19Z",
      "submitted_at": "2017-11-03T23:44:19Z",
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "conversion_rate": 0,
      "processing_currency": "string",
      "failed": true,
      "payout_failed": true
    }
  ],
  "current_payment": {
    "id": "string",
    "status": "pending",
    "number": 0,
    "percentage": 1,
    "due_deadline": "2017-11-03T23:44:19Z",
    "paid_at": "2017-11-03T23:44:19Z",
    "accepted_at": "2017-11-03T23:44:19Z",
    "submitted_at": "2017-11-03T23:44:19Z",
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "conversion_rate": 0,
    "processing_currency": "string",
    "failed": true,
    "payout_failed": true
  },
  "next_payment_due_deadline": "2017-11-03T23:44:19Z",
  "cost_range": [
    {
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "min_slots": 0,
      "max_slots": 0
    }
  ],
  "current_product_cost_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "current_total_cost_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "max_product_cost_by_slots": {
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "min_slots": 0,
    "max_slots": 0
  },
  "min_product_cost_by_slots": {
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "min_slots": 0,
    "max_slots": 0
  },
  "max_product_cost_by_amount": {
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "min_slots": 0,
    "max_slots": 0
  },
  "fees_structure": {
    "currency_code": "string",
    "payment_destination_type": "bank_account",
    "consumer_fees": {
      "per_share": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "per_share_max": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "per_share_min": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "percentage": 1
    },
    "merchant_service_fees": {
      "per_share": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "per_purchase_max": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "percentage": 1
    },
    "merchant_processing_fees": {
      "per_transaction": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "percentage": 1
    }
  },
  "apply_consumer_fee_to_organizer": true,
  "product": {
    "images": [
      {
        "name": "string",
        "version": "string",
        "url": "string"
      }
    ],
    "default_image_url": "string",
    "allowed_split_types": "even_split",
    "cost_type": "total",
    "costs": [
      {
        "amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "min_slots": 0,
        "max_slots": 0
      }
    ],
    "description": "string",
    "name": "string",
    "end_datetime": "2017-11-03T23:44:19Z",
    "start_datetime": "2017-11-03T23:44:19Z",
    "external_purchase_id": "string",
    "inventory_id": "string",
    "link": "string",
    "max_slots": 0,
    "min_slots": 0,
    "legal_documents": [
      {
        "id": "string",
        "type": "tos",
        "title": "string",
        "content": "string",
        "created_at": "2017-11-03T23:44:19Z",
        "updated_at": "2017-11-03T23:44:19Z"
      }
    ]
  },
  "group": {
    "commit_deadline": "2017-11-03T23:44:19Z",
    "max_slots": 0,
    "min_slots": 0,
    "min_contribution": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "organizer_email": "user@example.com",
    "organizer_full_name": "string",
    "legal_document_ids": [
      "string"
    ],
    "split_type": "even_split"
  },
  "memberships": [
    {
      "id": "string",
      "status": "holdout",
      "refund_status": "none",
      "failed": true,
      "short": true,
      "role": "organizer",
      "claimed_slots": 0,
      "opt_in_marketing": true,
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "share_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "fees": {
        "consumer_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "merchant_service_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        }
      },
      "consumer_field_values": {
        "name": "string",
        "scope": "member",
        "required": true
      },
      "allowed_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "allowed_share_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "allowed_fees": {
        "consumer_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "merchant_service_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        }
      },
      "max_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "max_share_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "max_fees": {
        "consumer_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "merchant_service_fee": {
          "amount_cents": 0,
          "currency_code": "string"
        }
      },
      "collected_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "collected_share_amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "current_contribution": {
        "id": "string",
        "status": "created",
        "refund_status": "none",
        "amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "share_amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "fees": {
          "consumer_fee": {
            "amount_cents": 0,
            "currency_code": "string"
          },
          "merchant_service_fee": {
            "amount_cents": 0,
            "currency_code": "string"
          }
        },
        "charged_at": "2017-11-03T23:44:19Z",
        "failed_at": "2017-11-03T23:44:19Z",
        "created_at": "string"
      },
      "user": {
        "id": "string",
        "email": "user@example.com",
        "full_name": "string",
        "first_name": "string",
        "last_name": "string",
        "avatar_url": "string",
        "language_code": "string",
        "created_at": "string"
      },
      "purchase_id": "string",
      "payment_source": {
        "id": "string",
        "name": "string",
        "type": "string",
        "info": {
          "account_name": "string",
          "account_number": "string",
          "account_holder_type": "string"
        },
        "created_at": "2017-11-03T23:44:19Z"
      },
      "committed_at": "2017-11-03T23:44:19Z",
      "created_at": "2017-11-03T23:44:19Z"
    }
  ],
  "collected_shares_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "committed_shares_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "committed_slots": 0,
  "needed_amount_to_current_payment": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "needed_slots_to_min": 0,
  "product_or_group_max_slots": 0,
  "product_or_group_min_slots": 0,
  "language_code": "string",
  "created_at": "2017-11-03T23:44:19Z"
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
id|string(uuid)|false|Pay By Group UUID for this Purchase used for API calls
slug|string|false|Short, unique identifier of this Purchase for easy reference in the Business Portal and with end users 
merchant|[Merchant](#schemamerchant)|false|No description
» id|string(uuid)|false|Unique ID for the merchant.
» unique_name|string|false|Unique Pay By Group-assigned slug to identify this merchant
» display_name|string|false|Display name chosen by merchant for end users to see
» support_email|string(email)|false|Email provided for end users to contant the merchant
» support_phone|string|false|Phone provided for end users to contant the merchant
» logo_url|string|false|Logo provided by the merchant for display to end users
» defaults|[MerchantDefaults](#schemamerchantdefaults)|false|No description
»» currency_code|string|false|Default currency code for this merchant, which applies to new purchases where a currency is not specified 
»» language_code|string|false|Default language for this merchant, which applies to new purchases where a default language is not specified 
»» timezone_code|string|false|Default timezone code for this merchant, which applies to new datetimes created under the merchant's purchases where a time is not specified. 
»» product_image_url|string|false|URL of the default image for this merchant, which applies to new purchases where a purchase image is not specified. 
status|string|false|Current status of the purchase. One of: - created Purchase has been created by the Merchant. - active Purchase has been claimed by an organizer and is in process. - completed All payments have been successfully paid out to the Merchant for this Purchase. - canceled The Purchase has been canceled by the merchant or organizer and is not recoverable. 
refund_status|string|false|Status that determines whether the Purchase is partially or fully refunded. One of: - none None of the Purchase's Memberships were refunded. - partial Some of the Purchase's Memberships were partially or fully refunded. - full All of the Purchase's Memberships were fully refunded. 
processing_refund|boolean|false|Determines whether or not a refund is being processed for the purchase.
tipped|boolean|false|The minimum required slots have been claimed for the organizer to submit payment
auto_pilot_enabled|boolean|false|The organizer has chosen to have payments triggered automatically as soon as the trigger_slots level they set is reached 
auto_pilot_trigger_slots|integer(int32)|false|The number of slots set by the organizer, which when reached, will automatically trigger payment submission 
has_consumer_field_schemas|boolean|false|Whether or not this purchase has any consumer field schema declared.
currency_code|string|false|3-letter currency code for all money values related to the Purchase
payment_destination_id|string(uuid)|false|ID of the payment destination that will receive all future payments made under this Purchase.
currency_config|object|false|All unsupported payment source types by this Purchase's payment destination, which members cannot use for their contributions 
» supported_payment_sources|[object]|false|List of supported payment sources based on the currency of this Purchase
»» type|string|false|Type of the supported payment source
»» unsupported_cards|[string]|false|List of unsupported credit cards for this particular payment source.
current_payment|[Payment](#schemapayment)|false|No description
» id|string(uuid)|false|Pay By Group UUID for this payment
» status|string|false|One of: - pending A planned future payment on the purchase. - active The currently active, next payment to be paid on the purchase - authorizing The constituent contributions that comprise this   payment are in the process of having their funds verified. - authorized All funds have been verified for this payment and it   awaits acceptance by the merchant. - captured All funds have been taken from group members for the   purchase and are awaiting payout to the merchant. - processing_payout The payout to the merchant is in process. - canceled This payment has been canceled. - paid All funds are paid out to the Payout Account. 
» number|integer(int32)|false|Number of this payment in the overall sequence of the purchase. It is 0 if the purchase has only 1 payment. 
» percentage|integer(int32)|false|Percent of the total purchase cost due for this payment, which must be an integer. All payments on a purchase must sum to 100. 
» due_deadline|string(date-time)|false|Datetime by when this payment must be submitted to the merchant for the purchase to be valid. It is required for all payments after the first payment but may be passed for the first, or only, payment as well. 
» paid_at|string(date-time)|false|Timestamp when the payment is paid out to the merchant
» accepted_at|string(date-time)|false|Timestamp when the payment is accepted by the merchant
» submitted_at|string(date-time)|false|Timestamp when the payment is originally submitted by the organizer
» amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» conversion_rate|number(float)|false|If the currency of the purchase differs from the required currency of the payment destination then this is the conversion rate used to determine the transacted amount. 
» processing_currency|string|false|The required currency of the payment destination, which is the currency in which all transactions related to this payment occur 
» failed|boolean|false|true if any of the contributions under this payment are currently in a failed state
» payout_failed|boolean|false|true if the last attempt to perform a payout failed
next_payment_due_deadline|string(date-time)|false|This is the next due deadline set by the merchant for an upcoming payment
current_product_cost_amount|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value
current_total_cost_amount|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value
max_product_cost_by_slots|[ProductCost](#schemaproductcost)|false|No description
» amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» min_slots|integer(int32)|false|Minimum number of slots that must be claimed by group members before the Purchase can be made at the amount specified for this range. 
» max_slots|integer(int32)|false|Maximum allowed number of slots that may be claimed by group members at the amount specified for this range. 
min_product_cost_by_slots|[ProductCost](#schemaproductcost)|false|No description
» amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» min_slots|integer(int32)|false|Minimum number of slots that must be claimed by group members before the Purchase can be made at the amount specified for this range. 
» max_slots|integer(int32)|false|Maximum allowed number of slots that may be claimed by group members at the amount specified for this range. 
max_product_cost_by_amount|[ProductCost](#schemaproductcost)|false|No description
» amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» min_slots|integer(int32)|false|Minimum number of slots that must be claimed by group members before the Purchase can be made at the amount specified for this range. 
» max_slots|integer(int32)|false|Maximum allowed number of slots that may be claimed by group members at the amount specified for this range. 
fees_structure|[PurchaseFeesStructure](#schemapurchasefeesstructure)|false|No description
» currency_code|string|false|3-letter currency code for which this fee structure applies
» payment_destination_type|string|false|Payment destination identifier for which this fee structure applies
» consumer_fees|[ConsumerFeesStructure](#schemaconsumerfeesstructure)|false|No description
»» per_share|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» per_share_max|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» per_share_min|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» percentage|integer(int32)|false|Percentage applied to member's total share to determine fee
» merchant_service_fees|[MerchantServiceFeesStructure](#schemamerchantservicefeesstructure)|false|No description
»» per_share|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» per_purchase_max|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» percentage|integer(int32)|false|Percentage fee applied to each member's share
» merchant_processing_fees|[MerchantProcessingFeesStructure](#schemamerchantprocessingfeesstructure)|false|No description
»» per_transaction|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» percentage|integer(int32)|false|Percentage fee for each successful transaction sent through Pay By Group
apply_consumer_fee_to_organizer|boolean|false|Tells if consumer fee applies to the purchase's organizer
product|[Product](#schemaproduct)|false|No description
» default_image_url|string|false|The primary or default image for this product
» cost_type|string|false|Cost type that determines whether the product_costs amount(s) are: - per_slot The amount is per slot claimed in the Purchase so the   total amount paid to the merchant is a function of the number of   slots claimed by group members. - total A single total amount so long as the number of slots claimed   is in the allowed range for that amount. 
» description|string|false|Description of the product for this Purchase
» name|string|false|Name of the product being purchased as it should be shown to end users
» end_datetime|string(date-time)|false|End date time for the product being purchased (e.g. check-out date time, flight arrival date time, or activity ending time) 
» start_datetime|string(date-time)|false|Start date time for the product being purchased (e.g. check-in date time, flight departure date time, or event starting time) 
» external_purchase_id|string|false|ID supplied by the merchant that identifies this Purchase (e.g. order or booking) in the merchant's system 
» inventory_id|string|false|Inventory ID supplied by the merchant that identifies the product being bought in this Purchase (e.g. SKU or property ID) 
» link|string|false|Link to the product being purchased on the merchant's (or other third party's) website
» max_slots|integer(int32)|false|The maximum possible slots allowed by the merchant based on product_costs
» min_slots|integer(int32)|false|The minimum possible slots allowed by the merchant based on product_costs
» images|[[Image](#schemaimage)]|false|The set of images for this product
»» name|string|false|Filename of the image as provided by the merchant
»» version|string|false|Version of the image generated by PBG
»» url|string|false|No description
» allowed_split_types|[string]|false|Array of allowed split types
» costs|[[ProductCost](#schemaproductcost)]|false|The set of product_costs and the optional allowed range(s) of slots for each provided by the merchant 
»» amount|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» min_slots|integer(int32)|false|Minimum number of slots that must be claimed by group members before the Purchase can be made at the amount specified for this range. 
»» max_slots|integer(int32)|false|Maximum allowed number of slots that may be claimed by group members at the amount specified for this range. 
» legal_documents|[[LegalDocument](#schemalegaldocument)]|false|All legal documents attached to this purchase that must be agreed to by the group members
»» id|string(uuid)|false|Pay By Group UUID of this legal document
»» type|string|false|Specified by the merchant as either cancellation policy for cancellation and refund terms or tos for all other legal documents. 
»» title|string|false|Mechant's title for this legal document
»» content|string|false|Full content as provided by the merchant, either in plain text or as a URL
»» created_at|string(date-time)|false|When this legal document was added by the merchant
»» updated_at|string(date-time)|false|When this legal document was last updated by the merchant
group|[Group](#schemagroup)|false|No description
» commit_deadline|string(date-time)|false|Pay By Group-generated deadline that encourages invitees to commit to the group quickly. It auto-extends unless overriden by the merchant or organizer 
» max_slots|integer(int32)|false|The organizer-specified value for the maximum number of slots they will allow to be claimed. It must be within the bounds allowed by the merchant. 
» min_slots|integer(int32)|false|The organizer-specified value for the minimum number of slots they require to be claimed. It must be within the bounds allowed by the merchant. 
» min_contribution|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» organizer_email|string(email)|false|Email of the expected organizer as provided by the merchant
» organizer_full_name|string|false|Full name of the expected organizer as provided by the merchant
» split_type|string|false|Splitting type chosen by the organizer for how to divide the cost among group members. One of: - even_split Only compatible with total cost_type and means the   Purchase amount is split evenly across each slot claimed. - specified_per_person Only compatible with total cost_type and   means each member may pay a different amount. - fixed_per_person Only compatible with per_slot cost_type and means   each group member pays a fixed amount per slot they claim. 
» legal_document_ids|[string]|false|Array of legal document IDs that must be accepted by the members in this purchase
collected_shares_amount|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value
committed_shares_amount|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value
committed_slots|integer(int32)|false|Sum of all slots group members have claimed in the Purchase at this point
needed_amount_to_current_payment|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value
needed_slots_to_min|integer(int32)|false|Number of slots group members must claim in order to meet the minimum required to submit the current payment 
product_or_group_max_slots|integer(int32)|false|The active minimum number of slots that must be claimed based on the parameters set by the merchant and organizer 
product_or_group_min_slots|integer(int32)|false|The active maximum number of slots that are allowed to be claimed based on the parameters set by the merchant and organizer 
language_code|string|false|Default language for this purchase. It is going to be used in the claim and commit steps; and as one of the fallbacks when detecting what language to show to the user 
created_at|string(date-time)|false|Timestamp of when the Purchase was first created by the merchant
consumer_fields|[[ConsumerField](#schemaconsumerfield)]|false|Array of consumer fields for this Purchase
» name|string|false|No description
» label|string|false|No description
» description|string|false|No description
» type|string|false|No description
» settings|object|false|No description
» scope|string|false|No description
» default_value|string|false|No description
consumer_field_values|[[ConsumerFieldValue](#schemaconsumerfieldvalue)]|false|Array of values for each of the consumer fields defined.
» name|string|false|Name of the schema
» scope|string|false|One of member or purchase.
» required|boolean|false|Whether the schema field should be required or not.
consumer_field_schemas|[[ConsumerFieldSchema](#schemaconsumerfieldschema)]|false|List of consumer field schemas to use for the purchase
» id|string(uuid)|false|No description
» name|string|false|No description
» label|string|false|No description
» scope|string|false|Any of member or purchase.
» required|boolean|false|Whether the field for this schema should be required or not.
» type|string|false|No description
payments|[[Payment](#schemapayment)]|false|Full payment schedule as set by the merchant for this Purchase
» id|string(uuid)|false|Pay By Group UUID for this payment
» status|string|false|One of: - pending A planned future payment on the purchase. - active The currently active, next payment to be paid on the purchase - authorizing The constituent contributions that comprise this   payment are in the process of having their funds verified. - authorized All funds have been verified for this payment and it   awaits acceptance by the merchant. - captured All funds have been taken from group members for the   purchase and are awaiting payout to the merchant. - processing_payout The payout to the merchant is in process. - canceled This payment has been canceled. - paid All funds are paid out to the Payout Account. 
» number|integer(int32)|false|Number of this payment in the overall sequence of the purchase. It is 0 if the purchase has only 1 payment. 
» percentage|integer(int32)|false|Percent of the total purchase cost due for this payment, which must be an integer. All payments on a purchase must sum to 100. 
» due_deadline|string(date-time)|false|Datetime by when this payment must be submitted to the merchant for the purchase to be valid. It is required for all payments after the first payment but may be passed for the first, or only, payment as well. 
» paid_at|string(date-time)|false|Timestamp when the payment is paid out to the merchant
» accepted_at|string(date-time)|false|Timestamp when the payment is accepted by the merchant
» submitted_at|string(date-time)|false|Timestamp when the payment is originally submitted by the organizer
» amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» conversion_rate|number(float)|false|If the currency of the purchase differs from the required currency of the payment destination then this is the conversion rate used to determine the transacted amount. 
» processing_currency|string|false|The required currency of the payment destination, which is the currency in which all transactions related to this payment occur 
» failed|boolean|false|true if any of the contributions under this payment are currently in a failed state
» payout_failed|boolean|false|true if the last attempt to perform a payout failed
cost_range|[[ProductCost](#schemaproductcost)]|false|The range of possible costs for this product based on the product_costs merchant provides
» amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» min_slots|integer(int32)|false|Minimum number of slots that must be claimed by group members before the Purchase can be made at the amount specified for this range. 
» max_slots|integer(int32)|false|Maximum allowed number of slots that may be claimed by group members at the amount specified for this range. 
memberships|[[Membership](#schemamembership)]|false|Array that includes all members in this Purchase without their contributions.
» id|string|false|Pay By Group UUID for this membership
» status|string|false|One of: - holdout (user has been invited but not joined the group); - committed (user has joined the group and whether they have been charged is in the contribution object); 
» refund_status|string|false|Status that determines whether the Membership is partially or fully refunded. One of: - none (none of the Membership's Contributions were refunded). - partial (some of the Membership's Contributions were partially   or fully refunded). - full (all of the Membership's Contributions were fully refunded). 
» failed|boolean|false|User is currently in the group with a failed payment method, which is preventing the purchase from completing 
» short|boolean|false|The user is currently in the group but has not agreed to pay their new required share amount due to updates to the purchase. 
» role|string|false|Either organizer or invitee
» claimed_slots|integer(int32)|false|Number of slots the member has claimed in the group. Defaults to 1 if none is selected by the user.
» opt_in_marketing|boolean|false|true if the user has opted in to receive marketing communication from the merchant. Otherwise false.
» amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» share_amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» fees|[Fees](#schemafees)|false|No description
»» consumer_fee|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» merchant_service_fee|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
» consumer_field_values|[ConsumerFieldValue](#schemaconsumerfieldvalue)|false|No description
»» name|string|false|Name of the schema
»» scope|string|false|One of member or purchase.
»» required|boolean|false|Whether the schema field should be required or not.
» allowed_amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» allowed_share_amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» allowed_fees|[Fees](#schemafees)|false|No description
»» consumer_fee|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» merchant_service_fee|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
» max_amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» max_share_amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» max_fees|[Fees](#schemafees)|false|No description
»» consumer_fee|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» merchant_service_fee|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
» collected_amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» collected_share_amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» current_contribution|[Contribution](#schemacontribution)|false|No description
»» id|string|false|UUID of this contribution
»» status|string|false|Current status of the contribution, any of created, authorized, captured, holdout or failed
»» refund_status|string|false|Status that determines whether the Contribution is partially or fully refunded. One of: - none (none of the Contribution's Transactions were refunded). - partial (some of the Contribution's Transactions were partially   or fully refunded). - full (all of the Contribution's Transactions were fully refunded). 
»» amount|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» share_amount|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» fees|[Fees](#schemafees)|false|No description
»»» consumer_fee|[Money](#schemamoney)|false|No description
»»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»»» currency_code|string|false|3-letter currency code attached to every money value
»»» merchant_service_fee|[Money](#schemamoney)|false|No description
»»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»»» currency_code|string|false|3-letter currency code attached to every money value
»» charged_at|string(date-time)|false|Timestamp of when this contibution was charged
»» failed_at|string(date-time)|false|Timestamp of when this contribution most recently failed
»» created_at|string|false|Timestamp when the record of this contribution was first created, which is not necessarily when it was charged 
» user|[User](#schemauser)|false|No description
»» id|string(uuid)|false|Pay By Group UUID for this user
»» email|string(email)|false|User's email address
»» full_name|string|false|User's full name
»» first_name|string|false|User's first name
»» last_name|string|false|User's last name
»» avatar_url|string|false|URL of the User's avatar
»» language_code|string|false|The preferred language selected by this user
»» created_at|string(uuid)|false|No description
» purchase_id|string(uuid)|false|Pay By Group slug of the purchase to which this membership is tied
» payment_source|[PaymentSource](#schemapaymentsource)|false|No description
»» id|string(uuid)|false|Pay By Group UUID of this payment source
»» name|string|false|Full name of this payment source's owner
»» type|string|false|Describes the type of payment source, any of credit_card or bank_account
»» info|object|false|Bank account information of this payment source
»»» account_name|string|false|Listed name of the account holder
»»» account_number|string|false|Account number
»»» account_holder_type|string|false|Either a business or individual
»» created_at|string(date-time)|false|Timestamp when the payment source was first added to the system
» committed_at|string(date-time)|false|Timestamp of when the member agreed to pay into the purchase
» created_at|string(date-time)|false|When the membership was first created


#### Enumerated Values

|Property|Value|
|---|---|
status|created|
status|active|
status|completed|
status|canceled|
refund_status|none|
refund_status|partial|
refund_status|full|
»» type|credit_card|
» status|pending|
» status|active|
» status|authorizing|
» status|authorized|
» status|captured|
» status|processing_payout|
» status|canceled|
» status|paid|
» payment_destination_type|bank_account|
» payment_destination_type|payment_gateway|
» cost_type|total|
» cost_type|per_slot|
»» type|tos|
»» type|cancelation_policy|
» split_type|even_split|
» split_type|specified_per_person|
» split_type|fixed_per_person|
» type|text|
» type|textarea|
» type|datetime|
» type|address|
» type|single_select multi_select|
» scope|member|
» scope|purchase|
» scope|member|
» scope|purchase|
» scope|member|
» scope|purchase|
» type|text|
» type|textarea|
» type|datetime|
» type|address|
» type|single_select multi_select|
» status|pending|
» status|active|
» status|authorizing|
» status|authorized|
» status|captured|
» status|processing_payout|
» status|canceled|
» status|paid|
» status|holdout|
» status|committed|
» refund_status|none|
» refund_status|partial|
» refund_status|full|
» role|organizer|
» role|invitee|
»» scope|member|
»» scope|purchase|
»» status|created|
»» status|authorized|
»» status|captured|
»» status|holdout|
»» status|failed|
»» refund_status|none|
»» refund_status|partial|
»» refund_status|full|


## Merchant

<a name="schemamerchant"></a>

```json
{
  "id": "string",
  "unique_name": "string",
  "display_name": "string",
  "support_email": "user@example.com",
  "support_phone": "string",
  "logo_url": "string",
  "defaults": {
    "currency_code": "string",
    "language_code": "string",
    "timezone_code": "string",
    "product_image_url": "string"
  }
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
id|string(uuid)|false|Unique ID for the merchant.
unique_name|string|false|Unique Pay By Group-assigned slug to identify this merchant
display_name|string|false|Display name chosen by merchant for end users to see
support_email|string(email)|false|Email provided for end users to contant the merchant
support_phone|string|false|Phone provided for end users to contant the merchant
logo_url|string|false|Logo provided by the merchant for display to end users
defaults|[MerchantDefaults](#schemamerchantdefaults)|false|No description
» currency_code|string|false|Default currency code for this merchant, which applies to new purchases where a currency is not specified 
» language_code|string|false|Default language for this merchant, which applies to new purchases where a default language is not specified 
» timezone_code|string|false|Default timezone code for this merchant, which applies to new datetimes created under the merchant's purchases where a time is not specified. 
» product_image_url|string|false|URL of the default image for this merchant, which applies to new purchases where a purchase image is not specified. 



## MerchantDefaults

<a name="schemamerchantdefaults"></a>

```json
{
  "currency_code": "string",
  "language_code": "string",
  "timezone_code": "string",
  "product_image_url": "string"
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
currency_code|string|false|Default currency code for this merchant, which applies to new purchases where a currency is not specified 
language_code|string|false|Default language for this merchant, which applies to new purchases where a default language is not specified 
timezone_code|string|false|Default timezone code for this merchant, which applies to new datetimes created under the merchant's purchases where a time is not specified. 
product_image_url|string|false|URL of the default image for this merchant, which applies to new purchases where a purchase image is not specified. 



## ConsumerField

<a name="schemaconsumerfield"></a>

```json
{
  "name": "string",
  "label": "string",
  "description": "string",
  "type": "text",
  "settings": {},
  "scope": "member",
  "default_value": "string"
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
name|string|false|No description
label|string|false|No description
description|string|false|No description
type|string|false|No description
settings|object|false|No description
scope|string|false|No description
default_value|string|false|No description


#### Enumerated Values

|Property|Value|
|---|---|
type|text|
type|textarea|
type|datetime|
type|address|
type|single_select multi_select|
scope|member|
scope|purchase|


## ConsumerFieldValue

<a name="schemaconsumerfieldvalue"></a>

```json
{
  "name": "string",
  "scope": "member",
  "required": true
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
name|string|false|Name of the schema
scope|string|false|One of member or purchase.
required|boolean|false|Whether the schema field should be required or not.


#### Enumerated Values

|Property|Value|
|---|---|
scope|member|
scope|purchase|


## ConsumerFieldSchema

<a name="schemaconsumerfieldschema"></a>

```json
{
  "id": "string",
  "name": "string",
  "label": "string",
  "scope": "member",
  "required": true,
  "type": "text"
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
id|string(uuid)|false|No description
name|string|false|No description
label|string|false|No description
scope|string|false|Any of member or purchase.
required|boolean|false|Whether the field for this schema should be required or not.
type|string|false|No description


#### Enumerated Values

|Property|Value|
|---|---|
scope|member|
scope|purchase|
type|text|
type|textarea|
type|datetime|
type|address|
type|single_select multi_select|


## Payment

<a name="schemapayment"></a>

```json
{
  "id": "string",
  "status": "pending",
  "number": 0,
  "percentage": 1,
  "due_deadline": "2017-11-03T23:44:19Z",
  "paid_at": "2017-11-03T23:44:19Z",
  "accepted_at": "2017-11-03T23:44:19Z",
  "submitted_at": "2017-11-03T23:44:19Z",
  "amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "conversion_rate": 0,
  "processing_currency": "string",
  "failed": true,
  "payout_failed": true
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
id|string(uuid)|false|Pay By Group UUID for this payment
status|string|false|One of: - pending A planned future payment on the purchase. - active The currently active, next payment to be paid on the purchase - authorizing The constituent contributions that comprise this   payment are in the process of having their funds verified. - authorized All funds have been verified for this payment and it   awaits acceptance by the merchant. - captured All funds have been taken from group members for the   purchase and are awaiting payout to the merchant. - processing_payout The payout to the merchant is in process. - canceled This payment has been canceled. - paid All funds are paid out to the Payout Account. 
number|integer(int32)|false|Number of this payment in the overall sequence of the purchase. It is 0 if the purchase has only 1 payment. 
percentage|integer(int32)|false|Percent of the total purchase cost due for this payment, which must be an integer. All payments on a purchase must sum to 100. 
due_deadline|string(date-time)|false|Datetime by when this payment must be submitted to the merchant for the purchase to be valid. It is required for all payments after the first payment but may be passed for the first, or only, payment as well. 
paid_at|string(date-time)|false|Timestamp when the payment is paid out to the merchant
accepted_at|string(date-time)|false|Timestamp when the payment is accepted by the merchant
submitted_at|string(date-time)|false|Timestamp when the payment is originally submitted by the organizer
amount|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value
conversion_rate|number(float)|false|If the currency of the purchase differs from the required currency of the payment destination then this is the conversion rate used to determine the transacted amount. 
processing_currency|string|false|The required currency of the payment destination, which is the currency in which all transactions related to this payment occur 
failed|boolean|false|true if any of the contributions under this payment are currently in a failed state
payout_failed|boolean|false|true if the last attempt to perform a payout failed


#### Enumerated Values

|Property|Value|
|---|---|
status|pending|
status|active|
status|authorizing|
status|authorized|
status|captured|
status|processing_payout|
status|canceled|
status|paid|


## Money

<a name="schemamoney"></a>

```json
{
  "amount_cents": 0,
  "currency_code": "string"
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
currency_code|string|false|3-letter currency code attached to every money value



## ProductCost

<a name="schemaproductcost"></a>

```json
{
  "amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "min_slots": 0,
  "max_slots": 0
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
amount|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value
min_slots|integer(int32)|false|Minimum number of slots that must be claimed by group members before the Purchase can be made at the amount specified for this range. 
max_slots|integer(int32)|false|Maximum allowed number of slots that may be claimed by group members at the amount specified for this range. 



## PurchaseFeesStructure

<a name="schemapurchasefeesstructure"></a>

```json
{
  "currency_code": "string",
  "payment_destination_type": "bank_account",
  "consumer_fees": {
    "per_share": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "per_share_max": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "per_share_min": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "percentage": 1
  },
  "merchant_service_fees": {
    "per_share": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "per_purchase_max": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "percentage": 1
  },
  "merchant_processing_fees": {
    "per_transaction": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "percentage": 1
  }
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
currency_code|string|false|3-letter currency code for which this fee structure applies
payment_destination_type|string|false|Payment destination identifier for which this fee structure applies
consumer_fees|[ConsumerFeesStructure](#schemaconsumerfeesstructure)|false|No description
» per_share|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» per_share_max|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» per_share_min|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» percentage|integer(int32)|false|Percentage applied to member's total share to determine fee
merchant_service_fees|[MerchantServiceFeesStructure](#schemamerchantservicefeesstructure)|false|No description
» per_share|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» per_purchase_max|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» percentage|integer(int32)|false|Percentage fee applied to each member's share
merchant_processing_fees|[MerchantProcessingFeesStructure](#schemamerchantprocessingfeesstructure)|false|No description
» per_transaction|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» percentage|integer(int32)|false|Percentage fee for each successful transaction sent through Pay By Group


#### Enumerated Values

|Property|Value|
|---|---|
payment_destination_type|bank_account|
payment_destination_type|payment_gateway|


## ConsumerFeesStructure

<a name="schemaconsumerfeesstructure"></a>

```json
{
  "per_share": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "per_share_max": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "per_share_min": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "percentage": 1
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
per_share|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value
per_share_max|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value
per_share_min|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value
percentage|integer(int32)|false|Percentage applied to member's total share to determine fee



## MerchantServiceFeesStructure

<a name="schemamerchantservicefeesstructure"></a>

```json
{
  "per_share": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "per_purchase_max": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "percentage": 1
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
per_share|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value
per_purchase_max|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value
percentage|integer(int32)|false|Percentage fee applied to each member's share



## MerchantProcessingFeesStructure

<a name="schemamerchantprocessingfeesstructure"></a>

```json
{
  "per_transaction": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "percentage": 1
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
per_transaction|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value
percentage|integer(int32)|false|Percentage fee for each successful transaction sent through Pay By Group



## Product

<a name="schemaproduct"></a>

```json
{
  "images": [
    {
      "name": "string",
      "version": "string",
      "url": "string"
    }
  ],
  "default_image_url": "string",
  "allowed_split_types": "even_split",
  "cost_type": "total",
  "costs": [
    {
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "min_slots": 0,
      "max_slots": 0
    }
  ],
  "description": "string",
  "name": "string",
  "end_datetime": "2017-11-03T23:44:19Z",
  "start_datetime": "2017-11-03T23:44:19Z",
  "external_purchase_id": "string",
  "inventory_id": "string",
  "link": "string",
  "max_slots": 0,
  "min_slots": 0,
  "legal_documents": [
    {
      "id": "string",
      "type": "tos",
      "title": "string",
      "content": "string",
      "created_at": "2017-11-03T23:44:19Z",
      "updated_at": "2017-11-03T23:44:19Z"
    }
  ]
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
default_image_url|string|false|The primary or default image for this product
cost_type|string|false|Cost type that determines whether the product_costs amount(s) are: - per_slot The amount is per slot claimed in the Purchase so the   total amount paid to the merchant is a function of the number of   slots claimed by group members. - total A single total amount so long as the number of slots claimed   is in the allowed range for that amount. 
description|string|false|Description of the product for this Purchase
name|string|false|Name of the product being purchased as it should be shown to end users
end_datetime|string(date-time)|false|End date time for the product being purchased (e.g. check-out date time, flight arrival date time, or activity ending time) 
start_datetime|string(date-time)|false|Start date time for the product being purchased (e.g. check-in date time, flight departure date time, or event starting time) 
external_purchase_id|string|false|ID supplied by the merchant that identifies this Purchase (e.g. order or booking) in the merchant's system 
inventory_id|string|false|Inventory ID supplied by the merchant that identifies the product being bought in this Purchase (e.g. SKU or property ID) 
link|string|false|Link to the product being purchased on the merchant's (or other third party's) website
max_slots|integer(int32)|false|The maximum possible slots allowed by the merchant based on product_costs
min_slots|integer(int32)|false|The minimum possible slots allowed by the merchant based on product_costs
images|[[Image](#schemaimage)]|false|The set of images for this product
» name|string|false|Filename of the image as provided by the merchant
» version|string|false|Version of the image generated by PBG
» url|string|false|No description
allowed_split_types|[string]|false|Array of allowed split types
costs|[[ProductCost](#schemaproductcost)]|false|The set of product_costs and the optional allowed range(s) of slots for each provided by the merchant 
» amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» min_slots|integer(int32)|false|Minimum number of slots that must be claimed by group members before the Purchase can be made at the amount specified for this range. 
» max_slots|integer(int32)|false|Maximum allowed number of slots that may be claimed by group members at the amount specified for this range. 
legal_documents|[[LegalDocument](#schemalegaldocument)]|false|All legal documents attached to this purchase that must be agreed to by the group members
» id|string(uuid)|false|Pay By Group UUID of this legal document
» type|string|false|Specified by the merchant as either cancellation policy for cancellation and refund terms or tos for all other legal documents. 
» title|string|false|Mechant's title for this legal document
» content|string|false|Full content as provided by the merchant, either in plain text or as a URL
» created_at|string(date-time)|false|When this legal document was added by the merchant
» updated_at|string(date-time)|false|When this legal document was last updated by the merchant


#### Enumerated Values

|Property|Value|
|---|---|
cost_type|total|
cost_type|per_slot|
» type|tos|
» type|cancelation_policy|


## Image

<a name="schemaimage"></a>

```json
{
  "name": "string",
  "version": "string",
  "url": "string"
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
name|string|false|Filename of the image as provided by the merchant
version|string|false|Version of the image generated by PBG
url|string|false|No description



## Membership

<a name="schemamembership"></a>

```json
{
  "id": "string",
  "status": "holdout",
  "refund_status": "none",
  "failed": true,
  "short": true,
  "role": "organizer",
  "claimed_slots": 0,
  "opt_in_marketing": true,
  "amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "share_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "fees": {
    "consumer_fee": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "merchant_service_fee": {
      "amount_cents": 0,
      "currency_code": "string"
    }
  },
  "consumer_field_values": {
    "name": "string",
    "scope": "member",
    "required": true
  },
  "allowed_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "allowed_share_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "allowed_fees": {
    "consumer_fee": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "merchant_service_fee": {
      "amount_cents": 0,
      "currency_code": "string"
    }
  },
  "max_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "max_share_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "max_fees": {
    "consumer_fee": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "merchant_service_fee": {
      "amount_cents": 0,
      "currency_code": "string"
    }
  },
  "collected_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "collected_share_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "current_contribution": {
    "id": "string",
    "status": "created",
    "refund_status": "none",
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "share_amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "fees": {
      "consumer_fee": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "merchant_service_fee": {
        "amount_cents": 0,
        "currency_code": "string"
      }
    },
    "charged_at": "2017-11-03T23:44:19Z",
    "failed_at": "2017-11-03T23:44:19Z",
    "created_at": "string"
  },
  "user": {
    "id": "string",
    "email": "user@example.com",
    "full_name": "string",
    "first_name": "string",
    "last_name": "string",
    "avatar_url": "string",
    "language_code": "string",
    "created_at": "string"
  },
  "purchase_id": "string",
  "payment_source": {
    "id": "string",
    "name": "string",
    "type": "string",
    "info": {
      "account_name": "string",
      "account_number": "string",
      "account_holder_type": "string"
    },
    "created_at": "2017-11-03T23:44:19Z"
  },
  "committed_at": "2017-11-03T23:44:19Z",
  "created_at": "2017-11-03T23:44:19Z"
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
id|string|false|Pay By Group UUID for this membership
status|string|false|One of: - holdout (user has been invited but not joined the group); - committed (user has joined the group and whether they have been charged is in the contribution object); 
refund_status|string|false|Status that determines whether the Membership is partially or fully refunded. One of: - none (none of the Membership's Contributions were refunded). - partial (some of the Membership's Contributions were partially   or fully refunded). - full (all of the Membership's Contributions were fully refunded). 
failed|boolean|false|User is currently in the group with a failed payment method, which is preventing the purchase from completing 
short|boolean|false|The user is currently in the group but has not agreed to pay their new required share amount due to updates to the purchase. 
role|string|false|Either organizer or invitee
claimed_slots|integer(int32)|false|Number of slots the member has claimed in the group. Defaults to 1 if none is selected by the user.
opt_in_marketing|boolean|false|true if the user has opted in to receive marketing communication from the merchant. Otherwise false.
amount|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value
share_amount|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value
fees|[Fees](#schemafees)|false|No description
» consumer_fee|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» merchant_service_fee|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
consumer_field_values|[ConsumerFieldValue](#schemaconsumerfieldvalue)|false|No description
» name|string|false|Name of the schema
» scope|string|false|One of member or purchase.
» required|boolean|false|Whether the schema field should be required or not.
allowed_amount|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value
allowed_share_amount|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value
allowed_fees|[Fees](#schemafees)|false|No description
» consumer_fee|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» merchant_service_fee|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
max_amount|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value
max_share_amount|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value
max_fees|[Fees](#schemafees)|false|No description
» consumer_fee|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» merchant_service_fee|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
collected_amount|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value
collected_share_amount|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value
current_contribution|[Contribution](#schemacontribution)|false|No description
» id|string|false|UUID of this contribution
» status|string|false|Current status of the contribution, any of created, authorized, captured, holdout or failed
» refund_status|string|false|Status that determines whether the Contribution is partially or fully refunded. One of: - none (none of the Contribution's Transactions were refunded). - partial (some of the Contribution's Transactions were partially   or fully refunded). - full (all of the Contribution's Transactions were fully refunded). 
» amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» share_amount|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» fees|[Fees](#schemafees)|false|No description
»» consumer_fee|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
»» merchant_service_fee|[Money](#schemamoney)|false|No description
»»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»»» currency_code|string|false|3-letter currency code attached to every money value
» charged_at|string(date-time)|false|Timestamp of when this contibution was charged
» failed_at|string(date-time)|false|Timestamp of when this contribution most recently failed
» created_at|string|false|Timestamp when the record of this contribution was first created, which is not necessarily when it was charged 
user|[User](#schemauser)|false|No description
» id|string(uuid)|false|Pay By Group UUID for this user
» email|string(email)|false|User's email address
» full_name|string|false|User's full name
» first_name|string|false|User's first name
» last_name|string|false|User's last name
» avatar_url|string|false|URL of the User's avatar
» language_code|string|false|The preferred language selected by this user
» created_at|string(uuid)|false|No description
purchase_id|string(uuid)|false|Pay By Group slug of the purchase to which this membership is tied
payment_source|[PaymentSource](#schemapaymentsource)|false|No description
» id|string(uuid)|false|Pay By Group UUID of this payment source
» name|string|false|Full name of this payment source's owner
» type|string|false|Describes the type of payment source, any of credit_card or bank_account
» info|object|false|Bank account information of this payment source
»» account_name|string|false|Listed name of the account holder
»» account_number|string|false|Account number
»» account_holder_type|string|false|Either a business or individual
» created_at|string(date-time)|false|Timestamp when the payment source was first added to the system
committed_at|string(date-time)|false|Timestamp of when the member agreed to pay into the purchase
created_at|string(date-time)|false|When the membership was first created


#### Enumerated Values

|Property|Value|
|---|---|
status|holdout|
status|committed|
refund_status|none|
refund_status|partial|
refund_status|full|
role|organizer|
role|invitee|
» scope|member|
» scope|purchase|
» status|created|
» status|authorized|
» status|captured|
» status|holdout|
» status|failed|
» refund_status|none|
» refund_status|partial|
» refund_status|full|


## Fees

<a name="schemafees"></a>

```json
{
  "consumer_fee": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "merchant_service_fee": {
    "amount_cents": 0,
    "currency_code": "string"
  }
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
consumer_fee|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value
merchant_service_fee|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value



## Contribution

<a name="schemacontribution"></a>

```json
{
  "id": "string",
  "status": "created",
  "refund_status": "none",
  "amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "share_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "fees": {
    "consumer_fee": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "merchant_service_fee": {
      "amount_cents": 0,
      "currency_code": "string"
    }
  },
  "charged_at": "2017-11-03T23:44:19Z",
  "failed_at": "2017-11-03T23:44:19Z",
  "created_at": "string"
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
id|string|false|UUID of this contribution
status|string|false|Current status of the contribution, any of created, authorized, captured, holdout or failed
refund_status|string|false|Status that determines whether the Contribution is partially or fully refunded. One of: - none (none of the Contribution's Transactions were refunded). - partial (some of the Contribution's Transactions were partially   or fully refunded). - full (all of the Contribution's Transactions were fully refunded). 
amount|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value
share_amount|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value
fees|[Fees](#schemafees)|false|No description
» consumer_fee|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» merchant_service_fee|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
charged_at|string(date-time)|false|Timestamp of when this contibution was charged
failed_at|string(date-time)|false|Timestamp of when this contribution most recently failed
created_at|string|false|Timestamp when the record of this contribution was first created, which is not necessarily when it was charged 


#### Enumerated Values

|Property|Value|
|---|---|
status|created|
status|authorized|
status|captured|
status|holdout|
status|failed|
refund_status|none|
refund_status|partial|
refund_status|full|


## User

<a name="schemauser"></a>

```json
{
  "id": "string",
  "email": "user@example.com",
  "full_name": "string",
  "first_name": "string",
  "last_name": "string",
  "avatar_url": "string",
  "language_code": "string",
  "created_at": "string"
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
id|string(uuid)|false|Pay By Group UUID for this user
email|string(email)|false|User's email address
full_name|string|false|User's full name
first_name|string|false|User's first name
last_name|string|false|User's last name
avatar_url|string|false|URL of the User's avatar
language_code|string|false|The preferred language selected by this user
created_at|string(uuid)|false|No description



## PaymentSource

<a name="schemapaymentsource"></a>

```json
{
  "id": "string",
  "name": "string",
  "type": "string",
  "info": {
    "account_name": "string",
    "account_number": "string",
    "account_holder_type": "string"
  },
  "created_at": "2017-11-03T23:44:19Z"
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
id|string(uuid)|false|Pay By Group UUID of this payment source
name|string|false|Full name of this payment source's owner
type|string|false|Describes the type of payment source, any of credit_card or bank_account
info|object|false|Bank account information of this payment source
» account_name|string|false|Listed name of the account holder
» account_number|string|false|Account number
» account_holder_type|string|false|Either a business or individual
created_at|string(date-time)|false|Timestamp when the payment source was first added to the system



## Error

<a name="schemaerror"></a>

```json
{
  "errors": [
    {
      "code": 0,
      "message": "string"
    }
  ]
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
errors|[object]|false|Array of errors returned by the endpoint
» code|integer(int32)|false|Error code to identify the message. Not used at the moment.
» message|string|false|Description of the error.



## Group

<a name="schemagroup"></a>

```json
{
  "commit_deadline": "2017-11-03T23:44:19Z",
  "max_slots": 0,
  "min_slots": 0,
  "min_contribution": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "organizer_email": "user@example.com",
  "organizer_full_name": "string",
  "legal_document_ids": [
    "string"
  ],
  "split_type": "even_split"
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
commit_deadline|string(date-time)|false|Pay By Group-generated deadline that encourages invitees to commit to the group quickly. It auto-extends unless overriden by the merchant or organizer 
max_slots|integer(int32)|false|The organizer-specified value for the maximum number of slots they will allow to be claimed. It must be within the bounds allowed by the merchant. 
min_slots|integer(int32)|false|The organizer-specified value for the minimum number of slots they require to be claimed. It must be within the bounds allowed by the merchant. 
min_contribution|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value
organizer_email|string(email)|false|Email of the expected organizer as provided by the merchant
organizer_full_name|string|false|Full name of the expected organizer as provided by the merchant
split_type|string|false|Splitting type chosen by the organizer for how to divide the cost among group members. One of: - even_split Only compatible with total cost_type and means the   Purchase amount is split evenly across each slot claimed. - specified_per_person Only compatible with total cost_type and   means each member may pay a different amount. - fixed_per_person Only compatible with per_slot cost_type and means   each group member pays a fixed amount per slot they claim. 
legal_document_ids|[string]|false|Array of legal document IDs that must be accepted by the members in this purchase


#### Enumerated Values

|Property|Value|
|---|---|
split_type|even_split|
split_type|specified_per_person|
split_type|fixed_per_person|


## PaymentTransaction

<a name="schemapaymenttransaction"></a>

```json
{
  "id": "string",
  "short_id": "string",
  "parent_id": "string",
  "chargable_type": "string",
  "action": "auth",
  "status": "pending",
  "amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "fees": {
    "consumer_fee": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "merchant_service_fee": {
      "amount_cents": 0,
      "currency_code": "string"
    }
  },
  "payout_account": {
    "id": "string",
    "name": "string",
    "status": "verified",
    "user_id": "string",
    "merchant_id": "string",
    "supported_currency_codes": [
      "string"
    ],
    "currency_configs": "string"
  },
  "payment_gateway": {
    "id": "string",
    "name": "string",
    "merchant_id": "string",
    "supported_currency_codes": [
      "string"
    ]
  },
  "payment_source": {
    "id": "string",
    "name": "string",
    "type": "string",
    "info": {
      "account_name": "string",
      "account_number": "string",
      "account_holder_type": "string"
    },
    "created_at": "2017-11-03T23:44:19Z"
  },
  "created_at": "2017-11-03T23:44:19Z",
  "processing_currency": "string",
  "conversion_rate": 0
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
id|string(uuid)|false|Pay By Group UUID for this transaction
short_id|string|false|Unique ID of this transaction for easy reference
parent_id|string|false|Another transaction related to and replaced by this one - e.g. the credit card authorization for which this transaction is the capture or the capture for which this is the refund. 
chargable_type|string|false|No description
action|string|false|One of: - auth (holds funds or the specified amount on the user's payment   method for later capture). - capture (captures funds that were previously authorized at an   amount = or < the authorized amount). - charge (instantly charges an amount without first making an   authorization). - void (voids a previously created authorization). - refund (refunds a previously created capture or charge). - payout (sends funds to a bank account). 
status|string|false|Oneo of pending, completed or failed
amount|[Money](#schemamoney)|false|No description
» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
» currency_code|string|false|3-letter currency code attached to every money value
fees|[Fees](#schemafees)|false|No description
» consumer_fee|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
» merchant_service_fee|[Money](#schemamoney)|false|No description
»» amount_cents|integer(int32)|false|Format of all money values is in cents where 100 is equivalent to $1.00
»» currency_code|string|false|3-letter currency code attached to every money value
payout_account|[BankAccount](#schemabankaccount)|false|No description
» id|string(uuid)|false|Pay By Group UUID for this bank account
» name|string|false|Displayed name of bank account with last 4 of account number
» status|string|false|verified or unverified depending on whether micro-deposit amounts have confirmed account ownership
» user_id|string(uuid)|false|User that added the bank account
» merchant_id|string(uuid)|false|Merchant this bank account belongs to
» currency_configs|string|false|Set of payment sources supported across all currencies for this bank account. Not all currencies support all payment sources. 
» supported_currency_codes|[string]|false|3-letter currency codes that can be used for credits and debits with this account
payment_gateway|[PaymentGateway](#schemapaymentgateway)|false|No description
» id|string|false|Pay By Group UUID for this payment gateway
» name|string|false|Displayed name of the gateway
» merchant_id|string|false|Merchant this gateway belongs to
» supported_currency_codes|[string]|false|3-letter currency codes that can be used for payments to this gateway
payment_source|[PaymentSource](#schemapaymentsource)|false|No description
» id|string(uuid)|false|Pay By Group UUID of this payment source
» name|string|false|Full name of this payment source's owner
» type|string|false|Describes the type of payment source, any of credit_card or bank_account
» info|object|false|Bank account information of this payment source
»» account_name|string|false|Listed name of the account holder
»» account_number|string|false|Account number
»» account_holder_type|string|false|Either a business or individual
» created_at|string(date-time)|false|Timestamp when the payment source was first added to the system
created_at|string(date-time)|false|Timestamp when the transaction was created
processing_currency|string|false|The currency in which this transaction occurred
conversion_rate|number(float)|false|If the currency of the purchase differs from the required currency of the payout account then this is the conversion rate used to determine the transaction amount. 


#### Enumerated Values

|Property|Value|
|---|---|
action|auth|
action|capture|
action|charge|
action|void|
action|refund|
action|payout|
status|pending|
status|completed|
status|failed|
» status|verified|
» status|unverified|


## BankAccount

<a name="schemabankaccount"></a>

```json
{
  "id": "string",
  "name": "string",
  "status": "verified",
  "user_id": "string",
  "merchant_id": "string",
  "supported_currency_codes": [
    "string"
  ],
  "currency_configs": "string"
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
id|string(uuid)|false|Pay By Group UUID for this bank account
name|string|false|Displayed name of bank account with last 4 of account number
status|string|false|verified or unverified depending on whether micro-deposit amounts have confirmed account ownership
user_id|string(uuid)|false|User that added the bank account
merchant_id|string(uuid)|false|Merchant this bank account belongs to
currency_configs|string|false|Set of payment sources supported across all currencies for this bank account. Not all currencies support all payment sources. 
supported_currency_codes|[string]|false|3-letter currency codes that can be used for credits and debits with this account


#### Enumerated Values

|Property|Value|
|---|---|
status|verified|
status|unverified|


## PaymentGateway

<a name="schemapaymentgateway"></a>

```json
{
  "id": "string",
  "name": "string",
  "merchant_id": "string",
  "supported_currency_codes": [
    "string"
  ]
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
id|string|false|Pay By Group UUID for this payment gateway
name|string|false|Displayed name of the gateway
merchant_id|string|false|Merchant this gateway belongs to
supported_currency_codes|[string]|false|3-letter currency codes that can be used for payments to this gateway



## LegalDocument

<a name="schemalegaldocument"></a>

```json
{
  "id": "string",
  "type": "tos",
  "title": "string",
  "content": "string",
  "created_at": "2017-11-03T23:44:19Z",
  "updated_at": "2017-11-03T23:44:19Z"
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
id|string(uuid)|false|Pay By Group UUID of this legal document
type|string|false|Specified by the merchant as either cancellation policy for cancellation and refund terms or tos for all other legal documents. 
title|string|false|Mechant's title for this legal document
content|string|false|Full content as provided by the merchant, either in plain text or as a URL
created_at|string(date-time)|false|When this legal document was added by the merchant
updated_at|string(date-time)|false|When this legal document was last updated by the merchant


#### Enumerated Values

|Property|Value|
|---|---|
type|tos|
type|cancelation_policy|


## LegalBinding

<a name="schemalegalbinding"></a>

```json
{
  "id": "string",
  "type": "string",
  "title": "string",
  "content": "string",
  "created_at": "string",
  "remote_ip": "string",
  "user_id": "string",
  "purchase_id": "string"
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
id|string(uuid)|false|Pay By Group UUID of this specific record of acceptance by the user
type|string|false|Either cancellation policy for cancellation and refund terms or tos for all other legal documents provided by merchant. 
title|string|false|Mechant's title for this legal document as accepted by the user
content|string|false|Full content as accepted by the user at the moment they agreed to this legal document
created_at|string|false|Verifiable timestamp when the user accepted this legal document
remote_ip|string|false|User's IP address at the moment they accepted this legal document
user_id|string|false|ID of the user that accepted the document, which includes their name and email
purchase_id|string|false|The purchase for which this document was accepted by the user



## ConsumerFieldTemplate

<a name="schemaconsumerfieldtemplate"></a>

```json
{
  "id": "string",
  "name": "string",
  "label": "string",
  "description": "string",
  "type": "text",
  "default_value": "string",
  "options": [
    {
      "type": "text",
      "value": "string"
    }
  ],
  "order": 0,
  "scope": "member",
  "default": true,
  "special": true,
  "required": true
} 
```

### Properties

Name|Type|Required|Description
---|---|---|---|
id|string(uuid)|false|Pay By Group UUID for this consumer field template
name|string|false|A unique name for the template.
label|string|false|Text to display as the field label.
description|string|false|A description for the template
type|string|false|Type of field to display for this template.
default_value|string|false|Default value to use for the template.
order|integer(int32)|false|Order in which the template should be displayed.
scope|string|false|Whether the template is at the member level, or purchase level.
default|boolean|false|Whether the template should be default or not.
special|boolean|false|Whether the template is a special field or not.
required|boolean|false|Whether the template is required or not.
options|[object]|false|Array of options to use for a list template.
» type|string|false|Value type for the option item
» value|string|false|Value for the option item


#### Enumerated Values

|Property|Value|
|---|---|
type|text|
type|textarea|
type|datetime|
type|address|
type|single_select|
type|multi_select|
scope|member|
scope|purchase|
» type|text|
» type|textarea|
» type|datetime|
» type|address|
» type|single_select|
» type|multi_select|





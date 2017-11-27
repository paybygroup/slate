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

This is the Pay By Group API for merchant integrations. See our
[Full Documentation](https://developers.paybygroup.com/v1.0/docs) for
additional information and walkthroughs of recommended integration workflows.

Base URLs:

* <a href="https://api.paybygroup.com/">https://api.paybygroup.com/</a>

* <a href="https://api-test.paybygroup.com/">https://api-test.paybygroup.com/</a>



Email: <a href="mailto:support@paybygroup.com">Pay By Group</a> 

# Authentication



- Basic Authentication. Use your own Access Key and Secret Key. See details at https://developers.paybygroup.com/v1.0/reference#authentication.



# purchases

These are all operations that can be done on Purchase objects. Many other objects,
such as Memberships and Payments, can be accessed and updated within the Purchase object.
See this summary of [all object relationships](https://developers.paybygroup.com/v1.0/docs/objects)
for a useful overview.

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
      "logo_url": "string"
    },
    "status": "created",
    "currency_code": "string",
    "payments": [
      {
        "id": "string",
        "status": "pending",
        "number": 0,
        "percentage": 1,
        "due_deadline": "2017-11-27T23:35:47Z",
        "amount": {
          "amount_cents": 0,
          "currency_code": "string"
        },
        "submitted_at": "2017-11-27T23:35:47Z",
        "accepted_at": "2017-11-27T23:35:47Z",
        "paid_at": "2017-11-27T23:35:47Z",
        "processing_currency": "string",
        "conversion_rate": 0,
        "failed": true,
        "payout_failed": true
      }
    ],
    "current_payment": {
      "id": "string",
      "status": "pending",
      "number": 0,
      "percentage": 1,
      "due_deadline": "2017-11-27T23:35:47Z",
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "submitted_at": "2017-11-27T23:35:47Z",
      "accepted_at": "2017-11-27T23:35:47Z",
      "paid_at": "2017-11-27T23:35:47Z",
      "processing_currency": "string",
      "conversion_rate": 0,
      "failed": true,
      "payout_failed": true
    },
    "next_payment_due_deadline": "2017-11-27T23:35:47Z",
    "product": {
      "images": [
        {
          "id": "string",
          "name": "string",
          "version": "string",
          "url": "string"
        }
      ],
      "default_image_url": "string",
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
      "start_datetime": "2017-11-27T23:35:47Z",
      "end_datetime": "2017-11-27T23:35:47Z",
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
          "created_at": "2017-11-27T23:35:47Z",
          "updated_at": "2017-11-27T23:35:47Z"
        }
      ]
    },
    "group": {
      "commit_deadline": "2017-11-27T23:35:47Z",
      "max_slots": 0,
      "min_slots": 0,
      "min_contribution": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "organizer_email": "user@example.com",
      "organizer_full_name": "string",
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
          }
        },
        "consumer_field_values": {
          "id": "string",
          "schema_id": "string",
          "name": "string",
          "slot": 0,
          "value": "string"
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
            }
          },
          "charged_at": "2017-11-27T23:35:47Z",
          "failed_at": "2017-11-27T23:35:47Z",
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
          "created_at": "2017-11-27T23:35:47Z"
        },
        "purchase_id": "string",
        "payment_source": {
          "id": "string",
          "name": "string",
          "type": "string",
          "info": {
            "card_type": "string",
            "last_four": "string",
            "valid_until": "string"
          },
          "created_at": "2017-11-27T23:35:47Z"
        },
        "committed_at": "2017-11-27T23:35:47Z",
        "created_at": "2017-11-27T23:35:47Z"
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
    "needed_amount_to_current_payment": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "committed_slots": 0,
    "needed_slots_to_min": 0,
    "product_or_group_min_slots": 0,
    "product_or_group_max_slots": 0,
    "tipped": true,
    "auto_pilot_enabled": true,
    "auto_pilot_trigger_slots": 0,
    "current_product_cost_amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "current_total_cost_amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
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
    "consumer_field_schemas": [
      {
        "id": "string",
        "order": 0,
        "scope": "member",
        "required": true,
        "name": "string",
        "label": "string",
        "description": "string",
        "default_value": "string",
        "type": "address",
        "options": [
          {
            "type": "text",
            "value": "string"
          }
        ]
      }
    ],
    "has_consumer_field_schemas": true,
    "consumer_field_values": [
      {
        "id": "string",
        "schema_id": "string",
        "name": "string",
        "slot": 0,
        "value": "string"
      }
    ],
    "payment_destination_id": "string",
    "currency_config": {
      "supported_payment_sources": [
        {
          "type": "credit_card",
          "unsupported_cards": [
            "visa"
          ]
        }
      ]
    },
    "refund_status": "none",
    "processing_refund": true,
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
    "language_code": "DA (Danish)",
    "created_at": "2017-11-27T23:35:47Z"
  }
]
```
<h3 id="RetrieveMerchantPurchases-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success response.|[[Purchase](#schemapurchase)]

<aside class="warning">
To perform this operation, you must be authenticated by HTTP Basic Authorization header.
</aside>

## CreatePurchase

`POST /purchases`

*Create a purchase*

Creates a new purchase and returns the Purchase object, which contains
the slug you can use to redirect an end user to their group's hub page,
or you can proceed to use PATCH /purchases/:id/claim if you want to fully
embed the experience. See this
[breakdown of the entire flow](https://developers.paybygroup.com/v1.0/docs/standard-flow)
for a list of all calls to use for a fully embedded experience.

> Body parameter

```json
{
  "product": {
    "name": "Trip to Las Vegas!",
    "cost_type": "total",
    "description": "Weekend package for Las Vegas.",
    "default_image_url": "https://example.com/image.jpg",
    "inventory_id": "SKU-1234",
    "link": "https://mycompany.com/product/sku-1234/details",
    "start_datetime": "2018-11-03T14:57:54Z",
    "end_datetime": "2018-11-08T14:57:54Z",
    "external_purchase_id": "87654",
    "costs": [
      {
        "amount": {
          "amount_cents": 200000,
          "currency_code": "USD"
        },
        "min_slots": 1,
        "max_slots": 3
      },
      {
        "amount": {
          "amount_cents": 250000,
          "currency_code": "USD"
        },
        "min_slots": 4,
        "max_slots": 4
      }
    ],
    "legal_documents": [
      "03DEFD52-E46C-42CF-BD88-A61EB5A61BB5"
    ]
  },
  "group": {
    "organizer_full_name": "John Doe",
    "organizer_email": "john@example.com"
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
body|body|object|true|Request body object.
» product|body|object|true|All parameters describing what is being purchased
»» name|body|string|true|Name of the product being purchased as it should be shown to end users
»» cost_type|body|string|false|Cost type that determines whether the product_costs amount(s) are for the whole group or per slot.<br/>-`per_slot` The product cost provided is for each slot a Member commits to in the Purchase,<br/>so the total amount paid to the merchant is a function of the number of<br/>slots claimed by all group members.<br/>-`total` The product cost is single total amount so long as<br/>the number of slots claimed is in the allowed range for that amount. (default if no value is provided)<br/>
»» description|body|string|false|Description of the product for this Purchase
»» default_image_url|body|string|false|The primary image to display to users for this product. The<br/>merchant default image applies if none is provided. Use the<br/>[CreatePurchaseImages](#createpurchaseimages) call to add an image using the API.<br/>
»» inventory_id|body|string|false|Inventory ID supplied by the merchant that identifies the product<br/>being bought in this Purchase (e.g. SKU or property ID)<br/>
»» link|body|string|false|Link to the product being purchased on the merchant's (or other third party's) website
»» start_datetime|body|string(date-time)|false|Start date time for the product being purchased<br/>(e.g. check-in date time, flight departure date time, or event<br/>starting time)<br/>
»» end_datetime|body|string(date-time)|false|End date time for the product being purchased<br/>(e.g. check-out date time, flight arrival date time, or activity ending time)<br/>
»» external_purchase_id|body|string|false|ID supplied by the merchant that identifies this Purchase<br/>(e.g. order or booking) in the merchant's system<br/>
»» costs|body|[[ProductCost](#schemaproductcost)]|true|The set of product_costs and the optional allowed range(s) of slots<br/>for each cost as provided by the merchant. The currency of the product cost<br/>determines the currency of the purchase.<br/>
»» legal_documents|body|[string]|false|Array of [legal document IDs](#legaldocument)<br/>that must be accepted by the members in this purchase. If no values are passed, the default Legal<br/>Documents will be attached to the Purchase. If one or more value is passed, it will override all defaults.<br/>
» group|body|object|false|All parameters describing the particular setup of this group
»» organizer_full_name|body|string|false|Full name of the expected organizer as provided by the merchant
»» organizer_email|body|string(email)|false|Email of the expected organizer as provided by the merchant
» language_code|body|string|false|Default language for this purchase. It is going to be used in the<br/>claim and commit steps; and as one of the fallbacks when detecting<br/>what language to show to the user.<br/>
» payment_destination_id|body|string(uuid)|false|ID of the payment destination that will receive all future payments<br/>made under this Purchase. The merchant's default for the Purchase's currency<br/>will apply if none is provided.<br/>
» payments|body|[object]|false|Breakdown of payment amounts and deadlines due over time for this purchase
»» percentage|body|integer(int32)|true|Percent of the total purchase cost due for this payment, which must<br/>be an integer. All payments on a purchase must sum to 100. If you are<br/>not doing installment or deposit payments, this is most likely "100".<br/>If no payments are passed, then by default a single payment for "100"<br/>percent with no `due_deadline` will be created.<br/>
»» due_deadline|body|string(date-time)|false|Datetime by when this payment must be submitted to the merchant for<br/>the purchase to be valid. It is required for all payments after<br/>the first payment but may be passed for the first, or only, payment as well.<br/>
» consumer_field_schemas|body|[object]|false|The set of consumer fields that should be attached to this purchase, by name,<br/>and their accompanying options. If any consumer_field_schemas are passed, then<br/>they override all default consumer_field_templates for the merchant.<br/>
»» name|body|string|true|The name of the consumer_field_template you want to attach to the purchase.<br/>Values set in the template apply as default unless overriden here.<br/>
»» scope|body|string|false|Determines whether all group members complete this field or only the<br/>organizer does on behalf of the whole purchase<br/>
»» required|body|boolean|false|Whether the field for this schema should be required or not.


#### Enumerated Values

|Parameter|Value|
|---|---|
»» cost_type|total|
»» cost_type|per_slot|
»» scope|member|
»» scope|purchase|

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
    "logo_url": "string"
  },
  "status": "created",
  "currency_code": "string",
  "payments": [
    {
      "id": "string",
      "status": "pending",
      "number": 0,
      "percentage": 1,
      "due_deadline": "2017-11-27T23:35:47Z",
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "submitted_at": "2017-11-27T23:35:47Z",
      "accepted_at": "2017-11-27T23:35:47Z",
      "paid_at": "2017-11-27T23:35:47Z",
      "processing_currency": "string",
      "conversion_rate": 0,
      "failed": true,
      "payout_failed": true
    }
  ],
  "current_payment": {
    "id": "string",
    "status": "pending",
    "number": 0,
    "percentage": 1,
    "due_deadline": "2017-11-27T23:35:47Z",
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "submitted_at": "2017-11-27T23:35:47Z",
    "accepted_at": "2017-11-27T23:35:47Z",
    "paid_at": "2017-11-27T23:35:47Z",
    "processing_currency": "string",
    "conversion_rate": 0,
    "failed": true,
    "payout_failed": true
  },
  "next_payment_due_deadline": "2017-11-27T23:35:47Z",
  "product": {
    "images": [
      {
        "id": "string",
        "name": "string",
        "version": "string",
        "url": "string"
      }
    ],
    "default_image_url": "string",
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
    "start_datetime": "2017-11-27T23:35:47Z",
    "end_datetime": "2017-11-27T23:35:47Z",
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
        "created_at": "2017-11-27T23:35:47Z",
        "updated_at": "2017-11-27T23:35:47Z"
      }
    ]
  },
  "group": {
    "commit_deadline": "2017-11-27T23:35:47Z",
    "max_slots": 0,
    "min_slots": 0,
    "min_contribution": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "organizer_email": "user@example.com",
    "organizer_full_name": "string",
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
        }
      },
      "consumer_field_values": {
        "id": "string",
        "schema_id": "string",
        "name": "string",
        "slot": 0,
        "value": "string"
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
          }
        },
        "charged_at": "2017-11-27T23:35:47Z",
        "failed_at": "2017-11-27T23:35:47Z",
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
        "created_at": "2017-11-27T23:35:47Z"
      },
      "purchase_id": "string",
      "payment_source": {
        "id": "string",
        "name": "string",
        "type": "string",
        "info": {
          "card_type": "string",
          "last_four": "string",
          "valid_until": "string"
        },
        "created_at": "2017-11-27T23:35:47Z"
      },
      "committed_at": "2017-11-27T23:35:47Z",
      "created_at": "2017-11-27T23:35:47Z"
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
  "needed_amount_to_current_payment": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "committed_slots": 0,
  "needed_slots_to_min": 0,
  "product_or_group_min_slots": 0,
  "product_or_group_max_slots": 0,
  "tipped": true,
  "auto_pilot_enabled": true,
  "auto_pilot_trigger_slots": 0,
  "current_product_cost_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "current_total_cost_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
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
  "consumer_field_schemas": [
    {
      "id": "string",
      "order": 0,
      "scope": "member",
      "required": true,
      "name": "string",
      "label": "string",
      "description": "string",
      "default_value": "string",
      "type": "address",
      "options": [
        {
          "type": "text",
          "value": "string"
        }
      ]
    }
  ],
  "has_consumer_field_schemas": true,
  "consumer_field_values": [
    {
      "id": "string",
      "schema_id": "string",
      "name": "string",
      "slot": 0,
      "value": "string"
    }
  ],
  "payment_destination_id": "string",
  "currency_config": {
    "supported_payment_sources": [
      {
        "type": "credit_card",
        "unsupported_cards": [
          "visa"
        ]
      }
    ]
  },
  "refund_status": "none",
  "processing_refund": true,
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
  "language_code": "DA (Danish)",
  "created_at": "2017-11-27T23:35:47Z"
}
```
<h3 id="CreatePurchase-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Created response.|[Purchase](#schemapurchase)

<aside class="warning">
To perform this operation, you must be authenticated by HTTP Basic Authorization header.
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
    "logo_url": "string"
  },
  "status": "created",
  "currency_code": "string",
  "payments": [
    {
      "id": "string",
      "status": "pending",
      "number": 0,
      "percentage": 1,
      "due_deadline": "2017-11-27T23:35:47Z",
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "submitted_at": "2017-11-27T23:35:47Z",
      "accepted_at": "2017-11-27T23:35:47Z",
      "paid_at": "2017-11-27T23:35:47Z",
      "processing_currency": "string",
      "conversion_rate": 0,
      "failed": true,
      "payout_failed": true
    }
  ],
  "current_payment": {
    "id": "string",
    "status": "pending",
    "number": 0,
    "percentage": 1,
    "due_deadline": "2017-11-27T23:35:47Z",
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "submitted_at": "2017-11-27T23:35:47Z",
    "accepted_at": "2017-11-27T23:35:47Z",
    "paid_at": "2017-11-27T23:35:47Z",
    "processing_currency": "string",
    "conversion_rate": 0,
    "failed": true,
    "payout_failed": true
  },
  "next_payment_due_deadline": "2017-11-27T23:35:47Z",
  "product": {
    "images": [
      {
        "id": "string",
        "name": "string",
        "version": "string",
        "url": "string"
      }
    ],
    "default_image_url": "string",
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
    "start_datetime": "2017-11-27T23:35:47Z",
    "end_datetime": "2017-11-27T23:35:47Z",
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
        "created_at": "2017-11-27T23:35:47Z",
        "updated_at": "2017-11-27T23:35:47Z"
      }
    ]
  },
  "group": {
    "commit_deadline": "2017-11-27T23:35:47Z",
    "max_slots": 0,
    "min_slots": 0,
    "min_contribution": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "organizer_email": "user@example.com",
    "organizer_full_name": "string",
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
        }
      },
      "consumer_field_values": {
        "id": "string",
        "schema_id": "string",
        "name": "string",
        "slot": 0,
        "value": "string"
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
          }
        },
        "charged_at": "2017-11-27T23:35:47Z",
        "failed_at": "2017-11-27T23:35:47Z",
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
        "created_at": "2017-11-27T23:35:47Z"
      },
      "purchase_id": "string",
      "payment_source": {
        "id": "string",
        "name": "string",
        "type": "string",
        "info": {
          "card_type": "string",
          "last_four": "string",
          "valid_until": "string"
        },
        "created_at": "2017-11-27T23:35:47Z"
      },
      "committed_at": "2017-11-27T23:35:47Z",
      "created_at": "2017-11-27T23:35:47Z"
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
  "needed_amount_to_current_payment": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "committed_slots": 0,
  "needed_slots_to_min": 0,
  "product_or_group_min_slots": 0,
  "product_or_group_max_slots": 0,
  "tipped": true,
  "auto_pilot_enabled": true,
  "auto_pilot_trigger_slots": 0,
  "current_product_cost_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "current_total_cost_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
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
  "consumer_field_schemas": [
    {
      "id": "string",
      "order": 0,
      "scope": "member",
      "required": true,
      "name": "string",
      "label": "string",
      "description": "string",
      "default_value": "string",
      "type": "address",
      "options": [
        {
          "type": "text",
          "value": "string"
        }
      ]
    }
  ],
  "has_consumer_field_schemas": true,
  "consumer_field_values": [
    {
      "id": "string",
      "schema_id": "string",
      "name": "string",
      "slot": 0,
      "value": "string"
    }
  ],
  "payment_destination_id": "string",
  "currency_config": {
    "supported_payment_sources": [
      {
        "type": "credit_card",
        "unsupported_cards": [
          "visa"
        ]
      }
    ]
  },
  "refund_status": "none",
  "processing_refund": true,
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
  "language_code": "DA (Danish)",
  "created_at": "2017-11-27T23:35:47Z"
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
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success response.|[Purchase](#schemapurchase)
404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|[Error](#schemaerror)

<aside class="warning">
To perform this operation, you must be authenticated by HTTP Basic Authorization header.
</aside>

## UpdatePurchase

`PATCH /purchases/{id}`

*Update an existing purchase*

To update a purchase where the inventory is no longer available and you can offer alternate inventory
that is available, you should change details of the in-progress group. You should also
update the purchase if other details change before it completes such as the the price,
start datetime, due deadline, etc. You can update a purchsae at any time until you accept
the last (or only) payment for that purchase. NOTE: you can never update the `cost_type`.
You can not update `payments` or `product_costs` after you have accepted at least 1 payment.

> Body parameter

```json
{
  "product": {
    "name": "Grand Canyon Excursion",
    "description": "2-day, 3-night hiking tour of the Grand Canyon",
    "inventory_id": "SKU-9876",
    "link": "https://mycompany.com/product/sku-9876/details",
    "start_datetime": "2018-12-03T14:57:54Z",
    "end_datetime": "2018-12-08T14:57:54Z",
    "costs": [
      {
        "amount": {
          "amount_cents": 100000,
          "currency_code": "USD"
        },
        "min_slots": 1,
        "max_slots": 4
      }
    ]
  }
}
```
<h3 id="UpdatePurchase-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|string(uuid)|true|ID of the Purchase to update.
body|body|object|true|Request body object.
» product|body|object|false|No description
»» name|body|string|false|Name of the product being purchased as it should be shown to end users
»» description|body|string|false|Description of the product for this Purchase
»» default_image_url|body|string|false|The primary image to display for this product
»» inventory_id|body|string|false|Inventory ID supplied by the merchant that identifies the product<br/>being bought in this Purchase (e.g. SKU or property ID)<br/>
»» link|body|string|false|Link to the product being purchased on the merchant's (or other third party's) website
»» start_datetime|body|string(date-time)|false|Start date time for the product being purchased<br/>(e.g. check-in date time, flight departure date time, or event<br/>starting time)<br/>
»» end_datetime|body|string(date-time)|false|End date time for the product being purchased<br/>(e.g. check-out date time, flight arrival date time, or activity<br/>ending time)<br/>
»» external_purchase_id|body|string|false|ID supplied by the merchant that identifies this Purchase<br/>(e.g. order or booking) in the merchant's system<br/>
»» costs|body|[[ProductCost](#schemaproductcost)]|false|The set of product_costs and the optional allowed range(s) of slots<br/>for each cost as provided by the merchant. When updating the product_costs,<br/>you cannot use a different currency than the existing one after the purchase<br/>has been claimed. You cannot edit the range of slots to be less than the current<br/>number of committed slots.<br/>
»» legal_documents|body|[string]|false|Array of legal document IDs that must be accepted by the members in this purchase. These should NOT<br/>be updated after a Purchase has been claimed because then some members will end up with different<br/>accepted legal terms from others.<br/>
» group|body|object|false|All parameters configuring the group, including those set by the organizer at the claim step.
»» organizer_full_name|body|string|false|Full name of the expected organizer as provided by the merchant. This will only affect information<br/>displayed to the merchant if updated after the Purchase is claimed.<br/>
»» organizer_email|body|string(email)|false|Email of the expected organizer as provided by the merchant. This will only affect information<br/>displayed to the merchant if updated after the Purchase is claimed.<br/>
»» split_type|body|string|false|Splitting type chosen by the organizer for how to divide the cost<br/>among group members.<br/>One of:<br/>-`even_split` Only compatible with total cost_type and means the<br/>Purchase amount is split evenly across each slot claimed.<br/>-`specified_per_person` Only compatible with total cost_type and<br/>means each member may pay a different amount.<br/>-`fixed_per_person` Only compatible with per_slot cost_type and means<br/>each group member pays a fixed amount per slot they claim.<br/>
»» min_slots|body|integer(int32)|false|The organizer-specified value for the minimum number of slots they<br/>require to be claimed. It must be within the bounds allowed by the merchant.<br/>Only compatible with `even_split` and `fixed_per_person` split types.<br/>
»» max_slots|body|integer(int32)|false|The organizer-specified value for the maximum number of slots they<br/>will allow to be claimed. It must be within the bounds allowed by the merchant.<br/>Only compatible with `even_split` and `fixed_per_person` split types.<br/>
»» min_contribution|body|[Money](#schemamoney)|false|Minimum required contribution from each group member.<br/>Only compatible with `specified_per_person` split type.<br/>
» language_code|body|string|false|Default 2-character language code for this purchase. It is going<br/>to be used in the claim and commit steps; and as one of the<br/>fallbacks when detecting what language to show to the user<br/>
» payment_destination_id|body|string(uuid)|false|ID of the payment destination that will receive all future payments<br/>made under this Purchase. NOTE: updating this value will not affect<br/>any previously accepted payments on this purchase.<br/>
» payments|body|[object]|false|Breakdown of payment amounts and deadlines due over time for this Purchase.<br/>They can only be updated if no payment has yet been accepted by the merchant for this Purchase..<br/>
»» percentage|body|integer(int32)|true|Percent of the total purchase cost due for this payment, which must<br/>be an integer. All payments on a purchase must sum to 100. If you are<br/>not doing installment or deposit payments, this is most likely "100".<br/>
»» due_deadline|body|string(date-time)|false|Datetime by when this payment must be submitted to the merchant for<br/>the purchase to be valid. It is required for all payments after<br/>the first payment but may be passed for the first, or only, payment as well.<br/>


#### Enumerated Values

|Parameter|Value|
|---|---|
»» split_type|even_split|
»» split_type|specified_per_person|
»» split_type|fixed_per_person|
» language_code|DA (Danish)|
» language_code|EN (English)|
» language_code|ES (Spanish)|

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
    "logo_url": "string"
  },
  "status": "created",
  "currency_code": "string",
  "payments": [
    {
      "id": "string",
      "status": "pending",
      "number": 0,
      "percentage": 1,
      "due_deadline": "2017-11-27T23:35:47Z",
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "submitted_at": "2017-11-27T23:35:47Z",
      "accepted_at": "2017-11-27T23:35:47Z",
      "paid_at": "2017-11-27T23:35:47Z",
      "processing_currency": "string",
      "conversion_rate": 0,
      "failed": true,
      "payout_failed": true
    }
  ],
  "current_payment": {
    "id": "string",
    "status": "pending",
    "number": 0,
    "percentage": 1,
    "due_deadline": "2017-11-27T23:35:47Z",
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "submitted_at": "2017-11-27T23:35:47Z",
    "accepted_at": "2017-11-27T23:35:47Z",
    "paid_at": "2017-11-27T23:35:47Z",
    "processing_currency": "string",
    "conversion_rate": 0,
    "failed": true,
    "payout_failed": true
  },
  "next_payment_due_deadline": "2017-11-27T23:35:47Z",
  "product": {
    "images": [
      {
        "id": "string",
        "name": "string",
        "version": "string",
        "url": "string"
      }
    ],
    "default_image_url": "string",
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
    "start_datetime": "2017-11-27T23:35:47Z",
    "end_datetime": "2017-11-27T23:35:47Z",
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
        "created_at": "2017-11-27T23:35:47Z",
        "updated_at": "2017-11-27T23:35:47Z"
      }
    ]
  },
  "group": {
    "commit_deadline": "2017-11-27T23:35:47Z",
    "max_slots": 0,
    "min_slots": 0,
    "min_contribution": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "organizer_email": "user@example.com",
    "organizer_full_name": "string",
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
        }
      },
      "consumer_field_values": {
        "id": "string",
        "schema_id": "string",
        "name": "string",
        "slot": 0,
        "value": "string"
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
          }
        },
        "charged_at": "2017-11-27T23:35:47Z",
        "failed_at": "2017-11-27T23:35:47Z",
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
        "created_at": "2017-11-27T23:35:47Z"
      },
      "purchase_id": "string",
      "payment_source": {
        "id": "string",
        "name": "string",
        "type": "string",
        "info": {
          "card_type": "string",
          "last_four": "string",
          "valid_until": "string"
        },
        "created_at": "2017-11-27T23:35:47Z"
      },
      "committed_at": "2017-11-27T23:35:47Z",
      "created_at": "2017-11-27T23:35:47Z"
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
  "needed_amount_to_current_payment": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "committed_slots": 0,
  "needed_slots_to_min": 0,
  "product_or_group_min_slots": 0,
  "product_or_group_max_slots": 0,
  "tipped": true,
  "auto_pilot_enabled": true,
  "auto_pilot_trigger_slots": 0,
  "current_product_cost_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "current_total_cost_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
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
  "consumer_field_schemas": [
    {
      "id": "string",
      "order": 0,
      "scope": "member",
      "required": true,
      "name": "string",
      "label": "string",
      "description": "string",
      "default_value": "string",
      "type": "address",
      "options": [
        {
          "type": "text",
          "value": "string"
        }
      ]
    }
  ],
  "has_consumer_field_schemas": true,
  "consumer_field_values": [
    {
      "id": "string",
      "schema_id": "string",
      "name": "string",
      "slot": 0,
      "value": "string"
    }
  ],
  "payment_destination_id": "string",
  "currency_config": {
    "supported_payment_sources": [
      {
        "type": "credit_card",
        "unsupported_cards": [
          "visa"
        ]
      }
    ]
  },
  "refund_status": "none",
  "processing_refund": true,
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
  "language_code": "DA (Danish)",
  "created_at": "2017-11-27T23:35:47Z"
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
To perform this operation, you must be authenticated by HTTP Basic Authorization header.
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
  "organizer_name": "John Doe",
  "organizer_email": "johndoe@gmail.com",
  "group": {
    "split_type": "even_split",
    "min_slots": 2,
    "max_slots": 4
  }
}
```
<h3 id="ClaimPurchase-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|string(uuid)|true|ID of the Purchase to claim
body|body|object|true|Request body object.
» organizer_name|body|string|true|Full name of the organizer
» organizer_email|body|string|true|Email of the organizer
» organizer_allowed_share_amount|body|[Money](#schemamoney)|false|This is the recommended share for the organizer and is only relevant if split_type is `specified_per_person`
» min_contribution|body|[Money](#schemamoney)|false|Min contribution amount
» group|body|object|true|No description
»» split_type|body|string|true|Splitting type chosen by the organizer for how to divide the cost<br/>among group members.<br/>One of:<br/>-`even_split` Only compatible with total cost_type and means the<br/>  Purchase amount is split evenly across each slot claimed.<br/>-`specified_per_person` Only compatible with total cost_type and<br/>  means each member may pay a different amount.<br/>-`fixed_per_person` Only compatible with per_slot cost_type and means<br/>  each group member pays a fixed amount per slot they claim.<br/>
»» max_slots|body|integer(int32)|false|The organizer-specified value for the minimum number of slots they<br/>require to be claimed. It must be within the bounds allowed by the merchant.<br/>Only compatible with `even_split` and `fixed_per_person` split types.<br/>
»» min_slots|body|integer(int32)|false|The organizer-specified value for the maximum number of slots they<br/>will allow to be claimed. It must be within the bounds allowed by the merchant.<br/>Only compatible with `even_split` and `fixed_per_person` split types.<br/>
»» min_contribution|body|[Money](#schemamoney)|false|Minimum required contribution from each group member.<br/>Only compatible with `specified_per_person` split type.<br/>


#### Enumerated Values

|Parameter|Value|
|---|---|
»» split_type|even_split|
»» split_type|specified_per_person|
»» split_type|fixed_per_person|

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
    "logo_url": "string"
  },
  "status": "created",
  "currency_code": "string",
  "payments": [
    {
      "id": "string",
      "status": "pending",
      "number": 0,
      "percentage": 1,
      "due_deadline": "2017-11-27T23:35:47Z",
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "submitted_at": "2017-11-27T23:35:47Z",
      "accepted_at": "2017-11-27T23:35:47Z",
      "paid_at": "2017-11-27T23:35:47Z",
      "processing_currency": "string",
      "conversion_rate": 0,
      "failed": true,
      "payout_failed": true
    }
  ],
  "current_payment": {
    "id": "string",
    "status": "pending",
    "number": 0,
    "percentage": 1,
    "due_deadline": "2017-11-27T23:35:47Z",
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "submitted_at": "2017-11-27T23:35:47Z",
    "accepted_at": "2017-11-27T23:35:47Z",
    "paid_at": "2017-11-27T23:35:47Z",
    "processing_currency": "string",
    "conversion_rate": 0,
    "failed": true,
    "payout_failed": true
  },
  "next_payment_due_deadline": "2017-11-27T23:35:47Z",
  "product": {
    "images": [
      {
        "id": "string",
        "name": "string",
        "version": "string",
        "url": "string"
      }
    ],
    "default_image_url": "string",
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
    "start_datetime": "2017-11-27T23:35:47Z",
    "end_datetime": "2017-11-27T23:35:47Z",
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
        "created_at": "2017-11-27T23:35:47Z",
        "updated_at": "2017-11-27T23:35:47Z"
      }
    ]
  },
  "group": {
    "commit_deadline": "2017-11-27T23:35:47Z",
    "max_slots": 0,
    "min_slots": 0,
    "min_contribution": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "organizer_email": "user@example.com",
    "organizer_full_name": "string",
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
        }
      },
      "consumer_field_values": {
        "id": "string",
        "schema_id": "string",
        "name": "string",
        "slot": 0,
        "value": "string"
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
          }
        },
        "charged_at": "2017-11-27T23:35:47Z",
        "failed_at": "2017-11-27T23:35:47Z",
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
        "created_at": "2017-11-27T23:35:47Z"
      },
      "purchase_id": "string",
      "payment_source": {
        "id": "string",
        "name": "string",
        "type": "string",
        "info": {
          "card_type": "string",
          "last_four": "string",
          "valid_until": "string"
        },
        "created_at": "2017-11-27T23:35:47Z"
      },
      "committed_at": "2017-11-27T23:35:47Z",
      "created_at": "2017-11-27T23:35:47Z"
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
  "needed_amount_to_current_payment": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "committed_slots": 0,
  "needed_slots_to_min": 0,
  "product_or_group_min_slots": 0,
  "product_or_group_max_slots": 0,
  "tipped": true,
  "auto_pilot_enabled": true,
  "auto_pilot_trigger_slots": 0,
  "current_product_cost_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "current_total_cost_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
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
  "consumer_field_schemas": [
    {
      "id": "string",
      "order": 0,
      "scope": "member",
      "required": true,
      "name": "string",
      "label": "string",
      "description": "string",
      "default_value": "string",
      "type": "address",
      "options": [
        {
          "type": "text",
          "value": "string"
        }
      ]
    }
  ],
  "has_consumer_field_schemas": true,
  "consumer_field_values": [
    {
      "id": "string",
      "schema_id": "string",
      "name": "string",
      "slot": 0,
      "value": "string"
    }
  ],
  "payment_destination_id": "string",
  "currency_config": {
    "supported_payment_sources": [
      {
        "type": "credit_card",
        "unsupported_cards": [
          "visa"
        ]
      }
    ]
  },
  "refund_status": "none",
  "processing_refund": true,
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
  "language_code": "DA (Danish)",
  "created_at": "2017-11-27T23:35:47Z"
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
To perform this operation, you must be authenticated by HTTP Basic Authorization header.
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
      "email": "joanna@gmail.com",
      "full_name": "Joanna Ross"
    },
    {
      "email": "michael@hotmail.com",
      "full_name": "Michael Wilson",
      "allowed_share_amount": {
        "amount_cents": 25000,
        "currency_code": "USD"
      }
    }
  ],
  "message": "Join in so we can finally book this Grand Canyon trip!",
  "subject": "Grand Canyon booking"
}
```
<h3 id="InviteMembersToPurchase-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|string(uuid)|true|ID of the Purchase to invite to.
body|body|object|true|Request body object.
» message|body|string|false|Message from the organizer to include in the invite notification.
» subject|body|string|false|Subject line of the notification to the invitee if sent by email.
» invitees|body|[object]|true|All people that should receive invitations to contribute to the Purchase
»» email|body|string(email)|true|Email to send the invite to.
»» full_name|body|string|false|Name of the invitee.
»» allowed_share_amount|body|[Money](#schemamoney)|false|Suggested contribution for the invitee. Only relevant for `specified_per_person` split type.


<h3 id="InviteMembersToPurchase-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|Success response|None
404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|None
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Unprocessable entity|None

<aside class="warning">
To perform this operation, you must be authenticated by HTTP Basic Authorization header.
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
  "reason": "Your overpayment for the extra night that was canceled",
  "amount": {
    "amount_cents": 30000,
    "currency_code": "USD"
  },
  "membership_shares": [
    {
      "membership_id": "03DEFD52-E46C-42CF-BD88-A61EB5A61BB5",
      "amount": {
        "amount_cents": 12000,
        "currency_code": "USD"
      }
    },
    {
      "membership_id": "0288FBB9-B49C-22DF-5588-F21EC5F77B33",
      "amount": {
        "amount_cents": 18000,
        "currency_code": "USD"
      }
    }
  ]
}
```
<h3 id="RequestPurchaseRefund-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|string(uuid)|true|ID of the purchase to refund
body|body|object|true|Request body object.
» reason|body|string|true|Reason why this amount is being refunded
» amount|body|[Money](#schemamoney)|true|Amount to be refunded. It may not be greater than the current<br/>collected amount of the purchase, which is the total purchase<br/>amount net of any previous refunds. If the memberships_shares<br/>array is provided, this value must equal the sum of those shares.<br/>
» funding_source_id|body|string(uuid)|false|UUID of the merchant's payment source they wish to use to fund this refund.<br/>This is only applicable if the merchant originally received the payment that is being<br/>refunded into the merchant's bank account instead of a through a custom gateway. If no<br/>value is provided, then the default will be used if it has been set, otherwise the<br/>original payout bank account will be used.<br/>
» memberships_shares|body|[object]|false|No description
»» membership_id|body|string|true|ID of the membership to refund.
»» amount|body|[Money](#schemamoney)|true|Amount to refund to this member.


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
    "logo_url": "string"
  },
  "status": "created",
  "currency_code": "string",
  "payments": [
    {
      "id": "string",
      "status": "pending",
      "number": 0,
      "percentage": 1,
      "due_deadline": "2017-11-27T23:35:47Z",
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "submitted_at": "2017-11-27T23:35:47Z",
      "accepted_at": "2017-11-27T23:35:47Z",
      "paid_at": "2017-11-27T23:35:47Z",
      "processing_currency": "string",
      "conversion_rate": 0,
      "failed": true,
      "payout_failed": true
    }
  ],
  "current_payment": {
    "id": "string",
    "status": "pending",
    "number": 0,
    "percentage": 1,
    "due_deadline": "2017-11-27T23:35:47Z",
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "submitted_at": "2017-11-27T23:35:47Z",
    "accepted_at": "2017-11-27T23:35:47Z",
    "paid_at": "2017-11-27T23:35:47Z",
    "processing_currency": "string",
    "conversion_rate": 0,
    "failed": true,
    "payout_failed": true
  },
  "next_payment_due_deadline": "2017-11-27T23:35:47Z",
  "product": {
    "images": [
      {
        "id": "string",
        "name": "string",
        "version": "string",
        "url": "string"
      }
    ],
    "default_image_url": "string",
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
    "start_datetime": "2017-11-27T23:35:47Z",
    "end_datetime": "2017-11-27T23:35:47Z",
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
        "created_at": "2017-11-27T23:35:47Z",
        "updated_at": "2017-11-27T23:35:47Z"
      }
    ]
  },
  "group": {
    "commit_deadline": "2017-11-27T23:35:47Z",
    "max_slots": 0,
    "min_slots": 0,
    "min_contribution": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "organizer_email": "user@example.com",
    "organizer_full_name": "string",
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
        }
      },
      "consumer_field_values": {
        "id": "string",
        "schema_id": "string",
        "name": "string",
        "slot": 0,
        "value": "string"
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
          }
        },
        "charged_at": "2017-11-27T23:35:47Z",
        "failed_at": "2017-11-27T23:35:47Z",
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
        "created_at": "2017-11-27T23:35:47Z"
      },
      "purchase_id": "string",
      "payment_source": {
        "id": "string",
        "name": "string",
        "type": "string",
        "info": {
          "card_type": "string",
          "last_four": "string",
          "valid_until": "string"
        },
        "created_at": "2017-11-27T23:35:47Z"
      },
      "committed_at": "2017-11-27T23:35:47Z",
      "created_at": "2017-11-27T23:35:47Z"
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
  "needed_amount_to_current_payment": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "committed_slots": 0,
  "needed_slots_to_min": 0,
  "product_or_group_min_slots": 0,
  "product_or_group_max_slots": 0,
  "tipped": true,
  "auto_pilot_enabled": true,
  "auto_pilot_trigger_slots": 0,
  "current_product_cost_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "current_total_cost_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
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
  "consumer_field_schemas": [
    {
      "id": "string",
      "order": 0,
      "scope": "member",
      "required": true,
      "name": "string",
      "label": "string",
      "description": "string",
      "default_value": "string",
      "type": "address",
      "options": [
        {
          "type": "text",
          "value": "string"
        }
      ]
    }
  ],
  "has_consumer_field_schemas": true,
  "consumer_field_values": [
    {
      "id": "string",
      "schema_id": "string",
      "name": "string",
      "slot": 0,
      "value": "string"
    }
  ],
  "payment_destination_id": "string",
  "currency_config": {
    "supported_payment_sources": [
      {
        "type": "credit_card",
        "unsupported_cards": [
          "visa"
        ]
      }
    ]
  },
  "refund_status": "none",
  "processing_refund": true,
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
  "language_code": "DA (Danish)",
  "created_at": "2017-11-27T23:35:47Z"
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
To perform this operation, you must be authenticated by HTTP Basic Authorization header.
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
body|body|object|true|Request body object.
» reason|body|string|true|Description to be provided to the group's organizer<br/>explaining why the group was canceled<br/>


<h3 id="CancelPurchase-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
204|[No Content](https://tools.ietf.org/html/rfc7231#section-6.3.5)|Success response|None
404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|None
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Unprocessable entity|None

<aside class="warning">
To perform this operation, you must be authenticated by HTTP Basic Authorization header.
</aside>

## CreatePurchaseImages

`POST /purchases/{id}/images`

*Create purchase image*

This call attaches the image you specify in the body to the purchase you
specify in the request. That image should be of the product and is used
for display to end users. The most recent image uploaded will be the primary
image displayed for the purchase.

> Body parameter

```yaml
url: string
file: string

```
<h3 id="CreatePurchaseImages-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|string(uuid)|true|ID of the Purchase to which this image applies
body|body|object|false|Request body object.
» url|body|string|true|URL of the image. It will only be retrieved once from this URL,<br/>after which it will be cached by Pay By Group. If a file is passed, URL<br/>is not required.<br/>
» file|body|string(binary)|true|Image file. If a URL is passed, an image file is not required.


> Example responses

```json
{
  "id": "string",
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
To perform this operation, you must be authenticated by HTTP Basic Authorization header.
</aside>

## RetrievePurchaseMemberships

`GET /purchases/{id}/memberships`

*Retrieve list of all memberships for a purchase*

Returns a paginated list of all memberships associated with the specified purchase.

<h3 id="RetrievePurchaseMemberships-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|string(uuid)|true|Purchase ID


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
      }
    },
    "consumer_field_values": {
      "id": "string",
      "schema_id": "string",
      "name": "string",
      "slot": 0,
      "value": "string"
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
        }
      },
      "charged_at": "2017-11-27T23:35:47Z",
      "failed_at": "2017-11-27T23:35:47Z",
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
      "created_at": "2017-11-27T23:35:47Z"
    },
    "purchase_id": "string",
    "payment_source": {
      "id": "string",
      "name": "string",
      "type": "string",
      "info": {
        "card_type": "string",
        "last_four": "string",
        "valid_until": "string"
      },
      "created_at": "2017-11-27T23:35:47Z"
    },
    "committed_at": "2017-11-27T23:35:47Z",
    "created_at": "2017-11-27T23:35:47Z"
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
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success response|[[Membership](#schemamembership)]
404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|[Error](#schemaerror)

<aside class="warning">
To perform this operation, you must be authenticated by HTTP Basic Authorization header.
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
      }
    },
    "payout_account": {
      "id": "string",
      "name": "string",
      "status": "verified",
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
        "card_type": "string",
        "last_four": "string",
        "valid_until": "string"
      },
      "created_at": "2017-11-27T23:35:47Z"
    },
    "created_at": "2017-11-27T23:35:47Z",
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
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success response|[[PaymentTransaction](#schemapaymenttransaction)]
404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|[Error](#schemaerror)

<aside class="warning">
To perform this operation, you must be authenticated by HTTP Basic Authorization header.
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
    "created_at": "2017-11-27T23:35:47Z",
    "updated_at": "2017-11-27T23:35:47Z"
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
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success response|[[LegalDocument](#schemalegaldocument)]
404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|[Error](#schemaerror)

<aside class="warning">
To perform this operation, you must be authenticated by HTTP Basic Authorization header.
</aside>

## RetrievePurchaseLegalBindings

`GET /purchases/{id}/legal_documents/acceptances`

*List legal document acceptance records for all members*

Returns a paginated list of all legal bindings, which
represent each individual acceptance of a legal document
for this purchase by a group member.

<h3 id="RetrievePurchaseLegalBindings-parameters">Parameters</h3>

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
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success response|[[LegalBinding](#schemalegalbinding)]
404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|[Error](#schemaerror)

<aside class="warning">
To perform this operation, you must be authenticated by HTTP Basic Authorization header.
</aside>

# payments

This section covers all operations on Payment objects. A purchase must have at least 1
payment and may have up to n payments. Each payment defines an amount of the purchase
that must be paid by the group by a certain date.

## AcceptPayment

`POST /payments/{id}/accept`

*Accept a payment*

Merchants must make this call to receive a payout for any payment
that is in authorized status unless the merchant is configured to auto-accept
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
To perform this operation, you must be authenticated by HTTP Basic Authorization header.
</aside>

# legal_documents

This section covers all operations on Legal Document objects. Legal Documents are terms of
service and other contractual requirements you want all members in a purchase to accept
when joining a purchase. All Legal Documents apply to every member in every purchase
unless you specify 1 or more Legal Documents to attach to a purchase when creating a purchase,
in which case only the specified Legal Documents will apply to that purchases's members.

## RetrieveMerchantLegalDocuments

`GET /legal_documents`

*Retrieve list of legal documents*

Returns a paginated list of all legal documents that currently exist under this merchant and are available to attach to purchases.

> Example responses

```json
[
  {
    "id": "string",
    "type": "tos",
    "title": "string",
    "content": "string",
    "created_at": "2017-11-27T23:35:47Z",
    "updated_at": "2017-11-27T23:35:47Z"
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
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success response|[[LegalDocument](#schemalegaldocument)]
404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not Found|[Error](#schemaerror)

<aside class="warning">
To perform this operation, you must be authenticated by HTTP Basic Authorization header.
</aside>

## CreateMerchantLegalDocument

`POST /legal_documents`

*Add new legal document*

Add a new legal document, which will then be available to attach to any purchase so that members are required to accept it.

> Body parameter

```json
{
  "type": "tos",
  "title": "Lease Agreement",
  "content": "https://example.com/lease-agreements/9877"
}
```
<h3 id="CreateMerchantLegalDocument-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
body|body|object|true|Request body object.
» type|body|string|false|Specified by the merchant as either the Cancellation Policy for cancellation and refund terms<br/>or TOS (Terms of Service) for all other legal documents. If the cancellation policy is included in the TOS, then<br/>refer to that document as type TOS. If none is provided, the value defaults to `tos`.<br/>
» title|body|string|false|Mechant's title for this legal document to be displayed to end users. If none is provided, it defaults to<br/>the generic term "Terms of Service."<br/>
» content|body|string|true|Full content of the legal document, as provided by the merchant, either in plain text or as a URL. If a URL is<br/>provided, it will be linked to directly and not cached, so ensure the URL works so long as the Purchase is active.<br/>


#### Enumerated Values

|Parameter|Value|
|---|---|
» type|tos|
» type|cancelation_policy|

> Example responses

```json
{
  "id": "string",
  "type": "tos",
  "title": "string",
  "content": "string",
  "created_at": "2017-11-27T23:35:47Z",
  "updated_at": "2017-11-27T23:35:47Z"
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
To perform this operation, you must be authenticated by HTTP Basic Authorization header.
</aside>

## RetrieveMerchantLegalDocument

`GET /legal_documents/{id}`

*Retrieve legal document*

Retrieves all information for a specific legal document that was previously provided by the merchant.

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
  "created_at": "2017-11-27T23:35:47Z",
  "updated_at": "2017-11-27T23:35:47Z"
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
To perform this operation, you must be authenticated by HTTP Basic Authorization header.
</aside>

## patchLegalDocumentsId

`PATCH /legal_documents/{id}`

*Update a legal document*

Makes changes to a legal document, which will apply to all
future acceptances by members where that document is attached
to a purchase. It will not apply retroactively to any Purchase
created prior to the moment it is updated.

> Body parameter

```json
{
  "content": "https://example.com/lease-agreements/123456"
}
```
<h3 id="patchLegalDocumentsId-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|string(uuid)|true|ID of the Legal Document to update.
body|body|object|true|Request body object.
» type|body|string|false|Specified by the merchant as either the Cancellation Policy for cancellation and refund terms<br/>or TOS (Terms of Service) for all other legal documents. If the cancellation policy is included in the TOS, then<br/>refer to that document as type TOS. If none is provided in this request, then the existing value<br/>for the Legal Document being updated will continue to apply.<br/>
» title|body|string|false|Mechant's title for this legal document to be displayed to end users. If none is provided, the existing value<br/>for the Legal Document being updated will continue to apply.<br/>
» content|body|string|true|Full content of the legal document, as provided by the merchant, either in plain text or as a URL. If a URL is<br/>provided, it will be linked to directly and not cached, so ensure the URL works so long as the Purchase is active.<br/>If none is provided, the existing value for the Legal Document being updated will continue to apply.<br/>


#### Enumerated Values

|Parameter|Value|
|---|---|
» type|tos|
» type|cancelation_policy|

> Example responses

```json
{
  "id": "string",
  "type": "tos",
  "title": "string",
  "content": "string",
  "created_at": "2017-11-27T23:35:47Z",
  "updated_at": "2017-11-27T23:35:47Z"
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
To perform this operation, you must be authenticated by HTTP Basic Authorization header.
</aside>

# consumer_field_templates

Consumer Field Templates define information you wish to collect from
the organizer pertaining to the entire purchase or from each group member.
The templates define the basic structure, which can be configured futher when
attaching each template to a purchase. All "default" templates apply to every
purchase unless you specify 1 or more templates, in which case only the specified
ones will apply.

## CreateConsumerFieldTemplate

`POST /consumer_field_templates`

*Creates a new consumer field template*

You must first use this method to create a template before you can attach the template
to a purchase and collect data based on it.

> Body parameter

```json
{
  "name": "shirt_size",
  "label": "Shirt size",
  "type": "single_select",
  "options": [
    {
      "type": "text",
      "value": "S"
    },
    {
      "type": "text",
      "value": "M"
    },
    {
      "type": "text",
      "value": "L"
    },
    {
      "type": "text",
      "value": "XL"
    }
  ],
  "order": 1,
  "scope": "member",
  "default": true,
  "required": true
}
```
<h3 id="CreateConsumerFieldTemplate-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
body|body|object|true|Request body object.
» name|body|string|true|A unique name for the template, used as the reference for attaching the template to a purchase.
» label|body|string|true|Text to display as the field label.
» description|body|string|false|A description for the template displayed as sub-text below the field label.
» type|body|string|true|Type of field to display for this template. Single_select and multi_select require passing `options` values.
» default_value|body|string|false|Default value to use for the template, which prepopulates the field for the user on landing.
» order|body|integer(int32)|false|Order in which the template should be displayed, with 1 being the first displayed.<br/>This value must be unique to each template, but the values do not have to be sequential.<br/>
» scope|body|string|true|Whether the template applies at the member level to every group member or at the purchase<br/>level, only to the organizer.<br/>
» default|body|boolean|false|Whether the template should be default or not. Default templates apply to every purchase unless<br/>you specify at least 1 template at purchase creation. Defaults to `false` if no value is provided.<br/>
» required|body|boolean|false|This is the default setting for whether the user is required to fill this field when it is presented.<br/>Defaults to `false` if no value is provided.<br/>
» options|body|[object]|false|Array of options to display, which is required for a template of single_select or multi_select type.
»» type|body|string|false|Defines the format of the value you provide to display to end users.<br/>
»» value|body|string|false|Value displayed to end users when presenting the options


#### Enumerated Values

|Parameter|Value|
|---|---|
» type|address|
» type|datetime|
» type|multi_select|
» type|single_select|
» type|text|
» type|textarea|
» scope|member|
» scope|purchase|
»» type|address|
»» type|datetime|
»» type|text|

> Example responses

```json
{
  "id": "string",
  "default": true,
  "special": true,
  "order": 0,
  "scope": "member",
  "required": true,
  "name": "string",
  "label": "string",
  "description": "string",
  "default_value": "string",
  "type": "address",
  "options": [
    {
      "type": "text",
      "value": "string"
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
<h3 id="CreateConsumerFieldTemplate-responses">Responses</h3>

Status|Meaning|Description|Schema
---|---|---|---|
201|[Created](https://tools.ietf.org/html/rfc7231#section-6.3.2)|Success response|[ConsumerFieldTemplate](#schemaconsumerfieldtemplate)
422|[Unprocessable Entity](https://tools.ietf.org/html/rfc2518#section-10.3)|Unprocessable entity|[Error](#schemaerror)

<aside class="warning">
To perform this operation, you must be authenticated by HTTP Basic Authorization header.
</aside>

# Schemas

## BankAccount

<a id="schemabankaccount"></a>

```json
{
  "id": "string",
  "name": "string",
  "status": "verified",
  "merchant_id": "string",
  "supported_currency_codes": [
    "string"
  ],
  "currency_configs": "string"
} 
```

Merchants that choose to use Pay By Group as their processor instead of a third-party gateway
receive their payouts to a bank account

### Properties

Name|Type|Description
---|---|---|
id|string(uuid)|Pay By Group UUID for this bank account
name|string|Displayed name of bank account with last 4 of account number
status|string|verified or unverified depending on whether micro-deposit amounts have confirmed account ownership
merchant_id|string(uuid)|Merchant this bank account belongs to
currency_configs|string|Set of payment sources supported across all currencies for this bank account. Not all currencies support all payment sources. 
supported_currency_codes|[string]|3-letter currency codes that can be used for credits and debits with this account


#### Enumerated Values

|Property|Value|
|---|---|
status|verified|
status|unverified|


## ConsumerFeesStructure

<a id="schemaconsumerfeesstructure"></a>

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

These parameters describe the fees a consumer is charged on top of their share of the purchase.
These fees are payable to Pay By Group and collected directly for merchants that use Pay By Group as
their processor or invoiced for merchants that use a third-party gateway. Merchants may use this object
to display how fees on a Purchase work to an end user.

### Properties

Name|Type|Description
---|---|---|
per_share|[Money](#schemamoney)|Amount due per group member across all payments on a Purchase, which overrides the percentage value if both exist. 
per_share_max|[Money](#schemamoney)|Maximum charge per member's total share when applying the percentage
per_share_min|[Money](#schemamoney)|Minimum charge per member's total share when applying the percentage
percentage|integer(int32)|Percentage applied to member's total share to determine the fee



## ConsumerFieldSchema

<a id="schemaconsumerfieldschema"></a>

```json
{
  "id": "string",
  "order": 0,
  "scope": "member",
  "required": true,
  "name": "string",
  "label": "string",
  "description": "string",
  "default_value": "string",
  "type": "address",
  "options": [
    {
      "type": "text",
      "value": "string"
    }
  ]
} 
```

The Consumer Field Schema object is a version of a Consumer Field Template that is specific to a
Purchase. It is created as a variation on a Consumer Field Template when creating a Purcahse
and will remain unchanged once it is created and attached to that Purchase, even if the template
used to create it does change. Certain parameters of each template may be customized when creating
a new Consumer Field Schema, including: `scope`, `required`, and `options`.

### Properties

Name|Type|Description
---|---|---|
id|string(uuid)|UUID that identfies this consumer_field_schema for this Purchase
order|integer(int32)|Order in which the template should be displayed.
scope|string|Either `member` (applies to every group member) or purchase (applies only for the organizer to fill out on behalf of the whole Purchase) 
required|boolean|Whether the field is required or not
name|string|Name of this consumer_field as provided in the consumer_field_template that created this consumer_field_schema
label|string|Text displayed as the field label
description|string|Descriptive helper text explaining the field to the end user
default_value|string|Default value shown on landing for the user
type|string|Format for how the field is displayed to end users
options|[object]|Array of options for the user to select from, which applies for `single_select` and `multi-select` `type` templates 


#### Enumerated Values

|Property|Value|
|---|---|
scope|member|
scope|purchase|
type|address|
type|datetime|
type|multi_select|
type|single_select|
type|text|
type|textarea|


## ConsumerFieldTemplate

<a id="schemaconsumerfieldtemplate"></a>

```json
{
  "id": "string",
  "default": true,
  "special": true,
  "order": 0,
  "scope": "member",
  "required": true,
  "name": "string",
  "label": "string",
  "description": "string",
  "default_value": "string",
  "type": "address",
  "options": [
    {
      "type": "text",
      "value": "string"
    }
  ]
} 
```

Consumer Field Templates may be created at any time and will then be available to attach
to Purchases as Consumer Field Schemas. They are a way for merchants to capture custom
information from the organizer or all group members on a per-slot basis. Examples include
size for clothing orders, passenger information for flights, or pick-up times for local tours.

### Properties

Name|Type|Description
---|---|---|
id|string(uuid)|Pay By Group UUID for this consumer field template
default|boolean|Whether the template should be default or not.
special|boolean|Whether the template is a special field or not. Special fields are standardized fields where the values a user enters may be pre-populated based on that user's previous activity. These fields are shipping address, billing address, and phone number. 
order|integer(int32)|Order in which the template should be displayed.
scope|string|Either `member` (applies to every group member) or `purchase` (applies only for the organizer to fill out on behalf of the whole Purchase) 
required|boolean|Whether the field is required or not when the template is attached to a Purchase
name|string|A unique name for the template, used when referencing the template to attach it to a Purchase
label|string|Text displayed as the field label
description|string|Descriptive helper text explaining the field to the end user
default_value|string|Default value shown on landing for the user
type|string|Format for how the field is displayed to end users
options|[object]|Array of options for the user to select from, which applies for `single_select` and `multi-select` `type` templates 


#### Enumerated Values

|Property|Value|
|---|---|
scope|member|
scope|purchase|
type|address|
type|datetime|
type|multi_select|
type|single_select|
type|text|
type|textarea|


## ConsumerFieldValue

<a id="schemaconsumerfieldvalue"></a>

```json
{
  "id": "string",
  "schema_id": "string",
  "name": "string",
  "slot": 0,
  "value": "string"
} 
```

Consumer Field Values record what a user enters or selects when presented with a Consumer Field Schema.

### Properties

Name|Type|Description
---|---|---|
id|string(uuid)|Unique identifier for this consumer field value.
schema_id|string(uuid)|Unique identifier for the schema that this field value is attached to.
name|string|Name of schema this field value belongs to.
slot|integer(int32)|Member's slot this field value is applied to, which is only relevant when the value is for a membership and the Member claimed multiple slots in the group. 
value|string|Stored value entered by the member or organizer or selected from the available options for the schema.



## Contribution

<a id="schemacontribution"></a>

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
    }
  },
  "charged_at": "2017-11-27T23:35:47Z",
  "failed_at": "2017-11-27T23:35:47Z",
  "created_at": "string"
} 
```

Contribution(s) are nested inside each membership and describe the relationship between each
member and each payment, so a membership can have multiple contributions, 1 for each payment.

### Properties

Name|Type|Description
---|---|---|
id|string|UUID of this contribution
status|string|Current status of the contribution, any of: -`created` (default value when member is committed, but has no payment activity on this contribution yet); -`authorized` (the member's payment method was successfully authorized for this charge); -`captured` (the full contribution amount has been captured from the member's payment method); -`holdout` (the member is not currently committed to the purchase); or -`failed` (the charge or this contribution failed and Pay By Group is attempting to resolve it) 
refund_status|string|Status that determines whether the Contribution is partially or fully refunded, one of: -`none` (none of the Contribution's Transactions were refunded); -`partial` (some of the Contribution's Transactions were partially or fully refunded); or -`full` (all of the Contribution's Transactions were fully refunded) 
amount|[Money](#schemamoney)|Amount of this contribution, the sum of the purchase share and consumer fees
share_amount|[Money](#schemamoney)|This contribution's share of the total purchase, not including consumer fees
fees|[Fees](#schemafees)|The consumer fee added to this contribution's share and payable to Pay By Group
charged_at|string(date-time)|Timestamp of when this contibution was charged
failed_at|string(date-time)|Timestamp of when this contribution most recently failed, if at all
created_at|string|Timestamp when the record of this contribution was first created, which is not necessarily when it was charged 


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


## CurrencyConfig

<a id="schemacurrencyconfig"></a>

```json
{
  "supported_payment_sources": [
    {
      "type": "credit_card",
      "unsupported_cards": [
        "visa"
      ]
    }
  ]
} 
```

Describes the payment methods that members can and cannot use for their
contributions based on this Purchase's currency and payment destination

### Properties

Name|Type|Description
---|---|---|
supported_payment_sources|[[SupportedPaymentSource](#schemasupportedpaymentsource)]|List of supported payment sources for configuration



## Error

<a id="schemaerror"></a>

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

When an endpoint fails, the error object is returned

### Properties

Name|Type|Description
---|---|---|
errors|[object]|Array of errors returned by the endpoint



## Fees

<a id="schemafees"></a>

```json
{
  "consumer_fee": {
    "amount_cents": 0,
    "currency_code": "string"
  }
} 
```

Represents a set of possible fees applied to the object this belongs to.

### Properties

Name|Type|Description
---|---|---|
consumer_fee|[Money](#schemamoney)|Amount charged to the user and due to Pay By Group for the Membership



## Group

<a id="schemagroup"></a>

```json
{
  "commit_deadline": "2017-11-27T23:35:47Z",
  "max_slots": 0,
  "min_slots": 0,
  "min_contribution": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "organizer_email": "user@example.com",
  "organizer_full_name": "string",
  "split_type": "even_split"
} 
```

The Group parameters are nested in the Purchase object and cover selections typically made
by the group organizer within the constraints set by the Merchant.

### Properties

Name|Type|Description
---|---|---|
commit_deadline|string(date-time)|Pay By Group-generated deadline that encourages invitees to commit to the group quickly. It auto-extends unless overriden by the merchant or organizer. 
max_slots|integer(int32)|The organizer-specified value for the maximum number of slots they will allow to be claimed. It must be within the bounds of the highest max_slots set by the merchant in Product Costs 
min_slots|integer(int32)|The organizer-specified value for the minimum number of slots they require to be claimed. It must be above the minimum of the lowest min_slots set by the merchant in Product Costs 
min_contribution|[Money](#schemamoney)|The organizer-specified minimum required contribution by each member, which only applies for Purchases set to `specified_per_person` `split_type` 
organizer_email|string(email)|Email of the expected organizer as provided by the merchant
organizer_full_name|string|Full name of the expected organizer as provided by the merchant
split_type|string|Splitting type chosen by the organizer for how to divide the cost among group members, which is one of: `even_split` (only compatible with total cost_type and means the Purchase amount is split evenly across each slot claimed); `specified_per_person` (only compatible with total cost_type and means each member may pay a different amount); or `fixed_per_person` (only compatible with per_slot cost_type and means   each group member pays a fixed amount per slot they claim) 


#### Enumerated Values

|Property|Value|
|---|---|
split_type|even_split|
split_type|specified_per_person|
split_type|fixed_per_person|


## Image

<a id="schemaimage"></a>

```json
{
  "id": "string",
  "name": "string",
  "version": "string",
  "url": "string"
} 
```

This object is for all images in the system.

### Properties

Name|Type|Description
---|---|---|
id|string(uuid)|Pay By Group UUID of this image
name|string|Filename of the image as provided by the merchant
version|string|Version of the image as generated by Pay By Group
url|string|URL to retrieve the image stored with Pay By Group



## LegalBinding

<a id="schemalegalbinding"></a>

```json
{
  "id": "string",
  "type": "tos",
  "title": "string",
  "content": "string",
  "created_at": "string",
  "remote_ip": "string",
  "user_id": "string",
  "purchase_id": "string"
} 
```

Legal Bindings represent every instance a User agrees to the terms in a Legal Document
that is attached to a Purchase.

### Properties

Name|Type|Description
---|---|---|
id|string(uuid)|Pay By Group UUID of this specific record of acceptance by the user
type|string|Either `cancellation_policy` for cancellation and refund terms or `tos` for all other legal documents provided by merchant. 
title|string|Mechant's title for this legal document at the time it was accepted by the user
content|string|Full content as accepted by the user at the moment they agreed to this legal document
created_at|string|Verifiable timestamp when the user accepted this legal document
remote_ip|string|User's IP address at the moment they accepted this legal document
user_id|string|ID of the user that accepted the document, which includes their name and email
purchase_id|string|The purchase for which this document was accepted by the user


#### Enumerated Values

|Property|Value|
|---|---|
type|tos|
type|cancelation_policy|


## LegalDocument

<a id="schemalegaldocument"></a>

```json
{
  "id": "string",
  "type": "tos",
  "title": "string",
  "content": "string",
  "created_at": "2017-11-27T23:35:47Z",
  "updated_at": "2017-11-27T23:35:47Z"
} 
```

Each Legal Document may be attached, either via API or by default, to a Purchase and will
then be required for each group member to accept. Those acceptancs are stored as Legal Binding objects.

### Properties

Name|Type|Description
---|---|---|
id|string(uuid)|Pay By Group UUID of this legal document
type|string|Specified by the merchant as either `cancellation_policy` for cancellation and refund terms or `tos` for all other legal documents. 
title|string|Mechant's title for this legal document
content|string|Full content as provided by the merchant, either in plain text or as a URL
created_at|string(date-time)|When this legal document was added by the merchant
updated_at|string(date-time)|When this legal document was last updated by the merchant


#### Enumerated Values

|Property|Value|
|---|---|
type|tos|
type|cancelation_policy|


## Membership

<a id="schemamembership"></a>

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
    }
  },
  "consumer_field_values": {
    "id": "string",
    "schema_id": "string",
    "name": "string",
    "slot": 0,
    "value": "string"
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
      }
    },
    "charged_at": "2017-11-27T23:35:47Z",
    "failed_at": "2017-11-27T23:35:47Z",
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
    "created_at": "2017-11-27T23:35:47Z"
  },
  "purchase_id": "string",
  "payment_source": {
    "id": "string",
    "name": "string",
    "type": "string",
    "info": {
      "card_type": "string",
      "last_four": "string",
      "valid_until": "string"
    },
    "created_at": "2017-11-27T23:35:47Z"
  },
  "committed_at": "2017-11-27T23:35:47Z",
  "created_at": "2017-11-27T23:35:47Z"
} 
```

The Membership defines the relationship between a single end-user and the Purchase and
contains all details for that User's commitment to the Purchase.

### Properties

Name|Type|Description
---|---|---|
id|string|Pay By Group UUID for this membership
status|string|One of: `holdout` (user has been invited but not joined the group) or `committed` (user has joined the group and whether they have been charged is in the contribution object) 
refund_status|string|Status that determines whether the Membership is partially or fully refunded, which is one of: `none` (none of the Membership's Contributions were refunded); `partial` (some of the Membership's Contributions were partially or fully refunded); or `full` (all of the Membership's Contributions were fully refunded). 
failed|boolean|User is currently in the group with a failed payment method, which is preventing the purchase from completing 
short|boolean|The user is currently committed but has not agreed to pay their new required amount for their share due to changes to the purchase since they first committed. 
role|string|Either organizer or invitee
claimed_slots|integer(int32)|Number of slots the member has claimed in the group, defaulted to 1 if none is selected by the user
opt_in_marketing|boolean|True if the user has opted in to receive marketing communication from the merchant, otherwise false
amount|[Money](#schemamoney)|Total amount this member will be charged based on the current purchase details across all payments, which is the sum of the `share_amount` and `fees` 
share_amount|[Money](#schemamoney)|This member's share of the total purchase across all payments based on the current purchase details and not including fees 
fees|[Fees](#schemafees)|The total consumer fees paid to Pay By Group by this member
consumer_field_values|[ConsumerFieldValue](#schemaconsumerfieldvalue)|Values that have been filled out by the member for each consumer_field_schema scoped to the Purchase and each slot they have claimed, when applicable 
allowed_amount|[Money](#schemamoney)|Maximum amount, including consumer fees, this member has agreed to be charged under any circumstance across all payments
allowed_share_amount|[Money](#schemamoney)|Maximum amount this member has agreed to be charged for their share of the purchase across all payments
allowed_fees|[Fees](#schemafees)|Maximum amount this member has agreed to be charged for their consumer fees due to Pay By Group
collected_amount|[Money](#schemamoney)|Sum of all paid contributions making up this member's share that have been paid to date (including fees). 
collected_share_amount|[Money](#schemamoney)|Sum of all paid contributions making up this member's share that have been paid to date, not including fees
current_contribution|[Contribution](#schemacontribution)|This is the next upcoming contribution by this member towards their share of the Purchase and corresponds to the next Payment on the Purchase 
user|[User](#schemauser)|Details for the user that owns this membership
purchase_id|string(uuid)|Pay By Group UUID of the purchase to which this membership is tied
payment_source|[PaymentSource](#schemapaymentsource)|The payment source (e.g. credit card or bank account) currently tied to this membership to be used for all future contributions 
committed_at|string(date-time)|Timestamp of when the member committed to pay into the purchase
created_at|string(date-time)|When the membership was first created


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


## Merchant

<a id="schemamerchant"></a>

```json
{
  "id": "string",
  "unique_name": "string",
  "display_name": "string",
  "support_email": "user@example.com",
  "support_phone": "string",
  "logo_url": "string"
} 
```

Details for how the Merchant is referenced and presented to users

### Properties

Name|Type|Description
---|---|---|
id|string(uuid)|UUID for the merchant used for API calls
unique_name|string|Unique Pay By Group-assigned slug to identify easily identify the merchant
display_name|string|Display name chosen by the Merchant for end users to see
support_email|string(email)|Email provided by the Merchant for end users to contant
support_phone|string|Phone provided by the Merchant for end users to contant
logo_url|string|Logo provided by the merchant for display to end users



## MerchantProcessingFeesStructure

<a id="schemamerchantprocessingfeesstructure"></a>

```json
{
  "per_transaction": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "percentage": 1
} 
```

These parameters describe the fees a merchant is charged for processing payments.
These fees are always invoiced to the merchant and vary depending on whether the merchant
uses Pay By Group as their processor or a third-party gateway.

### Properties

Name|Type|Description
---|---|---|
per_transaction|[Money](#schemamoney)|Charge for each successful transaction sent through Pay By Group
percentage|integer(int32)|Percentage fee for each successful transaction sent through Pay By Group



## MerchantServiceFeesStructure

<a id="schemamerchantservicefeesstructure"></a>

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

These parameters describe the fees a merchant is charged for the Pay By Group service.
Typically they are charged in place of the Consumer Fees when the merchant chooses to absorb
the cost of the service instead of passing it onto end users. It is useful for merchants to
calculate their own costs if needed.

### Properties

Name|Type|Description
---|---|---|
per_share|[Money](#schemamoney)|Amount due per group member, which may be in place of or combined with `percentage`
per_purchase_max|[Money](#schemamoney)|Maximum total charge per each Purchase across all members
percentage|integer(int32)|Percentage fee applied to each member's share, which may be in place of or combined with `per_share`



## Money

<a id="schemamoney"></a>

```json
{
  "amount_cents": 0,
  "currency_code": "string"
} 
```

Structure of all money objects in the API

### Properties

Name|Type|Description
---|---|---|
amount_cents|integer(int32)|Format of all money values is in cents where 100 is equivalent to $1.00
currency_code|string|3-letter currency code attached to every money value



## Payment

<a id="schemapayment"></a>

```json
{
  "id": "string",
  "status": "pending",
  "number": 0,
  "percentage": 1,
  "due_deadline": "2017-11-27T23:35:47Z",
  "amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "submitted_at": "2017-11-27T23:35:47Z",
  "accepted_at": "2017-11-27T23:35:47Z",
  "paid_at": "2017-11-27T23:35:47Z",
  "processing_currency": "string",
  "conversion_rate": 0,
  "failed": true,
  "payout_failed": true
} 
```

A payment is a nested object (or array of objects) inside a purchase describing the amount(s)
a merchant expects to receive for a given purchase over time as a % of the product_cost(s).
A single purchase may have multiple payments over time, which may be a deposit + balance payment
or a series of installments. Most purchases have a single payment for 100% of the purchase value.

### Properties

Name|Type|Description
---|---|---|
id|string(uuid)|Pay By Group UUID for this payment
status|string|Current status of the payment, one of: `pending` (planned future payment on the purchase); `active` (currently active, next payment to be paid on the purchase); `authorizing` (contributions that comprise this payment are in the process of having their funds verified); `authorized` (all funds have been verified for this payment and it awaits acceptance by the merchant); `captured` (all funds have been taken from group members for the purchase and are awaiting payout to the merchant); `processing_payout` (payout to the merchant is in process); `canceled` (the Purchase, therefore the payment, has been canceled); `paid` (all funds are paid out to the Merchant's payout account). 
number|integer(int32)|Number of this payment in the overall sequence of the purchase. It is 0 if the purchase has only 1 payment. 
percentage|integer(int32)|Percent of the total Purchase cost due for this payment, which must be an integer. All payments on a purchase must sum to 100. 
due_deadline|string(date-time)|Datetime by when this payment must be submitted to the merchant for the purchase to be valid. It is required for all payments after the first payment but may be passed for the first, or only, payment as well. 
amount|[Money](#schemamoney)|Calculated amount, in currency, of this payment based on the percentage of the purchases total cost. 
submitted_at|string(date-time)|Timestamp when the payment is originally submitted by the organizer
accepted_at|string(date-time)|Timestamp when the payment is accepted by the merchant
paid_at|string(date-time)|Timestamp when the payment is paid out to the merchant
processing_currency|string|The required currency of the payment destination, which is the currency in which all transactions related to this payment occur 
conversion_rate|number(float)|If the currency of the purchase differs from the required currency of the payment destination then this is the conversion rate used to determine the transacted amount. 
failed|boolean|true if any of the contributions under this payment are currently in a failed state
payout_failed|boolean|true if the last attempt to perform a payout failed


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


## PaymentGateway

<a id="schemapaymentgateway"></a>

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

Merchants that choose to use a third-party gateway to receive payments will see
this object as the payment destination on their Purchases instead of a `bank_account`.

### Properties

Name|Type|Description
---|---|---|
id|string|Pay By Group UUID for this payment gateway
name|string|Displayed name of the gateway
merchant_id|string|Merchant this gateway belongs to
supported_currency_codes|[string]|3-letter currency codes that can be used for payments to this gateway



## PaymentSource

<a id="schemapaymentsource"></a>

```json
{
  "id": "string",
  "name": "string",
  "type": "string",
  "info": {
    "card_type": "string",
    "last_four": "string",
    "valid_until": "string"
  },
  "created_at": "2017-11-27T23:35:47Z"
} 
```

Each committed Member has a Payment Source that is charged for their contributions to the
Purchase and which is represented by this object.

### Properties

Name|Type|Description
---|---|---|
id|string(uuid)|Pay By Group UUID of this payment source
name|string|Full name of this payment source's owner
type|string|Describes the type of payment source, any of credit_card or bank_account
info|[PaymentSourceInfo](#schemapaymentsourceinfo)|Detailed information of this payment source
created_at|string(date-time)|Timestamp when the payment source was first added to the system



## PaymentSourceInfo

<a id="schemapaymentsourceinfo"></a>

```json
{
  "card_type": "string",
  "last_four": "string",
  "valid_until": "string"
} 
```

Detailed information of a given Payment Source

### Properties

Name|Type|Description
---|---|---|
card_type|string|Brand of card, i.e. visa, mastercard, etc.
last_four|string|Last four digits of the credit card.
valid_until|string|Expiration date in mm/yy format.



## PaymentTransaction

<a id="schemapaymenttransaction"></a>

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
    }
  },
  "payout_account": {
    "id": "string",
    "name": "string",
    "status": "verified",
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
      "card_type": "string",
      "last_four": "string",
      "valid_until": "string"
    },
    "created_at": "2017-11-27T23:35:47Z"
  },
  "created_at": "2017-11-27T23:35:47Z",
  "processing_currency": "string",
  "conversion_rate": 0
} 
```

A Payment Transaction is the most granular object that exists in the Pay By Group system from
a financial tracking standpoint. Every interaction with a Payment Source or Payment Destination
will have one or more corresponding Payment Transaction records. Each Contribution typically
will have 2 Payment Transactions, an `auth` and a `capture`, but a single Contribution will
have multiple `auths` and/or `captures` in rare cases.

### Properties

Name|Type|Description
---|---|---|
id|string(uuid)|Pay By Group UUID for this transaction
short_id|string|Unique ID of this transaction for easy reference
parent_id|string|Another transaction related to and replaced by this one - e.g. the credit card authorization for which this transaction is the capture or the capture for which this is the refund. 
chargable_type|string|Entity name of the chargable object related to this transaction, one of: `contribution`, `payment`, or `invoice` 
action|string|One of: -`auth` (holds funds or the specified amount on the user's payment method for later capture); -`capture` (captures funds that were previously authorized at an amount = or < the authorized amount); -`charge` (instantly charges an amount without first making an authorization); -`void` (voids a previously created authorization); -`refund` (refunds a previously created capture or charge); -`payout` (sends funds to a payout bank account). 
status|string|One of: -`pending` (transaction has been submitted for processing and our system awaits reponse); -`completed` (transaction succeeded); or -`failed` (transaction failed) 
amount|[Money](#schemamoney)|Amount, in cents, of the transaction
fees|[Fees](#schemafees)|Portion of the transaction that is consumer fees separate from the purchase's share of the transaction 
payout_account|[BankAccount](#schemabankaccount)|Payout account where the transaction is paid out to
payment_gateway|[PaymentGateway](#schemapaymentgateway)|Payment gateway where the transaction is run directly into
payment_source|[PaymentSource](#schemapaymentsource)|Payment source of funds for this transaction
created_at|string(date-time)|Timestamp when the transaction was created
processing_currency|string|The currency in which this transaction occurred
conversion_rate|number(float)|If the currency of the purchase differs from the required currency of the payout account then this is the conversion rate used to determine the transaction amount in the processing_currency. 


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


## Product

<a id="schemaproduct"></a>

```json
{
  "images": [
    {
      "id": "string",
      "name": "string",
      "version": "string",
      "url": "string"
    }
  ],
  "default_image_url": "string",
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
  "start_datetime": "2017-11-27T23:35:47Z",
  "end_datetime": "2017-11-27T23:35:47Z",
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
      "created_at": "2017-11-27T23:35:47Z",
      "updated_at": "2017-11-27T23:35:47Z"
    }
  ]
} 
```

The product is a nested object inside the Purchase that defines all the details of
what is being bought. All Product parameters are set by the merchant.

### Properties

Name|Type|Description
---|---|---|
default_image_url|string|The primary or default image for this product first displayed to end users
cost_type|string|Cost type that determines whether the product_costs amount(s) are: -`total` (single total amount so long as the number of slots claimed is in the allowed range for that amount) or -`per_slot` (amount is per slot claimed in the Purchase so the total amount paid to the merchant is a function of the number of slots claimed by group members) 
description|string|Description of the product for this Purchase for end users
name|string|Name of the product being purchased as it should be shown to end users
start_datetime|string(date-time)|Start date time for the product being purchased (e.g. check-in date time, flight departure date time, or event starting time) 
end_datetime|string(date-time)|End date time for the product being purchased (e.g. check-out date time, flight arrival date time, or activity ending time) 
external_purchase_id|string|ID supplied by the merchant that identifies this Purchase (e.g. order or booking) in the merchant's system 
inventory_id|string|Inventory ID supplied by the merchant that identifies the product being bought in this Purchase (e.g. SKU or property ID) 
link|string|Link to the product being purchased on the merchant's (or other third party's) website
max_slots|integer(int32)|The maximum possible slots allowed by the merchant based on product_costs
min_slots|integer(int32)|The minimum possible slots allowed by the merchant based on product_costs
images|[[Image](#schemaimage)]|The set of images showcasing this product to end users
costs|[[ProductCost](#schemaproductcost)]|The set of product_costs and the optional allowed range(s) of slots for each provided by the merchant 
legal_documents|[[LegalDocument](#schemalegaldocument)]|All legal documents attached to this purchase that must be agreed to by the group members


#### Enumerated Values

|Property|Value|
|---|---|
cost_type|total|
cost_type|per_slot|


## ProductCost

<a id="schemaproductcost"></a>

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

Product Cost is a nested object inside the product that allows Merchants
to vary the price of the Purchase based on the size of the group that participates
to make the Purchase.

### Properties

Name|Type|Description
---|---|---|
amount|[Money](#schemamoney)|Cost as provided by the merchant (either `total` or `per_slot` depending on the `cost_type` for this range of slots. If no slots are provided, it is for the entire Purchase. 
min_slots|integer(int32)|Minimum number of slots that must be claimed by group members before the Purchase can be made at the amount specified for this range. 
max_slots|integer(int32)|Maximum allowed number of slots that may be claimed by group members at the amount specified for this range. 



## Purchase

<a id="schemapurchase"></a>

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
    "logo_url": "string"
  },
  "status": "created",
  "currency_code": "string",
  "payments": [
    {
      "id": "string",
      "status": "pending",
      "number": 0,
      "percentage": 1,
      "due_deadline": "2017-11-27T23:35:47Z",
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "submitted_at": "2017-11-27T23:35:47Z",
      "accepted_at": "2017-11-27T23:35:47Z",
      "paid_at": "2017-11-27T23:35:47Z",
      "processing_currency": "string",
      "conversion_rate": 0,
      "failed": true,
      "payout_failed": true
    }
  ],
  "current_payment": {
    "id": "string",
    "status": "pending",
    "number": 0,
    "percentage": 1,
    "due_deadline": "2017-11-27T23:35:47Z",
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "submitted_at": "2017-11-27T23:35:47Z",
    "accepted_at": "2017-11-27T23:35:47Z",
    "paid_at": "2017-11-27T23:35:47Z",
    "processing_currency": "string",
    "conversion_rate": 0,
    "failed": true,
    "payout_failed": true
  },
  "next_payment_due_deadline": "2017-11-27T23:35:47Z",
  "product": {
    "images": [
      {
        "id": "string",
        "name": "string",
        "version": "string",
        "url": "string"
      }
    ],
    "default_image_url": "string",
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
    "start_datetime": "2017-11-27T23:35:47Z",
    "end_datetime": "2017-11-27T23:35:47Z",
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
        "created_at": "2017-11-27T23:35:47Z",
        "updated_at": "2017-11-27T23:35:47Z"
      }
    ]
  },
  "group": {
    "commit_deadline": "2017-11-27T23:35:47Z",
    "max_slots": 0,
    "min_slots": 0,
    "min_contribution": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "organizer_email": "user@example.com",
    "organizer_full_name": "string",
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
        }
      },
      "consumer_field_values": {
        "id": "string",
        "schema_id": "string",
        "name": "string",
        "slot": 0,
        "value": "string"
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
          }
        },
        "charged_at": "2017-11-27T23:35:47Z",
        "failed_at": "2017-11-27T23:35:47Z",
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
        "created_at": "2017-11-27T23:35:47Z"
      },
      "purchase_id": "string",
      "payment_source": {
        "id": "string",
        "name": "string",
        "type": "string",
        "info": {
          "card_type": "string",
          "last_four": "string",
          "valid_until": "string"
        },
        "created_at": "2017-11-27T23:35:47Z"
      },
      "committed_at": "2017-11-27T23:35:47Z",
      "created_at": "2017-11-27T23:35:47Z"
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
  "needed_amount_to_current_payment": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "committed_slots": 0,
  "needed_slots_to_min": 0,
  "product_or_group_min_slots": 0,
  "product_or_group_max_slots": 0,
  "tipped": true,
  "auto_pilot_enabled": true,
  "auto_pilot_trigger_slots": 0,
  "current_product_cost_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
  "current_total_cost_amount": {
    "amount_cents": 0,
    "currency_code": "string"
  },
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
  "consumer_field_schemas": [
    {
      "id": "string",
      "order": 0,
      "scope": "member",
      "required": true,
      "name": "string",
      "label": "string",
      "description": "string",
      "default_value": "string",
      "type": "address",
      "options": [
        {
          "type": "text",
          "value": "string"
        }
      ]
    }
  ],
  "has_consumer_field_schemas": true,
  "consumer_field_values": [
    {
      "id": "string",
      "schema_id": "string",
      "name": "string",
      "slot": 0,
      "value": "string"
    }
  ],
  "payment_destination_id": "string",
  "currency_config": {
    "supported_payment_sources": [
      {
        "type": "credit_card",
        "unsupported_cards": [
          "visa"
        ]
      }
    ]
  },
  "refund_status": "none",
  "processing_refund": true,
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
  "language_code": "DA (Danish)",
  "created_at": "2017-11-27T23:35:47Z"
} 
```

The purchase object is the core object that ties together all other objects involved in a group purchase.

### Properties

Name|Type|Description
---|---|---|
id|string(uuid)|Pay By Group UUID for this Purchase used for API calls
slug|string|Short, unique identifier of this Purchase for easy reference in the Business Portal, with end users, and in URLs. 
merchant|[Merchant](#schemamerchant)|The merchant under which this Purchase exists.
status|string|Current status of the Purchase, one of: -`created` (Purchase has been created by the Merchant); -`active` (Purchase has been claimed by an organizer and is in process); -`completed` (All payments have been successfully paid out to the Merchant for this Purchase. No further changes or payments may be made, only refunds.); or -`canceled` (Purchase has been canceled by the merchant or organizer and is not recoverable). 
currency_code|string|3-letter currency code that determines how all money values relatedd to the Purchase are presented to users 
current_payment|[Payment](#schemapayment)|This is the next upcoming group payment due for the purchase
next_payment_due_deadline|string(date-time)|This is the next due deadline set by the merchant for an upcoming payment. If the current payment does not have a `due_deadline` then the `due_deadline` for the next payment after that will apply here. 
product|[Product](#schemaproduct)|Hash that includes all product attributes, which are set by the Merchant
group|[Group](#schemagroup)|Hash that includes all group attributes, which are usually provided by the organizer or set by Pay By Group
collected_shares_amount|[Money](#schemamoney)|Sum of all collected contributions so far where the Members were successfully charged.
committed_shares_amount|[Money](#schemamoney)|Sum of all Contributions group Members have agreed to pay towards the Purchase's total cost at this point, even though some or all of these may not yet be collected. 
needed_amount_to_current_payment|[Money](#schemamoney)|Amount group Members must still commit to in order to submit the current Payment, which applies primarily to Purchases with the `specified_per_person` `split_type` 
committed_slots|integer(int32)|Sum of all slots group Members have committed to in the Purchase at this point
needed_slots_to_min|integer(int32)|Number of slots group members must claim in order to meet the minimum required to submit the current payment, which applies primarily to Purchases with the `even_split` and `fixed_per_person` split types 
product_or_group_min_slots|integer(int32)|The active minimum number of slots that must be claimed, which is the higher of the values set by the merchant and organizer in cases where both exist 
product_or_group_max_slots|integer(int32)|The active maximum number of slots that are allowed to be claimed, which is the lower of the values set by the merchant and organizer in cases where both exist 
tipped|boolean|The minimum required slots have been claimed (even_split and fixed_per_person split_types) or amount committed (specified_per_person split_type) for the organizer to submit payment 
auto_pilot_enabled|boolean|The organizer has chosen to have payments triggered automatically as soon as the trigger_slots level they set is reached. For multi-payment Purchases, payments subsequent to the first payment are triggered automatically one day before each payment's `due_deadline`. 
auto_pilot_trigger_slots|integer(int32)|The number of slots set by the organizer, which when reached, automatically triggers the next payment's submission without requiring any further action by the organizer. 
current_product_cost_amount|[Money](#schemamoney)|The cost of the product (either `total` or `per_slot` depending on `cost_type`) for this Purchase based on the current number of claimed slots 
current_total_cost_amount|[Money](#schemamoney)|Total amount due to merchant for this Purchase based on the current number of claimed slots
has_consumer_field_schemas|boolean|Whether or not this Purchase has any consumer field schemas declared
payment_destination_id|string(uuid)|ID of the payment destination, either a bank account or third-party gateway, that will receive all future Payments made under this Purchase, which means all Payments that are still in `active` status 
currency_config|[CurrencyConfig](#schemacurrencyconfig)|Describes the payment methods that members can and cannot use for their contributions based on this Purchase's currency and payment destination 
refund_status|string|Status that describes whether the Purchase is partially or fully refunded, one of: `none` (none of the Purchase's Memberships were refunded); `partial` (some of the Purchase's Memberships were partially or fully refunded); or `full` (all of the Purchase's Memberships were fully refunded). 
processing_refund|boolean|Determines whether or not a refund is currently being processed for the Purchase. If multiple refunds have been triggered, they will be processed sequentially instead of synchronously.
fees_structure|[PurchaseFeesStructure](#schemapurchasefeesstructure)|Full breakdown of fees due to Pay By Group from the merchant and/or group member(s) for this Purchase 
apply_consumer_fee_to_organizer|boolean|Tells if the consumer_fees apply to the purchase's organizer for this Purchase
language_code|string|Default 2-character language code for this purchase. It is going to be used in the claim and commit steps; and as one of the fallbacks when detecting what language to show to the user 
created_at|string(date-time)|Timestamp of when the Purchase was first created by the merchant
payments|[[Payment](#schemapayment)]|Full payment schedule as set by the merchant for this Purchase
memberships|[[Membership](#schemamembership)]|Array that includes all members in this Purchase and the details for each. The only information not included are every `contribution` if it is a multi-payment Purchase. Only the Contribution for the current Payment is included. 
cost_range|[[ProductCost](#schemaproductcost)]|The minimum and maximum possible costs for this product based on the `costs` merchant supplies and the current `product_or_group_min_slots` and `product_or_group_max_slots`, presented as the set of the two `product_costs` that define the minimum and maximum possible costs. 
consumer_field_schemas|[[ConsumerFieldSchema](#schemaconsumerfieldschema)]|The set of consumer field schemas that are attached to this Purchase and their accompanying options
consumer_field_values|[[ConsumerFieldValue](#schemaconsumerfieldvalue)]|Values that have been provided by the organizer for each consumer_field_schema scoped to the Purchase


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
language_code|DA (Danish)|
language_code|EN (English)|
language_code|ES (Spanish)|


## PurchaseFeesStructure

<a id="schemapurchasefeesstructure"></a>

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

Defines which consumer and merchant fees structures apply based on the currency of the
Purchase and its payment destination type.

### Properties

Name|Type|Description
---|---|---|
currency_code|string|3-letter currency code for which this fee structure applies
payment_destination_type|string|Payment destination type for which this fee structure applies
consumer_fees|[ConsumerFeesStructure](#schemaconsumerfeesstructure)|Structure of fees paid by end users for using Pay By Group, which can be in place of or in addition to merchant_service_fees 
merchant_service_fees|[MerchantServiceFeesStructure](#schemamerchantservicefeesstructure)|Fees charged to merchant for use of the Pay By Group service, which can be in place of or in addition to consumer_fees 
merchant_processing_fees|[MerchantProcessingFeesStructure](#schemamerchantprocessingfeesstructure)|Fees charged to the merchant for the processing of payments, either through the Pay By Group gateway or the merchant's own gateway 


#### Enumerated Values

|Property|Value|
|---|---|
payment_destination_type|bank_account|
payment_destination_type|payment_gateway|


## SupportedPaymentSource

<a id="schemasupportedpaymentsource"></a>

```json
{
  "type": "credit_card",
  "unsupported_cards": [
    "visa"
  ]
} 
```

Describes the charteristics of a supported payment source

### Properties

Name|Type|Description
---|---|---|
type|string|Type of the supported payment source
unsupported_cards|[string]|List of unsupported credit cards for this particular payment source if the type is `credit_card`. If none are listed, then all of Amex, Diner's Club, Discover, JCB, MasterCard, and Visa are supported. 


#### Enumerated Values

|Property|Value|
|---|---|
type|credit_card|
unsupported_cards|visa|
unsupported_cards|master|
unsupported_cards|american_express|
unsupported_cards|discover|
unsupported_cards|jcb|
unsupported_cards|diners_club|
unsupported_cards|dankort|


## User

<a id="schemauser"></a>

```json
{
  "id": "string",
  "email": "user@example.com",
  "full_name": "string",
  "first_name": "string",
  "last_name": "string",
  "avatar_url": "string",
  "language_code": "string",
  "created_at": "2017-11-27T23:35:47Z"
} 
```

Each user is a single end-user who can have multiple memberships across different Purchases.

### Properties

Name|Type|Description
---|---|---|
id|string(uuid)|Pay By Group UUID for this user
email|string(email)|User's email address
full_name|string|User's full name
first_name|string|User's first name
last_name|string|User's last name
avatar_url|string|URL of the User's avatar
language_code|string|The preferred language selected by this user
created_at|string(date-time)|Timestamp of when this user was first created






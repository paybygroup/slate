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



- Basic Authentication. Use your own Access Key and Secret Key.



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
        "due_deadline": "2017-11-24T22:58:00Z",
        "paid_at": "2017-11-24T22:58:00Z",
        "accepted_at": "2017-11-24T22:58:00Z",
        "submitted_at": "2017-11-24T22:58:00Z",
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
      "due_deadline": "2017-11-24T22:58:00Z",
      "paid_at": "2017-11-24T22:58:00Z",
      "accepted_at": "2017-11-24T22:58:00Z",
      "submitted_at": "2017-11-24T22:58:00Z",
      "amount": {
        "amount_cents": 0,
        "currency_code": "string"
      },
      "conversion_rate": 0,
      "processing_currency": "string",
      "failed": true,
      "payout_failed": true
    },
    "next_payment_due_deadline": "2017-11-24T22:58:00Z",
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
      "end_datetime": "2017-11-24T22:58:00Z",
      "start_datetime": "2017-11-24T22:58:00Z",
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
          "created_at": "2017-11-24T22:58:00Z",
          "updated_at": "2017-11-24T22:58:00Z"
        }
      ]
    },
    "group": {
      "commit_deadline": "2017-11-24T22:58:00Z",
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
          "charged_at": "2017-11-24T22:58:00Z",
          "failed_at": "2017-11-24T22:58:00Z",
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
          "created_at": "2017-11-24T22:58:00Z"
        },
        "committed_at": "2017-11-24T22:58:00Z",
        "created_at": "2017-11-24T22:58:00Z"
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
    "created_at": "2017-11-24T22:58:00Z"
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
body|body|object|true|Request body object.
» product|body|object|false|No description
»» name|body|string|false|Name of the product being purchased as it should be shown to end users
»» cost_type|body|string|false|Cost type that determines whether the product_costs amount(s) are:<br/>- per_slot The amount is per slot claimed in the Purchase so the<br/>  total amount paid to the merchant is a function of the number of<br/>  slots claimed by group members.<br/>- total A single total amount so long as the number of slots claimed<br/>  is in the allowed range for that amount.<br/>
»» description|body|string|false|Description of the product for this Purchase
»» default_image_url|body|string|false|The primary or default image for this product
»» inventory_id|body|string|false|Inventory ID supplied by the merchant that identifies the product<br/>being bought in this Purchase (e.g. SKU or property ID)<br/>
»» link|body|string|false|Link to the product being purchased on the merchant's (or other third party's) website
»» start_datetime|body|string(date-time)|false|Start date time for the product being purchased<br/>(e.g. check-in date time, flight departure date time, or event<br/>starting time)<br/>
»» end_datetime|body|string(date-time)|false|End date time for the product being purchased<br/>(e.g. check-out date time, flight arrival date time, or activity<br/>ending time)<br/>
»» external_purchase_id|body|string|false|ID supplied by the merchant that identifies this Purchase<br/>(e.g. order or booking) in the merchant's system<br/>
»» costs|body|[[ProductCost](#schemaproductcost)]|false|The set of product_costs and the optional allowed range(s) of slots<br/>for each provided by the merchant<br/>
» group|body|object|false|No description
»» organizer_full_name|body|string|false|Full name of the expected organizer as provided by the merchant
»» organizer_email|body|string(email)|false|Email of the expected organizer as provided by the merchant
»» legal_document_ids|body|[string]|false|Array of legal document IDs that must be accepted by the members in this purchase
» language_code|body|string|false|Default language for this purchase. It is going to be used in the<br/>claim and commit steps; and as one of the fallbacks when detecting<br/>what language to show to the user<br/>
» payment_destination_id|body|string(uuid)|false|ID of the payment destination that will receive all future payments<br/>made under this Purchase.<br/>
» payments|body|[object]|false|No description
»» percentage|body|integer(int32)|false|Percent of the total purchase cost due for this payment, which must<br/>be an integer. All payments on a purchase must sum to 100.<br/>
»» due_deadline|body|string(date-time)|false|Datetime by when this payment must be submitted to the merchant for<br/>the purchase to be valid.<br/>It is required for all payments after the first payment but may be<br/>passed for the first, or only, payment as well.<br/>
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
      "due_deadline": "2017-11-24T22:58:00Z",
      "paid_at": "2017-11-24T22:58:00Z",
      "accepted_at": "2017-11-24T22:58:00Z",
      "submitted_at": "2017-11-24T22:58:00Z",
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
    "due_deadline": "2017-11-24T22:58:00Z",
    "paid_at": "2017-11-24T22:58:00Z",
    "accepted_at": "2017-11-24T22:58:00Z",
    "submitted_at": "2017-11-24T22:58:00Z",
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "conversion_rate": 0,
    "processing_currency": "string",
    "failed": true,
    "payout_failed": true
  },
  "next_payment_due_deadline": "2017-11-24T22:58:00Z",
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
    "end_datetime": "2017-11-24T22:58:00Z",
    "start_datetime": "2017-11-24T22:58:00Z",
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
        "created_at": "2017-11-24T22:58:00Z",
        "updated_at": "2017-11-24T22:58:00Z"
      }
    ]
  },
  "group": {
    "commit_deadline": "2017-11-24T22:58:00Z",
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
        "charged_at": "2017-11-24T22:58:00Z",
        "failed_at": "2017-11-24T22:58:00Z",
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
        "created_at": "2017-11-24T22:58:00Z"
      },
      "committed_at": "2017-11-24T22:58:00Z",
      "created_at": "2017-11-24T22:58:00Z"
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
  "created_at": "2017-11-24T22:58:00Z"
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
      "due_deadline": "2017-11-24T22:58:00Z",
      "paid_at": "2017-11-24T22:58:00Z",
      "accepted_at": "2017-11-24T22:58:00Z",
      "submitted_at": "2017-11-24T22:58:00Z",
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
    "due_deadline": "2017-11-24T22:58:00Z",
    "paid_at": "2017-11-24T22:58:00Z",
    "accepted_at": "2017-11-24T22:58:00Z",
    "submitted_at": "2017-11-24T22:58:00Z",
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "conversion_rate": 0,
    "processing_currency": "string",
    "failed": true,
    "payout_failed": true
  },
  "next_payment_due_deadline": "2017-11-24T22:58:00Z",
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
    "end_datetime": "2017-11-24T22:58:00Z",
    "start_datetime": "2017-11-24T22:58:00Z",
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
        "created_at": "2017-11-24T22:58:00Z",
        "updated_at": "2017-11-24T22:58:00Z"
      }
    ]
  },
  "group": {
    "commit_deadline": "2017-11-24T22:58:00Z",
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
        "charged_at": "2017-11-24T22:58:00Z",
        "failed_at": "2017-11-24T22:58:00Z",
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
        "created_at": "2017-11-24T22:58:00Z"
      },
      "committed_at": "2017-11-24T22:58:00Z",
      "created_at": "2017-11-24T22:58:00Z"
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
  "created_at": "2017-11-24T22:58:00Z"
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
To perform this operation, you must be authenticated by HTTP Basic Authorization header.
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
    "start_datetime": "2017-11-24T22:58:00Z",
    "end_datetime": "2017-11-24T22:58:00Z",
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
      "due_deadline": "2017-11-24T22:58:00Z"
    }
  ]
}
```
<h3 id="UpdatePurchase-parameters">Parameters</h3>

Parameter|In|Type|Required|Description
---|---|---|---|---|
id|path|string(uuid)|true|ID of the Purchase to update.
body|body|object|true|Request body object.
» language_code|body|string|false|Default language for this purchase. It is going to be used in the<br/>claim and commit steps; and as one of the fallbacks when detecting<br/>what language to show to the user<br/>
» payment_destination_id|body|string(uuid)|false|ID of the payment destination that will receive all future payments<br/>made under this Purchase.<br/>
» product|body|object|false|No description
»» name|body|string|false|Name of the product being purchased as it should be shown to end users
»» description|body|string|false|Description of the product for this Purchase
»» default_image_url|body|string|false|The primary or default image for this product
»» inventory_id|body|string|false|Inventory ID supplied by the merchant that identifies the product<br/>being bought in this Purchase (e.g. SKU or property ID)<br/>
»» link|body|string|false|Link to the product being purchased on the merchant's (or other third party's) website
»» start_datetime|body|string(date-time)|false|Start date time for the product being purchased<br/>(e.g. check-in date time, flight departure date time, or event<br/>starting time)<br/>
»» end_datetime|body|string(date-time)|false|End date time for the product being purchased<br/>(e.g. check-out date time, flight arrival date time, or activity<br/>ending time)<br/>
»» external_purchase_id|body|string|false|ID supplied by the merchant that identifies this Purchase<br/>(e.g. order or booking) in the merchant's system<br/>
»» costs|body|[[ProductCost](#schemaproductcost)]|false|The set of product_costs and the optional allowed range(s) of slots<br/>for each provided by the merchant<br/>
» group|body|object|false|No description
»» organizer_full_name|body|string|false|Full name of the expected organizer as provided by the merchant
»» organizer_email|body|string(email)|false|Email of the expected organizer as provided by the merchant
»» split_type|body|string|false|Splitting type chosen by the organizer for how to divide the cost<br/>among group members.<br/>One of:<br/>- even_split Only compatible with total cost_type and means the<br/>  Purchase amount is split evenly across each slot claimed.<br/>- specified_per_person Only compatible with total cost_type and<br/>  means each member may pay a different amount.<br/>- fixed_per_person Only compatible with per_slot cost_type and means<br/>  each group member pays a fixed amount per slot they claim.<br/>
»» max_slots|body|integer(int32)|false|The organizer-specified value for the maximum number of slots they<br/>will allow to be claimed.<br/>It must be within the bounds allowed by the merchant.<br/>
»» min_slots|body|integer(int32)|false|The organizer-specified value for the minimum number of slots they<br/>require to be claimed.<br/>It must be within the bounds allowed by the merchant.<br/>
»» legal_document_ids|body|[string]|false|Array of legal document IDs that must be accepted by the members in this purchase
» payments|body|[object]|false|No description
»» percentage|body|integer(int32)|false|Percent of the total purchase cost due for this payment, which must<br/>be an integer. All payments on a purchase must sum to 100.<br/>
»» due_deadline|body|string(date-time)|false|Datetime by when this payment must be submitted to the merchant for<br/>the purchase to be valid.<br/>It is required for all payments after the first payment but may be<br/>passed for the first, or only, payment as well.<br/>


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
      "due_deadline": "2017-11-24T22:58:00Z",
      "paid_at": "2017-11-24T22:58:00Z",
      "accepted_at": "2017-11-24T22:58:00Z",
      "submitted_at": "2017-11-24T22:58:00Z",
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
    "due_deadline": "2017-11-24T22:58:00Z",
    "paid_at": "2017-11-24T22:58:00Z",
    "accepted_at": "2017-11-24T22:58:00Z",
    "submitted_at": "2017-11-24T22:58:00Z",
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "conversion_rate": 0,
    "processing_currency": "string",
    "failed": true,
    "payout_failed": true
  },
  "next_payment_due_deadline": "2017-11-24T22:58:00Z",
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
    "end_datetime": "2017-11-24T22:58:00Z",
    "start_datetime": "2017-11-24T22:58:00Z",
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
        "created_at": "2017-11-24T22:58:00Z",
        "updated_at": "2017-11-24T22:58:00Z"
      }
    ]
  },
  "group": {
    "commit_deadline": "2017-11-24T22:58:00Z",
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
        "charged_at": "2017-11-24T22:58:00Z",
        "failed_at": "2017-11-24T22:58:00Z",
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
        "created_at": "2017-11-24T22:58:00Z"
      },
      "committed_at": "2017-11-24T22:58:00Z",
      "created_at": "2017-11-24T22:58:00Z"
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
  "created_at": "2017-11-24T22:58:00Z"
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
body|body|object|true|Request body object.
» organizer_name|body|string|false|Name of the organizer
» organizer_email|body|string|false|Email of the organizer
» organizer_allowed_share_amount|body|[Money](#schemamoney)|false|Allowed share of the organizer
» min_contribution|body|[Money](#schemamoney)|false|Min contribution amount
» group|body|object|false|No description
»» split_type|body|string|false|Splitting type chosen by the organizer for how to divide the cost<br/>among group members.<br/>One of:<br/>- even_split Only compatible with total cost_type and means the<br/>  Purchase amount is split evenly across each slot claimed.<br/>- specified_per_person Only compatible with total cost_type and<br/>  means each member may pay a different amount.<br/>- fixed_per_person Only compatible with per_slot cost_type and means<br/>  each group member pays a fixed amount per slot they claim.<br/>
»» max_slots|body|integer(int32)|false|The organizer-specified value for the maximum number of slots they<br/>will allow to be claimed.<br/>It must be within the bounds allowed by the merchant.<br/>
»» min_slots|body|integer(int32)|false|The organizer-specified value for the minimum number of slots they<br/>require to be claimed.<br/>It must be within the bounds allowed by the merchant.<br/>


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
      "due_deadline": "2017-11-24T22:58:00Z",
      "paid_at": "2017-11-24T22:58:00Z",
      "accepted_at": "2017-11-24T22:58:00Z",
      "submitted_at": "2017-11-24T22:58:00Z",
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
    "due_deadline": "2017-11-24T22:58:00Z",
    "paid_at": "2017-11-24T22:58:00Z",
    "accepted_at": "2017-11-24T22:58:00Z",
    "submitted_at": "2017-11-24T22:58:00Z",
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "conversion_rate": 0,
    "processing_currency": "string",
    "failed": true,
    "payout_failed": true
  },
  "next_payment_due_deadline": "2017-11-24T22:58:00Z",
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
    "end_datetime": "2017-11-24T22:58:00Z",
    "start_datetime": "2017-11-24T22:58:00Z",
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
        "created_at": "2017-11-24T22:58:00Z",
        "updated_at": "2017-11-24T22:58:00Z"
      }
    ]
  },
  "group": {
    "commit_deadline": "2017-11-24T22:58:00Z",
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
        "charged_at": "2017-11-24T22:58:00Z",
        "failed_at": "2017-11-24T22:58:00Z",
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
        "created_at": "2017-11-24T22:58:00Z"
      },
      "committed_at": "2017-11-24T22:58:00Z",
      "created_at": "2017-11-24T22:58:00Z"
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
  "created_at": "2017-11-24T22:58:00Z"
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
body|body|object|true|Request body object.
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
body|body|object|true|Request body object.
» reason|body|string|false|Reason why this amount is being refunded
» amount|body|[Money](#schemamoney)|false|Amount to be refunded. It may not be greater than the current<br/>collected amount of the purchase, which is the total purchase<br/>amount net of any previous refunds. If the memberships_shares<br/>are provided, this value must equal the sum of those shares.<br/>
» funding_source_id|body|string(uuid)|false|UUID of the merchant's payment source for funding refunds
» memberships_shares|body|[object]|false|No description
»» membership_id|body|string|false|ID of the membership to refund.
»» amount|body|[Money](#schemamoney)|false|Amount to refund to this member.


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
      "due_deadline": "2017-11-24T22:58:00Z",
      "paid_at": "2017-11-24T22:58:00Z",
      "accepted_at": "2017-11-24T22:58:00Z",
      "submitted_at": "2017-11-24T22:58:00Z",
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
    "due_deadline": "2017-11-24T22:58:00Z",
    "paid_at": "2017-11-24T22:58:00Z",
    "accepted_at": "2017-11-24T22:58:00Z",
    "submitted_at": "2017-11-24T22:58:00Z",
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "conversion_rate": 0,
    "processing_currency": "string",
    "failed": true,
    "payout_failed": true
  },
  "next_payment_due_deadline": "2017-11-24T22:58:00Z",
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
    "end_datetime": "2017-11-24T22:58:00Z",
    "start_datetime": "2017-11-24T22:58:00Z",
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
        "created_at": "2017-11-24T22:58:00Z",
        "updated_at": "2017-11-24T22:58:00Z"
      }
    ]
  },
  "group": {
    "commit_deadline": "2017-11-24T22:58:00Z",
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
        "charged_at": "2017-11-24T22:58:00Z",
        "failed_at": "2017-11-24T22:58:00Z",
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
        "created_at": "2017-11-24T22:58:00Z"
      },
      "committed_at": "2017-11-24T22:58:00Z",
      "created_at": "2017-11-24T22:58:00Z"
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
  "created_at": "2017-11-24T22:58:00Z"
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
» reason|body|string|false|Description to be provided to the group's organizer<br/>explaining why the group was canceled<br/>


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
body|body|object|false|Request body object.
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
To perform this operation, you must be authenticated by HTTP Basic Authorization header.
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
      "charged_at": "2017-11-24T22:58:00Z",
      "failed_at": "2017-11-24T22:58:00Z",
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
      "created_at": "2017-11-24T22:58:00Z"
    },
    "committed_at": "2017-11-24T22:58:00Z",
    "created_at": "2017-11-24T22:58:00Z"
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
      "created_at": "2017-11-24T22:58:00Z"
    },
    "created_at": "2017-11-24T22:58:00Z",
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
    "created_at": "2017-11-24T22:58:00Z",
    "updated_at": "2017-11-24T22:58:00Z"
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
200|[OK](https://tools.ietf.org/html/rfc7231#section-6.3.1)|Success response|[[LegalBinding](#schemalegalbinding)]
404|[Not Found](https://tools.ietf.org/html/rfc7231#section-6.5.4)|Not found|[Error](#schemaerror)

<aside class="warning">
To perform this operation, you must be authenticated by HTTP Basic Authorization header.
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
To perform this operation, you must be authenticated by HTTP Basic Authorization header.
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
    "created_at": "2017-11-24T22:58:00Z",
    "updated_at": "2017-11-24T22:58:00Z"
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
body|body|object|true|Request body object.
» type|body|string|false|Specified by the merchant as either cancellation policy for cancellation and refund terms<br/>or tos for all other legal documents<br/>
» title|body|string|false|Mechant's title for this legal document
» content|body|string|false|Full content as provided by the merchant, either in plain text or as a URL<br/>


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
  "created_at": "2017-11-24T22:58:00Z",
  "updated_at": "2017-11-24T22:58:00Z"
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
  "created_at": "2017-11-24T22:58:00Z",
  "updated_at": "2017-11-24T22:58:00Z"
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
body|body|object|true|Request body object.
» type|body|string|false|Specified by the merchant as either cancellation policy for cancellation<br/>and refund terms or tos for all other legal documents<br/>
» title|body|string|false|Mechant's title for this legal document
» content|body|string|false|Full content as provided by the merchant, either in plain text or as a URL<br/>


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
  "created_at": "2017-11-24T22:58:00Z",
  "updated_at": "2017-11-24T22:58:00Z"
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
body|body|object|true|Request body object.
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
To perform this operation, you must be authenticated by HTTP Basic Authorization header.
</aside>

# Schemas

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
      "due_deadline": "2017-11-24T22:58:00Z",
      "paid_at": "2017-11-24T22:58:00Z",
      "accepted_at": "2017-11-24T22:58:00Z",
      "submitted_at": "2017-11-24T22:58:00Z",
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
    "due_deadline": "2017-11-24T22:58:00Z",
    "paid_at": "2017-11-24T22:58:00Z",
    "accepted_at": "2017-11-24T22:58:00Z",
    "submitted_at": "2017-11-24T22:58:00Z",
    "amount": {
      "amount_cents": 0,
      "currency_code": "string"
    },
    "conversion_rate": 0,
    "processing_currency": "string",
    "failed": true,
    "payout_failed": true
  },
  "next_payment_due_deadline": "2017-11-24T22:58:00Z",
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
    "end_datetime": "2017-11-24T22:58:00Z",
    "start_datetime": "2017-11-24T22:58:00Z",
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
        "created_at": "2017-11-24T22:58:00Z",
        "updated_at": "2017-11-24T22:58:00Z"
      }
    ]
  },
  "group": {
    "commit_deadline": "2017-11-24T22:58:00Z",
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
        "charged_at": "2017-11-24T22:58:00Z",
        "failed_at": "2017-11-24T22:58:00Z",
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
        "created_at": "2017-11-24T22:58:00Z"
      },
      "committed_at": "2017-11-24T22:58:00Z",
      "created_at": "2017-11-24T22:58:00Z"
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
  "created_at": "2017-11-24T22:58:00Z"
} 
```

A purchase object.

### Properties

Name|Type|Description
---|---|---|
id|string(uuid)|Pay By Group UUID for this Purchase used for API calls
slug|string|Short, unique identifier of this Purchase for easy reference in the Business Portal and with end users 
merchant|[Merchant](#schemamerchant)|No description
status|string|Current status of the purchase. One of: - created Purchase has been created by the Merchant. - active Purchase has been claimed by an organizer and is in process. - completed All payments have been successfully paid out to the Merchant for this Purchase. - canceled The Purchase has been canceled by the merchant or organizer and is not recoverable. 
refund_status|string|Status that determines whether the Purchase is partially or fully refunded. One of: - none None of the Purchase's Memberships were refunded. - partial Some of the Purchase's Memberships were partially or fully refunded. - full All of the Purchase's Memberships were fully refunded. 
processing_refund|boolean|Determines whether or not a refund is being processed for the purchase.
tipped|boolean|The minimum required slots have been claimed for the organizer to submit payment
auto_pilot_enabled|boolean|The organizer has chosen to have payments triggered automatically as soon as the trigger_slots level they set is reached 
auto_pilot_trigger_slots|integer(int32)|The number of slots set by the organizer, which when reached, will automatically trigger payment submission 
has_consumer_field_schemas|boolean|Whether or not this purchase has any consumer field schema declared.
currency_code|string|3-letter currency code for all money values related to the Purchase
payment_destination_id|string(uuid)|ID of the payment destination that will receive all future payments made under this Purchase.
currency_config|object|All unsupported payment source types by this Purchase's payment destination, which members cannot use for their contributions 
current_payment|[Payment](#schemapayment)|This is the next upcoming payment by the group towards the purchase
next_payment_due_deadline|string(date-time)|This is the next due deadline set by the merchant for an upcoming payment
current_product_cost_amount|[Money](#schemamoney)|Product cost amount for this Purchase based on the current number of claimed slots
current_total_cost_amount|[Money](#schemamoney)|Total amount due to merchant for this Purchase based on the current number of claimed slots
max_product_cost_by_slots|[ProductCost](#schemaproductcost)|The maximum cost this product may be based on the set of product_costs
min_product_cost_by_slots|[ProductCost](#schemaproductcost)|The minimum cost this product may be based on the set of product_costs
max_product_cost_by_amount|[ProductCost](#schemaproductcost)|The maximum cost this product may be based on the set of product_costs
fees_structure|[PurchaseFeesStructure](#schemapurchasefeesstructure)|Full breakdown of fees due to Pay By Group from the merchant and/or group member(s) for this Purchase 
apply_consumer_fee_to_organizer|boolean|Tells if consumer fee applies to the purchase's organizer
product|[Product](#schemaproduct)|Hash that includes all product attributes
group|[Group](#schemagroup)|Hash that includes all group attributes
collected_shares_amount|[Money](#schemamoney)|Sum of all collected shares so far.
committed_shares_amount|[Money](#schemamoney)|Sum of all payments group members have agreed to pay towards the Purchase''s total cost at this point 
committed_slots|integer(int32)|Sum of all slots group members have claimed in the Purchase at this point
needed_amount_to_current_payment|[Money](#schemamoney)|Amount group members must still commit to in order to submit the current payment
needed_slots_to_min|integer(int32)|Number of slots group members must claim in order to meet the minimum required to submit the current payment 
product_or_group_max_slots|integer(int32)|The active minimum number of slots that must be claimed based on the parameters set by the merchant and organizer 
product_or_group_min_slots|integer(int32)|The active maximum number of slots that are allowed to be claimed based on the parameters set by the merchant and organizer 
language_code|string|Default language for this purchase. It is going to be used in the claim and commit steps; and as one of the fallbacks when detecting what language to show to the user 
created_at|string(date-time)|Timestamp of when the Purchase was first created by the merchant
consumer_fields|[[ConsumerField](#schemaconsumerfield)]|Array of consumer fields for this Purchase
consumer_field_values|[[ConsumerFieldValue](#schemaconsumerfieldvalue)]|Array of values for each of the consumer fields defined.
consumer_field_schemas|[[ConsumerFieldSchema](#schemaconsumerfieldschema)]|List of consumer field schemas to use for the purchase
payments|[[Payment](#schemapayment)]|Full payment schedule as set by the merchant for this Purchase
cost_range|[[ProductCost](#schemaproductcost)]|The range of possible costs for this product based on the product_costs merchant provides
memberships|[[Membership](#schemamembership)]|Array that includes all members in this Purchase without their contributions.


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

<a id="schemamerchant"></a>

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

Name|Type|Description
---|---|---|
id|string(uuid)|Unique ID for the merchant.
unique_name|string|Unique Pay By Group-assigned slug to identify this merchant
display_name|string|Display name chosen by merchant for end users to see
support_email|string(email)|Email provided for end users to contant the merchant
support_phone|string|Phone provided for end users to contant the merchant
logo_url|string|Logo provided by the merchant for display to end users
defaults|[MerchantDefaults](#schemamerchantdefaults)|All default settings for the merchant that are used for Purchases when the corresponding value is not specified 



## MerchantDefaults

<a id="schemamerchantdefaults"></a>

```json
{
  "currency_code": "string",
  "language_code": "string",
  "timezone_code": "string",
  "product_image_url": "string"
} 
```

undefined

### Properties

Name|Type|Description
---|---|---|
currency_code|string|Default currency code for this merchant, which applies to new purchases where a currency is not specified 
language_code|string|Default language for this merchant, which applies to new purchases where a default language is not specified 
timezone_code|string|Default timezone code for this merchant, which applies to new datetimes created under the merchant's purchases where a time is not specified. 
product_image_url|string|URL of the default image for this merchant, which applies to new purchases where a purchase image is not specified. 



## ConsumerField

<a id="schemaconsumerfield"></a>

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

undefined

### Properties

Name|Type|Description
---|---|---|
name|string|No description
label|string|No description
description|string|No description
type|string|No description
settings|object|No description
scope|string|No description
default_value|string|No description


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

<a id="schemaconsumerfieldvalue"></a>

```json
{
  "name": "string",
  "scope": "member",
  "required": true
} 
```

undefined

### Properties

Name|Type|Description
---|---|---|
name|string|Name of the schema
scope|string|One of member or purchase.
required|boolean|Whether the schema field should be required or not.


#### Enumerated Values

|Property|Value|
|---|---|
scope|member|
scope|purchase|


## ConsumerFieldSchema

<a id="schemaconsumerfieldschema"></a>

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

undefined

### Properties

Name|Type|Description
---|---|---|
id|string(uuid)|No description
name|string|No description
label|string|No description
scope|string|Any of member or purchase.
required|boolean|Whether the field for this schema should be required or not.
type|string|No description


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

<a id="schemapayment"></a>

```json
{
  "id": "string",
  "status": "pending",
  "number": 0,
  "percentage": 1,
  "due_deadline": "2017-11-24T22:58:00Z",
  "paid_at": "2017-11-24T22:58:00Z",
  "accepted_at": "2017-11-24T22:58:00Z",
  "submitted_at": "2017-11-24T22:58:00Z",
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

undefined

### Properties

Name|Type|Description
---|---|---|
id|string(uuid)|Pay By Group UUID for this payment
status|string|One of: - pending A planned future payment on the purchase. - active The currently active, next payment to be paid on the purchase - authorizing The constituent contributions that comprise this   payment are in the process of having their funds verified. - authorized All funds have been verified for this payment and it   awaits acceptance by the merchant. - captured All funds have been taken from group members for the   purchase and are awaiting payout to the merchant. - processing_payout The payout to the merchant is in process. - canceled This payment has been canceled. - paid All funds are paid out to the Payout Account. 
number|integer(int32)|Number of this payment in the overall sequence of the purchase. It is 0 if the purchase has only 1 payment. 
percentage|integer(int32)|Percent of the total purchase cost due for this payment, which must be an integer. All payments on a purchase must sum to 100. 
due_deadline|string(date-time)|Datetime by when this payment must be submitted to the merchant for the purchase to be valid. It is required for all payments after the first payment but may be passed for the first, or only, payment as well. 
paid_at|string(date-time)|Timestamp when the payment is paid out to the merchant
accepted_at|string(date-time)|Timestamp when the payment is accepted by the merchant
submitted_at|string(date-time)|Timestamp when the payment is originally submitted by the organizer
amount|[Money](#schemamoney)|Calculated amount, in currency, of this payment based on the percentage of the purchases total cost. 
conversion_rate|number(float)|If the currency of the purchase differs from the required currency of the payment destination then this is the conversion rate used to determine the transacted amount. 
processing_currency|string|The required currency of the payment destination, which is the currency in which all transactions related to this payment occur 
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


## Money

<a id="schemamoney"></a>

```json
{
  "amount_cents": 0,
  "currency_code": "string"
} 
```

undefined

### Properties

Name|Type|Description
---|---|---|
amount_cents|integer(int32)|Format of all money values is in cents where 100 is equivalent to $1.00
currency_code|string|3-letter currency code attached to every money value



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

undefined

### Properties

Name|Type|Description
---|---|---|
amount|[Money](#schemamoney)|Total cost as provided by the merchant for this range of slots. If no slots are provided, it is for the entire Purchase. 
min_slots|integer(int32)|Minimum number of slots that must be claimed by group members before the Purchase can be made at the amount specified for this range. 
max_slots|integer(int32)|Maximum allowed number of slots that may be claimed by group members at the amount specified for this range. 



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

undefined

### Properties

Name|Type|Description
---|---|---|
currency_code|string|3-letter currency code for which this fee structure applies
payment_destination_type|string|Payment destination identifier for which this fee structure applies
consumer_fees|[ConsumerFeesStructure](#schemaconsumerfeesstructure)|Structure of fees paid by end users for using Pay By Group
merchant_service_fees|[MerchantServiceFeesStructure](#schemamerchantservicefeesstructure)|Fees charged to merchant for use of the Pay By Group service. Can be in place of or in addition to consumer fee. 
merchant_processing_fees|[MerchantProcessingFeesStructure](#schemamerchantprocessingfeesstructure)|Fees charged to the merchant for the processing of payments, either through the Pay By Group gateway or the merchant's own gateway 


#### Enumerated Values

|Property|Value|
|---|---|
payment_destination_type|bank_account|
payment_destination_type|payment_gateway|


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

undefined

### Properties

Name|Type|Description
---|---|---|
per_share|[Money](#schemamoney)|Amount due per group member, which overrides the percentage value if both exist. 
per_share_max|[Money](#schemamoney)|Maximum charge per member's total share when applying the percentage
per_share_min|[Money](#schemamoney)|Minimum charge per member's total share when applying the percentage
percentage|integer(int32)|Percentage applied to member's total share to determine fee



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

undefined

### Properties

Name|Type|Description
---|---|---|
per_share|[Money](#schemamoney)|Amount due per group member.
per_purchase_max|[Money](#schemamoney)|Maximum total charge per each Purchase across all members
percentage|integer(int32)|Percentage fee applied to each member's share



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

undefined

### Properties

Name|Type|Description
---|---|---|
per_transaction|[Money](#schemamoney)|Charge for each successful transaction sent through Pay By Group
percentage|integer(int32)|Percentage fee for each successful transaction sent through Pay By Group



## Product

<a id="schemaproduct"></a>

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
  "end_datetime": "2017-11-24T22:58:00Z",
  "start_datetime": "2017-11-24T22:58:00Z",
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
      "created_at": "2017-11-24T22:58:00Z",
      "updated_at": "2017-11-24T22:58:00Z"
    }
  ]
} 
```

undefined

### Properties

Name|Type|Description
---|---|---|
default_image_url|string|The primary or default image for this product
cost_type|string|Cost type that determines whether the product_costs amount(s) are: - per_slot The amount is per slot claimed in the Purchase so the   total amount paid to the merchant is a function of the number of   slots claimed by group members. - total A single total amount so long as the number of slots claimed   is in the allowed range for that amount. 
description|string|Description of the product for this Purchase
name|string|Name of the product being purchased as it should be shown to end users
end_datetime|string(date-time)|End date time for the product being purchased (e.g. check-out date time, flight arrival date time, or activity ending time) 
start_datetime|string(date-time)|Start date time for the product being purchased (e.g. check-in date time, flight departure date time, or event starting time) 
external_purchase_id|string|ID supplied by the merchant that identifies this Purchase (e.g. order or booking) in the merchant's system 
inventory_id|string|Inventory ID supplied by the merchant that identifies the product being bought in this Purchase (e.g. SKU or property ID) 
link|string|Link to the product being purchased on the merchant's (or other third party's) website
max_slots|integer(int32)|The maximum possible slots allowed by the merchant based on product_costs
min_slots|integer(int32)|The minimum possible slots allowed by the merchant based on product_costs
images|[[Image](#schemaimage)]|The set of images for this product
allowed_split_types|[string]|Array of allowed split types
costs|[[ProductCost](#schemaproductcost)]|The set of product_costs and the optional allowed range(s) of slots for each provided by the merchant 
legal_documents|[[LegalDocument](#schemalegaldocument)]|All legal documents attached to this purchase that must be agreed to by the group members


#### Enumerated Values

|Property|Value|
|---|---|
cost_type|total|
cost_type|per_slot|
» type|tos|
» type|cancelation_policy|


## Image

<a id="schemaimage"></a>

```json
{
  "name": "string",
  "version": "string",
  "url": "string"
} 
```

Attaches an image of the product to the purchase specified in the
request. The most recent image uploaded will be the primary image for
the purchase.

### Properties

Name|Type|Description
---|---|---|
name|string|Filename of the image as provided by the merchant
version|string|Version of the image generated by PBG
url|string|No description



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
    "charged_at": "2017-11-24T22:58:00Z",
    "failed_at": "2017-11-24T22:58:00Z",
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
    "created_at": "2017-11-24T22:58:00Z"
  },
  "committed_at": "2017-11-24T22:58:00Z",
  "created_at": "2017-11-24T22:58:00Z"
} 
```

undefined

### Properties

Name|Type|Description
---|---|---|
id|string|Pay By Group UUID for this membership
status|string|One of: - holdout (user has been invited but not joined the group); - committed (user has joined the group and whether they have been charged is in the contribution object); 
refund_status|string|Status that determines whether the Membership is partially or fully refunded. One of: - none (none of the Membership's Contributions were refunded). - partial (some of the Membership's Contributions were partially   or fully refunded). - full (all of the Membership's Contributions were fully refunded). 
failed|boolean|User is currently in the group with a failed payment method, which is preventing the purchase from completing 
short|boolean|The user is currently in the group but has not agreed to pay their new required share amount due to updates to the purchase. 
role|string|Either organizer or invitee
claimed_slots|integer(int32)|Number of slots the member has claimed in the group. Defaults to 1 if none is selected by the user.
opt_in_marketing|boolean|true if the user has opted in to receive marketing communication from the merchant. Otherwise false.
amount|[Money](#schemamoney)|Total amount this member will be charged based on the current purchase details. It is the sum of the purchase share and consumer fees 
share_amount|[Money](#schemamoney)|This member's share of the total purchase based on the current purchase details, not including consumer fees 
fees|[Fees](#schemafees)|The total consumer fees paid to Pay By Group by this member
consumer_field_values|[ConsumerFieldValue](#schemaconsumerfieldvalue)|No description
allowed_amount|[Money](#schemamoney)|Maximum amount, including consumer fees, this member has agreed to be charged under any circumstance
allowed_share_amount|[Money](#schemamoney)|Maximum amount this member has agreed to be charged for their share of the purchase
allowed_fees|[Fees](#schemafees)|Maximum amount this member has agreed to be charged for their consumer fees due to Pay By Group
max_amount|[Money](#schemamoney)|No description
max_share_amount|[Money](#schemamoney)|No description
max_fees|[Fees](#schemafees)|No description
collected_amount|[Money](#schemamoney)|Sum of all paid contributions making up this member's share that have been paid to date (including fees). 
collected_share_amount|[Money](#schemamoney)|Sum of all paid contributions making up this member's share that have been paid to date
current_contribution|[Contribution](#schemacontribution)|This is the next upcoming payment by this member towards their share of the purchase
user|[User](#schemauser)|Details for the user that owns this membership
purchase_id|string(uuid)|Pay By Group slug of the purchase to which this membership is tied
payment_source|[PaymentSource](#schemapaymentsource)|The payment source (e.g. credit card or bank account) currently tied to this membership to be used for all future contributions. 
committed_at|string(date-time)|Timestamp of when the member agreed to pay into the purchase
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

<a id="schemafees"></a>

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

undefined

### Properties

Name|Type|Description
---|---|---|
consumer_fee|[Money](#schemamoney)|No description
merchant_service_fee|[Money](#schemamoney)|No description



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
    },
    "merchant_service_fee": {
      "amount_cents": 0,
      "currency_code": "string"
    }
  },
  "charged_at": "2017-11-24T22:58:00Z",
  "failed_at": "2017-11-24T22:58:00Z",
  "created_at": "string"
} 
```

undefined

### Properties

Name|Type|Description
---|---|---|
id|string|UUID of this contribution
status|string|Current status of the contribution, any of created, authorized, captured, holdout or failed
refund_status|string|Status that determines whether the Contribution is partially or fully refunded. One of: - none (none of the Contribution's Transactions were refunded). - partial (some of the Contribution's Transactions were partially   or fully refunded). - full (all of the Contribution's Transactions were fully refunded). 
amount|[Money](#schemamoney)|Amount of this contribution, the sum of the purchase share and consumer fees
share_amount|[Money](#schemamoney)|This contribution's share of the total purchase, not including consumer fees
fees|[Fees](#schemafees)|The consumer fee added to this contribution's share and paid to Pay By Group
charged_at|string(date-time)|Timestamp of when this contibution was charged
failed_at|string(date-time)|Timestamp of when this contribution most recently failed
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
  "created_at": "string"
} 
```

undefined

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
created_at|string(uuid)|No description



## PaymentSource

<a id="schemapaymentsource"></a>

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
  "created_at": "2017-11-24T22:58:00Z"
} 
```

undefined

### Properties

Name|Type|Description
---|---|---|
id|string(uuid)|Pay By Group UUID of this payment source
name|string|Full name of this payment source's owner
type|string|Describes the type of payment source, any of credit_card or bank_account
info|object|Bank account information of this payment source
created_at|string(date-time)|Timestamp when the payment source was first added to the system



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

Creates a new consumer field template

### Properties

Name|Type|Description
---|---|---|
errors|[object]|Array of errors returned by the endpoint



## Group

<a id="schemagroup"></a>

```json
{
  "commit_deadline": "2017-11-24T22:58:00Z",
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

undefined

### Properties

Name|Type|Description
---|---|---|
commit_deadline|string(date-time)|Pay By Group-generated deadline that encourages invitees to commit to the group quickly. It auto-extends unless overriden by the merchant or organizer 
max_slots|integer(int32)|The organizer-specified value for the maximum number of slots they will allow to be claimed. It must be within the bounds allowed by the merchant. 
min_slots|integer(int32)|The organizer-specified value for the minimum number of slots they require to be claimed. It must be within the bounds allowed by the merchant. 
min_contribution|[Money](#schemamoney)|The organizer-specified minimum required contribution by each member
organizer_email|string(email)|Email of the expected organizer as provided by the merchant
organizer_full_name|string|Full name of the expected organizer as provided by the merchant
split_type|string|Splitting type chosen by the organizer for how to divide the cost among group members. One of: - even_split Only compatible with total cost_type and means the   Purchase amount is split evenly across each slot claimed. - specified_per_person Only compatible with total cost_type and   means each member may pay a different amount. - fixed_per_person Only compatible with per_slot cost_type and means   each group member pays a fixed amount per slot they claim. 
legal_document_ids|[string]|Array of legal document IDs that must be accepted by the members in this purchase


#### Enumerated Values

|Property|Value|
|---|---|
split_type|even_split|
split_type|specified_per_person|
split_type|fixed_per_person|


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
    "created_at": "2017-11-24T22:58:00Z"
  },
  "created_at": "2017-11-24T22:58:00Z",
  "processing_currency": "string",
  "conversion_rate": 0
} 
```

undefined

### Properties

Name|Type|Description
---|---|---|
id|string(uuid)|Pay By Group UUID for this transaction
short_id|string|Unique ID of this transaction for easy reference
parent_id|string|Another transaction related to and replaced by this one - e.g. the credit card authorization for which this transaction is the capture or the capture for which this is the refund. 
chargable_type|string|No description
action|string|One of: - auth (holds funds or the specified amount on the user's payment   method for later capture). - capture (captures funds that were previously authorized at an   amount = or < the authorized amount). - charge (instantly charges an amount without first making an   authorization). - void (voids a previously created authorization). - refund (refunds a previously created capture or charge). - payout (sends funds to a bank account). 
status|string|Oneo of pending, completed or failed
amount|[Money](#schemamoney)|Amount, in cents, of the transaction
fees|[Fees](#schemafees)|Portion of the transaction that was consumer fees separate from the purchase's share of the transaction. 
payout_account|[BankAccount](#schemabankaccount)|Payout account where the transaction is paid out to.
payment_gateway|[PaymentGateway](#schemapaymentgateway)|Payment gateway where the transaction is run through
payment_source|[PaymentSource](#schemapaymentsource)|Payment source of funds for the transaction
created_at|string(date-time)|Timestamp when the transaction was created
processing_currency|string|The currency in which this transaction occurred
conversion_rate|number(float)|If the currency of the purchase differs from the required currency of the payout account then this is the conversion rate used to determine the transaction amount. 


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

<a id="schemabankaccount"></a>

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

undefined

### Properties

Name|Type|Description
---|---|---|
id|string(uuid)|Pay By Group UUID for this bank account
name|string|Displayed name of bank account with last 4 of account number
status|string|verified or unverified depending on whether micro-deposit amounts have confirmed account ownership
user_id|string(uuid)|User that added the bank account
merchant_id|string(uuid)|Merchant this bank account belongs to
currency_configs|string|Set of payment sources supported across all currencies for this bank account. Not all currencies support all payment sources. 
supported_currency_codes|[string]|3-letter currency codes that can be used for credits and debits with this account


#### Enumerated Values

|Property|Value|
|---|---|
status|verified|
status|unverified|


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

undefined

### Properties

Name|Type|Description
---|---|---|
id|string|Pay By Group UUID for this payment gateway
name|string|Displayed name of the gateway
merchant_id|string|Merchant this gateway belongs to
supported_currency_codes|[string]|3-letter currency codes that can be used for payments to this gateway



## LegalDocument

<a id="schemalegaldocument"></a>

```json
{
  "id": "string",
  "type": "tos",
  "title": "string",
  "content": "string",
  "created_at": "2017-11-24T22:58:00Z",
  "updated_at": "2017-11-24T22:58:00Z"
} 
```

undefined

### Properties

Name|Type|Description
---|---|---|
id|string(uuid)|Pay By Group UUID of this legal document
type|string|Specified by the merchant as either cancellation policy for cancellation and refund terms or tos for all other legal documents. 
title|string|Mechant's title for this legal document
content|string|Full content as provided by the merchant, either in plain text or as a URL
created_at|string(date-time)|When this legal document was added by the merchant
updated_at|string(date-time)|When this legal document was last updated by the merchant


#### Enumerated Values

|Property|Value|
|---|---|
type|tos|
type|cancelation_policy|


## LegalBinding

<a id="schemalegalbinding"></a>

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

undefined

### Properties

Name|Type|Description
---|---|---|
id|string(uuid)|Pay By Group UUID of this specific record of acceptance by the user
type|string|Either cancellation policy for cancellation and refund terms or tos for all other legal documents provided by merchant. 
title|string|Mechant's title for this legal document as accepted by the user
content|string|Full content as accepted by the user at the moment they agreed to this legal document
created_at|string|Verifiable timestamp when the user accepted this legal document
remote_ip|string|User's IP address at the moment they accepted this legal document
user_id|string|ID of the user that accepted the document, which includes their name and email
purchase_id|string|The purchase for which this document was accepted by the user



## ConsumerFieldTemplate

<a id="schemaconsumerfieldtemplate"></a>

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

undefined

### Properties

Name|Type|Description
---|---|---|
id|string(uuid)|Pay By Group UUID for this consumer field template
name|string|A unique name for the template.
label|string|Text to display as the field label.
description|string|A description for the template
type|string|Type of field to display for this template.
default_value|string|Default value to use for the template.
order|integer(int32)|Order in which the template should be displayed.
scope|string|Whether the template is at the member level, or purchase level.
default|boolean|Whether the template should be default or not.
special|boolean|Whether the template is a special field or not.
required|boolean|Whether the template is required or not.
options|[object]|Array of options to use for a list template.


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





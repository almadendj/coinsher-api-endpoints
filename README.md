#### GET  ``` /sellers ```
```javascript
// DESCRIPTION: GET LIST OF SELLERS
Params: {
	currency: "BTC",
	fiat_currency?: "PHP",
	limit: 10,
	amount?: 5000,
	offset: 10, // to control pagination
	payment_methods?: [ "pm_gcash", "bpi_bank", "..." ],
}

Returns: [
	{
		"id": "seller123",
		"profile_pic": "https://coinsher.com/public/lkasjdfkldaj",
		"username": "seller_name",
		"total_orders": 100,
		"rating": 4.8,
		"rate": 3594662.38,
		"minimum": 1000,
		"maximum": 10000,
		"available_amount": 2.5,
		"currency": "BTC",
		"average_completion_time": "30 minutes",
		"verified": true,
		"fiat_currency": "PHP",
		"payment_methods"?: [
			{
				"name": "GCASH",
				"logo": "https://gcash.com/klsajdfjla",
			}, 
			{
				"name": "GCASH",
				"logo": "https://gcash.com/klsajdfjla",
			},
		],
	}
]
```

#### GET  ``` /sellers/{seller_id} ```
```javascript
// DESCRIPTION: GET SELLER
Params: {
	currency: "BTC",
	fiat_currency?: "PHP",
	limit: 10,
	amount?: 5000,
	offset: 10, // to control pagination
	payment_methods?: [ "pm_gcash", "bpi_bank", "..." ],
}

Returns: {
	"id": "seller123",
	"profile_pic": "https://coinsher.com/public/lkasjdfkldaj",
	"username": "seller_name",
	"total_orders": 100,
	"rating": 4.8,
	"minimum": 1000,
	"maximum": 10000,
	"rate": 3594662.38,
	"available_amount": 2.5,
	"currency": "BTC",
	"average_completion_time": "30 minutes",
	"verified": true,
	"fiat_currency": "PHP",
	"payment_methods"?: [
		{
			"name": "GCASH",
			"logo": "https://gcash.com/klsajdfjla",
		}, 
		{
			"name": "GCASH",
			"logo": "https://gcash.com/klsajdfjla",
		},
	],
}
```

### GET  ``` /buyers ``` 
```javascript
// DESCRIPTION: GET LIST OF BUYERS
Params: {
	currency: "USDT",
	fiat_currency?: "PHP",
	amount?: 5000,
	limit: 10,
	offset: 10,
	payment_methods: [ "pm_gcash", "bpi_bank", "..." ],
}

Returns: [
	{
		"id": "listing123",
		"username": "buyer_name",
		"profile_pic": "https://coinsher.com/public/alkjasdlkjf",
		"rating": 4.5,
		"minimum": 1000,
		"maximum": 10000,
		"total_orders": 100,
		"rate": 3594662.38,
		"min_amount": 0.01,
		"max_amount": 5,
		"currency": "BTC",
		"fiat_currency": "USD",
		"average_completion_time": "45 minutes",
		"verified": true,
		"payment_methods"?: [
			{
				"name": "GCASH",
				"logo": "https://gcash.com/klsajdfjla",
			}, 
			{
				"name": "GCASH",
				"logo": "https://gcash.com/klsajdfjla",
			},
		],
	}
]
```

### GET  ``` /buyers/{buyer_id} ``` 
```javascript
// DESCRIPTION: GET BUYER
Params: {
	currency: "USDT",
	fiat_currency?: "PHP",
	amount?: 5000,
	limit: 10,
	offset: 10,
	payment_methods: [ "pm_gcash", "bpi_bank", "..." ],
}

Returns: {
	"id": "listing123",
	"username": "buyer_name",
	"profile_pic": "https://coinsher.com/public/alkjasdlkjf",
	"rating": 4.5,
	"minimum": 1000,
	"maximum": 10000,
	"total_orders": 100,
	"rate": 3594662.38,
	"min_amount": 0.01,
	"max_amount": 5,
	"currency": "BTC",
	"fiat_currency": "USD",
	"average_completion_time": "45 minutes",
	"verified": true,
	"payment_methods"?: [
		{
			"name": "GCASH",
			"logo": "https://gcash.com/klsajdfjla",
		}, 
		{
			"name": "GCASH",
			"logo": "https://gcash.com/klsajdfjla",
		},
	],
}
```

### POST ```/buy/buy-order ```
```javascript
Params: {
	seller_id: "sellerID",
	amount: 100,
	currency: "BTC",
	fiat_currency: "PHP",
	payment_method: "pm_gcash"
}

Returns: {
	"order_id": "order123",
	"seller_id": "seller123",
	"buyer_id": "buyer123",
	"amount": 100,
	"currency": "BTC",
	"fiat_currency": "PHP",
	"payment_method": "GCash",
	"status": "pending"
}
```

### GET ``` /orders/{order_id} ```
```javascript
Returns: {
	"order_id": "order123",
	"seller_id": "seller123",
	"buyer_id": "buyer123",
	"amount": 100, // crypto amount
	"currency": "BTC",
	"fiat_currency": "PHP",
	"price": 58.78, // price in fiat currency
	"payment_method": "GCash",
	"status": "pending",
	"created_at": "2024-07-01T12:00:00Z", 
	"expires_at": "2024-07-01T15:00:00Z"
}
```

### POST ```/orders/{order_id}/confirm-payment```
```javascript
Params: {
	// none for now
}

Returns: {
	"order_id": "order123",
	"status": "confirmed",
	"message": "Order status updated successfully."
}
```

### POST ``` /orders/{order_id}/upload-proof ```
```javascript
Params: {
	file: // file data
}

Returns: {
	"order_id": "order123",
	"proof_id": "proof123",
	"file_url": "https://example.com/lkjasdf",
	"status": "uploaded",
	"message": "Proof of payment uploaded successfully"
}
```
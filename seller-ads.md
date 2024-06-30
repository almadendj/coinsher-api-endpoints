### GET  ``` /sellers ```
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
			"id": "pm_gcash",
			"name": "GCash",
			"logo_url": "https://example.com/lkajd",
		},
		{
			"id": "bpi",
			"name": "BPI Bank Transfer",
			"logo_url": "https://example.com/lksjdf",
		}
	],
}
```
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
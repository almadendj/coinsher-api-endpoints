### GET ``` /user/ads ```
```js
Authentication: true

Returns: [
	{
		"ad_id": "ad123",
		"type": "buy",
		"currency": "BTC",
		"fiat_currency": "PHP",
		"amount": 1000,
		"price_per_unit": 3700000,
		"payment_methods": [
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
		"status": "online",
		"created_at": "2024-07-02T14:30:00Z",
	},
	{
		"ad_id": "ad123",
		"type": "buy",
		"currency": "BTC",
		"fiat_currency": "PHP",
		"amount": 1000,
		"price_per_unit": 3700000,
		"payment_methods": [
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
		"status": "online",
		"created_at": "2024-07-02T14:30:00Z",
	}
]
```
### POST ``` /create-buy-ads ```
```js
Params: {
	currency: "ETH",
	fiat_currency: "USD",
	minimum: 100,
	maximum: 10000,
	price_per_unit: 370092.12,
	amount: 5000,
	payment_methods: [ "pm_gcash", "bpi_transfer", "..." ],
	time_limit: 30, // in minutes
	status: "online",
	remarks: "sample remark....",
	auto_reply: "sample auto reply...",
}

Returns: {
	"ad_id": "ad123",
	"buyer_id": "buyer123",
	"currency": "BTC",
	"fiat_currency": "PHP",
	"amount": 5000,
	"price_per_unit": 370092.12,
	"payment_methods": [ "GCash", "Bank Transfer" ],
	"status": "online",
}
```
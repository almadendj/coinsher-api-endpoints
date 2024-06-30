### GET ``` /user/payment-methods ```
```js
Authorization: true

Returns: [
	{
		"id": "pm_gcash",
		"type": "E-Wallet",
		"details": {
			"name": "GCash",
			"phone_number": "09165980287",
			"account_name": "Dan Jeryll R. Almaden"
		},
		"verified": true,
		"created_at": "2024-07-02T14:30:00Z",
	},
	{
		"id": "bpi",
		"type": "Bank Transfer",
		"details": {
			"name": "BPI Bank Transfer",
			"account_number": "123123123",
			"account_name": "Dan Jeryll R. Almaden"
		},
		"verified": true,
		"created_at": "2024-07-02T14:30:00Z"
	},
	{
		"id": "paypal",
		"type": "PayPal",
		"details": {
			"username": "almadendj",
			"email": "almadendj@gmail.com"
		},
		"verified": false,
		"created_at": "2024-07-02T14:30:00Z"
	}
]
```
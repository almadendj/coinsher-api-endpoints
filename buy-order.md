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

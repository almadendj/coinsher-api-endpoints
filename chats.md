### POST ``` /chats/messages ```
```javascript
// DESCRIPTION: SEND MESSAGE
Params: {
	order_id: "order123",
	message: "Hello, have you received my payment?",
}

Returns: {
	"message_id": "msg123",
	"order_id": "order123",
	"sender_id": "sender123", // derived from JWT
	"receiver_id": "receiver123",
	"message": "Hello, have you received my payment?",
	"timestamp": "2024-07-02T14:30:00Z" 
}
```

### GET ``` /chats/conversations/{order_id} ```
```javascript
Params: {
	limit?: 10,
	offset?: 0, // pagination offset
}

Returns: [
	{
		"message_id": "msg123",
		"order_id": "order123",
		"sender_id": "sender123",
		"receiver_id": "receiver123",
		"message": "Hello, have you received my payment?",
		"timestamp": "2024-07-02T14:30:00Z" 
	},
	{
		"message_id": "msg123",
		"order_id": "order123",
		"sender_id": "sender123",
		"receiver_id": "receiver123",
		"message": "Hello, have you received my payment?",
		"timestamp": "2024-07-02T14:30:00Z" 
	}
]
```

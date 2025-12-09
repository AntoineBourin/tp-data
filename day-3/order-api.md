## API Orders

Domaines accessibles : `https://api.antoinebourin.com` ou `https://order-api-two.vercel.app`

- GET `https://order-api-two.vercel.app/api/orders`

- GET one order `https://order-api-two.vercel.app/api/orders/{id}`

- GET orders by productId `https://order-api-two.vercel.app/api/orders/product/{productId}`

- POST create one order `https://order-api-two.vercel.app/api/orders`

```
{
    "firstName": "Antoine",
    "lastName": "Bourin",
    "email": "antoine.bourin@outlook.com",
    "productId": "121"
}
```

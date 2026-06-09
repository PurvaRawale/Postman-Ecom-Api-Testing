## 🛒 Postman Ecom Api Testing

A hands-on API testing project where I tested a dummy ecommerce REST API using Postman. The project covers everything from logging in and grabbing a JWT token automatically, to fetching user profiles and product data — with test scripts validating each response.

---
## Why I Built This

I wanted to practice real-world API testing workflows not just sending requests, but also writing scripts that extract tokens, chain requests together, and assert response values automatically. This project helped me understand how QA engineers test APIs end to end.

---
## 🔗 API Used

DummyJSON — a free fake ecommerce REST API, perfect for testing.
Base URL: https://dummyjson.com

---

## Requests I Tested

1. Login API — POST /auth/login  
Sends username and password, gets back a JWT token. I wrote a script to save that token automatically in the environment.

2. Get User Profile — GET /auth/me  
Uses the saved token to fetch the logged-in user's details.

3. Get Products — GET /products  
Fetches all products. Also saves the first product's ID for the next request.

4. Get Single Product — GET /products/1  
Fetches one product using the ID saved from the previous request.

---

## Test Results

All 4 requests passed with status 200.

![Collection Runner](screenshot05_collection_runner.jpg)

| Request | Status | Test |
|---|---|---|
| Login API | 200 OK | ✅ Pass |
| Get User Profile | 200 OK | ✅ Pass |
| Get Products | 200 OK | ✅ Pass |
| Get Single Product | 200 OK | ✅ Pass |

Total: 4 passed, 0 failed, 0 errors

---

## Environment Variables

| Variable | Description |
|---|---|
| base_url | https://dummyjson.com |
| token | Auto-saved after login |
| productId | Auto-saved from products response |

---

## How to Use

1. Clone this repo
2. Open Postman
3. Import the collection file
4. Import the environment file
5. Select Env1 as active environment
6. Run Login API first — token saves automatically
7. Then run the rest or use Collection Runner

---

## Tools Used

Postman — API testing and automation

DummyJSON — Fake ecommerce REST API

JavaScript — Pre/Post request scripts

GitHub — Version control

---

## What I Learned

✅ Environment variables for reusable config
✅ JWT token auto-extraction via post-response scripts
✅ Bearer Token authorization
✅ Request chaining (Login → Profile → Products → Single Product)
✅ Automated assertions using pm.test() on all 4 requests
✅ Collection Runner for end-to-end execution

---
👩‍💻 Author
Purva Rawale
 

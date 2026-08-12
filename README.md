# API Testing Assignment — JSONPlaceholder

Functional API validation with **Postman** and basic performance/load testing with **Apache JMeter**, using the free [JSONPlaceholder](https://jsonplaceholder.typicode.com/) REST API.

## Overview

This project tests the JSONPlaceholder REST API using two tools:
- **Postman** — functional testing of GET, POST, PUT and DELETE requests with automated test scripts.
- **Apache JMeter** — a basic load test simulating multiple users hitting the API at once.

## Contents

| File | Purpose |
|------|---------|
| `JSONPlaceholder_API_Testing.postman_collection.json` | Postman collection with all 5 requests and automated tests |
| `JSONPlaceholder.postman_environment.json` | Postman environment holding the `base_url` variable |
| `JSONPlaceholder_Load_Test.jmx` | JMeter test plan (10 users, 5s ramp-up, 5 loops) |
| `screenshots/` | Postman and JMeter result screenshots |
| `README.md` | This file |

## API Endpoints Tested

Base URL: `https://jsonplaceholder.typicode.com`

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/posts` | Retrieve all posts (100 items) |
| GET | `/posts/1` | Retrieve a single post |
| POST | `/posts` | Create a new post |
| PUT | `/posts/1` | Update an existing post |
| DELETE | `/posts/1` | Delete a post |

## How to Run the Postman Tests

1. Install [Postman](https://www.postman.com/downloads/).
2. Click **Import** and add both `JSONPlaceholder_API_Testing.postman_collection.json` and `JSONPlaceholder.postman_environment.json`.
3. In the top-right dropdown, select the **JSONPlaceholder** environment.
4. Open any request and click **Send**, or use the **Collection Runner** to run all 5 requests at once.
5. Check the **Test Results** tab to see the automated tests pass.

Each request includes automated tests for:
- Status code validation
- Response time validation (under 2000 ms)
- Response structure validation
- Field and value validation (`id`, `title`, `body`, `userId`)

**Result:** 21 out of 21 tests passed with 0 failures.

## How to Run the JMeter Load Test

1. Install [Apache JMeter](https://jmeter.apache.org/download_jmeter.cgi) (requires Java).
2. Launch JMeter and open `JSONPlaceholder_Load_Test.jmx` via **File → Open**.
3. Click the green **Start** button to run the test.
4. View results in the **Summary Report** and **View Results Tree** listeners.

Test configuration:
- Number of Threads (users): **10**
- Ramp-Up Period: **5 seconds**
- Loop Count: **5**

**Results:** 100 samples, average response time 91 ms, throughput 1.7/sec, error rate 0.00%.

## Screenshots

Screenshots of both the Postman test results and the JMeter results are available in the `screenshots/` folder.

## Tools Used

- Postman
- Apache JMeter
- JSONPlaceholder (test API)

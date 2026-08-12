# Assignment No. 4 – API Testing

## Project
API testing of JSONPlaceholder using Postman for functional testing and Apache JMeter for basic load testing.

## Tools
- Postman
- Apache JMeter
- JSONPlaceholder REST API

## Postman Collection
The collection contains:
1. GET - All Posts
2. GET - Single Post
3. POST - Create Post
4. PUT - Update Post
5. DELETE - Delete Post

### Automated validations
The Postman tests validate:
- HTTP status codes
- Response time (< 2000 ms)
- Response structure
- Required fields: id, title, body, userId
- Expected values for GET/POST/PUT requests

### How to run
1. Import `JSONPlaceholder_API_Testing.postman_collection.json` into Postman.
2. Import `JSONPlaceholder.postman_environment.json` if you want to use the environment.
3. Select the environment if imported.
4. Open the collection and run all requests.
5. Open the Postman Test Results/Test Results area and take screenshots showing passed tests.
6. Export the collection again if your instructor requires the exported collection from your own Postman workspace.

## JMeter Load Test
Configuration:
- Threads/Users: 10
- Ramp-Up Period: 5 seconds
- Loop Count: 5
- Total requests: 50
- Endpoint: GET https://jsonplaceholder.typicode.com/posts/1
- Listeners: View Results Tree and Summary Report

### How to run
1. Install Apache JMeter.
2. Open `JSONPlaceholder_Load_Test.jmx`.
3. Run the test using the green Start button.
4. Open Summary Report.
5. Record:
   - Average response time
   - Min/Max response time
   - Throughput
   - Error %
6. Take a screenshot of the Summary Report and View Results Tree for submission.

GitHub file structure
assignment-4-api-testing/
├── JSONPlaceholder_API_Testing.postman_collection.json
├── JSONPlaceholder.postman_environment.json
├── JSONPlaceholder_Load_Test.jmx
├── README.md
└── screenshots/
    ├── postman_get_tests.png
    ├── postman_post_put_delete.png
    ├── jmeter_summary.png
    └── jmeter_results_tree.png


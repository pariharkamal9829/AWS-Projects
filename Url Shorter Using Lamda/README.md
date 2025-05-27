🔗 Serverless URL Shortener (AWS Lambda + API Gateway + DynamoDB)
This project demonstrates how to build a serverless URL shortener using AWS Lambda, API Gateway, and DynamoDB. It's designed to be beginner-friendly and includes step-by-step instructions specifically tailored for Windows users.

🚀 Features
🔐 Generate short codes for long URLs

🔁 Redirect users to the original URL using the short code

☁️ Fully serverless and scalable

🧰 Prerequisites
Ensure you have the following before starting:

✅ AWS Account — Sign up for AWS Free Tier

✅ AWS CLI — Download AWS CLI for Windows

sh
Copy
Edit
aws configure
Enter your Access Key, Secret Key, region, and output format.

✅ Python 3.x — Download Python

During installation, make sure to check "Add Python to PATH"

✅ Postman (optional) — Download Postman for testing the API

📘 Step-by-Step Guide
🔹 Step 1: Set Up DynamoDB Table
Go to AWS Console → DynamoDB

Click Create Table

Table name: URLShortener

Partition key: short_code (String)

Click Create

🔹 Step 2: Create the Lambda Function
Go to AWS Console → Lambda

Click Create Function

Name: URLShortenerFunction

Runtime: Python 3.x

Permissions: Create a new role with basic Lambda permissions

Click Create Function

🔹 Step 3: Add Code to Lambda
In the Lambda editor, replace the default code with the code in lambda_function.py

Click Deploy

🔹 Step 4: Set Up API Gateway
Go to AWS Console → API Gateway

Click Create API → Choose HTTP API → Click Build

Add Routes:

POST /shorten — to shorten URLs

GET /redirect — to redirect using the short code

Integrate each route with the URLShortenerFunction

Click Deploy

Create a stage (e.g., prod)

Note the API endpoint URL
Example: https://<api-id>.execute-api.<region>.amazonaws.com/prod

🧪 Step 5: Test the URL Shortener
🔸 Using Postman
Create a Short URL

Set method to POST

URL:

php-template
Copy
Edit
https://<api-id>.execute-api.<region>.amazonaws.com/prod/shorten
Go to Body → Select raw → Choose JSON → Add:

json
Copy
Edit
{
  "long_url": "https://www.example.com"
}
Click Send → You should receive a response with a short_code

Redirect to Original URL

Set method to GET

URL:

php-template
Copy
Edit
https://<api-id>.execute-api.<region>.amazonaws.com/prod/redirect?short_code=<short_code>
Click Send → You should be redirected

🔸 Using Command Prompt or PowerShell
Create a Short URL

powershell
Copy
Edit
Invoke-RestMethod -Uri "https://<api-id>.execute-api.<region>.amazonaws.com/prod/shorten" `
 -Method Post `
 -ContentType "application/json" `
 -Body '{"long_url": "https://www.example.com"}'
Redirect to Original URL

powershell
Copy
Edit
Invoke-RestMethod -Uri "https://<api-id>.execute-api.<region>.amazonaws.com/prod/redirect?short_code=<short_code>"
🧹 Step 6: Clean Up Resources
To avoid charges:

🗑️ Delete the DynamoDB table

🗑️ Delete the Lambda function

🗑️ Delete the API Gateway

🤝 Contributing
We welcome contributions! You can:

🚀 Add new features or improve existing ones

📘 Write documentation or tutorials

🐞 Fix bugs or optimize the code

Open an issue or submit a pull request to get started.

💬 Support
If you have questions or encounter any issues, feel free to open an issue.
We’ll be happy to help or accept corrections and suggestions!


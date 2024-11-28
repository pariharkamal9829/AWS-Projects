<div align="center">
  <h1 style="font-size: 36px; color: #2F855A; font-weight: bold;">Hosting a Static Website on AWS S3</h1>
  <p style="font-size: 18px; color: #555;">Welcome to the guide on hosting a static website using AWS S3. This README provides a step-by-step walkthrough for setting up and deploying a static website on AWS S3 with ease.</p>
</div>

---

## Table of Contents
1. [Introduction](#introduction)
2. [Step-by-Step Guide](#step-by-step-guide)
3. [Common Errors and Solutions](#common-errors-and-solutions)
4. [Conclusion](#conclusion)
5. [Contact Information](#contact-information)

---

## <span style="color: #2F855A; font-weight: bold;">Introduction</span>
Amazon S3 (Simple Storage Service) is a powerful and cost-effective solution for hosting static websites. By utilizing S3, you can host websites comprising HTML, CSS, JavaScript, and other static files without the need for a dedicated web server.  

With AWS's Free Tier, you can even enjoy 5GB of free storage for a year, making it an excellent choice for small websites and personal projects.

---

## <span style="color: #2F855A; font-weight: bold;">Step-by-Step Guide</span>
Follow these steps to host your static website:

### 1. **Access AWS Console**
   - Log in to your [AWS Management Console](https://aws.amazon.com/console/).
   - Search for **S3** in the search bar and select **S3**.

### 2. **Create a Bucket**
   - Click on **Create Bucket**.
   - Enter a globally unique **Bucket Name**.
   - Choose an appropriate AWS Region based on your needs (latency, compliance, or cost).
   - Adjust bucket settings as needed and click **Create Bucket**.

### 3. **Configure Bucket Settings**
   - In the bucket's **Permissions** tab, uncheck **Block all public access** to allow public access for your website.
   - Add a **Bucket Policy** under **Permissions** to enable access to the files:
     ```json
     {
       "Version": "2012-10-17",
       "Statement": [
         {
           "Sid": "PublicReadGetObject",
           "Effect": "Allow",
           "Principal": "*",
           "Action": "s3:GetObject",
           "Resource": "arn:aws:s3:::your-bucket-name/*"
         }
       ]
     }
     ```

### 4. **Enable Static Website Hosting**
   - Navigate to the **Properties** tab.
   - Enable **Static Website Hosting** and select **Host a static website**.
   - Specify your `index.html` as the Index Document and `error.html` as the Error Document (optional).

### 5. **Upload Website Files**
   - Upload your `index.html` and other files (e.g., CSS, images) using the **Upload** button in the S3 console.
   - Ensure the files are public by modifying their permissions.

### 6. **Access Your Website**
   - Navigate to the **Properties** tab to find the bucket's static website endpoint URL.
   - Open the URL in a browser to view your hosted website.

---

## <span style="color: #2F855A; font-weight: bold;">Common Errors and Solutions</span>
### Error: "Access Denied"
   - Ensure the **Bucket Policy** grants public access.
   - Check that the files have appropriate permissions for public read access.

### Error: "Website Not Loading"
   - Verify that the `index.html` file exists and is specified correctly in the Static Website Hosting configuration.
   - Double-check the bucket endpoint URL.

---

## <span style="color: #2F855A; font-weight: bold;">Conclusion</span>
Hosting a static website on AWS S3 is a straightforward process that offers scalability, reliability, and cost-effectiveness. By following the steps outlined above, you can deploy your website with minimal effort and take advantage of AWS's robust infrastructure.

---

## <span style="color: #2F855A; font-weight: bold;">Contact Information</span>
For further assistance or collaboration, feel free to reach out:  

**LinkedIn:** [Kamlesh Parihar's LinkedIn](https://www.linkedin.com/in/kamlesh-parihar/)  
**Email:** [kamlesh@example.com](mailto:kamlesh@example.com)

---

<div align="center">
  <p style="font-size: 16px; color: #555;">Thank you for following this guide. I hope it helps you host your website seamlessly using AWS S3!</p>
  <strong>Author:</strong> Kamlesh Parihar
</div>

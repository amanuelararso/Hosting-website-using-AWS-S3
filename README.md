# Hosting Website Using AWS S3

## Project Overview

The "Hosting Website Using AWS S3" project is a simple yet effective solution to host a website on the Amazon Web Services (AWS) platform using an S3 (Simple Storage Service) bucket. In this project, I have leveraged AWS S3 to host a website that serves as your personal resume. This README provides a brief overview of the project and instructions for setting up your own website hosting using AWS S3.

## Features

- **Website Hosting:** Host your personal website (resume) on AWS S3, making it accessible via a public URL.

- **S3 Bucket Configuration:** Properly configure the S3 bucket to serve static website content securely.
- **Route 53:** Create a record of type A, NS, SOA and CNAME
- **Certificate Manager:** Create an SSL certificate for the website
- **CloudFront:** Create distribution 

## Prerequisites

Before you begin, make sure you have the following prerequisites:

- An AWS account with appropriate permissions to create and configure S3 buckets.
- Your website content, such as HTML, CSS, and other assets, is ready for hosting.
- Bought domain name like example.com
- Basic knowledge of AWS services and using the AWS Management Console.

## Project Setup

Follow these steps to set up your website hosting using AWS S3:

1. **Create an S3 Bucket:**

   - Log in to your AWS Management Console.
   - Navigate to the S3 service.
   - Create a new S3 bucket and choose a globally unique name for it.
   - Make sure the bucket is configured to allow public access.

2. **Upload Website Content:**

   - Upload your website files (HTML, CSS, images, etc.) to the S3 bucket.
   - Make sure to set the appropriate permissions to make the files public.

3. **Enable Website Hosting:**

   - In the S3 bucket properties, go to the "Static website hosting" section.
   - Select 'enable'
   - Specify the index document (e.g., `index.html`) and error document if applicable.

4. **Set Up Permissions:**

   - Update the bucket policy to grant public read access to the objects in your bucket.

5. **Access Your Website:**

   - Once your website is hosted, you can access it using the provided S3 bucket's endpoint URL.

## Example

Your website should now be accessible via a URL that follows this pattern:

```
http://your-bucket-name.s3-website-your-region.amazonaws.com
```

Replace `your-bucket-name` with the name of your S3 bucket and `your-region` with the AWS region where your bucket is hosted.

Mine is http://staticwebbucket89.s3-website-us-west-2.amazonaws.com

**Domain and SSL Certificate Configuration**

1. Configure DNS (Route 53):
        Create a hosted zone with the name of your domain, e.g., amanuelararso.me, and set the type to "public hosted zone."
        After the zone is created, NS (Name Server) and SOA (Start of Authority) records will appear by default.
        If your domain is not bought from Route 53, add the four nameservers shown in the NS records to the "Manage Nameservers" section of your domain's DNS settings.

2. SSL Certificate (Certificate Manager):
        Go to AWS Certificate Manager.
        Click on "Request a certificate," then select "Request a public certificate."
        Input your domain name and leave all other settings as default.
        Wait for a minute for the certificate to be issued.

3. Add SSL Certificate to Route 53:
        Click on the certificate ID in AWS Certificate Manager.
        Click on "Create records in Route 53."
        You will see that a third record is added under your previously created hosted zone.

**Amazon CloudFront Configuration**
To Create a Distribution:
1. Go to Amazon CloudFront.
2. Create a new distribution.
3. Paste the S3 website endpoint into the "Origin Domain" section, e.g., 'staticwebbucket89.s3-website-us-west-2.amazonaws.com'. Be careful not to enter the S3 address like staticwebbucket89.s3.us-west-2.amazonaws.com; it won't work with this.
4. Set the Viewer Protocol Policy to "Redirect HTTP to HTTPS."
5. Do not enable WAF (Web Application Firewall).
6. Choose the custom SSL certificate from the dropdown.
7. Leave anything else as default and click "Create Distribution."

## EXAMPLE 
Your website should be live by now. My website is:
```
https://amanuelararso.me
```

## Contributing

Contributions to this project are welcome! If you have improvements, suggestions, or bug fixes, feel free to open an issue or create a pull request.

## License

This project is open-source and available under the MIT License.

## Support

If you encounter any issues, have questions, or need assistance with hosting your website on AWS S3, please reach out for help.

Happy hosting! 🚀

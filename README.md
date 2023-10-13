# Hosting Website Using AWS S3

## Project Overview

The "Hosting Website Using AWS S3" project is a simple yet effective solution to host a website on the Amazon Web Services (AWS) platform using an S3 (Simple Storage Service) bucket. In this project, we have leveraged AWS S3 to host a website that serves as your personal resume. This README provides a brief overview of the project and instructions for setting up your own website hosting using AWS S3.

## Features

- **Website Hosting:** Host your personal website (resume) on AWS S3, making it accessible via a public URL.

- **S3 Bucket Configuration:** Properly configure the S3 bucket to serve static website content securely.

## Prerequisites

Before you begin, make sure you have the following prerequisites:

- An AWS account with appropriate permissions to create and configure S3 buckets.
- Your website content, such as HTML, CSS, and other assets, ready for hosting.
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

## Contributing

Contributions to this project are welcome! If you have improvements, suggestions, or bug fixes, feel free to open an issue or create a pull request.

## License

This project is open-source and available under the MIT License.

## Support

If you encounter any issues, have questions, or need assistance with hosting your website on AWS S3, please reach out for help.

Happy hosting! 🚀

# Project: XML File Handling with AWS Glue and AWS Lambda

This project involves setting up a pipeline to handle XML files from an S3 bucket, including validation, dynamic schema handling, data filtering, and monitoring with AWS Lambda and Glue.

## Steps

### XML File Handling
- **Pipeline reads XML files** from a specified S3 bucket.
- Each XML file will be **validated against its corresponding XSD schema** to ensure data integrity.

### Dynamic Schema Handling
- The XML files may have **nested data structures**, requiring the pipeline to handle dynamic schemas effectively.

### Data Filtering
- **Check for required columns**: `Company_id` and `revenue`.
- **Exclude records where `revenue` is 0**.
- **Ensure that `Company_id` is not null**.

### Output
- Write the filtered DataFrame to S3 in **Parquet format**.

### AWS Lambda Monitoring
- Implement an **AWS Lambda function** to monitor the specified S3 bucket for new XML file uploads.
- When a new XML file is detected, the Lambda function will **trigger an AWS Glue job**.

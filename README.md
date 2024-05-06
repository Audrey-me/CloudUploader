# CloudUploader
A bash-based CLI tool that allows users to quickly upload files to a specified cloud storage solution, providing a simple and seamless upload experience similar to popular storage services.

### Steps to Take
1. Clone the repo
2. Ensure you have AWS CLI installed
3. Create an AWS IAM User and set permissions to allow S3 access
4. run "chmod 744 ./clouduploader"  to be able to access the script
5. run "./clouduploader" to run the script
6. install "pv" to enable the display of the progress of your upload. eg for Mac users use (brew install pv)


### Explaining the Script
1. a generic " display_text_duration " function that displays a message when a process is running in the background, just to let the user know what is actually running and to exercise a little patience.

2. The "check_user" function checks if the IAM user has been configured correctly and if it has the necessary permissions needed to execute the later commands.

3. The "check_bucket" function checks if the provided bucket name is not empty and it is in line with the AWS Bucket naming convention and then throws an error if not validated true. else a new bucket is created successfully.

4. Then the "file_upload" function lists out existing buckets you have and prompts you to specify the particular bucket you want to upload your files to. and in cases when you want to upload the file to an entirely new bucket, the "check_bucket" function runs.
Then you can successfully upload your files to the specified S3 bucket

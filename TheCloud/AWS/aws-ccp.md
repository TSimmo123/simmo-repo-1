# AWS Certified Cloud Practitioner

Here you will find a lot of key information that will help you when studying for the Amazon Certified Cloud Practitioner Exam.

You can also visit [here](https://github.com/TSimmo123/simmo-repo-1/blob/main/TheCloud/AWS/aws-service-dictionary.md) to view the AWS Service Directory.

Firstly, it is important to note that the fundamentals of cloud architecture will be on the exam, so I would suggest reading the information on the previous page so that you are fully up to grips with `The Cloud`.

## AWS Support

AWS have a tool called `AWS Trusted Advisor` that us used for checking your AWS usage against best practices. The AWS Trusted Advisor provides recommendations in the following 5 categories:
- Cost Optimisation
- Performance
- Security
- Fault Tolerance
- Service Limits

AWS has 4 different support plans available to consumers:
- Basic (Free)
- Developer (29$ a month min.)
- Business (100$ a month min.)
- Enterprise ($15,000 a month min.)

The below diagram shows what you can expect from each plan.

![commit](../../images/aws-support-plan.jpg)

## How to Generate an Access Key
In order to use the AWS CLI (Command Line Interface), you need to generate an access key. This is done by:
1. Log into the AWS console
2. Select your username in the top bar, and select My Security Credentials in the dropdown menu.
3. Next, select the access key options
4. Select the option to Create New Access Key (if this is a root account, you should delete these when you are done with them)
5. Download your key file
6. Install the CLI based on the installation instructions
7. Run AWS configure and pass in the access key and secret key that you just created

You should now be able to leverage the AWS CLI at this point.

## Amazon EC2 Overview

The four concepts that we need to know to launch an EC" instance are:
- Instance types
- Root device type
- Amazon Machine Image (AMI)
- Purcahse Options

The `Instance Type` defines the processor, memory, and storage type available to any server that is launched with that instance type.

The two root device types for an EC2 instance are:
- Instance Store
- Elastic Block Store (EBS) - more favourable

Amazon EC2 Purchase Options:
- On-Demand - You pay for the second for the instance that are launched
- Reserved Instances - You purchase at a discount instances in adavnce for 1-3 years
- Spot - You can leverage unused EC2 capacity in a region for a large discount

Reserved Instances Cost Models:
- All up-front
- Partial up-front
- No upfront

## Launching EC2 Instances

Below is a step-by-step guide on how to Launch an EC2 instance
1. Log into the AWS Console.
2. Open the EC2 service dashboard (search for EC2 in the ‘Find Services’ input).
3. Select the Launch Instance option.
4. Select the Amazon Linux 2 AMI.
5. Be sure that the t2.micro instance type is selected (it should be selected by default).
Select the Next button.
6. Set the Auto-assign Public IP option to Enable.
7. Scroll down to Advanced Details and open these settings. In the User data field, enter
the text included below these instructions. Select the Next button.
8. Leave the storage settings with their default values. Select the Next button.
9. Add tags if you would like. Select the Next button.
10. In the Configure Security Group settings view, change the Source for the SSH type to
be My IP Address.
11. Next, select the Add Rule button. In the new role, set the type to be HTTP. Select the
Next button.
12. Next, select Launch.
13. Create a keypair (if you don’t have one) and then select Launch Instance.
14. Next, select the ID of the server that you just launched.
15. Once the instance has transitioned from pending to running, copy the public DNS into
your browser. You should see the test page in your browser.
16. Finally, back in the AWS console select the instance and then navigate to Actions.
Select Instance State - Terminate. Confirm your decision.


## Launching an App on Elastic Beanstalk

Firstly, why would we use Elastic Beanstalk?
- Deploy an application with minial knowledge of other services
- Reduce the overall maintenance needed for the application
- Few customisations are needed

Below is a step-by-step guide on how to Launch an app on Elastic Beanstalk
1. Navigate to the Elastic Beanstalk Tutorials and Samples page. Select a sample
application to download to your local machine.
2. Log into the AWS console and navigate to the Elastic Beanstalk service page.
3. If you see the “Welcome to AWS Elastic Beanstalk” screen, select Get Started.
4. In the screen that follows, give your application a name and select the platform (it will
need to be the same platform as the sample application you downloaded.
5. Select the option to upload your code, and then upload the zip file you downloaded
that contains your sample application.
6. Select the option to Configure More Options.
7. Next, review the settings for this environment. Select Create app.
8. Wait for the application and then navigate to the URL near the top of the page.
9. After viewing the application, navigate back to the console and select Actions -
Terminate Environment.

## Why use the AWS Global Accelerator

The AWS Global Accelerator is a newtoking service that can route your traffic through the AWS global network infrastructure to improve performance.

It utilises IP addresses that route to edge locations. Once the request reaces edge locations, traffic is routed through AWS network. It can route requests to many AWS resources including load balancers and EC2 instances.

Using it has the following performance improvements:
- Distance between user and initial endpoint is minimised by using edge locations
- Traffic is optimised by using AWS network instead of public internet
- Results in improvement of first byte latency, jitter, and throughput
- Provides superior fualt tolerance by not relying on DNS resolution

## Hosting a Website on Amazon S3

1. Log into the AWS Console, and select the S3 service.
2. Click the Create Bucket button.
3. In the dialog, give the bucket a unique name and click Next.
4. In the next view, you can simply click Next.
5. Deselect the option to Block all Public Access. Once the warning appears you will need
to click the checkbox in the acknowledgement. Click Next.
6. In the Review view, you can click the Create Bucket button.
7. Next, click on the newly created bucket in the list.
8. Next, click the Upload button. From the dialog, click the Add Files button.
9. Select the files from the exercise files. Click Next.
10. From the Permissions view, you can click Next.
11. In the properties view, leave the default storage class. Scroll down and set encryption to
the Amazon S3 Master Key. Click Next.
12. From the Review view, click Upload.
13. Select the ps-logo.jpg file from the list. Attempt to navigate to the Object URL for this
image.
14. Navigate back to the console and click on the image in the list. Click the permissions
option to edit the permissions.
15. Scroll down to the section titled Public Access and select the Everyone group.
16. Be sure that Read object option is selected in the dialog. Click Save.
17. Reload the image URL, and it should load without issue.
18. Back in the console, navigate to the bucket and then select the Properties tab.
19. From the properties tab, select Static Website Hosting.
20. Next, select the option to Use this bucket to host a website. Enter index.html for the
index document, Click Save.
21. Navigate to the URL for the static website hosting option. You will see that it is
forbidden.
22. Next, navigate back to the console and select the index.html file. Update the
permissions just as you did for the image.
23. Next, navigate back to the static website hosting URL. The site should now work.

## Glacier and Glacier Deep Archive

Both S3Glacier and Glacier Deep Archive are designed for archival of data within S3 as a separate storage class.

|`S3 Glacier`|`S3 Glacier Deep Archive`|
|--|--|
|Designed for archival data|Designed for archival data|
|90 day minimum storage duration change|180 day minimum storage duration change|
|Can be retrieved in either minutes or hours|Can be retrieved in hours|
|You pay a fee for GB retrieved in addition to the storage costs|You pay a retrieval fee per GB retrieved|
|Over 5 times less expensive han S3 Standard Storage Class|Over 23 times less expensive than S3 standard storage class|




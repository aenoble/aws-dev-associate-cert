# "AWS Certified Developer -- Associate" Study Notes

Target Date: April 15, 2019
Exam Guide: [Found Here](AWS_Certified_Developer_Associate_Updated_June_2018_Exam_Guide_v1.3.pdf)

Prereqs: Your own AWS account, credit card.

Note: Setup billing alarm in case you go over

## Regions
* Tied to a physical area in the world (e.g. us-east-1)
* Regions have many availabilty zones, all designated by the region's shortform id and ending in a letter (e.g. us-east-1a)
* Availability zones are physical data centers in the region, but isolated from others.
* Not all services are scoped by region (e.g. IAM, S3)

## IAM (Identity and Access Management)
* Responsible for assigning security permissions.
    * Users
    * Groups
    * Roles
* Root accounts (one that registered for AWS to begin with) should never be used after creation.
* Every AWS service uses IAM
* Policies (granting permissions to Users/Groups/Roles/etc) are written in JSON.
* has predefined "managed policies".
* Least Privilege Principle - it's best to give users the minimal amount of permissions to perform their job
    * Don't grant permissions that aren't necessary.
* Never write IAM creds in code, ever.
* Never commit IAM creds, ever.
* Never use root IAM creds

### Users
* A person
* Only have one User per physical person.

### Groups
* A collection of users with the same sets of permissions.

### Roles
* AWS Resources (i.e. non-human) assigned with the same set of allowed functions (e.g. EC2 instance(s) allowed to perform some task).
* Only have one IAM Role per application.

### IAM Federation
* Used to integrate third party system / repository of users to integrate with AWS.
    * e.g. integrating Active Directory with AWS and IAM
* User can login into AWS using their company credentials.
* Used mainly in larger companies (?)
* Identity federation uses SAML.

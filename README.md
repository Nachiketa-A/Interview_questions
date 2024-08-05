# Interview_questions

#### What methods do you use to check for code vulnerabilities?

Ans: When checking for code vulnerabilities, you can use several methods to make sure the code is safe and secure.

     1.Code Reviews: Have other experienced developers look at your code. They might spot problems you missed.

     2.Static Code Analysis: Use tools that automatically check your code for common issues and bad practices without running the program. These tools analyze the code's 
       structure and syntax.

     3.Dynamic Analysis: Test your code while it’s running to find vulnerabilities. This can include things like checking how the code behaves with different inputs to see if 
       it does anything unexpected.

     4.Penetration Testing (Pen Testing): Simulate attacks on your software to find security weaknesses. This helps you see how an attacker might exploit your system.

     5.Dependency Scanning: Check the libraries and modules your code uses to make sure they don’t have known vulnerabilities. This is important because you rely on other 
       people's code when you use libraries.

#### How would you access data in an S3 bucket from Account A when your application is running on an EC2 instance in Account B?

ANS: To access data in an S3 bucket from Account A when your application is running on an EC2 instance in Account B, you can follow these steps:

     1. Create an IAM Role in Account B:

        In Account B, create an IAM role that allows the EC2 instance to access S3 buckets.

        Attach a policy to this role that gives permissions to access the specific S3 bucket in Account A.

     2.Set Up Trust Relationship:

       In Account A, update the bucket policy to allow access from the IAM role created in Account B.

       The bucket policy should include the AWS Account ID of Account B and the specific IAM role.

     3.Attach the IAM Role to the EC2 Instance:

       In Account B, attach the IAM role to the EC2 instance running your application. This gives the EC2 instance the permissions specified in the role.
 
     4.Configure the Application:

      In your application running on the EC2 instance, use AWS SDKs or CLI to access the S3 bucket. The application will use the permissions of the attached IAM role to 
      access the bucket in Account A.


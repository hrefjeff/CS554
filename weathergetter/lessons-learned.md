## Lessons Learned

In the beginning we provisioned AWS Elastic Compute Cloud (EC2 for short).

This IAAS allows users to rent virtual computers on which to run their own computer applications.

The instances we spun up were linux-based that had web servers installed serving static PHP content.

During our research, we found another AWS service that provided the same functionality we were looking to achieve, but in a cheaper and easier manner.



Enter AWS Lambda! This is an event-driven, serverless computing platform provided by Amazon as a part of Amazon Web Services that was introduced in 2014.

It is a computing service that runs code in response to events and automatically manages the computing resources required by that code.

Since our SOA operates serverless we removed the need for EC2 instances.

The result was that we were able to save money and time because of how we only needed to deploy a single python script versus maintaining an entire operating system.

## Difficulties experienced

Python versioning. Unable to make requests with the latest 3.9 that was available, had to go to 3.7.

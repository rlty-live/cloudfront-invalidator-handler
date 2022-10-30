# CloudFront Invalidator (for CodePipeline)
### Overview
This is an AWS Lambda function to be triggered by CodePipeline in a Lambda Node environment. It is deployable using AWS SAM CLI.

This Lambda function creates a CloudFront Invalidation so that your distibution is updated with the latest objects the next time those edge location's objects are requested again.

This code does _not_ report the actual status of the invalidation back to CodePipeline. It is assumed that CloudFront will handle invalidation properly after it receives the request.


# BlogLoom
Blog generator - Under development
## Steps
- In AWS Bedrock access all models. Create a lambda function in AWS Lambda.
- Edit the timeout(3 min and 0 sec) in configuration tab.
- write the code app.py to make a lambda handler.
- copy paste the code in aws lambda code tab and deploy it.
- Install boto3 package in boto3_layer folder using "pip install boto3 -t python/". Compress it in zip format.
- Create layers(packages/libraries used in projects) upload the zip file while creating. select the runtimes as well.
- Add the layer in lambda function. Now, we need to add a trigger.
- Go to API Gateway service and create an api(HTTP API). Create routes(POST and endpoint "\blog_generation") and Deploy it.
- Attach an Integration to lambda function. 
- create stages for testing and development and deploy it. Copy invoke url and attach route next to the url.
- Create s3 bucket with same name in lambda handler.
- Go to lambda function and in permissions tab under configuration tab click on role name link. Add the admin access in attach policies.
- Test the api gateway link in postman with post method(body and raw).
- Check CloudWatch, s3 for output. 

Note : Don't forget to delete the services created as they may incur costs.
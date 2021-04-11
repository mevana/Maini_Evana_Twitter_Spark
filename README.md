<<<<<<< Updated upstream
# Project Goal

The project intends to layout the differences between setting up and querying MySQL vs Spark using the Twitter dataset that we have used in class. We will also use AWS RDS and EMR to accomplish the assignment. 
=======
# Maini_Evana_Twitter_Spark
## Project Goal
The goal of this project is to migrate the Twitter dataset into AWS and use S

Performing this step each day at a predetermined time: 
Lambda (15 mins max) or EC2 instance that will have Python script to follow users based on our interested that we define (for example, follow users if their tweets mention 'Machine Learning', 'coding', etc). This will be automated to happen every day, at a fixed time (we can use EC2 scheduled spot instances for this or lambda (depending on how long we expect this process to take)). We can use 'Python-Twitter' library to access Twitter API and easily follow users. 
Then, we get the user data and save it to either mySQL database (AWS RDS) or straight to S3. 

After a few weeks of collecting this data: 
Use AWS Glue to connect the AWS components
- AWS RDS or S3 (via AWS Glue) ->  sagemaker for training [https://docs.aws.amazon.com/machine-learning/latest/dg/using-amazon-rds-with-amazon-ml.html]
- trained model -> run predictions on todays new requests. Report back the following from the model via SQS service (send email or text to us) with the twitter followers we followed today and the likelihood that they will follow us back. 

The pipeline will be VERY similar to this: 
[https://aws.amazon.com/blogs/machine-learning/moving-from-notebooks-to-automated-ml-pipelines-using-amazon-sagemaker-and-aws-glue/]

>>>>>>> Stashed changes

# Dining Concierge AI Agent

## About

A Dining Recommendation Chatbot deployed using AWS. [Website url](http://dining.ai.agent.s3-website-us-east-1.amazonaws.com/)

## Author
Chi Wu, Wanqi Wu

## Services

![image](https://user-images.githubusercontent.com/43989412/136854235-2a53af0f-ab25-4a1e-8a64-5f8fab229839.png)


1. Front-end is hosted using S3 bucket
2. API-gateway used for channeling back-end lambda functions
3. AWS LEX used to build and train the dining bot
4. Yelp APIs called to collect random restaurants from Manhattan area
5. DynamoDB used to store restaurant information
6. Opensearch Service instance created for indexing
7. Lambda Functions
	* LF0: used to call and send user utterances to AWS LEX service, and return LEX response to the user
   * LF1: used to extract useful fields as well as validate the user utterances, send data to SQS
   * LF2: used to retrieve recommendated restaurants information from Opensearch and DynamoDB, send data to SNS
8. SMS used to send recommendation results to users

## Example Message

<img src="https://user-images.githubusercontent.com/43989412/136856523-27be0a60-d70c-4eef-8718-b902248abbd7.jpg" alt="drawing" width="250"/>

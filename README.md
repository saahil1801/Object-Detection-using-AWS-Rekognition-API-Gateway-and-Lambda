# Object Detection using AWS Rekognition API Gateway Lambda

This repository provides a simple implementation of object detection from an image using AWS Rekognition, API Gateway, and Lambda functions. The Lambda function is triggered by API Gateway when an image is sent through a POST request. The API can be tested using Postman.

## Overview of Architecture with a Use Case Explanation

The architecture involves the following components:

1. **AWS Lambda Function:** Receives image data from API Gateway, decodes it, and performs object detection using the AWS Rekognition service.

2. **AWS Rekognition Service:** Used for detecting labels in the image.

3. **API Gateway:** Serves as the interface for external applications to interact with the Lambda function. It triggers the Lambda function when a POST request with an image is received.

### Use Case Explanation

The use case for this implementation is to detect objects in an image. The Lambda function receives the image through API Gateway, processes it using AWS Rekognition, and returns information about the detected objects along with their confidence levels.

## Creation of Lambda Function and In-Depth Code Explanation

The Lambda function is responsible for decoding the base64-encoded image data, converting it to the required format, and utilizing the AWS Rekognition service to perform object detection. The extracted information about the detected objects is then returned in the API response.

## Lambda Layer Creation

A Lambda Layer is utilized to include external libraries, such as `PIL` (Pillow), required for image processing. This ensures a clean and organized code structure.

## API Gateway Setup and Configuration of Lambda Integration

API Gateway is configured to trigger the Lambda function when a POST request is received. The integration allows seamless communication between the external application and the Lambda function.

## Deployment of the API

The API is deployed, making it accessible for external applications to send images for object detection.

## Testing of the Deployed API using Postman

Postman can be used to test the deployed API by sending a POST request with a binary image in the request body. The API response includes information about the detected objects and their confidence levels.

## ScreenShots

![Screenshot 2024-01-09 131407](https://github.com/saahil1801/Object-Detection-using-AWS-Rekognition-API-Gateway-and-Lambda/assets/84408557/48e4b644-7ef1-4f04-a1df-96b391f90391)
![Screenshot 2024-01-09 131426](https://github.com/saahil1801/Object-Detection-using-AWS-Rekognition-API-Gateway-and-Lambda/assets/84408557/7c02b0b1-2f56-417a-9c43-b3dd4ed6f353)
![Screenshot 2024-01-09 131155](https://github.com/saahil1801/Object-Detection-using-AWS-Rekognition-API-Gateway-and-Lambda/assets/84408557/115fc06c-6f2b-431c-a979-3116ce1f8e56)
![Screenshot 2024-01-09 131217](https://github.com/saahil1801/Object-Detection-using-AWS-Rekognition-API-Gateway-and-Lambda/assets/84408557/0cddfbbc-b8a9-4270-9ee2-3296d3acf0ca)
![Screenshot 2024-01-09 131238](https://github.com/saahil1801/Object-Detection-using-AWS-Rekognition-API-Gateway-and-Lambda/assets/84408557/465b21ef-ccec-416c-8543-9a2c5fcad238)
![Screenshot 2024-01-09 131313](https://github.com/saahil1801/Object-Detection-using-AWS-Rekognition-API-Gateway-and-Lambda/assets/84408557/f2d873a4-889d-447d-b496-06b3d22d04d8)
![Screenshot 2024-01-09 131342](https://github.com/saahil1801/Object-Detection-using-AWS-Rekognition-API-Gateway-and-Lambda/assets/84408557/2022e22e-ab91-4a25-837c-91071911ad9b)


## License

This project is licensed under the [MIT License](LICENSE).

Feel free to contribute, open issues, or provide feedback!

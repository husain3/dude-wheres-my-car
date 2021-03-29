# dude-wheres-my-car

This project contains source code and supporting files for an AWS Step Function that runs AWS Fargate Tasks for object detection machine learning using computer vision. Ultimately, it will be used to detect if an automobile is available in the home garage. The Faster R-CNN algorithm from keras-frcnn is used for object detection learning.

It includes the following files and folders:

```
DUDE-WHERES-MY-CAR
|---CarDetectionLearning
|   └---main.py                         - Code for the task's ML procedure
|   └---requirements.txt                - Pip requirements installed during container build.
|   └---Dockerfile                      - Contains the commands needed to build docker container
|---pipeline
|   └---pipeline.yaml                   - CI/CD pipeline
|---StateMachine
|   └---WheresMyCarLearning.asl.json    - ASL specification for step function
|---README.md                           - This README file
└---template.yaml                       - Template that defines the AWS resources.
```

The application uses several AWS resources, including an API Gateway API, an ECS Cluster, ECS Tasks, and a Step Function. These resources are defined in the `template.yaml` file in this project. You can update the template to add AWS resources through the same deployment process that updates your application code.

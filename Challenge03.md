# Challenge 3 - A Run in the Clouds

## Background

It's not just enough to be able to build a world class machine learning model, you need to know how to deploy it so that it can be consumed by team members, developers, and third parties to provide useful functionality to applications and services for Adventure Works customers.

In this challenge you will use *Azure Machine Learning Services* and the *Azure Machine Learning SDK* to operationalize your model as a scoring endpoint in the cloud (specifically, as a containerized web service), so that developers at Adventure Works and elsewhere can write consumer applications and use this scoring endpoint for prediction.

## Prerequisites

* Your DSVM
* Your working model and code from Challenge02.

## Challenge

There are three elements to this challenge:

1. Explore Azure ML Deployment.
2. Deploy your gear classification model as a web service.
3. Use your web service.

### 1. Explore Azure ML Deployment

Explore the notes and code in the **03-Azure ML (*framework*).ipynb** notebook in the **/notebooks** folder to see an example of using Azure ML to deploy a model to a containerized web service.



#### Hints

* AML Workspaces are not available in every region...look at any errors and adjust accordingly.  `east us` works.  
* Open the Azure Portal and examine what the AML Workspace looks like.  After each cell that interacts with the workspace, look at what was added/changed in the portal.  
  * many times you will ask aml to do something and the command will complete, yet you won't see it in the Azure Portal.  For instance, "creating an image".  This is because you are actually only *defining* the container.  It gets built during the deployment.  
* It may take some time for some of the AML steps to complete.  You can see their status in the Azure Portal under AML|Activities

#### Questions

* where is the config written?  
* how can you examine `score_pytorch.py`?
* **Do not delete the workspace...yet!!** 


### 2. Deploy your gear classification model as a web service

Use the Azure Machine Learning SDK to provision an Azure Machine Learning Workspace, and deploy your gear classification model as a web service in an ACI container.

### Hints

* Make sure you are using the **Python 3.6 - Azure ML** kernel in Jupyterhub on your DSVM.
* Your deployment must include a scoring script that loads your model, uses it to generate a prediction from the input data, and returns the prediction. Remember that you must apply any data transformations that were used to pre-process the training data to the input data.
* You need to specify the Python libraries used by your scoring script in a .yml file, so that they are installed in the container image when it is deployed.
* Pay careful attention to the expected formats for input and output data, which is exchanged over HTTP when using the deployed model.

### 3. Use your web service

Write code to consume your deployed web service and generate a predicted class for a new image of your choice.

## Success Criteria

* Deploy a working container image that hosts your model.
* Run Python code that successfully calls your deployed web service with new image data, and displays the prediction that it returns.

When your coach has verified your team's solution, you can proceed to the [next challenge](Challenge04.md).

## References

* <a href="https://docs.microsoft.com/en-us/azure/machine-learning/service/overview-what-is-azure-ml" target = "_blank">What is Azure Machine Learning Service?</a>
* <a href="https://docs.microsoft.com/en-us/azure/machine-learning/service/how-to-deploy-to-aci" target="_blank">Deploy models with the Azure Machine Learning service</a>
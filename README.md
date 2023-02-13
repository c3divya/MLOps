# MLOps

## Overview of Model Deployment

## Why is modern deployment challenging?

- Modern deployment presents the challenges of traditional software like reliability, reusability, maintainability and flexibility, and it also presents additional challenges that are specific to machine learning,like reproducibility.


- Reliability refers to the ability of the software to produce the intended result and to be robust to errors.

- Reusability refers to the ability of the software to be used across systems and across projects

- Maintainability is the ease with which we can maintain the software in time

- Flexibility is the ability of add or remove functionality from the software.

- Reproducibility instead refers to the ability of the software to produce the same result, given the same data across systems.

## Let's discuss reproducibility in more detail 

- ML Model deployment is also challenging because it needs the coordination of various themes within an organization to ensure
that the more they produce the intended result and that it works reliably, it usually needs the coordination of
  - data scientists who develop the machine learning model 
  - I.T. teams and software developers who help put the model in   production
  - business professionals who understand how the model will be used in the organization and the customers and purpose that it is intended to model.
  
- Deployment is also challenging because there is often a discrepancy between the programming language in which the model is developed and the programming languages that are available in the production environments.

- If this is the case, then in the model to fit the languages available in production extends the project timeline and also risks the lack of reproducibility.

## Summary
- Model deployment is one of the most important stages in the machine learning lifecycle.

- And this is because to start using the machine learning model, it needs to be effectively deployed nto production so that it can provide its predictions to other software systems.

- In other words, to maximize the value of the machine learning model we create, we need to be able to reliably extract the predictions from the model and share them with other systems.


## Model Deployment Pipelines

We're normally talk about the deployment of machine learning models when, in fact we refer to deployment of machine learning pipelines.

So in this section, I want to introduce what a machine learning pipeline is and why we deploy pipelines instead of just mothers.

- In a simple way of imagining machine learning models, the organization has some data that can be stored in databases in the cloud or retrieved from Third-Party APIs. And then it feeds these data to build a model that then is able to provide some predictions that are of use to the business.

- However, data is almost never ready to be used to train machine learning models.
- In fact, data presents a variety of characteristics in terms of format and quality that make it unsuitable to machine loving mothers.
    - For example, data, one percent missing values and some of the library's tutoring machine learning models cannot cope with the lack of values in a data set.

    -  Data can also contain strings instead of numbers, and the computer cannot perform computations with strings.So we need to transform them into numbers to variables in the data present some distributions and the

   -  distribution of the variable may affect the performance of the model. So we may want to change some distributions.

   -  The data may also present outliers and some models are sensitive to the presence of outliers, so we may choose to censor or remove these values, the different variables in our dataset, maybe in a different scale.

   - Some mothers are sensitive to the scale of the variables, so we need to rescale them.
   
   - Sometimes our data is in the form of text, so we need to be able to extract information from this text into some sort of input that can be computed sometimes our data, our images.
   - And again, we should be able to extract data or features from these images.
   - Some of our data may be transactional and we may want to aggregate this data to have a more streamlined view of the customer.
   - Sometimes the data is geolocation and we may want to extract features from this data.
   - Sometimes we have a time series that we need to process or aggregate in a certain way, and we can also have date and time variables that we cannot use straight away in our models, but instead we derive eatures from them.

So before we can use these data to train them, although we need to carry out a lot of variable transformation, extract features from data, or create new features by combining existing ones. So then we're not talking of just training the models, but we are also talking about preprocessing
the data to make it suitable to train them over. And sometimes we may not want to use all the features available to us. So we may include a type of feature selection.

## So a machine learning pipeline contains a variety of steps 

That allow us to go from the raw data to the data format that is suitable to train the machine learning models so that we can obtain the predictions
when we deploy our machine learning model, then we do not just deploy the model itself, but we need to deploy the entire pipeline.

And why is that? Well, because both in the research and in the production environment, most likely we are going to receive the raw data.
So we need the steps of the pipeline that will allow us to produce the mature data with which we will be able to either train the model or once the model is train, obtain the predictions. I'm going to discuss the details of the different steps of the machine learning pipeline later on in Section four.

For the rest of this section, we're going to focus on the concept of building reproducible machine learning pipelines.


## Creating Machine Learning reproducible pipeline : 
In this section we will focus on about building reproducible machine learning pipelines and why that matters.

### What is deployment of machine learning model?
The deployment of a machine learning model is the process of making our model available in production environments where they can provide predictions to other software systems.

### Are the Machine learning model that we develop in Jupyter notebook means ML deployment ?
The ML Model that we develop in our jupyter notebook are the models developed in the Jupyter notebook. We 
do so in the so-called research environment.

### What is a research environment?
This is an isolated environment without contact to light data when the data scientist has the freedom to try and research the different models and find out a solution to a certain product need. In a common setting, we have historical data and we use this data to train a machine learning model, once we're happy with the performance of our model in the research environment, we're ready to migrate it to the production environment where it can receive input from life data and output predictions that can be used to make decisions.

*We often talk about deployment of machine learning models when, in fact, we mean deployment of a machine learning pipeline.*

### So what is a machine learning pipeline?

It is the series of steps that need to occur from the moment we received the data up to the moment we obtain a prediction.

- A typical machine learning pipeline includes a big proportion of feature transformation steps.</br>
Perhaps this is even the biggest part of the pipeline.

- Then it includes steps to train the machine learning mother and steps to output a prediction would create an entire pipeline in a research environment.

- I would need to deploy as well the entire pipeline to the production environment.
    - Why do we need to do?
     Because in the light environment, we're also going to receive raw data as input and we need to transform it to create the necessary features so that the model can interpret them and return the prediction.
- When we deploy our pipeline to production, we need to do it in a way so that the pipelines are reproducible.

### When we deploy our pipeline to production, we need to do it in a way so that the pipelines are reproducible.What does this mean?

It means that if both the pipeline in the research environment and the pipeline in the production environment receive the same raw data input, both pipelines should return this same protection, same data. Khamsin same output should come out of both pipelines.

Why do you think the research phase of our project we built a model and we optimized its performance. Static maximizes the business value.

When we develop a machine learning model for a machine learning pipeline, I should say we test model performance from a statistical perspective, utilizing classical metrics like the accuracy, the precision, recall, medium squared error and any other metric that you're familiar with. And we also evaluate metrics that translate these parameters into business value.For example, we may measure the increased revenue that our model will create or the increased customer satisfaction or any other measure that we're interested in, and that will vary with the organization.

If we want to translate this value, this revenue increase, for example, as I show in this light from a research environment to the real life that is to the environment, we need to make sure that the like model reproduces.

Exactly, or at least as much as possible in practice the that we created in the research environment. And this is why our models need to be reproducible.

*So why is reproducibility matters first, if we cannot reproduce our machine learning pipelines within the research and production environments we may incur in financial costs.*

But we also incur in substantial time loss because we need to spend a lot of time trying to figure out why the models are not identical, or at least very similar. And these will end up in the loss of reputation of the theme. But more important for me, at least, is the fact that without the ability to replicate the model results exactly.

It is very difficult to determine if a new model is truly better than the existing one. When we develop the machine learning model would usually compare it with the current model or set of rules that the organization is using without the ability to replicate the results.

Exactly. It is very difficult to determine if the new model is truly better than the current one.

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

   - Data can also contain strings instead of numbers, and the computer cannot perform computations with strings.So we need to transform them into numbers to variables in the data present some distributions and the

  -  distribution of the variable may affect the performance of the model.

So we may want to change some distributions.

The data may also present outliers and some models are sensitive to the presence of outliers, so we

may choose to censor or remove these values, the different variables in our dataset, maybe in a different

scale.

Some mothers are sensitive to the scale of the variables, so we need to rescale them.

Sometimes our data is in the form of text, so we need to be able to extract information from this text

into some sort of input that can be computed sometimes our data, our images.

And again, we should be able to extract data or features from these images.

Some of our data may be transactional and we may want to aggregate this data to have a more streamlined

view of the customer.

Sometimes the data is geolocation and we may want to extract features from this data.

Sometimes we have a time series that we need to process or aggregate in a certain way, and we can also

have date and time variables that we cannot use straight away in our models, but instead we derive

features from them.

So before we can use these data to train them, although we need to carry out a lot of variable transformation,

extract features from data, or create new features by combining existing ones.

So then we're not talking of just training the models, but we are also talking about preprocessing

the data to make it suitable to train them over.

And sometimes we may not want to use all the features available to us.

So we may include a type of feature selection.

So a machine learning pipeline contains a variety of steps that allow us to go from the raw data to

the data format that is suitable to train the machine learning models so that we can obtain the predictions

when we deploy our machine learning model, then we do not just deploy the model itself, but we need

to deploy the entire pipeline.

And why is that?

Well, because both in the research and in the production environment, most likely we are going to

receive the raw data.

So we need the steps of the pipeline that will allow us to produce the mature data with which we will

be able to either train the model or once the model is train, obtain the predictions.

I'm going to discuss the details of the different steps of the machine learning pipeline later on in

Section four.

For the rest of this section, we're going to focus on the concept of building reproducible machine

learning pipelines.

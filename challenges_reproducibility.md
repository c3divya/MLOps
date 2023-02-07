## In this Section, I want to discuss some of the challenges encountered when we want to transform the code

that we have in the research environment into production code and how these challenges affect the productivity

and the mood of the team and how why thinking ahead of even beginning to develop the model in the research

environment, we can mitigate some of these challenges and streamlined model deployment.

I would also like to discuss how open source libraries can help us streamline model deployment, minimize

the timelines for deployment and maximize reproducibility.

We mentioned previously that the pipelines that we build in the research environment and those in the

production environment should be identical or at least as similar as possible.

And this is to retain the value that we observed in the research environment, in the light environment.

We also mentioned that feature engineering involves a lot of data transformation and also model training

involves a lot of parameters that may be a challenge for reproducibility.

So when we research and develop a model in the research environment, we have a lot to code.

And much of this code is very repetitive within the same project.

But more importantly, across various projects, the machine learning pipelines across various machine

learning projects within the organization can be very similar to what we develop the machine learning

pipeline, the transformations and the machine learning models, no parameters from the data.

And we need to store these parameters somehow and all of this or may challenge reproducibility because

we have a lot to code to transform our data.

This process is very time consuming.

And because a different data scientist may code the same procedure differently in the different projects

that they're working on, we end up with different versions of the code that produces the same output

across the time.

We have multiple copies of the same code across projects and across systems.

We have different versions of the same code and therefore it is very difficult to keep track of what

is the last version or which one is the optimized version.

We may also end up with multiple intermediate files throughout the pipeline to save the parameters that

the feature transformation and models have learned.

And these parameters are usually saved and stored in config files or brown files.

If we didn't think about carefully when we started researching the model in the research environment,

when we transform the code into production code would end up having to rewrite a lot of code and also

to integrate models in production.

Because we want the software to work reliably, we need to include testing.

And in this process, we need to ensure as well reproducibility, so these stochastic procedures of

research and put in a model in production ends up with decreased in performance because of frustration,

lack of reproducibility between environments, and therefore it increases the deployment timelines.

Fortunately, with the use of open source, we can increase team performance, prevent frustration,

maximize reproducibility and minimize deployment times.

First of all, open source libraries already offer a variety of feature transformations and machine

learning models that we can take off the shelf and apply to our data.

Therefore, for the team, this means that there is no more need of coding the transformations on the

models by ourselves.

This work has been taken off our hands.

Open source libraries are also Persian, which help us track reproducibility, each version has information

that describes what the version contains and what is new in that version.

And by calling a specific version of the library, we can guarantee that we are using the same software

between the environments.

In open source libraries, also the classes and the functions that include the transformations for the

features on the machine learning models are tested.

Therefore, we do not need to include unit testing while we transform the projects from the research

into the production environments, because these libraries already include the tests that guarantee

that the functionality is the intended one.

So, as you can see, utilizing open source removes a lot of work from a hands both in the research

phase but more importantly, in the deployment phase.

So if I want to maximize reproducibility while decreasing deployment times, when we go through the

different steps of the machine learning pipeline, instead of writing code to perform the feature transformations

from scratch, which many of us tend to do, we should consider utilizing a various open source packages

for feature transformation, feature selection and also machine learning.

So that was we are happy with the model that we have in the research environment.

We only need to use the same versions of the library in the production environment and this will help

us maximize reproducibility and decrease production time.

I will talk more about the Python libraries that we can use to build machine learning pipelines in Section

four.

That is all for this video.

# AZ-Project (how to boostrap your first pipeline )
Step2: Create an Organization
Before you can begin creating a new DevOps project, you need to create a New Organization. C.lick on “New Organization” on the left hand menu to create one now (or you can choose to use an existing organization)
![image](https://github.com/Dmtry32/AZ-Project/assets/88732558/d2943d32-657d-4de8-88b3-5f4c90f1f888)

Step3: Create a Project
Once the organization is created, you need to create a new project like below:

![image](https://github.com/Dmtry32/AZ-Project/assets/88732558/22032d45-b0c3-4408-ace0-66c9a1202dae)

Choose any name you like, we are creating “Azure DevOps Pipeline Tutorial” for the sake of this tutorial. When the project is successfully created, you’ll see the dashboard of the project like below:


![image](https://github.com/Dmtry32/AZ-Project/assets/88732558/3afe962f-e1bd-4414-a764-18a035f74cde)

On the left menu, you’ll notice a range of services/tools like Boards, Repos, Pipelines, Test Plans, Artifacts that Azure DevOps has to offer. You can update which services you want to use by turning them on/off from the Project Settings (bottom button on the left menu)

![image](https://github.com/Dmtry32/AZ-Project/assets/88732558/2a11ea85-9b22-40cb-ad47-7fde0fd85484)

Step4: Create/Import a Repo
Before we begin to build pipeline, we need to have a code repository to build pipeline for. If you already have a code repository anywhere else (like GitHub, BitBucket, any private git repository, or Subversion) and want to import it to build the pipeline, you can skip this step and directly more to the next step to create the pipeline.

I am choosing to create a new Azure repository for the sake of this article. To create a new azure repo, click on Repos on the left menu to open the following page:

![image](https://github.com/Dmtry32/AZ-Project/assets/88732558/4e5c4494-d93e-4865-a9c0-43f3ee0e4582)

You’ll see a default repository created with the name of the project. You can either choose to use the default repository, or create a new repository. I am creating a new empty repository (without even the README.md file) named “pipeline-demo” as shown below. The reason to create empty repo is to be able to get instructions to push existing code to this repo. The newly created repository looks as below:

![image](https://github.com/Dmtry32/AZ-Project/assets/88732558/5bc57757-5cb3-424c-a908-845004c2b90c)
Next, import the code to this repository following the instructions on the new repo page. Now that we have a repository, its time to build a pipeline for this repo.

Step5: Create Azure Pipeline
You can create a new pipeline by either clicking the Set up build button on the repository page as shown below:

![image](https://github.com/Dmtry32/AZ-Project/assets/88732558/f21161ce-46bd-4172-8825-28b8c3540ebf)

OR

by choosing Pipelines from the left menu and clicking Create Pipeline button as shown below:

![image](https://github.com/Dmtry32/AZ-Project/assets/88732558/97df9780-f83c-4f8a-81f1-76b43279ce01)

We’ll use the second option, as it covers the longest journey of creating a pipeline. When you click the Create Pipeline button, you’ll be asked to choose the location of code repository that you would like to build pipeline for. The choices are as follows:

![image](https://github.com/Dmtry32/AZ-Project/assets/88732558/21a2b19d-d7fa-4cd6-8b3d-19f127e8cae8)
For the sake of this tutorial, I choose Azure Repos, which opens the following page showing all the azure repos from your projects:

![image](https://github.com/Dmtry32/AZ-Project/assets/88732558/fc8a6be4-eadb-4fd7-a23f-276b9940079a)

Lets choose the pipeline-demo repository that we created before.

Next step is to Configure the pipeline strategy. There are a number of options available (click Show More button to reveal all the options) which can help you build a starter template pipeline to deploy web application, deploy azure functions, container images, build and deploy maven sprintg-boot application, deploy azure App Service from container images etc etc. For the sake of this tutorial, I am going to choose Starter Pipeline

![image](https://github.com/Dmtry32/AZ-Project/assets/88732558/958c08e0-6125-4034-9153-6204b912b0a7)

Choosing Starter pipeline, will generate azure-pipelines.yml file (you can rename this file later if you want to) as shown below:


Your pipeline is ready to run. The basic pipeline shown above is already configured to use cloud build agents to run the pipeline. Click Save and Run button to run the pipeline.


Once the run is complete, you can see the results:

![image](https://github.com/Dmtry32/AZ-Project/assets/88732558/87d7c489-8c7b-41be-bd48-1863b550c4b2)

Clicking on the job, you can also see the detailed pipeline run logs as below:
![image](https://github.com/Dmtry32/AZ-Project/assets/88732558/ff3609c6-9ea3-4d4a-a20f-43718e6d44f7)


Notice all the steps like initialize, checkout, …, finalize above? These steps are injected by default when you create a pipeline. You can control some of these steps, for example, if you do not want to checkout the code for every stage of the pipeline, then you can specify so in the azure-pipelines.yml file.








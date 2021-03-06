## 1. Introduction
Welcome! This tutorial will walk you through the most crucial and relevant steps that a data scientist at Cien has to perform when beginning development at Cien. 

## 2. Data Science tools, platforms and practices
At Cien, we are engaged with a variety of tools and techniques for making the data science processes as exciting as possible while yielding the best on time. In this regard, we would like to introduce you to following tools-
- **Git** : Git is a version control system for tracking changes in computer files and coordinating work on those files among multiple people. It is primarily used for source code management in software development,but it can be used to keep track of changes in any set of files. Git can be installed through this [link](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git) or by using the link https://git-scm.com/downloads
- **Bitbucket** : Bitbucket is a web-based version control repository hosting service owned by Atlassian, for source code and development projects that use Git revision control systems. We can signup for the bitbucket using the @cien.ai extension email at this [link](https://bitbucket.org/account/signup/)
- **Jira** : Jira is a proprietary issue tracking product, developed by Atlassian. It provides bug tracking, issue tracking, and project management functions. 
  + **What is Jira workflow?** 
  
   The JIRA workflow describes the process of tracking the progress of the development of a model or resolution of a conflict/issue. This process tracking is important for a lot of purposes sucha as backlog tracking, status identification of assignment etc. We can understand the workflow exactly as used by the Cien's data science team through this document: [Understanding JIRA workflow](https://docs.google.com/document/d/1RMRGyiqh09yaYUGUhB3x7PxzztUnFqsBMARneZ_Q74s/edit)
  
  
- **Python** : At Cien, we are working with the Python 2.7 as our preferred language for developing data science software. We can install Python 2.7: https://www.anaconda.com/download/
- **Sublime Text** or **VS Code** or some IDE of your choice for running Python
- **MongoDB** :
- **Studio 3t** : It is a GUI based interface to access MongoDB. We can download it from https://studio3t.com/download/ . 
- **Lastpass** : This is the coolest password management system known to data science community. At Cien, we use it extensively for sharing passwords during the development. We can download it from the link [Download Lastpass](https://lastpass.com/misc_download2.php). Once you have downloaded the lastpass, you've to register using the email with @cien.ai extension and request the Cien development manager or your supervisor to share the shared data science folder with you.
- Cien_DS Package :
- Linter or Flake8: In case you're installing linter on sublime text, you can do so by going to the package manager and choosing the option of linter. In case you're a user of sublime text, you can do so by clicking on this intructional manual [Installing flake8](https://code.visualstudio.com/docs/python/linting)

## 3. Installing the dependencies for the Cien-DS Package
- Copy the following and paste it into a text file "requirements.txt" in your local working directory (i.e. the directory where you are at present rather than the root / parent directory).
  + simplejson==3.13.2
  + scikit-learn==0.18.1
  + statsmodels==0.8.0
  + lifelines==0.10.1
  + numpy==1.13.1
  + gensim==2.2.0
  + pandas==0.20.1
  + pymongo==3.4.0
  + slackclient==1.0.9
  + editdistance==0.4
  + unidecode
  + nltk==3.2.4
  + joblib==0.11
  + xlrd==1.0.0

To install the above python packages in pip, run `"pip install -r requirements.txt"` .
Alternatively,  to install an individual package, run `"pip install <package-name>==<version>"` (e.g. : pip install gensim==2.2.0) 

for all the packages you wish to install, Run the following shell command:
`python -m nltk.downloader -d /usr/share/nltk_data words stopwords wordnet`

By now, you must have created accounts in the following (ask access if you cannot do it on your own):
- Jira
- Bitbucket
- Confluence
- Lastpass

So, now you can ask for access to: Lastpass shared folders from your immediate supervisor or the Cien's development manager. 
You should now be familiar with git commands. The project uses GitFlow Workflow. Information on this process can be found here: https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow.

Firstly, clone the main Cien repo by issuing the following command (change <myusername>)

`git clone https://<myusername>@bitbucket.org/cienbcn/cien-ds.git`

An important thing to note is that code should never get pushed directly into master. You should start out by checking out code using the following command:

`git checkout -b develop origin/develop`

When working on a feature, perform a git checkout with the branch name, e.g. if your branch is called ' DS-412 ' (created from a JIRA ticket):

`git fetch & checkout DS-412`
A typical set of git commands for working on a new feature is as follows:

`git checkout DS-412`

In case you wish to add/edit/delete files for the new feature

`git add .`

`git commit -am "friendly message"`

`git push //pushes your changes`

Copy/paste the link that will be returned and do the pullrequest from your browser to develop branch and add Ben, Christina and Pierre as reviewers.

  
## 4. Installing the Cien-DS Package
This documentation will take you through the process of installing the Cien DS package.

- Prerequisites For the installation, you need:

  + Ubuntu 16.04
  + Python 2.7
  + pip 9.0.1
  + Git
  + A BitBucket account. Once ready, ask a Cien dev manager to add you as member of the BitBucket group.
  + A LastPass account. Once ready, ask a Cien dev manager to share the Shared-Data Science folder with you.
  
**Downloading the repository**: The project repository is located on BitBucket. Download it with git:

`$ git clone git@bitbucket.org:cienbcn/cien-ds.git`

Installing the requirements
Change directory to the following location:

`$ cd cien-ds/job_runner`
The Cien DS package depends on some other Python packages. Install them by issuing the following commands (However, if you've installed the packages mentioned in requirements.txt file, you don't have to do this again):

`$ pip install -r requirements.txt`

`$ sudo python -m nltk.downloader -d /usr/share/nltk_data words stopwords wordnet`

**Setting the environment variables**: Go to LastPass and copy to clipboard the contents of the bash profile DS note, located in the Shared-Data Science folder. Then, paste the contents of the note at the end of the `~/.bashrc` file. Save and close. Finally, close and open the terminal to make the changes effective.

## 5. Understanding the Cien-DS Package
- In order to have a brief overview of most relevant directories in the cien-ds package, this document explaining the structure of the cien-ds package can be of utmost importance: [structure of cien-ds package](https://docs.google.com/document/d/1m3RcmNx4XixGw-jmImSZDdN-10zsoZ1CcLPREi63h7I/edit?usp=sharing).


## 6. Understanding the Cien's Mongo Database 
- structure of our Mongo database: entity collections, data logs, job logs, also some basic info on mongo, such as this: https://cienbcn.atlassian.net/wiki/spaces/DAT/pages/82706433/2.+MongoDB

- Which are the most important common fields in Mongo, such as coid, docid, `_id`, distinction between raw, crm and ml fields
creating training sets, refer to Shelby's documentation

- Where should I go for having definitions about: lead, opp, account, how salesforce can be used for prospecting and selling, how collections are related: activities performed on an opp/lead/account object, etc, some documentation on this should be in Drive : We can always look to this [documentation](https://docs.google.com/document/d/1WM2FzXr8zbVry1q48Comq1dUGbqBwqTY5AKCWOrgGIs/edit?usp=sharing) for having a brief insight about these terms and processes

## 7. Doing Machine Learning on Cien Platform
- **When do I begin working on a machine learning model?**
  + We begin working on a task of creating a machine learning model once a task is assigned to us in the form of a JIRA card  through the JIRA issue tracking system. The steps to proceed once an issue is assigned to create a model is described in this document :[first steps after issuance of a JIRA Card](https://docs.google.com/document/d/1YwwBfZslVnn2nOg5A1gWE94Obh_Cl9VGZehBmumjLRA/edit?usp=sharing)
- **How can I create training sets for my machine learning models?**
  + Once we have followed the above mentioned steps to create a branch to work on our assigned task, we can always go on to create a model from scratch or maybe by using some of the existing resource that the data scientists at cien have already created. In this case, the file mentioned here can be of exemplary importance:  [Introduction to Training Set Creation](https://docs.google.com/document/d/1svG5GuPW6aU9uG1Z8pnc6b-b0ULGNaWVpIMdyo6T9vk/edit?usp=sharing)
- **How can I create machine learning models? How do I know that which type of model is required for my assignment?**

  + When you have a task assigned to you through the JIRA, you may have to develop a model to resolve the issue. In that case, the underlying model might be an assignment model or it might be a training model. We need **Asssignment Models** in the case when we just have to transform the data to finish the task. However, in case the task requires us to learn from data, maybe transform and use a machine learning algorithm to predict on test set, we have to use a **Training Model**. The **base model** and steps for writing an assignment model & training model can be explained by referring to: [Creating Your first Machine Learning Learning](https://docs.google.com/document/d/1GhmIiBDns63pyHeJUfjvAktOXUQxofLguLZm-rKLBfI/edit?usp=sharing)

- **How can I run the machine learning models that I have created for the purpose of training, validation, testing and writing the computed values in databse?**

   + The need to run the machine learning models (both assignment or training) can be due to either of the following reasons:
   + Checking how well your model is performing in terms of training error;
   + Checking what values an assignment model is computing as part of final computations;
   + Writing the values computed by your model to the database which is MONGODB in our case.

   + So, we can accomplish all these objectives and many similar like them using our **model tester**. The objective of the model tester as the name says is to run the model as part of testing procedures. However, even if we are not testing and actually willing to write directly into the database, the model tester is something that we have to use. 
In order to run model tester, we have to follow the steps specified in this documentation: [Introduction to the Model Tester](https://docs.google.com/document/d/144Rz6addcV3dcSbpZAf4c2FK0PbTEZc9qASd6mAvTBg/edit?usp=sharing)

- **How can I perform Quality Assurance/Analysis for the Machine Learning Model that I have developed on the Cien Platform?**

In order to perform and enforce quality checks on your model, you have to follow a set of standard procedure developed by Data Scientists at Cien. These are well documented in our report that can be accessed here: [Quality Assessment for Data Science Processes](https://docs.google.com/document/d/1nqkvnuPkWZcAbF2GZn6UVmPh7orFvKkwZFET5w0-DPo/edit)
- **How can I utilize the ability of having a local MONGO on my working computer to work locally with the database?**

We can run the local MONGO whenever and wherever required by following the documentation described here- [Quality Assessment for Data Science](https://docs.google.com/document/d/1kK8Z7aUse9tq6yEgxJXY48TkbHdkIsbCufvKVR9oUEo/edit)

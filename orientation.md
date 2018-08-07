## 1. Introduction


## 2. Data Science tools, platforms and practices
At Cien, we are engaged with a variety of tools and techniques for making the data science processes as exciting as possible while yielding the best on time. In this regard, we would like to introduce you to following tools-
- **Git** : Git is a version control system for tracking changes in computer files and coordinating work on those files among multiple people. It is primarily used for source code management in software development,but it can be used to keep track of changes in any set of files.
- **Bitbucket** : Bitbucket is a web-based version control repository hosting service owned by Atlassian, for source code and development projects that use Git revision control systems.
- **Jira** : Jira is a proprietary issue tracking product, developed by Atlassian. It provides bug tracking, issue tracking, and project management functions.
- **Python** : 
- **Sublime Text** or **VS Code** or some IDE of your choice for running Python
- **MongoDB** :
- **Studio 3t** :
- **Lastpass** :
- Cien_DS Package :

## 3. Setting up the Python
- Install Python 2.7: https://www.anaconda.com/download/
- Install Git: https://git-scm.com/downloads
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

To install the above python packages in pip, run "pip install -r requirements.txt" 
Alternatively,  to install an individual package, run "pip install <package-name>==<version>" (e.g. : pip install gensim==2.2.0) for all the packages you wish to install
Run the following shell command:
python -m nltk.downloader -d /usr/share/nltk_data words stopwords wordnet
Install Studio 3T (MongoDB interface): https://studio3t.com/download/ 
Create accounts in the following (ask access if you cannot do it on your own):
Jira
Bitbucket
Confluence
Lastpass
Ask access to:
Lastpass shared folders
Clone the Git repository of the cien_ds package locally following the instructions here: https://bitbucket.org/cienbcn/cien-ds/src/a6b4d62abc1e4482db2e80f626e61bef99f6128a/docs/git.md
  
## 4. Installing the Cien-DS
This documentation will take you through the process of installing the Cien DS package.

- Prerequisites For the installation, you need:

  + Ubuntu 16.04
  + Python 2.7
  + pip 9.0.1
  + Git
  + A BitBucket account. Once ready, ask a Cien dev manager to add you as member of the BitBucket group.
  + A LastPass account. Once ready, ask a Cien dev manager to share the Shared-Data Science folder with you.
  + Downloading the repository
The project repository is located on BitBucket. Download it with git:

`$ git clone git@bitbucket.org:cienbcn/cien-ds.git`

Installing the requirements
Change directory to the following location:

`$ cd cien-ds/job_runner`
The Cien DS package depends on some other Python packages. Install them by issuing the following commands:

$ pip install -r requirements.txt
$ sudo python -m nltk.downloader -d /usr/share/nltk_data words stopwords wordnet
Setting the environment variables
Go to LastPass and copy to clipboard the contents of the bash profile DS note, located in the Shared-Data Science folder.

Then, paste the contents of the note at the end of the ~/.bashrc file. Save and close.

Finally, close and open the terminal to make the changes effective.


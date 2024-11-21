---
title: PIVOT
layout: default
nav_order: 3
parent: Repositories
---

This repository contains the code required to run the Phytoplankton Image Validation Optimization Toolkit (PIVOT) streamlit application locally.  

# Installation and Setup Instructions

__Installations:__

- Git interfaces (needed to clone the PIVOT repository). Download and follow the installation instructions at the [git](https://git-scm.com/downloads) or [git bash (for Windows)](https://gitforwindows.org/) websites. Configure with your name and email using the commands: `git config --global user.name "Your Name"` and `git config --global user.email "your-email@example.com"`. Verify with: `git config --global –list`
- Miniconda (used to run PIVOT). Download and follow the installation instructions at the miniconda installation [website](https://docs.anaconda.com/miniconda/install/). You can check whether the installation is correct by opening the miniconda terminal and typing `conda -V`. The prompt should return the version of conda installed. You can update the version with the command: `conda update conda`

__Cloning the repository to your local machine:__  

1.	Open your git interface and navigate to the folder where you want your PIVOT folder to be located: `cd path/to/folder`
2.	Clone the PIVOT repository using the command: `git clone https://github.com/ifcb-utopia/PIVOT.git`   

__Setting up your virtual environment:__  

3. Open miniconda and navigate to the first PIVOT folder: `cd path/to/folder/PIVOT`
4.	Create a virtual environment using the provided yml file: `conda env create -f environment.yml`. Note: you can check to see which environments you have set up by typing `conda env list` or `conda info --envs`. Activate an environment with the command `conda activate environment_name` and deactivate with `conda deactivate`. 
5.	Activate the PIVOT environment: `conda activate pivot`  

__Running PIVOT:__  

6.	Log into [Azure](https://portal.azure.com/#home) and navigate to the ifcbsql resource. In Overview > Properties, click on Networking and scroll down to Firewall rules. You can add your IP address by clicking ‘Add your client IPv4 address’ or entering a new firewall rule. If you don’t have access to Azure, send your IP address to one of the ifcbUTOPIA organizers. Note: your IP address may change, so if you repeatedly have issues accessing the SQL server, check to see whether you still have access in Azure.  
7.	Run the streamlit app by typing: `streamlit run PIVOT/app.py`. The app may automatically pop up in your internet browser, but if it doesn’t, copy and paste the URL that appears in the miniconda prompt into your browser to access the page. If the page gives you a SQL server error, wait a minute for the server to wake up or check Azure to ensure your IP address has access. 
8.	Enter your email in the User Information section. If you are a new user, you’ll be asked to enter a bit of additional information (name, organization, experience).
9.	Select which dataset you would like to work on and the validation specifications.
10.	Congrats, you’re ready to start classifying plankton!

# 260115-challenge

Challenge

```
python -m venv .socratic && source .socratic/bin/activate   # or conda env create -f environment.yml
pip install -r requirements.txt

```


# Challenge
In this project we will try to predict the current GA_NUM if will be trigger a pipeline or not.

There are two files, the data.pkl.gz which contain the whole information and the target.pkl.gz contains 3 fields, the VISITDATA and the conversion (trigger or not the pipeline).

We will try to focus the effort to try to solve it. So we frame the escenario as follows.

- Multiples records form the same **GA_NUM** may occur one or more days, we will try to identify the conexion that trigger the conversion if  **AUTOFORMCOMPLETES** or **FORMCOMPLETES** has a flag, to differenciate each one there are **timestampsevent** (linux time).
- We will keep only one record from each **GA_NUM** that matches with the formcompleetes
- we will remove records that happend after the **VISITDATE**
- We will keep only records that are **Paid Search** from the **MARKETINGCHANNEL**


This document its a iteration of a livedocument, we try to keep a clean and comprensive version, if the reviewer wants to check previous iteration he could review other notebooks that are in drafts. We try to follow the *CRISP-DM* framework to solve this challenge

One of the biggest task from data analysis is the EDA (Exploratory Data Analysis). Instead of focusing in only one part, We try to focus the effort of the challenge in showing the capabilities of the whole end to end ml problem. 

For this we use the YDATA; a python framework that create EDA. 


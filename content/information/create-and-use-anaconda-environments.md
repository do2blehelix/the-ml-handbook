---
title: Python Environments
description: Create And Use Anaconda Environments
date: 2021-04-05 18:30:00 +0000
weight: 4
collapsible: false

---
# Python Environments

Anaconda Environments provide a way of working with python packages. You can have any version of any package installed in a specific environment without changing you original set of packages. It is especially helpful for installing version compatible packages together. 

#### Create the environment

###### Anaconda

    conda create --name <<myenv>>

###### Python

    python -m venv <<myenv>>

#### Check if environment was created

###### Anaconda

    conda env list

###### Python

#### Activate the environment

###### Anaconda

    conda activate <<myenv>>

###### Python

    .\env\Scripts\activate

#### That's it install packages the way you do

###### Anaconda

    conda install pandas

###### Python

    pip install pandas

#### Deactivate

###### Anaconda

    conda deactivate

###### Python

    deactivate
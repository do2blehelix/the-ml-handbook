---
title: Anaconda Environments
description: Create And Use Anaconda Environments
date: 2021-04-05 18:30:00 +0000
weight: 4
collapsible: false

---
# Anaconda Environments

Anaconda Environments provide a way of working with python packages. You can have any version of any package installed in a specific environment without changing you original set of packages. It is especially helpful for installing version compatible packages together. 

#### Create the environment

    conda create --name <<myenv>>

#### Check if environment was created

    conda env list

#### Activate the environment

    conda activate <<myenv>>

#### That's it install packages the way you do

    conda install pandas
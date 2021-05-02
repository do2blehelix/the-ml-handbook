---
title: Share Python with Packages
date: 2021-04-03T18:30:00.000+00:00
weight: 
enableToc: false
tocLevels: []
tags: []

---
# Install PIP and Packages in Python Embeddable

## Download Python Embeddable

Python Embeddable is a lite flavor of python with barebone necessities. It can be used to deploy web-apps to systems which don't have permission to install python or its packages.

\[Download it from Here: Official Python 3.8.9\](https://www.python.org/ftp/python/3.8.9/python-3.8.9-embed-amd64.zip)

## Configure PIP

Even if explicitly stated that the embeddable [version of Python does not support Pip](https://docs.python.org/using/windows.html#windows-embeddable), it is possible with care. You need to:

1. Download and unzip Python [embeddable zip](https://python.org/downloads) file.
2. In the file `python39._pth` or similar, uncomment the `import` command. Result should look similar to this:

       python39.zip
       .
       import site
3. [Download get-pip.py](https://pip.pypa.io/en/stable/installing) to the Python install folder
4. Run `get-pip.py`. this installs Pip into the `Scripts` directory:

       python get-pip.py

## Install Packages

Run Pip directly from command line as Pip is a executable program (this example is to install Pandas):

    .\Scripts\pip install pandas
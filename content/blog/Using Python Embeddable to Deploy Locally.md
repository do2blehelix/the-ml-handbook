---
title: ''
date: 
weight: 
enableToc: false
enableBlogBreadcrumb: false
tocLevels: []
tags: []

---
# Install PIP and Packages in Python Embeddable

Even if explicitly stated that the embeddable [version of Python does not support Pip](https://docs.python.org/using/windows.html#windows-embeddable), it is possible with care. You need to:

1. Download and unzip Python [embeddable zip](https://python.org/downloads) file.
2. In the file `python39._pth` or similar, uncomment the `import` command. Result should look similar to this:

       python39.zip
       .
       import site
3. [Download get-pip.py](https://pip.pypa.io/en/stable/installing) to the Python install folder
4. Run `get-pip.py`. this installs Pip into the `Scripts` directory:

       python get-pip.py
5. Run Pip directly from command line as Pip is a executable program (this example is to install Pandas):

       .\Scripts\pip install pandas
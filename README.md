# Data Science

mono repo for data science projects and data sets

# Installing TF and tools on an m1 mac

I followed this tutorial and was able to run a simple TF jupyter notebook in the hello_ds project
https://code.visualstudio.com/docs/python/data-science-tutorial

But trying to run a few google examples using more TF features (like covnets) failed.  So I looked at making sure I was running TF correctly on the mac m1, which led me to:

https://github.com/apple/tensorflow_macos
https://github.com/apple/tensorflow_macos/issues/153

1. Install Miniforge as your primary python interpreter, and make sure conda is using it
2. Follow the steps in tensorflow_macos to create a conda envrionment with tensorflow installed.  Tensorflow HAS to be installed after the environment, and Pandas.
3. Follow the vscode tutorial but use the conda environment set up in step 2 instead of creating a new one.
4. Install any dependencies required but not installed as part of the environment (like Pandas) using pip
5. Matplot lib requires libjpeg - install with homebrew or build from source
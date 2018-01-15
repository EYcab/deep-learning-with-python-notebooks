# Companion Jupyter notebooks for the book "Deep Learning with Python"

This repository contains Jupyter notebooks implementing the code samples found in the book [Deep Learning with Python (Manning Publications)](https://www.manning.com/books/deep-learning-with-python?a_aid=keras&a_bid=76564dff). Note that the original text of the book features far more content than you will find in these notebooks, in particular further explanations and figures. Here we have only included the code samples themselves and immediately related surrounding comments.

These notebooks use Python 3.6 and Keras 2.0.8. They were generated on a p2.xlarge EC2 instance.

Let's try zero setup DL in the Cloud, [FloydHub](https://www.floydhub.com/) has already prepared the environment for you! Following the next steps you will have a GPU instance up and running for executing the Jupyter Notebooks.

Happy Deep Learning with Python :)

## FloydHub setup

### 1. Create a FloydHub account

* [Sign up](https://www.floydhub.com/signup) on FloydHub
* Install the floyd CLI on your local machine through these two [steps](https://www.floydhub.com/welcome):

```
$ pip install -U floyd-cli

$ floyd login
# Follow the instructions on your CLI
```

### 2. Clone this project to your local machine

```
$ cd /path/to/your-project-dir
$ floyd clone redeipirati/projects/deep-learning-with-python-notebooks/22
```

### 3. Create your project version on FloydHub
* [Create a project](https://www.floydhub.com/projects/create) on FloydHub and then sync the cloned repository with your new project
```
$ floyd init your-project-name
```

### 4. Run the project through a jupyter notebook

* The `--env` flag specifies the environment that this project should run on, which is a Tensorflow 1.4.0 + Keras 2.0.8 backend environment with Python 3.6.
* The `--data` flag specifies that the cats_and_dogs_small dataset should be available at the `/input` directory
* The `--mode` flag specifies that this job should provide us a Jupyter notebook
* Note that the `--gpu` flag is optional for now, unless you want to start right away to run the code on a GPU machine. Since you'll be exploring and playing around with the code, you might not need a GPU instance right away, so you can avoid that flag now and restart it later with a GPU instance.

```
floyd run \
  --env tensorflow-1.4 \
  --data redeipirati/datasets/cats_and_dogs_small/1:input \
  --mode jupyter \
  --gpu
```

Once the job is started, the jupyter notebook will open in your browser and you are ready to go!


### More about FloydHub platform

* Note that changes you make to the notebook running on Floyd servers are not going to be saved at your local directory, but they are going to be available in the [output](redeipirati/projects/deep-learning-with-python-notebooks/22/output) section of your job.
* Once you stop the Jupyter notebook job you were running, from the job page, you can click on [Restart](http://blog.floydhub.com/restart-jupyter-notebook-workflow/?utm_medium=email&utm_source=21sep17) to restart your job exactly how you left it and optionally choosing another environment (CPU or GPU). This is a great way to spend less of your GPU hours if you are working on tasks that does not require a GPU.
* If you need any help check our [documentation](http://docs.floydhub.com/) and [forum](https://forum.floydhub.com/).



## Table of contents

* Chapter 2:
    * [2.1: A first look at a neural network](http://nbviewer.jupyter.org/github/fchollet/deep-learning-with-python-notebooks/blob/master/2.1-a-first-look-at-a-neural-network.ipynb)
* Chapter 3:
    * [3.5: Classifying movie reviews](http://nbviewer.jupyter.org/github/fchollet/deep-learning-with-python-notebooks/blob/master/3.5-classifying-movie-reviews.ipynb)
    * [3.6: Classifying newswires](http://nbviewer.jupyter.org/github/fchollet/deep-learning-with-python-notebooks/blob/master/3.6-classifying-newswires.ipynb)
    * [3.7: Predicting house prices](http://nbviewer.jupyter.org/github/fchollet/deep-learning-with-python-notebooks/blob/master/3.7-predicting-house-prices.ipynb)
* Chapter 4:
    * [4.4: Underfitting and overfitting](http://nbviewer.jupyter.org/github/fchollet/deep-learning-with-python-notebooks/blob/master/4.4-overfitting-and-underfitting.ipynb)
* Chapter 5:
    * [5.1: Introduction to convnets](http://nbviewer.jupyter.org/github/fchollet/deep-learning-with-python-notebooks/blob/master/5.1-introduction-to-convnets.ipynb)
    * [5.2: Using convnets with small datasets](http://nbviewer.jupyter.org/github/fchollet/deep-learning-with-python-notebooks/blob/master/5.2-using-convnets-with-small-datasets.ipynb)
    * [5.3: Using a pre-trained convnet](http://nbviewer.jupyter.org/github/fchollet/deep-learning-with-python-notebooks/blob/master/5.3-using-a-pretrained-convnet.ipynb)
    * [5.4: Visualizing what convnets learn](http://nbviewer.jupyter.org/github/fchollet/deep-learning-with-python-notebooks/blob/master/5.4-visualizing-what-convnets-learn.ipynb)
* Chapter 6:
    * [6.1: One-hot encoding of words or characters](http://nbviewer.jupyter.org/github/fchollet/deep-learning-with-python-notebooks/blob/master/6.1-one-hot-encoding-of-words-or-characters.ipynb)
    * [6.1: Using word embeddings](http://nbviewer.jupyter.org/github/fchollet/deep-learning-with-python-notebooks/blob/master/6.1-using-word-embeddings.ipynb)
    * [6.2: Understanding RNNs](http://nbviewer.jupyter.org/github/fchollet/deep-learning-with-python-notebooks/blob/master/6.2-understanding-recurrent-neural-networks.ipynb)
    * [6.3: Advanced usage of RNNs](http://nbviewer.jupyter.org/github/fchollet/deep-learning-with-python-notebooks/blob/master/6.3-advanced-usage-of-recurrent-neural-networks.ipynb)
    * [6.4: Sequence processing with convnets](http://nbviewer.jupyter.org/github/fchollet/deep-learning-with-python-notebooks/blob/master/6.4-sequence-processing-with-convnets.ipynb)
* Chapter 8:
    * [8.1: Text generation with LSTM](http://nbviewer.jupyter.org/github/fchollet/deep-learning-with-python-notebooks/blob/master/8.1-text-generation-with-lstm.ipynb)
    * [8.2: Deep dream](http://nbviewer.jupyter.org/github/fchollet/deep-learning-with-python-notebooks/blob/master/8.2-deep-dream.ipynb)
    * [8.3: Neural style transfer](http://nbviewer.jupyter.org/github/fchollet/deep-learning-with-python-notebooks/blob/master/8.3-neural-style-transfer.ipynb)
    * [8.4: Generating images with VAEs](http://nbviewer.jupyter.org/github/fchollet/deep-learning-with-python-notebooks/blob/master/8.4-generating-images-with-vaes.ipynb)
    * [8.5: Introduction to GANs](http://nbviewer.jupyter.org/github/fchollet/deep-learning-with-python-notebooks/blob/master/8.5-introduction-to-gans.ipynb
)

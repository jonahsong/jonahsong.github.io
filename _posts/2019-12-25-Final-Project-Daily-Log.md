---
layout: post
Title: Final Project Daily Log
---

Below is a log of my daily progress, including:

1.) What I worked on today

2.) What I learned

3.) Any road blocks or questions that I need to get answered

4.) What my goals are for tomorrow

**January 7th**


Today I researched what neural networks actually and the different methods for programming them. I looked into PyTorch, TensorFlow, and Keras. With my experience in Python, I decided that I will use PyTorch for the project because of its Pythonic nature. Overall, I learned that neural networks are algorithms that use pattern recognition to interpret data with labeling or clustering. My goal for tomorrow is to actually learn how to utilize PyTorch.


**January 8th**


Today I started learning how to actually use PyTorch with an example with gradient descent. I read a very detailed article that examined how to execute gradient descent, while comparing methods with Numpy and PyTorch. The article generally reviewed each of the main components of PyTorch and then explained how they were used in the gradient descent example. I feel that I learned the bare bones of PyTorch (autogrid, dynamic computation graph, model classes) today. My goal for tomorrow is to decide on how I want to apply neural networks. I want to determine what the actual project is and how it will utilize neural networks.


**January 9th**


Today Sophie and I decided what we want to do for our project. Using torchtext, we plan to make a translator. During class, I researched the different tools and features of PyTorch that will go into our translator. I learned that our translator will use the Field class so that all of our data in both languages can be easily iterated through in a way in which each sentence has a predetermined specified way of being preprocessed. I’m not positive on how we will do the tokenization for the program but I think that Spacy will be a pretty easy way for us to do it. We will have to use Space (or another program besides torchtext because torchtext only has tokenizers for English. Lastly, I believe that torchtext’s BucketIterator will be crucial in our model. What the BucketIterator will do is define an iterator that pairs example sentences of similar lengths together, reducing the amount of padding needed. Tomorrow, I want to find a good and comprehensible tutorial and read through it, making sure that I completely understand it.



**January 10th**


Today we found and read through a really detailed tutorial on the PyTorch website on how to code a language translator using torchtext. We learned how to to preprocess sentences  into the standard format for NLP using TranslationDataset, Field, and BucketIterator (3 convenience classes of torchtext). I also downloaded PyTorch, Spacy, and CUDA packages  today so that we can start programming on Monday. We started building the program at the end of the period but we are still having some errors related to PyTorch and Space imports  that we need to sort out.



**January 13th**



We are currently having many errors with running our code. My personal error messages are stating that the system is unable to find the functions and imports that I am trying to call. I believe that the downloads that I had to do using terminal (PyTorch, Spacy, CUDA) were somehow not executed correctly. I used Anaconda to install these packages but maybe for my computer I should have used to pip to install them (?). I am still trying to work these issues out with my diligent partner in crime, Sophie.



**January 15th** 



With the help of Lauren, I was able to resolve the issues I was having in running the preliminary pieces of code. Somehow, there was an error when I initially installed Spacy with Anaconda. So, Lauren showed me how to download the package using pip. After I completed the download, the code was running smoothly. Currently, all our translator does is return metrics about the training and testing data. What we want to do in the coming days is figure out how we can enter a sentence in one language, and return the sentence in the other language.




**January 16th**

**January 17th**
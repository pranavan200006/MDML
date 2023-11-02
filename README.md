# MDML
Machine learning-based Malware Detection tool

Malware has emerged as a major cyber hazard in the modern era due to the Internet's rapid expansion. Malware is any software that engages in malicious activities, such as data theft, espionage, etc. "A type of computer program designed to infect a legitimate user's computer and inflict harm on it in multiple ways" is what Kaspersky Labs (2017) defines as malware. 
Anti-virus scanners are unable to keep up with the growing diversity of malware, leaving millions of hosts vulnerable to attacks. In 2015, 4,000,000 distinct malware items were found and 6,563,145 distinct sites were attacked, according to Kaspersky Labs (2016). Consequently, by 2019, the cost of data breaches is expected to exceed $2.1 trillion worldwide, according to Juniper Research (2016).

In addition, because of the widespread availability of attack tools on the Internet these days, the amount of expertise needed to create malware is declining. Anyone can become an attacker, regardless of skill level, thanks to the widespread availability of anti-detection techniques and the ability to purchase malware on the black market. According to recent studies, an increasing number of attacks are either automated or carried out by script kiddies. (2010, Aliyev). Since all current malware applications tend to have multiple polymorphic layers to avoid detection or to use side mechanisms to automatically update themselves to a newer version at short intervals to avoid detection by any antivirus software, malware detection through standard, signature-based methods is becoming more and more difficult. Antivirus software may identify novel threats without depending on signatures thanks to machine learning. Antivirus software used to mostly rely on fingerprinting, which compares files to a sizable database of known malware.

The main problem with this is that signature checkers are limited to identifying malware that has already been seen. Considering that hundreds of thousands of new malware types are developed every day, that is a rather big blind spot. In contrast, machine learning can be trained to distinguish between the telltale indications of healthy and unhealthy files, allowing it to spot dangerous patterns and identify infection independent of its prior exposure.

# Product Objectives

As previously mentioned, signature-based malware detectors are capable of detecting known malware that has already been uncovered by some anti-virus software providers. But it cannot identify new malware for which signatures have not yet been produced, nor can it identify polymorphic malware, which can alter its signatures. However, heuristic-based detectors' accuracy is frequently insufficient for sufficient detection, leading to a high number of false positives and false negatives. In 2016, Baskaran and Ralescu. The fast rate at which polymorphic viruses spread dictates the necessity for novel detection techniques.

# Dataset Resources

PE Header: https://www.kaggle.com/datasets/dscclass/malware

# Functional Requirements

Modules used (while installation):

* sklearn 0.24.1
* pyfiglet 0.8.post1
* pefile
* joblib 1.1.0

#Malicious URL Detection

This part of the program also consists of two phases, Cleaning the data for the Logistic Regression and then training the machine to identify if it is malicious or not. The Model is sketched out in such a way that it can meaningfully understand the data from which it has to be trained upon and tried to develop a defined behaviour from the data-sets. Data-sets are the backbone of any model and hence it should be adequate and precise data for good as well as bad URLs present in the data for the model to be trained upon. The Machine Learning for the malicious website detection will first involve in cleaning of our data within the data-sets. We used pandas and defined our own vectorizer to clear the data-sets and then used Logistic Regression to train our model.

Since the URLs are different from our normal text documents, a sanitization method is used to get the relevant data from raw URLs.

We will implement our sanitization function in python to filter the URLs. This will give us the desired URL data-set values to train the model and test it. The data-set will have two column structure one for URLs and other for labels (malicious or not).

Then we used Tf-idf machine learning text feature extraction approach from the sklearn python module. Before that we need to read the data-sets into data frames and matrix which can be understood by the vectorizer we prepared and later pass onto the term-frequency and inverse document frequency text extraction approach. We used pandas module in python for that task. As stated above we used logistic regression method to train our model but before that we passed the data to our custom vectorizer function using Tf-idf approach and after that we can train and test our ML model.

Still the model was not able to predict all the good URLs and hence club good URLs with bad URLs so we used the classical method of URL filtering with conjunction to the machine learning model i.e., Whitelist Filter. It is the list of websites that we know are good and at-least non-malicious and won’t harm our users. So, we allow these particular websites through our internet traffic, the opposite is called as blacklisting. It’s a very simple but efficient approach to segregate our network traffic, similarly we implemented that in our machine learning model.

#Performance Analysis

* The Accuracy percentage of Random Forest Classifier: 99.37%
* The Accuracy of Logistic Regression: 98.46%
* The Precision of Logistic Regression: 99.18%
* The Recall of Logistic Regression: 96.25%

#Future Enhancement

* Use a wider, well-labelled dataset.
* Instead of only hosting it in our local system, we can upload it in the web and provide the feature of uploading files to be checked and also create a section for URL detector.
* GUI based program can be made for windows, as of now it is only made for terminal.
* Real time scanning of every file while downloading/transferring can be done to be used in daily life scenario to detect malicious files.

Steps to Use the Product

First you need to clone this repo, you can do this using

`git clone https://github.com/Kiinitix/Malware-Detection-using-Machine-learning.git`

After clone this repo, open the terminal in that location and install all the dependencies of the project using,

`pip install -r requirement.text`

Now you can use the project in your local machine, if you wish to make any changes in the repo then you first need to make a new branch and switch to that new branch using

`git branch new-branch`
`git checkout new-branch`
After changing your current branch, make change locally and then add all those changes in your branch and then fianlly commit

git add .
git commit -m "<comment>"
After successfully commiting the changes you need to push the code using,

`git push --set-upstream origin new-branch`
After pushing the changes you are now good to send the pull request and after evaluation we can commit it in the main-branch.

# To start the Tool

`Python3 main.py` then you can run the tool

# Product Features

* Malicious File Detection
* Malicious URL Detection

Thank for your Reading....


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



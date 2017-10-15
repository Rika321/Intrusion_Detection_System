Machine Learning for Network Intrusion Detection
He Qu
Fall 2017 SPIN Intern
Undergraduate Student
Computer Science, Senior
                                            Mentor: Volodymyr Kindratenko



1. Background
As networked systems become more and more pervasive and businesses continue to move more and more of their sensitive data online, the number and sophistication of cyber attacks and network security breaches has risen dramatically. Organizations are increasingly relying on network intrusion detection systems (NIDS) to monitor their network traffic and report suspicious behavior. 

2. Project Goal
Since network traffic packets usually consist of many important information like protocol types, durations, source bytes and destination bytes, I would like to apply some machine learning algorithms to classify the existed network traffic records. I will also build my own network intrusion detection system (NIDS) to detect and report suspicious packets based on my classifier predictions. After achieving certain threshold of accuracy, I will implement my NIDS method on an FPGA board or other external devices with the goal of optimizing the performance. 

3. Method and Design
Collection of data
Firstly, I plan to use data from The Third International Knowledge Discovery and Data Mining Tools Competition (KDD Cup ’99) [1]. The dataset is compiled by MIT’s Lincoln Laboratory at the behest of DARPA in 1998 [2]. For the KDD Cup ’99 subset, there are about 5M total network connections’ worth of training data, and a test set of about 319K connections. Although such dataset is no longer an accurate representation of network activity in most recent environment, it still serves a valuable role as a benchmark for training and comparison of my sample detection algorithms. After getting high accuracy by simple machine learning methods, such as Decision Trees, Random Forests or Support Vector Machine, I will begin to use dataset collected by NCSA security group and myself. 

Algorithm and Implementation
I plan to design and implement the following types of machine learning and deep learning algorithms to classify the dataset. My initial goal is to get both high prediction accuracy and precision. And since my dataset will contain diverse and accurate features and labels, I prefer to apply supervised learning method. First I will consider Support Vector Machine (SVM) method. 
An SVM is a discriminative classifier formally defined by a separating hyperplane. In other words, given labeled training data, the algorithm outputs an optimal hyperplane which categorizes new examples. I will also consider Decision trees and Random forests methods. They are both supervised approaches that model the decision boundary as leaves of a binary tree, with the interior nodes representing different features of the input connections ordered by their relative importance for classification. The strength of these two algorithm is that they can handle the dataset with rich features and mostly binary labels. The KDD Cup ‘99 dataset has these characteristics. I also plan to develop some more advanced deep learning methods such as multi-layer perceptrons. These methods should help to make prediction more accurate. 



4. Deliverables
By the end of next semester, the following will be produced:
A custom-made network intrusion detection system implementing one or more of the classification algorithms discussed in Section 3.
A dataset of sample network traffic that includes “normal” network traffic patterns and suspicious traffic. 

 
References
[1] KDD Cup 1999 Data, Kdd cup 1999 data, http://kdd.ics.uci.edu/databases/kddcup99/kddcup99.html, Web. Nov 2014.

[2] MIT Lincoln Laboratory: Communication Systems, Cyber Security: Cyber Systems, and Technology, Darpa intrusion detection evaluation, http://www.ll.mit.edu/mission/communications/cyber/CSTcorpora/ideval/data/1998data.html, Web. Nov 2014.

# SDS Autumn 2019, M2, Assignment 1
Daniel S. Hain (<dsh@business.aau.dk>) & Roman Jurowetzki (<roman@business.aau.dk>)
07/10/2019

# Introduction

In your first assignment in M2, you will replicate a well known network analysis, with different data and some twists. The data is to be found [HERE](https://github.com/SDS-AAU/M2-2019/tree/master/notebooks/assignments/assignment_1/data)
# Data: What do I get?

## Background

Let the fun begin. You will analyze network datacollected from the managers of a high-tec company. This dataset, originating from the paper below, is widely used in research on organizational networks. Time to give it a shot as well.

[Krackhardt D. (1987). Cognitive social structures. Social Networks, 9, 104-134.](https://www.andrew.cmu.edu/user/krack/documents/pubs/1987/1987%20Cognitive%20Social%20Structures.pdf)

The company manufactured high-tech equipment on the west coast of the United States and had just over 100 employees with 21 managers. Each manager was asked to whom do you go to for advice and who is your friend, to whom do you report was taken from company documents. 

## Description

The dataset includes 4 files - 3xKrack-High-Tec and 1x High-Tec-Attributes.

**Krack-High-Tec** includes the following three 21x21 text matrices: 

* ADVICE non-symmetric, binary
* FRIENDSHIP non-symmetric, binary
* REPORTS_TO non-symmetric, binary

Column 1 contains the ID of the **ego** (from wehere the edge starts), and column 3 the **alter** (to which the edge goes). Column 3 indicates the presence (=1) or absence (=0) of an edge.

**High-Tec-Attributes** includes one 21x4 valued matrix.

* ID: Numeric ID of the manager
* AGE: The managers age (in years)
* TENURE:	The length of service or tenure (in years)
* LEVEL: The level in the corporate hierarchy (coded 1,2 and 3; 1 = CEO, 2 = Vice President, 3 = manager)
* DEPT: The department (coded 1,2,3,4 with the CEO in department 0, ie not in a department)

# Instructions: What shall I do?

## 1. Create a network

* Generate network objects for the companies organizational structure (reports to), friendship, advice
* This networks are generated from the corresponding edgelists
* Also attach node characteristics from the corresponding nodelist

## Analysis

Make a little analysis on:

### Network level characteristics

Find the overal network level of..

* Density
* Transistivity (Clustering Coefficient)
* Reciprocity

... for the different networks. Interpret the results. Answer questions such as: Are relationships like friendship and advice giving usually reciprocal? Are friends of your friends also your friends?

### Node level characteristics

Likewise, find out who is most popular in the networks. Who is the most wanted friend, and advice giver? And: Are managers in higher hirarchy more popular?

### Relational Characteristics

Are managers from the same department, or on the same hirarchy, age, or tenuere more likely to become friends or give each others advice?

### Aggregated Networks

Reconstruct the advice and friendship network on the level of departments, where nodes represent departments and edges the number of cross departmental friendships/advice relationships.

## Visualization

Everything goes. Show us some pretty and informative plots. Choose what to plot, and how, on your own. Interpret the results and share some cool insights.


# Deliverables

Please submit a PDF or HTML version of your notebook on peergrade.io. In adittion, include a link to a functioning goocle colab notebook included. Please make sure(eg. own test in “anonymous” setting in your browser) that otherscan acess it.

This notebook should:

* It should solve the questions in an straightforward and elegant way.
* It should contain enough explanations to enable your fellow students (or others on a similar level of knowledge) to clearly understand what you are doing, why, what is the outcome, how to interpret it, and how to reconstruct the exercise. Be specific and understandable, but brief.

# Further process and dates

* You will receive an upload link on peergrade.io by XX.10.209 morning with concrete instructions.
* The notebook upload is also due 10.10.2018, 11:55pm. Delays are not accepted.
* On latest 11.10.2018, you will recieve an invitation to peergrade your fellows exams on peergrade.io. You will be asked for the evaluation of 3 peer-assignments is part of the assignment and mandatory.
* The peergrade evaluation is due XX.10.2019, 11:55pm. Delays are not accepted.

# Evaluation

* Supervised peer-evaluation.
* Evaluation by 3 peer-reviewers
*

# Hints

General

* Keep in mind, you are looking in all cases at directed and unweighted networks.

R 

* Use `fread` from the `data.table` package to conveniently read the files



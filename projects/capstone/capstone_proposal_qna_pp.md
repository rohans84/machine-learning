# Machine Learning Engineer Nanodegree
## Capstone Proposal
Rohan Shah  
November 27th, 2017

## Proposal

The objective of the capstone project is to build an NLP model that can perform information extraction from set of Policies and Procedures documents  and can provide answer to questions on the policies and procedures

The project aims to build a Q&A system that can take input questions related to the given policies & procedures set, perform information extraction from the indexed P&P documents and provide appropriate and correct answers for the questions. For this, the project will be using a sample set for the medical industry provided by **Physicians Medical Group of San Jose, Inc** available here - http://www.pmgmd.com/wp-content/uploads/2014/08/sample_office_policy_and_procedures.pdf

This project will be referring only to this provided P&P document to perform the task of information extraction. 

### Domain Background

[BusinessDictionary.com](http://www.businessdictionary.com) defines Policies and Procedures as:

> A set of policies are principles, rules, and guidelines formulated or adopted by an organization to reach its long-term goals and typically published in a booklet or other form that is widely accessible.

> Policies and procedures are designed to influence and determine all major decisions and actions, and all activities take place within the boundaries set by them. Procedures are the specific methods employed to express policies in action in day-to-day operations of the organization.

> Together, policies and procedures ensure that a point of view held by the governing body of an organization is translated into steps that result in an outcome compatible with that view.

from:  http://www.businessdictionary.com/definition/policies-and-procedures.html

Thus, it can be clearly understood that the P&P documents serve as a very critical framework for organizations to run smoothly. They are necessitated not just by business goals but in many cases also are required to be adhered to by Federal, State & local level laws.

### Problem Statement

Every organization needs to ensure that its policies and procedures are followed in letter and in spirit. With employee attrition, frequent changes in laws & regulations, increased media scrutiny and presence of active social media, it is imperative for organizations to ensure that their employees / members have clear understanding of their policies and procedures. They need to ensure adequate trainings and understanding of these policies. However, it becomes too complex for the employees to keep up with them and thus need a clear and intuitive way to grasp them.

The project aims to build an NLP model that can parse through the provided document, get trained on a subset of policies and procedures and provide an interface to allow clients to ask questions on the entire set of those documents. The model should be effective in answering the questions by performing the relevant information extraction task. 

The P&P document used for this project is an example provided by [Physicians Medical Group of San Jose, Inc](http://www.pmgmd.com/wp-content/uploads/2014/08/sample_office_policy_and_procedures.pdf). 

Through this system, member of the medical staff having queries on policies and procedures can get the required answers. This will avoid the need to go through pages of documents to perform their daily tasks.

### Datasets and Inputs

The dataset for this project is basically a textual version of a sample P&P document provided by [Physicians Medical Group of San Jose, Inc](http://www.pmgmd.com/wp-content/uploads/2014/08/sample_office_policy_and_procedures.pdf).

This document has policies and procedures for a medical clinic / office that talks about performing activities like:
1. Facility Standards
1. Emergency plans
1. Office Procedures
1. Medical Records
1. Infection Control
1. Pharmaceuticals
1. ...

The data will be converted into a text corpus using NLTK library (a python library for Natural Language Processing)

A subset of the corpus will be tagged by hand to setup training data for parts of speech tagging, for Named Entity extraction and for relationship extraction.

### Solution Statement

The NLP model for this project will be developed using Python programming language and will make use of the [NLTK library](http://www.nltk.org/). Standard NLP preprocessing tasks like tokenization of words, POS tagging will be performed. Model for Named Entity extraction and for relationship between entities and tasks will be developed using Supervised learning - 

* Perform tokenization of corpus and segmentation of sections, sentences 
* Perform POS tagging
* Identify set of relevant name entities used in the corpus
* Identify set of relations to be extracted (actions / tasks performed by named entities)
* Hand Label / use a regular expression pattern to identify the named entities in the training set
* Hand label the relations between the entities and also actions / tasks to be performed by those named entities
* Break the corpus into training, development and test set
* Train a classifier on the training set

### Benchmark Model
_(approximately 1-2 paragraphs)_

In this section, provide the details for a benchmark model or result that relates to the domain, problem statement, and intended solution. Ideally, the benchmark model or result contextualizes existing methods or known information in the domain and problem given, which could then be objectively compared to the solution. Describe how the benchmark model or result is measurable (can be measured by some metric and clearly observed) with thorough detail.

### Evaluation Metrics
_(approx. 1-2 paragraphs)_

In this section, propose at least one evaluation metric that can be used to quantify the performance of both the benchmark model and the solution model. The evaluation metric(s) you propose should be appropriate given the context of the data, the problem statement, and the intended solution. Describe how the evaluation metric(s) are derived and provide an example of their mathematical representations (if applicable). Complex evaluation metrics should be clearly defined and quantifiable (can be expressed in mathematical or logical terms).

### Project Design
_(approx. 1 page)_

In this final section, summarize a theoretical workflow for approaching a solution given the problem. Provide thorough discussion for what strategies you may consider employing, what analysis of the data might be required before being used, or which algorithms will be considered for your implementation. The workflow and discussion that you provide should align with the qualities of the previous sections. Additionally, you are encouraged to include small visualizations, pseudocode, or diagrams to aid in describing the project design, but it is not required. The discussion should clearly outline your intended workflow of the capstone project.

-----------

**Before submitting your proposal, ask yourself. . .**

- Does the proposal you have written follow a well-organized structure similar to that of the project template?
- Is each section (particularly **Solution Statement** and **Project Design**) written in a clear, concise and specific fashion? Are there any ambiguous terms or phrases that need clarification?
- Would the intended audience of your project be able to understand your proposal?
- Have you properly proofread your proposal to assure there are minimal grammatical and spelling mistakes?
- Are all the resources used for this project correctly cited and referenced?

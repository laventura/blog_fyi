---
title: On Learning Deep Learning
author: Atul Acharya
date: '2016-03-01'
slug: on-learning-deep-learning
description: How to learn deeply about deep learning
categories:
  - Deep Learning
tags:
  - Deep Learning
  - Machine Learning
---

I'm often asked about how to go learning about machine learning, deep learning and artificial intelligence (AI). This post is a (constantly updated) list of resources that _I_ have found useful. Your mileage _will vary_ by your own experience, background, motivation and expertise. I do hope you will find this useful though.

---
### My Interests

When I first dipped my toes in machine learning (early 2000s) as a technical architect, the sector was small, and full of technical mumbo-jumbo; the "experts" loved to keep it that way. It turned me off, and I pursued other areas.

Later in 2010-2012, I renewed my interest and found _machine learning_ somewhat changed, updated, and scrubbed. As my own work focused more on analytics, I enjoyed understanding _natural language processing_, _recommendation systems_, and their practical applications. However, large scale use cases were few and far between among the technology leaders and academic labs.

In the modern era (c. 2014 onwards), as academic researchers lead one breakthrough after another in _deep learning_, and tech leaders brought these latest ideas to market, there has been a renaissance in both research and applications of machine learning, deep learning, and AI.

My view of AI is that _artificial intelligence is an augmentation tool for humans._ As such, I am completely fascinated by **applied AI, deep learning**. I like and understand the theories; however, I am more enamored by _practical use cases of deep learning_.

---

### Approach

I use a combination of projects, books, online learning, and offline events and workshops to go deep (_no pun_). Here are some of my favorite resources.

# Books

*1.* [_Python Machine Learning_](https://www.packtpub.com/big-data-and-business-intelligence/python-machine-learning-second-edition) by Sebastian Raschka [Review: ★★★★✯]

<blockquote>
Very readable, expects familiarity with linear algebra, calculus and Python. Very hands-on! Most algorithms are implemented from scratch. If you want to learn fundamentals, with good hands-on practice, this book is excellent. This book is about _machine learning_ though, not deep learning per se.
</blockquote>


*2.* [_Hands-on Machine Learning with TensorFlow and Scikit Learn_](http://shop.oreilly.com/product/0636920052289.do) by Aurélien Geron [Review: ★★★★✯]

<blockquote>

This is another excellent book for both machine learning and basics of deep learning. It is a slightly dense, though very readable. It goes from basics of machine learning using both scikit learn and TensorFlow framework. As such, this book is meant to be read hands-on. You really need to go through the Jupyter notebook tutorials to understand the implementations fully (and that is my chief gripe, although a minor one). Recommended! 

</blockquote>

*3.* [_Deep Learning with Python_](https://www.manning.com/books/deep-learning-with-python?a_aid=keras&a_bid=76564dff) by François Chollet [Review: ★★★★★]

<blockquote>

Written by the creator of the deep learning framework [Keras](https://keras.io), this is a highly readable book on deep learning. I like this one because my own philosophy matches very closely with that of François; like him, I believe deep learning should be made easy, jargon-free, and accessible to all, including non-PhD practitioners. Keras is a high-level framework on top of other (lower level) frameworks like TensorFlow, Cognitive Toolkit (CNTK), Theano (now no longer in development). It makes development of deep learning projecs _very easy_. This book is largely jargon-free, hype-free and math-free. It goes over projects you can easily implement on your own laptop (and optionally in the cloud), with difficulty going from easy to hard.
I'd highly recommend this book to anyone starting their deep learning journey!
(If you're reading this, François - thank you and allow me to buy you a beer or coffee and talk AI stuff. 👍 )

</blockquote>

*4.* [_Deep Learning_](http://www.deeplearningbook.org/) by Ian Goodfellow, Yoshua Bengio, and Aaron Courville [Review: ★★★★✯]

<blockquote>

This book, by three well known researchers in the deep learning community, is _the classic reference_ for deep learning! It is highly mathematical, very thorough on all the basics - linear algebra, calculus, optimization, machine learning algorithms, deep learning techniques, and more. It is exhaustive. It is also highly theoretical. It is a great book for reference, when you need to understand some pesky detail from the ground up. It is _not_ a book you would use for tinkering with projects or implementing something out of the box (your mileage will vary, of course).
I only rate it 4.5/5 stars because this book can be daunting (it is to me) with highly detailed (and sometimes scary) math symbols. If math is not for you, I'd skip this book until you get comfortable with some practice.  I'd recommend this book for reference though (which is how I use it).

</blockquote>

*5.* [_Neural Networks and Deep Learning_](http://neuralnetworksanddeeplearning.com/) by Michael Nielsen [Review: ★★★★✯]

<blockquote>

This book by Michael Nielsen is a free, online book, and one of the first ones I read as it was under development. Michael graciously shared his writing and ideas online, and this book reflects the great care with which it is written. His exposition is clear, figures are excellent. His book offers a clear, principled and hands-on approach to understanding and implementing neural networks. It does assume familiarity with both (elementary) calculus and linear algebra as well as Python, but the reader is rewarded with clear explanations that few other books offer. One of the clearest examples Michael offers is how to implement a simple neural network that classifies hand-written digits from the MNIST dataset. It also offers one of the best explanations of the Backpropagation algorithm, fundamental to implementing neural networks (although the math is slightly intimidating).

If you are a beginner, I'd highly recommend this book. My one minor complaint is that it doesn't offer nearly enough in the latest research in deep learning. That's how much I like it. Go check it out!

</blockquote>


# Online Courses

The following courses reviewed are those I have personally completed; I've noted where this is not the case. 

*1.* [_Introduction to Deep Learning_](https://www.udacity.com/course/deep-learning--ud730) at Udacity, by Google [Review: ★★★★✯]

This course, developed by Google (Vincent Vanhoucke) is a great hands-on introduction to deep learning. And it is free on Udacity. It is most useful if you _already_ know some machine learning fundamentals, Python, and some linear algebra and calculus. It offers a great overview of Google's TensorFlow library. The course goes from basics of machine learning (linear regression, logistic regression), to more advanced material such as convolutional neural networks (CNN) and recurrent neural networks (RNN). It gives you enough to understand these at a high-level, though you can dig deeper (_no pun_) in the projects. However, the course itself does not go very deep into each separate topic. 

Recommended to any beginner or intermediate learner. 

*2.* [_Deep Learning Specialization_](https://www.deeplearning.ai/) - by Andrew Ng at Coursera [Review: ★★★★★]

If you were to start your learning today, this is the course I would recommend! Developed by Andrew Ng, whose first course _Machine Learning_ on Coursera launched a thousand learners, this is a **new, 5-course** specialization that was launched in August 2017. The specialization offers _five_ courses, each lasting anywhere from 2 to 7 weeks, and each goes deep(er) into specific topics. You can complete just one of these course, though I would recommend completing the entire specialization as it is very enriching. 

_I might do a separate review of these courses, but here's a brief review._

* **Neural Networks and Deep Learning** - covers basics of neural networks and deep networks.
* **Improving Deep Neural Networks** - helps understand how to tune hyperparameters for neural networks in the real word. 
* **Structured Machine Learning Projects** - perhaps the only course that looks at the _big picture_ of ML projects. Very good. 
* **Convolutional Neural Networks** - one of the best explanations of CNNs anywhere. Requires working through math but it is very enriching. Offers excellent projects - e.g. neural style transfer, image classification, semantic segmentation and more.
* **Sequence Models** - great insights into sequence modeling for applications like, machine translation, time series analyses, speech recognition, and more. 

The course are demanding; each requires working on projects in Jupyter Notebooks in the cloud (hosted on Coursera's infrastructure), but without the hassle of rolling your compute in the cloud. That alone is highly productive for the beginner. It does require understanding the math, which can be quite tricky, but Andrew Ng's explanations are excellent and highly detailed (though some times one can get lost in the details).

I may be biased in recommending this specialization; _I'm a course mentor_, and I enjoy helping others learn. But this is one of the more comprehensive courses around. Highly recommended to anyone - beginner or intermediate.

*3.* [_Machine Learning Specialization_](https://www.coursera.org/specializations/machine-learning) - by University of Washington at Coursera [Review: ★★★★✯]

A **4-course** specialization offered by UW's Carlos Guestrin and Emily Fox. This is a highly technical and **excellent** deep dive into machine learning. Guestrin and Fox's teaching style is highly engaging and their dedication shows in these courses. The material is very thorough, though sometimes the math can be intimidating. They use the open-source GraphLab library, developed by [Turi](https://turi.com/), for project work (although you could also use the more standard scikit learn library). [Fun fact: Carlos Guestrin was a co-founder of Turi (nee Dato), which was acquired by Apple, and Turi is officially supported by Apple.]

While the  mini-projects are interesting and useful, I thought some of these projects were much smaller in content and could have had more meat on the bone, so to say. Regardless, the content (and slides) are excellent.

It took me longer than my usual to complete this specialization, as I was in the middle of completing my Self-Driving Car Nanodegree. However, I enjoyed the course. 
Recommended to a committed beginner. 


*4.* [_Deep Learning Foundations Nanodegree_](https://www.udacity.com/course/deep-learning-nanodegree--nd101) - at Udacity 

I have not officially taken this Nanodegree, though I have completed several of the modules in it. If that's any experience to go by, I'd recommend this Nanodegree to anyone who's starting their learning journey. 

This is ideally meant as a first course in deep learning, and gives a great overview of basics of machine learning, convolutional neural networks (CNNs), and recurrent (RNNs). The style of teaching is excellent, though the best learning materials are the projects which are the hallmark of Udacity.

Recommended to any beginner.

*5.* [_Practical Deep Learning for Coders_](http://www.fast.ai/) [Review: ★★★★✯]

Developed by Jeremy Howard and Rachel Thomas, this really is a set of two courses - one (Part 1) more basic, other (Part 2) more advanced. 

What differentiates them from all others is their focus on developers, and their style of teaching. As they've [written elsewhere] (http://www.fast.ai/2016/10/08/overview/), Jeremy and Rachel teach you how to drive a car without first teaching you the basics of internal combustion engine. This style works best for hands-on coders, developers, and hackers who want to get dirty with the code without (necessarily) understanding the _whys_ of the underlying library. Jeremy and Rachel developed their own library/framework (fast.ai) that sits on top of [PyTorch] (http://pytorch.org/) (the other up-and-coming framework for deep learning). They show you _how_ to use the fast.ai library, and implement deep learning first, without diving too deep into the mechanics of mathematics, calculus, linear algebra and such. This can be both great (if you're impatient), and not-so-great (if you're curious about the mechanics of algorithms and the explanations).

My experience with Fast.ai was both. I enjoyed the speed, but I also craved the logical explanations (which, thankfully, I had learned elsewhere). 

I would recommend this to hacker-types and developers in a hurry. Come for the projects, stay for the latest in deep learning.

I'm looking forward to taking the [Cutting Edge Deep Learning for Coders - Part 2] (http://course.fast.ai/part2.html)


_More to come..._

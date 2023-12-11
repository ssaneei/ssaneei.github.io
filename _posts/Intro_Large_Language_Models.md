---
layout: post
title: New to Large Language Model?
tags: [Summaries]
---

<p>Hello! 
I am back from my holidays in South Africa!! AND it is my first day at work! <3
Today, I came across with this video by Andrej Karpathy. In this video, he is trying to introduce LLMs. The talk is for about an hour and in the end of it, you will have a good understanding of these models. <p>
<ul>
  <li>He starts with Llama 2 70B to define LLMs to a busy person! So you won't need any pre-requisits.</li>
  <li>He continues with what a neural network is doing: predicting the next word in the sequence. Then he introduce the pre-training (first stage of training) in which he describes documents of Internet as the source of this step. </li>
  <li>In the next step, he tries to explain the fine-tuning (second stage of training) to train the assistant. He mentions that we don't need a document generator as it's not of a great help, though we want to be able to give questions to a model and being provided with the answers. Here, again the task is the next word generation task but we will swap the dataset on which we are training. </li>
  <li>In the pre-training step, the corpus/dataset was Internet documents, here we need a dataset so we hire people to make these datasets: to collect questions and answers.</li>
  <li></li>
  
  <li>Here I list the sentenses that he uses that is interesting to me:</li>
    <ul>
      <li><i>There is a very close relation between prediction and compression.</i></li>
      <li>Next word prediction forces the neural network to learn a lot about the world.</li>
      <li>Think of LLMs mostly as inscrutable artifacts, they're not like any products built as in an engineering discipline, they're not like a car in which we sort of understand all the parts. They are these neural nets that come from a long process of optimization and so we don't currently understand how they work although there's a field called interpretability or mechanistic interpretability which tries to go deeper and figuer out what all the parts of these neural nets are doing. Right now, it's feasible to some extent but not fully.</li>
      <li>In the pre-trainig, we prefer quantity to quality but in the second stage, the fine tuning, we would like to have quality in our dataset and quantity is not of the same importance.</li>
      
    </ul>
    
  <li></li>
  <li></li>
  <li></li>

  <li><a href="https://aclanthology.org/2020.acl-main.463.pdf">Climbing towards NLU: On Meaning, Form, and Understanding in the Age of Data</a></li>
</ul>
</p>

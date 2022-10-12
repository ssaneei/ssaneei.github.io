---
layout: post
title: Summaries on Inception Loop article
tags: [Summaries]
---

<p>Hey there! Today I want to write about the article I want to work on these days. The name is "Inception loops discover what excites neurons most using deep predictive models".
As I'm not that expert in the Neuroscience field, the explanations could be sometimes basic or redundant and sometimes more than the article itself. :)) I'll add the notes that I have for myself as "exp"s (abbr. explantions). </p>

<p>So the main goal in this article is to dissect the neural mechanism of sensation and to understand the information processing in the brain, they want to find the stimuli that optimally drive neurons.</p>
<p>In linear systems, linear filters elicit responses optimally. 
Linear Nonlinear (LN) Models with center-surround filters have high predictive power in the retina and drive its activity.</p>
exp: what is center-surround filter?
You can see it here:
<img src="https://www.mdpi.com/jimaging/jimaging-08-00076/article_deploy/html/images/jimaging-08-00076-g004.png">
<p>BUT the thing is the response selectivity of lots of cortical neurons is inherently nonlinear 
And even in V1, the predictive power of LN or energy models is low, specially for the responses to natural stimuli.</p>
<p>exp: V1 means Primary Visual Cortex. The primary visual cortex is the last “generalized” processing region of the visual pathway and thus the most downstream area that is considered for implantation with visual prostheses.
(Prostheses for the Brain, 2021)</p>
<p>exp: In classical conditioning, a <b>neutral stimulus</b> is something that does not elicit a response.</p>

<p>Since the high-dimensional space of possible images seems out of control, it'd be difficult to identify optimal sensory input
for neurons with nonlinear sensitivity.</p>
<p>
To managethis high-dim space, there are these solutions:
<ol> 
 <li>The active learning approach</li>
  Negative point: 
  <ol>
    <li>Experimental constraints limit the number of responses that we expect to measure from a single cell,</li>
    <li>The dimensionality of the stimilus space would be restricted.</li>
  </ol>

 <li> The model-driven stimulus optimization</li>
    which requires functional models predicting the responses of the neurons to arbitrary stimuli, including natural images.
    Doing so, neither of the two negative points of the first suggestion happens.

 <li>Deep learning-based models</li>
    They set new standards in predicting of the cortical responses to natural images.
 </ol>
</p>

<p>This article worked on the third solution meaning Deep learning-based models, with end-to-end training to synthesize and search
for optimal stimuli in silico that verified back in the brain</p>
exp: Types of experiments:

<ul>
  <li>In silico:  (in silicon) Using/in the computers</li>
  <li>In vitro:   (in glass) Outside living organism (in a petri dish)</li>
  <li>Ex vivo:    outside of a living body </li>
  <li>In vivo:    (not in vitro) inside whole living organism</li>
</ul>

<p>Method:

   They designed a closed-loop experimental paradigm which they call an inception loop. This loop combines in vivo recordings
   with in silico modeling to synthesize stimuli that evoke a desired response. (that they confirm in vivo)</p>
  <img src="_img/a1.jpg">
  <p>
   The inception loop experiment was held in days:
   on day 1:
   <ul>
     <li>Recorded the neural responses of large neuronal population to 1000s of natural images.</li>
     <li>Trained a CNN (Convolutional Neural Network) to predict these responses based on the presented images.</li>
     <li>Optimized images to maximize the model responses of selected model neurons.</li>
   </ul>

   over subsequent days
    <ul>
     <li>Presented the tailored images to corresponding neurons in the brain to test whether they indeed produced the
     strongest responses among all control stimuli.</li>
     They recorded the responses to natural images of over 2000 excitory neurons in layer 2/3 of the V1 (V1 L2/3)
     <li>Trained a CNN (Convolutional Neural Network) to predict these responses based on the presented images.</li>
     <li>Optimized images to maximize the model responses of selected model neurons.</li>
   </ul>
   </p>

<p></p>
<p></p>
<p></p>


<!-- Source:

```markdown
- [x] Eating
- [ ] Walking
  - [ ] Running
- [ ] Sleeping
```

Rendered:

- [x] Eating
- [ ] Walking
  - [ ] Running
- [ ] Sleeping -->

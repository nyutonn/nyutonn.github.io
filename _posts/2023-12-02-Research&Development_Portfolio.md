---
layout: post
title: Research and Development Portfolio
date: 2023-12-02 22:00:00 +0900

# subtitle: I'm a member of Tohoku NLP Group.
thumbnail-img: /assets/img/erica.png
# cover-img: /assets/img/milk.jpeg
# gh-repo: daattali/beautiful-jekyll
# gh-badge: [star, fork, follow]
# tags: [test]
comments: true
# author: Nakano Yuto
---

## hagi-bot

<img src="/assets/img/erica.png" width="300x300">

##### Overview
<img src="/assets/img/system_picture.png" width="800x400">

##### Abstract
This is a system submitted to the Sixth Dialogue System Live Competition. It is a task-oriented multi-modal dialogue system that integrates (1) response generation module and (2) avatar control module. Within the response generation module, we use LLM (GPT-4) to generate responses along with emotion and action labels considering the dialogue history and the topics to be discussed. Specifically, by monitoring the dialogue state through slot filling and continuously changing prompts based on the situation, the module achieves a natural dialogue progression. The avatar control module enables human-like natural behavior by operating voice (pitch, volume, and speaking speed), facial expressions, and gestures. These operations are based on predefined rules designed in reference to models such as Russell’s Circumplex Model of Affect, corresponding to the content of speech together with emotion and action labels. The combination of these two modules achieves the generation of responses appropriate to the situation and natural behaviors based on the content of utterances and emotions. This system won the first place in the preliminary round.

The dialogue system is [available](https://github.com/cl-tohoku/hagi-bot)

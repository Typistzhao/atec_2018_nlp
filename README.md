# Welcome to the atec_2018_nlp
official websit is [https://dc.cloud.alipay.com/index#/topic/intro?id=3](atec)
I did some clean up, but the code is exactly what I submitted in the competition!
Only one type of model used, with different input(word embedding and char embedding)
you should be able to get >0.623 locally with 0.05 VP for ensemble.


* the data was for season1 only(for some security reason, season2 data can not be shared)

* to run the char model(avg score:0.5729852440408627,prd_thr:0.21000000000000002):

    `python model.py -m train_model -ms "ELMOEM128_CHAR"`

* to run the word model:(avg score:0.5582690659811482,prd_thr:0.18000000000000002)

    `python model.py -m train_model -ms "ELMOEM128"`

* to run ensemble:

    `python model.py -m train_model -ms "ELMOEM128_21,ELMOEM128_CHAR_21"`

* to debug:

    `python model.py -m train_model -ms "ELMOEM128_CHAR"` -d

* with different validation size:

    `python model.py -m train_model -ms "ELMOEM128_CHAR"` -vp 0.05

# I do read lots papers, but only one was really used for my code(ELMO)
[Deep contextualized word representations](https://arxiv.org/abs/1802.05365)

[UWB at SemEval-2016 Task 1: Semantic Textual Similarity using Lexical,
Syntactic, and Semantic Information](http://www.aclweb.org/anthology/S16-1089)

[Injecting Relational Structural Representation in Neural Networks
for Question Similarit](https://arxiv.org/pdf/1806.08009.pdf)

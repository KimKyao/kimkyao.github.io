---
title:  "[DL][기초] Attention Mechanism" 

categories:
  - dl

toc: true
toc_sticky: true

date: 2023-07-13
last_modified_at: 2023-07-13
---

Attention이 처음 나오게 된 것은, many to many 중 '기계 번역' task를 더 잘 풀기 위함이였습니다. Attention을 Sparse하게 가져갈 것인지, Hard에게 가져갈 것인지에 따라 모델이 또 다르고, Attention을 이미지에 적용할 수도, 그래프에 적용할 수도 있습니다. 어텐션을 잘 활용하게 되면 Recurrent-based model을 사용하지 않아도 괜찮지 않겠냐는, Transformer 모델 또한 널리 쓰이고 있습니다. 또한, softmax를 주로 활용하기 때문에 softmax에 대해서도 깊게 살펴볼 필요가 있습니다.


NLP의 기존 모델 seq2seq에서는 인코더가 입력 시퀀스를 context vector로 압축하고, 디코더는 이 벡터를 통해서 출력 시퀀스를 만들어 냅니다.

<br>

    개인 공부 기록용 블로그입니다.
    틀린 부분이 있을 수 있습니다. :)

[맨 위로 이동하기](#){: .btn .btn--primary }{: .align-right}
---
title: "BERT 논문 요약"
date: 2019-02-11 21:55:00 -0400
categories: BERT LanguageModel DeepLearning
---

## BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding

2018년 10월 Google에서 공개한 인공지능 언어모델인 BERT의 논문을 요약 및 리뷰하려 합니다.

큰 뱡항은 [BERT 개발팀이 공유한 논문][bert-paper]에 기반하고 있으며, [여러 다른][reference-01] [참고 사이트][reference-02]들의 도움도 많이 받았습니다.

##### Abstract

최근에 다루어지는 언어 표현 모델들과 달리 (Peters et al., 2018, Radford et al., 2018) BERT는 pre-train된 deep bidirectional 표현 모델입니다. BERT는 모든 계층에서 왼쪽과 오른쪽 양방향의 Context 모두를 조정하며 학습합니다.

다음은 [논문][bert-paper]에서 가져온 pre-training model들의 구조를 비교한 그림입니다.

![bert_f1](./img/bert_fig01.png)

그림 1 : 사전 교육 모델 아키텍처의 차이점. BERT는 양방향 Transformer를 사용합니다. OpenAI GPT는 왼쪽에서 오른쪽으로 변압기를 사용합니다. ELMo는 독립적으로 훈련 된 왼쪽에서 오른쪽 및 오른쪽에서 왼쪽으로 연결되는 LSTM의 연결을 사용하여 다운 스트림 작업을위한 기능을 생성합니다. 세 가지 중에서, BERT 표현 만이 모든 계층의 왼쪽 및 오른쪽 컨텍스트 모두에 공동으로 조건이 지정됩니다.

이 절에서는 BERT와 그 세부 구현을 소개합니다. 먼저 모델 아키텍처와 BERT에 대한 입력 표현을 다룹니다. 그런 다음 3.3 절에서 본 백서의 핵심 혁신 인 사전 교육 과제를 소개합니다. 예비 훈련 절차 및 미세 조정 절차는 각각 3.4 절과 3.5 절에 자세히 설명되어 있습니다.
마지막으로, BERT와 OpenAI GPT의 차이점은 3.6 절에서 논의됩니다.





[bert-paper]: https://arxiv.org/abs/1810.04805
[reference-01]: https://medium.com/ai-networkkr/%EC%B5%9C%EC%B2%A8%EB%8B%A8-%EC%9D%B8%EA%B3%B5%EC%A7%80%EB%8A%A5-%EC%86%94%EB%A3%A8%EC%85%98%EB%93%A4-1-%EA%B5%AC%EA%B8%80-bert-%EC%9D%B8%EA%B0%84%EB%B3%B4%EB%8B%A4-%EC%96%B8%EC%96%B4%EB%A5%BC-%EB%8D%94-%EC%9E%98-%EC%9D%B4%ED%95%B4%ED%95%98%EB%8A%94-ai-%EB%AA%A8%EB%8D%B8-9704ebc016c4
[reference-02]: http://jalammar.github.io/illustrated-transformer/

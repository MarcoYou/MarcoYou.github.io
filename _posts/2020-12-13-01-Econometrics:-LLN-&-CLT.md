---
layout: post
toc: true
title: "01. Econometrics"
categories: Econometrics
tags: [LLN, CLT, sample, population]
math: true
author:
  - Marco You
[comment]: <> (mathjax inline > \\(...\\) )
[comment]: <> (mathjax block  > $$...$$   )
[comment]: <> <p align="center"> <img src="/image/file_name.png" alt="file_name" width="460" height="260"> </p>
---

Econometrics(계량경제학) 노트 제 1장.

## 1. Introduction

개인적으로 계량경제학을 경제학의 한 분야로 보기 보다는 통계학의 한 분야, 더 정확하게는 통계학의 경제학적 응용이라고 보고 있다. 이 노트에서 앞으로 다룰 모든 내용 또한 사실 주로 통계학이다. 다만 통계적 분석에 사용되는 데이터들이 경제 데이터들(따로 경제 데이터라는 종류가 존재하는것은 아니지만...)이기 때문에 통계해석이 필연적으로 경제적 현상을 설명하게 된다.

계량경제학에서 주료 사용되는 통계 툴은 Regression Analysis(회귀분석) 이다. 먼저 회귀분석이 무엇인지 알아보자면 그 역사는 Francis Galton 이라는 영국의 인류학자에 의해 시작됐다 (참고로 프란시스 갈튼은 진화론의 찰스 다윈의 사촌이다). 위키피디아에 따르면 갈튼이 콩들의 성장발현도와 그 콩들의 씨앗들의 크기 사이의 인과관계를 조사하면서 표를 작성하고 있었는데 씨앗들의 크기를 표시한 점들이 어느정도 **선형적인** 관계를 보인다는것을 발견하게 됐다. 곧 이어 그는 이 콩들의 (씨앗크기;성장발현도) 좌표들이 평균적인 씨앗크기와 평균적인 성장발현도를 이은 선의 위 또는 아래에 위치하는것을 발견하였고 이 현상을 **평균으로의 회귀(Regression toward mean)** 이라고 정의하면서 처음으로 회귀분석이라는 단어가 정의되게 되었다. 다른 글들에서 달튼이 아들과 아버지의 키를 조사하면서 처음 알게되었다거나 forearm과 신장 사이의 관계를 조사하면서 처음 알게되었다거나 하는것을 본 기억이 있는데 사실 결론은 같으므로 그냥 넘어가겠다.
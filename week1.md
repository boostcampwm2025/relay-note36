# Week1: 우리가 발견한 문제와 퀘스트 제안

## 🤔 토론 주제

### 1. 부스트캠프에서 1주차를 보내며 아쉬웠던 점

- 피어 피드백 시간에 뭘 이야기해야 할지 막막하다
- 구현에 집중하느라 CS 지식을 금방 잊는다
- 개인 회고를 제대로 하지 못한다
- 동료 코드 리뷰 시간이 부족하다

이런 문제들을 해결하기 위해, AI를 도구로 삼아보면 어떨까? 라는 아이디어가 나왔고, 다음과 같은 실천 퀘스트들을 기획하게 되었습니다.

---

## 🔍 조사 및 퀘스트 제안


### ✅ 1. 피어 세션 진행이 막막할 때: `AI가 짜준 피어 세션 일정표 따라 해보기`

### 배경
부스트캠프에서는 매일 어제의 미션을 돌아보고 동료들끼리 의견을 주고받을 수 있는 1시간의 피어 세션 시간이 주어집니다.

모두가 피어 세션을 통해 많은 것을 배워가고 싶은 의욕이 넘치지만, 막상 피어 세션을 진행하려고 하면 진행자를 정하는 것부터, 다양한 의견을 활발하게 주고받기 위한 말문을 열기가 쉽지 않은 것 같습니다. 


### 목적
따라서 LLM을 통해 그날의 미션 내용에 맞는 피어 세션 ‘일정’ 가이드라인을 만들고, 해당 가이드라인에 따라 피어 세션을 막힘 없이 진행해보는 것이 목적입니다.

### 달성 기준
- 사용하는 LLM 모델은 어떤 것이든 상관없습니다.

- 미션 내용을 AI에게 전달하기 전에, 먼저 스스로가 생각하는 부스트캠프에서 진행하는 ‘피어 피드백’의 진행 목적, 진행 시간, 참여자 모두의 정보를 프롬프트에 잘 정리합니다. 
- 스스로가 정리한 미션의 전반적인 내용과, 피어 세션에서 얻어가고 싶은 항목들을 구체적으로 전달합니다. ex) 코드 리뷰, 미션 해결 경험 공유 등등
- 원활한 피어 피드백의 진행을 위해 AI가 만들어준 가이드라인에 포함되어야 할 내용은 아래와 같습니다.
- 참여자들 중 진행자 1명이 선정되어야 합니다.
	- 간단한 스몰 토크 주제 선정을 통한 아이스브레이킹 타임이 있어야 합니다.
	- 피어 세션에서 얻어가고 싶은 항목들에 대한 이야기 시간이 있어야 합니다.
- 조금 더 체계적인 가이드라인이 필요하다면 일정을 분 단위로 세워서 1시간 내로 끝내게 할 수도 있습니다.


---

### ✅ 2. CS 지식 복습: `공부한 내용을 생성형 AI의 퀴즈로 복습하기`

### 배경
열심히 새로운 CS 지식을 공부해도 다음 날이면 잊어버리는 부분이 많아서 아쉬웠습니다.

실제로 `에빙하우스의 망각곡선`이라는 시간이 지나면 얼마나 잊는지에 대한 그래프가 있습니다.
이론에 따르면, 어떤 내용을 학습한 뒤 24시간이 지나면 33%만이 기억에 남는다고 합니다. 하지만 한 번 학습한 것을 다시 학습하면 망각 속도가 점점 느려지고 장기기억으로 남는 양도 많아진다고 합니다.

복습으로 가장 효과적인 방법은 `문제 풀기`라고 생각합니다. 정리한 내용을 단순히 다시 읽는 것보다는, 정답을 떠올리기 위해 애쓰는 과정이 효과적입니다.

하지만 학습정리.md를 쓸 시간도 부족하기 때문에, 직접 퀴즈를 만들 시간이 없습니다. 그렇다면 ‘퀴즈 생성 프롬프트’를 이용하고, 학습정리.md 파일과 README.md 파일을 복붙하면 편하지 않을까요?

### 목적
이미 공부했던 `CS 지식`을 오래 기억하기 위해, **생성형 AI**를 이용해서 간편하게 **퀴즈**를 만들어 복습한다.


### 달성 기준
- `퀴즈 생성 프롬프트`를 작성한다.
- 프롬프트에 필수적으로 들어가야 하는 내용: `문제 수`, `난이도`, `문제 유형`(객관식 4지선다, 객관식 5지선다, 단답형, 서술형 등), **그 외 자유**
- 프롬프트 - 문제 수: 최소 3문제 이상
- `학습정리.md` 파일 또는 `README.md` 파일은 원본 그대로 **복사/붙여넣기**해서 전달한다. (gist에서 파일의 ‘RAW’버튼 눌러서 전체복사하면 편한 것 같아요)
- 프롬프트를 생성형AI에게 전달해서 **퀴즈를 만들고 풀어본 뒤**, 내 답과 정답을 비교해본다.


---

### ✅ 3. 개인 회고 실천: `AI 회고 템플릿으로 주 2회 이상 회고하기`

### 배경
미션 해결에 많은 시간을 소모하면서 개인 회고를 충분히 하지 못한 점이 아쉬움으로 남았습니다. 이를 보완하기 위해 AI를 활용한 개인 회고 퀘스트를 제안합니다.

### 목적
AI의 도움을 받아 회고에 대한 부담을 줄이고 바쁜 일정 속에서도 꾸준히 개인 회고를 실천하는 것이 목표입니다.

### 퀘스트 내용

### 1. 개인 회고 템플릿 생성 (필수)
- AI를 활용하여 매일 사용할 개인 회고 템플릿을 작성합니다
- 다음 세 가지 항목은 반드시 포함되어야 합니다
    - 잘한 점
    - 아쉬운 점
    - 개선 방법
- 회고를 진행하면서 필요에 따라 템플릿을 수정하거나 고도화할 수 있습니다
    
### 2. 회고 주기 및 시간 설정 (필수)
- 회고를 진행할 주기와 시간을 정합니다
    - 예시: 매일 Gist를 최종 제출한 후에 회고 진행
- 설정한 일정에 따라 1번에서 만든 템플릿을 활용하여 회고를 작성합니다

### 3. AI 피드백 받기 (선택)
- 작성한 회고에 대해 AI로부터 피드백을 받을 수 있습니다
- 회고마다 피드백을 요청하거나 일정 기간 작성한 회고를 모아 피드백을 받을 수 있습니다
- 피드백 방식은 자율적으로 결정합니다

## 달성 기준
- 회고 템플릿과 해당 템플릿을 만들기 위해 사용한 프롬프트를 공유합니다 (필수)
- 회고를 진행할 기간, 시간과 달성 여부를 공유합니다 (필수)
	- 최소 주 2회 이상 회고를 하길 권장합니다
    - 공유하고 싶은 회고 내용이나 AI 피드백이 있다면 자율적으로 공유합니다 (선택)


---

### ✅ 4. 코드 리뷰 시간 부족: `AI의 코드 리뷰와 내 리뷰 비교해보기`

### 배경

같은 미션을 해결한 동료들의 코드를 살펴보고 배우고 싶지만, 어려운 구현 내용이 대다수이다 보니 1시간 안에 3명의 코드를 리뷰하는 것이 힘들들다고 느꼈습니다. 

또한, 다른 사람의 코드를 분석해본 경험이 많지 않다 보니 어떻게 해야 할지 막막한 느낌도 드는 것 같습니다. 1시간 안에 코드를 보기가 너무 힘들다면, 혹은 더 나은 코드 리뷰를 하고 싶은 사람이라면 ai의 도움을 받는 것도 좋은 방법일 것이라 생각합니다.

### 목적

동료의 코드를 보다 효율적으로 리뷰하기.
ai의 리뷰와 나의 리뷰를 비교해보며, 내 코드 리뷰 방식의 개선점 찾아보기

### 퀘스트

먼저 스스로 동료의 코드 분석해보기.
ai에게 코드 리뷰를 요청하기
어떻게 요청할 것인지는 자율적으로 정한다. 예를 들면 다음과 같이 질문할 수 있다.

위 코드를 이해하기 쉽도록, 다음 내용들을 작성해줘.

1. 코드를 이해하기 쉽도록 주석 달기(어떤 로직을 수행하는 코드인지, 어떤 값을 저장하고 있는 변수인지 등등) 
2. 함수의 흐름 알기 쉬운 형태로 정리 
3. 어떤 cs 지식들이 사용된 코드인지 키워드 정리

### 달성 기준

- 하루에 최소 한 명의 동료 코드에 퀘스트를 적용해보기

---

## 미션 소감### ✅ 3. 개인 회고 실천: `AI 회고 템플릿으로 주 2회 이상 회고하기`

### 배경
미션 해결에 많은 시간을 소모하면서 개인 회고를 충분히 하지 못한 점이 아쉬움으로 남았습니다. 이를 보완하기 위해 AI를 활용한 개인 회고 퀘스트를 제안합니다.

### 목적
AI의 도움을 받아 회고에 대한 부담을 줄이고 바쁜 일정 속에서도 꾸준히 개인 회고를 실천하는 것이 목표입니다.

### 퀘스트 내용

### 1. 개인 회고 템플릿 생성 (필수)
- AI를 활용하여 매일 사용할 개인 회고 템플릿을 작성합니다
- 다음 세 가지 항목은 반드시 포함되어야 합니다
    - 잘한 점
    - 아쉬운 점
    - 개선 방법
- 회고를 진행하면서 필요에 따라 템플릿을 수정하거나 고도화할 수 있습니다
    
### 2. 회고 주기 및 시간 설정 (필수)
- 회고를 진행할 주기와 시간을 정합니다
    - 예시: 매일 Gist를 최종 제출한 후에 회고 진행
- 설정한 일정에 따라 1번에서 만든 템플릿을 활용하여 회고를 작성합니다

### 3. AI 피드백 받기 (선택)
- 작성한 회고에 대해 AI로부터 피드백을 받을 수 있습니다
- 회고마다 피드백을 요청하거나 일정 기간 작성한 회고를 모아 피드백을 받을 수 있습니다
- 피드백 방식은 자율적으로 결정합니다

## 달성 기준
- 회고 템플릿과 해당 템플릿을 만들기 위해 사용한 프롬프트를 공유합니다 (필수)
- 회고를 진행할 기간, 시간과 달성 여부를 공유합니다 (필수)
	- 최소 주 2회 이상 회고를 하길 권장합니다
    - 공유하고 싶은 회고 내용이나 AI 피드백이 있다면 자율적으로 공유합니다 (선택)


---

### ✅ 4. 코드 리뷰 시간 부족: `AI의 코드 리뷰와 내 리뷰 비교해보기`

### 배경

같은 미션을 해결한 동료들의 코드를 살펴보고 배우고 싶지만, 어려운 구현 내용이 대다수이다 보니 1시간 안에 3명의 코드를 리뷰하는 것이 힘들들다고 느꼈습니다. 

또한, 다른 사람의 코드를 분석해본 경험이 많지 않다 보니 어떻게 해야 할지 막막한 느낌도 드는 것 같습니다. 1시간 안에 코드를 보기가 너무 힘들다면, 혹은 더 나은 코드 리뷰를 하고 싶은 사람이라면 ai의 도움을 받는 것도 좋은 방법일 것이라 생각합니다.

### 목적

동료의 코드를 보다 효율적으로 리뷰하기.
ai의 리뷰와 나의 리뷰를 비교해보며, 내 코드 리뷰 방식의 개선점 찾아보기

### 퀘스트

먼저 스스로 동료의 코드 분석해보기.
ai에게 코드 리뷰를 요청하기
어떻게 요청할 것인지는 자율적으로 정한다. 예를 들면 다음과 같이 질문할 수 있다.

위 코드를 이해하기 쉽도록, 다음 내용들을 작성해줘.

1. 코드를 이해하기 쉽도록 주석 달기(어떤 로직을 수행하는 코드인지, 어떤 값을 저장하고 있는 변수인지 등등) 
2. 함수의 흐름 알기 쉬운 형태로 정리 
3. 어떤 cs 지식들이 사용된 코드인지 키워드 정리

### 달성 기준

- 하루에 최소 한 명의 동료 코드에 퀘스트를 적용해보기

---

## 📒 미션 소감
### 1주차
- K031_홍원택

 	퀴즈를 통해 CS 개념을 능동적으로 복습할 수 있어 기억에 오래 남았고, 프롬프트 수정을 통해 AI 퀴즈 생성 방식도 원하는 형태로 잘 조정할 수 있었다. 다만 5문제 모두 정답이 'C'로 나와 변별력이 떨어졌고, 문제 출제가 초반 내용에 치우쳐 있다는 점은 아쉬웠다. 전반적으로 자동화된 복습 루틴으로 활용 가치가 높다고 느꼈다.

- J005_강민석

 	매일 퀴즈를 만들어서 풀어보니까 전날의 내용들이 새록새록 기억나서 좋았다.
내가 공부한 내용을 내가 퀴즈로 만들면 정답을 미리 아니까 의미가 없을텐데 확실히 AI가 뚝딱 하고 만들어주니까 너무 좋은 것 같았다.
퀴즈를 만드는 것 외에도 AI를 활용해서 학습하는 방법을 더 찾아서 시도해보고 싶은 생각이 들었다.

- J165_유태근

  	5일 동안 코드분석 AI를 활용해 동료들의 코드를 그날의 미션 맥락에 맞춰 분석하면서, 피드백의 깊이와 정확도를 한층 높일 수 있었다. 기능 구현 여부뿐 아니라 구조, 성능, 가독성까지 입체적으로 바라볼 수 있어 코드 리뷰가 더 유의미하게 다가왔다. 특히 내가 미처 보지 못한 개선 포인트까지 짚어줘서 피드백의 신뢰도와 설득력이 높아졌다. 분석 기준을 상황에 따라 유연하게 조정하는 과정도 좋은 훈련이 되었고, 앞으로도 팀 내 리뷰나 코드 품질 향상에 지속적으로 활용하고 싶다. 

- J233_임정원

   	이번 퀘스트를 통해 하루를 정리하고 되돌아볼 수 있었다. 매일 바쁘게 지나가는 일정 속에서 무엇을 잘했는지, 어떤 점이 아쉬웠는지를 스스로 묻고 기록하는 과정이 큰 힘이 되어주었다. AI 회고 템플릿 덕분에 질문들을 가지고 고민 없이 바로 작성에 들어갈 수 있어 부담도 적었고, 배운 내용을 자연스럽게 정리할 수 있어 아카이빙의 시작점으로 더 응용할 수 있다고 생각했다. 앞으로도 이 회고 템플릿을 더 고도화해서 의미 있는 한 달을 쌓아가고 싶다.

> 미션 수행 기록은 `수행할 내용` 디렉토리에 정리해두었습니다.

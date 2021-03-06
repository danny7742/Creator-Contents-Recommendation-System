# Creator-Contents-Recommendation-System
## 1. 개요
시간이 지나가면서 Youtube 채널을 운영하는 1인 크리에이터가 점점 늘어나고 있다. 이에 따라 다양한 Youtube 컨텐츠 시장도 기하급수적으로 늘어나는 것을 알 수 있다.
YouTube에선 시청자들이 특정 영상을 보고 관련된 영상중 시청자들이 보기에 알맞은 영상을 추천해 주는 기능을 제공한다.

우리는 YouTube 시청자들에게는 자신의 관심사와 시청 경향에 맞춰 다른 동영상을 추천해주는 시스템은 있는 데 비해, YouTube에 영상을 업로드하는 채널 운영자, 즉 1인 크리에이터들에게는 왜 더 질 높은 영상을 만들 수 있도록 컨텐츠 활용 전략을 추천해주는 시스템이 없는 지 궁금해졌고, 관련된 내용을 검색해보니 아래와 같은 애로사항이 있었다.
-	YouTube 채널을 상세히 분석해주는 시스템은 있지만, 사용하기에 어렵고, 사용을 위해서 비용부담이 만만치 않다(월 190$ 이상의 이용료).
-	컨텐츠 추천 사례가 있는 경우 특정 분야에서만 추천 시스템이 동작하고, 업로드한 영상을 분석해 자동으로 추천을 진행해주는 서비스는 없다.

이에 우리는 ‘1인 미디어 크리에이터를 위한 컨텐츠 추천 시스템’ 을 고안했다.

## 2. 목표
예상조회수가 가장 높은 컨텐츠의 조합을 추천해줌으로서 크리에이터의 객관적인 의사결정을 지원하는 것이 최종 목표이다.

## 3. 데이터셋 및 알고리즘
우리가 이용할 데이터셋은 샌드박스소속의 유명 크리에이터에 대한 데이터로

-	영상별 조회수 증감
-	추천시스템을 통한 영상 노출 빈도 및 해당 경로를 통한 조회수
-	각 영상별 시청자 수
-	영상길이
-	영상 카테고리(해시태그)
-	영상별 시청자 체류시간
-	댓글 수

위의 데이터들을 크롤링해 추출한다. 추출된 데이터들을 가공한 후 여러 가중치를 적용시켜 데이터셋으로 이용할 예정이다.

프로세싱한 데이터를 가지고 영상의 카테고리를 이용하여 컨텐츠 베이스드 필터링을 통하여 어떤 카테고리의 조합이나 누구와 합동방송등을 하였을 때 더 좋은 반응을 예측할 수 있는지를 보일 것이다.

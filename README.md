# MLOoops-Recommend
# 추천 알고리즘 개발
    
    → 유인재 + 이지해 + 우태경 + (김태현)
    
    - 관심사 기반
    - 비관심사 기반
    - 통계 데이터 기반

### 1. 사용자 관심사 기반 추천

- 구현 방법
    - 콘텐츠 기반
    - 사용자 기반
    1. 추천
        - 구독 기반
            - 관심 키워드
            - 관심 분야
            - 관심 언론사
        - 사용자 분석 기반([링크](https://www.geeksforgeeks.org/user-based-collaborative-filtering/))
            - 사용자 분석을 통해, 비슷한 사람이 읽은 기사 추천
        - 비 맞춤 분야 추천
            - 성별/연령대 기반
                - 본인의 관심 분야는 아니지만, 이러한 것은 어떤가요? 하고 추천
            - 관심 키워드/분야/언론사 유사 사람들의 나와는 다른 관심 기반
                - 본인의 관심 분야로 선택되지는 않지만, 이러한 관심 분야는 어떤가요?
        - 내용 분석 기반([링크](https://www.analyticsvidhya.com/blog/2015/08/beginners-guide-learn-content-based-recommender-systems/))
- 구현 기술
    - 데이터 수집
        - 뉴스 수집 API
        - 사용자 데이터 수집
        1. 뉴스 API를 통해서 데이터 가져오기
        2. DB 저장
        3. 추천
            - 컨텐츠 기반
                - 어레이 유사도(vector)
            - 사용자 기반
                - 사용자가 봤던 뉴스들 기반으로
            - 계산 시점 : 일정 시점마다 / 사용자가 접속할 때마다 / 새로고침 버튼
---
### 2. 사용자가 관심없어도 추천

- 구현 방법
    - 발생조건
        - 유튜브에서 내가 관심없는 영상이 뜨는 방식
        - 조회수가 많거나 최근 인기가 많은
        - 사용자의 성별 / 연력
    - 선별조건
        - 알고리즘의 선택을 받은
        
- 구현 기술
    - 조회수 기반으로 인기있는 기사 추천
    - DB 기반
    - ES 사용
        - 검색
---
### 3. 통계 데이터 기반 추천

- 구현 방법
    - 특수 목적
        - 취준생을 위한
        - 최신 기사에서 많이 언급되는 새로운 단어 기반
- 구현 기술
    - 새로운 단어 추출
    - 취준생을 위한이면 취업에 필요한 단어를 추출해서 카테고리 만들기
    - ES 사용?
    - 추천하는 방식 → 단어 수 기반
# 클러스터링 코드 버전 관리

## version
* [8/18 최초 모델링 코드](https://github.com/bettertospeak/codeit07_advanced_pj/blob/main/pj_team1/advanced_pj_modeling.ipynb)
---
* [8/20 votes + hackle 모델링 코드](https://github.com/bettertospeak/codeit07_advanced_pj/blob/main/Desktop/only_behavior_test.ipynb)

### 1️⃣ First Commit (Bransh 'main')
> 🔁 변동사항
1. votes에서 만든 questionset_cnt(질문세트 생성 수), vote_cnt(투표 수) 변수 제거
2. 7-8월 hackle_properties, hackle_events를 session_id로 병합, user_id 기준으로 마스터에 병합한 뒤 다음 변수 가져옴
   - friend_count
   - votes_count
   - heart_balance
3. attendance_cnt(출석일수), votes_count(투표 수)가 0인 건은 제외하고 클러스터링(17091건)
> 🔺 본 버전에서 처리할 부분
1. 불필요한 점검 코드 정리
2. hackle에서 user_id별, session별 duration 변수 추가

  
### 2️⃣ Second Commit (Branch 'session')
> 🔁 변동사항
1. 모델링 전 테이블 전처리 코드 정리
2. hackle에서 user별 세션 수 집계하여 추가 (session_count)
   * 유저별 평균 세션 지속시간을 구하고싶었는데, 집계 결과가 이상하게 나와서 추가하지 않았음
3. 실루엣 계수 0.487
> 🔺 본 버전에서 처리할 부분
1. 공선성 높은 변수 처리
   - heart_balance, point
   - pending_chat, report_count
2. 불필요한 점검 코드 뒷부분도 정리

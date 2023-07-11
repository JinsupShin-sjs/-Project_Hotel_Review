# -Project_Hotel_Review_Solo
 ## 2nd Project


## <프로젝트 계획>

### 프로젝트 주제	 호텔 이용 후기 데이터를 활용한 평점 예측 프로젝트

1. 프로젝트 개요
(프로젝트에 대한 설명)	
인터넷 검색 엔진을 통해 제주 지역 소재 호텔을 예약 구매한 이용객들의 후기에서 리뷰 글의 긍정적이거나 부정적인 감성 분석 평가 모형을 만들고
이용객이 직접 남긴 평점을 이용한 정형데이터와 융합하여 성능을 향상 시킨 평점 예측 모형을 구축하고 배포함. 

3. 데이터셋	 
 - Selenium을 이용한 Crawler 로 Text 리뷰 및 별점 Data 취합
 - 검색 엔진 : 네이버 호텔, Google Hotel  
 - Base URL  
    •	https://hotels.naver.com/
    •	https://www.google.com/maps/search/Hotels/data=!3m1!4b1?hl=en
3.분석방법	
 - Data 분석 계획
   •	한글 (네이버 호텔), 영어(Google Hotel) 구분하여 언어별로 Text Mining 분석
   •	정형(평점-Number)과 비정형 (리뷰-Text) 데이터 비교 분석 및 융합    
-	Tools : Python, R, Flask, Django, google slides 
-	Package : Konlpy,Tensorflow, Keras, Wordcloud, Regression & Classification (Logit,Tree,  Random Forest, SVM, KNN, ANN, DNN), Etc


## 1주차 (2022.05.22 ~ 05.26) 
-	Data 취합 
  1) Data Sorce 사이트 네이버 호텔 Crawling 작업 중
* 대상 호텔 Link URL 확보 및 호텔 별 리뷰 취합 코드 완성 
* 특이사항 : 네이버 크롤링 횟수 제한 IP 차단되어 지연됨
  2) Kaggle 에서 일부 참고용 Data set 확보 
(미국 호텔 후기 및 평점 데이터, 한국 Bookings.com 리뷰)

## 2주차 (2022.05.30 ~ 06.02) 
-	Data 취합 완료 및 회귀분석을 위한 추가 Data 확보 
  1) 네이버호텔에서 제주 지역 50개 호텔 리뷰 36,865개 및 746개 호텔 평점 및 호텔 등급 Scrawling 완료 
  2) 제주 관광공사 공공데이터 숙박콘텐츠에서 호텔 Room 등 추가 변수 데이터 확보 및 결합 
-	회귀분석 : 평점, 호텔 등급, 객실 수 등 파생 변수 대상 실시
-	Review Text 분석 : 학습용 Data 20,000개, 검증용 10,000개 분류 및 전처리 작업 실시
-	호텔 별 평점 예측 모형 구축

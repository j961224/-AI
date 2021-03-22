# 1주차 내용

## list와 set
 - list는 [] 형태로 중복되는지 상관없이 출력
 
 - set(집합)은 {} 형태로 중복되면 제거하고 출력
   1. set 2개 사이에 | 넣으면 합집합 완성
   2. set 2개 사이에 & 넣으면 교집합 완성
   3. set 2개 사이에 - 넣으면 차집합 완성

## 데이터 크롤링
  - web crawler: 웹 페이지의 데이터를 모아주는 소프트웨어
  
  - web crawling: 크롤러를 사용해 웹 페이지의 데이터를 추출해내는 행위
  
  - BeautifulSoup: 데이터를 가져와서 의미있는 데이터로 변형해주는 기능

  - parsing: 데이터를 의미있게 분해하는 방법으로 파싱을 도와주는 것이 parser(ex. html.parser)

## Api 사용
  : client와 server를 연결하는 api로 f-string으로 문자열 안에 원하는 변수를 넣을 수 있다.
  
  ex) f"http://api.openweathermap.org/data/2.5/weather?q={city}&appid={apikey}"
 
## 번역하기
  : googletrans라는 언어 감지 및 번역 기능 있는 라이브러리 사용하여 번역
  
  |Translator().detect를 통한 언어감지 결과|언어|
  |------------------|-----------------|
  |fr|프랑스어|
  |ar|아랍어|
  |vi|베트남어|
  |de|독일어|
  |es|스페인어|
  |mn|몽골어|
  |zh-CN|중국어|
  |hi|힌디어|
  
## 메일 송신
  1. SMTP(메일 약속 프로토콜-간단하게 메일을 보내기 위한 약속)를 통한 메일 보내기(import smtplib사용)
  ![3 11-1 smtp와 imap](https://user-images.githubusercontent.com/59636424/112011962-1cbfe900-8b6c-11eb-8bdb-07facad66dd6.png)
  - 과정: b-> smtp를 이용해 b@gmail.com에 전송 -> smtp로 a@gamil.com에게 전송 -> imap을 이용해 a email client에게 전송
  - 파이썬 프로그램에서 이메일을 만들고 SMTP로 이메일로 전송 -> a 이메일 서버를 b라는 이메일 서버에 보낼 때 SMTP 사용 (반대도 가능)
  - IMAP으로 다른 이메일이 우리 프로그램으로 가져올 수 있다.
  
  2. import imghdr를 추가하여 메일로 사진 보내기
  
  3. import re를 이용하여 메일 주소 유효성 검사
  - 규칙1: 처음과 끝은 ^와 $를 붙인다.
  - 규칙2: .과@로 끊을 때 +로 연결하며 끊고 각각의 영역에 []를 통해 유효성 검사
  - 규칙3: []{}는 []안의 규칙을 최소 몇번에서 최대 몇번까지 반복함을 뜻함 ex) [a-zA-Z]{2,3} a부터 z까지, A부터 Z까지가 최소 2회, 최대 3번 반복

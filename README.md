# 다락방 

## 주제선정 배경
### 전자책 시장 성장률
<img width="291" alt="image" src="https://user-images.githubusercontent.com/48540791/177830301-1aacf1c5-e652-489b-b836-8b6379c33136.png">
출처 : https://mcst.go.kr/kor/s_notice/press/pressView.jsp?pSeq=12597

### 전자책을 읽는 매체
<img width="355" alt="image" src="https://user-images.githubusercontent.com/48540791/177830361-7f07f784-5605-4bc5-aea7-498b76ce6ba2.png">
출처 : https://www.kocca.kr/knowledge/publication/focus/__icsFiles/afieldfile/2012/10/19/4BRfDylIFv47.pdf

## 현재 어플과의 차별성
- 나만의 독서 리스트를 생성하여 다양한 카테고리를 사용
- 독서 달력에서 책의 읽기 상태를 표시
- 독서 완료한 책을 기준으로 목표치를 확인

## 시스템 구조
<img width="684" alt="12" src="https://user-images.githubusercontent.com/48540791/177830651-f594a14b-8906-4793-8c7a-00a8c1ed6bc4.png">
<img width="667" alt="2" src="https://user-images.githubusercontent.com/48540791/177830877-0c97c37d-7fd2-4ef5-9147-1bd08af399d5.png">

## 기술 설명
< 구성 요소 >
Database
: 데이터베이스 홀더를 포함, SQLite DB에 접근할 수 있는 엑세스 포인트를 제공
2) Entity 
: 데이터베이스의 테이블
3) DAO(Data Access Objects)
: 데이터베이스에 접속하기 위한 메서드 
( Insert, Query, Update, Delete )
<img width="312" alt="image" src="https://user-images.githubusercontent.com/48540791/177830982-1f0ad334-d846-490d-a0dc-d60bd98f284b.png">

### RoomDB사용 
**Entity 어노테이션으로 Data Class 선언**
<img width="174" alt="image" src="https://user-images.githubusercontent.com/48540791/177831084-800c27e2-b57c-45ba-87df-c3ab91590bda.png">
![image](https://user-images.githubusercontent.com/48540791/177831098-112a974b-5b8c-4b9a-b917-fa01e9c8596e.png)

**DAO ( Data Access Objects ) 객체 선언**
<img width="240" alt="image" src="https://user-images.githubusercontent.com/48540791/177831222-11e8c2b4-420d-4327-85ae-3a6147ef0259.png">
- Data access에 사용할 메서드 ( Insert, Query, Update, Delete) 선언
- Dao 객체는 Interface로 선언
- @Dao 어노테이션 사용
- Data access에 필요한 메소드를 해당 어노테이션을 추가하여 선언

**데이터베이스 생성**
<img width="425" alt="image" src="https://user-images.githubusercontent.com/48540791/177831348-705780f1-bf3f-48b3-b7cd-d51c685cd763.png">
- RoomDatabase()를 상속한 abstract 클래스로 선언
- @Database 어노테이션 추가
- Entities()를 사용하여 DB에서 사용할 Entity를 가져오고
- 버전 관리를 위한 version 설정
- 데이터베이스 선언 후 데이터베이스 빌더를 사용하여 DB 생성

## 결과물
### 나만의 독서리스트 생성
<img width="564" alt="image" src="https://user-images.githubusercontent.com/48540791/177831500-952c82fb-77a4-4bae-9660-739a38c0f6c7.png">

### 인상깊은 구절 추가 
<img width="482" alt="image" src="https://user-images.githubusercontent.com/48540791/177831640-cce39c4a-cc97-4ee1-96f9-8adc2597ad7f.png">

### 독서 달력 및 목표량
<img width="490" alt="image" src="https://user-images.githubusercontent.com/48540791/177831699-036d08f1-78c1-44f0-802a-bad5aa741ee5.png">




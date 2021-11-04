# 관통프로젝트: HappyHouse_Framework 
> 기존 백엔드 프로젝트를 spring legacy 혹은 spring boot로 변환(2021.11.02~)
>
> 어떤 알고리즘을 넣어야 더 좋은 프로젝트가 될 수 있을지 생각(~2021.11.03)



### 처리된 요구사항 목록

#### framework 분야

|난이도|구현기능(DB 구축 및 연결)|세부|작성여부(O/X)|
|:---:|---|---|:---:|
|기본|메인화면||O|
|기본|회원관리|회원정보 등록,수정,삭제,검색|O|
|기본|로그인/로그아웃||O|
|기본|실거래가 검색, 결과|전체검색화면|O|
|기본|실거래가 검색, 결과|상세검색화면|O|
|기본|실거래가 검색, 결과|동별화면|O|
|기본|실거래가 검색, 결과|아파트별검색화면|O|
|추가|비밀번호찾기/사이트맵/메뉴구성화면||X|
|추가|관심지역 동네 업종 정보 조회||X|
|추가|관심시역 대기오염 정보 조회||X|
|심화|웹사이트 소개/공지사항관리화면||X|

#### algorithm 분야

|난이도|구현기능(DB 구축 및 연결)|세부|작성여부(O/X)|
|:---:|---|---|:---:|
|기본|알고리즘 2개 추가 및 구현한 프로젝트||O|
|추가|알고리즘 추가||O|
|심화|새로운 기능을 추가한 프로젝트 요구사항 정의서||X|

#### 기본 알고리즘 1

 - 제목:  비싼 집이라고 다 좋을까?
 - 적용 효과: 집 계약 후 만족도가 높은 삶을 살 수 있게 해준다.
 - 적용 이유: 아무리 좋다고 소문난 아파트일지언정 만족도가 무조건 높을 수는 없을 것이다. 
    - 힘들게 구한 집이 팔리기 전까지 생활 만족도를 떨어트린다면 예쁜 쓰레기가 될 것이다.
 - 구현할 내용: 매물마다 만족도를 넣을 테이블을 생성.
    - 선택한 아파트에 대한 만족도를 조회할 때 아파트 별 평균 만족도를 구할 수 있도록 만들어준다.
    - 선택한 아파트의 만족도가 선택한 법정동의 전체 평균 만족도와 비교할 수 있도록 한다.
       - 만족도가 법정동 평균보다 높다면, 어떤 이유에서 높은지 검색할 기회를 제공
       - 만족도가 법정동 평균보다 낮다면, 어떤 불편함이 있었는지 확인 가능
       - WordCloud형태로 보여질 수도 있게...
 - 적용부분: houseService



#### 기본 알고리즘 2

 - 제목: 맞춤형 집 고르기
 - 적용 효과: 원하는 조건으로 빠르게 매물을 찾을 수 있다.
 - 적용 이유:  바쁜 사회에 매물들 중 매물을 찾기 위해선 부동산을 방문과 수많은 매물을 확인 하는 불편함 해소. 
 - 구현할 내용: 조합 알고리즘을 이용
    - 헤더 부분에 '맞춤 매물'이라는 카테고리를 새로 추가하여 조회할 수 있는 페이지를 생성한다. 
    - 조회 시 필수 내용은 허용 예산 범위, 찾는 지역이고, 부가적으로 건축년도 등을 입력할 수 있도록 한다. 
    - 사용자가 입력한 정보를 토대로 매물을 조회하여 여러 조합을 생성한다.
    - 생성된 조합들 중에 만족도가 높은 매물 2~3개를 추천한다.
 - 적용부분: houseService



 #### 추가 알고리즘 1

 - 제목: 클릭 4번으로 매물 찾기
 - 적용 효과: 미리 정한 키워드로 손 쉽게 매물을 찾을 수 있다.
 - 적용 이유: 포털사이트 매물 검색 시에 여러 페이지를 거치면서 광고성 매물이 많아 원하는 정보를 얻기 힘듦.
 - 구현할 내용: 사용자 DB(member)에 관심 키워드 항목을 추가한다.
     - 사용자가 관심있는 키워드를 3개정도 등록할 수 있도록 한다. 
     - 등록한 키워드를 바탕으로 매물을 조회할때, 관심 키워드와 관련된 매물들 순으로 보여지도록한다.
     -  원하는 매물이 나올때까지 찾아보지 않아도 빠르게 매물을 찾을 수 있는 기능이다. 
 - 적용부분: houseService

 

<span style="color:red">
* 작성된 기능은 반드시 캡쳐되어야 합니다.<br>
* 추가로 구현한 기능을 표에 추가시키세요.
</span>

### 실행화면 캡쳐 - 
TODO: 요구사항 목록에서 완료 처리된 사항의 캡쳐 이미지를 등록하세요.



1. 구현 기능: Main(메인화면)
   ![](https://github.com/Doppio1101/PJT/blob/master/Framework_PJT/result/main.PNG?raw=true)



2. 구현 기능: loginPage
   ![](https://github.com/Doppio1101/PJT/blob/master/Framework_PJT/result/loginPage.PNG?raw=true)



3. 구현 기능: loginCheck
   ![](https://github.com/Doppio1101/PJT/blob/master/Framework_PJT/result/loginCheck.PNG?raw=true)



4. 구현 기능: main_after_login
   ![](https://github.com/Doppio1101/PJT/blob/master/Framework_PJT/result/main_after_login.PNG?raw=true)



5. 구현 기능: myPage
   ![](https://github.com/Doppio1101/PJT/blob/master/Framework_PJT/result/myPage.PNG?raw=true)



6. 구현 기능: askUpdate
   ![](https://github.com/Doppio1101/PJT/blob/master/Framework_PJT/result/askUpdate.PNG?raw=true)



7. 구현 기능: updateCheck
   ![](https://github.com/Doppio1101/PJT/blob/master/Framework_PJT/result/updateCheck.PNG?raw=true)



8. 구현 기능: delete
   ![](https://github.com/Doppio1101/PJT/blob/master/Framework_PJT/result/delete.PNG?raw=true)



9. 구현 기능: joinPage
   ![](https://github.com/Doppio1101/PJT/blob/master/Framework_PJT/result/joinPage.PNG?raw=true)



10. 구현 기능: registerCheck
    ![](https://github.com/Doppio1101/PJT/blob/master/Framework_PJT/result/registerCheck.PNG?raw=true)



11. 구현 기능: findHouseMain
    ![](https://github.com/Doppio1101/PJT/blob/master/Framework_PJT/result/findHouseMain.PNG?raw=true)



12. 구현 기능: dongFind
    ![](https://github.com/Doppio1101/PJT/blob/master/Framework_PJT/result/dongFind.PNG?raw=true)



13. 구현 기능: aptFind
    ![](https://github.com/Doppio1101/PJT/blob/master/Framework_PJT/result/aptFind.PNG?raw=true)







### 소감

- 장정훈
  - 이전 백엔드 프로젝트를 스프링 프레임워크로 변환 하고 일부를 RestAPI로 변환하는 작업
  - 이전 프로젝트를 스프링 부트 패턴으로 변환하며 옮기는 작업이 익숙하지 않았던 것 같습니다.
  - 백엔드에서 스프링 legacy -> 스프링 부트 순서로 배우고 프로젝트를 진행해서 그런지 이전 버전들보다 스프링 부트에서의 작업량이 줄어들었다는 것을 체감할 수 있었습니다.
  - <b>스프링 부트의 마이크로 서비스의 개념을 이해할 수 있던 프로젝트였습니다.</b> 
  - <b>STS에서 스프링 부트 프로젝트를 깃 관리를 할 때 자동으로 .ignore파일 설정이 되어 페어에게 프로젝트를 고스란히 넘기지 못 해서 헤맸던 것 같습니다. </b>
  
- +(2021.11.05)
  - 이전 프로젝트와 이번 스프링 변환 및 아이디어 추가를 진행 하면서 기본에 충실하자는 생각이었습니다.
  - 프론트엔드 프로젝트부터 코드를 다시 읽어보면서 추가, 심화 기능을 추가하고자 합니다.
  - 이전에 했던 코드에서 더 낫고 깔끔한 코딩을 해보고자 합니다.
  - 또, 주석을 달면서 다른 사람이 봐도 어떤 코드인지 쉽게 이해할 수 있도록 할 예정입니다.
  - 다음에 있을 Vue를 이용한 프로젝트 후 위 계획을 실행하고자 합니다.


# Project 정리

> Front -> DB -> Back -> Framework -> Vue 순서로 프로젝트를 확장하는 중입니다.
>
> - 주로 2인 1조가 되어 프로젝트를 진행했습니다. 
> - 풀스택 역량을 늘리고자 프론트엔드, 백엔드를 구분짓지 않고 기능 단위로 나누어 작업을 진행했습니다.
> - SSAFY GitLab을 이용하여 형상관리를 진행중입니다.
>
> WEB_TIL은 이렇게 PJT를 진행하면서 공부했던 내용을 담아 놓는 중입니다.



## 프로젝트 개요



### 1. Front_End_PJT

- 순수 프론트엔드 프로젝트로 데이터를 관리하는 데에 로컬스토리지로 대체하여 진행했습니다.
- AJAX를 이용하여 공공데이터 포탈로부터 데이터를 받아 파싱하여 관리하였습니다
- 공공데이터 포탈로 받은 데이터를 카카오 맵 API를 활용하여 지도에 뿌리도록 하였습니다



### 2. Back_End_PJT

- DB프로젝트에서 만들었던 DAO를 기반으로 진행한 프로젝트입니다.
- DB프로젝트에서는 Controller의 위치에서 main메서드를 이용하여 출력을 확인하였고
- 이 프로젝트에서 이전 프론트엔드 프로젝트와 연동하는 작업을 진행하였습니다.



### 3. Framewokr_PJT

- 이전 BacEnd 프로로젝트를 Spring MVC 패턴에 맞추고어 변형하였습니다.
- DB 연결을 MyBatis로 변환 하였고, 스프링 부트로 변환하는 작업을 진행하였습니다.
- 이후 Vue.js를 이용한 SPA 프로젝트를 준비했습니다.



### 4. Vue_PJT

- Q&A 게시판을 제작. (로그인 기능의 부재)
- Vue를 이용한 프론트엔드 페이지 제작을 했습니다.
- 이를 위한 RestAPI 백엔드를 스프링 부트와 마이바티스를 활용하여 제작했습니다.
- SPA를 이해할 수 있었던 시간이 되었고 Vuex를 이용하여 컴포넌트 간의 데이터 공유를 이해할 수 있었습니다.
- 세션 활용이 안 되면서 JWT와 토큰에 대해 공부의 필요성을 깨달은 프로젝트입니다.



### 5. Final_PJT

- 제로베이스에서부터 다시 시작하고 프론트엔드를 Vue로 바꾸었습니다.
- 프론트/백을 나누지않고 기능별 개발을 진행했습니다.
- 프론트엔드에서는 카카오MAP API를 이용하여 맵을 불러와 마커를 찍고 
- 공공데이터에 좌표가 존재하지 않은 값은 카카오를 이용하여 좌표로 변환 후 마커를 찍었습니다.
- 이때 공공데이터에서 아파트 실거래 매매 상세정보를 백엔드의 서비스 파트에서 구군코드를 이용하여 불러왔습니다.
- ~~교통 정보 중 버스정류장의 좌표도 공공데이터로 받아오고자 합니다.~~
- ~~지하철의 정보는 카카오API에서 제공되는 카테고리 검색을 사용하고자 합니다.~~ 시간부족으로 반영하지 못 했습니다.
- 이렇게 백엔드에서 받아온 매매정보를 회원가입에서 입력한 주소 기반 좌표를 중심으로 반경을 지정하여 보여주고자 합니다.


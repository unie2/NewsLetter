<h2> 뉴스레터 서비스 </h2>

## 1. 개발 배경
특정 그룹 혹은 개인을 대상으로 공유할 이슈 내용을 공지 게시판 등에 업로드 해야 하는 불편함을 바탕으로 교내 요청에 따라 교수님들께서 사용하실 수 있는 `뉴스레터 서비스` 를 제작하였습니다.

---------------------

## 2. 개발 내용
#### (1) 개발 환경 : Spring Boot & React & MySQL

#### (2) 회원 가입
<img src="https://user-images.githubusercontent.com/54324782/164892629-1799f221-6150-459e-b8c0-cdaa51611c61.png" align="left">
    - 특정 교수님들만 사용하시므로 관리자 계정에서만 회원을 추가할 수 있도록 하였습니다.
    <br><br>
    - 이메일의 경우 중복 확인 기능을 포함시켰으며, 비밀번호, 기관명, 대표자명, 전화번호를 입력하여 가입 처리를 할 수 있습니다.
    
<br><br><br><br><br><br><br><br><br><br>
    
#### (3) 마이페이지
<img src="https://user-images.githubusercontent.com/54324782/164892872-14a7639b-86e0-47dc-804e-708bb96baa37.png" align="left">
<img src="https://user-images.githubusercontent.com/54324782/164893000-446250cd-1911-4bb3-95be-52c723a09933.png">
<br><br><br><br><br>
    - 프로필 변경과 비밀번호 변경 항목을 Tab으로 구별하여 사용자가 한 페이지에서 더욱 편리하게 수행할 수 있습니다.
    <br><br>
    - 프로필 변경 : 초기 값은 현재 DB에 저장되어 있는 값들을 가져와 default값으로 표시하였습니다.<br>
                        이메일과 전화번호의 경우 올바른 형식으로 작성해야만 프로필 변경이 가능합니다.  
    <br>
    - 비밀번호 변경 : 오타 문제를 방지하기 위해 `다시 한번 입력` 항목을 포함하였습니다.

<br><br>

#### (4) 작성한 뉴스레터 목록
<img src="https://user-images.githubusercontent.com/54324782/165057068-b58fca5c-9e76-45e2-86e7-5d43b41f1939.png">
    - 제목, 수신자(명), 작성일을 확인할 수 있도록 테이블 형태로 구성하였습니다.
    <br><br>
    - '수신자(명)' 의 경우 커서를 올리면 수신자 이름 혹은 이메일을 한 눈에 확인할 수 있도록 구현하였습니다.
    <br><br>
    - 사용자가 목록을 편리하게 확인할 수 있도록 페이징 처리를 작업하였습니다.
    
<br><br>

#### (5) 그룹 및 주소록 관리
<img src="https://user-images.githubusercontent.com/54324782/165060497-723ca486-deaa-42f0-8d9b-75ce44dd8902.png" align="left">
<img src="https://user-images.githubusercontent.com/54324782/165060005-94a8d2c3-e0c0-4455-9880-f9d544139c35.png">
    - 그룹 추가 : 그룹 이름을 작성하여 추가할 수 있으며, 중복 처리될 수 없도록 구현하였습니다.
    <br><br>
    - 주소록 추가 : 수신자의 이름과 이메일을 작성하여 주소록을 추가할 수 있으며, 
    <br>
                        그룹을 선택하여 해당 그룹에 수신자가 포함될 수 있도록 하였습니다.
    <br>
                        또한, 수신자의 이메일의 경우 중복 추가될 수 없도록 하기 위해 로그인한 계정을 통해 생성한 수신자 이메일이 이미 존재하는지 확인합니다.
                        
<br><br>

#### (6) 뉴스레터 작성 및 메일 전송
<img src="https://user-images.githubusercontent.com/54324782/165063111-10d01489-dea5-43b2-8ffe-c7b4c947fb5d.png">
    - 보내는 사람의 경우 로그인 중인 사용자의 이메일 계정을 가져와 자동으로 발신자 정보에 등록될 수 있도록 구현하였습니다.
    <br><br>
    - 받는 사람 항목에는 직접 이메일이나 수신자 이름을 작성할 수 있으며, 
    <br>
       `수신자 선택` 혹은 `그룹 선택` 모달 창을 통해 특정 수신자 혹은 그룹을 선택하여 추가할 수 있습니다.
    <br>
       또한, `전체 선택` 시 주소록에 저장되어 있는 모든 수신자들이 자동으로 추가됩니다.
    <br><br>
    - 이후 제목과 내용을 작성하여 메일 전송을 수행할 수 있습니다.

<br><br>

| 수신자 선택 | 그룹 선택 |
| :--------: | :-------: |
| ![수신자 선택](https://user-images.githubusercontent.com/54324782/165067556-bb45ad85-4711-436e-82e3-64475fb54ce5.png)    | ![그룹 선택](https://user-images.githubusercontent.com/54324782/165067778-b96925ca-538c-43c8-8e06-69298a476f1f.png)      |
<br>

## 3. 서버 배포
### (1) Spring Boot 
  - war 파일 생성 후 Tomcat을 통해 컨테이너 구축 및 배포하였습니다.
### (2) React
  - build 파일 생성 후 컨테이너를 구축하고 index.js 파일을 읽어들일 수 있는 경로에 배포하였습니다.
### (3) 다른 웹 사이트와 함께 구동되어야 하므로 Nginx를 사용하였습니다.

<h2> 뉴스레터 서비스 </h2>

## 1. 개발 배경
특정 그룹 혹은 개인을 대상으로 공유할 이슈 내용을 공지 게시판 등에 업로드 해야 하는 불편함을 바탕으로 교내 요청에 따라 교수님들께서 사용하실 수 있는 `뉴스레터 서비스` 를 제작하였습니다.

---------------------

## 2. 개발 내용
(1) 개발 환경 : Spring Boot & React & MySQL


(2) 회원 가입
<br><br>
<img src="https://user-images.githubusercontent.com/54324782/164892629-1799f221-6150-459e-b8c0-cdaa51611c61.png" align="left">
    - 특정 교수님들만 사용하시므로 관리자 계정에서 회원을 추가할 수 있도록 하였습니다.
    <br><br>
    - 이메일의 경우 중복 확인 기능을 포함시켰으며, 비밀번호, 기관명, 대표자명, 전화번호를 입력하여 가입 처리를 할 수 있습니다.
    
<br><br><br><br><br><br><br><br><br><br>
    
(3) 마이페이지
<br><br>
<img src="https://user-images.githubusercontent.com/54324782/164892872-14a7639b-86e0-47dc-804e-708bb96baa37.png" align="left">
<img src="https://user-images.githubusercontent.com/54324782/164893000-446250cd-1911-4bb3-95be-52c723a09933.png">
<br><br><br><br><br><br>
    - 프로필 변경과 비밀번호 변경 항목을 Tab으로 구별하여 사용자가 한 페이지에서 더욱 편리하게 수행할 수 있습니다.
    <br><br>
    - 프로필 변경 : 초기 값은 현재 DB에 저장되어 있는 값들을 가져와 default값으로 표시하였습니다.<br>
                        이메일과 전화번호의 경우 올바른 형식으로 작성해야만 프로필 변경이 가능합니다.  
    <br><br>
    - 비밀번호 변경 : 오타 문제를 방지하기 위해 `다시 한번 입력` 항목을 포함하였습니다.
    
<br><br><br><br><br><br><br><br><br><br>


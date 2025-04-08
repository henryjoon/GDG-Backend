백엔드 1주차
백엔드와 api

웹과 HTTP
웹: 여러 컴퓨터가 서로 연결되어 정보를 공유하는 공간
정보교환의 일반적인 형태: 클라이언트-서버 패러다임

클라이언트-서버 패러다임: 클라이언트: 요청 / 서버:수행,응답
3단계이면: 2단계일 때 서버가 클라이언트가 될 수도 있음

프로토콜과 HTTP
    데이터 전송 방법 명시해줘야 함. 이에 대한 규칙 필요
    이 규칙을 프로토콜이라 부름
    웹은 HTTP라는 프로토콜 사용
    요청할 때: HTTP Method, URL 필요
    Http method: get조회,post생성,put수정,patch수정,delete삭제
    URL: 프로토콜/서버주소/서버 내 데이터 위치
        Path parameter: URL의 일반화된 표현 방법
        Query string: ?key=value&key=value…
    Http 헤더: 통신에 대한 정보(언제 누가 보냈는지, method종류, 요청경오 …)
    HTTP 바디: 받으려는 데이터(json: python딕셔너리와 같은 형태)
    상태코드
      2: 성공
        200: 처리성공
        201: 데이터 생성 성공
      4: 클라이언트 오류
        400: 클라이언트 요청 오류
        404: 요청 데이터 없음
        500: 서버 에러

프론트엔드와 백엔드
    매일 바뀌는 내용에 대해 html을 매번 수정해야할까?
    자주 변하지 않는 것과 변하는 것 구분
    프론트가 백엔드에 컨텐츠 내용 요청
    백엔드는 디비에서 가져와 응답
Rest API
    Api: HTTP 구체적인 통신 방법 정해야 함.
        Application Programming Interface
        어플이케이션과 소통하는 방법 정의한 것
        백엔드 api: 프론트가 백엔드에 요청 보낼 때 어떤 http method, url 사용해야 하는지 정의한 것
    Rest api: url을 명사로 method를 동사로 쓰자.
    
<Task>
1. 할일 전체 조회: GET/todo/whole
2. 할일 생성: POST/todo
3. 할일 수정: PATCH/todo/{user_id}
4. 할일 삭제: DELETE/todo/{user_id}
5. 할일 체크: POST/todo/{user_id}/check
6. 할일 체크 해제: POST/todo/{user_id}/uncheck
7. 로그인: POST/login
8. 로그아웃: POST/logout
9. 회원가입: POST/sign_up
10. 좋아요: POST/like
!!
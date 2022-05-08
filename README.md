## 프로젝트 기획안<br/>
**작성일 : 2022. 05. 04**<br/>
**작성자 : 민소희**<br/>
**프로젝트 명 : 좀비콘텐츠 OTT**<br/>
### 기획 의도 <br/>
⦁	전세계의 모든 사람들이 보다 편하게 오직 좀비 콘텐츠만을 시청할 수 있습니다.<br/>
⦁	좀비 컨텐츠, 미디어가 활성화되길 바라는 마음에 이러한 프로그램을 기획했습니다.<br/>
⦁	OTT 회원가입, 멤버십 구독기간 확인, 영화 및 드라마 추천, 시청내역 확인<br/>
### 벤치마킹 <br/>
⦁	왓챠, 넷플릭스 참고<br/>
⦁	장단점: <br/>
⦁	기능 참고:<br/>
### 주요 기능 <br/>
1. 객체지향 프로그래밍 프로젝트 (좀비영화 OTT)
    1. 고객 정보(ClientDTO)
        1. 고객번호: id
        2. 고객아이디:clientId
        3. 고객이름: clientName
        4. 비밀번호: clientPass
        5. 시청내역: watchList
        6. 구독일자: clientCreatedDate
    2. 영화 정보(WatchDTO)
        1. 영화: movieList
        2. 드라마: dramaList
        3. 고객아이디: clientId
    3. 주요 기능
        1. 프로그램을 실행하면 아래와 같은 메뉴가 출력되고 각 메뉴의 숫자를 입력하면 해당 기능을 실행할 수 있다. 모든 기능은 처리가 끝난 후 다시 메인 메뉴가 출력되도록 한다.
            1. 회원가입
            2. 로그인
            3. 메뉴보기
            4. 시청내역
            5. 시청내역
            6. 멤버십 내역확인
        2. 모든 고객의 데이터는 WatchDTORepository의 clientList에 저장되고 관리된다.
            1. clientList는 static으로 선언하도록 한다.
        3. 모든 거래내역의 데이터는 WatchDTORepository의 watchingList에 저장되고 관리된다.
            1. watchingList는 static으로 선언하도록 한다.
            
        
        1.  회원가입
            1. 회원가입시 고객이름, 비밀번호를 입력할 수 있다.
            2. 신규 등록 고객의 시청내역은  “아직 시청하지 않았어요.” 이다.
            3. 회원가입 고객번호는 자동으로 하나씩 증가되도록 한다. 가입일자도 현재 시간이 입력되도록 한다.
            4. 회원가입이 완료되면 “WELCOME TO ZOMBIE WORLD” 라는 내용이 출력된다.
        
        2. 로그인
            1. 입력한 아이디와 비밀번호가 일치하다면 “로그인 성공!” 로고가 뜨고, 좀비 top5 콘텐츠 목록이 출력된다
            2.  로그인 정보가 일치하지 않는다면 “로그인에 실패했습니다.”
            
        3. 메뉴보기 및 추천
            1. 좀비 인기 top5 콘텐츠 목록이 출력된다.  top5까지는 1~5 번호 입력하면 간단한 줄거리 및 감상평이 나온다. 6번을 입력하면 전체 리스트가 출력
            2. 영화와 드라마 중 어떤 것을 보겠냐고 물어본다
                - 좀비 영화 선택
                    1. 좀비영화를 List를 출력하도록 한다.
                    2. scan을 받아 시청할 영화를 입력받고 진행됐을 때는 시청영화를 시청내역 목록에 추가한다.
                - 좀비 드라마 선택
                    1. 좀비드라마를 List를 출력하도록 한다.
                    2. scan을 받아 시청할 드라마를 입력받고 진행됐을 때는 시청드라마를 시청내역 목록에 추가한다..
                    
        4. 시청내역(while~if문을 사용하여 아래 3가지 항목이 뜬다)
            1. 해당 아이디의 그동안 시청한 총 시청내역을 확인한다.
            2. 해당 아이디의 영화 내역만 확인
            3. 해당 아이디의 드라마 내역만 확인
        5. 추천받기
            1. 배열에 저장된 영화 리스트를 랜덤으로 추출하여 영화추천을 도와준다.
        6. 멤버십내역확인
            1. 로그인한 회원의 가장 최근에 보던 컨텐츠가 포함된 회원정보 내역이 출력된다.
            2. 로그인한 회원의 구독기간과 구독만료일을 출력한다.
        7. 종료
    4. Class 구성
        1. WatchMain Class
        2. WatchService Class
        3. WatchRepository Class
        4. ClientDTO Class
        5. WatchDTO Class

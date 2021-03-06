# Bookmark-Manager
Bookmark Manager with Java GUI (CAU 2022-1)  
시연 영상, 북마크 매니저 기능 설명, 구현 사항 요약, 사용 기술에 대해 설명.  
북마크 매니저 설명은 2022-1 중앙대학교 소프트웨어프로젝트 박창윤 교수님의 과제 설명서를 참고하였음.   

## 시연 영상
[![Video Label](http://img.youtube.com/vi/JKR_q0bkFfY/0.jpg)](https://youtu.be/JKR_q0bkFfY?t=0s)

## 북마크 매니저 기능
프로그램 시작 시 bookmark-input.txt에 있는 북마크 정보들을 테이블 형태로 읽어 오고, 같은 group의 북마크들은 모아서 저장   
실제 브라우저의 북마크와의 연동이 아닌, 자료 관리 목적의 GUI 프로그램   

#### 1. open/close 기능:   
같은 group에 속하는 북마크들은 묶어서 처리. 디폴트는 close (“>”) 모드로 개개의 북마크는 보이지 않고, 그룹 이름만 표시   
모드 버튼을 클릭하면, 모드가 open (“V”)로 바뀌면서 그룹 이름 항목 아래로 개별 북마크들의 세부 사항 표시   

#### 2. add 기능:
“ADD” 버튼을 누르면, 빈칸으로 표시되고 입력을 할 수 있는 새로운 북마크 정보 입력 창 생성, 입력 처리   

#### 3. delete 기능:
“DELETE” 버튼을 누르면, 선택된 북마크를 테이블에서 제거하고, 내부 자료 구조에서도 제거   

#### 4. up, down 기능:
“UP” 또는 “DOWN” 버튼을 누르면, 선택된 북마크를 테이블에서 위 또는 아래로 한 줄 이동   
open된 group의 그룹 표시와 각각의 북마크는 한 줄로 취급되며, close된 group은 그룹 전체가 한 줄로 취급   
이동이 발생하면 일시적으로 group 경계가 어긋날 수 있지만, close/open 동작 후에는 group이 모아서 관리되는 원칙에 따라서 재정렬   

#### 5. save 기능:
“SAVE”버튼을 누르면, 현재 메모리에 있는 븍마크 정보들, 즉, 화면에 표시된 북마크 테이블의 상태를 정해진 파일에 저장   
(별도로 “SAVE”를 하지 않으면, 북마크의 갱신은 프로그램이 종료되면 무효화)   

## 사용 기술, 패턴
- OOP 에 기반한 Java GUI (swing)

## 참고 자료
- 2022-1 중앙대학교 박창윤 교수님 소프트웨어프로젝트 과제 설명서

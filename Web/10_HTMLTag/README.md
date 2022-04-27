## Body 배경 지정
### 배경 이미지 지정
    background="~"
### 배경색 지정
    bgcolor="~"
### 배경의 스크롤바 지정
    bgproperties="fixed|공백"

#
## < a > 태그의 속성을 미리 결정
### 글자 색상 지정
    text="~"
### 방문하지 않았을 때 색상 지정
    link="~"
### 링크 클릭 때 바뀌는 색상 지정
    alink="~"
### 방문한 적이 있는 링크 색상 지정
    vlink="~"

#
## 여백 관리
### 여백
    topmargin="~"
    leftmargin="~"
    rightmargin="~"
    bottommargin="~"
### 스크롤바 생성
    scroll="no|yes|auto"

#
## 문자 서식 태그
### 두께를 두껍게
    <b>
### 이태릭체
    <i>
### 윗 첨자
    <sup>
### 아랫 첨자
    <sub>
### 크기를 작게
    <small>
### 크기를 크게
    <big>
### 타자기체
    <tt>
### 밑줄
    <u>
### 취소선
    <s>

#
## 폰트 태그 < font >
### 글꼴 속성
    <font face="글꼴">
### 크기 속성
    <font size="크기">
### 색상 속성
    <font color="색상명">

#
## 특수 문자
- 요소 태그와 충돌하는 문자를 특수 기호로 표시

#
## 단락 서식 태그
### 줄 바꿈
    <br>
### 단락
    <p>
### 수평 가로선
    <hr>

#
## 목록 태그
### 순서없는 리스트
    <ul type="disc | circle | square">
        <li>
### 순서있는 리스트
    <ol type="1 | A | a | I | i" start="~">
        <li type="1 | A | a | I | i" start="~">
### 정의된 용어 리스트
    <dt>  // 용어 제목
        <dd>  // 용어 설명

#
## 링크 태그 < a >
    <a href="url" title="설명" target="클릭시 문서가 열릴 위치">
### target 속성값
- _blank : 새로운 윈도우에 띄우기
- _self : 현재 자기 자신의 프레임에 띄우기
- _top : 새로운 프레임이 생기기 전 최초 프레임에서 띄우기
- _parent : 현재 프레임의 부모 프레임에서 띄우기

###
    <a name="앵커이름">
    <a href=#앵커이름>  // 클릭시 지정된 앵커로 이동

#
## 이미지 태그 < img >
    <img src="이미지 URL" alt="설명">
### 상하여백 크기
    vspace="픽셀수|비율(%)"
### 좌우여백 크기
    hspace="픽셀수|비율(%)"

#
## 테이블 태그 < table >
### 테이블 정의
    <table>
### 행 정의
    <tr>
### 제목 셀 정의
    <th>
### 일반 셀 정의
    <td>
### 테이블 설명
    <catpion>
###
    <table>
        <tr>
            <th> ~ </th>
            <th> ~ </th>
        </tr>
        <tr>
            <td> ~ </td>
            <td> ~ </td>
        </tr>
        <tr>
            <td> ~ </td>
            <td> ~ </td>
        </tr>
    </table>

#
## < table 속성> 
### 셀과 셀 사이의 간격
    cellspacing="픽셀수"
### 셀과 글자 사이의 간격
    cellpadding="픽셀수"

#
## < td 속성 >
### 행의 수평 정렬
    align = "left|right|center|"
### 셀의 수직 정렬
    valign = "top|middle|bottom"
### 행 합치기
    rowspan="숫자"
### 셀 합치기
    colspan="숫자"

#
## 프레임
- 하나의 웹브라우저 화면을 2개 이상의 화면으로 분할하여 사용하는 것
### 프레임 정의
    <frameset rows|cols = "25%, 25%, ...">
        <frame src="URL1">
        <frame src="URL2">
        ...
    </frameset>
### 내부 프레임
- 해당 웹 페이지 안에 또 다른 하나의 웹페이지를 삽입
    
        <iframe src="URL">

#
## < embed >
- 외부 애플리케이션을 포함시킬 수 있는 태그

        <embed src="URL">

#
## < form >
- 사용자 입력을 CGI 프로그램에 전달하는 입력 폼을 정의

        <form action="url" method = "get|post" accept-charset="utf-8" name="person_info">
### 속성
- action : 폼 입력값이 전달될 서버 CGI 프로그램 지정
- name : 폼을 식별할 이름 지정
- accept-charset : 폼에 사용된 문자 인코딩
- target : CGI 프로그램 결과 HTML 문서를 출력할 창
- method : 입력자료를 구성하여 전달하는 방법 HTTP 메소드

### 폼 요소 그룹화와 라벨
#### < fildset >
- 폼 요소 태그 안 관련 입력 요소들을 그룹화 할 때 사용
- < form > 외부에서 사용시 ID를 사용하여 연관성 지정 가능
#### < legend >
- < fildset >의 하위 태그
- 그룹화의 요소들을 목적에 맞게 이름 지정
#### < label >
- 폼 내 컨트롤의 라벨을 붙이는 역할

        <form id="user"> ~ </form>
        <fieldset form="user">
            ~
        </fieldset>

        <input id="abc">
        <label for="abc"> ~ </label>

### 폼 내부 태그 종류
#### < input >
- 문자열 입력 또는 항목 선택
- type : 다양한 자료 형식
- name : 요소 태그 고유이름 지정
- readonly : 읽기전용 지정
- maxlength : 입력 최대 글자수 지정
- required : 태그를 필수로 지정
- autofocus : 페이지가 로딩되면 본 속성 지정 태그로 포커스가 이동
- placeholder : 마우스를 다면 입력할 값에 대한 힌트를 제공
- pattern ; 정규 표현식을 사용
#### < select >
- 드롭다운 리스트 형태로 선택
- size : 한 번에 표시할 항목 수
- multiple : 다중 선택 허용 지정 여부
- < optgroup > : < select > 목록들 중 일부를 그룹화 할 때 사용
- < option > : 목록들을 나타냄
#### < textarea >
- 문자열 줄 문장을 입력
- disabled : 클릭할 수 없음
- wrap : 텍스트 줄바꿈 지정
    * soft : 기본값으로 줄바꿈이 없음
    * hard : 줄바꿈이 있음
#### < keygen >
- keygen 요소는 폼 태그 안에서 private key와 public key를 쌍으로 생성
- 자신은 private key를 저장학 서버는 public key를 보냄
#### < output >
- form이 입력된 뒤에 form을 처리한 결과를 표시하는 요소

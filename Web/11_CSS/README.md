## CSS
- Cascading Style Sheet
- CSS로 요소 태그에 작용될 스타일을 한 번 독립적으로 기술하면 일관성 있는 요소 태그에 적용 가능
- 문서 출력 스타일을 디자인 하여 요소 태그에 CSS를 작용하여 스타일보다 문서의 내용에만 집중하도록 함

#
## CSS 표현 기본 형식
    선택자 {속성값: 값;}

#
## CSS 스타일 적용 방식
### 임베디드 방식
- HTML 문서에 삽입하는 방식
- < head >내 < style >로 CSS 스타일을 정의
- HTML 문서마다 다른 스타일을 적용할 때 편리

        <head>
            <style>
                CSS ~
            </style>
        </head>
### 링크 방식
- HTML 문서와는 별도로 스타일만을 지정한 CSS 파일을 만들어 사용하는 방식

        <style>
            @import url('style.css');
        </style>

        <style>
            <link rel='stylesheet' href='style.css'>
        </style>
### 인라인 방식
- 하나의 요소 태그에만 적용하는 방식

        <h1 style="color:blue">
#
## 선택자와 Rule Set
- 선택자는 선언블럭의 Rule Set을 적용하도록 하는 요소 태그를 선택하는 지정자
### 선택자 종류
#### 전체 선택자
- HTML 페이지의 모든 요소 태그에 CSS 속성을 적용
        
        * { ~ }
#### 요소 선택자
- 지정한 요소에 스타일 적용
- 지정하지 않은 다른 스타일이 적용되지 않음

        p { ~ }
#### 클래스 선택자
- 지정한 클래스에 스타일 적용
        
        p.c1 { ~ }
#### 아이디 선택자
- 지정한 아이디에 스타일 적용

        #c1 { ~ }
#### 속성 선택자
- 태그에 적용되는 것이 아니고 특정 태그 속성에 스타일을 지정
- 특정 태그에 속성값이 어떤 조건을 가질 때 적용
- 태그[attr] : attr 속성이 포함된 태그에 적용
#### 복합 선택자
- 두 개 이상의 선택자 요소가 모인 선택자
- 하위 선택자 : 자손 요소를 선택

        section ul { ~ }
- 자식 선택자 : 자식 요소를 선택

        section>ul { ~ }
#### 가상 클래스 선택자
- 선택자 뒤에 가상이벤트를 붙이면 특정 이벤트마다 적용 할 스타일을 설정할 수 있음
- link : 방문한 적이 없는 링크 일때
- visited : 방문한 적이 있는 링크 일때
- hover : 마우스를 롤오버 했을 때
- checked : check 되어있는 요소일 떄

        a:link{ ~ }

#
## CSS 원천 소스
- 스타일 시트는 author, user, user agent 등 세 개의 다른 CSS 원천 소스를 가질 수 있음
- author : 웹 사이트 제작자가 지정하는 자신의 페이지 스타일
- user : 사용자가 직접 정의하는 자신이 사용할 스타일
- user agent : 웹 브라우저 자체에 지정된 기본 스타일

#
## 글꼴 속성
- font : 글자 스타일 지정
- font-familly : 글자체 지정
- font-size : 글자 크기 지정
- font-weight : 글자 굵기 지정
- font-style : 글자 스타일 지정
- font-varient : 작은 대문자로 변환

#
## 사용자 폰트 스타일
    @font-face{font-family: 폰트이름; src: 폰트위치;}

#
## 텍스트 속성
- letter-spacing : 글자 간격 지정
- word-spacing : 단어 간격 지정
- vertical-align : 수직 정렬 지정
- text-align : 수평 정렬 지정
- text-decoration : 글자 장식 지정
- text-transform : 대소문자 지정
- text-indent : 들여쓰기 간격 지정
- line-height : 줄 간격 지정
- text-shadow : 그림자 효과 지정
- word-brak : 줄바꿈 지정
- text-overflow : 말줄임 지정

#
## 콘텐츠 위치 지정
### position
- static : 요소가 순서대로 배치
- absolute : 문서 혹은 상위 요소 내에서의 절대위치에 배치
- relative : 직전 요소에 이어서 상대위치에 배치
- fixed : 현재 브라우저 화면 내에서의 절대위치에 배치
### z-index
- 앞 뒤 순서 지정
### float
- 플로팅 박스 지정 속성
- 특정 컨텐츠를 주변 컨텐츠와 별도로 분리하여 배치하고 싶을 때
- left : 플로팅 박스를 왼쪽에, 주변 콘텐츠는 오른쪽에 위치
- right : 플로팅 박스를 오른쪽에, 주변 콘텐츠는 왼쪽에 위치
- none(기본값) : 플로팅 박스를 적용 없이 순서대로 배치
### overflow
- 콘텐츠 분량이 요소 박스 크기를 초과할 때 처리 방법
- visible(기본값) : 박스 아래쪽에 초과된 컨텐츠가 계속해서 나타남
- hidden : 박스 크기를 초과하는 컨텐츠는 잘려서 보이지 않음
- scroll : 스크롤 바가 있어서 초과하는 컨텐츠를 볼 수 있음
- auto : 콘텐츠가 박스를 초과할 경우 스크롤바가 나타남

#
## 박스 효과
### border-radius
- 둥근 모서리 속성
### box-shadow
- 박스 그림자

#
## 객체 투명도 및 가시성
### opacity
- 투명도 속성
### visibility
- 가시성 속성
#
## 자바스크립트 코드 위치
1. 이벤트 리스너 속성에 작성
2. < script > ... < /script>에 작성
3. 자바스크립트 코드 작성 후 파일 저장 후 import
4. URL 부분에 작성(ex: a태그)

#
## 자바스크립트 HTML 출력
- 자바스크립트로 HTML 태그를 페이지에 직접 삽입

        document.write("<h1>hello</h1>");
        document.writeln("<h1>hello</h1>");

#
## 자바스크립트의 대화
### 프롬프트 대화창
- 사용자로부터 문자열을 입력받아 반환

    var ret = propmpt("message", "default input");
### 확인 대화창
- 메시지 출력후 확인/취소 버튼이 출력
- 확인을 누르면 true, 취소면 false 반환

        var ret = cofirm("메시지");
### 경고 대화창
- 메시지와 확인 버튼을 출력

        alert("메시지");
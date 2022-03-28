## GIF
- 비트맵 그래픽 파일 포맷
- 이미지에서 평균적으로 많이 쓰는 색 256개만 선정하여 인덱스를 만들고 색 정보를 컬러 인덱스로 대치하여 이미지 용량을 줄이는 방식
- 색상 표현에 한계가 있음
- 이미지 용량이 작음

#
## PNG
- 비손실 그래픽 파일 포맷
- GIF 처럼 색상수를 줄인 압축 포맷
- 기본 트루컬러(24비트)를 지원
- 비손실 압축을 사용하므로 이미지의 형태 변형이 없음

#
## JPG
- 정지 화상 손실 압축 표준
- GIF와 다르게 RGB 컬러 정보를 유지
- 압축으로 인한 이미지 손실이 있음
- 파일 용량이 적음

#
## SVG
- 벡터 이미지
- 이미지의 모든 그래픽 객체 정보를 수치로 담음
- 벡터 : 이미지의 객체들을 픽셀 단위로 그 정보를 담는 것이 아니라 시작과 끝의 좌표로 이미지 내 객체 정보를 표현하므로 용량이 줄어 듬

#
## 쿠키
- 방문한 서버가 사용자 컴퓨터에 나중 사용을 목적으로 저장해 놓은 작은 크기의 파일
- 사용자 컴퓨터에 설치 되어 반복 사용되는 기록서 이고 새 정보로 수시 변경이 가능

#
## 웹 서버
- 특정 목적의 정보의 HTML 문서를 저장 관리하고 사용자의 요청에 따라 문서를 검색하고 처리하는 사이트 컴퓨터의 프로그램

#
## 웹 서버 고급 기능
### 인증
- HTTP 요청 메시지의 송신 브라우저의 합법성을 확인하는 인증서로 인증
### 보안
- HTTP 보안 버전 HTTPS는 TCP 연결을 SSL로 암호화
### 콘텐츠 압축
- 정보양을 줄여 전송속도 증가
### 가상 호스팅
- 물리적 호스트에 여러 도메인을 허용하는 방식
### 로드 밸런싱
- 한 도메인에 여러 물리적 서버를 할당하여 대역폭을 조정
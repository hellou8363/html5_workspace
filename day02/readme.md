## Study Record
\
**Scoop을 이용한 tomcat9 설치**  
```
scoop update
scoop search tomcat9
scoop install tomcat9
scoop info --verbose tomcat9
cd $env:CATALINA_BASE
dir
cd bin
dir
configtest 입력 후 tab -> Enter
catalina.bat 입력 후 tab -> Enter
.\catalina.bat run -> tomcat 구동
.\catalina.bat stop -> tomcat 구동 중단
```  
\
**Server 구동**: startup.bat  
**Server 중단**: shutdown.bat  
\
\
**CMD 창에서 한글 깨짐 방지**
```
cd $env:CATALINA_BASE
cd ..
cd conf
code -r .\logging.properties -> vscode에서 파일 open

--------- logging.properties(리소스 번들 파일) ----------
java.util.logging.ConsoleHandler.encoding = UTF-8 -> MS949로 변경
---------------------------------------------------------
```  
\
**IPv4 Address 조회 명령어(cmd)**  
Windows: ipconfig  
Mac: ifconfig  
Linux: ip addr show  
\
\
**Web Server 접속(tomcat)**  
[http://127.0.0.1:8080/](http://127.0.0.1:8080/)  
[http://localhost:8080/](http://localhost:8080/)  
\
\
**사용 중인 Port 조회**

```
scoop info --verbose sysinternals
cd $(scoop prefix sysinternals)
.\tcpview.exe
---------------------------------
TCPView에서 TCP v4탭만 활성화 -> Local Port에서 사용 중인 Port 확인
tomcat의 경우 Process Name이 java.exe (자바로 만들었기 때문)
```  
\
**URL & URI**
```
<------------ URL ------------>
http://localhost:8080/ttt/1.png
					  <- URI ->

URL: Uniform Resource Locator
⇒ 단일한 방법으로, 웹에 공개된 자원의 “위치”를 알려주는 주소)

URI: Uniform Resource Indicator
=> 단일한 방법으로, 웹에 공개된 자원의 "의미"를 알려주는 URL의 일부분
```
\
**REST Client(Huachao Mao) 확장 설치**  
test.http 파일 생성 및 샘플 테스트 코드 입력
```
GET http://localhost:8080/tomcat.css  
```
Send Request 수행 => 단축키: Ctrl + Alt + R  
Response view 확인 가능
- code line: 1 ~ 8 => Header
- code line: 10 ~ => Body  
  
Header와 Body 사이에 공백 한 줄로 구분  
Body(Payload)는 size의 제약 X, 메모리에 대한 제약 O  
\
\
**HTTP 통신규약(Protocol)의 특징**
1. Client와 Web Server가 연결됨(Connection 생성)
2. 정해진 규약에 따라,
   - HTTP request를 웹 서버로 전송하고
   - HTTP response를 클라이언트로 보내면
3. 1의 Connection을 바로 끊어버린다.  

특징: Connectionless Protocol, Stateless Protocol  
\
\
**Tomcat Server에 Manager계정 추가**  
scoop으로 tomcat 설치 시 계정이 없음  
```
cd $env:CATALINA_BASE
cd conf
code -r .\tomcat-users.xml
---------------------------- vscode에서 open된 후 아래 코드 추가
<role rolename="manager-gui" />
<role rolename="admin-gui" />

<user username="tomcat" password="tomcat" roles="manager-gui,admin-gui" />
---------------------------- tomcat server 재구동
```  
\
http://localhost:8080/manager 로 접속(생성 계정으로 접속)  
 
경로 목록 → /examples → Servlets examples  
→ Hello Word ~ Sessions까지 Execute로 확인 가능  
\
\
**HTML 문서를 구성하는 태그(tag)**  
<시작태그이름> ~ </종료태그이름>  
<시작태그이름/> ⇒ 단축형, 시작/종료 태그 사이에 내용이 없을 경우  
태그는 속성을 가질 수 있다(대신, 시작태그에만 속성이 올 수 있음).  
예) <person 주민번호=”123456-1234567” />

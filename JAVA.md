![자바..](https://github.com/yhs0429/TIL/blob/master/png/1_J76LX5mvMD-bP1qCj8PQpA.png)

개발자가 되어보자고 맘 먹고 아무것도 모르는 상태에서 공부를 시작하게 되었다... 정말 처음 접해보는 신세계다.

아직도 잘은 모르겠지만 꾸준히 하다보면 눈에 잘 들어오는 날이 오겠지..

나라에서 공짜로 해주는거니 열심히 들어서 내꺼로 만들어보자 !



## Java 란 ?

- 프로그래밍 언어 중에서 C, C++과 같은 **고급언어**에 속한다
- 제임스 고슬링 형님께서 1991년 언어를 만들고 1995년 5월 공식적으로 발표했다



## Java의 특징

- 이식성이 좋다 - OS에 구애받지 않고 사용 가능
- 바이트 코드(byte code) - JVM에서 동작 , class파일에 저장된다
- 객체 지향 언어(OOP : Object Oriented Programming)
- 함수적 스타일 코딩 지원 - 람다식(Lambda Expressions) 지원
- 메모리 자동 관리 - 객체 생성시 자동으로 메모리 할당, 사용 완료 후 GC(Garbage Collecotr)가 사용하지 않는 객체 자동 삭제
- 다양한 애플리케이션 개발 가능 - 거의 모든 곳에서 실행되는 프로그램 개발 가능
- 멀티 스레드(Multi - Thread) 구현가능 - 동시에 여러가지 작업 및 대용량 작업 처리 빠르게 가능
- 동적 로딩(Dynamic Loading)지원 - 필요할때만 메모리 확보 , 유지보수 쉽고 빠르게 가능
  - 정적 로딩(Static Loading) - 처음부터 메모리 확보 , 메모리 많이잡아 먹음

- 오픈 소스 라이브러리 풍부!



## Java 개발 환경 구축

자바 파일은 (.java) JVM 으로만 실행할 수 있다.

- **JDK**  (Java Devolopment Kit)
  - 자바 응용 개발 환경으로 **개발**에 필요한 도구 포함
  - 컴파일러, JRE , 클래스 라이브러리 , 샘플 등

- **JRE**
  - 자바 실행 환경으로 JVM 역활을 하는 소프트웨어
  - 자바 실행 환경만 필요한 경우 사용

``` 
개발자들은 최신판이 아니라 구판을 사용 한다고 한다 ! 
🙄why? 최신판보다 구판이 오히려 안정적이며 모든 사람들이 최신판을 사용하지 않기 때문
```

```
자바 설치 후 환경 변수 지정 
 - 환경 변수의 설정 (내 PC -> 속성 ->정보 -> 고습시스템 설정 -> 고급 -> 환경변수) 
     . 경로와 경로사이는 반드시 ";"으로 구분을 해주어야 합니다. 
     . 일반적으로 환경변수명은 대문자를 사용합니다.
     . path는 기존내용이 지워지지 않도록 키보드 Home 키를 누른후 작성한다.

  - JAVA_HOME : C:\Program Files\Java\jdk1.8.0_151 (자바설치위치)
  - CLASSPATH : .;%JAVA_HOME%\lib\tools.jar
  - Path : %JAVA_HOME%\bin;기존패스
            ; 구분값
            
JDK설치 확인
 - cmd 창에서 JDK설치 확인
 java -version
 echo %JAVA_HOME%
 echo %CLASSPATH%
 echo %path%
 javac
 java            
```



## 이클립스

수월하게 개발하기 위한 도구

1. 이클립스 셋팅

   - 유니코드 UTF-8 로 변경  

   ```Window ``` →```General```→```Content Types```→```Text```→```Default encoding UTF-8 설정```

   ```General```→```workspace```→```Text file encoding UTF-8확인```

   - **글꼴**```General```→```Apperance```→```Colors and Fonts```→```Basic```→```Text Font```(글꼴 세로출력 , 12이상)
   - **취소 버퍼 크기** ```General```→```Editors```→```Text Editors```→```Undo history size : 20480, Display tab width :2```
   - **라인 번호** ```General```→```Editors```→```Text Editors```→```"Insert spaces for Tabs, Show Line Number"```
   - **TAB의 공백 지정** ```Java```→```Code Style```→```Formatter```→```New..Button click```→```Profile name : Java```→```Indentation > Tab policy>"Spaces only"```→```Indentation size : 2 Tab size : 2```\



## 식별자

- 클래스 이름, 메소드 이름, 변수 이름 등을 말한다
- 이름 자체로 어느정도 내용을 알 수 있게해야함
- 대소문자 구분! Test tese 서로 다름

1. 식별자 규칙

   1. 일반문자 사용가능
   2. $, _ 를 제외한 모든 특수문자 사용불가
   3. 숫자 두번째부터 사용가능 

   - 잘못된 식별자 예

     int 3Chapter; 숫자 사용

     class if{} if는 자바의 예약어

     char false; false는 사용불가

     void null(){} nell 사용불가

     class %calc{} %특수문자 불가

2. 
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

2. 메소드명,필드,멤버변수 

   1. 첫자는 일반적으로 소문자 사용
   2. 메소드의 마디는 대문자 사용

3. 변수(Variable)

   1. 하나의 값을 저장할 수 있는 메모리 공간 (date 저장하는 그릇)
   2. 변수는 데이타타입과 함께 선언하며, 초기화 한 후 사용한다
   3. 메소드 내에서 선언된 변수는 로컬변수(local vairable)라고 칭하며 메소드 실행이 끝나면 메모리에서 자동삭제 된다



## 데이터 타입

모든 변수에는 타입이 존재하며 타입에 따라 저장할 수 있는 값의 종류와 범위가 달라짐

![데이터타입](https://github.com/yhs0429/TIL/blob/master/png/java03_01.jpg)

1. 자바의 8가지 기본형 타입

   1. 논리형 

      - boolean : 1Byte(8 Bit)
      - 값의 범위 : true , false

   2. 문자형

      - char : 2Byte(16Bit)
      - 문자 한 글자를 나타냄 ,  ' ' 로 표현

   3. 숫자형 ( 정수 )

      - **long 타입은 뒤에 L을 붙인다 (int타입 보다 큰 정수일때)**

        !(숫자형 정수)[]

   4. 숫자형 ( 실수 ) 

      - float : 4Byte  float 타입 변수에는 뒤에 f , F 를 붙여야 사용가능
      - **double : 8Byte **

## 참조 타입(레퍼런스 타입)

- 클래스, 배열, 인터페이스
- 변수에 참조값(해쉬코드)을 갖는다
- String타입이 많이쓰임

```
   String  str = "왕눈이"; 
            │ 
            └----> 참조값(해쉬코드)
            
   StringBuffer *sb*  =  new  StringBuffer();



   Object b = new Object(); 
           │ 
           └----> 참조값(해쉬코드) 


   int[]   *ia*   = {100, 200, 300, 400, 500};

```

## 형변환 (data type casting)

- 실수를 정수로 바꾸는것이 형변환
- Casting시에는 데이터 짤림이 발생하는지 확인해야한다
- 데이터 짤림이 발생하면 캐스팅은 피해야 한다 

```

        |              double        (자동 변환) 
        |                                 ▲ 
        |               float             | 
        |                                 | 
        |               long              | 
        |                                 | 
        |                int              | 
        |                                 | 
        |            short, char          | 
       ▼                                  | 
   (casting)            byte              | 

```

## 연산자

- 연산에 사용되는 표시나 기호

![연산](https://github.com/yhs0429/TIL/blob/master/png/java04-01.jpg)

![증가/감소 연산자](https://github.com/yhs0429/TIL/blob/master/png/1.jpg)



## 조건문(if,switch)

**1. if문**

- 조건식의 결과에 따라 블록 실행 여부가 결정됨

- 조건식에는 true/false 값을 산출하는 연산식 or boolean 변수 사용 가능

- 조건식이 true일 때 블록실행 , false면 블록 실행 안함

  ``` 
  if(조건식){
  
  	참일 경우 실행;
  
  	참일 경우 실행;
  
  }
  ```


**2.if-else문 + if-else문**

- if문의 조건식이 true면 if블록을 실행하고 , false면 else 블록 실행되는 조건문
- else if 는 제한없이 추가가능, 마지막에는 else로 끝낸다.

```
if(조건식){
실행문;
}else if(조건식){
실행문;
}else if(조건식){
실행문;
}else{
실행문;
}
```

**3.중첩if문**

- if문 내부에 if문을 또 사용한 것

```
if (조건식){
	if(조건식){
		실행문;
	} else {
		실행문;
  }else{
  	실행문;
  } 
}
```

**4.switch문**

- switch문에는 조건식 사용안함
- 변수의 값에 따른 실행문을 선택해서 실행문이 결정됨 (if문 보다 간결하게 작성가능)
- switch() 괄호안에는 정수타입 , String타입 의 변수만 들어갈수있음
- case뒤에는 **break;** 가 있어야 한다
- case가 없으면 default 실행 (default 생략가능)

```
switch(정수타입,String타입){
case 1: 실행문1; break;
case 2: 실행문2; break;
case 3: 실행문3; break;
default: 실행문4; break; // defualt 생략가능
}
```

## 반복문 

**1.for문**

- 지정한 횟수만큼 실행문을 반복하는 반복문 , 반복시킬 횟수를 알고 있을때 사용하는것이 일반적
- 초기화식에서 루프 카운트변수를 선언할때에는 부동소수점 타입 사용 x 

```
for(int i=0; i<5 i++){
실행문;
}
```

```
for문 도 중첩가능
for(int i=0; i<5; i++){
	for(int j=0; j<5; j++){
	System.out.println("i="+i+", j="+j+)
	}
}
```

**2.while문**

- while문 은 조건식이 true면 무한반복 (false 되면 멈춤)
- 조건식에는 true/false 값을 내는 연산식이나 boolean 변수 사용
- 무한반복되는 while문을 빠져나가기 위해 break를 사용함

```
while(조건식){
실행문;
}
```

```
while문 도 중첩가능
while(조건식){
실행문;
	while(조건식){
	실행문;
	}
}
```

**3.do-while문**

- 실행문부터 먼저 실행하고, 실행문의 결과에 따라 루프 여부를 결정할때 쓰는 반복문

```
do{
	실행문;
}while(조건식);
```

```
do-while문 예제
	Scanner sc = new Scanner(System.in);
	int sum = 0;
	int n;
	do {
		String input = sc.nextLine();
		n = Integer.parseInt(input);
		sum += n;
	} while (n != 0);
	System.out.println(sum);
	}
}
```

**4.break문**

- switch문이나 반복문을 종료할때 씀

```
예제
	int sum = 0;
	int i;
	for (i=1;;i++) {  // while (true) = for (;;)
		sum += i;
		if (sum>=100) break;
	}
	System.out.println("Sum: " + sum + ", i: " + i);
	}
}
```

- 반복문이 중첩되어 있는 경우, 가까운 반복문을 종료하며 바깥쪽 반복문은 종료안함
- 바깥쪽 반복문까지 종료원할시 바깥쪽 반복문에 이름(라벨)붙이고 **break 이름;** 사용

```
	Outter: for (int i=0; i<10; i++) {
		for (int j=0; j<10; j++) {
			System.out.println("i: " + i + ", j: " + j);
			if (j==3) break Outter;
			}
		}
	}
}
```

**5.continue 문**

- continue문은 반복문(for,while,do-while문)에서만 사용
- continue문은 breack문과 반대로 반복문의 조건식으로 이동하여 무한반복시킴

```
	// 1 - 100 중 3의 배수가 아닌 수의 합
	int sum = 0;
	for (int i=1; i<=100; i++) {
		if (i%3==0) continue;  // 증감식으로 바로 이동, 3의 배수 건너뛰기
		sum += i;
		}
		System.out.println(sum);
	}
}
```


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

- **JDK** (Java Devolopment Kit)

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

   `Window ` →`General`→`Content Types`→`Text`→`Default encoding UTF-8 설정`

   `General`→`workspace`→`Text file encoding UTF-8확인`

   - **글꼴**`General`→`Apperance`→`Colors and Fonts`→`Basic`→`Text Font`(글꼴 세로출력 , 12이상)
   - **취소 버퍼 크기** `General`→`Editors`→`Text Editors`→`Undo history size : 20480, Display tab width :2`
   - **라인 번호** `General`→`Editors`→`Text Editors`→`"Insert spaces for Tabs, Show Line Number"`
   - **TAB의 공백 지정** `Java`→`Code Style`→`Formatter`→`New..Button click`→`Profile name : Java`→`Indentation > Tab policy>"Spaces only"`→`Indentation size : 2 Tab size : 2`\

## 식별자

- 클래스 이름, 메소드 이름, 변수 이름 등을 말한다
- 이름 자체로 어느정도 내용을 알 수 있게해야함
- 대소문자 구분! Test tese 서로 다름

1. 식별자 규칙

   1. 일반문자 사용가능
   2. $, \_ 를 제외한 모든 특수문자 사용불가
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
      - 문자 한 글자를 나타냄 , ' ' 로 표현

   3. 숫자형 ( 정수 )

      - **long 타입은 뒤에 L을 붙인다 (int타입 보다 큰 정수일때)**

        !(숫자형 정수)[]

   4. 숫자형 ( 실수 )

      - float : 4Byte float 타입 변수에는 뒤에 f , F 를 붙여야 사용가능
      - **double : 8Byte **

## JVM의 메모리 사용영역

1. 메소드 영역 (Method Area)

   - .class 같은 실행할 명령어들이 있는 영역

   - 메소드 영역은 JVM이 실행될 때 생성되고 모든 스레드가 공유하는 영역

2. 힙 영역(Heap Area)

   - 객체와 배열이 생성되는 영역

   - 사용되지 않는 객체는 GC(Grabage Colletor)가 자동 제거

3. JVM 스택 영역(JVM Stack Area)
   - 각 스레드마다 하나씩 존재 , 스레드가 시작될 때 할당됨
   - JVM 스택은 메소드를 호출할 때마다 프레임을 추가하고 메소드가 종료되면 해당 프레임을 제거함
   - 기본 타입 변수는 스택 영역에 직접 값을 갖고 있으나 , 참조 타입 변수는 힙 영역이나 메소드 영역의 객체 주소를 가진다

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

## [조건문]()(if,switch)

### if문

- 조건식의 결과에 따라 블록 실행 여부가 결정됨

- 조건식에는 true/false 값을 산출하는 연산식 or boolean 변수 사용 가능

- 조건식이 true일 때 블록실행 , false면 블록 실행 안함

  ```
  if(조건식){

  	참일 경우 실행;

  	참일 경우 실행;

  }
  ```

### if-else문 + if-else문

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

### 중첩if문

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

### switch문

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

### for문

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

### while문

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

### do-while문

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

### break문

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

### continue 문

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

## 배열

같은 타입의 많은 데이터를 순차적으로 저장하는 공간으로 인덱스를 사용함

- 배열은 객체로서 힙 영역에 생성, 배열 변수는 배열 객체를 참조함
- 배열 타입도 참조 타입에 속하므로 null로 초기화 할 수 있다
- **장점** :

  - 통일된 하나의 변수로 다량의 데이터를 처리할 수 있다
  - 반복문을 사용해서 많은 양의 데이터를 쉽게 처리 할 수 있다

- **단점**:

  - 같은 타입의 데이터만 저장 할 수 있다
  - 배열의 길이를 생성할 때 결정하기 때문에 변경할 수 없다
  - 배열의 요소를 선언하고 전부 이용하지 않으면 심각한 메모리 낭비가 발생함

- 배열의 사용 예:

  - 사이즈가 변경되지 않는 데이터 배열 (1~12월 , 월~일요일 , 학교의 학년 ....)

- 다차원 배열 :
  - 2차원 배열은 일반적으로 for문을 2개이상 동반함

## 객체지향 프로그래밍

### 객체의 특징

- 물리적으로 존재하는 것과 추상적으로 생각할 수 있는 것 중에서 **속성과 동작을 가지는 모든**것이 객체

- 필드(속성)와 메소드(동작)로 구성된 자바 객체로 모델링이 가능

- 객체끼리 서로의 기능(동작)을 이용하고 데이터를 주고 받음 **객체의 상호 작용**

- 객체는 상호 작용 수단으로 메소드를 호출함

### 객체간의 관계

- 집합 관계 : 완성품 - 부품

- 사용 관계 : 객체 - 객체, 한 객체가 다른 객체의 메소드를 호출하여 사용

- 상속 관계 : 종류 객체(상위 객체) - 구체적인 사물 객체(하위 객체)

### 객체 지향 프로그래밍의 특징

- 부품에 해당하는 객체들을 먼저 만든다음 조립하여 하나의 프로그램을 완성시키는것

- 캡슐화

  객체의 필드와 메소드를 하나로 묶어서 구현 내용을 감춤. 외부 객체는 객체 내부의 구조를 알 수 없으며

  해당 객체의 필드와 메소드만 이용 가능. 캡슐화하여 보호하는 이유는 외부의 잘못된 사용으로 객체가

  손상되는 것을 방지하기 위함. 캡슐화를 위해 자바는 접근제한자(Access Modifier)를 사용함

- 상속

상위 객체의 필드와 메소드를 하위 객체에 물려주는 것. 하위 객체는 상위 객체를 확장해서 추가적인

필드와 메소드를 가질 수 있다

- 다형성

  같은 타입이지만 실행 결과가 다양한 객체를 대입할 수 있는 성질. 자바는 인터페이스나 부모 클래스의 타입 변환이 가능하다.

## 객체와 클래스

- 자바에서는 클래스가 설계도에 해당 ✔**클래스(붕어빵틀) , 객체 (붕어빵)**

- 클래스로부터 만들어진 객체를 해당 클래스의 인스턴스라고 하며, 그 과정을 인스턴스화 라고 한다
- 객체의 구성요소
  - 속성 = 변수
  - 기능 = 메소드

### 클래스 선언방법

- 하나 이상의 문자로 구성
- 첫글자는 숫자,$,\_ 외의 특수문자,자바 키워드 불가
- 영어로 작성하는것이 관례 대소문자 구분
- 각 단어의 첫문자를 대문자로

### 객체 생성 방법

- new 연산자가 클래스로부터 객체 생성(인스턴스화) 역활을 함

## 클래스의 구성 멤버

- 필드
  - 객체의 데이터가 저장되는 곳
- 객체 생성 시 초기화 역활을 담당(실체는 메모리)
- new 연산자로 생성자가 성공적으로 실행되면 힙 영역에 객체가 생성되고 객체의 주소가 리턴됨
- 모든 클래스는 생성자가 반드시 존재하며, 하나 이상을 가질 수 있다
- 메소드와 비슷한 모양이지만 리턴 타입이 없고 클래스 이름과 동일
- 클래스에 생성자가 명시적으로 선언되어 있는 경우에는 반드시 선언된 생성자를 호출해서 객체 생성해야함(기본생성자 호출 불가)

# 멤버메소드

- C언어의 함수와 비슷
- 데이터 처리 기능을 구현
- 리턴값이 없는 메소드는 **void**형을 지정
- 메소드가 받는 인수의 데이터 타입은 메소드를 호출하는 쪽과 일치해야함
- 메소드 오버로딩(중복정의),오버리딩(재정의)기술로 확장됨
- 메소드가 리턴하는 값과 리턴되는 값의 데이터 타입은 일치해야함

```
세금계산 메소드
   public int taxCalc(){
       return (int)(bonbong * 0.045 + 0.5);
    }

 실수령액 계산 메소드 --
    public int silsuCalc(){
        return money - taxCalc();
    }

 데이터 출력메소드  -- 리턴값 없으므로 void형으로 지정
   public void printPay(){
      System.out.println("--------------------");
       System.out.println("---12월 급여 내역---");
       System.out.println("--------------------");
       System.out.println("성명: " + name);
       System.out.println("본봉: " + bonbong);
       System.out.println("세금: " + taxCalc());
       System.out.println("실수령액: " + silsuCalx());
    }
```

- 매개변수 있는 메소드와 매개변수 없는 메소드
  - 캡슐화된 멤버변수 초기화를 위한 setter메소드 선언(매개변수 존재)
  - 캡슐화된 멤버변수의 값을 가져오기 위한 getter 메소드 선언(매개변수 존재안함)
  - 멤버변수가 캡슐화 되어 다른 클래스에서 접근이 불가 할 때 setter,getter 메소드 추가하여 사용

```
   public void setName(String name){

    this.name = name;
    }
    public String getName(){
    return name;
    }

    public void setBonbong(int bonbong){
    this.bonbong = bonbong;
    }

    public int getBonbong(){
    return bonbong;
    }
```

## 변수의 유효 범위(scope)

- 멤버 변수 (instance 변수)
  - 변수가 메소드 밖에 선언되는 변수 (멤버변수,인스턴스변수,필드 라고 한다)
  - 멤버 변수는 모든 메소드에서 사용 가능
  - 메모리 모델에서 Heap 메모리 이용
  - 변수 선언시 값을 주지 않아도 특정 값으로 초기화됨

📌변수 사용 후 클래스의 객체 자체가 gc에 의해 회수 되기 전에는 할당받은 메모릴 계속 유지함

불필요한 변수 사용은 메모리 낭비!!

- 지역 변수 (Local Variable)
  - 변수가 메소드 안에서 선언되는 것
  - Stack 메모리를 이용
  - 메소드의 이용이 끝나면 자동으로 메소드 영역이 없어져 변수도 회수됨
  - 초기화를 해야 사용할 수 있다

```
public class Variable {
    //멤버 변수, 인스턴스 변수, 필드, Heap
    String movie = "트로이";

    //지역변수가 없음으로 전역변수가 출력
    public void show(){
        System.out.println("show 메소드 영역:" + movie);//트로이
    }

    //지역변수가 우선으로 출력됩니다. Stack
    public void title(){
        String movie = "아마겟돈";
        System.out.println("title 메소드 영역:" + movie);
        System.out.println("title this.movie:" + this.movie);
    }

    public static void main(String[] args) {

        Variable v = new Variable();
        v.show();
        v.title();
    }
}

```

## Call By Value / Reference

- Call By Value : 값에 의한 호출
  - 메소드로 한 문자 , 상수 문자열, 숫자를 전달하면 전부 값에 의한 호출이라고 하고 Call By Value 라 한다

```
class Code {
  public String getArea(int index){ // Call By Value
    // 1차원 배열
    String[] areas = {"서울", "천안", "대전", "대구", "광주", "강릉"};
    //                        0       1       2        3         4       5

    return areas[index-1]; // String return
  }
}
public class CodeUse {

  public static void main(String[] args) {
    Code co = new Code();
    String area = co.getArea(6);

    System.out.println(area);

  }

}
```

- Call By Reference : 참조값에 의한 호출 (Hash Code)

  - 메스드로 참조type 을 전송 할 수 있다

  - 메소드로 클래스의 객체를 전달하면 메모리가 전달되는 것이 아닌 객체의 Hash Code가 전달됨으로

    Call By Reference 라고 함

  - Call By Reference의 경우 참조값(Hash Code)을 전달한 객체는 자신의 참조값이 전달됨으로 값의 변화가 발생할 수 있고 heap memory를 공유한다.

```
class Pay{
int ppp;
public void payRefer(Pay a){
a.ppp = a.ppp + 2000;
}
public void payValue(int j){
j = j + 2000;
}
}


public class PayTest {
public static void main(String[] args) {
Pay p = new Pay();
p.ppp = 10;

int i = 10;

p.payRefer(p); //call by reference로 전달
p.payValue(i); //call by value로 전달

System.out.println(p.ppp); //객체가 변경되서 2010
System.out.println(i);//10
}

}
```

📌String 객체의 특징 !!

- 한번생성된 객체는 불변이다

- 클래스를 객체화할때 new를 사용하지만 String은 사용하지 않아도 된다

- 메모리상에서 같은 문자열은 공유 한다

  - String name = "크롱";

  - String str = "크롱";

    name hashcode와 str hashcode는 같다

- 변경되는 객체가 있을 때 마다 새로운 객체가 만들어진다

## Method Overloading

- 같은 클래스 내에서 같은 이름의 메소드를 여러개 선언하는 것을 말한다

- 호출하는 이름은 같지만 , 파라미터의 개수나 타입이 다르다 , 파라미터의 개수가 같다면 타입이 다름

  return타입은 다를 수 있다

```
   - method overloading의 대표적인 경우
     System.out.println(1);
     System.out.println(1.5);
     System.out.println("우리는 한국인입니다.");
     System.out.println("IT 기술을 " + " 다양한 분야로 적용해야 합니다.");

   - 메소드 오버로딩을 사용하지 않는 경우
     public void printInt(int x){ }
     public void printFloat(float x){ }
     public void printString(String x){ }

     │
     │
     ↓

     메소드 오버로딩을 적용한 경우

     public void println(int x){ }
     public void println(float x){ }
     public void println(String x){ }



   - PrintStream 클래스의 메소드 오버로딩예

     void print(char c){ }   //print('C')

     void print(double d){ } //print(10.5)

     void print(float f){ }  //print(10.5f)

     void print(int i){ }    //print(10)
```

- 메소드가 호출되는 경우 메소드의 인수 데이터 타입과 갯수가 일치하는 메소드가 호출된다
- println()메소드 및 생성자는 대표적인 메소드 오버로딩
- 한 클래스 내에서 두 개 이상의 이름이 같은 메소드 작성
- 메소드 이름이 동일 해야 함
- 메소드의 인자의 개수가 서로 다르거나 ,메소드의 인자 타입이 달라야 한다
- 메소드의 **이름,인자의 개수 ,타입** 이 모두 같은데 메소드의 리턴 타입이 다르면 메소드 오버로딩 성립안됨

```
//메소드 오버로딩 성공
class MethodOverloading{
	public int getSum(int i , int j){
	return i+j;
	}
	public int getSum(int i , int j , int k){
	return i+j+k;
	}
	public double getSum(double i, double j){
	return i+j;
	}
}
public static void main (String args[])
	MethordSampla a = new MethordSample();
	int i = a.getSum(1,2);
	int j = a.getSum(1,2,3);
	double k = a.getSum(1.1,2.2);

//메소드 오버로딩 실패
class MethodOverloading{
	public int getSum(int i, int j){
	return i+j;
	}
	public double getSum(int i , int j){
	return (double)(i+j);
	}
}
```

## 생성자(Constructor)

- return type 이 없다
- 클래스 이름이 같아야함(대소문자 구별)
- new를 이용하여 객체를 메모리에 할당한 후 할당된 메모리를 특정 값으로 초기화하는 역활
- 생성자가 없을때 기본생성자를 자동으로 만들어준다

```
// 기본 생성자 생략
class School2{
    int kuk = 0;
    int eng = 0;
    int tot = 0;

    public int hap(){
        tot = kuk+eng;

        return tot;
    }
}

public class SchoolMain2 {

    public static void main(String[] args) {
        School2 sc2 = new School2();
        sc2.kuk=90;
        sc2.eng=100;
        System.out.println("hap: " + sc2.hap());
    }
}



//기본 생성자 선언
class School3{
    int kuk = 0;
    int eng = 0;
    int tot = 0;

    public School3(){

    }

    public int hap(){
        tot = kuk+eng;

        return tot;
    }
}

public class SchoolMain3 {

    public static void main(String[] args) {
        School3 sc3 = new School3();
        sc3.kuk=90;
        sc3.eng=100;
        System.out.println("hap: " + sc3.hap());
    }
}
```

📌**기본생성자를 선언해야 하는 경우!!!**

- 인수를 받는 생성자가 존재하게되면 반드시 기본 생성자를 선언해야함
- 기본 생성자는 하는 일이 없어도 반드시 선언을 권장 !

```
class School4{
    int kuk = 0;
    int eng = 0;
    int tot = 0;

    //기본 생성자
    public School4(){ }

    //아래처럼 인수를 받는 생성자가 존재하면
    //반드시 기본 생성자를 명시적으로 선언해야 합니다.
    public School4(int kuk, int eng){
        this.kuk = kuk;
        this.eng = eng;
    }

    public int hap(){
        tot = kuk+eng;

        return tot;
    }
}

public class SchoolMain4 {

    public static void main(String[] args) {
        School4 sc4 = new School4();
        sc4.kuk=90;
        sc4.eng=100;
        System.out.println("hap: " + sc4.hap());

        School4 sc = new School4(90, 100);
        System.out.println("hap: " + sc.hap());
    }
}
```

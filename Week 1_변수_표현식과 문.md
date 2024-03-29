# 변수
## 변수(Variable) 
- 변수(Variable): 하나의 값을 저장하기 위해 확보한 메모리 공간 자체 또는 그 메모리 공간을 식별하기 위해 붙힌 이름
- 변수는 프로그래밍 언어에서 값을 저장하고 참조하는 매커니즘으로, **값의 위치를 가리키는 상징적인 이름**
- 변수는 프로그래밍 언어의 컴파일러 또는 인터프리터에 의해 값이 저장된 메모리 공간의 주소로 치환되어 실행된다. 

```javascript
const result = 10 + 20;
```
- 'result'는 **변수 이름(변수명)**, 변수에 저장된 값 '30'을 **변수 값**이라고 한다.
- 변수에 값을 저장하는 것을 **할당(assignment)** 대입/저장이라고 하고, 변수에 저장된 값을 읽어 들이는 것을 **참조(reference)** 라 한다.

### 식별자
- 변수 이름을 식별자(identifier)라고도 한다. 식별자는 어떤 값을 구별해서 식별할 수 있는 고유한 이름을 말한다.
- 식별자는 값이 아닌 **메모리 주소**로 기억한다.

## 변수 선언
- 변수 선언(variable declaration)이란 변수를 생성하는 것을 말한다. 
- 값을 저장하기 위한 메모리 공간을 확보(allocate)하고,
- 변수 이름과 확보된 메모리 공간의 주소를 연결(name binding)해서 값을 저장할 수 있게 준비해 준다. 
- 변수를 선언할 때는 **var, let, const 키워드**를 사용한다. *키워드: 자바스크립트 코드를 해석하고 실행하는 자바스크립트 엔진이 수행할 동작을 규정한 일종의 명령어
- var는 블록 레벨 스코프를 지원하지 않고, 함수 레벨 스코프를 지원하기 때문에 의도치 않게 전역 변수가 선언되어 부작용이 발생하기도 해 사용을 권장하지 않는다.

## 변수 선언의 실행 시점과 변수 호이스팅
### 실행 시점
- 자바스크립트 엔진은 소스코드를 한 줄씩 순차적으로 실행하기에 앞서 먼저 소스코드의 평가 과정을 거치면서 소스코드를 실행하기 위한 준비를 한다.
- 평가 과정: 변수 선언을 포함한 모든 선언문을 소스코드에서 찾아내 먼저 실행
- 평가과정이 끝나면 변수 선언을 포함한 모든 선언문을 제외하고 소스코드를 순차적으로 실행 
### 변수 호이스팅
- 변수 선언문이 코드의 선두로 끌어 올려진 것처럼 동작하는 자바스크립트 고유의 특징
- 변수 선언문 뿐 아니라 var, let, const, function, function* class 키워드를 사용해서 선언하는 모든 식별자(변수, 함수, 클래스 등)은 호이스팅 된다. 

## 값의 할당
- 변수 선언과 값의 할당의 실행 시점은 다르다. 
-> 변수 선언은 소스코드가 순차적으로 실행되는 시점인 런타임 이전에 먼저 실행, 값의 할당은 소스코드가 순차적으로 실행되는 시점인 런타임에 실행된다.

# 표현식과 문
## 값(Value)
- 식(표현식 expression)이 평가(evaluate)되어 생성된 결과
- 변수에 할당되는 것은 값이다.

## 리터럴(literal)
- 사람이 이해할 수 있는 문자 또는 약속된 기호를 사용해 값을 생성하는 표기법(notation)
- 리터럴을 사용하면 다양한 data type을 생성할 수 있다. (정수, 부동소수점, 2진수~16진수, 문자열, 불리언, null, undefined, 객체, 배열, 함수, 정규표현식)

## 표현식(expression)
- 값으로 평가될 수 있는 문(statement). 
- 표현식이 평가되면 새로운 값을 생성하거나 기존 값을 참조한다.
- 값으로 평가될 수 있는 문은 모두 표현식이다.

## 문(statement)
- 프로그램을 구성하는 기본 단위이자 최소 실행 단위. *문의 집합 = 프로그램, 문을 작성하고 순서에 맞게 나열하는 것 = 프로그래밍
- 문은 여러 토큰(token)으로 구성된다. *토큰: 문법적인 의미를 가지며, 문법적으로 더이상 나눌 수 없는 코드의 기본 요소(키워드, 식별자, 연산자, 리터럴, 세미콜론, 마침표 등 특수기호)
- 문은 명령문이라고도 부른다.
- 선언문, 할당문, 조건문, 반복문 등으로 구분한다.

## 세미콜론
- 문의 종료 (;)
- 0개 이상의 문을 중괄호로 묶은 코드 블록 뒤에는 붙이지 않는다. (if 문, for 문, 함수 등)

## 표현식인 문과 표현식이 아닌 문
- 구별하는 가장 간단한 방법은 **변수에 할당해 보는 것**이다.


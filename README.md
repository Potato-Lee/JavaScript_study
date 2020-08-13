# JavaScript_study 
 [mdn의 JavaScript 재입문하기(JS 튜토리얼)](https://developer.mozilla.org/ko/docs/A_re-introduction_to_JavaScript)
 ## JavaScript 타입
* 수(Number)
* 문자열(String)
* 부울(Boolean)
* 함수(Function)
* 객체(Object)
* 기호(Symbol)
* 정의되지 않음(Undefined)
* 널(Null)
* 객체
	* 배열(Array)객체
	* 날짜(Date)객체
	* 정규식(RegExp)객체
### 수(Numbers)
* 덧셈, 뺄셈, 계수 (또는 나머지) 연산을 포함하는 표준 산술 연산자가 지원됨
* 또한 고급 수학 함수와 상수를 다루기 위한 Math 내장객체가 있음
```
Math.sin(3.5);
var circumference = 2 * Math.PI * r ;
```
* 내장 parseInt()함수를 사용하여 문자열을 정수로 변환가능
* parseInt() 함수가 0으로 시작되는 문자열을 8진수로, "0x"로 시작하는 문자열은 16진수로 취급하기  
때문에 발생함
* parseFloat()를 사용하여 부동 소수점 숫자를 파싱할 수 있음 (항상 10진수를 사용한다.)
* 단항 연산자 + 사용하여 값을 숫자로 변환할 수 있음
```
+'42'; //42
+'010'; //10
+'0x10'; //16
```
* 문자열이 수가 아닌 경우 NaN("Not a Number")
* isNaN()함수 이용해서 검사

<hr/>

### 문자열(Strings)
JavaScript에서 문자열은 유니코드 문자들이 연결되어 만들어진 것 (문자열도 객체로 취급됨)  
문자열도 객체로 취급되므로 메소드도 포함함

<hr/>

### 이외의 타입들
객체'null'(값이 없음)  
'undefined'(초기되지 않은 값, 할당되지 않은 변수)  
JavaScript에서 변수에 값을 주지 않고 선언하는 것이 가능  
변수의 타입은 undefined가 됨  
* 부울타입을 가짐(true,false값을 가지는), 어떤 값을 부울값으로 변환할 수 있음
	1. false, 0, 빈 문자열(" "), 수가 아님을 뜻하는 NaN,null, undefined 모두 false
	2. 다른 모든 값은 true
```
Boolean( ' ' ); //false
Boolean(234); //true
```
* 반드시 Boolean()함수를 사용할 필요는 없음, 이러한 작업은 if문과 같이 부울값이 필요한 경우를 만나게 되면 자동으로 사용자가 모르는 사이에 처리해줌
* 부울 연산자는 &&(그리고), ||(또는), !(부정)이 지원됨

<hr/>

### 변수(Variables)
JavaScript에서 let, const, var 키워드를 사용하여 변수 선언  
let을 사용하여 블록 유효 범위 변수를 선언가능  
선언된 변수는 변수가 포함된 함수 블록에서만 사용 가능  

const로는 변경되지 않는 변수를 선언할 때 사용하고 var는 가장 일반적인 키워드
var로 선언된 변수는 변수는 let, const가 가지는 제한을 가지지 않음, 그리고 변수가 선언되 함수 내에서만 사용이 가능함  
JavaScript는 함수에만 범위가 존재함, let, const를 사용하여 블록 범위 변수를 만듬

<hr/>


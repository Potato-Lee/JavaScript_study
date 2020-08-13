# JavaScript_study 
 [JavaScript 재입문하기](https://developer.mozilla.org/ko/docs/A_re-introduction_to_JavaScript)
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

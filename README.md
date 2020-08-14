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
var array=[1,2,3,4,5];
Math.max(array);
```
* 내장 parseInt()함수를 사용하여 문자열을 정수로 변환가능
* parseInt() 함수가 0으로 시작되는 문자열을 8진수로, "0x"로 시작하는 문자열은 16진수로 취급하기  
때문에 발생함
* parseFloat()를 사용하여 부동 소수점 숫자를 파싱할 수 있음 (항상 10진수를 사용한다.)
* 단항 연산자 + 사용하여 값을 숫자로 변환할 수 있음
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
* JavaScript에서 let, const, var 를 사용하여 변수 선언  
* let을 사용하여 블록 유효 범위 변수를 선언가능  
선언된 변수는 변수가 포함된 함수 블록에서만 사용 가능  

* const로는 변경되지 않는 변수를 선언할 때 사용하고 var는 가장 일반적인 키워드
* var로 선언된 변수는 그 변수가 선언된 함수 내에서만 사용이 가능함  
* JavaScript는 함수에만 범위가 존재함, let, const를 사용하여 블록 범위 변수를 만듬

<hr/>

### 연산자(Operators)
* 산술 연산자 +, -, *, /, %
* = 연산자로 값을 할당
* += (x=x+y), -= (x=x-y)  
* 증감연산자,  ++, --
* +연산자는 문자열을 이어붙임(문자열에 어떤 수를 더하면 모두 문자열)
``` '3' + 4 + 5 + 6; //"3456" ```
* !=, !== 연산자
* 비교연산자 <, >, <=, >=, 이 연산자들은 문자열과 수 양쪽에서 다 동작 가능
* 이중 등호( == )연산자는 피연산자가 다른 타입일 때 타입 강제 변환을 수행하므로 기대하지 않은 결과를 줄 수 있음
```
123 == '123'; //true
1 == true; //true
```

<hr/>

### 제어구조
* if else( 중첩가능 )
* while반복문
* do-while반복문
* for 반복문
* switch case문
* for...of문
```
for(let value of array){
	//value로 작업을 실행함
}
```
* for...in
```
for(let property in object){
	//object의 항목(property)으로 작업을 실행함
}
```
* &&(두개 다 true일 경우 true반환)와 ||(둘 중에 하나라도 true일경우 true반환)연산자 
* 삼중 연산자  
``` ( 조건 ) ? true : false ; ```

<hr/>

### 객체(Objects)
JavaScript내의 모든것들은 객체로 취급  
* 빈 객체를 생성하는 방법
``` var obj = new Object(); ```
``` var obj = {} ; ```
* 객체 리터럴 구문, 객체 리터럴 구문은 JSON구문의 핵심
* 객체 리터럴 구문으로 객체의 전체적인 구조를 초기화 할 수 있음

#### 리터럴(상수값)
* 문자 그대로 스크립트에 값을 제공하는 것
* 속성에 연속적으로 접근 가능  
```
obj.details.color; //orange
obj[ "details" ][ "size" ]; //12
```
객체 프로토 타입(Person)과 프로토타입의 인스턴스(you)를 생성함
```
function Person(name, age) {
	this.name = name;
	this.age = age;
}

var you = new Person('You', 24);
```
```
obj["name"] = "Simon";
var name = obj["name"];

var user = prompt('what is your key?');
obj[user] = prompt('what is its value?');
```
의미적으로 같음, 두번째 방법은 속성의 이름이 실행기간에 계산될 수 있는 문자열로 주어짐  
하지만 이 방법을 사용하면 일부 JavaScript엔진과 압축기 최적화를 적용할 수 없음  

<hr/>

### 배열(Arrays)
* 일반 객체와 비슷하게 동작
* length라는 속성을 가짐, 항상 배열의 가장 큰 인덱스보다 하나 더 큰값임  
* 존재하지 않는 배열 인덱스를 참조하려고 하면 undefined를 얻게됨
* for...in루프를 이용하여 배열에 루프를 돌릴수도 있지만, 이방법은 배열 요소를 반복하는게  
아니라 배열인덱스를 반복함  
forEach()  
```
[ 'dog', 'cat', 'hen' ].forEach(function(currentValue, index, array) {
	//currentValue나 array[index]로 뭔가를 수행
}
```
* for...of문, for...in문 사용가능, for...in문은 배열요소를 반복하는게 아니라 배역 인덱스를 반복함
* array.push(배열에 추가할 요소)

<hr/>

### 함수(Functions)
* 가장 기본적인 함수의 예
```
function add(x, y) {
	var total = x + y;
	return total;
}
```  
* 함수는 해당 함수내에서 지역적으로 변수를 보유할 수 있음  
* return문은 언제나 값을 돌려주고 함수의 실행을 끝내는데 사용될 수 있음  
(리턴문이 없으면,(혹은 값이 없는 리턴이 사용되면) JavaScript는 undefined를 돌려줌)  

* 함수가 기대하는 원래의 매개변수보다 많은 매개변수를 넘겨줄 있는, 이때 arguments객체를 사용하여 함수에 넘겨진 매개변수의 모든 값을 가지고 사용 가능, 배열과 비슷함
* 인수는 배열과 닮은것이지 배열이 아님, 인수 객체는 번호 붙여진 인덱스와 길이 속성을 가지고 있다는 점에서 배열과 닮은 것

<hr/>

### 사용자 정의 객체
this키워드, this는 현재 객체를 참조함  
해당 호출에서 dot표기법이나 bracket표기법을 사용하지 않은 경우, this는 전역 객체를 참조하게 됨 

<hr/>

### 내장함수 (Inner functions)
* 다른 함수의 내부에서 함수를 선언하는 것
* 중첩함수는 부모 함수 범위의 변수에 접근할 수 있음

<hr/>
  
### 클로저(Closures)
상태를 저장할 수 있도록 허용함, 객체의 내부에서 자주 사용될 수 있음  
함수와 함수에 의해 생성되는 범위 객체를 함께 지칭하는 용어  

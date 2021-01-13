---
description: javascript study
---

# javascript-100

{% code title="객체 리터럴 \(객체 초기화\) - 데이터 값을 객에 저장하는 방법 " %}
```javascript
const obj10 = {
name1: "array",
name2: "object"
}

const name1 = obj10.name1;
const name2 = obj10.name2;

document.write('*** 35 객체 리터럴(객체 초기화) *** <br>');
document.write(name1, "<br>");
document.write(name2, "<br><br><br>");
// -- Result --
```
{% endcode %}

## 01. 변수

자바스크립트에서는 **숫자, 문자열, 불리언** 총 세 가지의 기본 자료형이 있다. 숫자는 말 그대로 숫자이며, 숫자 그대로 사용 가능 하다. 또한, 연산\(+, -, \*, /\)이 가능하다. 문자열은 큰 따옴표로 감싼 모든 것을 문자열이라고 한다. 아래의 예로 들면 `"javascript"` 가 문자열이다. 마지막으로 불리언은 참\(true\) 또는 거짓\(false\)이 될 수 있는 값이다.

자바스크립트에서는 **변수\(variable\)**를 써서 값에 이름을 붙일 수 있다. 한 가지 물건을 넣을 수 있는 상자라고 생각하면 쉽다. 변수에는 값을 할당할 수 있으며, 그 값은 변할 수 있다.

{% code title="01. 변수" %}
```javascript
var x = 100;
var y = 200;
var z = "javascript";

document.write("*** 01 변수 *** <br>");
document.write(x, "<br>");
document.write(y, "<br>");
document.write(x + y, "<br>");
document.write(z, "<br><br><br>");

// -- Result --
// *** 01 변수 ***
// 100
// 200
// 300
// javascript
```
{% endcode %}

## 02. 배열

자바스크립트에서 **배열**은 **데이터의 값을 하나의 목록**으로 만들어 사용할 수 있다. 배열을 만드는 방법은 여러가지가 있다. 배열을 선언 해주거나 대괄호\[ \] 를 사용하는 방법이 있다. 그 중 아래의 예제는 변수에 배열을 만들겠다고 선언을 한 후, 배열의 순서대로 데이터를 할당해주는 방법이다.

{% code title="02. 배열" %}
```javascript
let arr1 = new Array();
arr1[0] = 100;
arr1[1] = 200;
arr1[2] = "javascript";

document.write("*** 02 배열 *** <br>");
document.write(arr1[0], "<br>");
document.write(arr1[1], "<br>");
document.write(arr1[2], "<br><br><br>");

// -- Result --
// *** 02 배열 ***
// 100
// 200
// javascript
```
{% endcode %}

{% hint style="info" %}
_**var, let, const 차이점**_

**var** 은 변수 재 선언이 가능하지만, **let** 과 **const** 는 변수 재 선언이 불가능하다.
{% endhint %}

{% code title="var, let, const 차이점" %}
```javascript
// var
// 이미 만들어진 변수 이름을 재 선언 했지만, 에러가 발생하지 않는다.
var a = 100;
var a = 200;

// let
let b = 100;
let b = 200; // Uncaught SyntaxError: Identifier 'b' has already been declared
b = 300; // 가능

// const
const c = 100;
const c = 200;// Uncaught SyntaxError: Identifier 'c' has already been declared
c = 300; // Uncaught TypeError:Assignment to constant variable.
```
{% endcode %}

{% hint style="info" %}
_**let, const 차이**_

**let** 과 **const** 의 차이점은 **let** 은 변수에 재 할당이 가능하지만, **const** 는 변수 재 선언, 재 할당이 모두 불가능하다.
{% endhint %}

{% code title="let, const 차이점" %}
```javascript
// let은 선언 후, 값 할당이 가능
let a;
a = 100;

// const는 선언과 동시에 값을 할당 해야 함
const b; // Missing initializer in const declaration
```
{% endcode %}

## 03. 배열

아래의 예제는 상수에 먼저 배열을 뜻하는 대괄호\[ \]를 사용한 후, 배열의 순서대로 데이터를 할당하는 방법이다.

{% code title="03. 배열" %}
```javascript
const arr2 = [];
arr2[0] = 100;
arr2[1] = 200;
arr2[2] = "javascript";

document.write("*** 03 배열 *** <br>");
document.write(arr2[0], "<br>");
document.write(arr2[1], "<br>");
document.write(arr2[2], "<br><br><br>");

// -- Result --
// *** 03 배열 ***
// 100
// 200
// javascript
```
{% endcode %}

## 04. 배열

아래의 예제는 상수에 배열을 선언한 후, 배열 안에 데이터를 나열하는 방법이다.

{% code title="04. 배열" %}
```javascript
const arr3 = new Array(100, 200, "javascript");

document.write('*** 04 배열 *** <br>');
document.write(arr3[0], "<br>");
document.write(arr3[1], "<br>");
document.write(arr3[2], "<br><br><br>");

// -- Result --
// *** 04 배열 ***
// 100
// 200
// javascript
```
{% endcode %}

## 05. 배열

아래의 예제는 상수에 대괄호\[ \]를 사용하여 데이터를 배열로 나열한 방법이다.

{% code title="05. 배열" %}
```javascript
const arr4 = [100, 200, "javascript"];

document.write('*** 05 배열 *** <br>');
document.write(arr4[0], "<br>");
document.write(arr4[1], "<br>");
document.write(arr4[2], "<br><br><br>");

// -- Result --
// *** 05 배열 ***
// 100
// 200
// javascript
```
{% endcode %}

## 06. 2차 배열

배열 안에서 또 다른 배열을 넣을 수 있다. 대괄호\[ \]를 사용하여 배열을 나열한 후, 새로운 대괄호\[ \]를 안에 넣으면 2차 배열을 사용 할 수 있다.

데이터를 불러올 때에는 `arr5[2][0]`와 같이 배열의 2번째 중 0번째의 데이터를 호출해야 정확하게 불러올 수 있다.

{% code title="06. 2차 배열" %}
```javascript
const arr5 = [100, 200, ["javascript", "jquery"]];

document.write('*** 06 배열 *** <br>');
document.write(arr5[0], "<br>");
document.write(arr5[1], "<br>");
document.write(arr5[2][0], "<br>");
document.write(arr5[2][1], "<br><br><br>");

// -- Result --
// *** 06 배열 ***
// 100
// 200
// javascript
// jquery
```
{% endcode %}

## 07. 배열의 개수

배열의 개수 구할 때에는 변수 이름 뒤에 `.length` 를 붙이면 배열의 개수를 알 수 있다.

{% code title="07. 배열의 개수" %}
```javascript
const arr6 = [100, 200, "javascript"];

document.write('*** 07 배열 수 *** <br>');
document.write(arr6.length,"<br><br><br>");

// -- Result --
// *** 07 배열 수 ***
// 3
```
{% endcode %}

## 08. 배열 불러오기 \(for 문\)

자바스크립트에서 반복문은 매우 다양한 종류가 있다. 반복문이 기본적으로 하는 일은 모두 같다. 반복문은 한 동작을 여러 번 반복한다. \(0회 반복하는 것도 가능\) 다양한 반복문 메커니즘은 다양한 방법으로 반복문의 시작 점과 끝나는 점을 정할 수 있다.

* [for 문](https://developer.mozilla.org/ko/docs/Web/JavaScript/Guide/Loops_and_iteration#for_%EB%AC%B8)
* [do...while 문](https://developer.mozilla.org/ko/docs/Web/JavaScript/Guide/Loops_and_iteration#do...while_%EB%AC%B8)
* \*\*\*\*[**while 문**](https://developer.mozilla.org/ko/docs/Web/JavaScript/Guide/Loops_and_iteration#while_%EB%AC%B8)\*\*\*\*
* \*\*\*\*[**레이블 문**](https://developer.mozilla.org/ko/docs/Web/JavaScript/Guide/Loops_and_iteration#%EB%A0%88%EC%9D%B4%EB%B8%94_%EB%AC%B8)\*\*\*\*
* \*\*\*\*[**break 문**](https://developer.mozilla.org/ko/docs/Web/JavaScript/Guide/Loops_and_iteration#break_%EB%AC%B8)\*\*\*\*
* \*\*\*\*[**continue 문**](https://developer.mozilla.org/ko/docs/Web/JavaScript/Guide/Loops_and_iteration#continue_%EB%AC%B8)\*\*\*\*
* \*\*\*\*[**for...in 문**](https://developer.mozilla.org/ko/docs/Web/JavaScript/Guide/Loops_and_iteration#for...in_%EB%AC%B8)\*\*\*\*
* \*\*\*\*[**for...of 문**](https://developer.mozilla.org/ko/docs/Web/JavaScript/Guide/Loops_and_iteration#for...of_%EB%AC%B8)\*\*\*\*

**for 반복문**은 어떤 특정한 조건이 거짓으로 판별 될 때까지 반복한다.

{% code title="for 반복문" %}
```javascript
for ( [초기문]; [조건문]; [증감문] ) 문장
```
{% endcode %}

1. 초기화 구문인 **초기문**이 존재한다면 초기문이 실행된다. 복잡한 구문 혹은 변수로 선언되기도 한다.
2. **조건문**은 조건을 검사한다. 만약 조건문이 참이라면, 그 반복문은 실행된다. 만약 조건문이 거짓이라면, 그 for문은 종결된다. 만약 그 조건문이 생략된다면, 그 조건문은 참으로 추정된다.
3. 문장 실행된다. 많은 문장을 실행할 경우에는 중괄{ } 를 사용해서 문장들을 묶어 준다.
4. 갱신 구문인 **증감문**이 존재한다면 실행되고 2번째 단계로 돌아간다.

{% code title="08. 배열 불러오기 \(for 문\)" %}
```javascript
const arr7 = [100, 200, "javascript"];

document.write('*** 08 배열 불러오기(for문) *** <br>');

for( let i = 0; i < arr7.length; i++ ) {
    document.write(arr7[i], "<br>");
}

// -- Result --
// *** 08 배열 불러오기(for문) ***
// 100
// 200
// javascript
```
{% endcode %}

## 09. 배열 불러오기 \(forEach\)

**`forEach()`** 메서드는 **주어진 함수를 배열 요소 각각에 대해 실행**한다.

{% code title="array.prototype.forEach\(\)" %}
```javascript
arr.forEach( callback (currentvalue[, index[, array]])[, thisArg])
```
{% endcode %}

* `callback` - 각 요소에 대해 실행 할 함수. 다음 세 가지의 매개 변수를 받는다.
* `currentvalue` - 처리할 현재 요소
* `index` - \(option\) 처리할 현재 요소의 인덱스
* `array` - \(option\) `forEach()` 를 호출한 배열
* `thisArg` - \(option\) `callback` 을 실행할 때 `this` 로 사용

**`forEach()`** 는 주어진 `callback` 을 배열에 있는 각 요소에 대해 오름 차순으로 한 번씩 실행한다. 삭제했거나 초기화하지 않은 인덱스 속성에 대해서는 실행하지 않는다.

`callback` 은 다음 세 인수와 함께 호출된다.

* 요소 값
* 요소 인덱스
* 순회 중인 배열

{% code title="forEach\(\) 방법 1" %}
```javascript
const arr8 = [100, 200, "javascript"];

arr8.forEach(function( elem ) {
    document.write(elem, "<br>");
});

// -- Result --
// 100
// 200
// javascript
```
{% endcode %}

{% code title="forEach\(\) 방법 2 - 축약형, 화살표 함수" %}
```javascript
const arr8 = [100, 200, "javascript"];

arr8.forEach( elem => {
    document.write(elem, "<br>");
});

// -- Result --
// 100
// 200
// javascript
```
{% endcode %}

{% code title="forEach\(\) 방법 3" %}
```javascript
const arr8 = [100, 200, "javascript"];

arr8.forEach( (element, index, array) => {
    document.write(element, "<br>");
    document.write(index, "<br>");
    document.write(array, "<br><br>");
});

// -- Result --
// 100
// 0
// 100,200,javascript

// 200
// 1
// 100,200,javascript

// javascript
// 2
// 100,200,javascript
```
{% endcode %}

## 10. 배열 불러오기 \(map\)

{% code title="array.prototype.map\(\)" %}
```javascript
array.map(callback(currentValue[, index[, array]])[, thisArg])
```
{% endcode %}

아래의 예제를 살펴보면, `array = [1, 2, 3, 4, 5];` 를 만든 후, 새로운 `newArray` 는 기존 `array` 의 각 인덱스에 있는 아이템 값에 `+2` 를 하여 구성하고 싶다. `map()` 메서드를 사용한 결과는 `newArray = [3, 4, 5, 6, 7]` 이다.

`map()` 메서드는 이처럼 **원본의 처음 인덱스부터 마지막 인덱스까지 순회하며 현재 인덱스\(index\)의 아이템\(element\)의 데이터를 가공**할 수 있고, **`return`을 하면 가공된 데이터를 새로운 리스트의 인덱스\(index\)에 담게 된다.**

이때, `return` 을 하였다고 `map() {}` 의 `scope` 를 빠져나가는 것은 아니다. 그 다음 인덱스를 가리키는 것이다. **`map() {}` 의 `scope` 를 빠져나가는 시점은 원본\(`array`\)의 마지막 인덱스\(index\)까지 모두 순회하였을 경우**이다.

`map()` 메서드를 사용해서 만들어진 새로운 배열의 `.length` 는 원본 배열의 `.length` 와 동일하게 되며, 내부의 아이템\(element\)만 다르게 되는 것이다.

{% code title="map\(\) 메서드" %}
```javascript
let array = [1, 2, 3, 4, 5];
let newArray = array.map(function(element, index) {
	return element + 2;
});

console.log(newArray);

// -- Result --
// [3, 4, 5, 6, 7]
```
{% endcode %}

`array` 의 마지막 인덱스에서만 `+2` 를 도출하고 싶다면 어떻게 해야 할까?

아래의 예제 결과를 보면 `map() {}` 에서 `return` 을 하지 않으면 해당 인덱스\(index\)는 undefined로 초기화 되는 것을 알 수 있다.

{% code title="map\(\) 메서드" %}
```javascript
let array = [1, 2, 3, 4, 5];
let newArray = array.map(function(element, index) {
	if( element === 5 ) return element + 2;
});

console.log(newArray);

// -- Result --
// [undefined, undefined, undefined, undefined, 7]
```
{% endcode %}



{% code title="map\(\) 방법 1" %}
```javascript
const arr9 = [100, 200, "javascript"];

arr9.map(function( elem ) {
    document.write(elem, "<br>");
});

// -- Result --
// 100
// 200
// javascript
```
{% endcode %}

{% code title="map\(\) 방법 2 - 축약형, 화살표 함수" %}
```javascript
const arr9 = [100, 200, "javascript"];

arr9.map( elem => {
    document.write(elem, "<br>");
});

// -- Result --
// 100
// 200
// javascript
```
{% endcode %}

{% code title="map\(\) 방법 3" %}
```javascript
const arr9 = [100, 200, "javascript"];

arr9.map( (element, index, array) => {
    document.write(element, "<br>");
    document.write(index, "<br>");
    document.write(array, "<br><br>");
});

// -- Result --
// 100
// 0
// 100,200,javascript

// 200
// 1
// 100,200,javascript

// javascript
// 2
// 100,200,javascript
```
{% endcode %}

## \* for\( \) vs forEach\( \) vs map\( \)

### 1. for\( \)

초깃값부터 시작해서 증가 또는 감소하면서 조건에 부합하면 계속 순회한다. 중간에 `break;` 문을 만나면 반복문을 중단한다.

{% code title=" for\(\)" %}
```javascript
for ([initialization]; [condition]; [final-expression])
   statement

// 예
const a = ["a", "b"];
for (let i = 0; i < a.length; i++) {
  console.log(a[i]);
}

// -- Result --
// a
// b
```
{% endcode %}

### 2. forEach\( \)

배열의 각 요소에 대해 `callback` 을 실행한다. 배열을 순회하므로 중간에 `break;` 문을 사용할 수 없다. 이런 경우라면 `for( )` 문을 사용해야 한다.

{% code title="forEach\(\)" %}
```javascript
array.forEach(callback(currentvalue[, index[, array]])[, thisArg])

// 예제
const a = ["a", "b"];
a.forEach( elem => {
  console.log(elem);
});

// -- Result --
// a
// b
```
{% endcode %}

### 3. map\( \)

배열의 각 요소에 대해 `callback` 을 실행하고 **실행 결과를 모은 새 배열을 리턴**한다. 배열을 순회하므로 중간에 `break;` 문을 사용할 수 없다. 이런 경우라면 `for( )` 문을 사용해야 한다.

{% code title="map\(\)" %}
```javascript
array.map(callback(currentValue[, index[, array]])[, thisArg])

// 예제
const a = ["a", "b"];
aa = a.map( elem => {
  console.log(elem);
});
console.log(aa);

// -- Result --
// a
// b
// [undefined, undefined]-> 별도의 return이 없기때문에 순회했던 개수만큼의 undefined을 도출 
```
{% endcode %}

`map()` 메서의 용도를 제대로 살리려면 `return` 문이 있어야 한다. `return` 문이 포함되면 배열의 각 요소에 대해 `callback` 을 실행하고 실행 결과를 모은 새 배열을 리턴 했다.

{% code title="map\(\), return" %}
```javascript
const a = ["a", "b"];
aa = a.map( elem => {
  console.log(elem);
  return "alphabet " + elem;
});
console.log(aa);

// -- Result --
// a
// b
// ["alphabet a", "alphabet b"]
```
{% endcode %}

{% hint style="info" %}
단순 반복은 _**for\(\)**_

배열을 순회 하려면 _**forEach\(\)**_

배열을 순회 한 후, 새 배열을 얻고 싶다면 _**map\(\)**_
{% endhint %}

## 11. 배열 불러오기 \(for...in 문\)

**`for...in`** 문은 **객체의 프로퍼티명을 열거하는 반복문**이다.

{% code title="for...in 문" %}
```javascript
for (variable in object) {
  statements : 객체에 열거할 수 있는 모든 프로퍼티의 개수만큼 반복적으로 실행하고자 하는 실행문;
}
```
{% endcode %}

배열도 객체로 놓고 보자면 인덱스의 숫자가 프로퍼티명에 해당하기 때문에 `for...in` 문에 나열할 수 있다. 하지만 배열 요소를 나열할 때는 `for...in` 문의 사용을 권장하지 않는다.

### `for...in` 문에서 주의할 사항

1. 프로퍼티를 열거하는 순서

   객체 리터럴 식 쓴 것에 대한 결과 값이 순서대로 나오기는 하지만 객체 리터럴에 쓴 순서대로 열거되지는 않는다. 즉, 순서가 보장되는 것이 아니다. 원래 프로퍼티 간에는 순서가 없는 것으로 순서를 의식하는 것 자체가 잘못된 것이다.

   하지만, 배열의 경우는 순서를 의식하는 데이터 타입이다. 아래의 예제에서 기대한 순서를 보이고 있지만 `for...in` 문은 순서를 보장하지 않기 때문에 이 같은 동작 방식에 지나치게 의존해서는 안된다.

2. 열거할 수 없는 프로퍼티의 존재

   `for...in` 문에 나열할 수 없는 프로퍼티의 경우. 예를 들어, 배열 객체에는 `length` 프로퍼티가 존재하지만 `for...in` 문에서는 열거할 수 없다. `length` 프로퍼티는 열거할 수 없는 속성의 프로퍼티이기 때문이다.

3. 프로토타입 상속한 프로퍼티

   `for...in` 문은 프로토타입에서 상속한 프로퍼티도 나열한다.

{% code title="for...in 문" %}
```javascript
const arr10 = [100, 200, "javascript"];

document.write('*** 11 배열 불러오기(for in문) *** <br>');

for( let i in arr10 ) {
    document.write(arr10[i]);
}

// -- Result --
// *** 11 배열 불러오기(for in문) ***
// 100200javascript
```
{% endcode %}

{% hint style="info" %}
_**for...in**_ 문은 **vue**에서 많이 사용한다.
{% endhint %}

## 12. 배열 불러오기 \(for...of 문\)

ES6에서 추가된 새로운 컬렉션 전용 반복 구문이다. 모든 객체가 아닌 컬렉션만 반복한다. \[Symbol.iterator\] 속성을 가지는 컬렉션의 프로퍼티를 반복한다.

{% code title="for...of 문" %}
```javascript
const arr11 = [100, 200, "javascript"];

document.write('*** 12 배열 불러오기(for of문) *** <br>');

for (let i of arr11) {
    document.write(i);
}

// -- Result --
// *** 12 배열 불러오기(for of문) ***
// 100200javascript
```
{% endcode %}

배열이나 객체에 따라 사용하는 방법이 다르다. `for...in 문`  배열, `for...of 문` 은 객체.

## \* for...in vs for...of

### 1. for...in

모든 객체의 모든 열거 가능한 속성을 반복한다. 즉, **객체의 요소들\(Data\)를 순회**하기 위한 구문이다.

* **인덱스가 리턴**
* 루프 구문이 요소들만 순회하는 것이 아니라 프로토타입 체도 순회
* 루프 순회 순서가 무작위

{% code title="for...in" %}
```javascript
for (var i in 'string') {
    alert(i); 
}

// 0, 1, 2, 3, 4, 5
```
{% endcode %}

### 2. for...of

모든 객체가 아닌 컬렉션만 반복한다. \[Symbol.iterator\] 속성을 가지는 컬렉션의 프로퍼티를 반복한다. 즉, **객체의 속성**들을 순회하기 위한 구문이다.

* **값이 리턴**되어 바로 값을 사용 할 수 있음
* 배열 순회를 지원하는 문법 중에서 가장 간결하고 직접적으로 접근 가능
* `forEach()` 메서드 에서 지원하지 않는 break, continue, return  구문 사용 가능 

{% code title="for...of" %}
```javascript
for (var i of 'string') {
    alert(i); 
} 

// s, t, r, i, n, g
```
{% endcode %}

{% hint style="info" %}
_**Iterator, 이터레이터**_

이터레이터는 '반복자'라는 의미로 **Iterable\(이터러블, 순회 가능한 자료구조\)의 요소를 탐색**하기 위한 포인터로서 `next( )`함수를 가지고 있는 객체이다.

**컬렉션을 반복할 수 있게 하는 객체**이다.
{% endhint %}

### 3. for...in vs for...of 예제 

{% code title="for...in VS for...of VS \(collection\)" %}
```javascript
// for...in : index 리턴
document.write('*** for...in 예제 *** <br>');

const num = [1, 2, 3, 4, 5];

for (let i in num) {
    document.write(i);
}

// -- Result --
// *** for...in 예제 ***
// 01234


// for...of : 값 리턴
document.write('*** for...of 예제 *** <br>');

for (let i of num) {
    document.write(i);
}

// -- Result --
// *** for...of 예제 ***
// 12345


// for...in (collection)
document.write('*** for...in (collection) 예제 *** <br>');

const obj1 = {
    apple: "red",
    banana: "yellow",
    grape: "purple"
}

for (let i in obj1) {
    document.write(i);
}

// -- Result --
// *** for...in (collection) 예제 ***
// applebananagrape


// for...of (collection)
document.write('*** for...of (collection) 예제 *** <br>');

const obj2 = {
    apple: "red",
    banana: "yellow",
    grape: "purple",
    [Symbol.iterator]: function* () {
        yield this.apple;
        yield this.banana;
        yield this.grape;
    }
}

for ( let i of obj2 ) {
    document.write(i);
}

// -- Result --
// *** for...of (collection) 예제 ***
// redyellowpurple
```
{% endcode %}

## 13. 배열 조회하기

회원 정보가 있는지 없는지 확인 하거나 카드 게임에서 많이 사용한다.

{% code title="배열 조회하기" %}
```javascript
const arr12 = [100, 200, "javascript"];

let search = "javascript";

document.write('*** 13 배열 조회하기 *** <br>');

for ( let i = 0; i < arr12.length; i++ ) {
    if (search == arr12[i]) {
        document.write(search + "를 찾았습니다.");
    }
}

// -- Result --
// *** 13 배열 조회하기 ***
// javascript를 찾았습니다.
```
{% endcode %}

## 14. 배열 펼침 연산자 \(Spread Syntax\)

펼침 연산자는 **배열을 펼쳐주는 역할**을 한다. 배열을 바꾸지 않고도 새로운 값을 복사하거나, 배열을 합치거나, 배열을 펼쳐진 상태로 파라미터로 전달하는 등의 활용이 가능해진다. 펼침 연산자의 장점은 **기존 컬렉션을 조작하지 않는다는** 점이다.

{% code title="... Spread Syntax" %}
```javascript
const arr13 = [100, 200, "javascript"];

document.write('*** 14 배열 펼침 연산자(Spread Syntax) *** <br>');

document.write(arr13, "<br>");
document.write(...arr13, "<br>"); // 쉼표가 없이 데이터를 불러옴

// -- Result --
// *** 14 배열 펼침 연산자(Spread Syntax) ***
// 100,200,javascript
// 100200javascript
```
{% endcode %}

{% code title="... Spread Syntax \(배열 복사, 합침, 파라미터 전달\)" %}
```javascript
let a = [100, 200, 300, 400];
let b = [...a];

console.log(a); // [100, 200, 300, 400]
console.log(b); // [100, 200, 300, 400]

console.log(a === b); // false
// 새로운 배열로서 메모리에 들어간 복사를 한 형태
// concat을 이용한 것과 같은 결과
// 배열을 바꾸지 않고 새로운 값을 복사할 수 있음 

let c = [...a, 500];
console.log(c) // [100, 200, 300, 400, 500]
// 기존의 복잡한 방법 대신 간단하게 값을 추가하여 배열을 복사할 수 있음 
```
{% endcode %}

## 15. 배열 최댓값 구하기

{% code title="배열 최댓값 구하기" %}
```javascript
const arr14 = [100, 200, 300, 400, 500];

let max;

for ( let i = 0; i < arr14.length; i++ ) {
    if (arr14[i] > arr14[0]) {
        max = arr14[i];
    }
}

document.write('*** 15 배열 최댓값 구하기 *** <br>');
document.write(max);

// -- Result --
// *** 15 배열 최댓값 구하기 ***
// 500
```
{% endcode %}

## 16. 배열 Math로 최댓값 구하기

{% code title="배열 Math로 최댓값 구하기" %}
```javascript
const arr15 = [100, 200, 300, 400, 500];

let max2 = Math.max(...arr15);

document.write('*** 16 배열 Math로 최댓값 구하기 *** <br>');
document.write(max2);

// -- Result --
// *** 16 배열 최댓값 구하기 ***
// 500
```
{% endcode %}

## 17. 배열 메서드 - join\( \)

**`join()`** 메서드는 **원소를 결합해서 하나의 문자열로 반환**한다. ****

{% code title="Array.prototype.join\(\) Syntax" %}
```javascript
arr.join([separator])
```
{% endcode %}

{% code title="join\(\)" %}
```javascript
const arr16 = [100, 200, 300, 400, 500];

document.write('*** 17 배열 join *** <br>');
document.write(arr16.join("*"));

// -- Result --
// *** 17 배열 join ***
// 100*200*300*400*500
```
{% endcode %}

{% code title="join\(\)" %}
```javascript
var uint8 = new Uint8Array([1,2,3]);

uint8.join();      // '1,2,3'
uint8.join(' / '); // '1 / 2 / 3'
uint8.join('');    // '123'
```
{% endcode %}

## 18. 배열 메서드 - reverse\( \)

**`reverse()`** 메서드는 **배열을 역순으로 정렬**한다. 첫 번째 배열 요소가 마지막 요소가 되고 마지막 배열 요소가 첫 번째 요소가 된다. 메서드를 사용하는 순간 원본 배열이 바뀐다.

{% code title="Array.prototype.reverse\(\) Syntax" %}
```javascript
a.reverse()
```
{% endcode %}

{% code title="reverse\(\)" %}
```javascript
const arr16 = [100, 200, 300, 400, 500];

document.write('*** 18 배열 reverse *** <br>');
document.write(arr16.reverse());

// -- Result --
// *** 18 배열 reverse ***
// 500,400,300,200,100
```
{% endcode %}

## 19. 배열 메서드 - sort\( \)

**`sort()`** 메서드는 **원본 배열을 직접 변경하여 정렬된 배열을 반환**한다. 기본 정렬 순서는 오름차순이며, 내림차순도 가능하다. 이때, 정렬의 순서는 문자열의 유니코드 코드 포인트를 따르는데. 배열의 요소가 숫자여도 배열의 요소를 일시적으로 문자열로 변환한 후 문자열의 **유니코드를 비교하여 정렬**한다.

`map()` 혹은 `fliter()` 메서드는 원본 배열을 변경하지 않고 새로운 배열을 생성하여 반환한다. 이를 _accessor method_ 라고 한다. 반면, `sort()` 메서드는 원본 배열을 직접 변경하는데 이를 _mutator method_라고 한다. 

{% code title="Array.prototype.sort\(\) Syntax" %}
```javascript
arr.sort([compareFunction])
```
{% endcode %}

{% code title="sort\(\) 메서드의 숫자와 문자열 정렬 순서" %}
```javascript
const color = ['red', 'yellow', 'greeng'];
document.write(color.sort());

// -- Result --
// greeng,red,yellow

const number = [1, 5, 11, 100, 22];
document.write(number.sort());

// -- Result --
// 1,100,11,22,5
```
{% endcode %}

{% code title="sort\(\)" %}
```javascript
const arr16 = [100, 500, 200, 400, 300];

document.write('*** 19 배열 sort *** <br>'); 
document.write(arr16.sort());

// -- Result --
// *** 19 배열 sort ***
// 100,200,300,400,500
```
{% endcode %}

`sort()` 메서드로 오름차순, 내림차순으로 정렬이 가능한데. 매개 변수로 익명 함수를 사용할 수 있다. 그 과정을 자세히 살펴보자.

 먼저 _**a에 100**_을 대입하고 _**b에 200**_을 대입하면 _**반환 값은 -200\(음수\)**_이다. 따라서, 순서는 그대로 유지된다. 

{% code title="sort\(\) 오름차순 정렬" %}
```javascript
const arr16 = [100, 500, 200, 400, 300];

document.write('*** 19 배열 sort 오름차순 정 *** <br>'); 
document.write(arr16.sort(function (a, b) {
    return a - b
}));

// -- Result --
// *** 19 배열 sort 오름차순 정렬  ***
// 100,200,300,400,500
```
{% endcode %}

다음은 _**a에 400**_을 대입하고 _**b에 500**_을 대입하면 _**반환 값은 100\(양수\)**_이다. 따라서, 순서는 바뀌게 되고, 500은 400보다 먼저 정렬 된다.

{% code title="sort\(\) 내림차순 정렬" %}
```javascript
const arr16 = [100, 500, 200, 400, 300];

document.write('*** 19 배열 sort 내차순 정렬 *** <br>'); 
document.write(arr16.sort(function (a, b) {
    return b - a
}));

// -- Result --
// *** 19 배열 sort 내차순 정렬 ***
// 500,400,300,200,100
```
{% endcode %}

##  20. 배열 메서드 - slice\( \)

**`slice()`** 메서드는 _**start 부터 end 전**_까지의 복사본을 **새로운 배열 객체로 반환**한다. 원본 배열은 수정되지 않는다.

{% code title="Array.prototype.slice\(\) Syntax" %}
```javascript
arr.slice([start[, end]])
```
{% endcode %}

_**start : 추출 시작 점에 대한 인덱스 \(포함\)**_

* undefined - 0 부터 시작
* 음수 - 배열의 끝에서 부터 길이를 나타냄 . `slice(-2)` 의 경우, 배열의 마지막 2개를 추출
* 배열의 길이와 같거나 큰 수 - 빈 배열 반환

_**end : 추출을 종료할 기준의 인덱스 \(제외, end를 제외하고 그 전까지 요소만 추출\)**_

* 지정하지 않음 - 배열의 끝까지 포함
* 음수 - 배열의 끝에서부터 길이를 나타냄. `slice(1, -2)` 의 경우, 두 번째부터 끝에서 세 번째 요소까지 추출
* 배열의 길이와 같거나 큰 수 - 배열의 끝까지 추출 

{% code title="slice\(\)" %}
```javascript
const arr16 = [100, 500, 200, 400, 300];

document.write('*** 20 배열 slice *** <br>');
document.write(arr16.slice(1, 3));

// -- Result --
// *** 20 배열 slice ***
// 200, 300
```
{% endcode %}

`slice( )` 메서드 예제를 통해 더욱 자세히 알아보자.

* arr1 : index번호 3부터 4까지 추출
* arr2 : index번호 0부터 4까지 추출
* arr3 : 뒤에서 3개 추출
* arr4 : 뒤에서부터 3번째 숫자인 8부터 추출하기 시작해서 앞에서부터 9번째 숫자\(10\) 전까지 추출하므로 숫자 8과 9 추출
* arr5 : 배열의 길이가 10이므로 index번호 10부터 추출하면 추출할 요소가 없으므로 빈 배열을 리턴한다.
* arr6 : index번호 4부터 끝까지 추출
* arr7 : 처음부터 끝까지 추출함
* arr8 : index번호 5번인 6부터 추출 시작하여 끝에서부터 -4번째인 7 전까지 추출하므로 숫자 6을 추출
* arr9 : index번호 2번부터 끝까지 추출

{% code title="slice\(\) 예제" %}
```javascript
var arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

var arr1 = arr.slice(3, 5); // [4, 5]
var arr2 = arr.slice(undefined, 5); // [1, 2, 3, 4, 5]
var arr3 = arr.slice(-3); // [8, 9, 10]
var arr4 = arr.slice(-3, 9); // [8, 9]
var arr5 = arr.slice(10); // []
var arr6 = arr.slice(4); // [5, 6, 7, 8, 9, 10]
var arr7 = arr.slice(undefined); // [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
var arr8 = arr.slice(5, -4); // [6]
var arr9 = arr.slice(2, 15); // [3, 4, 5, 6, 7, 8, 9, 10]

console.log(arr); // [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
console.log(arr1); // [4, 5]
console.log(arr2); // [1, 2, 3, 4, 5]
console.log(arr3); // [8, 9, 10]
console.log(arr4); // [8, 9]
console.log(arr5); // []
console.log(arr6); // [5, 6, 7, 8, 9, 10]
console.log(arr7); // [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
console.log(arr8); // [6]
console.log(arr9); // [3, 4, 5, 6, 7, 8, 9, 10]


출처: https://im-developer.tistory.com/103 [Code Playground]
```
{% endcode %}

## 21. 배열 메서드 - concat\( \)

**`concat()`** 메서드는 **두 개 이상의 배열을 병합**하는데 사용한다. 이 메서드는 **기존 배열을 변경하지 않고 새 배열을 반환**한다.

{% code title="Array.prototype.concat\(\) Syntax" %}
```javascript
const new_array = old_array.concat([value1[, value2[, ...[, valueN]]]])
```
{% endcode %}

{% code title="concat\(\)" %}
```javascript
const arr16 = [100, 200, 300, 400, 500];
const arr17 = [600, 700, 800, 900, 1000];
const concatArray = arr16.concat(arr17);

document.write('*** 21 배열 concat *** <br>');
document.write(concatArray), "<br><br>");

// -- Result --
// *** 21 배열 concat ***
// 100,200,300,400,500,600,700,800,900,1000
```
{% endcode %}

## 22. 배열 메서드 - shift\( \)

**`shift()`** 메서드는 **배열에서 첫 번째 요소를 제거**하고 **제거된 요소를 반환**한다. 이 메서드는 **배열의 길이를 변경**한다. 메서드가 실행될 때 마다 배열의 길이가 줄어든다.

{% code title="Array.prototype.shift\(\) Syntax" %}
```javascript
arr.shift()
```
{% endcode %}

{% code title="shift\(\) " %}
```javascript
const arr16 = [100, 200, 300, 400, 500];

document.write(arr16.shift(), "<br>"); // 제거된 요소 반환 
document.write(arr16, "<br>"); // 남아 있는 배열 반환 

// -- Result --
// 100
// 200, 300, 400, 500
```
{% endcode %}

##  23. 배열 메서드 - unshift\( \)

**`unshift()`** 메서드는 **배열의 시작 부분에 하나 이상의 요소를 추가**하고 **배열의 새 길이를 반환**한다.

{% code title="Array.prototype.unshift\(\) Syntax" %}
```javascript
arr.unshift(element1[, ...[, elementN]])
```
{% endcode %}

{% code title="unshift\(\)" %}
```javascript
const arr16 = [200, 300, 400, 500];

document.write('*** 23 배열 unshift *** <br>');
document.write(arr16.unshift(100), "<br>"); // 배열의 길이를 반환
document.write(arr16, "<br><br>"); // 추가된 배열을 반환

// -- Result --
// *** 23 배열 unshift ***
// 5
// 100,200,300,400,500
```
{% endcode %}

##  24. 배열 메서드 - pop\( \)

**`pop()`** 메서드는 **배열에서 마지막 요소를 제거**하고 **해당 요소를 반환**한다. 이 메서드는 **배열의 길이를 변경**한다.

{% code title="Array.prototype.pop\(\) Syntax" %}
```javascript
arrName.pop()
```
{% endcode %}

{% code title="pop\(\)" %}
```javascript
const arr16 = [100, 200, 300, 400, 500];

document.write('*** 24 배열 pop *** <br>');
document.write(arr16.pop(), "<br>"); // 제거된 요소 반환
document.write(arr16, "<br><br>"); // 남아 있는 배열 반환 

// -- Result --
// *** 24 배열 pop ***
// 500
// 100,200,300,400
```
{% endcode %}

##  25. 배열 메서드 - push\( \)

`push()` 메서드 **하나 이상의 요소를 배열의 가장 마지막에 추가**한다. 원본 배열은 추가한 요소의 수만큼 길이\(length\)가 늘어나게 되며, 요소를 성공적으로 추가하면 **배열의 총 길이를 반환**한다.

{% code title="Array.prototype.push\(\) Syntax" %}
```javascript
arr.push(element1[, ...[, elementN]])
```
{% endcode %}

{% code title="push\(\)" %}
```javascript
const arr16 = [100, 200, 300, 400, 500];

document.write('*** 25 배열 push *** <br>');
document.write(arr16.push(500), "<br>"); // 추가된 요소 배열의 길이를 반환
document.write(arr16, "<br><br>"); // 추가된 배열을 반환

// -- Result --
// 6
// 100, 200, 300, 400, 500
```
{% endcode %}

## \* 변수, 배열, 객체

* 변수 : 데이터를 저장하는 곳\(한 개\)
* 배열 : 데이터를 저장하는 곳\(두  개 이상\)
* 객체 : 데이터를 저장하는 곳\(두 개 이상, "키, 값"\)  

## 26. 객체를 배열 방식으로 사용하기 

{% code title="객체를 배열 방식으로 사용하기" %}
```javascript
const obj1 = new Object();
obj1[0] = 100;
obj1[1] = 200;
obj1[2] = "javascript";

document.write('*** 26 객체, 배열 방식으로 사용하기 *** <br>');
document.write(obj1[0], "<br>");
document.write(obj1[1], "<br>");
document.write(obj1[2], "<br>");

// -- Result --
// *** 26 객체 배열 방식으로 사용하기 ***
// 100
// 200
// javascript
```
{% endcode %}

{% hint style="info" %}
_**new**_  
생성자, 새로 생기다.
{% endhint %}

## 27. 객체 방식으로 사용하기 

{% code title="객체 방식으로 사용하기" %}
```javascript
const obj2 = new Object();
obj2.a = 100;
obj2.b = 200;
obj2.c = "javascript";

document.write('*** 27 객체 방식으로 사용하기 *** <br>');
document.write(obj2.a, "<br>");
document.write(obj2.b, "<br>");
document.write(obj2.c, "<br>");

// -- Result --
// *** 27 객체 방식으로 사용하기 ***
// 100
// 200
// javascript
```
{% endcode %}

## 28. 객체, Object 

### 객체\(Object\)란?

**자바스크립트는 객체\(Object\) 기반의 스크립트 언어이며 자바스크립트를 이루고 있는 거의 "모든 것"이 객체**이다. 원시 타입\(Primitives\)을 제외한 나머지 값들\(함수, 배열, 정규표현식 등\)은 모두 객체이다.

**자바스크립트의 객체는 키\(key\)와 값\(value\)으로 구성된 프로퍼티\(Property\)들의 집합**이다. 프로퍼티의 값으로 자바스크립트에서 사용할 수 있는 모든 값을 사용할 수 있다. 자바스크립트의 함수는 일급 객체이므로 값으로 취급할 수 있다. 따라서 프로퍼티 값으로 함수를 사용할 수도 있으며 프로퍼티 값이 함수일 경우, 일반 함수와 구분하기 위해 메서드라고 부른다.

이와 같이 객체는 데이터를 의미하는 프로퍼티\(Porperty\)와 데이터를 참조하고 조작할 수 있는 동작\(behavior\)을 의미하는 메서드\(method\)로 구성된 집합이다. 객체는 데이터\(프로퍼티\)와 그 데이터에 관련되는 동작\(메서드\)을 모두 포함할 수 있기 때문에 데이터와 동작을 하나의 단위로 구조화할 수 있어 유용하다.

자바스크립트의 객체는 객체지향의 상속을 구현하기 위해 프로토타입\(Prototype\)이라고 불리는 객체의 프로퍼티와 메서드를 상속받을 수 있다. 이 프로토타입은 타 언어와 구별되는 중요한 개념이다.

{% hint style="info" %}
_**원시 타입\(Primitives\)**_   
자바스크립트는 포로토타입 객체 지향 언어로 클래스라는 개념이 없다. 하지만 ES6부터는 클래스를 대체하는 타입이라는 개념이 등장했다. 타입에는 원시 타입과 참조 타입이 있다.
{% endhint %}

### 프로퍼티

프로퍼티는 프로퍼티 키\(이름\)와 프로퍼티 값으로 구성된다. 프로퍼티는 프로퍼티 키로 유일하게 식별할 수 있다. 즉, 프로퍼티 키는 프로퍼티를 식별하기 위한 식별자\(identifier\)다. 프로퍼티 키의 명명 규칙과 프로퍼티 값으로 사용할 수 있는 값은 아래와 같다.

* 프로퍼티 키 : 빈 문자열을 포함하는 모든 문자열 또는 symbol 값
* 프로퍼티 값 : 모든 값

프로퍼티 키에 문자열이나 symbol 값 이외의 값을 지정하면 암묵적으로 타입이 변환되어 문자열이 된다. 이미 존재하는 프로퍼티 키를 중복 선언하면 나중에 선언한 프로퍼티가 먼저 선언한 프로퍼티를 덮어쓴다. 배열과는 달리 객체는 프로퍼티를 열거할 때 순서를 보장하지 않는다.

### 메서드

프로퍼티 값이 함수일 경우, 일반 함수와 구분하기 위해 메서드라 부른다. 즉, 메서드는 객체에 제한되어 있는 함수를 의미한다.

{% code title="객체" %}
```javascript
const obj3 = {};
obj3.a = 100;
obj3.b = 200;
obj3.c = "javascript";

document.write('*** 28 객체 *** <br>');
document.write(obj3.a, "<br>");
document.write(obj3.b, "<br>");
document.write(obj3.c, "<br><br>");

// -- Result --
// *** 28 객체 ***
// 100
// 200
// javascript
```
{% endcode %}

## 29. 객체의 정석 

### 객체 리터럴 

가장 일반적인 자바스크립트의 객체 생성 방식이다. 클래스 기반 객체 지향 언어와 비교할 때 매우 간편하게 생성할 수 있다. **중괄호{ }를 사용하여 객체를 생성**하는데 { } 내에 1개 이상의 프로퍼티를 기술하면 해당 프로퍼티가 추가된 객체를 생성할 수 있다. { } 내에 아무것도 기술하지 않으면 빈 객체가 생성된다.

{% code title="객체 리터럴" %}
```javascript
var object = {};
console.log(typeof object); // object

var person = {
    name: "Kim",
    gender: "female",
    myName: function () {
        console.log("My name is " + this.name);
    }
};

console.log(typeof person); // object
console.log(person);

person.myName(); // My name is Kim
```
{% endcode %}

{% code title="객체의 정석" %}
```javascript
const obj4 = {
    a: 100,
    b: 200,
    c: "javascript",
}

document.write('*** 29 객체의 정석 *** <br>');
document.write(obj4.a, "<br>");
document.write(obj4.b, "<br>");
document.write(obj4.c, "<br><br><br>");

// -- Result --
// *** 29 객체의 정석 ***
// 100
// 200
// javascript
```
{% endcode %}

### Object 생성자 함수 

_**new**_ 연산자와 \*\*\*Object 생성자 함수\*\*\*를 호출하여 빈 객체를 생성할 수 있다. 빈 객체 생성 이후 프로퍼티 또는 메서드를 추가하여 객체를 완성하는 방법이다.

**생성자\(constructor\) 함수란** _**new**_ **키워드와 함께 객체를 생성하고 초기화하는 함수**를 말한다. 생성자 함수를 통해 생성된 객체를 인스턴스\(instance\)라 한다. 자바스크립트는 Object 생성자 함수 이외에도 String, Number, Boolean, Array, Date, RegExp 등의 빌트인 생성자 함수를 제공한다. 일반 함수와 생성자 함수를 구분하기 위해 생성자 함수의 이름을 파스칼 케이스\(PascalCase\)를 사용하는 것이 일반적이다.

객체가 소유하고 있지 않은 프로퍼티 키에 값을 할당하면 해당 객체에 프로퍼티를 추가하고 값을 할당한다. 이미 존재하는 프로퍼티 키에 새로운 값을 할당하면 프로퍼티 값은 할당한 값으로 변경된다.

{% code title="Obejct 생성자 함수" %}
```javascript
// 빈 객체의 생성
var person = new Object();

// 프로퍼티 추가
person.name = "Kim";
person.gender = "female";
person.myName = function () {
    console.log("My name is " + this.name);
};

console.log(typeof person); // obejct
console.log(person); // {name: "Kimg", gender: "female", myName: f}

person.myName(); // My name is Kim
```
{% endcode %}

반드시 Object 생성자 함수를 사용해 빈 객체를 생성해야 하는 것은 아니다. 객체를 생성하는 방법은 객체 리터럴을 사용하는 것이 더 간편하다. Object 생성자 함수 방식은 특별한 이유가 없다면 그다지 유용해 보이지 않는다.

사실 **객체 리터럴 방식으로 생성된 객체는 결국 빌트인\(Built-in\) 함수인 Object 생성자 함수로 객체를 생성하는 것을 단순화시킨 축약 표현**이다. 다시 말해, 자바스크립트 엔진은 객체 리터럴로 객체를 생성하는 코드를 만나면 내부적으로 Object 생성자 함수를 사용하여 객체를 생성한다. 따라서 개발자가 일부러 Object 생성자 함수를 사용해 객체를 생성해야 할 일은 거의 없다.

### 생성자 함수

객체 리터럴 방식과 Object 생성자 함수 방식으로 객체를 생성하는 것은 프로퍼티 값만 다른 여러 개의 객체를 생성할 때 불편하다. 동일한 프로퍼티를 갖는 객체 임에도 불구하고 매번 같은 프로퍼티를 기술해야 한다.

{% code title="객체 리터럴 방식, Object 생성자 함수 방식" %}
```javascript
var person1 = {
    name: "Kim",
    gender: "female",
    myName: function () {
        console.log("My name is " + this.name);
    }
};

var person2 = {
    name: "Han",
    gender: "male",
    myName: function () {
        console.log("My name is " + this.name);
    }
};
```
{% endcode %}

생성자 함수를 사용하면 마치 객체를 생성하기 위한 탬플릿\(클래스\)처럼 사용하여 프로퍼티가 동일한 객체 여러 개를 간편하게 생성할 수 있다.

{% code title="생성자 함수" %}
```javascript
// 생성자 함수
function Person (name, gender) {
    this.name = name;
    this.gender = gender;
    this.myName = function () {
        console.log("My name is " + this.name);
    };
};

// 인스턴스의 생성
var person1 = new Person("Kim", "female");
var person2 = new Person("Han", "male");

console.log("person1: ", typeof person1); // person1: object
console.log("person2: ", typeof person2); // person2: object
console.log("person1: ", person1); // person1: object
console.log("person2: ", person2); // person2: object

person1.myName(); // My name is Kim
person2.myName(); // My name is Han
```
{% endcode %}

* 생성자 함수 이름은 일반적으로 대문자로 시작한다. 이것은 생성자 함수임을 인식하도록 도움을 준다.
* 프로퍼티 또는 메서드 명 앞에 기술한 `this` 는 생성자 함수가 생성할 인스턴스\(instance\)를 가르킨다.
* `this` 에 연결\(바인딩\)되어 있는 프로퍼티와 메서드는 `public` \(외부에서 참조 가능\)하다.
* 생성자 함수 내에서 선언된 일반 변수 `private` \(외부에서 참조 불가능\) 하다. 즉, 생성자 함수 내부에서는 자유롭게 접근이 가능하나 외부에서 접근할 수 없다.

{% code title="생성자 함수" %}
```javascript
function Person (name, gender) {
    var married = true;         // private
    this.name = name;           // public
    this.gender = gender;       // public
    this.myName = function () { // public
        console.log("My name is " + this.name);
    };
};

var person1 = new Person("Kim", "female");

console.log(typeof person1); // obejct
console.log(Person); // ƒ Person (name, gender) {
							               // var married = true;
							               // this.name = name;
							               // this.gender = gender;
							               // this.myNmae = function() {							                    
console.log(person1.gender); // "female"
console.log(person1.married); // undefined
```
{% endcode %}

자바 스크립트의 생성자 함수는 이름 그대로 객체를 생성하는 함수이다. 하지만 자바와 같은 클래스 기반 객체지향 언어의 생성자\(constructor\)와는 다르게 그 형식이 정해져 있는 것이 아니라 기존 함수와 동일한 방법으로 생성자 함수를 선언하고 `new` 연산자를 붙여서 호출하면 해당 함수는 생성자 함수로 동작한다.

이는 생성자 함수가 아닌 일반 함수에 `new` 연산자를 붙여 호출하면 생성자 함수처럼 동작할 수 있다는 것을 의미한다. 따라서 일반적으로 생성자 함수명은 첫문자를 대문자로 기술하여 혼란을 방지하려는 노력을 한다.

`new` 연산자와 함께 함수를 호출하면 `this` 바인딩이 다르게 동작한다. 생성자 호출 패턴을 참조하자.

## 30. 객체 \(배열 속의 객체\)

{% code title="객체 \(배열 속의 객체\)" %}
```javascript
const obj5 = [
    {
        a: 100,
        b: 200
    },
    {
        c: 300,
        d: 400
    }
];

document.write('*** 30 객체(배열 속 객체) *** <br>');
document.write(obj5[0].a, "<br>");
document.write(obj5[0].b, "<br>");
document.write(obj5[1].c, "<br>");
document.write(obj5[1].d, "<br>");


// -- Result --
// *** 30 객체 (배열 속의 객체) ***
// 100
// 200
// 300
// 400
```
{% endcode %}

## 31. 객체 \(객체 속의 배열\)

{% code title="객체 \(객체 속의 배열\)" %}
```javascript
const obj6 = {
    a: 100,
    b: [200, 300],
    c: "javascript"
}

document.write('*** 31 객체(객체 속의 배열) *** <br>');
document.write(obj6.a, "<br>");
document.write(obj6.b[0], "<br>");
document.write(obj6.b[1], "<br>");
document.write(obj6.c, "<br><br><br>");

// -- Result --
// *** 31 객체 (객체 속의 배) ***
// 100
// 200
// 300
// javascript
```
{% endcode %}

## 32. 객체 \(객체 속의 함수\)

{% code title="객체 \(객체 속의 함수\)" %}
```javascript
const obj7 = {
    a: 100,
    b: [200, 300],
    c: "javascript",
    d: function() {
        document.write("자바스크립트가 실행되었습니다. <br>");
    },
    e: function() {
        document.write(this.c + "가 실행되었습니다. <br>");
    }
}

document.write('*** 32 객체(객체 속의 함수) *** <br>');
document.write(obj7.a, "<br>");
document.write(obj7.b[0], "<br>");
document.write(obj7.b[1], "<br>");
document.write(obj7.c, "<br>");
obj7.d();
obj7.e();

// -- Result --
// *** 32 객체(객체 속의 함수) ***
// 100
// 200
// 300
// javascript
// 자바스크립트가 실행되었습니다.
// javascript가 실행되었습니다.
```
{% endcode %}

{% hint style="info" %}
_**배열 속에는 함수를 넣을 수 없다.**_
{% endhint %}

## 33. 객체 생성자 함수

{% code title="객체 생성자 함수" %}
```javascript
function obj8(a, b) {
    this.a = a;
    this.b = b;
    this.c = function () {
        document.write(this.a + this.b);
    };
};

const result1 = new obj8(100, 200);
const result2 = new obj8("javascript", "react");

document.write('*** 33 객체 생성자 함수 *** <br>');
document.write(result1.a, "<br>");
document.write(result1.b, "<br>");
document.write(result2.a, "<br>");
document.write(result2.b, "<br>");
result1.c();

document.write("<br>");

result2.c();

// -- Result --
// *** 33 객체 생성자 함수 ***
// 100
// 200
// javascript
// react
// 300
// javascriptreact
```
{% endcode %}

{% hint style="info" %}
_**생성자 함수란?**_  
객체를 생성할 때 사용하는 함수   
여러 개의 동일한 프로퍼티를 가지는 객체를 생성하기 위해 사용 

![](https://t1.daumcdn.net/cfile/tistory/99C293435BBB5FDD32)  
\(1\) new 키워드는 빈 객체 {}를 생성

\(2\) 생성자 함수는 빈 객체에 생성 할 프로퍼티를 정의

\(3\) 함수의 인수들을 프로퍼티에 할당

\(4\) 생성된 Student 객체를 student에 할당  
  
출처: [https://doitnow-man.tistory.com/132\#t1](https://doitnow-man.tistory.com/132#t1) \[즐거운인생 \(실패 또하나의 성공\)\]
{% endhint %}

## 34. 객체 리터럴 \(객체 초기화\) - 데이터 값을 변수에 저장

{% code title="객체 리터럴 \(객체 초기화\) - 데이터 값을 변수에 저장" %}
```javascript
// 변수
const name1 = "array";
const name2 = "object";

const obj9 = {
    name1,
    name2,
}

document.write('*** 34 객체 리터럴(객체 초기화) *** <br>');
document.write(obj9.name1, "<br>");
document.write(obj9.name2, "<br><br><br>");

// -- Result --
// *** 34 객체 리터럴(객체 초기화) - 데이터 값을 변수에 저장 ***
// array
// object
```
{% endcode %}

## 35. 객체 리터럴 \(객체 초기화\) - 데이터 값을 객체에 저장

{% code title="객체 리터럴 \(객체 초기화\) - 데이터 값을 객체에 저장" %}
```javascript
// 객체 
const obj10 = {
    name1: "array",
    name2: "object"
}

const name1 = obj10.name1;
const name2 = obj10.name2;

document.write('*** 35 객체 리터럴(객체 초기화) *** <br>');
document.write(name1, "<br>");
document.write(name2, "<br><br><br>");

// -- Result --
// *** 35 객체 리터럴(객체 초기화) -데이터 값을 객체에 저장  ***
// array
// object
```
{% endcode %}

## 36. 객체 구조 분해 할당 \(데이터를 뽑아내는 방법\)

{% code title="객체 구조 분해 할당 \(데이터를 뽑아내는 방법\)" %}
```javascript
const obj11 = {
    name1: "array",
    name2: "object"
}

const { name1, name2 } = obj11;

document.write('*** 36 객체 구조 분해 할당 *** <br>');
document.write(name1, "<br>");
document.write(name2, "<br><br><br>");

// -- Result --
// *** 36 객체 구조 분해 할당 ***
// array
// object
```
{% endcode %}

{% code title="참고 사항" %}
```javascript
// 이러한 객체 구조 분해 할당 방법은
const { name1, name2 } = obj11;

// 아래와 같은 방법을 축약한 형태이다.
const name1 = obj10.name1;   
const name2 = obj10.name2;
```
{% endcode %}

{% hint style="info" %}
_React 에서 많이 사용하는 방법이**다.**_
{% endhint %}

## 37. 배열 구조 분해 할당 \(데이터를 뽑아내는 방법\)

{% code title="배열 구조 분해 할당 \(데이터를 뽑아내는 방법\)" %}
```javascript
const arr18 = ["array", "object"];

const [ name1, name2 ] = arr18;

document.write('*** 37 배열 구조 분해 할당 *** <br>');
document.write(name1, "<br>");
document.write(name2, "<br><br><br>");

// -- Result --
// *** 37 배 구조 분해 할당 ***
// array
// object
```
{% endcode %}

{% code title="참고 사항" %}
```javascript
// 이러한 배 구조 분해 할당 방법은
const [ name1, name2 ] = arr18;

// 아래와 같은 방법을 축약한 형태이다.
const name1 = arr18[0];
const name2 = arr18[1];
```
{% endcode %}

## 38. 객체 펼침 연산자 

{% code title="객체 펼침 연산자" %}
```javascript
const spread = {
    nameA: "array",
    nameB: "object"
}

const newSpread = { ...spread };

document.write('*** 38 객체 펼침 연산자 *** <br>');
document.write(newSpread.nameA, "<br>");
document.write(newSpread.nameB, "<br><br><br>");

// -- Result --
// *** 38 객체 펼침 연산자 ***
// array
// object
```
{% endcode %}

{% hint style="info" %}
React, Vue 에서 많이 사용하는 방법이다.
{% endhint %}

## 39. 객체 펼침 연산자 \(프로퍼티 추가\) 

{% code title="객체 펼침 연산자" %}
```javascript
const spread = {
    nameA: "array",
    nameB: "object"
}

const newSpread = { ...spread, nameC: "react" };

document.write('*** 39 객체 펼침 연산자 *** <br>');
document.write(newSpread.nameA, "<br>");
document.write(newSpread.nameB, "<br>");
document.write(newSpread.nameC, "<br><br><br>");

// -- Result --
// *** 39 객체 펼침 연산자 ***
// array
// object
// react
```
{% endcode %}

## 40. 배열 펼침 연산자 \(복사\)

{% code title="배열 펼침 연산자 \(복사\)" %}
```javascript
const spread = ["array", "object"];
const newSpread = [ ...spread ];

document.write('*** 40 배열 펼침 연산자(복사) *** <br>');
document.write(newSpread, "<br><br><br>");

// -- Result --
// *** 40 배열 펼침 연산자(복사) ***
// array,object
```
{% endcode %}

## 41. 배열 펼침 연산자 \(결합\)

{% code title="배열 펼침 연산자 \(결합\)" %}
```javascript
const spread1 = ["array", "object"];
const spread2 = ["react", "vue"];
const newSpread = [ ...spread1, ...spread2 ];

document.write('*** 41 배열 펼침 연산자(결합) *** <br>');
document.write(newSpread, "<br><br><br>");

// -- Result --
// *** 41 배열 펼침 연산자(결합) ***
// array,object,react,vue
```
{% endcode %}

## \* 데이터 저장, 데이터 출력

1. 데이터 저장

   * 변수
   * 배열
   * 객체

2. 데이터  출력
   * 함수

## 42. 선언적 함수 

가장 기본적으로 사용하는 함수의 형태이다. 기본적으로 함수는 함수 이름을 설정하고 함수 이름을 호출해야 실행된다.

{% code title="선언적 함수 Syntax" %}
```javascript
function 함수이름() {
    // 실행 코드
}

함수이름(); // 함수 호
```
{% endcode %}

{% code title="선언적 함수" %}
```javascript
function func1() {
    document.write("*** 42 선언적 함수 *** <br>");
    document.write("func1이 실행되었습니다.<br><br>");
};

func1();

// -- Result --
// *** 42 선언적 함수 ***
// func1이 실행되었습니다.
```
{% endcode %}

## 43. 익명 함수

**익명 함수**란 **함수의 이름을 지정할 때, 변수의 이름을 빌려서 사용**하는 것이다. 

익명 함수는 함수에 이름이 없기 때문에 변수에 넣어서 사용하는 함수이다. 변수에는 숫자, 문자도 들어갈 수 있지만 함수도 들어갈 수 있다.

{% code title="익명 함수 Syntax" %}
```javascript
var 변수이름 = function(){
     //실행 코드
}

변수이름(); //함수 호출
```
{% endcode %}

{% code title="익명 함수" %}
```javascript
const func2 = function () {
    document.write("*** 43 익명 함수 *** <br>");
    document.write("func2가 실행되었습니다.<br><br>");
};

func2();

// -- Result --
// *** 43 익명 함수 ***
// func2가 실행되었습니다.
```
{% endcode %}

## 44. 매개 변수가 있는 함수 

{% code title="매개 변수가 있는 함수" %}
```javascript
function func3(name) {
    document.write("*** 44 매개 변수가 있는 함수 *** <br>");
    document.write("func3이 실행되었습니다.<br><br>");
}

func3();

// -- Result --
// *** 44 매개 변수가 있는 함수 ***
// func3이 실행되었습니다.
```
{% endcode %}

## 45. 리턴 값이 있는 함수 

**리턴 값이 있는 함수는 결과 값이 있는 함수**이다. `return` 이라는 키워드를 이용하여 함수의 결과 값을 출력하는 방법이다. 리턴 값은 실행문을 강제로 종료하는 역할도 한다. 

{% code title="리턴 값이 있는 함수" %}
```javascript
function func4() {
    const str = "func4가 실행되었습니다.<br><br>";
    return str; // 출력하는 역할
};

// func4(); -> 작동되지 않는다.

document.write("*** 45 리턴값이 있는 함수 *** <br>");
document.write(func4(), "<br><br>");

// -- Result --
// *** 45 리턴값이 있는 함수 ***
// func4가 실행되었습니다.
```
{% endcode %}

## 46. 재귀 함수 

**재귀 함수**는 **함수 정의문 내에서 다시 함수를 호출 시켜주는 함수**이다. **함수를 여러 번 실행** 시킬 때 사용한다.

{% code title="재귀 함수" %}
```javascript
function func5(num) {
    if (num == 0) {
        document.write("func5이 실행되었습니다.<br>");
    } else {
        document.write("func5이 샐힝되었습니다.<br>");
        func5(num - 1);
    }
};

document.write("*** 46 재귀 함수 *** <br>");
func5(9);

// -- Result --
// *** 46 재귀 함수 ***
// func5이 샐힝되었습니다.
// func5이 샐힝되었습니다.
// func5이 샐힝되었습니다.
// func5이 샐힝되었습니다.
// func5이 샐힝되었습니다.
// func5이 샐힝되었습니다.
// func5이 샐힝되었습니다.
// func5이 샐힝되었습니다.
// func5이 샐힝되었습니다.
// func5이 샐힝되었습니다.
```
{% endcode %}

{% code title="재귀 함수를 잘 못 사용한 예제" %}
```javascript
// 이런 경우 무한 루프에 빠지므로 사이트가 다운된다. 

function func5() {
    document.write("*** 46 재귀 함수 *** <br>");
    func5();
}
```
{% endcode %}

## 47. 콜백 함수 

**콜백 함수**는 **함수를 실행시키고 난 뒤, 또 함수를 실행** 시키고 싶을 때 사용하는 함수이다.

{% code title="콜백 함수" %}
```javascript
function func6() {
    document.write("func6이 실행되었습니다. <br><br>");
}

// callback안에 매개변수를 넣어주고, 매개변수를 함수화 시킴.
function callback(text) {
    text(); // 매개 변수를 함수화 시킴
}

document.write("*** 47 콜백 함수 *** <br>");

// 실행 함수 안에 매개변수를 함수화 시킴
callback(func6);

// -- Result --
// *** 47 콜백 함수 ***
// func6이 실행되었습니다.
```
{% endcode %}

## 48. 콜백 함

**함수를 변수 혹은 매개변수인 것처럼 처리**를 한다.

{% code title="콜백 함수" %}
```javascript
function func7() {
    document.write("func7이 실행되었습니다.<br>");
};

function callback(num) {
    for( let i = 1; i <= 10; i++ ) {
        num(i);
    }
};

document.write("*** 48 콜백 함수 *** <br>");

callback(func7);

// -- Result --
// *** 48 콜백 함수 ***
// func7이 실행되었습니다.
// func7이 실행되었습니다.
// func7이 실행되었습니다.
// func7이 실행되었습니다.
// func7이 실행되었습니다.
// func7이 실행되었습니다.
// func7이 실행되었습니다.
// func7이 실행되었습니다.
// func7이 실행되었습니다.
// func7이 실행되었습니다.
```
{% endcode %}

{% code title="콜백 함수" %}
```javascript
function callback(num) {
    for ( let i = 0; i <= 10; i++ ) {
        num(i);
    }
};

const func6 = function (i) { // 익명 함수인데 매개 변수가 있음
    document.write("func6이 실행되었습니다.<br>"); // 실행 함수
};

document.write("*** 47 콜백 함수 *** <br>");
callback(func6);

// -- Result --
// *** 47 콜백 함수 ***
// func6이 실행되었습니다.
// func6이 실행되었습니다.
// func6이 실행되었습니다.
// func6이 실행되었습니다.
// func6이 실행되었습니다.
// func6이 실행되었습니다.
// func6이 실행되었습니다.
// func6이 실행되었습니다.
// func6이 실행되었습니다.
// func6이 실행되었습니다.
// func6이 실행되었습니다.
```
{% endcode %}

## 48-1. 콜백 함수 \(동기\)

**동기 콜백 함수**는 함수가 **순서대로 실행** 된다.

{% code title="콜백 함수 \(동기\)" %}
```javascript
function a() {
    console.log("a");
};

function b() {
    console.log("b");
}

a();
b();

// -- RESULT --
// a
// b
```
{% endcode %}

{% code title="콜백 함수\(동기\)" %}
```javascript
function funcA() {
    document.write("funcA가 실행되었습니다. <br>");
};

function funcB() {
    document.write("funcB가 실행되었습니다. <br>");
};

document.write("*** 48-1 콜백 함수(동기) *** <br>");

funcA();
funcB();

// -- RESULT --
// *** 48-1 콜백 함수(동기) ***
// funcA가 실행되었습니다.
// funcB가 실행되었습니다.
```
{% endcode %}

## 48-2. 콜백 함수 \(동기\)

**비동기 콜백 함수**는 함수의 **순서가 바뀌어서 실행** 된다.

{% code title="콜백 함수 \(비동기\)" %}
```javascript
function c() {
    setTimeout(function() {
        console.log("c");
    }, 1000);
};

function d() {
    console.log("d");
};

c();
d();

// -- RESULT --
// d
// c
```
{% endcode %}

**비동기 콜백 함수**는 A를 실행한 후 싹 다 **초기화**되어버린다.

{% code title="콜백 함수 \(비동기\)" %}
```javascript
function funcA() {
    setTimeout(function() {
        document.write("funcA가 실행되었습니다. <br>");
    }, 1000);
};

function funcB() {
    document.write("funcB가 실행되었습니다. <br>");
};

document.write("*** 48-1 콜백 함수(비동기) *** <br>");

funcA();
funcB();

// -- RESULT --
// *** 48-1 콜백 함수(비동기) ***
// funcB가 실행되었습니다. 

// 이 후에 모든 출력이 사라지고 아래와 같이 funcA만 실행 된다.
// // funcA가 실행되었습니다.
```
{% endcode %}

## 48-3. 콜백 함수 

a 가 실행된 후, b 가 실행된다. 즉, **동기\(순서\)를 맞추기 위한 것**이다. 정식 법이 아니다.

{% code title="콜백 함수" %}
```javascript
function a(callback) {
    setTimeout(function() {
        console.log("a");
        callback();
    }, 1000);
};

function b() {
    console.log("b");
}

// a가 끝나고 b가 실행
a(function(){
    b();
});

// -- RESULT --
// a
// b
```
{% endcode %}

{% code title="콜백 함수\(동기\)" %}
```javascript
function funcA(callback) {
    setTimeout(function() {
        document.write("funcA가 실행되었습니다. <br>");
        callback();
    }, 1000);
};

function funcB() {
    document.write("funcB가 실행되었습니다. <br>");
};

document.write("*** 48-2 콜백 함수(동기) *** <br>");

funcA(function(){
    funcB();
});

// -- RESULT --
// *** 48-2 콜백 함수(동기) ***
// 이후 모든 출력이 사라지고 아래와 같이 출력 된다.
// funcA가 실행되었습니다.
// funcB가 실행되었습니다. 
```
{% endcode %}

## 48-4. 콜백 지옥 

{% code title="콜백 지옥" %}
```javascript
function a(callback) {
    setTimeout(function () {
        console.log("a");
        callback();
    }, 1000);
};

function b(callback) {
    setTimeout(function () {
        console.log("b");
        callback();
    }, 1000);
};

function c(callback) {
    setTimeout(function () {
        console.log("c");
        callback();
    }, 1000);
};

function d(callback) {
    setTimeout(function () {
        console.log("d");
    }, 1000);
};

a(function () {
    b(function () {
        c(function () {
            d();
        });
    });
});

// -- RESULT --
// a
// b
// c
// d
```
{% endcode %}

## 49. 즉시 실행 함수

**즉시 실행 함수**는 이름 그대로 **즉시 실행 함수**이다. 즉, **선언과 동시에 실행**이 된다. 호출 함수를 생략한다.

{% code title="즉시 실행 함수 " %}
```javascript
(function() {
    console.log();
}());
```
{% endcode %}

기존의 함수 호출 방식과는 다르게 선언과 동시에 실행되는 즉시 실행 함수이다. 또한, 내부에 있는 변수를 외부에서의 접근을 통제할 수 있다. 이러한 이유로 즉시 실행 함수는 플러그인이나 라이브러리에 많이 사용하고 있다. 이러한 플러그인이나 라이브러리 같은 경우는 변수에 추가하지 않아도 되기에 코드 충돌을 방지할 수 있고, 외부 접근을 통제할 수 있도록 하기 위해 즉시 실행 함수를 이용한다.

```javascript
// 외부 허용

var fn = (function() {
  var name = "lee";
  
  return {
    name: name
  }
}());

console.log(fn.name); // lee


//외부 허용 x
(function(){
  var name = "lee";
  
  return {
    name: name
  }
}())
```

{% code title="일반 함수와 즉시 실행 함수" %}
```javascript
// 일반 함수 호

function func8() {
    document.write("func8이 실행되었습니다. <br><br><br>");
};

document.write("*** 49 즉시 실행 함수 *** <br>");

func8();

// -- RESULT --
// *** 49 즉시 실행 함수 ***
// func8이 실행되었습니다.


// 즉시 실행 함수 : 호출 함수 생략 
(function () {
    document.write("*** 49 즉시 실행 함수 *** <br>");
    document.write("func8이 실행되었습니다. <br><br><br>");
}());

// -- RESULT --
// *** 49 즉시 실행 함수 ***
// func8이 실행되었습니다.
```
{% endcode %}

## 50. 화살표 함수 \(선언적 함수\)

화살표 함수는 `function` 키워드 대신 화살표\(=&gt;\)를 사용하여 좀 더 간단하게 함수를 사용할 수 있는 함수이다.

{% code title="Arrow Function Syntax" %}
```javascript
() => {
    // 실행문
};
```
{% endcode %}

### 화살표 함수 규칙 

* 매개 변수가 하나인 경우 괄호를 생략할 수 있음 
* 매개 변수가 두 개 이상인 경우 괄호를 생략할 수 없음
* 코드 블록을 지정하지 않고 한 문장으로 작성 시 return 문은 생략할 수 있음 
* 코드 블록을 지정했을 경우 return 문은 생략할 수 없음.

{% code title="선언적 함수" %}
```javascript
// 선언적 함
function func9() {
    document.write("*** 50 화살표 함수 *** <br>");
    document.write("func9이 실행되었습니다.");
};

func9();

// -- RESULT --
// *** 50 화살표 함수 ***
// func9이 실행되었습니다.
```
{% endcode %}

{% code title="화살표 함수 \(선언적 함수\)" %}
```javascript
// 화살표 함수 (선언적 함수)

func9 = () => {
    document.write("*** 50 화살표 함수 *** <br>");
    document.write("func9이 실행되었습니다.");
};

func9();

// -- RESULT --
// *** 50 화살표 함수 ***
// func9이 실행되었습니다.
```
{% endcode %}

## 51. 화살표 함수 \(익명 함수\)

{% code title="익명 함수" %}
```javascript
// 익명 함수
const func10 = function () {
    document.write("*** 51 화살표 함수(익명 함수) *** <br>");
    document.write("func10이 실행되었습니다. <br><br><br>");
};

func10();

// -- RESULT --
// *** 51 화살표 함수(익명 함수) ***
// func10이 실행되었습니다.
```
{% endcode %}

{% code title="화살표 함수 \(익명 함수\)" %}
```javascript
// 화살표 함수 (익명 함수)

const func10 = () => {
    document.write("*** 51 화살표 함수(익명 함수) *** <br>");
    document.write("func10이 실행되었습니다. <br><br><br>");
};

func10();

// -- RESULT --
// *** 51 화살표 함수(익명 함수) ***
// func10이 실행되었습니다.
```
{% endcode %}

## 52. 화살표 함수 \(리턴 값이 있는 함수\)

{% code title="리턴 값이 있는 함수" %}
```javascript
// 리턴 값이 있는 함수

function func11() {
    const str = "func11이 실행되었습니다. <br><br>";
    return str;
};

document.write("*** 52 화살표 함수(리턴 값이 있는 함수) *** <br>");
document.write(func11());

// -- RESULT --
// *** 52 화살표 함수(리턴 값이 있는 함수) ***
// func11이 실행되었습니다.
```
{% endcode %}

```javascript
// 화살표 함수 (리턴 값이 있는 함수)

const func11 = () => {
    const str = "func11이 실행되었습니다. <br><br>";
    return str;
};

document.write("*** 52 화살표 함수(리턴 값이 있는 함수) *** <br>");
document.write(func11());

// -- RESULT --
// *** 52 화살표 함수(리턴 값이 있는 함수) ***
// func11이 실행되었습니다.
```

## 53. 화살표 함수 \(리턴값 + 매개변수\)

{% code title="화살표 함수 \(리턴값 + 매개변수\)" %}
```javascript
// 화살표 함수 (리턴값 + 매개변수)

const func12 = (str) => {
    return str;
}

document.write("*** 53 화살표 함수(리턴값 + 매개변수) *** <br>");
document.write(func12("func12이 실행되었습니다. <br><br>"));

// -- RESULT --
// *** 53 화살표 함수(리턴값 + 매개변수) ***
// func12이 실행되었습니다.
```
{% endcode %}

## 54. 화살표 함수 \(리턴값 + 매개변수 생략\)

{% code title="화살표 함수 \(리턴값 + 매개변수 생략\)" %}
```javascript
// 화살표 함수 (리턴값 + 매개변수 생략)

const func13 = str => {
    return str;
}

document.write("*** 54 화살표 함수(리턴값 + 매개변수 생략) *** <br>");
document.write(func13("func13이 실행되었습니다. <br><br>"));

// -- RESULT --
// *** 53 화살표 함수(리턴값 + 매개변수) ***
// func12이 실행되었습니다.
```
{% endcode %}

## 55. 화살표 함수 \(리턴값 생략 + 매개변수 생략\)

{% code title="화살표 함수 \(리턴값 생략 + 매개변수 생략\)" %}
```javascript
// 화살표 함수 (리턴값 생략 + 매개변수 생략)

const func14 = str => str;

document.write("*** 55 화살표 함수(리턴값 생략 + 매개변수 생략) *** <br>");
document.write(func14("func14이 실행되었습니다. <br><br>"));

// -- RESULT --
// *** 55 화살표 함수(리턴값 생략 + 매개변수 생략) ***
// func14이 실행되었습니다.
```
{% endcode %}

{% hint style="info" %}
_**React 에서 많이 사용.**_
{% endhint %}

## 56. Default Parameters

{% code title="Default Parameters 기본 문법" %}
```javascript
// Default Parameters 기본 문법

function func15(str) {
    if (str == null) {
        str = "func15이 실행되었습니다. <br><br>";
        document.write(str);
    }
};

func15();

// -- RESULT --
// *** 56 Default Parameters ***
// func15이 실행되었습니다.
```
{% endcode %}

{% code title="Default Parameters 최신 문법" %}
```javascript
// 최신 문법 : 파라미터로 디폴트 값을 넘겨줄 수 있음

function func15(str = "func15이 실행되었습니다. <br><br>") {
    document.write(str);
};

document.write("*** 56 Default Parameters *** <br>");
func15();

// -- RESULT --
// *** 56 Default Parameters ***
// func15이 실행되었습니다.
```
{% endcode %}

## 57. 조건부 연산자 함수\(Ternary Operator\) = 삼항 연산자

{% code title="조건부 연산자 함수, if else 문" %}
```javascript
// 조건부 연산자 함수, if else 문

let Ternary = true; // true
// let Ternary = false; // flase
// let Ternary = undefined; // flase
// let Ternary = null; // false
// let Ternary = []; // true
// let Ternary = ''; // false
// let Ternary = 0; // false

function func16() {

    if (Ternary) {
        document.write("func16 true가 실행되었습니다. <br><br>");
    } else {
        document.write("func16 false가 실행되었습니다. <br><br>");
    }
 
 };
 
document.write("*** 57 조건부 연산자 함수(Ternary Operator) = 삼항 연산자 *** <br>");
func16();

// -- RESULT --
// *** 57 조건부 연산자 함수(Ternary Operator) = 삼항 연산자 ***
// func16 true가 실행되었습니다.

```
{% endcode %}

{% code title="조건부 연산자 함수, 삼항 연산자" %}
```javascript
// 조건부 연산자 함수, 삼항 연산자

let Ternary = true; // true
// let Ternary = false; // flase
// let Ternary = undefined; // flase
// let Ternary = null; // false
// let Ternary = []; // true
// let Ternary = ''; // false
// let Ternary = 0; // false

function func16() {

    Ternary ? document.write("True <br><br>") : document.write("False <br><br>");
 
document.write("*** 57 조건부 연산자 함수(Ternary Operator) = 삼항 연산자 *** <br>");
func16();

// -- RESULT --
// *** 57 조건부 연산자 함수(Ternary Operator) = 삼항 연산자 ***
// True
```
{% endcode %}

## 58. 템플릿 리터럴 \(Template Literals\)

**템플릿 리터럴은 백틱\(backtick\) 문자 ````` 를 사용하여 새로운 문자열을 삽입**할 수 있는 기능을 제공한다. 이를 문자열 인터폴레이션\(String Interpolation\)이라 한다.

{% code title="템플릿 리터럴 \(Template Literals\) Syntax" %}
```javascript
`${ … }`
```
{% endcode %}

{% code title="일반 함수" %}
```javascript
// 일반 함수

function func17(name) {
    document.write("func17이 실행되었습니다. <br><br>");
};

document.write("*** 58 템플릿 리터럴(Template Literals) *** <br>");
func17();

// -- RESULT --
// *** 58 템플릿 리터럴(Template Literals) ***
// func17이 실행되었습니다.
```
{% endcode %}

{% code title="템플릿 리터럴 \(Template Literals\)" %}
```javascript
// 템플릿 리터럴 (Template Literals)

function func17(name) {
    document.write("1. " + name + "이 실행되었습니다. <br>");
    document.write(`2. ${name}이 실행되었습니다. <br><br>`);
};

document.write("*** 58 템플릿 리터럴(Template Literals) *** <br>");
func17("func17");

// -- RESULT --
// *** 58 템플릿 리터럴(Template Literals) ***
// 1. func17이 실행되었습니다.
// 2. func17이 실행되었습니다.
```
{% endcode %}

## 59. 템플릿 리터럴 \(Template Literals\)

{% code title="템플릿 리터럴 \(Template Literals\)" %}
```javascript
// 템플릿 리터럴 (Template Literals)

const func18 = [
    { name: "1. func18", result: "실행되었습니다."},
    { name: "2. func18", result: "실행되었습니다."},
]

const result =
    `${func18[0].name}가 ${func18[0].result} <br>
     ${func18[1].name}가 ${func18[1].result}`;

document.write("*** 59 템플릿 리터럴(Template Literals) *** <br>");
document.write(result);

// -- RESULT --
// *** 59 템플릿 리터럴(Template Literals) ***
// 1. func18가 실행되었습니다.
// 2. func18가 실행되었습니다.
```
{% endcode %}

## 60. 템플릿 리터럴 \(Template Literals\)

{% code title="템플릿 리터럴 \(Template Literals\)" %}
```javascript
// 템플릿 리터럴 (Template Literals)

const func19 = (str) => {
    document.write(`${str}`);
};

document.write("*** 60 템플릿 리터럴(Template Literals) *** <br>");
func19("func19 함수가 실행되었습니다.");

// -- RESULT --
// *** 60 템플릿 리터럴(Template Literals) ***
// func19 함수가 실행되었습니다.
```
{% endcode %}

##  변수, 배열, 객체, 함수, 객체 지향 함수, 클래

* 변수 : 데이터를 저장하는 곳\(한 개\), 변수가 변함
* 상수 : 데이터를 저장하는 곳\(한 개\), 변수가 변하지 않
* 배열 : 데이터를 저장하는 곳\(두  개 이상\)
* 객체 : 데이터를 저장하는 곳\(두 개 이상, "키, 값"\)  
* 함수 : 데이터 실행\(출력\)
* 객체 + 함수 : 객체 지향 함수
* 클래스 : 함수의 집합체 &gt; 클래스 함수 &gt; 최종 &gt; 프레임웍\(리액트, 뷰, 앵귤러\)
* 데이터 베이스 : MySQL, Firebase, aws, ajax, json, API

## 61. 객체 + 함수 \(매개 변수로 출력하기\)

{% code title="객체 + 함수 \(매개 변수로 출력하기\)" %}
```javascript
// 객체 + 함수 (매개 변수로 출력하기)

function func20(num, name, job) {
    document.write( num + ". 내 이름은 " + name + "이며, 직업은 " + job + "입니다. <br>");
};

document.write("*** 61 객체 + 함수 (매개 변수로 출력하기) *** <br>");

func20("1", "웹스", "웹 퍼블리셔");
func20("2", "웹스토리보이", "프론트앤드 개발자");

// -- RESULT --
// *** 61 객체 + 함수 (매개 변수로 출력하기) ***
// 1. 내 이름은 웹스이며, 직업은 웹 퍼블리셔입니다.
// 2. 내 이름은 웹스토리보이이며, 직업은 프론트앤드 개발자입니다.
```
{% endcode %}

## 62. 객체 + 함수 \(변수로 출력하기\)

{% code title="객체 + 함수 \(변수로 출력하기\)" %}
```javascript
// 객체 + 함수 (변수로 출력하기)

function func21(num, name, job) {
    document.write( num + ". 내 이름은 " + name + "이며, 직업은 " + job + "입니다. <br>");
};

const youNum1 = "1";
const youName1 = "웹스";
const youJob1 = "웹 퍼블리셔";

const youNum2 = "2";
const youName2 = "웹스토리보이";
const youJob2 = "프론트앤드 개발자";

document.write("*** 62 객체 + 함수 (변수로 출력하기) *** <br>");

func21(youNum1, youName1, youJob1);
func21(youNum2, youName2, youJob2);

// -- RESULT --
// *** 62 객체 + 함수 (변수로 출력하기) ***
// 1. 내 이름은 웹스이며, 직업은 웹 퍼블리셔입니다.
// 2. 내 이름은 웹스토리보이이며, 직업은 프론트앤드 개발자입니다.
```
{% endcode %}

## 63. 객체 + 함수 \(객체로 출력하기\)

{% code title="객체 + 함수 \(객체로 출력하기\)" %}
```javascript
// 객체 + 함수 (객체로 출력하기)

function func22(num, name, job) {
    document.write( num + ". 내 이름은 " + name + "이며, 직업은 " + job + "입니다. <br>");
};

let info = [
    {
        num: 1,
        name: "웹스",
        job: "웹 퍼블리셔"
    },
    {
        num: 2,
        name: "웹스토리보이",
        job: "프론트앤드 개발자"
    }
]

document.write("*** 63 객체 + 함수 (객체로 출력하기) *** <br>");

func22(info[0].num, info[0].name, info[0].job);
func22(info[1].num, info[1].name, info[1].job);

// -- RESULT --
// *** 63 객체 + 함수 (객체로 출력하기) ***
// 1. 내 이름은 웹스이며, 직업은 웹 퍼블리셔입니다.
// 2. 내 이름은 웹스토리보이이며, 직업은 프론트앤드 개발자입니다.
```
{% endcode %}

## 64. 객체 + 함수 \(변수\)

{% code title="객체 + 함수 \(변수\)" %}
```javascript
// 객체 + 함수 (변수)

const info = {
    num1: 1,
    name1: "웹스",
    job1: "웹 퍼블리셔",
    num2: 2,
    name2: "웹스토리보이",
    job2: "프론트앤드 개발자",
    result1: function() {
        document.write(this.num1 + ". 내 이름은 " + this.name1 + "이며, 직업은 " + this.job1 + "입니다. <br>" );
    },
    result2: function() {
        document.write(this.num2 + ". 내 이름은 " + this.name2 + "이며, 직업은 " + this.job2 + "입니다. <br>" );
    },
}

document.write("*** 64 객체 + 함수 (변수) *** <br>");

info.result1();
info.result2();

// -- RESULT --
// *** 64 객체 + 함수 (변수) ***
// 1. 내 이름은 웹스이며, 직업은 웹 퍼블리셔입니다.
// 2. 내 이름은 웹스토리보이이며, 직업은 프론트앤드 개발자입니다.
```
{% endcode %}

## 65. 객체 생성자 함수

변수 안에 `객체 + 함수`는 복잡하다. 대신 **함수 안에 넣어 작업**하는 것이 **객체 생성자 함수**이다.

{% code title="객체 생성자 함수" %}
```javascript
// 객체 생성자 함수

function func23(num, name, job) {

    // 데이터를 가져와서 변수화 시켜 줌
    this.num = num; 
    this. name = name;
    this.job = job;
    this.result = function() {
        document.write( this.num + ". 내 이름은 " + this.name + "이며, 직업은 " + this.job + "입니다. <br>");
    };
}

// 인스턴스 생성
let info1 = new func23("1", "웹스", "웹 퍼블리셔");
let info2 = new func23("2", "웹스토리보이", "프론트앤드 개발자");

document.write("*** 65 객체 생성자 함수 *** <br>");

info1.result();
info2.result();

// -- RESULT --
// *** 65 객체 생성자 함수 ***
// 1. 내 이름은 웹스이며, 직업은 웹 퍼블리셔입니다.
// 2. 내 이름은 웹스토리보이이며, 직업은 프론트앤드 개발자입니다.
```
{% endcode %}

{% hint style="info" %}
_**인스턴스**_

인스턴스는 객체 생성자 함수의 **매개 변수**이다.  
객체 생성자 함수에  **new** 라는 키워드를 붙여 **새롭게 객체를 만든 것**이다.
{% endhint %}

## 66. 프로토타입 메서드 \(함수\)

함수가 많아지고 복잡해지므로 함수를 따로 빼준 것이 프로토 타입 함수이다. 자바스크립트 안에서만 프로토타입이 존재한다.

{% code title="프로토타입 메서드 \(함수\)" %}
```javascript
// 프로토타입 메서드 (함수)

function func24(num, name, job) {

    // 데이터를 가져와서 변수화 시켜 줌
    this.num = num;
    this.name = name;
    this.job = job;
};

// 결국 함수 안에 있는 것을 밖으로 꺼냄
func24.prototype.result = function () {
    document.write(this.num + ". 내 이름은 " + this.name + "이며, 직업은 " + this.job + "입니다. <br>");
}

// 인스턴스 생성
let info1 = new func23("1", "웹스", "웹 퍼블리셔");
let info2 = new func23("2", "웹스토리보이", "프론트앤드 개발자");

document.write("*** 66 프로토타입 메서드 (함수) *** <br>");

info1.result();
info2.result();

// -- RESULT --
// *** 66 프로토타입 메서드 (함수) ***
// 1. 내 이름은 웹스이며, 직업은 웹 퍼블리셔입니다.
// 2. 내 이름은 웹스토리보이이며, 직업은 프론트앤드 개발자입니다.
```
{% endcode %}

## 67. 객체 리터럴 함수 

리터럴 이란? 하나로 집합시켜 놓은 것 즉, 뭉쳐 놓은 것이다. 

함수를 따로 빼서 사용했지만, 여전히 중복되는 것이 많으므로 **중복되는 것을 하나로 빼주기 위해 사용하는 것이 객체 리터럴 함수**이다. 만약, this가 보인다면 객체 생성자 함수라고 생각하면 된다.

{% code title="객체 리터럴 함수" %}
```javascript
// 객체 리터럴 함수

// ** 변수값 **
function func25(num, name, job) {

    // 데이터를 가져와서 변수화 시켜 줌
    this.num = num;
    this.name = name;
    this.job = job;
};

// ** 함수값 **
// 여러 개 만들어지므로 문제이다. 그래서 하나로 합
func25.prototype = {
    result1: function() {
        document.write(this.num + ". 내 이름은 " + this.name + "이며, 직업은 " + this.job + "입니다. <br>");
    },
    result2: function() {
        document.write(this.num + ". 내 이름은 " + this.name + "이며, 직업은 " + this.job + "입니다. <br>");
    }
};

// 인스턴스 생성
let info1 = new func25("1", "웹스", "웹퍼블리셔");
let info2 = new func25("2", "웹스토리보이", "프론트앤드 개발자");

document.write("*** 67 객체 리터럴 함수 *** <br>");

info1.result1();
info2.result2();

// -- RESULT --
// ***  67 객체 리터럴 함수 ***
// 1. 내 이름은 웹스이며, 직업은 웹 퍼블리셔입니다.
// 2. 내 이름은 웹스토리보이이며, 직업은 프론트앤드 개발자입니다.
```
{% endcode %}

## 68. 클래스

**클래스**는 **한눈에 보기 쉽게 깔끔하게 정리**한 것이다. 하지만 세팅할 때 복잡하다. 클래스는 **함수의 집합체**이며, **클래스를 만들면 인스턴스 즉, 변수를 생성**해야 한다.

{% code title="클래스" %}
```javascript
// 클래스

class study {
    // 클래스가 실행됐을 때, 항상 실행되는 것
    constructor(num, name, job) {
    
        // 데이터를 가져와서 변수화 시켜 줌
        this.num = num;
        this.name = name;
        this.job = job;
    }

    result() {
        document.write(this.num + ". 내 이름은 " + this.name + "이며, 직업은 " + this.job + "입니다. <br>");
    }
}

// 인스턴스 생성
let info1 = new study("1", "웹스", "웹퍼블리셔");
let info2 = new study("2", "웹스토리보이", "프론트앤드 개발자");

document.write("*** 68 클래스 *** <br>");

info1.result();
info2.result();

// -- RESULT --
// ***  68 클래 ***
// 1. 내 이름은 웹스이며, 직업은 웹 퍼블리셔입니다.
// 2. 내 이름은 웹스토리보이이며, 직업은 프론트앤드 개발자입니다.
```
{% endcode %}

## 69. 클래스 상속

기존 클래스를 상속받고 싶을 때, 클래스 상속을 사용한다. **상속 시킨 후 프로퍼티를 추가**해야 한다.

{% code title="클래스 상속" %}
```javascript
// 클래스 상속

class study {
    // 클래스가 실행됐을 때, 항상 실행되는 것
    constructor(num, name, job) {
        // 데이터를 가져와서 변수화 시켜 줌
        this.num = num;
        this.name = name;
        this.job = job;
    }

    result() {
        document.write(this.num + ". 내 이름은 " + this.name + "이며, 직업은 " + this.job + "입니다. <br>");
    }
}

class study2 extends study {
    constructor(num, name, job, age) {
        // 기존에 것을 그대로 사용하고 프로퍼티를 추가하고 싶을 때, super 키워드를 사용. (이때! 기존 것만 매개변수로 가져와야 함)
        super(num, name, job);
        this.age = age;
    }

    result2() {
        document.write(this.num + ". 내 이름은 " + this.name + "이며, 직업은 " + this.job + "입니다. <br>");
    }
}

// 인스턴스 생성
let info1 = new study("1", "웹스", "웹퍼블리셔");
let info2 = new study2("2", "웹스토리보이", "프론트앤드 개발자", "40");

document.write("*** 69 클래스 상속 *** <br>");

info1.result();
info2.result();
info2.result2();

// -- RESULT --
// ***  68 클래 ***
// 1. 내 이름은 웹스이며, 직업은 웹 퍼블리셔입니다.
// 2. 내 이름은 웹스토리보이이며, 직업은 프론트앤드 개발자입니다.
// 2. 내 이름은 웹스토리보이이며, 직업은 프론트앤드 개발자입니다.
```
{% endcode %}


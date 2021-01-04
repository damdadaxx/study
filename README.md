---
description: javascript study
---

# javascript-100

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
let b = 200; // Uncaught SyntaxError: Identifier 'a' has already been declared
b = 300; // 가능

// const
const c = 100;
const c = 200;// Uncaught SyntaxError: Identifier 'a' has already been declared
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

데이터를 불러올 때에는 `arr5[2][0]`와 같이 배열의 2번째 중 1번째의 데이터를 호출해야 정확하게 불러올 수 있다.

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

배열의 개를 구할 때에는 변수 이름 뒤에 `.length` 를 붙이면 배열의 개수를 알 수 있다.

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
3. 문장 실행된다. 많은 문장을 실행할 경우에는 { } 를 사용해서 문장들을 묶어 준다.
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

{% code title="rray.prototype.forEach\(\)" %}
```javascript
arr.forEach( callback (currentvalue[, index[, array]])[, thisArg])
```
{% endcode %}

* `callback` - 각 요소에 대해 실행 할 함수. 다음 세 가지의 매개 변수를 받는다.
* `currentvalue` - 처리할 현재 요소
* `index` - \(option\) 처리할 현재 요소의 인덱스
* `array` - \(option\) `forEach()` 를 호출한 배열
* `thisArg` - \(option\) `callback` 을 실행할 때 `this` 로 사용할 

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

 **`map( )`** 메서드 는 호출 배열의 모든 요소에 대해 제공된 함수를 호출 한 결과로 채워진 **새 배열을 만든다.** 차이점은 있지만 **`forEach( )`** 와 같다.

{% code title="array.prototype.map\(\)" %}
```javascript
array.map(callback(currentValue[, index[, array]])[, thisArg])
```
{% endcode %}

{% code title="map\(\) 방법 1" %}
```javascript
const arr9 = [100, 200, "javascript"];

arr9.forEach(function( elem ) {
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

arr9.forEach( elem => {
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

arr9.forEach( (element, index, array) => {
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
animals.forEach( elem => {
  console.log(elem);
});

// -- Result --
// a
// b
```
{% endcode %}

### 3. map\( \)

배열의 각 요소에 대해 `callback` 을 실행하고 실행 결과를 **모은 새 배열을 리턴**한다. 배열을 순회하므로 중간에 `break;` 문을 사용할 수 없다. 이런 경우라면 `for( )` 문을 사용해야 한다.

{% code title="map\(\)" %}
```javascript
array.map(callback(currentValue[, index[, array]])[, thisArg])

// 예제
const a = ["a", "b"];
aa = animals.map(elem => {
  console.log(elem);
});
console.log(aa);

// -- Result --
// a
// b
// [undefined, undefined] -> 별도의 return이 없기때문에 순회했던 개수만큼의 undefined 원소
```
{% endcode %}

`map( )` 의 용도를 제대로 살리려면 `return` 문이 있어야 한다. `return` 문이 포함되면 배열의 각 요소에 대해 `callback` 을 실행하고 실행 결과를 모은 새 배열을 리턴 했다.

{% code title="map\(\), return" %}
```javascript
// 예제
const a = ["a", "b"];
aa = animals.map(elem => {
  console.log(elem);
  return "alphabet" + a;
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

배열을 순회 후 새 배열을 얻고 싶다면 _**map\(\)**_
{% endhint %}

## 11. 배열 불러오기 \(for...in 문\)

**`for...in`** 문은 **객체의 프로퍼티명을 열거하는 반복문**이다.

{% code title="for...in 문" %}
```javascript
for (variable in object) {
  statements : 객에 열거할 수 있는 모든 프로퍼티의 개수만큼 반복적으로 실행하고자 하는 실행문;
}
```
{% endcode %}

배열도 객체로 놓고 보자면 인덱스의 숫자가 프로퍼티명에 해당하기 때문에 `for...in` 문에 나열할 수 있다. 하지만 배열 요소를 나열할 때는 `for...in` 문의 사용을 권장하지 않는다.

### `for...in` 문에서 주의할 사항

1. 프로퍼티를 열거하는 순서

   객체 리터럴 식에 쓴 것에 대한 결과 값이 순서대로 나오기는 하지만 객체 리터럴에 쓴 순서대로 열거되지는 않는다. 즉, 순서가 보장되는 것이 아니다. 원래 프로퍼티 간에는 순서가 없는 것으로 순서를 의식하는 것 자체가 잘못된 것이다. 

   하지만, 배열의 경우는 순서를 의식하는 데이터 타입이다. 아래의 예제에서 기대한 순서를 보이고 있지만 `for...in` 문은 순서를 보장하지 않기 때문에 이 같은 동작 방식에  지나치게 의존해서는 안된다.

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
// *** 12 배열 불러오기(for in문) ***
// 100200javascript
```
{% endcode %}

배열이나 객체에 따라 사용하는 방법이 다르다. `for...in 문` 같은 배열, `for...of 문` 은 객체.

## \* for...in vs for...of

### 1. for...in

모든 객체의 모든 열거 가능한 속성을 반복한다. 즉, **객체의 요소**들\(Data\)를 순회하기 위한 구문이다.

* **인덱스가 리턴**
* 루프 구문이 요소들만 순회하는 것이 아니라 프로토타입 체임도 순회
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

*  **값이 리턴**되어 바로 값을 사용할 수 있음
* 배열 순회를 지원하는 문법 중에서 가장 간결하고 직접적으로 접근 가능
* forEach\(\) 에서 지원하지 않는 break, continue, return  구문 사용 가

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

### 3. for...in VS for...of 예

{% code title="for...in VS for...of VS \(collection\)" %}
```javascript
// for...in : index 리턴
document.write('*** for...in 예제 *** <br>');

const num = [1, 2, 3, 4, 5];

for (let i in num) {
    document.write(i);
}

document.write("<br><br><br>");


// for...of : 값 리턴
document.write('*** for...of 예제 *** <br>');

for (let i of num) {
    document.write(i);
}

document.write("<br><br><br>");


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

document.write("<br><br><br>");


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
// *** for...in 예제 ***
// 01234

// *** for...of 예제 ***
// 12345


// *** for...in (collection) 예제 ***
// applebananagrape


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

펼침 연산자는 **배열을 펼쳐주는 역할**을 한다. 배열을 바꾸지 않고도 새로운 값을 복사하거나, 배열을 합치거나, 배열을 펼쳐진 상태로 파라미터로 전달하는 등의 활용이 가능해진다. 펼침 연산자의 장점은 기존 컬렉션을 조작하지 않는다는 점이다. 

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
// 배열을 바꾸지 않고 새로운 값을 복사할 수 있

let c = [...a, 500];
console.log(c) // [100, 200, 300, 400, 500]
// 기존의 복잡한 방법 대신 간단하게 값을 추가하여 배열을 복사할 수 있
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
document.write(max, "<br><br><br>");

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
document.write(max2, "<br><br><br>");

// -- Result --
// *** 16 배열 최댓값 구하기 ***
// 500
```
{% endcode %}




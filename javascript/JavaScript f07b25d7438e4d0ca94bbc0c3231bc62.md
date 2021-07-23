# JavaScript

## 언어의 특징

### JS의 언어적인 특징?

- 인터프리터 언어
- 프로토타입 기반 언어
- ~~다중 패러다임 지원: 명령형, 함수형 객체지향 언어~~

### 인터프리터 언어와 컴파일 언어의 차이점?

인터프리터 언어: 인터프리터에 의해 소스코드를 한 줄 씩 읽어 바로 실행됨

컴파일 언어: 컴파일러에 의해 기계어로 모두 번역 후 실행

- 인터프리터 언어는 번역과 실행이 동시에 이루어져 별도의 실행 파일이 존재하지 않는다.
컴파일 언어는 컴파일러에 의해 실행 가능한 파일(: 오브젝트 파일, 바이너리 파일)이 생성된다.

### 인터프리터 언어와 컴파일 언어의 장단점?

인터프리터 언어

- 별도의 컴파일 시간 x → 크기가 큰 소스코드를 바로 실행 가능
- 런타임 환경에서 컴파일 언어에 비해 속도가 느림

컴파일 언어

- 일단 컴파일 되면 인터프리터를 통해 실행하는 것보다 빠르게 실행됨

### 프로토타입 기반 언어란?

객체를 원형, 즉 프로토타입으로 복제의 과정을 통해 객체의 동작 방식을 다시 사용할 수 있는 언어

- 클래스 기반 언어는 객체 생성 이전에 클래스를 정의하고, 해당 클래스로 인스턴스를 생성해 상속을 구현한다.

## 엔진 & 런타임

### JavaScript 엔진의 구성은?

- call stack : 코드 실행에 따라 콜 스택이 쌓이는 곳
- memory heap : 메모리 할당이 일어나는 곳

대표적인 JavaScript 엔진으로 Chrome의 V8 엔진이 있다.

### 런타임이란?

프로그래밍 언어가 구동되는 환경.

- 자바스크립트 런타임에는 브라우저, Node.js 등이 있다.
- 자바스크립트는 싱글 스레드인 반면, 자바스크립트 런타임인 브라우저, Node.js 등은 멀티 스레드를 지원한다.

## 객체(Object)

### Object(객체)란?

키와 값으로 구성된 프로퍼티들의 집합

- JavaScript에서 원시 타입을 제외한 모든 것이 객체(함수, 배열 등)이다.
- 프로퍼티의 값으로 JavaScript에서 사용할 수 있는 모든 값을 사용할 수 있다.
- 프로퍼티의 값으로 함수(: 일급 객체)를 사용할 수 있으며, 프로퍼티 값이 함수일 경우, 일반 함수와 구분 짓기 위해 메소드라고 부른다.

### 객체를 생성하는 방법은?

- 객체는 언제나 함수(Function)로 생성된다.

1. 객체 리터럴

- 중괄호(`{ }`)로 객체를 생성하는 방법

```jsx
const person = {
	name: 'Lee',
	gender: 'female',
}
```

- 객체 리터럴은 내부적으로 Object 생성자 함수를 통해 객체를 생성하는 축약 표현이다.

2. Object 생성자 함수

- new 연산자와 Object 생성자 함수를 호출해 빈 객체를 생성하는 방법

- '생성자 함수(constructor)': `new` 키워드와 함께 객체를 생성하고 초기화하는 함수
- Object 생성자 함수는 같은 용도에 비해 객체 리터럴에 코드가 길어 잘 쓰이지 않는다.
- 게다가, 프로퍼티 값만 다른 여러 객체를 생성할 때마다 같은 프로퍼티를 일일이 추가해줘야 하므로 불편하다.

```jsx
const person = new Object()
person.name = 'Lee'
person.gender = 'female'
```

3. 생성자 함수

```jsx
function Person(name, gender) {
	this.name = name // this는 생성자 함수가 생성할 인스턴스(instance)를 가리킨다.
	this.gender = gender
}
const person1 = new Person('Lee', 'female')
const person2 = new Person('Shin', 'male')
```

- 생성자 함수 내에서 this에 바인딩되어 있는 프로퍼티와 메소드는 외부에서 참조 가능하다.
- 생성자 함수 내에서 선언된 일반 변수는 외부에서 참조 불가능하다.

## 프로토타입(Prototype)

### 클래스 기반의 객체지향 프로그래밍 언어와, 프로토타입 기반의 객체지향 프로그래밍 언어(JavaScript)의 차이점은?

- 클래스 기반의 객체지향 프로그래밍 언어는 객체 생성 이전에 클래스를 정의하고, 클래스를 통해 객체(인스턴스)를 생성한다.
- 프로토타입 기반의 객체지향 프로그래밍 언어는 클래스 없이도 객체를 생성할 수 있다.

### prototype이란?

다른 객체의 원형 객체, 또는 상위 객체

- prototype은 prototype object(객체)의 줄임말이다.

### 프로토타입을 사용하는 이유는? (활용되는 예시는?)

프로퍼티의 값만 다른 여러 객체를 생성할 때, 메모리를 절약하는 용도로 활용할 수 있다.

예를 들어 `foo`라는 프로퍼티 또는 메소드를 가지는 100개의 객체를 생성한다고 하자.
내부에 `this.foo`를 통해 프로퍼티를 생성하는 생성자 함수로 100개의 객체를 생성하면,
100개의 `foo`가 메모리에 할당돼서 저장된다.

그러나 만약 생성자 함수의 프로토타입에 `foo` 프로퍼티를 설정한다면,
1개의 `foo`를 위한 메모리만 사용하면서 100개의 객체가 모두 `foo`를 참조할 수 있게 된다.

### (노트)

JavaScript의 모든 객체는 상속을 구현하기 위해 `[[Prototype]]`이라는 internal slot을 가진다.

- `[[Prototype]]` 객체의 프로퍼티는 상속되어, 자식 객체에서 사용할 수 있다.
- `[[Prototype]]`의 값은 프로토타입 객체이며, `__proto__`로 접근할 수 있다.

- internal slot: 명세에서 요구되는 행동을 정의(구현)하기 위해 사용되는 pseudo-property/method

함수 객체(함수도 객체이므로)는 일반 객체와 다르게 `[[Prototype]]` 이외에 `prototype`이라는 프로퍼티도 가진다.

- `prototype` 프로퍼티는, 함수 객체가 생성자 함수로 사용될 때, 이 함수를 통해 생성될 객체의 프로토타입 객체를 가리킨다.

### 프로토타입이 결정되는 시기는?

객체가 생성될 때 프로토타입이 결정된다.

- 결정된 프로토타입 객체는 다른 임의의 객체로 동적으로 변경할 수 있다.

### prototype chain이란?

특정 객체의 프로퍼티나 메소드에 접근하려고 할 때,
해당 객체에 접근하려는 프로퍼티 또는 메소드가 없다면,
`[[Prototype]]`이 가리키는 링크를 따라 프로토타입 객체의 프로퍼티나 메소드를 차례대로 검색한다.

이를 프로토타입 체인이라고 한다.

### 프로토타입 객체를 확장하는 방법은?

프로토타입 객체도 (일반 객체와 마찬가지로) 프로퍼티를 추가/삭제할 수 있다.

- 추가/삭제된 프로퍼티는 즉시 프로토타입 체인에 반영된다.

```jsx
function Person(name) {
	this.name = name
}
const lee = new Person('Lee')

Person.prototype.sayHello = function() {
	console.log(`Hi! I'm ${this.name}`)
}
lee.sayHello() // Hi! I'm Lee
```

### 값을 할당할 때와, 참조할 때 프로토타입 체인이 동작하는 여부?

객체의 프로퍼티를 참조하는 경우, 그리고 해당 객체에 해당 프로퍼티가 없는 경우, 프로토타입 체인이 작동한다.

객체의 프로퍼티에 값을 할당하는 경우, 프로토타입 체인이 동작하지 않는다.
왜냐햐면, 객체에 해당 프로퍼티가 있는 경우는 값을 재할당하고, 프로퍼티가 없는 경우에는 해당 객체에 프로퍼티를 동적으로 추가하기 때문이다.

### 프로토타입 객체를 동적으로 변경하는 방법은?

생성자 함수의 `prototype`이라는 프로퍼티의 값을 변경하면 된다.

### 프로토타입 객체를 동적으로 변경하기 이전에 생성된 객체와, 이후 생성된 객체의 차이점은?

- 변경 이전 생성된 객체는, 프로토타입으로 기존의 프로토타입 객체를 가진다.
- 변경 이후 생성된 객체는, 프로토타입으로 변경 이후의 프로토타입 객체를 가진다.

```jsx
function Person(name) {
	this.name = name
}

const lee = new Person('Lee')

// 프로토타입 객체를 동적으로 변경
Person.prototype = { gender: 'male' }

const shin = new Person()

console.log(lee.name) // Lee
console.log(lee.gender) // undefined
console.log(shin.gender) // male
```

## Class

### (노트)

class의 프로퍼티

- constructor 내부에 선언되는 프로퍼티와 메소드는 객체 인스턴스의 것이 된다.
- constructor 외부에 선언되는 메서드는, 생성자 함수의 프로토타입 객체의 것이 된다.
즉 객체 인스턴스의 것이 아니라, 단일 원본을 여러 인스턴스들이 프로토타입 체인에 의해 참조하게 된다.

```jsx
class Person {
	// 생성되는 객체 인스턴스의 것이 됨.
	constructor(name, gender) {
		this.name = name
		this.gender = gender
	}

	// Person.prototype에 추가됨
	greet() {
		return `HI, I'm ${this.name}`
	}
}
```

class는 ES6에 추가된 'syntactic suger'이다.

```jsx
class Person {
    constructor(name, gender) {
        this.name = name
        this.gender = gender
    }
    sayHello() {
        return `Hi! I'm ${this.name}`
    }
}

// class로 구현된 위의 Person은 아래와 같이 정확히 똑같이 구현될 수 있다.
function Person(name, gender) {
    this.name = name
    this.gender = gender
}

Person.prototype.sayHello = function() {
    return `Hi! I'm ${this.name}`
}
```

## Closure

**(고빈도 기출)**

### Closure란?

- 함수와, 그 함수가 선언됐을 때의 (lexical) 환경과의 조합
- (특정 함수로부터) 반환된 내부 함수가, 자신이 선언됐을 때의 환경을 기억해서, 자신이 선언됐을 때의 환경 밖에서 호출되어도 그 환경에 접근할 수 있는 함수

### Closure의 동작 원리를 (실행 컨텍스트와 관련하여) 설명?

내부 함수가 유효한 상태에서 외부 함수가 종료하여 외부 함수의 실행 컨텍스트가 반환되어도, 외부 함수의 실행 컨텍스트 내 활성 객체(AO)는 유효. 내부 함수가 스코프 체인을 통해 참조할 수 있게 되는 것.

![JavaScript%20f07b25d7438e4d0ca94bbc0c3231bc62/Untitled.png](JavaScript%20f07b25d7438e4d0ca94bbc0c3231bc62/Untitled.png)

### Closure의 활용법?

1. 상태 유지: 현재 상태를 기억하고 변경된 최신 상태를 유지하는 것.

- 즉시실행함수로 내부 함수를 리턴한다. 내부 함수는 즉시실행함수의 변수를 기억하는 클로저이다.
- 내부 함수가 존재하는 한 '자유 변수'는 유지되고, 
내부 함수가 실행되면 내부 함수의 로직에 따라 자유 변수는 변경되어 최신 상태를 유지한다.

    ```jsx
    const toggle = (() => {
    	let isVisible = false

    	return () => {
    		isVisible = !isVisible
    		box.style.display = isVisible ? 'block' : 'none'
    	}
    })()

    toggleBtn.onclick = toggle
    ```

    - 자유 변수(free variable) : 클로저에 의해 참조되는 외부 함수의 변수
    - 내부 함수의 지역 변수로 상태를 관리한다면, 내부 함수를 호출할 때마다 지역 변수가 초기화되므로 변경된 최신 상태를 기억하지 못하지! 반면 IIFE는 한번만 실행되므로 변수가 초기화 될 일은 없다.

2. 정보의 은닉

- 생성자 함수를 선언. 생성자 함수 내 변수는 this로 바인딩하지 않는 한 자유변수가 됨. 생성자 내부 메소드만 접근 가능.
- this 바인딩된 프로퍼티는 외부 접근 가능한 `public` 프로퍼티가 되지만, 자유변수는 `private` 프로퍼티가 된다.

    ```jsx
    function Counter() {
    	let counter = 0 // free variable

    	this.increase = () => ++counter
    	this.decrease = () => --counter
    }
    ```

### Closure의 상태 유지가 전역 변수에 비해 갖는 이점?

전역 변수는 누구나 접근할 수 있기 때문에 많은 부작용을 유발. 오류 원인.

### 렉시컬 스코핑(lexical scoping)이란?

스코프가 함수를 호출할 때가 아니라 함수가 선언될 때 결정되는 것

### Closure의 단점?

- 메모리: 내부 함수가 참조하고 있는 한 메모리는 해제되지 않고 남아있다.
(→ 지속적으로 반복문을 돌면서 클로저를 생성하는 등, 과도하게 사용할 시 문제)
- 퍼포먼스: 변수 조회 시 클로저로 생성한 스코프를 탐색. (→ 과도하게 사용할 시 문제)

### Closure가 참고하고 있는 메모리를 해제해주려면 어떻게 할까?

클로저가 해당 스코프의 변수를 더 이상 참조하지 않도록 해주면 된다.

- 종료된 외부 함수의 실행 컨텍스트의 활성 객체는 이를 필요로 하는 내부 함수가 하나 이상 존재할 경우 계속 유지된다.

### 클로저로 인해 자주 발생하는 실수에 대해 알고 있는지?

## this

### this란?

그것이 속해있는 객체를 표현하는 값

### this의 값이 결정되는 방식을 설명?

함수 호출 방식에 의해 this에 바인딩되는 객체가 동적으로 결정.

'동적'으로 결정된다는 말은, 함수가 선언될 때 this에 바인딩되는 객체가 '정적'으로 결정되는 것이 아니라, 함수가 호출될 때 어떻게 호출되었는지에 따라 결정된다는 말이다.

함수를

- 함수로서 호출 하는지
- 메소드로서 호출 하는지
- 생성자 함수로서 호출 하는지

에 따라 달라짐.

### 함수가 '일반 함수로서' 호출될 때 this가 바인딩되는 객체는?

전역객체(global object).

- 이를 '기본 바인딩'이라 한다.

### 전역객체란?

- 모든 객체의 유일한 최상위 객체를 의미.
- 전역 변수(global object)를 프로퍼티로 소유한다.

### Browser-side와 server-side에서의 전역객체가 어떻게 다른가?

전역객체는 Browser-side에서는 `window`. Node.js 등 server-side에서는 `global` 객체를 의미한다.

### 그러면 함수가 '일반 함수로서', 함수의 내부 함수나 메소드의 내부 함수, 콜백 함수 등으로서 호출될 때는?

함수로서 호출된다면 일반 함수, 함수의 내부 함수, 메소드의 내부 함수, 콜백 함수 어디에서 선언되든 관계 없이 this는 전역 객체를 바인딩한다.

### 함수가 '일반 함수로서' 호출되었을 때 this가 전역 객체를 참조하는 것을 회피하는 방법이 있을까?

~~1. 외부 함수의 this 값을 데이터로 가지는 변수를 선언하여 내부 함수에서 this 대신 사용.~~

2. apply, call, bind를 사용해서 명시적으로 this를 바인딩.

### 함수가 '메소드로서' 호출될 때 this가 바인딩되는 객체는?

해당 메소드를 소유한 객체.

- 함수가 객체의 프로퍼티 값이면 메소드로서 호출된다.
- 이를 '암시적 바인딩'이라 한다.

### 그러면 함수가 '프로토타입 객체의 메소드로서' 호출될 때는?

일반 메소드 방식과 마찬가지로 해당 메소드를 호출한 객체에 바인딩.

### 함수가 '생성자 함수로서' 호출될 때 this가 바인딩되는 객체는?

- 생성자 함수의 코드가 실행되기 전 생성되는 빈 객체를 가리킨다.
- this를 통해 빈 객체에 동적으로 프로퍼티나 메소드가 추가될 수 있다.

- 'new 바인딩'이라고도 한다.

### 객체 리터럴 방식과 생성자 함수 방식의 차이는?

프로토타입 객체( `[[Prototype]]` )에 차이가 있다.

객체 리터럴 방식의 경우, 생성된 객체의 프로토타입 객체는 `Object.prototype`이다.
생성자 함수 방식의 경우, 예를 들어 `Person`이라는 함수명을 가진 생성자 함수라고 했을 때, 생성된 객체의 프로토타입 객체는 `Person.prototype`이다.

### 명시적으로 this를 바인딩하는 방법?

`Function.prototype` 객체의 메소드인 apply와 call, bind 메소드를 사용할 수 있다.

- `Function.prototype`은 모든 함수 객체의 프로토타입 객체이다.
- apply와 call을 통한 바인딩을 '명시적 바인딩', bind를 통한 바인딩을 '하드 바인딩'이라 한다.

### this를 사용할 때 자주 발생하는 실수에 대해 아는 것이 있는지? (this가 문제를 일으키는 상황에 대해 알고 있는 것이 있는지?)

this를 사용하는 함수를 콜백 함수로 넘겨줄 때 의도와 다르게 동작하는 경우가 있다.

- 예를 들어, setTimeout의 콜백 함수로 어떤 객체의 메소드를 전달하면, 해당 콜백 함수는 메소드로서 실행되는 것이 아니라 일반 함수로 실행된다. 따라서 this는 전역 객체를 가리키게 된다.

    ```jsx
    name = "global context!"

    function hello() {
      console.log(this.name)
    }

    var obj = {
      name: "chris",
      hello: hello,
    }

    setTimeout(obj.hello, 1000) // "global context"
    ```

### apply, call, bind 메소드의 사용법에 대해 설명?

call

- this를 바인딩할 함수의 프로퍼티로 `call()`을 호출한다.
- `call()`의 첫 번째 인자로, 바인딩할 객체를 전달한다.
- `call()`의 두 번째 인자부터는 (optional) 함수로 전달할 인자를 전달한다.

- `call()`은 this를 바인딩할 뿐 아니라 `call()`을 호출한 함수를 실행한다.
- 첫 번째 인자로 `null`을 전달하면 this는 전역 객체를 바라본다.

apply

- `call()`과 모든 것이 동일하나, `call()`은 함수에 전달할 인자로 인자 여러 개를, `apply()`는 인자 여러 개를 하나로 묶은 배열 하나를 인자로 전달한다.

    ```jsx
    const say = function (city) {
    	console.log(`Hello, ${this.name} in ${city}`);
    }

    name = 'Jin';
    const obj = { name: 'Tom' };

    say("seoul"); // Hello, Jin in seoul
    say.call(obj, "paris"); // Hello, Tom in paris
    say.apply(obj, ["new york"]); // Hello, Tom in new york
    ```

bind

- this를 바인딩할 함수의 메소드로 `bind()`를 호출하고, 인자로 바인딩할 객체를 전달한다.
- apply, call과 다르게 바인딩만 하고 해당 함수를 호출하지는 않고 반환한다.

    ```jsx
    const obj1 = {
    	name: 'shin',
    	yell: function() {
    		console.log(this.name);
    	}
    }
    const obj2 = {
    	name: 'Lee'
    }

    const yell2 = obj1.yell.bind(obj2);
    yell2(); // 'Lee'
    ```

### 유사 배열(arguments)이 배열의 메소드를 사용할 수 있도록(조작할 때) apply와 call을 사용하는 방법에 대해 아는지?

유사 배열(`arguments`)은 함수에 전달된 인수로, 배열의 형태를 띄지만 실제 배열은 아니기에 유사 배열이라 불린다.

- 유사 배열은 실제 배열이 아니기 때문에 배열의 메소드를 사용할 수 없다.
- apply나 call을 사용해 이를테면 다음과 같이 사용할 수 있다.

    ```jsx
    function example() {
    	console.log(Array.prototype.join.call(arguments));
    }

    example(1, 'string', true); // '1,string,true'
    ```

### 암시적 바인딩과 명시적 바인딩의 우선 순위는?

암시적 바인딩 < 명시적 바인딩

```jsx
function hello() {
  console.log(this.name)
}

var obj = {
  name: "shin",
  hello: hello,
}

obj.hello() // 'shin'
obj.hello.call({ name: "lee" }) // 'lee'
```

new 바인딩 > 명시적 바인딩 > 암시적 바인딩 > 기본 바인딩

### arrow function에서의 this는 어떻게 동작하나?

- 기존 함수 호출을 통한 this 바인딩은 '동적 바인딩'인 것에 반해, arrow function에서는 '정적 바인딩'이 적용된다.
- array function은 코드상 상위 블록의 컨텍스트를 this로 바인딩한다.

```jsx
function hello() {
  setTimeout(function callback() {
    console.log(this.name)
  })
}

function helloArrow() {
  setTimeout(() => {
    console.log(this.name)
  })
}

var obj = {
  name: "Lee",
  hello: hello,
}

var name = "global context!"

hello() // 'global contenxt!'
helloArrow() // 'global contenxt!'
obj.hello() // 'global contenxt!'
obj.helloArrow() // 'chris'
hello.call({ name: "chris" }) // 'global contenxt!'
helloArrow.call({ name: "alice" }) // 'alice'
```

## 비동기 처리

프론트엔드에서 "비동기"에 대한 내용이 중요한 이유
- 현대에 들어서면서, 웹은 단방향으로 정보를 보여주기만 하는 정적인 웹에서, 사용자와 상호작용을 하는 동적인 웹으로 진화
→ 연속적으로 변경되는 정보를, 실시간으로 사용자에게 보여주어야 함.
- 그런데, 사용자에게 들어오는 요청을 들어온 순서대로만 처리할 수는 없었다. 타이머를 사용한 이벤트, 서버와의 통신, 애니메이션 등 예측할 수 없는 다양한 이벤트들로 인해 사용자의 대기시간이 늘어나게 될 것이다. (: UX 저하)

프론트엔드에서 "비동기 처리"가 필요한 이유?
: 무언가를 기다리는 것을 사용자가 아닌 브라우저가 하도록 하기 위해서이다.

### 최초의 비동기 처리 - callback 패턴

## Promise

### Promise란?

비동기 작업이 미래에 맞게되는 완료 또는 실패와 그 결과값을 나타내는 객체

- Promise는 ES6에 정식 채택되어 IE를 제외한 대부분의 최신 브라우저에서 정상 작동한다.

### 동기식 작업과 비동기식 작업이란? 차이점은?

동기식(Synchronous) 처리 모델

- 태스크가 순차적으로 실행된다.
- 어떤 작업이 수행 중이면 다음 작업은 대기하게 된다.

비동기식(Asynchronous/Non-Blocking) 처리 모델

- 태스크가 병렬적으로 실행된다.
- 어떤 작업이 수행 중일 경우(종료되지 않은 상태이더라도), 대기하지 않고 바로 다음 태스크를 실행한다.

### Promise는 어떤 문제점을 해결하고자 등장했나?

- js는 비동기 처리를 위해 전통적인 콜백 패턴을 사용했었다.
- 콜백 패턴은 콜백 헬로 인해 가독성이 나쁘다.
- 비동기 처리 중 발생한 에러 처리가 곤란하다. 여러 개의 비동기 처리를 한 번에 처리하는 데 한계가 있다.

### 비동기 처리에 콜백 패턴을 사용해야 하는 이유는?

- 처리 순서를 보장하기 위함
- js의 비동기식 처리는 실행 완료를 기다리지 않고 다음 태스크를 진행한다. 비동기 함수 내에서 처리 결과를 반환하는 로직이 기대한 대로 동작하지 않는다.
- 때문에 비동기 함수의 처리 결과에 대한 처리는 콜백 함수 내에서 진행해야 한다.

자바스크립트의 대부분의 DOM 이벤트와 Timer 함수, Ajax 요청은 비동기식 처리 모델로 동작한다.

### 콜백 방식의 비동기 처리가 에러 처리에 곤란한 이유는?

예외(exception)은 호출자(caller) 방향으로 전파되기 때문에, 콜백 함수 내에서 발생된 에러를 잡을 수 없기 때문이다.

예를 들어 try 블록 내에 비동기 처리 함수(예를 들어 setTimeout)가 있고, setTimeout의 콜백 함수는 예외를 발생시킨다고 하자.

`throw` 문은 사용자 정의 예외를 던질 수 있다. 호출자 함수 사이에 catch 블록이 없으면 프로그램이 중지된다.

- 비동기 처리 함수 setTimeout은 실행 후 콜 스택에서 즉시 제거된다.
- 콜백 함수는 이벤트 발생 시 태스크 큐로 이동한 후 콜 스택이 비워졌을 때 콜 스택으로 이동해 실행된다.
- 콜 스택에 setTimeout이 존재하지 않기 때문에, setTimeout은 콜백 함수의 호출자가 아니게 된다. 호출자라면 콜 스택에 존재해야 한다.
- 예외는 호출자 방향으로 전파되지만, setTimeout이 존재하지 않아 에러는 catch 블록에 잡히지 않는다. 프로세스는 종료된다.

- `try ... catch` 문은 실행할 코드 블록을 표시하고, 예외(exception)가 발생(throw)했을 경우 응답을 지정한다.

### Promise를 생성하는 방법은?

- Promise 생성자 함수를 통해 생성한다: `Promise()`
- 인자로 비동기 작업을 수행할 콜백 함수를 전달한다.

    - 콜백 함수는 resolve와 reject 함수를 인자로 전달 받는다.
    - 콜백 함수는 프로미스 내부 구현에 의해 즉시 실행된다. Promise 생성자 함수가 생성한 객체를 반환하기도 이전에 호출된다.

### Promise의 상태(state)는 어떤 것들이 있나?

pending, fulfilled, rejected, settled

- pending : 비동기 처리가 아직 수행되지 않은 상태. 즉 resolve나 reject 함수가 아직 호출되지 않은 상태
- fulfilled : 비동기 처리가 수행되었고 성공한 상태. 즉 resolve가 호출된 상태
- rejected : 비동기 처리가 수행되었고 실패한 상태. 즉 reject가 호출된 상태
- settled : 비동기 처리가 수행되었고 성공 또는 실패한 상태. 즉 resolve 또는 reject가 호출된 상태

### Promise의 후속 처리 메소드에 대해 설명?

- then과 catch, finally가 있다.
- Promise 객체의 결과 상태에 따라 후속 처리 메소드를 체이닝 방식으로 호출한다.

then은

- 두 개의 콜백 함수를 인자로 받는다. 첫 번째는 성공 시(fulfilled) 호출되고, 두 번째는 실패 시(rejected) 호출된다.

catch는

- 예외가 발생하면 호출된다.

finally는

- 성공, 혹은 실패 시 호출된다.

finally 메소드에는 인수가 없다. 즉 Promise가 이행되었는지, 거부되었는지 알 수 없다.

then과 catch, finally 메소드는 Promise를 반환한다.

### Promise의 에러 처리는 then과 catch 중 어떤 것으로 하는 것이 더 좋을까?

catch로 하는 것이 좋다.

then은

- 두 번째 콜백 함수로 비동기 작업 간에 발생하는 에러를 처리할 수 있다.
- 단, 첫 번째 콜백 함수에서 발생한 에러를 캐치하지 못한다.
- 코드가 복잡해져서 가독성이 좋지 않다.

catch는

- 모든 then 메소드를 호출한 이후 호출하면, 비동기 작업 간 발생한 에러 뿐만 아니라 then 메소드 내부에서 발생한 에러까지 모두 캐치할 수 있다.
- then에 비해 가독성이 좋고 명확하다.

catch 메소드는 내부적으로 `then(undefined, onRejected)`를 호출한다(완전 동일하다).

### Promise의 정적 메소드에 대해 설명?

Promise.resolve, Promise.reject, Promise.all, Promise.race가 있다.

Promise는 생성자 함수이지만, 함수도 객체이므로 메소드를 가질 수 있다.

### Promise.resolve와 Promise.reject에 대해 설명?

존재하는 값을 Promise로 매핑하기 위해 사용된다.

- Promise.resolve는 인자로 전달된 값을 resolve하는 Promise를 생성한다.
- Promise.reject는 인자로 전달된 값을 reject하는 Promise를 생성한다.

### Promise.all과 Promise.race에 대해 설명?

Promise.all

- Promise가 담겨 있는 배열 등을 인자로 받아, 내부 Promise를 병렬로 처리하고 그 처리 결과를 resolve하는 Promise를 반환한다.

    - 처리 순서가 보장된다. 즉, 배열의 첫 번째 Promise가 resolve한 처리 결과부터 차례대로 배열에 담아 그 배열을 resolve하는 Promise를 반환한다.
    - 프로미스의 처리가 하나라도 실패하면 가장 먼저 실패한 Promise가 reject한 에러를 reject하는 새로운 Promise를 즉시 반환한다.
    - 전달 받은 배열의 요소가 Promise가 아닐 경우, Promise.resolve 메소드를 통해 Promise로 매핑된다.

Promise.race

- Promise.all과 동일하게 Promise가 담겨 있는 배열 등을 인자로 받는다.
- 다만 배열의 모든 Promise를 병렬 처리하는 것이 아니라, 가장 먼저 처리된 Promise가 resolve한 처리 결과를 resolve하는 새로운 Promise를 반환한다.

## 이벤트 루프

### 이벤트 루프란?

자바스크립트의 싱글 스레드 엔진과 멀티 스레드 환경을 연동시켜주는 장치.

### 이벤트 루프가 필요한 이유는?

- 자바스크립트는 싱글 스레드 기반의 언어이다. → 한번에 하나의 작업만 처리할 수 있다.
- (브라우저 환경을 예시로 들면) 마우스 이벤트 발생, HTTP 요청, 애니메이션 등의 작업이 동시에 이뤄진다.
- 자바스크립트가 이러한 동시성을 지원할 수 있도록 이벤트 루프가 도와준다.

(즉, 싱글 스레드 기반 언어인 자바스크립트가 동시성을 지원할 수 있도록 도와주는 것은 브라우저, Node.js 등 외부의 환경이다.)

### Run-to-Completion이란?

자바스크립트에서 하나의 함수가 실행되면, 그 함수의 실행이 끝날 때까지 다른 어떤 작업도 중간에 끼어들지 못하는 특성.

### 자바스크립트가 Run-to-Completion으로 동작하는 이유(원리)는?

- 자바스크립트 엔진은 단일 콜 스택 구조로 이루어져 있다.
- 함수가 호출되면 스택에 해당 함수의 코드 블록이 쌓이고, 실행이 완료되면 코드 블록이 스택에서 제거된다.
- 하나의 함수가 콜 스택에 쌓이면, 콜 스택이 비워질 때까지 다른 함수의 코드 블록이 스택에 추가되지 않는다.

### 태스크 큐가 동작하는 과정은?

예를 들어 다음과 같은 상황이라고 하자.

```jsx
const A = () => {
	console.log('A');
}

const B = () => {
	for (let i = 0; i < 100000;i++);
	console.log('B');
}

setTimeout(A, 1000);
B();
// 'B'
// 'A'
```

- `setTimeout()` 함수가 콜 스택에 진입한다.
- `setTimeout()`은 즉시 콜 스택에서 제거되고, 백그라운드에서 1초를 센다.
- `B()`가 콜 스택에 진입한다. 반복문을 실행한다.
- 1초가 지나고, 백그라운드에서 콜백 함수 `A()`를 태스크 큐로 보낸다.
- `A()`가 실행할 준비를 마쳤어도, `B()`의 반복문이 끝나 콜 스택에서 제거되지 않으면 run-to-completion 특성으로 인해 `A()`는 실행되지 않는다.
- `B()`의 반복문이 끝나 콜 스택에서 제거되고 나서야, 이벤트 루프는 태스크 큐의 `A()`를 콜 스택에 추가한다.

- 대부분의 비동기 코드들(ex: Ajax, setTimeout, Promise 등)은 모두 Web API에서 처리된다.
- Web API에 요청했던 작업이 끝나면 콜백으로 전달한 함수가 큐에 등록된다.
- 이벤트 루프는 콜 스택이 비워져 있을 경우, 큐의 작업들을 콜 스택에 추가한다.

- Web API는 브라우저에서 제공하는 API이다.

### 태스크 큐와 마이크로 태스크 큐가 동작하는 과정은?

예를 들어 다음과 같은 상황이라고 하자.

```jsx
setTimeout(() => { console.log('A'); }, 1000);

Promise.resolve()
	.then(() => { console.log('B'); })
	.then(() => { console.log('C'); });
// B
// C
// A
```

- Promise는 마이크로 태스크(micro task)이다.
- 마이크로 태스크는 일반 태스크보다 높은 우선 순위를 가진다. 따라서 이벤트 루프는 콜 스택이 비어 큐의 작업을 추가할 때, 마이크로 태스크 큐를 먼저 확인한 후 태스크 큐를 확인한다.

- Animation Frames라는 큐도 있다. 브라우저 렌더링과 관련된 API가 해당된다.
- 우선 순위: 마이크로 태스크 > Animation Frame > 태스크

### 이벤트 루프(혹은 태스크 큐의 우선 순위)로 인해 사용자 경험에 해가 되는 경우가 있을까?

태스크는 이벤트 루프를 통해 순차적으로 실행되기 때문에, 고비용 연산을 포함한 태스크나 마이크로 태스크가 있다면 이로 인해 다른 작업들 - 그 중에서도 사용자 경험과 직결된 이벤트(클릭, 텍스트 입력, 렌더링 등)가 가로막힐 수 있다.

### 고비용 연산으로 인한 블로킹에 대응하는 방법은?

1. 고비용 연산을 수행하는 태스크를 적절히 쪼개 실행할 수 있다.

```jsx
let i = 0;

const count = () => {
	while (i % 100 !== 0) i++;
	
	if (i === 10000) console.log('work completed');
	else setTimeout(count);
}

count();
```

- 쪼개진 고비용 연산이 콜 스택에서 수행되는 동안 이벤트가 발생하면, 태스크 큐에서 대기한다.
- 쪼개진 연산이 끝나 콜 스택에서 제거되면, 다음 연산이 수행되기 전에 태스크 큐의 작업이 먼저 콜 스택에 추가되어 작업이 진행된다.

2. 자바스크립트의 웹 워커(Web Worker)를 사용해 멀티 스레딩을 할 수 있다.

- 웹 워커: 스크립트 연산을 별도의 백그라운드 스레드에서 실행할 수 있는 Web API.

    사용 방법

    - 메인 스레드에서 워커 객체를 생성한다. (파라미터로는 워커가 수행할 스크립트 파일 명을 전달한다.)
    `const myWorker = new Worker("work.js");`
    - 메인 스레드에서 메시지에 기반해 워커와 통신한다.

        `postMessage()`로 작업의 실행을 요청한다. 워커는 결과를 반환한다.

    한계

    - 메시지 기반으로만 통신이 가능하므로, 메인 스레드의 context에 접근할 수 없다.
    때문에, DOM 객체를 직접 조작할 수 없다.

### (progress bar에서의 활용)

```html
<div id="progress"></div>
<script>
	const count = () => {
		for (let i = 0; i < 10000; i++) {
			i++;
			progress.innerHTML = i;
		}
	}

	count();
</script>
```

- `i`가 `9999`가 되고 나서야 브라우저는 `<div>`에 `9999`를 출력한다. 이전의 `i`는 출력되지 않는다.
- 브라우저가 스크립트를 실행할 때는 렌더링 작업을 멈추기 때문이다.
- 이 역시 `setTimeout()`으로 스케줄링을 하면 `i`가 변하는 모습을 실시간으로 볼 수 있다.

## 실행 컨텍스트

### 실행 컨텍스트란?

실행 가능한 코드가 실행되기 위해 필요한 환경.

- "실행 가능한 코드를 형상화하고 구분하는 추상적인 개념" (by ECMAScript spec)

### 실행 가능한 코드란?

- 전역 코드: 전역 영역에 존재하는 코드
- 함수 코드: 함수 내에 존재하는 코드
- eval 코드: `eval` 함수로 실행되는 코드

### 실행에 필요한 환경이란?

변수, 함수 선언, 스코프, this 등

이와 같이 실행에 필요한 정보들을 형상화하고 구분하기 위해 자바스크립트 엔진은 실행 컨텍스트를 물리적 객체의 형태로 관리한다.

### 코드가 실행되고, 함수가 실행되고 끝나는 과정을 실행 컨텍스트 스택으로 설명해본다면?

- 실행 컨텍스트 스택은 Last-In-First-Out의 스택 구조를 띈다.
- 전역 코드(global code)에 진입하면, 전역 EC가 생성되고, EC 스택에 쌓인다.

    EC 스택은 어플리케이션이 종료될 때까지 유지된다.

- 함수를 호출하면, 해당 함수의 EC가 생성되며, 직전에 실행된 코드 블록의 EC 위에 쌓인다. 컨트롤이 새로 생성된 EC에게 이동한다.
- 함수 실행이 끝나면,해당 EC를 파기하고 직전의 EC에 컨트롤을 반환한다.

### 실행 컨텍스트의 (물리적인) 구조는?

1. Variable Object(변수 객체)

2. Scope Chain

3. this

### Variable Object란?

실행에 필요한 여러 정보들을 담은 객체.

- 변수
- 함수 선언
- parameter(매개변수)와 arguments(인수) 정보 (: 함수 컨텍스트인 경우에만)

- VO는 코드가 실행될 때 엔진에 의해 참조되며, 코드에서는 접근할 수 없다.

- 매개변수(parameters): 함수의 입력 변수 명
- 인수(arguments): 함수의 입력 값

### 전역 컨텍스트와 함수 컨텍스트에서 VO가 가리키는 객체(내용)의 차이는?

전역 컨텍스트 (← 전역 코드 실행 시 생성됨)

- 전역 객체(Global Object / GO)를 가리킨다.

    전역 변수는 다음을 프로퍼티로 가진다.

    - 전역에 선언된 전역 변수
    - 전역에 선언된 전역 함수

함수 컨텍스트 (← 함수를 실행할 때 생성됨)

- 활성 객체(Activation Object / AO)를 가리킨다.

    활성 객체는 다음 프로퍼티를 가진다.

    - 함수 코드에 선언된 지역 변수
    - 함수 코드에 선언된 내부 함수
    - parameter, arguments 정보를 담고 있는 arguments object

### 스코프 체인이란?

자신(EC)과, 자신의 상위 컨텍스트의 스코프(의 레퍼런스)를 차례대로 담고 있는 리스트

### 특정 EC의 스코프 체인에는 어떤 스코프가 담겨있나?

![JavaScript%20f07b25d7438e4d0ca94bbc0c3231bc62/Untitled%201.png](JavaScript%20f07b25d7438e4d0ca94bbc0c3231bc62/Untitled%201.png)

- 가장 먼저 현재 EC의 AO(활성 객체)
- 순차적으로 자신의 상위 EC의 AO를 가리키며
- 마지막은 전역 객체(GO)를 가리킨다.

- 스코프 체인의 값은 (함수의 실행이 아닌) 함수의 선언 시점에 결정된다.
- 상위 EC라 함은, 현재 실행되고 있는 함수가 선언된 EC를 말한다.
- 즉, 스코프 체인은 현재 EC의 AO, 그리고 상위 EC의 AO, ..., 마지막으로 GO를 가리키게 된다.

### 변수를 검색하는 과정을 스코프 체인과 연관하여 설명해본다면?

- 코드에서 변수를 참조하면, 엔진은 현재 EC의 스코프 체인의 첫번째 요소가 가리키는 AO에 접근해 변수를 검색한다.
- 검색에 실패하면, 리스트의 다음 요소가 가리키는 AO를 검색해 GO까지 내려간다.
- 만약 검색에 실패하면, 정의되지 않은 변수에 접근하는 것으로 판단하여 Reference 에러를 발생시킨다.

- 스코프 체인은 함수의 감춰진 프로퍼티 `[[Scope]]`로 참조된다.
- `console.dir()`로 함수를 찍어보면 볼 수 있다.

- `console.log()`는 HTML 구조로 파라미터를 출력한다. (→ 인수의 내부 HTML 구조 등을 확인할 수 있다.) `console.dir()`는 JSON 구조로 파라미터를 출력한다. (→ 인수의 내부 메소드 등을 확인할 수 있다.)

### 실행 컨텍스트에 값이 채워지는 순서는? (실행 컨텍스트가 생성되는 순서는?)

1. 스코프 체인이 생성되고, 초기화

2. 변수 객체화(variable instantiation) 실행

3. this value 결정

### 변수 객체화가 진행되는 과정은?

1. (함수 컨텍스트인 경우) 매개변수가 (VO의) 프로퍼티로, 인수가 값으로 설정된다.

2. 대상 컨텍스트(코드) 내의 함수 선언을 대상으로, 함수명이 (VO의) 프로퍼티로, 생성된 함수 객체가 값으로 설정된다. (→ 함수 호이스팅)

3. 대상 컨텍스트(코드) 내의 변수 선언을 대상으로, 변수명이 (VO의) 프로퍼티로, `undefined`가 값으로 설정된다. (→ 변수 호이스팅)

### 클로저를 실행 컨택스트에 기반해 설명해본다면?

- EC는 [스코프 체인 생성 및 초기화] → [변수 객체화] → [this 값 할당]의 순서로 진행된다.
- [변수 객체화] 단계에서, 가장 먼저 코드 내의 함수 선언을 대상으로, 함수명이 프로퍼티로, 생성된 함수 객체가 값으로 설정된다.
- 이때, 생성된 함수 객체는 `[[Scopes]]`라는 프로퍼티를 가진다.
    - `[[Scopes]]`는 함수 객체가 실행되는 환경을 가리킨다.
    - 즉, 현재 EC의 스코프 체인이 참조하고 있는 객체를 값으로 설정한다.
- ⇒ 내부 함수의 `[[Scopes]]`는 자신의 실행 환경과, 자신을 포함하는 외부 함수의 실행 환경, 그리고 전역 객체를 가리킨다.
    - 이때, 자신을 포함하는 외부 함수의 EC가 소멸해도 `[[Scopes]]`의 프로퍼티가 가리키는 외부 함수의 실행 환경은 소멸하지 않고 참조할 수 있다. 이것이 클로저이다.

### 함수 호이스팅이란?

코드가 실행되기 이전에, 현재 EC의 스코프 체인이 가리키는 VO에 함수가 이미 등록되어 있기 때문에, 함수 선언식 코드에 닿기 이전에 함수를 호출할 수 있는 현상.

- 함수 선언식은 VO에 함수명을 프로퍼티로, 함수 객체를 (즉시) 값으로 할당한다.
반면, 함수 표현식은 일반 변수의 방식을 따른다. 따라서 함수 표현식 코드에 닿기 이전에 함수를 호출할 수 없다.

### 변수 호이스팅이란?

- 변수 선언은 변수 객체화 단계에서 변수명이 프로퍼티로, `undefined`가 값으로 설정된다.(var로 선언된 변수의 경우에 그렇다.)
- 때문에 변수 선언 코드에 닿기 전에, 해당 변수를 참조할 수 있다. (`undefined`로) 이를 변수 호이스팅이라고 한다.

- 실제 값이 설정되는 것은 변수 선언 코드가 실행되는 시점이다.
- let과 const는 변수 객체화 단계에서 변수명이 프로퍼티로 설정되나, 값은 초기화되지 않는다. 때문에 변수 선언 드 이전에 변수를 참조하면 `uninitialized` 에러가 발생한다.

## 모듈 시스템

### AMD와 CommonJS에 대해 설명?

## EcmaScript

### EcmaScript란?

Ecma 인터내셔널이 스크립트 언어에 대해 규정해놓은 표준 중에 하나의 사양이다.
(ECMA → ECMA-262 → ECMAScript)

- ECMA 인터내셔널은 정보 통신에 대한 표준을 제정하는 기구이다.
- ES6는 ECMA-262 표준의 제 6판을 지칭하는 말이다.

### ECMAScript와 JavaScript의 관계는? 차이점은?

JavaScript는 ECMAScript 사양을 준수하는 스크립트 언어이다.

### ES6에서 추가된 문법에 대해 아는 것이 있는지?

- let & const
- Class
- arrow function
- Promise
- 비구조화 할당
- ``template literal``

- ES2015는 ES6의 동의어다.

## scope

## 기타

### use strict란?

파일 전체 또는 함수를 엄격한 운용 컨텍스트 안에서 실행할 수 있도록 한다.

- 오류는 아니지만 의도치 않은 함정이 될 수 있는 코드에 대해 오류를 발생시킨다.
- JavaScript 엔진의 최적화를 방해하는 코드에 오류를 발생시킨다.

예를 들어,

- 우발적인 전역 변수 선언을 방지한다.
`x = 3.14;`
(엄격 모드가 아니라면, 선언되지 않은 변수에 값을 할당하면 해당 이름의 전역 변수가 생성된다.)

### JavaScript의 가비지 콜렉터에 대해?

JavaScript 엔진은 가비지 콜렉터라는 소프트웨어를 가지고 있다. 가비지 콜렉터는 메모리 할당을 추적하고, 할당된 메모리가 더 이상 필요 없어졌을 때 해제하는 작업을 한다.
# WEEK9

[https://www.notion.so/WEEK9-91b01a0960cf4c9185f97219f33cf463?pvs=4](https://www.notion.so/WEEK9-91b01a0960cf4c9185f97219f33cf463)

https://www.gdschongik.com/web-study/subject/9

https://poiemaweb.com/

# 브라우저 동작 원리

대부분의 프로그래밍 언어는 운영체제(Operating System, OS) 위에서 실행되지만 웹 애플리케이션의 **자바스크립트는 브라우저에서 HTML, CSS와 함께 실행**된다

→ 브라우저 환경을 고려할 때 보다 효율적인 자바스크립트 프로그래밍이 가능하다.

- 브라우저의 핵심 기능은 사용자가 참조하고자 하는 웹페이지를 **서버에 요청(Request)**하고 **서버의 응답(Response)**을 받아 **브라우저에 표시**하는 것이다.
    
    → 브라우저는 서버로부터 HTML, CSS, Javascript, 이미지 파일 등을 응답받는다.
    

- 브라우저는 **동기(Synchronous)**적으로 **HTML, CSS, Javascript**을 처리한다.
    
    → script 태그의 위치에 따라 블로킹이 발생하여 DOM의 생성이 지연될 수 있다는 것을 의미한다.
    

- body 요소의 가장 아래에 자바스크립트를 위치시키는 것은 좋은 아이디어이다
    
    → HTML 요소들이 스크립트 로딩 지연으로 인해 렌더링에 지장 받는 일이 발생하지 않아 페이지 로딩 시간이 단축된다.
    
    → DOM이 완성되지 않은 상태에서 자바스크립트가 DOM을 조작한다면 에러가 발생한다.
    

# 객체

: **자바스크립트의 객체는 키(key)과 값(value)으로 구성된 프로퍼티(Property)들의 집합이다**

→ 프로퍼티의 값으로 자바스크립트에서 사용할 수 있는 모든 값을 사용할 수 있다.

프로퍼티 값이 함수일 경우, 일반 함수와 구분하기 위해 메소드라 부른다.(메소드는 객체에 제한되어 있는 함수를 의미한다.)

객체는 데이터를 의미하는 프로퍼티(property)와 데이터를 참조하고 조작할 수 있는 동작(behavior)을 의미하는 메소드(method)로 구성된 집합이다. 

자바스크립트의 객체는 객체지향의 상속을 구현하기 위해 “프로토타입(prototype)”이라고 불리는 객체의 프로퍼티와 메소드를 상속받을 수 있다.  여기서 프로토타입은 타 언어와 구별되는 중요한 개념

## ****프로퍼티****

**→ 프로퍼티 키(이름) + 프로퍼티 값**

→ 배열과는 달리 객체는 프로퍼티를 열거할 때 순서를 보장하지 않는다.

→ 프로퍼티 키는 프로퍼티를 식별하기 위한 식별자(identifier)

- **프로퍼티 키 :** 빈 문자열을 포함하는 모든 문자열 또는 symbol 값
- **프로퍼티 값 :** 모든 값

## ****객체 생성 방법 (객체 리터럴 + Object 생성자 함수 + 생성자 함수)**

→ 자바스크립트는 프로토타입 기반 객체 지향 언어로서 클래스라는 개념이 없고 별도의 객체 생성 방법이 존재한다.

→ 클래스 기반 객체 지향 언어는 클래스를 사전에 정의하고 필요한 시점에 new 연산자를 사용하여 인스턴스를 생성하는 방식으로 객체를 생성

### 객체 리터럴

**: 가장 일반적인 자바 스크립트의 객체 생성 방식**

→ 중괄호({})를 사용하여 객체를 생성

- {} 내에 1개 이상의 프로퍼티를 기술하면 해당 프로퍼티가 추가된 객체를 생성
- {} 내에 아무것도 기술하지 않으면 빈 객체가 생성

→ 객체 리터럴 방식으로 생성된 객체는 결국 빌트인(Built-in) 함수인 Object 생성자 함수로 객체를 생성하는 것을 단순화시킨 축약 표현(short-hand)이다.

### ****Object 생성자 함수****

**: new 연산자와 [Object 생성자 함수](https://poiemaweb.com/js-built-in-object#11-object)를 호출하여 빈 객체를 생성한다**

→ 빈 객체 생성 이후 **프로퍼티 또는 메소드를 추가하여 객체를 완성하는 방법**이다.

### ****생성자 함수****

→ 프로퍼티가 **동일한 객체 여러 개를 간편하게 생성**할 수 있다.

**특징**

- 생성자 함수 이름은 일반적으로 **대문자로 시작**
- 프로퍼티 또는 메소드명 앞에 기술한 `this`는 생성자 함수가 생성할 **인스턴스(instance)**를 가리킨다.
- this에 연결(바인딩)되어 있는 프로퍼티와 메소드는 `public`(외부에서 참조 가능)하다.
- 생성자 함수 내에서 선언된 일반 변수는 `private`(외부에서 참조 불가능)하다. 즉, 생성자 함수 내부에서는 자유롭게 접근이 가능하나 외부에서 접근할 수 없다.

## ****객체 프로퍼티 접근****

### ****프로퍼티 키****

: 일반적으로 **문자열(빈 문자열 포함)**을 지정

→ 프로퍼티 키에 문자열이나 symbol 값 이외의 값을 지정하면 암묵적으로 타입이 변환되어 문자열이 된다.

→ **프로퍼티 키는 문자열이므로 따옴표(‘’ 또는 ““)를 사용한다.**

- 자바스크립트에서 사용 가능한 유효한 이름인 경우, 따옴표를 생략할 수 있다.

### ****프로퍼티 값 읽기****

**: `마침표(.) 표기법`과 `대괄호([]) 표기법`이 존재**

→ 프로퍼티 키가 유효한 자바스크립트 이름이고 예약어가 아닌 경우 프로퍼티 값은 마침표 표기법, 대괄호 표기법 모두 사용할 수 있다.

→ 프로퍼티 이름이 유효한 자바스크립트 이름이 아니거나 예약어인 경우 프로퍼티 값은 **대괄호 표기법으**로 읽어야 한다. 

- 대괄호([]) 표기법을 사용하는 경우, **대괄호 내에 들어가는 프로퍼티 이름은 반드시 문자열이어야 한다.**

→ **객체에 존재하지 않는 프로퍼티를 참조**하면 `undefined`를 반환한다.

### ****프로퍼티 값 갱신****

→ **객체가 소유하고 있는 프로퍼티**에 **새로운 값을 할당하면 프로퍼티 값은 갱신**된다.

### ****프로퍼티 동적 생성****

**객체가 소유하고 있지 않은 프로퍼티 키**에 값을 할당하면 하면 **주어진 키와 값으로 프로퍼티를 생성**하여 **객체에 추가**한다.

### ****프로퍼티 삭제****

: `**delete` 연산자를 사용**. (이때 피연산자는 프로퍼티 키이어야 한다.)

### ****for-in 문****

**: 객체의 문자열 키(key)를 순회하기 위한 문법**

→ **배열에는 사용하지 않는 것**이 좋다

**이유**

1. 객체의 경우, 프로퍼티의 순서가 보장되지 않는다. 그 이유는 원래 객체의 프로퍼티에는 순서가 없기 때문이다. 배열은 순서를 보장하는 데이터 구조이지만 객체와 마찬가지로 순서를 보장하지 않는다.
2. 배열 요소들만을 순회하지 않는다.

→ for-in 문의 단점을 극복하기 위해 ES6에서 **[for-of 문](https://poiemaweb.com/es6-iteration-for-of)**이 추가되었다.

- f**or–in 문은 객체의 프로퍼티를 순회**하기 위해 사용하고 **for–of 문은 배열의 요소를 순회**하기 위해 사용한다.

## ****객체의 분류****

![object.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6955a47f-d771-4b90-b7ff-918748d892a8/object.png)

### [Built-in Object(내장 객체)](https://poiemaweb.com/js-built-in-object)

- [Standard Built-in Objects (or Global Objects)](https://poiemaweb.com/js-built-in-object)
- [BOM (Browser Object Model)](http://www.w3schools.com/js/js_window.asp)
- [DOM (Document Object Model)](https://poiemaweb.com/js-dom)

### Host Object(사용자 정의 객체)

: 사용자가 생성한 객체

# 함수

## **함수 정의**

→ 함수를 정의하는 방식은 3가지가 있다.

- **함수 선언문**
- **함수 표현식**
- **Function 생성자 함수**

### ****함수 선언문****

함수 선언문(Function declaration) 방식으로 정의한 함수는 `function` 키워드와 **함수명, 매개변수 목록, 함수 몸체**로 구성된다.

→ **함수 선언, 초기화, 할당이 한번에 이루어진다.** 

→ 함수 선언의 위치와는 상관없이 소스 내 어느 곳에서든지 호출이 가능하다.

- **함수명**
    
    → 함수 선언문의 경우, 함수명은 생략할 수 없다. 함수명은 함수 몸체에서 자신을 재귀적(recursive) 호출하거나 자바스크립트 디버거가 해당 함수를 구분할 수 있는 식별자이다.
    
- **매개변수 목록**
    
    → 0개 이상의 목록으로 괄호로 감싸고 콤마로 분리한다. 다른 언어와의 차이점은 매개변수의 타입을 기술하지 않는다는 것이다. 이 때문에 함수 몸체 내에서 매개변수의 타입 체크가 필요할 수 있다.
    
- **함수 몸체**
    
    → 함수가 호출되었을 때 실행되는 문들의 집합이다. 중괄호({ })로 문들을 감싸고 `return` 문으로 결과값을 반환할 수 있다. 이를 반환값(return value)라 한다.
    

### **함수 표현식**

**:함수의 일급객체 특성을 이용하여 함수 리터럴 방식으로 함수를 정의하고 변수에 할당한 것**

→ 함수명을 **생략**할 수 있다 (**익명 함수(anonymous function)**이라 한다)

→ 함수는 일급객체이기 때문에 **변수에 할당**할 수 있는데 이 변수는 함수명이 아니라 할당된 함수를 가리키는 참조값을 저장하게 된다. 

- 함수 호출시 함수명이 아니라 함수를 가리키는 변수명을 사용하여야 한다.

**함수의 일급 객체 특징**

1. **무명의 리터럴**로 표현이 가능하다.
2. **변수나 자료 구조(객체, 배열…)에 저장**할 수 있다.
3. **함수의 파라미터로 전달**할 수 있다.
4. **반환값(return value)으로 사용**할 수 있다.

### ****Function 생성자 함수****

→ 내장 함수 Function 생성자 함수로 함수를 생성하는 것을 단순화시킨 short-hand(축약법) 

⇒ 함수 선언문과 함수 표현식

→ Function 생성자 함수는 **Function.prototype.constructor 프로퍼티**로 접근할 수 있다.

### ****함수 호이스팅****

**: 함수 선언문을 함수 선언의 위치와는 상관없이 코드 내 어느 곳에서든지 호출이 하는 것**

→ 자바스크립트는 ES6의 let, const를 포함하여 모든 선언(var, let, const, function, function*, class)을 호이스팅(Hoisting)한다.

→ 변수 호이스팅은 **변수 생성 및 초기화와 할당이 분리되어 진행**된다. **호이스팅된 변수는 undefined로 초기화** 되고 **실제값의 할당은 할당문**에서 이루어진다.

### ****반환값****

- `return` 키워드는 함수를 호출한 코드(caller)에게 값을 반환할 때 사용한다.
- 함수는 배열 등을 이용하여 한 번에 여러 개의 값을 리턴할 수 있다.
- 함수는 반환을 생략할 수 있다. 이때 함수는 암묵적으로 undefined를 반환한다.
- 자바스크립트 해석기는 `return` 키워드를 만나면 함수의 실행을 중단한 후, 함수를 호출한 코드로 되돌아간다. 만일 `return` 키워드 이후에 다른 구문이 존재하면 그 구문은 실행되지 않는다.

### ****prototype 프로퍼티****

**: 함수 객체만이 소유하는 프로퍼티**

→ 함수가 객체를 생성하는 **생성자 함수로 사용될 때**, 생성자 함수가 생성한 **인스턴스의 프로토타입 객체를 가리킨다.**

## ****함수의 다양한 형태****

### ****즉시 실행 함수****

**: 함수의 정의와 동시에 실행되는 함수**

→ 최초 한번만 호출되며 다시 호출할 수는 없다

→ 최초 한번만 실행이 필요한 초기화 처리 등에 사용할 수 있다.

### ****내부 함수****

**: 함수 내부에 정의된 함수**

→ 내부함수 child는 자신을 포함하고 있는 **부모함수 parent의 변수에 접근**할 수 있다. 부모함수는 자식함수(내부함수)의 변수에 접근할 수 없다.

### ****콜백 함수****

**: 함수를 명시적으로 호출하는 방식이 아니라 특정 이벤트가 발생했을 때 시스템에 의해 호출되는 함수를 말한다.**

→ 콜백 함수는 매개변수를 통해 전달되고 전달받은 함수의 내부에서 **어느 특정시점**에 실행된다.

# 배열

## 배열의생성

### ****배열 리터럴****

→ 배열 리터럴은 객체 리터럴과 달리 **프로퍼티명이 없고 각 요소의 값만이 존재**한다

![object_array_prototype.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8fa0a45a-d025-4a4d-88fe-3c3714c7988b/object_array_prototype.png)

→ 배열 리터럴 `arr`의 프로토타입 객체는 `Array.prototype`

→ 객체 리터럴 `obj`의 프로토타입 객체는 `Object.prototype`

### ****Array() 생성자 함수****

: **내장 함수 Array() 생성자 함수로 배열을 생성하는 것**

→ Array() 생성자 함수는 Array.prototype.constructor 프로퍼티로 접근할 수 있다.

→ Array() 생성자 함수는 매개변수의 갯수에 따라 다르게 동작한다.

- **매개변수가 1개이고 숫자인 경우** 매개변수로 전달된 숫자를 length 값으로 가지는 빈 배열을 생성한다.
- **그 외의 경우** 매개변수로 전달된 값들을 요소로 가지는 배열을 생성한다

## ****배열 요소의 추가와 삭제****

### ****배열 요소의 추가****

**순서에 맞게 값을 할당할 필요는 없고 인덱스를 사용하여 필요한 위치에 값을 할당하면 동적으로 요소를 추가할 수 있다.**

→ 값이 할당되지 않은 인덱스 위치의 요소는 생성되지 않는다

### ****배열 요소의 삭제****

:`delete` 연산자를 사용

배열을 객체이기 때문

→ 요소를 완전히 삭제하여 length에도 반영되게 하기 위해서는 [Array.prototype.splice](https://poiemaweb.com/js-array#510-arrayprototypesplicestart-number-deletecountthislength-start-items-t-t-%EF%B8%8F-es3) 메소드를 사용한다.

## ****Array Property****

### ****Array.length****

- length 프로퍼티의 값은 양의 정수이며 232 - 1(4,294,967,296 - 1) 미만이다.
- length 프로퍼티의 값은 가장 큰 인덱스에 1을 더한 것과 같다.
    
    → length 프로퍼티의 값은 가장 큰 인덱스에 1을 더한 것과 같다.
    
- 배열 요소의 개수와 length 프로퍼티의 값이 반드시 일치하지는 않는다
- 현재 length 프로퍼티 값보다 더 큰 인덱스로 요소를 추가하면 새로운 요소를 추가할 수 있도록 자동으로 length 프로퍼티의 값이 늘어난다.
- length 프로퍼티의 값은 명시적으로 변경할 수 있다
    
    → length 프로퍼티의 값을 현재보다 작게 변경하면 변경된 length 프로퍼티의 값보다 크거나 같은 인덱스에 해당하는 요소는 모두 삭제된다.
    

# ****DOM (Document Object Model)****

![client-server.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/fec638e6-8ad1-4688-a725-ab059045ed1c/client-server.png)

**: 모든 요소와 요소의 어트리뷰트, 텍스트를 각각의 객체로 만들고 이들 객체를 부자 관계를 표현할 수 있는 트리 구조로 구성한 것**

→ 브라우저는 웹 문서(HTML, XML, SVG)를 로드한 후, 파싱하여 DOM(문서 객체 모델: Document Object Model)을 생성한다.

→ DOM은 자바스크립트를 통해 동적으로 변경할 수 있으며 변경된 DOM은 렌더링에 반영된다.

- 정적인 웹페이지에 접근하여 동적으로 웹페이지를 변경하기 위한 유일한 방법은 **메모리 상에 존재하는 DOM을 변경하는 것**이고, 이때 필요한 것이 **DOM에 접근하고 변경하는 프로퍼티와 메소드의 집합인 DOM API**이다.

## ****DOM tree****

![dom-tree.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/cbcf564c-8fc1-4507-8c31-c48538ab1052/dom-tree.png)

**:  브라우저가 HTML 문서를 로드한 후 파싱하여 생성하는 모델**

→ DOM에서 모든 요소, 어트리뷰트, 텍스트는 하나의 객체이며 Document 객체의 자식

→ 요소의 중첩관계는 객체의 트리로 구조화하여 부자관계를 표현한다

→ DOM tree는 네 종류의 노드로 구성된다.

- **문서 노드(Document Node)**
    
    : DOM tree에 접근하기 위한 시작점(entry point)이다.
    
- **요소 노드(Element Node)**
    
    :  HTML 요소를 표현한다
    
- **어트리뷰트 노드(Attribute Node)**
    
    : HTML 요소의 어트리뷰트를 표현한다
    
- **텍스트 노드(Text Node)**
    
    : HTML 요소의 텍스트를 표현한다. 텍스트 노드는 DOM tree의 최종단이다.
    

## **DOM Query / Traversing (요소에의 접근)**

### ****하나의 요소 노드 선택(DOM Query)****

![select-an-individual-element-node.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/866c180b-8093-48e2-814b-0510bd06df80/select-an-individual-element-node.png)

- **[document.getElementById(id)](https://developer.mozilla.org/ko/docs/Web/API/Document/getElementById)**
    
    • id 어트리뷰트 값으로 요소 노드를 한 개 선택한다. 복수개가 선택된 경우, 첫번째 요소만 반한다.
    • Return: HTMLElement를 상속받은 객체
    • 모든 브라우저에서 동작
    
- **[document.querySelector(cssSelector)](https://developer.mozilla.org/ko/docs/Web/API/Document/querySelector)**
    
    • CSS 셀렉터를 사용하여 요소 노드를 한 개 선택한다. 복수개가 선택된 경우, 첫번째 요소만 반환한다.
    • Return: HTMLElement를 상속받은 객체
    • IE8 이상의 브라우저에서 동작
    

### ****여러 개의 요소 노드 선택(DOM Query)****

![select-multiful-elements.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/90783fd1-efad-4b33-9502-943a7f3f63b5/select-multiful-elements.png)

- [**document.getElementsByClassName(class)**](https://developer.mozilla.org/ko/docs/Web/API/Document/getElementsByClassName)
    
    • class 어트리뷰트 값으로 요소 노드를 모두 선택한다. 공백으로 구분하여 여러 개의 class를 지정할 수 있다.
    • Return: HTMLCollection (live)
    
    → **실시간으로 Node의 상태 변경을 반영한다**
    • IE9 이상의 브라우저에서 동작
    
- **[document.getElementsByTagName(tagName)](https://developer.mozilla.org/ko/docs/Web/API/Element/getElementsByTagName)**
    
    • 태그명으로 요소 노드를 모두 선택한다.
    • Return: HTMLCollection (live)
    • 모든 브라우저에서 동작
    
- **[document.querySelectorAll(selector)](https://developer.mozilla.org/ko/docs/Web/API/Document/querySelectorAll)**
    
    • 지정된 CSS 선택자를 사용하여 요소 노드를 모두 선택한다.
    • Return: [NodeList](https://developer.mozilla.org/ko/docs/Web/API/NodeList) (non-live)
    • IE8 이상의 브라우저에서 동작
    

### ****DOM Traversing (탐색)****

![traversing.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/acd94d2e-f38c-41f6-b74e-4e5c4a324f09/traversing.png)

- **[parentNode](https://developer.mozilla.org/ko/docs/Web/API/Node/parentNode)**
    
    • 부모 노드를 탐색한다.
    • Return: HTMLElement를 상속받은 객체
    • 모든 브라우저에서 동작
    
- **[firstChild](https://developer.mozilla.org/ko/docs/Web/API/Node/firstChild), [lastChild](https://developer.mozilla.org/ko/docs/Web/API/Node/lastChild)**
    
    • 자식 노드를 탐색한다.
    • Return: HTMLElement를 상속받은 객체
    • IE9 이상의 브라우저에서 동작
    
- **[hasChildNodes()](https://developer.mozilla.org/ko/docs/Web/API/Node/hasChildNodes)**
    
    • 자식 노드가 있는지 확인하고 Boolean 값을 반환한다.
    • Return: Boolean 값
    • 모든 브라우저에서 동작
    
- **[childNodes](https://developer.mozilla.org/ko/docs/Web/API/Node/childNodes)**
    
    • 자식 노드의 컬렉션을 반환한다. **텍스트 요소를 포함한 모든 자식 요소를 반환한다.**
    • Return: [NodeList](https://developer.mozilla.org/ko/docs/Web/API/NodeList) (non-live)
    • 모든 브라우저에서 동작
    
- **[children](https://developer.mozilla.org/ko/docs/Web/API/ParentNode/children)**
    
    • 자식 노드의 컬렉션을 반환한다. **자식 요소 중에서 Element type 요소만을 반환한다.**
    • Return: [HTMLCollection](https://developer.mozilla.org/ko/docs/Web/API/HTMLCollection) (live)
    • IE9 이상의 브라우저에서 동작
    

**[previousSibling](https://developer.mozilla.org/ko/docs/Web/API/Node/previousSibling), [nextSibling](https://developer.mozilla.org/ko/docs/Web/API/Node/nextSibling)**

• 형제 노드를 탐색한다. **text node를 포함한 모든 형제 노드를 탐색한다.**
• Return: HTMLElement를 상속받은 객체
• 모든 브라우저에서 동작

**[previousElementSibling](https://developer.mozilla.org/en-US/docs/Web/API/NonDocumentTypeChildNode/previousElementSibling), [nextElementSibling](https://developer.mozilla.org/en-US/docs/Web/API/NonDocumentTypeChildNode/nextElementSibling)**

• 형제 노드를 탐색한다. **형제 노드 중에서 Element type 요소만을 탐색한다.**
• Return: HTMLElement를 상속받은 객체
• IE9 이상의 브라우저에서 동작

## ****DOM Manipulation (조작)****

### ****텍스트 노드에의 접근/수정****

**접근 방법**

1. 해당 텍스트 노드의 부모 노드를 선택한다. 텍스트 노드는 요소 노드의 자식이다.
2. firstChild 프로퍼티를 사용하여 텍스트 노드를 탐색한다.
3. 텍스트 노드의 유일한 프로퍼티(`nodeValue`)를 이용하여 텍스트를 취득한다.
4. `nodeValue`를 이용하여 텍스트를 수정한다.

### ****어트리뷰트 노드에의 접근/수정****

**[className](https://developer.mozilla.org/ko/docs/Web/API/Element/className), [classList](https://developer.mozilla.org/ko/docs/Web/API/Element/classList), [id](https://developer.mozilla.org/ko/docs/Web/API/Element/id), [asAttribute(attribute)](https://developer.mozilla.org/en-US/docs/Web/API/Element/hasAttribute), [getAttribute(attribute)](https://developer.mozilla.org/ko/docs/Web/API/Element/getAttribute), [setAttribute(attribute, value)](https://developer.mozilla.org/ko/docs/Web/API/Element/setAttribute), [removeAttribute(attribute)](https://developer.mozilla.org/ko/docs/Web/API/Element/removeAttribute)** 를 사용하여 어트리뷰트 노드를 접근 및 수정할 수 있다.

### ****HTML 콘텐츠 조작(Manipulation)****

![innerHTML.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/39712c44-9722-486f-9b1a-769800beb927/innerHTML.png)

→ **HTML 콘텐츠를 조작(Manipulation)하기 위해 아래의 프로퍼티 또는 메소드를 사용할 수 있다**

- **[textContent](https://developer.mozilla.org/ko/docs/Web/API/Node/textContent), [innerText](https://developer.mozilla.org/ko/docs/Web/API/Node/innerText), [innerHTML](https://developer.mozilla.org/ko/docs/Web/API/Element/innerHTML)**

### ****DOM 조작 방식****

: **innerHTML 프로퍼티를 사용하지 않고 새로운 콘텐츠를 추가할 수 있는 방법은 DOM을 직접 조작하는 것**

1. 요소 노드 생성 createElement() 메소드를 사용하여 새로운 요소 노드를 생성한다. createElement() 메소드의 인자로 태그 이름을 전달한다.
2. 텍스트 노드 생성 createTextNode() 메소드를 사용하여 새로운 텍스트 노드를 생성한다. 경우에 따라 생략될 수 있지만 생략하는 경우, 콘텐츠가 비어 있는 요소가 된다.
3. 생성된 요소를 DOM에 추가 appendChild() 메소드를 사용하여 생성된 노드를 DOM tree에 추가한다. 또는 removeChild() 메소드를 사용하여 DOM tree에서 노드를 삭제할 수도 있다.

### ****insertAdjacentHTML()****

→ **[insertAdjacentHTML(position, string)](https://developer.mozilla.org/en-US/docs/Web/API/Element/insertAdjacentHTML) 사용**

### ****innerHTML vs. DOM 조작 방식 vs. insertAdjacentHTML()****

**innerHTML**

| 장점 | 단점 |
| --- | --- |
| DOM 조작 방식에 비해 빠르고 간편하다. | XSS공격에 취약점이 있기 때문에 사용자로 부터 입력받은 콘텐츠(untrusted data: 댓글, 사용자 이름 등)를 추가할 때 주의하여야 한다. |
| 간편하게 문자열로 정의한 여러 요소를 DOM에 추가할 수 있다. | 해당 요소의 내용을 덮어 쓴다. 즉, HTML을 다시 파싱한다. 이것은 비효율적이다. |
| 콘텐츠를 취득할 수 있다. |  |

**DOM 조작 방식**

| 장점 | 단점 |
| --- | --- |
| 특정 노드 한 개(노드, 텍스트, 데이터 등)를 DOM에 추가할 때 적합하다. | innerHTML보다 느리고 더 많은 코드가 필요하다. |

**insertAdjacentHTML()**

| 장점 | 단점 |
| --- | --- |
| 간편하게 문자열로 정의된 여러 요소를 DOM에 추가할 수 있다. | XSS공격에 취약점이 있기 때문에 사용자로 부터 입력받은 콘텐츠(untrusted data: 댓글, 사용자 이름 등)를 추가할 때 주의하여야 한다. |
| 삽입되는 위치를 선정할 수 있다. |  |

**결론**

innerHTML과 insertAdjacentHTML()은 크로스 스크립팅 공격(XSS: Cross-Site Scripting Attacks)에 취약하다. 따라서 untrusted data의 경우, 주의하여야 한다. **텍스트를 추가 또는 변경시에는 textContent**, **새로운 요소의 추가 또는 삭제시에는 DOM 조작 방식을 사용**하도록 한다.

# 이벤트

****3.1 UI Event****

| Event | Description |
| --- | --- |
| load | 웹페이지의 로드가 완료되었을 때 |
| unload | 웹페이지가 언로드될 때(주로 새로운 페이지를 요청한 경우) |
| error | 브라우저가 자바스크립트 오류를 만났거나 요청한 자원이 존재하지 않는 경우 |
| resize | 브라우저 창의 크기를 조절했을 때 |
| scroll | 사용자가 페이지를 위아래로 스크롤할 때 |
| select | 텍스트를 선택했을 때 |

****3.3 Mouse Event****

| Event | Description |
| --- | --- |
| click | 마우스 버튼을 클릭했을 때 |
| dbclick | 마우스 버튼을 더블 클릭했을 때 |
| mousedown | 마우스 버튼을 누르고 있을 때 |
| mouseup | 누르고 있던 마우스 버튼을 뗄 때 |
| mousemove | 마우스를 움직일 때 (터치스크린에서 동작하지 않는다) |
| mouseover | 마우스를 요소 위로 움직였을 때 (터치스크린에서 동작하지 않는다) |
| mouseout | 마우스를 요소 밖으로 움직였을 때 (터치스크린에서 동작하지 않는다) |

****3.4 Focus Event****

| Event | Description |
| --- | --- |
| focus/focusin | 요소가 포커스를 얻었을 때 |
| blur/foucusout | 요소가 포커스를 잃었을 때 |

****3.2 Keyboard Event****

| Event | Description |
| --- | --- |
| keydown | 키를 누르고 있을 때 |
| keyup | 누르고 있던 키를 뗄 때 |
| keypress | 키를 누르고 뗏을 때 |

****3.5 Form Event****

| Event | Description |
| --- | --- |
| input | input 또는 textarea 요소의 값이 변경되었을 때 |
|  | contenteditable 어트리뷰트를 가진 요소의 값이 변경되었을 때 |
| change | select box, checkbox, radio button의 상태가 변경되었을 때 |
| submit | form을 submit할 때 (버튼 또는 키) |
| reset | reset 버튼을 클릭할 때 (최근에는 사용 안함) |

****3.6 Clipboard Event****
| Event | Description |
| --- | --- |
| cut | 콘텐츠를 잘라내기할 때 |
| copy | 콘텐츠를 복사할 때 |
| paste | 콘텐츠를 붙여넣기할 때 |

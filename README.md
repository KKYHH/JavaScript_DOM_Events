# GitHub Pages

https://kkyhh.github.io/JavaScript_DOM_Events/

<img src="../starter/guessMyNumber.png">

---

### 설명

JavaScript의 DOM 과 Events Fundamentals를 사용해본다

---

#### DOM ( 문서 객체 모델 )

HTML 문서를 구조적으로 나타내는것
DOM은 JavaScript를 이용해 HTML 요소와 스타일에 액세스해 조작할 수 있게 한다

---

#### DOM Tree Structure

웹 브라우저가 HTML 문서를 로드할 때 문서 내의 요소와 해당 관계를 나타내는 개체의 트리형 구조를 만든다

이 트리 구조를 DOM 트리라고 한다
각 HTML 요소는 트리의 노드가 된다

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Sample Page</title>
  </head>
  <body>
    <div id="container">
      <h1>Hello, World!</h1>
      <p>This is a sample paragraph.</p>
    </div>
  </body>
</html>
```

- `<html>` 요소는 루트 노드
- `<head>` 및 `<body>`는 `<html>`의 하위 노드
- `<title>`은 `<head>`의 하위 노드
- `<div>`는 `<body>`의 하위 노드
- `<h1>` 및 `<p>`는 `<div>`의 하위 노드

---

#### JavaScript 와 DOM의 관계

JavaScript는 DOM과 상호 작용하여 웹페이지의 콘텐츠, 구조 및 스타일을 동적으로 업데이트 한다. 브라우저는 현재 웹페이지의 DOM을 나타내는 '문서'라는 전역 개체를 노출한다. JavaScript를 사용하여 요소에 액세스하고 조작을 한다

```javascript
const heading = document.querySelector('h1');
heading.textContent = 'Hello, New World!';
```

여기서 `document.querySelector('h1')`는 `<h1>` 요소를 검색하고 `textContent`는 해당 텍스트를 변경하는 데 사용됩니다.

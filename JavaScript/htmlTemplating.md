HTML templating은 반복적인 HTML 태그 부분을 template로 만들어두고, 서버에서 온 데이터(주로 JSON)와 결합하여 화면에 추가하는 작업을 말한다.

```jsx
var data = { title: 'hello', content: 'lorem dkfief', price: 2000 };

//HTML의 script에서 가져온 HTML Template
var html = document.querySelector('#template-list-item').innerHTML;

html
  .replace('{title}', data.title)
  .replace('{content}', data.content)
  .replace('{price}', data.price); //메서드 체이닝

document.querySelector('.content').innerHTML = resultHtml;
```

id가 template-list-item인 템플릿 안의 HTML 코드를 가져와서, {title}을 data.title로, {content}를 data.content로, {price}를 data.price로 바꾼다.

class가 content인 요소의 안에 넣는다.

※ 템플릿 길이가 길면 따로 템플릿을 만들어 Ajax로 호출해서 사용하는 일이 많다. (데이터는 서버에서 호출),

템플릿 리터럴(template literal)을 쓰면 replace 메서드 없이 쉽게 템플릿 작업을 할 수 있다.

라이브러리를 사용하는 방법도 있다. ([handlebars 사용하는 법 보러가기](https://enai.tistory.com/16))

(자바스크립트 템플릿이란 HTML 조각을 동적으로 만들어서 페이지에 추가하는 것이다.)

리액트로 JSX를 사용했다. 자바스크립트 문법에 가깝고 쉬워 새로 배워야 할 것이 거의 없었기 때문이다.

# CORS

## JavaScript의 "동일출처정책(the same-origin policy)"에 대해서 설명하세요.

동일 출처 정책은 어떤 출처에서 불러온 문서나 스크립트가 다른 출처에서 가져온 리소스와 상호작용하는 것을 제한하는 보안 방식입니다.

여기서 동일한 출처는 두 URL의 프로토콜, 포트, 호스트가 모두 같은 경우를 말합니다.

동일 출처 정책은 잠재적으로 해로울 수 있는 문서를 분리함으로써 공격받을 수 있는 경로를 줄입니다.

## CORS는 무엇인가

CORS는 교차 출처 리소스 공유로, 추가 http 헤더를 사용하여 한 출처에서 실행중인 웹 애플리케이션이 다른 출처의 선택한 자원에 접근할 수 있는 권한을 부여하도록 브라우저에 알려주는 체제입니다.

웹 애플리케이션은 리소스가 자신의 출처와 다를 때 교차 출처 http 요청을 실행합니다.

보안 상의 이유로, 브라우저는 스크립트에서 시작한 교차 출처 http 요청을 제한하는 동일 출처 정책을 따릅니다. 따라서 다른 출처의 리소스를 불러오려면 그 출처에서 올바른 CORS 헤더를 포함한 응답을 반환해야합니다.

[참고 🔗](https://developer.mozilla.org/ko/docs/Web/HTTP/CORS)

## CORS를 대처하는 방법과 우회하는 방법

JSONP 사용 : HTML의 `script` 요소로부터 요청되는 호출에는 정책이 적용되지 않는 것을 이용한 우회 방법. 단점으로는 GET 요청만 가능하다.

Access-Control-Allow-Origin 세팅하기 : CORS 정책 위반으로 인한 문제를 해결하는 가장 대표적인 방법은, 그냥 정석대로 서버에서 Access-Control-Allow-Origin 헤더에 알맞은 값을 세팅해주는 것이다.

Webpack Dev Server로 리버스 프록싱하기 : webpack-dev-server 라이브러리가 제공하는 프록시 기능을 사용하면 아주 편하게 CORS 정책을 우회할 수 있다.

```jsx
module.exports = {
  devServer: {
    proxy: {
      '/api': {
        target: 'https://api.evan.com',
        changeOrigin: true,
        pathRewrite: { '^/api': '' },
      },
    },
  },
};
```

[참고 🔗](https://evan-moon.github.io/2020/05/21/about-cors/)

# Http(HyperText Transfer Protocol)

- Web상에서 Client와 Server 간 정보를 주고 받을 수 있는 프로토콜이다.
- TCP/IP 프로토콜을 기반으로 작동한다.
- Client와 Server 사이에서 이루어지는 **요청(HTTP Request)/응답(HTTP Response)** 프로토콜이다.
    - 요청과 응답은 **HTTP Message**로 이루어져 있다.

## HTTP Request
<img src="https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview/http_request.png" width="400" height="200">

[출처](https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview)

## HTTP Response
<img src="https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview/http_response.png" width="500" height="300">

[출처](https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview)


### HTTP Method
<img src="https://user-images.githubusercontent.com/85678496/235483820-bdda66b3-6662-465f-b0f3-796cbbb780dd.png" width="700" height="300">

[출처](https://ko.wikipedia.org/wiki/HTTP)

## HTTP Message

- HTTP Message는 크게 Headers와 Body로 나뉜다.

### [HTTP headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers)

- Client와 Server는 요청/응답과 함께 HTTP headers을 사용해 추가적인 정보를 전달할 수 있다.
    - 유형, 길이, 인코딩 방식 등의 정보를 포함하고 있다.
- HTTP headers는 `이름: 값` 형태로 구성된다.
    - 이름은 대소문자를 구분하지 않는다.
    - 값 앞에 공백은 무시한다.
- 값을 포함한 전체 HTTP headers는 한 줄로 구성되며 매우 길 수 있다.

### Body

- 실제 데이터가 포함되는 부분이다.
    - HTML 페이지나 이미지 파일 등이 포함된다.
- 모든 request에 body가 존재하는 것은 아니다.
    - GET, HEAD, DELETE, OPTIONS 와 같이 resources를 가져오는 request에는 일반적으로 Body가 필요하지 않다.
    - 서버로 데이터를 전송하는 일부 요청(ex. POST)의 경우 Body를 필요로 한다.
- Single-resource bodies :  Content-Type, Content-Length 두 헤더로 정의
- Multiple-resource bodies

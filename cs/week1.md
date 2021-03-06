week_1
======
### HTML, CSS, Javascript 란?
**HTML (hypertext markup language)** 의 약자로써 익히 일려 진 웹 서비스를 위한 언어이다. 태그(Tag) 혹은 요소(Element)들로 비교적 간단하게 구조적 문서를 작성할 수 있는 장점이 있습니다. 
> 하지만 프로그래밍 언어가 아니기에 단독 사용 시 제한된  기능들이 다수 존재합니다. 
###### 대표적인 HTML의 기본 구조
```html
<!doctype html>
<html>
  <head>
    <title>Lion's HTML</title>
  </head>
  <body>
    <p>Hello Lion!</p>
  </body>
</html>
```
예를 들어 같이 사용되는 언어 중 하나인 **CSS (cascading style sheets)** 는 마크업 언어의 시각적인 속성들을 조작할 수 있는 언어입니다. 개발자는 HTML + CSS로 대부분의 요구 조건들을 만족할 수 있지만 해당 언어 역시 프로그래밍 언어가 아니기에 특수한 효과 및 기능에 제한이 있습니다. 
>번외로 CSS 내 변수나 상속 기능, 반복문 등을 지원하여 양이 많아 복잡한 스타일 시트를 조금 더 편하게 도와주는 SASS, LESS 등이 존재합니다. 
###### 선택자를 활용하여 속성을 제어할 수 있으며 HTML 내에서 사용 시 <style> 태그로 감싸져야 한다.
```css
p {color: "#6dbfb6"}
```
CSS + HTML으로 웹페이지는 제작하였지만 다소 정적인 상태를 유지합니다. 이를 더욱 유연하고 동적인 페이지로 만들기 위해서는 **Javascript** 를 활용하여 완성도 있는 결과물을 제작할 수 있습니다. Javascript는 객체 기반의 프로그래밍 언어로써 웹 브라우저에서 주로 사용되며, 접근성과 범용성이 넓어 많은 라이브러리 등에 기반하여 사용되고 있다.
###### Javascript의 함수 사용 예시이며 CSS와 마찬가지로 문서 내 사용 시 <script> 태그로 감싸야 한다.
```javascript
alert("Hello Lion!");
```
 
 * * *
 
### 브라우저의 동작 방식에 대해서
사용자가 웹 브라우저를 통해 http://naver.com으로 이동한다면 짧은 시간 내에 홈페이지에 접근할 수 있다. 이 짧은 시간 내에 클라이언트와 서버 사이에서는 많은 작업이 발생한다. 
 
![브라우저 구조](/img/browser_struct.png)
###### 웹 브라우저의 구조
 
사용자 인터페이스를 통해 응답을 받게 된다면 브라우저 엔진이 렌더링 엔진으로 전송하게 되고, 렌더링 엔진으로 넘겨진 요청은 콘텐츠를 을 표시하는 역할이며 HTML 등 문서와 이미지 등을 표시합니다.
##### 각 브라우저마다 다른 엔진을 사용하기 때문에 조금은 다르지만 기본적인 동작은 다음과 같습니다.

![렌더링 엔진](/img/randering_engine.png)
###### 렌더링 엔진의 흐름

렌더링 엔진 HTML 문서를 분석하고, 콘텐츠 트리 내부에서 **DOM** 노드로 변환합니다. 다음으로 외부 CSS 파일과 함께 포함된 스타일 요소도 분석하고, 스타일 정보와 HTML 표시 규칙은 렌더 트리를 생성합니다.   
렌더 트리 생성을 마치면 화면 배치가 시작되어 각 노드별 위치에 표시합니다.

* * *
 
### DOM에 대해서
브라우저 렌더링 엔진은 웹 문서를 로딩한 후, 분석하여 웹 브라우저가 이해할 수 있는 구조로 구성되어 메모리에 적재합니다. 이를 **DOM(doument object model)** 이라 합니다. HTML, XML 문서에 접근하기 위한 인터페이스이며,  문서 내의 모든 요소를 정의하고, 각 요소별 접근 방법을 제공합니다. 
 
![DOM 구조](/img/DOM_struct.png)
###### DOM 구조
 
브라우저의 렌더링 엔진에서 제작된 DOM tree는 네 종류의 노드로 구성됩니다.
#### Document Node 
  * 트리의 최상위에 존재하며 각 노드에 접근하려면 문서 노드를 통해야 하고, DOM tree에 접근하기 위한 **시작점** 입니다.    
#### Element Node
  * HTML 요소를 표현합니다. 중첩에 의한 자손 관계를 가져 이 관계를 통해 정보를 구조화합니다.
#### Attribute Node
  * HTML 요소별 속성을 표현합니다. 종속관계를 가지지 않으며 해당 요소의 일부이며 요소 노드에 접근하면 속성을 참조, 수정할 수 있습니다.    
#### Text Node
  * HTML 요소의 텍스트를 나타내고 요소 노드의 자식이며 텍스트 노트는 종속을 받을 수 있지만 다른 노드를 종속시킬 수는 없습니다. **DOM tree** 의 끝점입니다.
 
> DOM은 Javascript를 통해 동적으로 변경할 수 있으며 변경된 DOM은 렌더링에 반영됩니다.
 
* * *
 
### HTTP, HTTPS에 대해서
**HTTP(hypertext transfer protocol)** 은 통신 프로토콜 중 하나이며 HTML 같은 리소스들을 가져올 수 있는 프로토콜입니다. 주로 웹에서 이루어지는 모든 데이터 교환의 기초이고, 클라이언트 - 서버 방식으로 **요청(request)** 과 **응답(response)** 을 통해 데이터를 송수신 합니다.

![DOM 구조](/img/HTTP.png)
###### HTTP
클라이언트 프로그램(웹 브라우저)는 URI(uniform resource identifiers)를 활용해  WWW 상에서 리소스 위치를 찾습니다. 리소스는 문서, 이미지, 동영상 등 모든 것이 될 수 있습니다. 웹페이지의 위치를 나타내기 위해 사용되는 http://www.naver.com 을 분석해 보자면

 * http : 리소스에 접근하기 위해 HTTP 프로토콜을 사용한다.
 * www.naver.com : 리소스의 인터넷 위치이며, DNS를 통해 IP 주소로 변환되어 서버의 위치를 찾을 수 있다.
 
###### HTTP 통신을 서버에 활용하려면 일부 Method를 통해 요청할 수 있고 종류는 GET, POST, PUT, DELETE, HEAD 등 이 있으며 정보를 요청 및 수정이 가능합니다.

요청받은 응답 데이터는 Header와 Body(본문)의 포맷으로 구성되어 있으며 Header에는 메시지, 요청 Method, HTTP 버전 등이 등재되어 있고 Body에는 HTML이 담겨 있어 브라우저가 화면에 렌더링 하게 된다.

> 상태 메시지에는 크게 4분류로 200번에서 500번대 메시지 있고, 대표적으로 많이 알려진 404 Not Found가 요청한 정보를 찾을 수 없을 때 나타나는 상태 메시지에 해당하는 것이다.
 ###### HHTTPS 
 **(HTTP SecuSecure)** 는 HTTPS의 암호화된 버전이며 클라이언트와 서버 간의 통신 정보를 암호화 하기 위해 SSL 이나 TLS을 사용한다. 
 * * *
 
###### 이미지 출처
* https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/
* https://www.w3schools.com/js/js_htmldom.asp

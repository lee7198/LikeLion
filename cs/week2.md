week_2
======



### CSS로 Login Form 구성하기
 [실습물](https://lee7198.github.io/LikeLion/week2/)
### Bootstrap 사용하여 UI 구성하기
 [실습물](https://lee7198.github.io/LikeLion/week2-2/)

- Ajax란
    
    AJAX란 비동기 자바스크립트와 XML (Asynchronous Javascript And XML)을 말합니다. 간단히 말하자면, 서버와 통신하기 위해 XMLHttpRequest 객체를 사용하는 것을 말합니다. 
    
    JSON, XML, HTML 그리고 일반 텍스트 형식 등을 포함한 다양한 포맷을 주고받을 수 있습니다. AJAX의 강력한 특징 중 하나인 **비동기성**은 페이지를 새로고침 하지 않고도 해당 객체만 업데이트할 수 있습니다.
> 웹페이지가 로드된 후에도 지속적으로 서버로 요청을 보내고 받을 수 있으며 백그라운드 영역에서도 서버로 데이터를 보낼 수 있습니다.
    
- 반응형 디자인이란
    
    디지털 시대가 다가오면서 다양한 크기의 화면을 가진 기기들이 시중에 나오고 있습니다.
    
    사용자들의 기기는 모바일 핸드폰, 태블릿, PC 등 다양해지고 있고 해상도 또한 다양하게 사용되고 있습니다. 
    
    기존 웹 페이지로써는 가장 대중적인 해상도를 지정하여 그 틀에서만 디자인을 하였다면, 현재는 반응형 디자인을 통해 어느 기기에서나 정보를 보여줄 수 있는 틀을 사용하게 되어. 유저는 모바일 기기에서나 PC에서나 어디에서든지 웹 서비스를 이용할 수 있습니다.
    
    웹에서 이용 방법은 주로 CSS에서 처리 가능하며 일반적으로 특정 크기에서 스타일 시트가 적용되게 작성하고 있습니다.

```css
/* 대표적인예시로 특정 크기 범위에서만 적용되게 */ 
@media (min-width: 481px) and (max-width: 768px) { 
	body { 
		/* 스타일 속성들 */ 
	} 
}
```

![반응형 웹](/img/responsive-web.jpeg)


###### 이미지 출처
* https://blog.helloweb.co.kr/hello-web-ecommerce-responsive-web/

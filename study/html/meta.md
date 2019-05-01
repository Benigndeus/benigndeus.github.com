# \<meta> 태그

메타태그는 서버와 브라우저간에 상호 교환되는 정보를 정의하는데 사용한다.

HTML 문서의 \<head\>와 \</head\> 사이에 입력하는 특수 태그로서 사이트의 디자인에는 전혀 영향을 미치지 않고 문서가 어떤 내용을 담고 있고, 문서의 키워드는 무엇이며, 누가 만들었는지 등의 문서 자체의 특성을 담는다.

## 메타태그의 속성

메타태그 속성에는 http-equiv, name, content 3가지 속성이 있다.

- http-equiv="항목명"  
  : 웹 브라우저가 서버에 명령을 내리는 속성으로 name 속성을 대신하여 사용될 수 있으며, HTML 문서가 응답 헤더와 함께 웹 서버로부터 웹 브라우저에 전송되었을 때에만 의미를 가진다.

- content="정보값"  
  : meta 정보의 내용을 지정한다.

- name="정보 이름"  
  : 몇 개의 meta 정보의 이름을 정할 수 있으며 지정하지 않으면 http-equiv 와 같은 기능을 한다.

## 메타태그의 종류

- 검색 엔진에 의해 검색되는 단어를 지정한다.  
`<meta name="Keywords" content="Web, html, 웹 표준" />`

- 검색 결과에 표시되는 문자를 지정한다.  
`<meta name="Description" content="Web, html, 웹 표준" />`

- 검색 로봇 제어  
`<meta name="Robots" content="noindex, nofollow" />`  
검색로봇에 대한 명령은 `<meta name="robots">`라는 형식으로 지정한다.

- content 속성에는 다음과 같이 지정할 수 있고 복수지정할 때에는 콤마(,)로 구분한다.  
  - `All(기본값)` : 'index, follow' 를 지정한 것과 같다.
  - `None` : 'noindex, nofollow' 를 지정한 것과 같다.
  - `Index` : 그 페이지를 수집 대상으로 한다.
  - `Follow` : 그 페이지를 포함해 링크가 걸린 곳을 수집 대상으로 한다.
  - `Noindex` : 그 페이지를 수집대상에서 제외한다.
  - `Nofollow` : 그 페이지를 포함해 링크가 걸린 곳을 수집 대상으로 하지 않는다.

이들 name 속성과 content 속성의 값에 대해 html4.01 권고안에는 대문자로 기술하고 대문자와 소문자를 구별하게 되어 있지만 실제 검색로봇을 대문자와 소문자를 구별하지 않는다.

또 아래와 같은 값도 사용되지만 웹 표준에서는 인정하지 않는 속성이 있다.

- `Noarchive` : 그 페이지를 캐시하지 않는다.
- `Noimageindex` : 그 페이지에 포함된 이미지를 검색 대상에서 제외한다.
- `Noimageclick` : 그 페이지에 포함된 이미지의 링크를 방지힌다.

## 문자 코드의 종류 설정  

`<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />`

문자 인코딩의 종류

- `EUC-KR / ISO-2022-KR` : 한국어 문자 인코딩
- `EUC-JP / ISO-2022-JP` : 일본어 문자 인코딩
- `GB2312` : 중국어 문자 인코딩
- `ISO-8859-1` : 북미, 서부유럽, 라틴 아메리카, 카리브해, 캐나다, 아프리카
- `ISO-8859-2` : 동유럽
- `ISO-8859-3` : 남동유럽, 에스페란토
- `ISO-8859-4` : 스칸디나비아, 발트 연안국
- `ISO-8859-5` : 불가리아어, 벨로루시어, 러시아어, 마케도니아
- `ISO-8859-6` : 아랍문자
- `ISO-8859-7` : 현대 그리스문자 언어뿐 만 아니라 수학 기호
- `ISO-8859-8` : 히브리어 문자를 사용하는 언어
- `ISO-8859-9` : 터키어
- `ISO-8859-10` : 에스키모, 북유럽 언어
- `UTF-8, UTF-16, UTF-32`  : 모든 언어의 문자를 지원하는 인코딩

위에 나열된 ISO-숫자 타입의 문자 설정은 크기에 제한이 있고 다국어 환경에서 호환이 되지 않기 때문에 유니코드 컨소시엄이 개발한 유니코드 표준으로 대체되어야 한다.

유니코드 표준은 모든 문자설정, 구두점, 세계의 기호에 적용된다.

유니코드는 어떤 언어든지 어떤 프로그램이던지 어떤 텍스트의 플랫폼을 기억하거나 바꾸는 것을 처리할 수 있게 한다.

유니코드 컨소시엄(The Unicode Consortium)은 유니코드 표준을 개발한다.

그들의 목적은 기존 문자를 유니코드 변환 포맷(UTF)로 대체하는 것이다.

유니코드 표준은 xml, java, ECMAScript(JavaScript), LDAP, WML 등에서 구현되고 있다. 그리고 유니코드 표준은 여러 운영체제와 모든 현대 웹 브라우저에서 지원된다.

유니코드 컨소시엄은 주요 표준개발기구(ISO, W3C, ECMA)와 협력하고 있다.

- 날짜(제작일)  
  `<meta name="Date" content="2016-02-15T07:45:37+09:00" />`
  name="Date"를 사용할 때 content '+09:00' 은 GMT(그리니치 표준시)로 부터의 시차이며, 한국은 '+09:00', 미국 동부는 '-05:00'(서머타임 때에는 -04:00)이 되며 나라/지역에 따라 결정된다.

- 웹 페이지에 쓰인 언어를 지정  
  `<meta http-equiv="Content-Script-Type" content="text/javascript" />`
  `<meta http-equiv="Content-Style-Type" content="text/css" />`

- 브라우저 호환성을 지정  
  `<meta http-equiv="X-UA-Compatible" content="IE=edge" />`

- 홈페이지 주제를 지정  
  `<meta http-equiv="Subject" content="웹 표준을 위한 사이트" />`

- 제목을 지정  
  `<meta http-equiv="Title" content="웹 표준" />`

- 페이지를 작성한 제작자명을 지정  
  `<meta http-equiv="Author" content="name" />`

- 제작사를 지정  
  `<meta http-equiv="Publisher" content="name" />`

- 웹 책임자를 지정  
  `<meta http-equiv="Other Agent" content="name" />`

- 제작 도구를 지정  
  `<meta http-equiv="Generator" content="CODA" />`

- 메일 주소를 지정  
  `<meta http-equiv="Reply-To" content="naver@naver.com" />`
  `<meta http-equiv="Email" content="naver@naver.com" />`

- 파일 이름을 지정  
  `<meta http-equiv="Filename" content="index.html" />`

- 위치를 지정  
  `<meta http-equiv="Location" content="위치" />`

- 배포자를 지정  
  `<meta http-equiv="Distribution" content="name" />`

- 저작권을 지정  
  `<meta http-equiv="Copyright" content="copyright@web address" />`

- 제작 년,월,일을 지정  
  `<meta http-equiv="Build" content="date" />`

- 최종 수정일을 정의  
  `<meta http-equiv="Last-Modified" content="Mon,20 Jul 2016 19:30:30" />`

- 그림 위에 마우스 오버시 이미지 관련 툴바를 생기지 않도록 하기 위해 지정  
  `<meta http-equiv="imagetoolbar" content="no" />`

- 캐쉬가 되지 않도록 하기 위해 정의  
  `<meta http-equiv="Cache-Control" content="no-cache" />`  
  `<meta http-equiv="Pragma" content="no-cache" />`  
  페이지를 cache에서 가져오지 않게 하며 항상 서버에 접속해서 페이지를 가져온다. 그러므로 방문자의 브라우저가 항상 cache를 읽도록 해 놓아도 이것을 무시하고 페이지를 갱신한다. 자주 고치는 페이지에서는 이것을 사용하는 것이 항상 방문자에게 바뀐 내용을 보여 줄 수가 있습니다. 하지만 페이지 출력 속도는 매번 페이지를 가져오므로 cache를 사용할 수 없어서 시간이 많이 걸린다는 점입니다.

- 캐쉬 만료일을 정의  
  `<meta http-equiv="Expires" content="Mon, 08 Sep 2016 10:10:10 GMT" />`

- 60초마다 새로고침을 정의  
  `<meta http-equiv="Refresh" content="60" />`

- 입력한 주소로 5초후 이동하는 것을 정의
  `<meta http-equiv="Refresh" content="5;url=주소" />`

- 페이지 들어갈 때 장면 전환 효과
  `<meta http-equiv="Page-Enter" content="revealtrans(Duration=1, Transition=12)" />`  

- 장면 전환 효과 속성값
  - `Box out` : 네모난 박스가 안쪽에서 바깥쪽으로
  - `Circle in` : 원이 바깥에서 안쪽으로
  - `Circle out` : 원이 안쪽에서 바깥쪽으로
  - `Wipe up` : 이미지의 아래에서 위쪽으로 수직 이동
  - `Wipe down` : 이미지의 위에서 아래쪽으로 수직 이동
  - `Wipe right` : 이미지의 왼쪽에서 오른쪽으로 수평 이동
  - `Wipe left` : 이미지의 오른쪽에서 왼쪽으로 수평 이동
  - `Vertical blinds` : 수직 블라인드가 쳐지는 형태로 변환
  - `Horizontal blinds` : 수평 블라인드가 쳐지는 형태로 변환
  - `Checkerboard acros`s : 바둑판 형태의 격자가 왼쪽에서 오른쪽으로 생성
  - `Checkerboard down` : 바둑판 형태의 격자가 위에서 아래로 생성
  - `Random dissove` : 안개와 비슷한 형태로 전환
  - `Split vertical in` : 왼쪽과 오른쪽 끝에서 중앙으로 수직 이동
  - `Split vertical out` : 중앙에서 양쪽 끝으로 수직 이동
  - `Split Horizontal in` : 양쪽에서 중앙으로 수평 이동
  - `Split Horizontal out` : 중앙에서 양쪽끝으로 수직이동
  - `Strips left down` : 대각선 형태로 오른쪽 상단에서 왼쪽 하단으로 이동
  - `Strips left up` : 대각선 형태로 오른쪽 하단에서 왼쪽 상단으로 이동
  - `Strips right down` : 대각선 형태로 왼쪽 상단에서 오른쪽 하단으로 이동
  - `Strips right up` : 대각선 형태로 왼쪽 하단에서 오른쪽 상단으로 이동
  - `Random bars horizontal` : 수평선이 무작위로 생성
  - `Random bars vertical` : 수직선이 무작위로 생성
  - `Random` : 임의로 생성

---

# http-equiv

meta 요소에서 문서의 초기정보를 나타내는 속성은 `http-equiv` 속성이다. 이속성을 지정하면 문서의 **기본언어(content-language)**, **MIME 타입(content-type)**, **기본 스타일시트(default-style)**, **브라우저호환성설정(X-UA-Compatible)**, **페이지 리로드(refresh)** 등을 나타낼 수 있다.  아래는 속성값에 대한 설명이다.

## content-language 속성값

`<meta http-equiv="content-language" content="ko">`

우선 content-language 속성값은 기본언어를 설정할 수 있다. content 속성값에는 그에 맞는 값을 입력해야한다. 여기선 기본언어에 대한 값이 들어가야한다.  아래 예제에서는 ko(한국어) 로 설정되어 있다.

## content-type 속성값

`<meta http-equiv="content-type" content="text/html ; charset=UTF-8 ">`

두번째로 볼 속성값은 content-type 속성값이다. 이 속성값은 문서의 MIME 타입이나 문서의 문자셋을 설정할 수 있다. MIME 타입 을지정한다음 문자 인코딩을 지정하기전에 세미콜론(;) 으로 구분을 해준다는걸 명심하자.

## default-style 속성값

`<meta http-equiv="default-style" content="middle">`  
`<link rel="stylesheet" media="screen" href="middle.css" type="text/css"  title="middle">`

세번째 속성값은 기본 스타일 시트를 설정하는  default-style 이다. 이 값은 기본 스타일 시트를 설정하는 부분이다. 이속성값을 지정하면 익스플로러 기준으로 본다면, 메뉴->보기->스타일 을 들어가서 설정된 값을 볼 수 있다. 근데 이 속성값이 과연 쓰이는지 의문이다. 이 속성을 적용하기 위해선 스타일시트를 지정할 때 아래처럼 title 속성을 정의 하여, 기본 스타일 시트 값을 지정해 주어야한다. 예제의 title 속성값은 middle 로 되어있다.

## X-UA-Compatible 속성값

`<meta http-equiv="X-UA-Compatible" content="IE=edge">`

다음으로 브라우저 호환 설정을 할 수 있는 X-UA-Compatible 속성값이 있다. 이속성값을 지정하면, 브라우저의 문서모드를 지정할 수 있다. 아래 같은경우 IE=edge 의 뜻은 최신버전으로 문서모드를 설정하라는 뜻이다.

## refresh 속성값

`<meta http-equiv="refresh" content="20 ; http://tistory.com">`  

마지막으로 페이지 리로드를 설정 하는 속성값인 refresh 가 있다. 이 속성값은 페이지를 리로드 하거나 자동으로 다른 페이지를 이동시키는 기능을 한다. 위 같은 경우 20초 후에 티스토리 싸이트로 이동하게 되는 설정이다. 이곳에서도 세미콜론(;)을 잘 확인할 것. 만약 content 속성값에 시간만 입력하고 이동될 페이지를 지정하지 않으면  그냥 리로드(새로고침)가 된다. 즉 웹페이지를 새로고침한 효과다.

---

meta 요소는 맨 처음 오는 속성값에 따라서 여러가지 정보를 설정할 수 있다. 그중에서 문서의 정보를 설정 할 수 있는 mete name 이 있다. 아래는 meta name 의 간단한 사용 예제이다.

- meta 의 name 속성 간단한 예제

`<meta name="author" content="Dreamload">`  
`<meta name="description" content="meta name 의 간단한 사용 예제">`  
`<meta name="keywords" content="meta,html,요소,속성">`  

위의 예제에서는 name 속성값으로 author, description, keywords 가 적용되었다. 아래의 표는 name 속성값으로 올 수 있는 값들이 나와있다. 이러한 속성값들을 지정하면 content 속성값에 그에 맞는 값들을 설정할 수 있다.

 name 속성 값으로 올 수 있는 것들

- `author`: 이 속성값을 지정하면 문서의 저자를 나타낼 수 있다.
- `description`: 이 속성값을 지정하면 문서의 개요를 설정할 수 있으며, 검색 엔진의 검색 결과로 표시가 된다. 하지만 요즘은 이 속성값보단 meta의 property 속성을 지정하여 문서의 여러 정보들을 설정하는듯 하다.
- `generator`: 이 속성값 사용설명에는 문서 작성에 사용된 소프트웨어의 이름을 나타낸다고 나와있지만, 이 속성값이 정말 쓰이는지는 의문이다.
- `keywords`: 이 속성값을 지정하면, 검색 엔진 로봇에게 제공할 키워드를 지정 할 수 있다. 이 속성 역시 검색 로봇이 반영하는지는 잘 모르겠다.
- `viewport`: 이 속성값을 지정하면 스마트폰 기기의 화면을 설정할 수 있다. 자세한건 아래 포스팅 자료를 확인하면 된다.
- `application-name`: 문서가 웹 애플리케이션용으로 만들어진 경우 이 속성값을 지정하면 웹 애플리케이션의 이름을 지정할 수 있다. 이 속성 역시 한 번도 사용해 본 적이 없어서 실제로 사용되는지 의문이다.
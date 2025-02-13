> # 2.1 자바스크립트의 탄생

- 간략하게 **웹페이지의 보조적인 기능을 수행하기 위해 브라우저에서 동작하는
경량 프로그래밍 언어**를 도입의 필요성이 있었는데, 그때 탄생한 것이 자바스크립트이다.

처음에는 보조적인 기능을 수행하기 위한 언어였지만, 현재는 모든 브라우저의 표준 프로그래밍 언어로 자리잡게 되었다

> # 2.2 자바스크립트의 표준화

- 넷스케이프 커뮤니케이션즈와 마이크로소프트는 자사 브라우저의 시장 점유율을 높이기 위해 자사 브라우저에서만 동작하는 기능을 경쟁적으로 추가하기 시작하였다.

이로인해 브라우저에 따라 웹페이지가 정상적으로 동작하지 않는 **크로스 브라우징**(Cross Browsing)이슈가 발생하였고, 결과적으로 모든 브라우저에서 정상적으로 동작하는 웹페이지를 개발하기가 어려워졌다.

모든 브라우저에서 정상적으로 동작하는 표준화된 자바스크립트의 필요성이 대두되기 시작하면서, 1997년 ECMA 인터내셔널에서 표준화된 자바스크립트의 초판 사양이 완성되었고, 상표권 문제로 **ECMAScript**로 명명되었다.

1997년에 완성된 초판인 ES1버전부터 시작하여 2020년까지 ES11버전까지 업데이트 되었다.

> # 2.3 자바스크립트 성장의 역사

- 초창기 자바스크립트는 웹페이지의 보조적인 기능을 수행하기 위해 한정적인 용도로 사용되었으며, **대부분의 로직은 웹 서버에서 실행**되었고, **브라우저는 서버로부터 전달받은 HTML과 CSS를 단순히 렌더링** 하는 수준이었다

### 2.3.1 Ajax의 등장

- 1999년 **서버와 브라우저가 비동기 방식으로 데이터를 교환할 수 있는 기능**인 
Ajax가 XMLHttpRequest라는 이름으로 등장했다.

이전의 웹페이지는 웹페이지 전체를 렌더링하는 방식으로 동작하였는데, 이로인해 화면이 전환되면 서버로부터 새로운 HTML을 전송받아 웹페이지 전체를 처음부터 다시 렌더링 하였다.

이로인해 변경할 필요가 없는 부분까지 포함된 코드를 서버로부터 다시 전송받기 때문에 불필요한 데이터 통신이 발생, 변경할 필요가 없는 부분까지 다시 렌더링 되므로 성능면에서도 불리하였다.

하지만 Ajax의 등장으로 **웹페이지는 변경할 필요가 없는 부분은 다시 렌더링 하지 않고, 서버로부터 필요한 데이터만 전송받아 변경해야 하는 부분만 한정적으로 렌더링하는 방식**이 가능해졌다

### 2.3.2 jQuery의 등장

2006년 jQuery의 등장으로 다소 번거롭고 논라이 있던 DOM(Document Object Model)을 더욱 쉽게 제어가 가능하였고, **크로스 브라우징**(Cross Browsing)이슈도 어느 정도 해결이되었다. 배우기가 다소 까다로운 자바스크립트보다 배우기 쉽고 직관적인 jQuery를 더 선호하는 개발자가 양산되었다고도 한다. 
(실제로 필자는 자바스크립트보다 jQuery가 더 읽기 쉬웠고, 난이도도 매우 낮았음)

### 2.3.3 V8자바스크립트 엔진

자바스크립트로 웹 애플리케이션을 구축하려는 시도가 늘면서 더욱 빠르게 동작하는 자바스크립트 엔진의 필요성이 대두되었다. 이때 V8자바스크립트 엔진이 등장하였으며, 자바스크립트는 데스크톱 애플리케이션과 유사한 **UX(사용자 경험)을 제공할 수 있는 웹 애플리케이션 프로그래밍 언어로 정착**하게 되었다. 이로인한 발전으로 자바스크립트는 과거 웹 서버에서 수행되던 로직들이 대부분 브라우저(클라이언트)로 이동하게 되었다

### 2.3.4 Node.js

- Node.js는 **V8 자바스크립트 엔진으로 빌드된 자바스크립트 런타임 환경**이다

Node.js는 **브라우저의 자바스크립트 엔진에서만 동작하던 자바스크립트를 브라우저 이외의 환경에서도 동작할 수 있도록 자바스크립트 엔진을 브라우저에서 독립시킨 자바스크립트 실행 환경**이다. 

**비동기 I/O(입력과 출력)를 지원**하며 **단일 스레드 이벤트 루프 기반으로 동작**함으로써 요청 처리 성능이 좋다. 따라서 **데이터를 실시간으로 처리하기 위해 I/O가 빈번하게 발생하는 애플리케이션에 적합**하다.

### 2.3.5 SPA 프레임워크

자바스크립트가 발전함에 따라 보다 더 좋은 성능과 사용자 경험을 제공하는 것이 필수가 되었고, 그에 따라 개발 규모와 복잡도도 상승하였다. 이전의 개발 방식으로는 복잡해진 과정을 필요에 따라 많은 패턴과 라이브러리가 등장하였지만 변경에 유연하면서 확장하기 쉬운 애플리케이션 아키텍처의 구축을 어렵게 하였고, 이 때문에 프레임워크가 등장하게 되었다.

> # 2.4 자바스크립트와 ECMAScript

- 위에서 설명했다시피 ECMAScript는 자바스크립트의 표준사양을 말하며, 프로그램의 핵심 문법을 규정한다. 각 제조사는 ECMAScript 사양을 준수해서 브라우저에 내장되는 자바스크립트 엔진을 구현한다.

즉 자바스크립트는 일반적으로 ECMAScript를 아우르는 개념이다

> # 2.5 자바스크립트의 특징

- 자바스크립트는 **웹 브라우저에서 동작하는 유일한 프로그래밍 언어**다.

- 자바스크립트는 개발자가 별도의 컴파일 작업을 수행하지 않는 **인터프리터 언어**다.

- 자바스크립트는 명령형, 함수형, 프로토타입 기반 객체지향 프로그래밍을 지원하는 **멀티 패러다임 프로그래밍 언어**다
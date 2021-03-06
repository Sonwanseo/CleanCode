# Chapter 4. 주석

> 나쁜 코드에 주석을 달지 마라. 새로 짜라. - 브라이언 W. 커니핸, P.J.플라우거

잘 달린 주석은 그 어떤 정보보다 유용하다.
경속하고 근거 없는 주석은 코드를 이해하기 어렵게 만든다.
오래되고 조잡한 주석은 거짓과 잘못된 정보를 퍼뜨려 해악을 미친다.

프로그래밍 언어 자체가 표현력이 풍부하다면, 아니 우리에게 프로그래밍 언어를 치밀하게 사용해 의도를 표현할 능력이 있다면, 주석은 거의 필요하지 않으리라.

우리는 코드로 의도를 표현하지 못해, 그러니까 실패를 만회하기 위해 주석을 사용한다.
주석은 언제나 실패를 의미한다.

주석은 오래될수록 코드에서 멀어진다.
이유는 단순하다.
프로그래머들이 주석을 유지하고 보수하기란 현실적으로 불가능하다.

코드는 변화하고 진화한다.
일부가 여기서 저기로 옮겨지기도 한다.
불행하게도 주석이 언제나 코드를 따라가지는 못한다.

부정확한 주석은 아예 없는 주석보다 훨씬 더 나쁘다.
부정확한 주석은 독자를 현혹하고 오도한다.

진실은 한곳에만 존재한다.
바로 코드다.
코드만이 자기가 하는 일을 진실되게 말한다.

## 주석은 나쁜 코드를 보완하지 못한다

코드에 주석을 추가하는 일반적인 이유는 코드 품질이 나쁘기 때문이다.

표현력이 풍부하고 깔끔하며 주석이 거의 없는 코드가, 복잡하고 어수선하며 주석이 많이 달린 코드보다 훨씬 좋다.
자신이 저지를 난장판을 주석으로 설명하려 애쓰는 대신에 그 난장판을 깨끗이 치우는 데 시간을 보내라!

## 코드로 의도를 표현하라!

확실히 코드만으로 의도를 설명하기 어려운 경우가 존재한다.
불행히도 많은 개발자가 이를 코드는 훌륭한 수단이 아니라는 의미로 해석한다.

## 좋은 주석

어떤 주석은 필요하거나 유익하다.
정말로 좋은 주석은, 주석을 달지 않을 방법을 찾아낸 주석이다.

### 법적인 주석

때로는 회사가 정립한 구현 표준에 맞춰 법적인 이유로 특정 주석을 넣으라고 명시한다.

### 정보를 제공하는 주석

때로는 기본적인 정보를 주석으로 제공하면 편리하다.

가능하다면, 함수 이름에 정보를 담는 편이 더 좋다.

### 의도를 설명하는 주석

때때로 주석은 구현을 이해하게 도와주는 선을 넘어 결정에 깔린 의도까지 설명한다.

### 의도를 명료하게 밝히는 주석

때때로 모호한 인수나 반환값은 그 의미를 읽기 좋게 표현하면 이해하기 쉬워진다.
일반적으로는 인수나 반환값 자체를 명확하게 만들면 더 좋겠지만, 인수나 반환값이 표준 라이브러리나 변경하지 못하는 코드에 속한다면 의미를 명료하게 밝히는 주석이 유용하다.

### 결과를 경고하는 주석

때로 다른 프로그래머에게 결과를 경고할 목적으로 주석을 사용한다.

### TODO 주석

때로는 '앞으로 할 일'을 //TODO 주석으로 남겨두면 편하다.

TODO 주석은 프로그래머가 필요하다 여기지만 당장 구현하기 어려운 업무를 기술한다.
하지만 어떤 용도로 사용하든 시스템에 나쁜 코드를 남겨 놓는 핑계가 되어서는 안 된다.

요즘 나오는 대다수 IDE는 TODO 주석 전부를 찾아 보여주는 기능을 제공하므로 주석을 잊어버릴 염려는 없다.

### 중요성을 강조하는 주석

자칫 대수롭지 않다고 여겨질 뭔가의 중요성을 강조하기 위해서도 주석을 사용한다.

### 공개 API에서 Javadocs

설명이 잘 된 공개 API는 참으로 유용하고 만족스럽다.
표준 자바 라이브러리에서 사용한 Javadocs가 좋은 예다.

공개 API를 구현한다면 반드시 훌륭한 Javadocs를 작성한다.

## 나쁜 주석

대다수 주석이 이 범주에 속한다.

### 주절거리는 주석

특별한 이유 없이 의무감으로 혹은 프로세스에서 하라고 하니까 마지못해 주석을 단다면 전적으로 시간낭비다.

### 같은 이야기를 중복하는 주석

주석이 코드보다 더 많은 정보를 제공하지 못한다.

### 오해할 여지가 있는 주석

때때로 의도는 좋았으나 프로그래머가 딱 맞을 정도로 엄밀하게는 주석을 달지 못하기도 한다.

### 의무적으로 다는 주석

모든 함수에 Javadocs를 달거나 모든 변수에 주석을 달아야 한다는 규칙은 어리석기 그지없다.
이런 주석은 코드를 복잡하게 만들며, 거짓말을 퍼뜨리고, 혼동과 무질서를 초래한다.

### 이력을 기록하는 주석

때때로 사람들은 모듈을 편집할 때마다 모듈 첫머리에 주석을 추가한다.

### 있으나 마나 한 주석

때때로 있으나 마나 한 주석을 접한다.
쉽게 말해, 너무 당연한 사실을 언급하며 새로운 정보를 제공하지 못하는 주석이다.

있으나 마나 한 주석을 달려는 유혹에서 벗어나 코드를 정리하라.
더 낫고, 행복한 프로그래머가 되는 지름길이다.

### 무서운 잡음

때로는 Javadocs도 잡음이다.

### 함수나 변수로 표현할 수 있다면 주석을 달지 마라

주석이 필요하지 않도록 코드를 개선하는 편이 좋다.

### 위치를 표시하는 주석

때때로 프로그래머는 소스 파일에서 특정 위치를 표시하려 주석을 사용한다.

### 닫는 괄호에 다는 주석

때로는 프로그래머들이 닫는 괄호에 특수한 주석을 달아놓는다.
중첩이 심하고 장황한 함수라면 의미가 있을지도 모르지만 작고 캡슐화된 함수에는 잡음일 뿐이다.
그러므로 닫는 괄호에 주석을 달아야겠다는 생각이 든다면 대신에 함수를 줄이려 시도하자.

### 공로를 돌리거나 저자를 표시하는 주석

소스 코드 관리 시스템은 누가 언제 무엇을 추가했는지 귀신처럼 기억한다.
저자 이름으로 코드를 오염시킬 필요가 없다.

### 주석으로 처리한 코드

주석으로 처리한 코드만큼 밉살스러운 관행도 드물다.

주석으로 처리된 코드는 다른 사람들이 지우기를 주저한다.
이유가 있어 남겨놓았으리라고, 중요하니까 지우면 안 된다고 생각한다.

### HTML 주석

소스 코드에서 HTML 주석은 혐오 그 자체다.
HTML 주석은 편집기/IDE에서조차 읽기가 어렵다.
도구로 주석을 뽑아 웹 페이지에 올릴 작정이라면 주석에 HTML 태그를 삽입해야 하는 태그를 삽입해야 하는 책임은 프로그래머가 아니라 도구가 져야 한다.

### 전역 정보

주석을 달아야 한다면 근처에 있는 코드만 기술하라.
코드 일부에 주석을 달면서 시스템의 전반적인 정보를 기술하지 말라.

### 너무 많은 정보

주석에다 흥미로운 역사나 관련 없는 정보를 장황하게 늘어놓지 마라.

### 모호한 관계

주석과 주석이 설명하는 코드는 둘 사이 관계가 명백해야 한다.
이왕 공들여 주석을 달았다면 적어도 독자가 주석과 코드를 읽어보고 무슨 소린지 알아야 하지 않겠는가?

주석을 다는 목적은 코드만으로 설명이 부족해서이다.

### 함수 헤더

짧은 함수는 긴 설명이 필요 없다.
짧고 한 가지마 수행하며 이름을 잘 붙인 함수가 주석으로 헤더를 추가한 함수보다 훨씬 좋다.

### 비공개 코드에서 Javadocs

공개 API는 Javadocs가 유용하지만 공개하지 않을 코드라면 Javadocs는 쓸모가 없다.
시스템 내부에 속한 클래스와 함수에 Javadocs를 생성할 필요가 없다.
유용하지 않을 뿐만 아니라 Javadocs 주석이 요구하는 형식으로 인해 코드만 보기 싫고 산만해질 뿐이다.

### 예제
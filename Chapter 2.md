# Chapter 2. 의미 있는 이름
---
## 들어가면서

소프트웨어에서 이름은 어디나 쓰인다.
우리는 변수에도 이름을 붙이고, 함수에도 이름을 붙이고, 인수와 클래스와 패키지에도 이름을 붙인다.
소스 파일에도 이름을 붙이고, 소스 파일이 담긴 디렉터리에도 이름을 붙인다.

## 의도를 분명히 밝혀라

변수나 함수 그리고 클래스 이름은 다음과 같은 굵직한 질문에 모두 답해야 한다.
변수(혹은 함수나 클래스)의 존재 이유는? 수행 기능은? 사용 방법은?

의도가 드러나는 이름을 사용하면 코드 이해와 변경이 쉬워진다.

## 그릇된 정보를 피하라

프로그래머는 코드에 그릇된 단서를 남겨서는 안된다.
그릇된 단서는 코드 의미를 흐린다.

예를 들어, 여러 계정을 그룹으로 묶을 때, 실제 List가 아니라면, accountList라 명명하지 않는다.
프로그래머에게 List라는 단어는 특수한 의미다.
그러므로 accountGroup, bunchOfAccounts, 아니면 단순히 Accounts라 명명한다.

서로 흡사한 이름을 사용하지 않도록 주의한다.

유사한 개념은 유사한 표기법을 사용한다.
이것도 정보다.
일관성이 떨어지는 표기법은 그릇된 정보다.

## 의미있게 구분하라

컴파일러나 인터프리터만 통과하려는 생각으로 코드를 구현하는 프로그래머는 스스로 문제를 일으킨다.

컴파일러를 통과할지라도 연속된 숫자를 덧붙이거나 불용어를 추가하는 방식은 적절하지 못하다.
이름이 달라야 한다면 의미도 달라져야 한다.

연속적인 숫자를 덧붙인 이름(a1, a2, ..., aN)은 의도적인 이름과 정반대다.
이런 이름은 그릇된 정보를 제공하는 이름도 아니며, 아무런 정보를 제공하지 못하는 이름일 뿐이다.
저자 의도가 전혀 드러나지 안흔ㄴ다.

함수 인수 이름으로 source와 destination을 사용한다면 코드 읽기가 훨씬 더 쉬워진다.

불용어는 중복이다.
변수 이름에 variable 이라는 단어는 단연코 금물이다.
표 이름에 table이라는 단어도 마찬가지다.

명확한 관례가 없다면 변수 moneyAmount는 money와 구분이 안 된다.
customerInfo는 customer와, accountData는 account와, theMessage는 message와 구분이 안 된다.
읽는 사람이 차이를 알도록 이름을 지어라.

## 발음하기 쉬운 이름을 사용하라

사람들은 단어에 능숙하다.
우리 두뇌에서 상당 부분은 단어라는 개념만 전적으로 처리한다.

발음하기 어려운 이름은 토론하기도 어렵다.

## 검색하기 쉬운 이름을 사용하라

문자 하나를 사용하는 이름과 상수는 텍스트 코드에서 쉽게 눈에 띄지 않는다는 문제점이 있다.

e라는 문자는 변수 이름으로 적합하지 못하다.
검색이 어려운 탓이다.
e는 영어에서 가장 많이 쓰이는 문자다.
검색하기 쉬운 이름이 상수보다 좋다.

개인적으로는 간단한 메서드에서 로컬 변수만 한 문자를 사용한다.
이름 길이는 범위 크기에 비례해야 한다.
변수나 상수를 코드 여러 곳에서 사용한다면 검색하기 쉬운 이름이 바람직하다.

이름을 의미 있게 지으면 함수가 길어진다.

## 인코딩을 피하라

굳이 부담을 더하지 않아도 이름에 인코딩할 정보는 아주 많다.
유형이나 범위 정보까지 인코딩에 넣으면 그만큼 이름을 해독하기 어려워진다.
대개 새로운 개발자가 익힐 코드 양은 상당히 많다.
여기다 인코딩 '언어'까지 익히라는 요구는 비합리적이다.
문제 해결에 집중하는 개발자에게 인코딩은 불필요한 정신적 부담이다.
인코딩한 이름은 거의가 발음하기 어려우며 오타가 생기기도 쉽다.

### 헝가리식 표기법

포트란은 첫 글자로 유형을 표현했다.
초창기 베이식은 글자 하나에 숫자 하나만 허용햇다.
헝가리식 표기법은 기존 표기법을 완전히 새로운 단계로 끌어올렸다.

요즘 나오는 프로그래밍 언어는 훨씬 많은 타입을 지원한다.
또한 컴파일러가 타입을 기억하고 강제한다.

자바 프로그래머는 변수 이름에 타입을 인코딩할 필요가 없다.
객체는 강한 타입이며, IDE는 코드를 컴파일하지 않고도 타입 오류를 감지할 정도로 발전했다.

### 멤버 변수 접두어

이제는 멤버 변수에 'm\_'이라는 접두어를 붙일 필요도 없다.
클래스와 함수는 접두어가 필요없을 정도로 작아야 마땅하다.

게다가 사람들은 접두어(또는 접미어)를 무시하고 이름을 해독하는 방식을 재빨리 익힌다.
코드를 읽을수록 접두어는 관심 밖으로 밀려난다.
결국은 접두어는 옛날에 작성한 구닥다리 코드라는 징표가 되버린다.

### 인터페이스 클래스와 구현 클래스

때로는 인코딩이 필요한 경우도 있다.
개인적으로 인터페이스 이름은 접두어를 붙이지 않는 편이 좋다고 생각한다.
옛날 코드에서 많이 사용하는 접두어 I는 주의를 흐트리고 과도한 정보를 제공한다.

## 자신의 기억력을 자랑하지 마라

독자가 코드를 읽으면서 변수 이름을 자신이 아는 이름으로 변환해야 한다면 그 변수 이름은 바람직하지 못하다.

문자 하나만 사용하는 변수 이름은 문제가 있다.
루프에서 반복 횟수를 세는 변수 i, j, k는 괜찮다.
단, 루프 범위가 아주 작고 다른 이름과 충돌하지 않을 때만 괜찮다.
루프에서 반복 횟수 변수는 전통적으로 한 글자를 사용하기 때문이다.

똑똑한 프로그래머와 전문가 프로그래머 사이에서 나타나는 차이점 하나만 들자면, 전문가 프로그래머는 명료함이 최고라는 사실을 이해한다.
전문가 프로그래머는 자신의 능력을 좋은 방향으로 사용해 남들이 이해하는 코드를 내놓는다.

## 클래스 이름

클래스 이름과 객체 이름은 명사나 명사구가 적합하다.
Manager, Processor, Data, Info 등과 같은 단어는 피하고, 동사는 사용하지 않는다.

## 메서드 이름

메서드 이름은 동사나 동사구가 적합하다.

생성자를 중복정의 할 때는 정적 팩토리 메서드를 사용한다.
메서드는 인수를 설명하는 이름을 사용한다.

생성자 사용을 제한하려면 해당 생성자를 private로 선언한다.

## 기발한 이름은 피하라

이름이 너무 기발하면 저자와 유머 감각이 비슷한 사람만, 그리고 농담을 기억하는 동안만, 이름을 기억한다.
재미나 이름보다 명료한 이름을 선택하라.

의도를 분명하고 솔직하게 표현하라.

## 한 개념에 한 단어를 사용하라

추상적인 개념 하나에 단어 하나를 선택해 이를 고수한다.

이클립스, 인텔리제이 등과 같은 최신 IDE는 문맥에 맞는 단서를 제공한다.
예를 들어, 객체를 사용하면 그 객체가 제공하는 메서드 목록을 보여준다.
하지만 목록은 보통 함수 이름과 매개변수만 보여줄 뿐 주석은 보여주지 않는다.
따라서 메서드 이름은 독자적이고 일관적이어야 한다.

## 말장난을 하지 마라

한 단어를 두 가지 목적으로 사용하지 마라.
다른 개념에 같은 단어를 사용한다면 그것은 말장난에 불과하다.

프로그래머는 코드를 최대한 이해하기 쉽게 짜야 한다.
집중적인 탐구가 필요한 코드가 아니라 대충 훑어봐도 이해할 코드 작성이 목표다.

## 해법 영역에서 가져온 이름을 사용하라

코드를 읽을 사람도 프로그래머라는 사실을 명심한다.
그러므로 전상 용어, 알고리즘 이름, 패턴 이름, 수학 용어 등을 사용해도 괜찮다.

## 문제 영역에서 가져온 이름을 사용하라

적절한 '프로그래머 용어'가 없다면 문제 영역에서 이름을 가져온다.
그러면 코드를 보수하는 프로그래머가 분야 전문가에게 의미를 물어 파악할 수 있다.

우수한 프로그래머와 설계자라면 해법 영역과 문제 영역을 구분할 줄 알아야 한다.
문제 영역 개념과 관련이 깊은 코드라면 문제 영역에서 이름을 가져와야 한다.

## 의미 있는 맥락을 추가하라

스스로 의미가 분명한 이름이 없지 않다.
하지마 대다수 이름은 그렇지 못하다.
그래서 클래스, 함수, 이름 공간에 넣어 맥락을 부여한다.
모든 방법이 실패하면 마지막 수단으로 접두어를 붙인다.

## 불필요한 맥락을 없애라

'고급 휘발유 충전소'라는 애플리케이션을 짠다고 가정하자.
모든 클래스 이름을 GSD로 시작하겠다는 생각은 전혀 바람직하지 못하다.

일반적으로는 짧은 이름이 긴 이름보다 좋다.
단, 의미가 분명한 경우에 한해서다.
이름에 불필요한 맥락을 추가하지 않도록 주의한다.

## 마치면서

좋은 이름을 선택하려면 설명 능력이 뛰어나야 하고 문화적인 배경이 같아야 한다.
좋은 이름을 선택하는 능력은 기술, 비즈니스, 관리 문제가 아니라 교육 문제다.
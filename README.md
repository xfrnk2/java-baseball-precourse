### 1주차 미션　
# 숫자 야구 게임
![Code: Java](https://img.shields.io/badge/code-java-orange)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)



## ⚾️ 요구조건

+ 프로그램은 1에서부터 9까지의 각각의 자릿수가 서로 다른 세 자리 난수를 생성해야 한다.
  사용자가 입력하는 수는 1에서부터 9까지의 수이며 0은 포함되지 않는다.
+ 프로그램은 사용자에게 두 숫자간 비교 결과를 바탕으로 힌트를 제공하는데, 같은 자릿수가 일치하면 스트라이크, 그렇지 않고 다른 자릿수에 해당 숫자를 포함하고 있으면 볼이다.
+ 제공되는 힌트는 스트라이크와 볼이 각각 0일 경우 "낫싱", 하나만 만족하는 경우"X볼" 또는 "X스트라이크", 둘 다 만족하는 경우 "X볼 X스트라이크" 형태로 힌트를 제공한다. (X는 임의의 횟수)
+ 만약 모든 수가 일치하여 "3스트라이크"가 되면 게임을 종료하는데, 이 때 재시작을 원하는지, 종료를 원하는지 사용자에게 물어본다.
+ 사용자는 1(재시작한다) 또는 2(종료한다)로 프로그램에게 알려준다.
+ 프로그램은 각각의 결과에 따라 요청 동작을 수행하도록 한다.


　
## ⚾️ 구현할 기능 목록

+ n개의 임의의 난수를 요구 조건에 맞게 생성하는 기능 **( n = 3)**

+ 사용자 입력이 유효한지 식별하고, 요구 조건을 만족하지 않거나 잘못된 값일 때 에러를 발생시키는 기능

+ 같은 길이의 두 수를 비교하여 특정 자릿수 일치 또는 상대의 해당 숫자 포함 여부 따라 “스트라이크” 또는 “볼”의 횟수를 계산하는 기능

+ 같은 길이의 두 수에 대한 비교 결과를 바탕으로 힌트를 출력하는 기능

+ 게임 종료 조건을 만족할 때까지 반복하는 기능

+ 게임 종료 조건 만족시 재시작 또는 종료여부를 판별하는 기능


　
## ⚾️ 예외 처리

+ 생성시킨 n자리 임의의 난수에 대하여 각각의 자릿수가 서로 다른 수가 아닌 경우 예외 발생

+ 사용자 입력으로 받은 n자리의 임의의 수가 정수가 아니거나, 0을 포함하는 경우 예외 발생

+ 볼 횟수의 합계와 스트라이크 횟수의 합계가 각각 n개를 초과하거나 게임의 전제에 어긋나는 경우 예외 발생

+ 게임 종료 조건 만족시 재시작 또는 종료 여부를 묻는 사용자 입력에 대하여 유효한 명령인지 검사하여 그렇지 못한 경우 예외 발생


　
## ⚾️ 상수 분류

+ 시스템 메시지를 별도의 상수로 보관

+ 힌트 메시지를 별도의 상수로 보관

+ 재시작 또는 종료 커맨드를 별도의 상수로 보관

+ 요구 조건을 따르는 숫자의 속성을 별도의 상수로 보관


　
## ⚾️ 테스트 케이스

+ 요구 조건을 따르는 n 자리 난수 생성 테스트

+ 사용자 숫자 입력 검사 테스트

+ 스트라이크 카운팅 테스트

+ 볼 카운팅 테스트

+ 재시작 및 종료 여부 판별 사용자 입력 검사 테스트


　
## ⚾️ 최종 디렉토리 구조
```
└─java-baseball-precourse
    │
└─src
    ├─main
    │  └─java
    │      ├─baseball
    │      │      Application.java
    │      │      Game.java
    │      │      Umpire.java
    │      │
    │      ├─constants
    │      │      ExitOption.java
    │      │      HintMessage.java
    │      │      NumberAttribute.java
    │      │      SystemMessage.java
    │      │
    │      └─utils
    │              InputValidator.java
    │              NumberGenerator.java
    │
    └─test
        └─java
            └─baseball
                    ApplicationTest.java
                    GameTest.java
                    InputValidatorTest.java
                    NumberGeneratorTest.java
```
  　


## ✔️ 실행 환경

> JDK 8 (ver 1.8)
> Gradle 5.4.1 +



## ✔️ 코딩컨벤션 검사 도구
**This project follows [hackday-conventions-java](https://github.com/naver/hackday-conventions-java/blob/master/rule-config/naver-checkstyle-rules.xml)**
#### mac or linux

> ./gradlew check

#### windows

> gradlew.bat check






## ✔️ 테스트 도구
#### mac or linux

> ./gradlew clean test

#### windows

> gradlew.bat clean test






## 📝 License

This project is [MIT](https://github.com/woowacourse/java-baseball-precourse/blob/master/LICENSE) licensed.

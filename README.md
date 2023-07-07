# kotlin-lotto

## 🚀 Step 2 - 로또(자동)

### 기능 요구사항

- 로또 구입 금액을 입력하면 구입 금액에 해당하는 로또를 발급해야 한다.
- 로또 1장의 가격은 1000원이다.

### 기능 목록

- [ ] 로또 머신은 구입 금액을 받아 로또 티켓을 발급한다.
- [ ] 구입 금액에 맞게 로또티켓을 발급한다.
  - [ ] 로또 1장의 가격은 1000원이다.
  - [ ] 구입 금액이 1000원 미만인 경우 예외가 발생한다.
  - [ ] 구입 금액이 1000원 단위가 아닌 경우 예외가 발생한다.
- [X] 로또티켓은 로또 목록을 갖는다
  - [X] 로또 목록은 1개 이상의 로또를 갖는다.
  - [ ] 숫자 목록 여러개를 받아 로또 티켓을 생성한다.
- [X] 로또는 6개의 로또 번호로 이루어진다.
  - [X] 아닌 경우 예외가 발생한다.
- [ ] 로또 번호는 자동으로 생성한다.
- [X] 로또 번호는 1 ~ 45 사이의 숫자이다.
  - [X] 범위를 벗어난 경우 예외가 발생한다. 
- [ ] 로또 번호는 중복될 수 없다.
- [ ] 당첨 번호는 6개의 로또 번호로 이루어진다.
  - [ ] 로또 번호를 비교하여 일치하는 개수를 반환한다.
- [ ] 일치하는 개수에 따라 당첨 금액을 반환한다.
  - [ ] 3개 일치: 5000원
  - [ ] 4개 일치: 50000원
  - [ ] 5개 일치: 1500000원
  - [ ] 6개 일치: 2000000000원
- [ ] 수익률을 계산한다.
  - [ ] 수익률 = (당첨 금액 - 구입 금액) / 구입 금액

### 프로그래밍 요구 사항

- 핵심 로직을 구현하는 코드와 UI를 담당하는 로직을 구분한다.
    - 핵심 로직은 TDD로 구현
    - 단위 테스트가 존재해야 한다.
- indent(인덴트, 들여쓰기) depth를 1까지만 허용한다.
- 함수(또는 메서드)의 길이가 15라인을 넘어가지 않도록 구현한다.
- 함수(또는 메서드)가 한 가지 일만 잘 하도록 구현한다.
- 기능을 구현하기 전에 README.md 파일에 구현할 기능 목록을 정리해 추가한다.
- 기능 단위 커밋

## 🚀 Step 1 - 문자열 덧셈 계산기

### 기능 요구 사항

- 쉼표(,) 또는 콜론(:)을 구분자로 가지는 문자열을 전달하는 경우 구분자를 기준으로 분리한 각 숫자의 합을 반환
    - (예: "" => 0, "1,2" => 3, "1,2,3" => 6, "1,2:3" => 6)
- 앞의 기본 구분자(쉼표, 콜론) 외에 커스텀 구분자를 지정할 수 있다.
    - 커스텀 구분자는 문자열 앞부분의 "//"와 "\n" 사이에 위치하는 문자를 커스텀 구분자로 사용한다.
    - "//;\n1;2;3" -> 커스텀 구분자: 세미콜론(;), 결과 값: 6
- 문자열 계산기에 숫자 이외의 값 또는 음수를 전달하는 경우 RuntimeException 예외를 throw 한다.

### 기능 목록

- [X] 문자열은 숫자 또는 구분자(정의된 기호)로 이루어진다.
    - [X] 기본 구분자는 쉼표(,), 콜론(:)이다.
    - [X] 기호를 변경하려는 경우 문자열 앞부분의 "//"와 "\n" 사이에 위치하는 문자를 커스텀 구분자로 사용한다.
- [X] 문자열이 비어있는(null or empty) 경우 0을 반환한다.
- [X] 문자열이 하나의 숫자로 이루어진 경우 해당 숫자를 반환한다.
- [X] 숫자가 아니거나 음수인 경우 예외가 발생한다.
- [X] 요구사항을 만족하는 문자열인 경우 구분자로 구분한 각 숫자의 합을 반환한다.

### 프로그래밍 요구 사항

- 들여쓰기는 1번만 허용한다.
- 함수(또는 메서드)의 길이가 10라인을 넘어가지 않도록 구현한다.
- 함수(또는 메서드)가 한 가지 일만 잘 하도록 구현한다.

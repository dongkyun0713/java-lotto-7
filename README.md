# java-lotto-precourse

## model

### Lotto

- **정수형 숫자 리스트를 필드로 가지는 클래스**
    - [x] 로또 번호가 6개가 아니면 예외 발생
    - [x] 로또 번호를 오름차순으로 정렬하여 저장
    - [x] 필드를 반환하는 메서드 추가

### AttemptCount

- **구매 금액을 입력 받아 시도 횟수로 변환하는 클래스**
    - [x] 구매 금액을 시도 횟수로 변환
    - [x] 1,000원으로 나누어 떨어지지 않는 경우 예외 발생

### Lottos

- **로또를 관리하는 일급 컬렉션**
    - [x] `List<Lotto>` 필드로 다수의 로또를 관리
    - [x] 주어진 시도 횟수에 맞춰 로또 목록을 생성하는 메서드

### WinningNumber

- **당첨 번호를 관리하는 클래스**
    - [x] 번호의 범위가 기준 범위를 넘어서면 예외 발생
    - [x] 당첨 번호에 중복된 숫자가 있는 경우 예외 발생
    - [x] 번호의 범위가 1부터 45 사이가 아니면 예외 발생

### BonusNumber

- **보너스 번호를 관리하는 클래스**
    - [x] 당첨 번호와 중복되면 예외 발생
    - [x] 1부터 45 사이의 숫자가 아니면 예외 발생

### Rank

- **로또 게임의 당첨 순위를 관리하는 열거형 클래스**
    - [x] 각 순위별로 일치하는 번호 개수, 보너스 번호 필요 여부, 상금을 정의
    - [x] 매칭 개수와 보너스 여부를 기반으로 Rank를 결정하는 기능

### LottoManager

- **로또 시스템을 관리하는 클래스**
    - [x] `AttemptCount`를 바탕으로 `Lottos`를 생성하여 관리
    - [x] 당첨 및 보너스 번호를 통해 로또 결과를 반환하는 메서드
    - [x] 로또 결과 통계를 생성하고 관리하는 메서드

## validator

### InputValidator

- **사용자 입력을 검증하는 클래스**
    - [x] 구매 금액 검증
    - [x] 당첨 번호 형식 검증
    - [x] 보너스 번호 검증

## utility

### GenerateRandomNumbers

- **범위에 맞는 랜덤 번호 리스트를 반환하는 유틸 클래스**
    - [x] 랜덤 리스트 생성 및 반환

### RetryUtil

- **입력을 재시도할 수 있는 유틸 클래스**
    - [x] 구매 금액 재입력
    - [x] 당첨 번호 재입력
    - [x] 보너스 번호 재입력

## dto

### LottoDTO

- **로또 번호 정보를 담는 DTO**
    - [x] 로또 번호를 반환하는 정적 팩토리 메서드 추가

### LottosDTO

- **로또 목록 정보를 담는 DTO**
    - [x] `List<LottoDTO>`를 필드로 가짐
    - [x] `Lottos` 객체에서 변환하는 메서드 추가

### LottoResultDTO

- **로또 결과 정보를 담는 DTO**
    - [x] 매칭된 번호 개수, 상금, 당첨 통계 등을 담는 필드 추가
    - [x] Rank 데이터를 DTO로 변환하는 메서드 추가

## view

### InputView

- **사용자 입력 담당**
    - [x] 구입 금액 입력
    - [x] 당첨 번호 입력
    - [x] 보너스 번호 입력

### OutputView

- **출력 담당**
    - [x] 생성된 로또 번호 결과 출력
    - [x] 당첨 통계 결과 출력

## controller

### LottoController

- **모델과 뷰를 연결하는 컨트롤러**
    - [x] 사용자의 입력을 받아 모델에 전달하고, 결과를 뷰에 전달

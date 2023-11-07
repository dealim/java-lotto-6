## 🚀 기능 요구 사항

- [ ] 로또 게임 기능을 시작한다
    - LottoGame.start()
    - LottoGame.isGaming : 게임 중임을 나타내는 boolean 변수
- [x] 로또 구입 금액을 입력한다. 잘못 입력할시 다시 입력하도록 한다.
    - LottoGame.money: 구입한 총 금액
    - LottoGame.inputMoney() : 로또를 위해 돈 넣기
- [x] 로또 구입 금액을 입력 받는다. 구입 금액은 1,000원 단위로 입력 받으며 1,000원으로 나누어 떨어지지 않는 경우 예외 처리한다.
    - LottoGame.validateThousandWonUnits() : 입력값이 천원 단위인지 검증
- [ ] 금액만큼 로또 티켓을 발행한다. 로또 1장의 가격은 1,000원이다.
    - LottoGame.lottoTickets<Lotto> : 구입된 로또 티켓 리스트(로또 객체)
    - LottoGame.generateLottoTickets() : 입력된 금액에 따라 로또 티켓 발행하기
- [ ] 로또 번호의 숫자 범위는 1~45까지이다, 1개의 로또를 발행할 때 중복되지 않는 6개의 숫자를 뽑는다.
    - LottoGame.winningNumbers : 당첨 번호
    - LottoGame.pickWinningNumbers() : 당첨 번호 뽑기
        - pickUniqueNumbersInRange(1, 45, 6)
    - 1개의 로또 티켓을 발행 > Lotto 객체 구성필요
- [ ] 당첨 번호 추첨 시 중복되지 않는 숫자 6개와 보너스 번호 1개를 뽑는다.
    - LottoGame
    - LottoGame.pickBonusNumber()
        - pickUniqueNumbersInRange(1, 45, 1)
- [ ] 당첨은 1등부터 5등까지 있다. 당첨 기준과 금액은 아래와 같다.
    ```
    1등: 6개 번호 일치 / 2,000,000,000원
    2등: 5개 번호 + 보너스 번호 일치 / 30,000,000원
    3등: 5개 번호 일치 / 1,500,000원
    4등: 4개 번호 일치 / 50,000원
    5등: 3개 번호 일치 / 5,000원
    ```
    - LottoGame.getLottoRank() : 숫자를 입력받아 등수를 판별
    - LottoGame.getMoneyForRank() : 등수를 입력받아 당첨금액을 반환
- [ ] 당첨 번호와 보너스 번호를 입력받는다.
    - Lotto.inputNumbers()
    - Lotto.inputBonusNumber()
- [ ] 사용자가 구매한 로또 번호와 당첨 번호를 비교하여 당첨 내역 및 수익률을 출력하고 로또 게임을 종료한다.
    - LottoGame.printResult()
    - LottoGame.getRateOfReturn()
    - LottoGame.getWinningHistory()
    - LottoGame.end()
- [ ] 사용자가 잘못된 값을 입력할 경우 `IllegalArgumentException`를 발생시키고, "[ERROR]"로 시작하는 에러 메시지를 출력 후 그 부분부터 입력을 다시 받는다.
    ```
    Exception`이 아닌 `IllegalArgumentException`, `IllegalStateException` 등과 같은 명확한 유형을 처리한다.
    ```
    - Lotto.validate() : LottoGame이 아닌 Lotto 객체가 입력받을때 직접 검증하고 출력
- [ ] Enum을 사용하여 문자열, 숫자등의 값은 상수로 관리
    - Constant Enum 생성

---

## ✏️ 과제 진행 요구 사항

- [x] 미션은 [java-lotto-6](https://github.com/woowacourse-precourse/java-lotto-6) 저장소를 Fork & Clone해 시작한다.
- [x] **기능을 구현하기 전 `docs/README.md`에 구현할 기능 목록을 정리**해 추가한다.
- [x] **Git의 커밋 단위는 앞 단계에서 `docs/README.md`에 정리한 기능 목록 단위**로 추가한다.
    - [커밋 메시지 컨벤션](https://gist.github.com/stephenparish/9941e89d80e2bc58a153) 가이드를 참고해 커밋 메시지를 작성한다.
- [x] 과제 진행 및 제출 방법은 [프리코스 과제 제출](https://github.com/woowacourse/woowacourse-docs/tree/master/precourse) 문서를 참고한다.
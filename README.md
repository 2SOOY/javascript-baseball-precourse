# ⚾ 미션 - 숫자 야구 게임

## 🎯 구조

```sh
├── index.html
└── src
    ├── index.js
    ├── Components
    │   └── App.js
    └── utils
        ├── constants.js
        ├── gameUtil.js
        └── validations.js
```

## 🎯 요구사항

### 📌 게임 시나리오

1. 게임이 시작되면 컴퓨터는 랜덤으로 3자리 숫자 생성
   - bindEvents(), generateTargetNumbers()
   - 클릭 및 키보드 이벤트 등록
   - state 값 초기화
2. 사용자는 Input에 임의의 3자리 숫자를 입력
   - 키보드 `Enter` 와 마우스 `click`를 통해 제출 가능
3. 컴퓨터는 Input에 대한 적절한 처리 진행
   - 입력에 대한 에러 처리
     - 숫자 X, 3자리 숫자 X, 중복된 숫자 O
4. Target과 다르다면 컴퓨터는 적절한 Hint 제공
   - play(), setState(), render(), getHint()
   - 스트라이크 : 숫자 & 자리수 동일
   - 볼 : 숫자만 존재
   - 낫싱 : 아무것도 해당 X
   - `볼, 스트라이크` 순으로
5. 숫자를 맞췄다면 게임 종료
   - 정답 메시지 출력과 함께 재시작 버튼 생성
   - 추가로 정답 제출 버튼 `비활성화`
6. 게임 종료시 재시작 버튼 생성 및 재시작 가능
   - restart()
   - 입력 창에 자동으로 `foucs` 되도록 설정

### 📌 세부 요구사항

- [x] JS 코딩 컨벤션 지키기
- [x] indent depth `2`까지 허용
- [x] 함수(또는 메소드)는 한 가지 역할만 수행하도록 설계
- [x] 생성된 숫자는 `서로 다른 수`로 이뤄져야 함 (숫자는 1 ~ 9)
- [x] 사용자의 잘못된 입력 => `alert` 이용해 처리
- [x] 힌트로 볼과 스트라이크가 제공될 경우 `볼 -> 스트라이크` 순으로 ex) 1볼 1스트라이크
- [x] 재시작 버튼의 id는 `game-restart-button`
- [x] `play(컴퓨터 랜덤값, 유저 입력값) -> String` 형태로 메소드 구현

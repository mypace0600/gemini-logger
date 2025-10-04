# Gemini Logger

Gemini Logger는 **Google Gemini API**를 이용한 간단한 CLI 대화 프로그램입니다.  
사용자의 입력을 받아 AI가 응답하며, 대화 기록은 **숨김 폴더에 저장**되고 종료 시 원하는 위치로 복사됩니다.


## ⚡ 기능
- 대화식 CLI 인터페이스
- AI 응답 자동 생성 (Gemini API 사용)
- 로그 저장
  - 숨김 폴더: `~/.gemini-logger/dialogues.txt`
  - 종료 시 보이는 폴더: `~/GeminiLogs/dialogues.txt`
- 경고 메시지 무시 (경고 로그 안 보임)
- 안전하게 API 키 환경 변수로 관리


## 💻 설치 및 실행

### 1. Python 3 설치 확인
```bash
python3 --version
````

### 2. 필요한 라이브러리 설치

```bash
pip install google-generativeai
# 선택적으로 absl 설치 (경고 로그 관리용)
pip install absl-py
```

### 3. 환경 변수 설정

```bash
export GEMINI_API_KEY="여기에_발급받은_API_KEY_입력"
```

### 4. 스크립트 실행

```bash
./gemini-logger
```

* 대화 시작 후 `exit` 또는 `quit` 입력 시 종료
* 종료 시 로그가 `~/GeminiLogs/dialogues.txt`로 복사됨


## 📂 로그 위치

| 구분     | 경로                               |
| ------ | -------------------------------- |
| 숨김 로그  | `~/.gemini-logger/dialogues.txt` |
| 보이는 로그 | `~/GeminiLogs/dialogues.txt`     |


## ⚙️ 사용 예시

```text
=== Gemini Logger ===
Type your message and press Enter. Type 'exit' to quit.

You: 안녕, Gemini!
AI: 안녕하세요! 무엇을 도와드릴까요?

You: 오늘 날씨 어때?
AI: 오늘은 맑고 화창할 것으로 예상됩니다.
```


## 📝 주의사항

* `GEMINI_API_KEY` 환경 변수를 반드시 설정해야 합니다.
* 로그 파일에는 개인 대화 내용이 저장되므로, 공유 시 주의하세요.
* Mac에서 `/Users/hyunsu/bin` 등 실행 파일 경로에 두고 CLI로 사용 가능.


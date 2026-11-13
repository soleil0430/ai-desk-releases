# AI 작업실 (ai-desk) 내려받기

AI 를 쓰는 동안 **기다리고, 놓치고, 쌓이는 것**을 맥 메뉴바 앱 하나가 챙깁니다. Claude·Codex 잔여량, 세션이 끝났거나 허락을 기다릴 때 알림, 화면 구석 캐릭터.

이 저장소에는 설치 파일만 있습니다.

## 필요한 것

- Apple Silicon 맥 (M1 이후), macOS 14 (Sonoma) 이상
- Claude Code 또는 Codex 를 설치하고 로그인해 둔 상태 (없으면 앱은 열리지만 보여 줄 것이 거의 없습니다)

## 설치 (터미널 한 줄, 추천)

터미널에 붙여 넣고 Enter. 받기 → 응용 프로그램 폴더에 넣기 → 켜기까지 한 번에 하고, 보안 경고도 뜨지 않습니다.

```bash
curl -fsSL https://github.com/soleil0430/ai-desk-releases/releases/latest/download/install.sh | bash
```

## 설치 (dmg)

터미널이 싫으면:

1. [ai-desk.dmg](https://github.com/soleil0430/ai-desk-releases/releases/latest/download/ai-desk.dmg) 를 받아 엽니다
2. 창에 보이는 `AI 작업실` 아이콘을 옆의 **Applications** 폴더로 끌어다 놓습니다
3. 응용 프로그램 폴더에서 앱을 엽니다. "Apple 에서 확인할 수 없습니다" 창이 뜨면 **완료**를 누릅니다
4. **시스템 설정 → 개인정보 보호 및 보안** 아래쪽 "AI 작업실" 옆 **그래도 열기**를 누르고, 암호를 넣은 뒤 다시 **그래도 열기** (처음 한 번만. Apple 유료 서명이 없어서 필요합니다)

## 처음 실행

처음 안내를 따라갑니다.

- 키체인 창이 뜨면 로그인 암호를 넣고 **항상 허용**을 누릅니다 (Claude 잔여량 조회용)
- 세션 알림 연결에 동의하면 `~/.claude/settings.json`, `~/.codex/hooks.json` 에 알림 명령이 들어갑니다 (원본은 `.ai-desk-backup` 으로 남음)

## 업데이트

새 버전이 나오면 앱이 하루 한 번 확인 창으로 알립니다. **지금 업데이트**를 누르면 앱이 바뀌고 다시 켜집니다. **나중에**를 누르면 다음 날 다시 묻고, 그 사이에는 메뉴바 패널 아래 **업데이트** 버튼으로 할 수 있습니다.

## 삭제

설정 → 연결 → **연결 끊기**로 훅을 지운 뒤, 앱을 휴지통으로 보내고 `~/Library/Application Support/ai-desk` 를 지웁니다.

## 주의 사항

- 잔여량은 공개 문서에 없는 주소로 조회합니다. 서비스 쪽 변경으로 언제든 멈출 수 있습니다
- 이 맥의 로그인 토큰(Claude 는 키체인, Codex 는 `~/.codex/auth.json`)을 읽어 해당 서비스의 조회 주소로만 보냅니다
- 정리 기능은 언제나 휴지통으로 보냅니다

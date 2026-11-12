# one-page-report — 한 장 보고서 스킬

회의 메모·업무 메모를 넣으면 **늘 같은 형식의 한 장 보고서를 Word(.docx) 파일로** 만들어 주는 AI 스킬입니다.
코드나 설치할 프로그램 없이, 지시문(`SKILL.md`)과 양식 파일만으로 이루어져 있습니다.

## 무엇을 해 주나요

메모를 아래 순서의 보고서로 바꿔 A4 한 장짜리 Word 파일로 줍니다.

```
[보고 종류] 제목
보고일 | 작성 | 보고 대상
■ 한 줄 요약   ■ 1. 배경   ■ 2. 주요 내용
■ 3. 이슈 · 리스크   ■ 4. 다음 단계   ※ 확인 필요
```

- 결론을 맨 앞에, 개조식(~함 · ~임)으로 씁니다.
- 메모에 없는 숫자·날짜·이름은 만들지 않고, 애매한 것은 '확인 필요'에 모읍니다.
- '내부용' 정보와 개인 연락처는 보고서에서 뺍니다.
- 보고받는 사람이나 보고 종류(결과 · 주간 · 검토)를 모르면 한 번만 묻습니다.
- "파일 없이"라고 하면 Word 파일 대신 채팅에 보고서를 보여줍니다.

예시는 [examples/example.md](examples/example.md)에 있습니다.

## 폴더 구조

```
one-page-report/
├ SKILL.md                   ← 이름 · 설명(언제 쓰는지) + 작업 순서
├ references/format.md       ← 보고서 양식 (작성할 때만 읽음)
├ references/word-format.md  ← Word 파일 서식 (저장할 때만 읽음)
└ examples/example.md        ← 메모 → 보고서 예시
```

## 설치

**ChatGPT** — 이 페이지에서 `Code → Download ZIP`으로 내려받은 뒤, 스킬 메뉴의 업로드에서 ZIP 파일을 그대로 올립니다.

**Claude (웹 · 데스크톱)** — 같은 ZIP 파일을 사이드바 `Customize` 메뉴에서 업로드합니다. 채팅에서는 `/` 또는 `+`로 불러 씁니다.

**Claude Code** — 터미널에서:

```bash
git clone https://github.com/katej5/one-page-report.git ~/.claude/skills/one-page-report
```

## 이렇게 씁니다

```
아래 메모로 본부장님께 올릴 결과 보고서 써줘.
(메모 붙여넣기)
```

"보고서 써줘", "주간 보고로 정리해줘", "한 장 보고서" 같은 말에 자동으로 켜집니다.

## 고쳐 쓰기

우리 팀 양식이 다르면 `references/format.md`를, 글꼴·크기 같은 Word 서식이 다르면 `references/word-format.md`를 고치면 됩니다. `SKILL.md`는 그대로 둬도 됩니다.

## 라이선스

[MIT](LICENSE)

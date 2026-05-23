# Equity Research Plugin

글로벌 주식 리서치를 위한 올인원 플러그인 — 국내외 종목의 전문 애널리스트 수준 분석을 지원합니다.

## 스킬 목록 (11개)

| 스킬 | 용도 | 출력 형식 |
|------|------|----------|
| `research-note` | 종목 리서치 노트 (커버리지 개시 포함) | Word (.docx) |
| `dcf-valuation` | DCF 밸류에이션 + 민감도 분석 | Excel (.xlsx) |
| `comps-analysis` | 피어 트레이딩 Comps 분석 | Excel (.xlsx) |
| `investment-memo` | Bull/Bear/Base 투자 메모 | Word (.docx) |
| `earnings-analysis` | 실적 발표 후 심층 분석 (컨콜 뉘앙스 포함) | Word (.docx) |
| `sector-analysis` | 섹터 종합 분석 (공급망·경쟁구도·밸류에이션) | Word (.docx) |
| `morning-note` | 장 시작 전 모닝노트 (매크로·뉴스·대응전략) | 채팅 |
| `event-calendar` | 이벤트 캘린더 (임상·실적·정책 일정) | Excel (.xlsx) |
| `earnings-preview` | 실적 발표 전 프리뷰 (서프라이즈/쇼크 확률) | Word (.docx) |
| `stock-screening` | 종목 발굴 (저평가·테마·퀄리티 스크리닝) | 채팅 |
| `sector-overview` | 섹터 개요 (공급망·경쟁구도·평균 멀티플) | 채팅 |

## 사용 예시

- "삼성전자 리서치 노트 써줘" → `research-note`
- "AAPL DCF 해줘, WACC 10%로" → `dcf-valuation`
- "2차전지 섹터 Comps 분석" → `comps-analysis`
- "오늘 모닝노트 작성해줘" → `morning-note`
- "다음 달 내 포트폴리오 이벤트 캘린더 만들어줘" → `event-calendar`
- "NVDA 실적 발표 전 프리뷰" → `earnings-preview`
- "실적 발표 후 분석: [실적 데이터 붙여넣기]" → `earnings-analysis`
- "AI 수혜 종목 발굴해줘 (나스닥)" → `stock-screening`
- "반도체 섹터 개요 알려줘" → `sector-overview`

## 대상 시장

- 국내: KOSPI, KOSDAQ
- 해외: NYSE, NASDAQ, 글로벌

## 출력 형식

- Word 문서: `docx` 스킬 필요
- Excel 모델: `xlsx` 스킬 필요
- 채팅 기반 스킬: 별도 스킬 불필요

## 주의사항

- 실시간 시장 데이터가 필요한 경우 사용자가 직접 붙여넣기 권장
- 재무 수치는 공개 자료 기반 — 최신 데이터는 직접 확인 필요
- 투자 권고가 아닌 분석 보조 도구로 활용

## 버전

v0.1.0 — 2026.05

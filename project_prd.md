# 학맞통 (hakmatong) PRD

## 1. 프로젝트 정의

**프로젝트명:** 학맞통 (hakmatong)
**목적:** 느린학습자를 돕는 활동가 교사들을 위한 AI 기반 심리상담 및 교육자료 지원 시스템
**운영 방식:** 사회공헌 자원봉사
**핵심 제약:** 경량, 단순, 저비용

---

## 2. 현재 상태

| 자료 | 형태 | 상태 |
|------|------|------|
| 활동가 일지 | 구글폼 | 운영 중 |
| 상담편지 | HTML | 완성 |
| 라포형성사례모음집 | HTML | 완성 |
| 미술심리감정분석 | 프로젝트 | 진행 중 |
| 상담 사례 자료집 | HTML | 완성 (책 1권 분량) |

---

## 3. 목표 시스템

### 기능 요구사항
- 개별 교사/아동에 대한 지속적·일관성 있는 AI 상담
- Torey Hayden 스타일의 전문적 글쓰기
- 자기존재감, 자기효능감 관점의 심리학적 분석
- 교육자료 자동 생성
- 1년 이상 누적 데이터 기반 개인화

### 비기능 요구사항
- 토큰 비용 최소화
- 로컬 실행 가능 (외부 서버 불필요)
- 민감 데이터 보호
- 유지보수 단순화

---

## 4. 기술 스택

| 역할 | 도구 | 비용 |
|------|------|------|
| Vector DB | Chroma | 무료 |
| LLM 보조 | Ollama + Gemma | 무료 |
| Framework | LangChain | 무료 |
| 프론트엔드 | 기존 HTML 재활용 | 무료 |
| 메인 AI | Claude Sonnet | 토큰 최적화 |
| 보조 AI | Claude Haiku | 저비용 |
| 서버 | 로컬 PC | 무료 |

### Claude 모델 사용 전략

| 작업 | 모델 | 이유 |
|------|------|------|
| 상담편지 작성 | Sonnet | 품질·감성 필요 |
| Torey Hayden 글쓰기 | Sonnet | 창의성 필요 |
| 심리 분석 보고서 | Sonnet | 전문성 필요 |
| RAG 검색·처리 | Haiku | 단순 작업 |
| 자료 분류·정리 | Haiku | 반복 작업 |
| 간단한 질문 응답 | Haiku | 비용 절감 |
| Opus | 미사용 | 비용 과다 |

---

## 5. 개발 단계

```
1. Design Thinking     ← 현재
2. PRD                 ← 이 문서
3. Plan / Architecture
4. Data Pipeline
5. Persona & Style Guide
6. SW 설계
7. Prototype / MVP
8. Ethics & Privacy
9. Deployment
10. Feedback & Iteration
```

---

## 6. 시스템 흐름 (계획)

```
기존 HTML 자료
      ↓
  Data Pipeline
      ↓
Chroma Vector DB
      ↓
  LangChain RAG
      ↓
  Claude API
(토큰 최적화)
      ↓
  교사에게 전달
(상담 / 교육자료)
```

---

## 7. 참고
- 작성일: 2026-05-03
- 작성: Claude Code + 학맞통 운영자

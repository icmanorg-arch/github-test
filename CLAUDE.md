# 학맞통 (hakmatong) 프로젝트

## 프로젝트 개요

느린학습자를 돕는 활동가 교사들을 위한 AI 기반 심리상담 및 교육자료 지원 시스템.
사회공헌 자원봉사 목적으로 운영되며, 경량·저비용·단순함을 최우선 원칙으로 한다.

## 핵심 원칙

- 가볍고 단순하게
- 비용 최소화 (무료 오픈소스 우선)
- 토큰 최적화 필수
- 개인정보 보호 (아동·상담 데이터)

## 글쓰기 스타일

- Torey Hayden(한아이 저자) 필체·문체·톤앤매너 기준
- 심리학적 접근: 자기존재감, 자기효능감 관점
- 따뜻하고 전문적인 상담 언어

## 보유 자료

- 구글폼 활동가 일지
- 상담편지.html
- 라포형성사례모음집.html
- 미술심리감정분석 프로젝트
- 상담 사례 자료집 (책 한 권 분량, HTML)

## 기술 스택 (계획)

- RAG + LangChain + Chroma (로컬 Vector DB)
- Ollama + Gemma (로컬 LLM, 무료)
- Claude Sonnet (상담·글쓰기 메인)
- Claude Haiku (단순·반복 작업 보조)
- 기존 HTML 재활용

## 모델 사용 원칙

- 상담편지, 글쓰기, 심리분석 → Sonnet
- RAG 처리, 분류, 단순응답 → Haiku
- Opus 미사용 (비용 과다)

## 개발 단계

1. Design Thinking (현재)
2. PRD
3. Plan / Architecture
4. Data Pipeline
5. Persona & Style Guide
6. SW 설계
7. Prototype / MVP
8. Ethics & Privacy
9. Deployment
10. Feedback & Iteration

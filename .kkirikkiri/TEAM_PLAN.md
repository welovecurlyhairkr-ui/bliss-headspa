# 팀 작업 계획

- 팀명: kkirikkiri-dev-0415
- 목표: BLISS HEADSPA 바우처 예약 플랫폼 — 프로젝트 세팅 + GitHub 연결 + 핵심 구조 구축
- 생성 시각: 2026-04-15
- 기획서: /Users/jakeshin/Downloads/bliss_headspa_planning_v1.1.docx

## 팀 구성
| 이름 | 역할 | 모델 | 담당 업무 |
|------|------|------|----------|
| team-lead | 팀장 | Opus | 계획/배분/검증/통합 |
| dev-backend | 개발자 1 | Opus | Convex 스키마, 함수, 인증 |
| dev-frontend | 개발자 2 | Opus | Next.js 프로젝트 세팅, 페이지/컴포넌트, UI |

## 기술 스택
- Frontend: Next.js 14+ (App Router) + Tailwind CSS + shadcn/ui
- Backend: Convex (BaaS - 서버리스 함수, 실시간 DB)
- 배포: Vercel + Convex Cloud
- 지도: Kakao Maps API
- SMS: NHN Cloud TOAST / Aligo

## 태스크 목록
- [ ] 태스크 1: Next.js + Convex 프로젝트 초기화 → dev-frontend
- [ ] 태스크 2: Convex 스키마 정의 (users, branches, vouchers, reservations) → dev-backend
- [ ] 태스크 3: Convex 함수 구현 (Query, Mutation, Action) → dev-backend
- [ ] 태스크 4: GitHub 레포 생성 + 초기 커밋 + push → dev-frontend
- [ ] 태스크 5: 핵심 페이지 구조 (레이아웃, 라우팅) → dev-frontend

## 주요 결정사항
(팀장이 결정할 때마다 여기에 기록)

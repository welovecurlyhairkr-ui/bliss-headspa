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
- [x] 태스크 1: Next.js + Convex 프로젝트 초기화 → dev-frontend ✅
- [x] 태스크 2: Convex 스키마 정의 (users, branches, vouchers, reservations, smsLogs) → dev-backend ✅
- [x] 태스크 3: Convex 함수 구현 (Query, Mutation, Action) → dev-backend ✅
- [x] 태스크 4: GitHub 레포 생성 + 초기 커밋 + push → dev-frontend ✅
- [x] 태스크 5: 핵심 페이지 구조 (레이아웃, 라우팅) → dev-frontend ✅

## 최종 검증 결과 (2026-04-15)

### 1. 빌드: PASS
- `npm run build` 성공 (Next.js 16.2.3 Turbopack)
- 11개 라우트 정상 생성

### 2. 스키마/함수: PASS
- 5개 테이블: users, branches, vouchers, reservations, smsLogs
- Convex 함수 파일: branches.ts, vouchers.ts, reservations.ts, users.ts, dashboard.ts, sms.ts
- 적절한 인덱스, 입력 검증, 비즈니스 로직 포함

### 3. GitHub: PASS
- 레포: https://github.com/welovecurlyhairkr-ui/bliss-headspa

### 4. 페이지 라우팅: PASS
- 고객: / (지점 목록), /reserve/[branchId] (예약)
- 어드민: /dashboard, /branches, /vouchers, /reservations
- 지점관리자: /my-branch
- 구매자: /my-vouchers
- 인증: /login

### 5. 수정사항 (팀장)
- tsconfig.json에 convex 디렉토리 exclude 추가 (Convex는 자체 빌드 파이프라인 사용, _generated 타입은 `npx convex dev` 시 생성)

## 주요 결정사항
- convex/ 디렉토리는 Next.js tsconfig exclude에 추가 (Convex 자체 빌드 시스템이 타입 체크 처리)
- voucher status는 "active" | "used" | "expired" | "cancelled" (기획서의 "issued"를 "active"로 변경)
- reservation status에 "pending" 추가 (기획서 외 추가)

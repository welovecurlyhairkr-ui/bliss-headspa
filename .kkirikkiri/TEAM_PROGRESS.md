# 진행 상황

## 2026-04-15
- [DONE] Task 1: Next.js + Convex 프로젝트 초기화 (dev-frontend)
  - Next.js 16 + TypeScript + Tailwind CSS + ESLint + App Router
  - Convex 설치 + 초기화 완료
  - shadcn/ui 초기화 완료
  - zustand, date-fns, lucide-react 설치 완료
  - ConvexClientProvider 생성 완료
  - npm run build 성공 확인
- [DONE] Task 2: Convex 스키마 정의 (dev-backend)
  - 5개 테이블: users, branches, vouchers, reservations, smsLogs
  - 적절한 인덱스 포함 (by_email, by_region, by_code, by_branch, by_status 등)
- [DONE] Task 3: Convex 함수 구현 (dev-backend)
  - branches.ts: list, getById, create, update, deactivate
  - vouchers.ts: validate, listByBuyer, issue, updateStatus, updateUsage
  - reservations.ts: getByBranch, getAvailableSlots, create, updateStatus
  - users.ts: create, update
  - dashboard.ts, sms.ts 추가 구현

## 최종 검증 (팀장)
- npm run build: PASS (11개 라우트 정상)
- tsconfig.json 수정: convex 디렉토리 exclude 추가 (Convex 자체 빌드 파이프라인 사용)
- 모든 팀원 shutdown 완료
- [DONE] Task 4: GitHub 레포 생성 + 연결 (dev-frontend)
  - https://github.com/welovecurlyhairkr-ui/bliss-headspa
  - main 브랜치 push 완료
- [DONE] Task 5: 핵심 페이지 구조 + 레이아웃 구축 (dev-frontend)
  - 고객: / (지점 리스트), /reserve/[branchId] (예약)
  - 관리자: /dashboard, /branches, /vouchers, /reservations
  - 지점관리자: /my-branch
  - 구매자: /my-vouchers
  - 로그인: /login

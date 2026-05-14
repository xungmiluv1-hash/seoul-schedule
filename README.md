# 서울인력 스케줄 관리 시스템

**배포:** https://seoul-schedule.vercel.app  
**기술 스택:** HTML + CSS + Vanilla JS + Leaflet.js  
**현재 버전:** v50

## 의료 통역사 자동 배정 시스템
병원별 환자 스케줄을 붙여넣으면 통역사를 자동으로 배정하고 카카오톡 공유용 텍스트를 복사할 수 있는 내부 도구

## 파일 구조
```
seoul-schedule/
├── index.html          ← 메인 앱 (단일 파일, ~330KB)
├── manifest.json       ← PWA 설정 (홈 화면 추가)
├── vercel.json         ← Vercel 배포 설정
├── CLAUDE.md           ← 개발 문서 (비즈니스 규칙, 아키텍처)
├── business-rules.md   ← 비즈니스 규칙 상세
├── changelog.md        ← 버전 히스토리
└── backups/            ← 로컬 백업 버전
    └── seoul-schedule-v50.html
```

## 다른 기기에서 개발 시작하기
```bash
git clone https://github.com/xungmiluv1-hash/seoul-schedule.git
cd seoul-schedule
# index.html 을 브라우저에서 열거나
# VS Code Live Server 등으로 실행
```

## 주요 기능 (v50)
- 🗓️ 월간 휴무 관리 + 직원 명단
- ⚡ 일일 배정 자동 생성 (언어별 통역사 점수 기반 배정)
- ⚡ 당일 예약 (임시 추가 환자 배정 추천)
- 📋 회의정보 (월 2회 회의록, rich text, Drive 내보내기)
- 🗺️ 지도 (Leaflet + Nominatim 주소 검색, 거리 측정)
- 📊 오늘 현황 대시보드 + 실시간 알림 (Supabase Realtime)
- 🟢 추가 출근 관리 (비번 직원 임시 출근)
- ☁️ Supabase 클라우드 동기화

## 환경 변수 / 설정
Supabase 설정은 앱 상단 ☁️ 버튼에서 URL과 anon key를 입력합니다.  
코드에 하드코딩된 기본값: `xkpmfmonkozievvokawx.supabase.co`

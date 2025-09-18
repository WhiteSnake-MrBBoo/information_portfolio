# HexaStay Admin – 호텔 관리 대시보드

<p align="center">
  <img src="../assets/hexastay-admin-overview.png" width="820" alt="HexaStay Admin Overview">
</p>

## 개요
Spring Boot 3.4 + Thymeleaf + MariaDB 기반 호텔 관리 관리자 대시보드.

## 문제 → 접근 → 성과
- **문제:** 예약/회원/객실 관리가 흩어져 있고 수동 작업 많음  
- **접근:** 모듈화된 CRUD + 공통 UI(공통 roomlist.html 재사용) + QR/메일 자동화  
- **성과:** 수정/알림 리드타임 단축, 프론트 유지보수성 향상

## 핵심 기능
- 룸/회원/예약 CRUD, 상태별 필터(체크인/체크아웃/표시/숨김)
- QR 인증 링크 발송, 예약 메일 본문 자동 구성(회원명/체크인·아웃/룸비번/QR)
- 모달 기반 검색·수정(@Query + Service(ModelMapper) + JSON 응답)

## 아키텍처
- **Backend:** Spring Boot 3.4, JDK21, ModelMapper, JPA, MariaDB, AWS  
- **Frontend:** Thymeleaf, Bootstrap 5  
- **공통 규칙:** Principal, 로그 포맷, CRUD 네이밍


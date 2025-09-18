# Excel → MariaDB “스키마 없이” 바로 저장

<p align="center">
  <img src="../assets/excel-importer-erd.png" width="820" alt="Excel Importer ERD">
</p>

## 개요
Excel 업로드만으로 테이블 생성/덮어쓰기, PK 타입 선택까지 지원.

## 문제 → 접근 → 성과
- **문제:** 비개발자 데이터 적재 장벽  
- **접근:** Controller→Service 분리, 테이블명 입력 시 존재/미존재 분기, PK 타입(INT/LONG) 선택  
- **성과:** 데이터 실험 속도↑, 운영 효율↑

## 핵심 기능
- 1열 PK 타입 변환, 예외 메시지 UI 반영
- 테이블 존재 시 덮어쓰기 / 없으면 생성
- 알림/실패 시나리오 명확화

## 기술 스택
Spring Boot, Apache POI(or EasyExcel), JDBC, MariaDB

## 실행(요약)
```bash
./gradlew bootRun

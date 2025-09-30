
<div align="center">
  <h1>JAVA · PYTHON · FLASK · Backend · AI_VISION · CV Engineer · LLM </h1>

  <!-- 스택 아이콘 (뱃지 벨트) -->
  <p align="center">
    <a href="https://www.java.com/"><img src="https://img.shields.io/badge/Java-ED8B00?logo=openjdk&logoColor=white" /></a><!--자바--> 
    <a href="https://spring.io/projects/spring-boot"><img src="https://img.shields.io/badge/Spring%20Boot-3.4-6DB33F?logo=springboot&logoColor=white" /></a>
    <a href="https://modelmapper.org/"><img src="https://img.shields.io/badge/ModelMapper-DI-FF6F00" /></a>    
    <a href="https://www.thymeleaf.org/"><img src="https://img.shields.io/badge/Thymeleaf-View-005F0F?logo=thymeleaf&logoColor=white" /></a>
    <a href="https://adoptium.net/temurin/releases/?version=21"><img src="https://img.shields.io/badge/JDK-21-007396?logo=java&logoColor=white" /></a><!--jdk21--> 
    <a href="https://mariadb.org/"><img src="https://img.shields.io/badge/MariaDB-Server-003545?logo=mariadb&logoColor=white" /></a>   
    <a href="https://github.com/ultralytics/ultralytics"><img src="https://img.shields.io/badge/YOLO-v11-222222" /></a><!--깃허브--> 
    <a href="https://www.kernel.org/"><img src="https://img.shields.io/badge/Linux-Server-FCC624?logo=linux&logoColor=black" /></a><!--라눅스-->
    <a href="https://www.python.org/"><img src="https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white" /></a><!--파이썬-->
    <a href="https://flask.palletsprojects.com/"><img src="https://img.shields.io/badge/Flask-Framework-000000?logo=flask&logoColor=white" /></a><!--Flask-->
    <a href="https://opencv.org/"><img src="https://img.shields.io/badge/OpenCV-Computer%20Vision-5C3EE8?logo=opencv&logoColor=white" /></a><br>
    <a href="https://www.uipath.com/"><img src="https://img.shields.io/badge/UiPath-VB.NET%20Invoke%20Code-FA4616?logo=uipath&logoColor=white" /></a>
    <a href="https://aws.amazon.com/"><img src="https://img.shields.io/badge/AWS-Cloud-232F3E?logo=amazon-aws&logoColor=white" /></a>
  </p>

  <p>
    <a href="README_en.md">English</a> ·
    <a href="mailto:mrbulsapabb@gmail.com">구글_Email</a> ·
    <!--<a href="https://www.linkedin.com/in/your-id">LinkedIn</a>-->  
  </p>
</div>

<!-- 빈 줄 하나 아래에도 둬야 함 -->
---

## 👋 TEAM 프로젝트
- 호텔 관리자용 ERP 생태계(HexaStay)**를 Spring Boot 3.4 + Thymeleaf +WEB Scocket(쌍방향)+ MariaDB로 구축/확장.
- 호텔객실 이용자_QR 인증·이메일 발송 + AI(인공 지능 인터페이스 구현) (고객용 UI/UX 구현)
- **SPRING BOOT : ModelMapper·Principal** 기반의 안정적인 백엔드 CRUD와 고급 **관리자 대시보드(UI/UX)** 설계.
- **YOLO + OpenCV**로 CCTV Vision AI 대시보드(영역 경보, 실시간 차트, 반응형 UI) 구현.
- **UiPath RPA**로 대용량 텍스트 요약/정리 파이프라인 구축(Invoke Code, JSON 파싱, Excel 출력 자동화).

---

## 🏆 대표 프로젝트
> 클릭 한 번에 “문제 → 접근 → 성과 → 기술 스택”이 보이도록 구성했습니다.
> > ### 더 자세한 내용은 이미지 클릭시**문서 상세페이지**로 연결됩니다.

### 1) HexaStay Admin – 호텔 관리 대시보드
**Stack:** Spring Boot 3.4, JDK 21, Thymeleaf, Bootstrap 5, MariaDB, ModelMapper, AWS, WEB Scocket(쌍방향)  
**핵심 기능:**  
- 객실/회원/예약 모듈, **QR 인증** & **이메일 발송**(예약 생성 시 자동 본문 구성: 회원명/체크인·아웃/룸비번/QR 링크)  
- 룸 상태별 리스트(체크인/체크아웃/표시/숨김) 필터, **공통 roomlist.html 재사용**  
- **모달 기반** 검색/수정(HotelRoom 이미지/메타 포함), @Query + Service(ModelMapper) + JSON 응답  

**성과(예시):**  
- 운영 인력의 수작업을 줄이고, 예약/수정/알림의 **단계 시간을 단축**
- QR 인증 절차를 통해 호텔객실 이용고객의 편의성 제공
- AI 추론 결과를 통해 이용 고객의 선택 편의성 등대
- 쌍방향 (WEB Socket)을 이용해사 객식 이용고객과 호텔 객실관리자와 실시간 알림 서비스 제공
- 단일 페이지 재사용 구조로 **프론트 유지보수성** 향상
> ### 이미지 클릭시 GIT 상세 설명 페이지로 이동

<!-- Card 1 -->
<div align="center">
  <a href="docs/hexastay-admin.md">
    <img src="assets/hexastay-admin-overview.png" alt="HexaStay Admin" width="820">
  </a>
</div>

---

### 2) CCTV Vision AI Dashboard
**Stack:** Python, Ultralytics YOLOv11, OpenCV, JS/Canvas(폴리곤), Threading(실시간/비동기), Flask/Socket.IO
**핵심 기능:**  
- 폴리곤 **Region** 기반 침입 카운팅, 실시간 경보(색상 단계: ALERT/WARN/SAFE/IDLE)  
- 반응형 UI + **실시간 그래프/차트** + **무제한 경보 패널**  
- 좌표 정규화, YOLO 결과 처리 함수화(테스트/확장 용이)

**성과(예시):**  
- 한 화면에서 **상황 인지** 및 **의사결정 속도** 개선  
- 영역 단위 경보로 **오탐/미탐 피드백 루프** 구축
- CCTV 객체 탐지의 영역의 다양한 장소에서 다변화 적용 가능
- 폴리곤 영역 안에 특정 클래스 객체만 탐지가능
> 활용영역의 확장 - 예시)산재 예방(폴리곤 영역에 탐지된 객체의 위험요소 경고), 특정 클래스만 탐지 통계데이터 데이터 구조화 

<!-- 시도 1: ./ 접두어 추가 (상대경로 명확화) -->
<!-- CCTV Vision AI Dashboard 카드 (영상 버전) -->

https://github.com/user-attachments/assets/cf991294-5b1c-45b3-a008-12115700f62c

---

[![CCTV_POLIGON_프로젝트_상세보기](https://img.shields.io/badge/CCTV_POLIGON_프로젝트_상세보기-FFFFFF?style=for-the-badge&logo=gitbook&logoColor=1B56FD)](https://github.com/WhiteSnake-MrBBoo/information_portfolio/blob/main/docs/cctv-vision-dashboard.md)


---

### 3) UiPath 리뷰 요약 자동화 파이프라인
**Stack:** UiPath, VB.NET Invoke Code, Newtonsoft JSON, Excel Activities  
**핵심 기능:**  
- Blind 리뷰 텍스트 → **긍/부정/결론** 3단 요약, **Dt_Blind_Ai_Result** 스키마 자동 구성  
- `choices[0].message.content`/`text` 안전 파싱, **MaxLength=-1** 처리, 오류 시 `Decision`에 JSON 기록  
- 대량 리뷰 입력 → **Excel 자동 출력**(WrapText, 열 너비 조정)
- ChatGPT (AI)을 활용 리뷰를 분석 추론 / 원하는 추론 결과를 도출

**성과(예시):**  
- 분석 리드타임 **단축** RPA
- 사내 리포팅 **반자동화**  - AI 을 통한 리뷰 분석 자동화
- EXCEL로 결과 데이터 로컬 저장 / 데이터 분석 및 데이터 활용에 용의성 증가
- 프롬프트 프리셋 & 파이프라인 표준화

https://github.com/user-attachments/assets/e8ea065c-bf0c-4f93-a32d-d476e298a9bf


---

[![RPA_기업리뷰_AI_SUMMARY_프로젝트_상세보기](https://img.shields.io/badge/RPA_기업리뷰_AI_SUMMARY_프로젝트_상세보기-0A66C2?style=for-the-badge&logo=openai&logoColor=white)](https://github.com/WhiteSnake-MrBBoo/information_portfolio/blob/main/docs/uipath-blind-review-pipeline.md)

---

### 4) Excel → MariaDB “스키마 없이” 바로 저장
**Stack:** Spring Boot, Apache POI(or EasyExcel), JDBC, MariaDB  
**핵심 기능:**  
- Excel 업로드 → **테이블명 입력 → 존재 시 덮어쓰기 / 미존재 시 생성**  
- **PK 타입 선택(INT/LONG)**, 첫 컬럼 자동 변환, 예외 메시지 UI 반영  
- Controller → Service 분리, 알림/실패 시나리오 명확화

**성과(예시):**  
- 비개발자도 **데이터 적재** 가능 / 샌드박스 테이블로 도메인 실험 가속

<!-- Card 4 -->
<div align="center">
  <a href="docs/excel-to-mariadb-importer.md">
    <img src="assets/excel-importer-erd.png" alt="Excel to MariaDB Importer" width="820">
  </a>
</div>

---

## 🧰 기술 스택
**Backend:** Spring Boot 3.4, JDK 21, Thymeleaf, ModelMapper, JPA, MariaDB, AWS  
**Vision/ML:** Ultralytics YOLOv5–v11, OpenCV, (Streamlit/Flask/Socket.IO)  
**RPA:** UiPath, VB.NET Invoke Code, Newtonsoft JSON, Excel Activities  
**Frontend:** Bootstrap 5, HTML5/CSS3/JS, jQuery/Ajax/Fetch  
**DevOps/Etc:** IntelliJ, GitHub, HeidiSQL, MobaXterm

---

## 🧭 설계 & 문서화
- **아키텍처/시퀀스/ERD**를 케이스 스터디에 포함  
- 공통 규칙: Principal 사용, ModelMapper 패턴, 로그 형식, CRUD 네이밍, 가독성 우선  
- 예외 메시지는 **UI까지 전달**(사용자 가시성)

---

## 📄 링크 & 연락
- Email: mrbulsapabb@gmail.com  
- GitHub: https://github.com/WhiteSnake-MrBBoo
- Resume: [KR PDF](assets/Resume_KR.pdf) · [EN PDF](assets/Resume_EN.pdf)

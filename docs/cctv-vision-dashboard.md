# CCTV Vision AI Dashboard – 폴리곤 영역 경보 & 실시간 분석

---

## 🎬 데모 영상

<div align="center">

  <!-- HTML5 비디오 -->
  <video 
    src="../assets/videos/cctv-demo.mp4"
    poster="../assets/cctv-dashboard-poster.png"
    width="820"
    controls
    muted
    playsinline
  >
    <a href="../assets/videos/cctv-demo.mp4">Watch the demo video</a>
  </video>

  <br/><br/>

  <!-- 썸네일 링크 (fallback) -->
  <a href="../assets/videos/cctv-demo.mp4" target="_blank" rel="noopener">
    <img src="../assets/cctv-dashboard-poster.png" width="360" alt="Open CCTV Demo Video">
  </a>

</div>

---

## 📌 개요
YOLOv11 + OpenCV 기반의 **실시간 CCTV 분석 대시보드**.  
사용자가 정의한 **폴리곤 영역(Region of Interest)** 에 객체가 진입/체류하는지 판정하여,  
**색상 경보 패널 + 실시간 차트**로 시각화.

---

## 🎯 문제 → 접근 → 성과
- **문제:** 단순 CCTV 화면만으로는 침입·혼잡 상황을 빠르게 인지하기 어려움  
- **접근:** 객체 탐지 결과를 Region 단위로 매핑하고, WebSocket을 통해 실시간으로 UI에 반영  
- **성과:**  
  - 관리자 한 화면에서 상황 인지 → **의사결정 속도 개선**  
  - **경보 색상 단계**(🟥 ALERT / 🟧 WARN / 🟩 SAFE / ⬜ IDLE)로 직관적 판단  
  - 오탐/미탐 데이터를 기록 → **지속적 피드백 루프** 가능

---

## 🧩 핵심 기능
- **폴리곤 Region 정의/정규화** :  
  프론트(Canvas)에서 마우스로 좌표 입력 → 백엔드에서 영상 해상도 기준으로 스케일링
- **YOLO 결과 처리 함수화** :  
  객체 바운딩 박스(xyxy)를 Region별로 매핑하여 카운팅
- **경보 패널 (4칸 UI)** :  
  - 🟥 ALERT : 침입 발생  
  - 🟧 WARN : 경계 상태  
  - 🟩 SAFE : 정상  
  - ⬜ IDLE : 미지정/데이터 없음
- **실시간 차트/로그** :  
  영역별 인원 수, 시간대별 변화량을 비동기 업데이트
- **WebSocket 양방향 통신** :  
  - 프론트에서 ROI 설정값 전송  
  - 백엔드에서 탐지 결과/경보 실시간 브로드캐스트

---

## 📺 시연 시나리오 (영상 흐름)
1. CCTV 스트림 입력 → YOLOv11 탐지 결과 표시  
2. 관리자가 **폴리곤 ROI** 지정 (예: 출입구, 복도, 위험 구역)  
3. 객체(사람/차량 등)가 ROI에 진입 → 경보 패널에 🟥 ALERT 표시  
4. 동시에 차트에 카운팅 반영 → **실시간 그래프 변화 확인**  
5. 다른 브라우저/클라이언트에서도 **WebSocket 브로드캐스트**로 동일 상태 동기화

---

## 🏗 아키텍처
- **Backend:** Python 3.x, Flask + Socket.IO, Ultralytics YOLOv11, OpenCV  
- **Frontend:** HTML5, JS/Canvas, Chart.js, 반응형 레이아웃  
- **Pipeline:**  

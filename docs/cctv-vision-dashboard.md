
---

## 2) `docs/cctv-vision-dashboard.md`

markdown
# CCTV Vision AI Dashboard – 폴리곤 영역 경보 & 실시간 분석

## 🎬 데모 영상 (CCTV Vision)

<!-- 반응형 느낌을 위한 래퍼: GitHub에서도 잘 동작하는 가장 안전한 형태 -->
<div align="center">

  <!-- HTML5 비디오: 모바일 자동재생은 muted + playsinline 필요 -->
  <video 
    src="../assets/videos/cctv-demo.mp4"
    poster="../assets/cctv-dashboard-poster.png"
    width="820"
    controls
    muted
    playsinline
  >
    <!-- 브라우저 호환을 더 챙기고 싶으면 source 태그 2개 형태로도 가능:
    <source src="../assets/videos/cctv-demo.webm" type="video/webm">
    <source src="../assets/videos/cctv-demo.mp4"  type="video/mp4">
    -->
    <!-- 대체 링크: 비디오 태그가 안 먹히는 뷰어용 -->
    <a href="../assets/videos/cctv-demo.mp4">Watch the demo video</a>
  </video>

  <br/><br/>

  <!-- 썸네일 클릭 시 동영상으로 이동: 일부 뷰어에서 비디오 태그 제한될 경우 대비 -->
  <a href="../assets/videos/cctv-demo.mp4" target="_blank" rel="noopener">
    <img src="../assets/cctv-dashboard-poster.png" width="360" alt="Open CCTV Demo Video">
  </a>

</div>


## 개요
YOLOv11 + OpenCV로 폴리곤 Region 침입/체류 감지, 실시간 경보/차트 대시보드.

## 문제 → 접근 → 성과
- **문제:** CCTV 다채널을 한 화면에서 정량적으로 파악하기 어려움  
- **접근:** Region 단위 카운팅·경보(알림 레벨), 반응형 UI + 실시간 그래프  
- **성과:** 상황 인지·의사결정 속도 개선, 오탐/미탐 피드백 루프 구축

## 핵심 기능
- 폴리곤 Region 정의/정규화(캔버스→원본 스케일)
- YOLO 결과 처리 함수화(테스트/확장 용이), 4칸 경보 패널
- 실시간 차트/지표(프런트 비동기 수신)

## 아키텍처
- **Backend:** Python, Flask/Socket.IO(또는 Streamlit), Ultralytics YOLOv11, OpenCV  
- **Frontend:** HTML/JS/Canvas, 반응형 레이아웃


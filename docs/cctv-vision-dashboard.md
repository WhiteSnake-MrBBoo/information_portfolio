
---

## 2) `docs/cctv-vision-dashboard.md`

markdown
# CCTV Vision AI Dashboard – 폴리곤 영역 경보 & 실시간 분석

<p align="center">
  <img src="../assets/cctv-dashboard.gif" width="820" alt="CCTV Dashboard">
</p>

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


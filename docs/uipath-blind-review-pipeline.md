# UiPath 리뷰 요약·추론 자동화 파이프라인 (RPA + AI)

## 🎬 데모 영상
https://github.com/user-attachments/assets/e8ea065c-bf0c-4f93-a32d-d476e298a9bf  
> 재생 버튼 클릭 영상 재생

---

## 📌 개요
**RPA 사무 자동화**로 수집된 기업 리뷰(Blind/설문/사내 피드백)를  
**AI 프롬프트 추론**으로 요약·분석하고,  
결과를 **Excel 자동 보고서**까지 이어지는 엔드투엔드 파이프라인입니다.  

또한 **Blind TOP9** 기업의 최신 리뷰/키워드를 **실시간 집계**하여  
비교·분석할 수 있게 설계했습니다.

- **핵심 가치**: 반복 수작업 제거 / 객관적 요약·추론 표준화 / 보고서 리드타임 단축  
- **도메인**: RPA(백오피스 자동화) + AI(텍스트 요약·추론) + Excel 리포팅

---

## 🎯 문제 → 접근 → 성과
- **문제**  
  - 대량 리뷰를 사람이 직접 읽고 요약 → 속도 느림, 편향 리스크  
  - 보고서 포맷 불일치, 재현 어려움  

- **접근**  
  - UiPath로 **수집 → 정제 → API 호출 → 검증 → 내보내기** 자동화  
  - **표준 프롬프트 + JSON 스키마** 강제 → 구조화 데이터 확보  
  - Blind TOP9 대상, **키워드·감성 실시간 집계**  

- **성과**  
  - 보고서 리드타임 **대폭 단축** → 담당자는 판단에 집중  
  - 추론 결과의 **일관성·재현성 확보**  
  - 데이터 → 의사결정으로 연결되는 신뢰성 강화  

---

## 🧩 핵심 기능
- **AI 요약·추론**:  
  - 긍/부정 키워드, 최종 추천(추천/중립/비추천), 이유(≤15자)  
- **표준 JSON 출력** → Excel/DB 안정 반영  
- **Excel 자동화**: 줄바꿈/열 폭 자동 조정, 누적 모드 지원  
- **오류 내성**: 파싱 실패/토큰 초과 시 `Decision` 컬럼에 원문 JSON 기록  
- **Blind TOP9 집계**: 9개 기업의 최신 리뷰/키워드 Top-N 차트 제공  

---

## 🧠 프롬프트 설계
> 실제 UiPath Invoke Code에서 사용한 **프롬프트 가이드 + 출력 포맷**  

<img width="820" alt="프롬프트 스크린샷" src="https://github.com/user-attachments/assets/9a51cf73-14bd-4c36-ad6a-39c206ec63e5" />

---

```text
당신은 객관적이고 공정한 데이터 분석 전문가입니다.
리뷰 데이터를 읽고 감정을 과도하게 넣지 않으며, 항상 간결하고 중립적으로 판단합니다.
AI 분석 결과는 의사결정을 돕는 참고자료라는 점을 명심하세요.

아래 입력은 하나의 JSON입니다.
형식: {"company":"회사명","reviews":{"rv":"리뷰텍스트","rt":평점(double)...}}
이 데이터를 분석하여 반드시 아래 JSON 형식으로만 답변하세요:

{
  "positives": ["장점 키워드1", "장점 키워드2", "장점 키워드3"],
  "negatives": ["단점 키워드1", "단점 키워드2", "단점 키워드3"],
  "decision": {
    "recommendation": "추천|중립|비추천",
    "reason": "AI가 최종 결정을 내린 핵심 이유 (최대 15자)"
  }
}

규칙:
1) positives/negatives 배열은 반드시 3개 키워드만 포함
2) 장점/단점 중복 불가, 리뷰에서 가장 많이 언급된 주제를 우선
3) recommendation은 추천/중립/비추천 중 하나
4) reason은 최대 15자 이내
5) JSON 외 텍스트 출력 금지

```
---
## 🔙 메인 포트폴리오로 돌아가기
[![Back_to_README](https://img.shields.io/badge/Back_to_Main_README-1B56FD?style=for-the-badge&logo=github&logoColor=white)](https://github.com/WhiteSnake-MrBBoo/information_portfolio/blob/main/README.md)

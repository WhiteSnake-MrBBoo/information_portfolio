
---

## 3) `docs/uipath-blind-review-pipeline.md`
```markdown
# UiPath 리뷰 요약 자동화 파이프라인

<p align="center">
  <img src="../assets/uipath-pipeline-arch.png" width="820" alt="UiPath Pipeline Architecture">
</p>

## 개요
Blind 리뷰 텍스트를 긍/부정/결론 3단으로 요약하고 Excel로 자동 출력.

## 문제 → 접근 → 성과
- **문제:** 대량 텍스트 수작업 요약/정리의 비효율  
- **접근:** Invoke Code(VB.NET)로 JSON 파싱 안전화, MaxLength=-1, 오류 시 Decision에 기록  
- **성과:** 보고서 리드타임 단축, 파이프라인 표준화

## 핵심 기능
- `choices[0].message.content`/`text` 파싱, 예외 안전
- `Dt_Blind_Ai_Result` 스키마 자동 구성(열 MaxLength=-1)
- Excel 출력(줄바꿈/열 폭)

## 기술 스택
UiPath, VB.NET Invoke Code, Newtonsoft JSON, Excel Activities

## 사용(요약)
- XAML 내 Invoke Code에 샘플 코드 삽입
- 변수: `Dt_Blind_New_Review_Table`(In), `Dt_Blind_Ai_Result`(Out)

## 배운 점
- 예외를 데이터로 남겨 재현성/추적성 확보

# GitHub Copilot 작업 지시문

이 저장소의 `index.html`은 신경세포의 excitation–transcription coupling을 설명하는 독립 실행형 인터랙티브 교육용 시뮬레이터다. 현재 구조와 기능을 먼저 읽고, 아래 조건을 지키면서 개선하라.

## 핵심 목표

세포 내부 이온통로·신호전달 요소의 변화가 활동전위의 특성을 바꾸고, Ca²⁺ 유입 및 CaMKIV·ERK/MAPK의 서로 다른 시간 경로를 통해 CREB 인산화와 유전자 전사를 변화시키며, 최종적으로 시냅스·수상돌기 수준의 장기적 변화에 연결되는 과정을 국소 구조 애니메이션으로 보여준다.

## 개선 요구

1. `index.html`을 실제 브라우저에서 실행해 기존 인터랙션과 반응형 화면을 확인한다.
2. K⁺ 통로 기능 조절이 활동전위 재분극 및 폭을 바꾸고, 그에 따라 Ca²⁺ 유입 모델값이 변하는 연결을 시각적으로 명확히 한다. 이 관계는 단순화된 교육용 계수임을 표시하고, 정확한 전기생리학적 예측이라고 주장하지 않는다.
3. CaMKIV 경로는 빠른 초기 CREB Ser133 인산화, ERK/MAPK 경로는 지연성 활성 및 후기 CREB 신호 지원으로 서로 다른 색과 시간 지연을 사용해 표현한다.
4. 칼슘 transient, CaMKIV, ERK/MAPK, 합산 pCREB, c-FOS 상대 전사 지수를 각각 시간 그래프로 표시한다.
5. 사용자가 두 가지 기준 자극 조건을 동시에 비교할 수 있도록 한다.
   - 10 Hz, 1.8초 burst, 1분 간격, 칼슘 peak 약 0.485 μM
   - 10 Hz, 9초 burst, 5분 간격, 칼슘 peak 약 0.735 μM
   두 조건은 Fields et al. (1997)에서 30분 동안 각각 총 540개 활동전위로 비교되었다. 두 번째 조건에서 칼슘 peak가 더 높아도 c-FOS 발현이 낮았다는 점을 강조한다.
6. 논문에 직접 보고된 값과 코드에서 단순화한 모형 매개변수 및 상대 지수를 반드시 구분한다. 상대 지수를 실제 mRNA 배수 변화나 임상적으로 해석 가능한 값으로 표시하지 않는다.
7. 논문에서 찾을 수 없는 수치 또는 경로별 반감기를 실험 측정값처럼 만들지 않는다. 불가피한 기본값은 “모델 가정”으로 명확히 표기한다.
8. 모바일 환경에서도 모든 슬라이더, 버튼, 애니메이션, 그래프가 정상 작동하도록 한다.
9. HTML/CSS/JavaScript 단일 파일 구조와 외부 CDN 없는 실행 방식을 유지한다.

## 출처

- Fields et al. (1997), *Action Potential-Dependent Regulation of Gene Expression*, Journal of Neuroscience: https://pmc.ncbi.nlm.nih.gov/articles/PMC6573446/
- Chawla et al. (2001), *CREB/CBP and SRE-interacting transcriptional regulators are fast on–off switches*: https://onlinelibrary.wiley.com/doi/10.1046/j.1471-4159.2001.00645.x
- Ma et al. (2023), *Excitation–transcription coupling, neuronal gene expression and synaptic plasticity*: https://pmc.ncbi.nlm.nih.gov/articles/PMC12024187/
- In vivo CREB imaging study (2020): https://pmc.ncbi.nlm.nih.gov/articles/PMC7144870/
- Voltage-gated potassium channel review: https://pmc.ncbi.nlm.nih.gov/articles/PMC4954569/

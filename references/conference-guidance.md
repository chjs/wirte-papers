# 공개 학회 문서의 적용 범위와 출처

조사 기준: **2026-10-08**. 스킬 반영: **2026-10-09**. 아래는 해당 판본에서 확인한 내용의 요약이며, 다른 연도·트랙의 영구 규칙이 아니다. 학회 맞춤 논증 리뷰, 제출 전 점검, rebuttal 작업 때 필요한 부분만 읽어라.

## 1. 근거의 권한을 구분하라

| 표시 | 의미 | 적용 방식 |
|---|---|---|
| 공식 요구 | 지정된 학회·연도·단계의 명시적 규정 | 해당 조건에서 적용하며 실제 작업 시 최신 원문을 확인한다. |
| 공식 권고 | CFP의 기대 수준, 저자 안내, SIG의 평가 지침 | 연구 유형과 주장에 맞춰 판단한다. 모두 자동 탈락 기준은 아니다. |
| 저자 조언 | 연구자들의 논문·에세이 | 공식 사이트가 추천해도 전부 필수 규정이 되는 것은 아니다. |
| 도출 절차 | 여러 자료를 바탕으로 이 스킬이 구성한 편집·리뷰 방법 | 유용한 작업 방식이며 학회 공식 심사표로 부르지 않는다. |

**CFP에 공개된 심사 기준, 실제 공개 심사 양식, artifact 심사 안내를 구분하라.** 아래 자료는 모든 PC 내부 지침을 확보한 결과가 아니다. ATC의 공개 양식은 extended abstract의 1차 심사용이고, ASPLOS의 아래 `For Reviewers` 페이지는 artifact용이다.

## 2. 학회·연도별 적용 카드

### OSDI 2027

- **공식 권고·공개 기준:** 기여의 새로움과 중요성, 명료성·정확성 등을 판단하며, 관련 시스템 선행 연구 대비 진전을 드러내도록 한다. ML 등 새 적용 분야에서도 시스템 관점의 문제·비교를 생략하지 않는다.
- **공식 트랙 설명:** Operational Systems는 새로운 연구 아이디어 자체를 필수로 삼지 않는다. 실제 운영을 통해 얻은 검증·통찰·교훈의 지식 기여를 평가하라.
- **조건부 공지:** 앞부분만 보는 초기 심사를 도입할 수 있다고 되어 있다. 확정된 ‘2쪽 심사’ 규정으로 바꾸지 마라.
- **도출 절차:** 연구형은 선행 대비 진전, 운영형은 관찰·맥락·교훈·전이 가능한 범위를 기여표에 적어라.

근거: [OSDI 2027 CFP](https://www.usenix.org/conference/osdi27/call-for-papers). [Requirements for Authors](https://www.usenix.org/conference/osdi27/requirements-authors)는 Levin–Redell, Gopen–Swan, *The Elements of Style*을 참고 자료로 소개한다. 이 추천이 본 스킬의 세부 절차 전체를 공식화하지는 않는다.

### ASPLOS 2027

- **공식 요구:** rapid review는 논문의 첫 2쪽만 대상으로 하며, 그 부분이 독립적으로 이해되어야 한다.
- **공식 기준:** architecture·OS·PL 또는 이들과 의미 있게 연결된 새 영역의 실질적인 학문적 진전이 중요하다. 도구 사용만으로 분야 기여가 되지는 않으며, 단일 핵심 분야의 획기적 결과도 허용한다.
- **공식 기대:** SIGPLAN empirical evaluation 지침을 따르고, 구현 상태와 장단점을 분명히 설명한다.
- **도출 절차:** 첫 2쪽만 받은 독자가 문제·선행 대비 차이·핵심 통찰·증거를 파악할 수 있는지 점검하라. 억지로 여러 분야의 기여를 만들어 넣지 마라.

근거: [ASPLOS 2027 CFP — Scope, Rapid Review, Research Advancement](https://www.asplos-conference.org/asplos2027/cfp/).

### EuroSys 2027

- **공식 권고·공개 기준:** 선행 대비 장점과 제한을 엄밀히 평가한다. 경험 논문도 공동체에 유용한 일반적 교훈과 정량 근거를 제시해야 한다.
- **도출 절차:** 이득을 주장한 조건과 손해·제약을 함께 확인하라. 단일 배포 사례의 성공을 모든 환경의 보장으로 바꾸지 마라. ‘경험 논문 환영’을 확인되지 않은 별도 트랙의 존재로 해석하지 마라.

근거: [EuroSys 2027 CFP](https://2027.eurosys.org/cfp.html).

### SOSP 2026

- **공식 권고·공개 기준:** 중요한 문제와 기여, 실용적 이점과 뒷받침되는 결론이 중요하다. 새로운 연구 영역과 경험·측정 연구도 환영하며, 초기 영역의 평가 여건이 성숙한 영역과 다를 수 있음을 인정한다.
- **도출 절차:** 시스템 구현의 효과를 주장하면 구현·측정 근거를 요구하라. 모든 논문에 새 시스템·완성된 대규모 배포를 일률적으로 요구하지 말고 연구 질문과 기여 유형에 맞춰라.

근거: [SOSP 2026 CFP](https://sigops.org/s/conferences/sosp/2026/cfp.html).

### ATC 2026

- **공식 요구:** 2쪽 extended abstract와 full paper는 각각 독립적으로 이해되어야 한다. 이것은 ASPLOS의 ‘full paper 첫 2쪽’과 다른 제출물이다.
- **공식 트랙 설명:** 짧은 논문도 범위가 좁은 완결된 연구여야 한다. Operational Systems는 새로운 아이디어만이 아니라 실제 시스템의 유용한 교훈을 기여로 인정한다.
- **공식 저자 권고:** extended abstract에서 동기, 기존 접근의 한계, 핵심 통찰·아이디어, 평가 개요를 설명한다. Introduction에도 적용되는 조언이다.
- **공개 심사 양식:** 위 내용의 명료성·중요성·선행 맥락·평가 적절성과 주장 지지를 묻는다. 1차 extended abstract 양식을 전체 논문의 유일한 심사 기준으로 확대하지 마라.
- **도출 절차:** Introduction의 역방향 읽기 점검에 이 질문들을 활용하되, 고정 문단 수나 분량 공식을 강제하지 마라.

근거: [ATC 2026 CFP](https://sigops.org/s/conferences/atc/2026/cfp.html), [Extended Abstract Guidelines](https://sigops.org/s/conferences/atc/2026/abstract.html), [1차 Sample Review Form](https://sigops.org/s/conferences/atc/2026/review.html).

## 3. 실제 제출·응답 작업에서 다시 확인할 것

**도출 절차:** 현재 요청에 관계되는 항목만 `학회/연도/트랙/주기/단계 → 공식 URL·절 → 확인일 → 적용 규정`으로 기록하라. 일반 편집을 위해 이 표를 전부 채우게 하지 마라. 오래된 링크만 있거나 공식 페이지를 읽지 못했다면 그 규정은 미확인으로 남기고 가능한 글 편집은 계속하라.

| 항목 | 기록할 내용 |
|---|---|
| 제출물·분량 | full paper, 별도 abstract, short paper, 본문·참고문헌·부록 포함 범위 |
| 심사 단계 | 첫 부분만 읽는 확정 단계인지, 도입 가능성을 알린 것인지 |
| 자족성 | 본문에 있어야 하는 핵심 근거와 선택적으로 읽는 보충 자료 |
| 응답 | 새 실험·자료의 허용 범위, 분량, 첨부 가능 여부 |
| 해당되는 정책 | 익명화, 생성형 AI 사용·공개, 재제출 등 현재 요청에 필요한 항목 |

응답 규칙의 차이를 보존하라. 확인한 판본에서 [ASPLOS 2027](https://www.asplos-conference.org/asplos2027/cfp/)은 리뷰어 우려에 직접 답하는 새 실험·자료를 허용하지만, [EuroSys 2027](https://2027.eurosys.org/cfp.html), [SOSP 2026](https://sigops.org/s/conferences/sosp/2026/cfp.html), [ATC 2026](https://sigops.org/s/conferences/atc/2026/cfp.html)은 새 실험·자료를 응답에 넣지 못하도록 한다. 이를 모든 학회의 일반 규칙으로 고정하지 마라. 응답을 쓸 때 해당 연도 원문을 재확인하고, 수행하지 않은 실험을 수행한 것처럼 쓰지 마라.

본문 자족성도 압축 기준으로 사용하라. 위 CFP들의 보충 자료 정책상 리뷰어가 부록·외부 자료를 모두 읽을 것으로 전제할 수 없다. 핵심 알고리즘이나 결론을 지지하는 유일한 결과를 부록으로 밀어내는 편집은 피하라. 세부 증명·설정·확장 결과의 적절한 위치는 내용과 현재 규정으로 판단하라.

## 4. 공통 절차를 뒷받침하는 자료

| 자료·권한 | 가져온 판단 기준 | 이 스킬의 적용 위치 |
|---|---|---|
| [SIGPLAN Empirical Evaluation](https://www.sigplan.org/Resources/EmpiricalEvaluation/) 및 [2018 checklist](https://raw.githubusercontent.com/SIGPLAN/empirical-evaluation/master/checklist/checklist.pdf), 공식 SIG 지침 | 주장에 맞는 비교·표본·지표·분석·설계·표현. 체크 개수로 합격을 결정하지 않음 | [empirical-evaluation.md](empirical-evaluation.md). ASPLOS의 명시적 연결을 다른 학회 전체의 의무로 확대하지 않음 |
| [SIGPLAN Review Policy](https://www.sigplan.org/Resources/Policies/Review/), 공식 SIG 정책 | 기여와 타당성, 결과를 이해·확장할 정보, 전문성에 맞는 심사 | [review-checklist.md](review-checklist.md). 모든 학회의 동일 정책으로 부르지 않음 |
| [Hill–McKinley, Constructive and Positive Reviewing, 2005](https://www.cs.utexas.edu/~mckinley/notes/reviewing.html), 저자 조언 | 가치와 약점을 함께 검토하고 구체적·건설적 근거를 제시 | 강점, 결론에 중요한 우려, 선택적 개선을 구별 |
| [Heiser, Systems Benchmarking Crimes](https://gernot-heiser.org/benchmarking-crimes.html), 저자 조언 | 선택 편향, 불공정 비교, 비용 누락, 측정 범위보다 큰 주장 탐지 | Evaluation 감사. 저자의 강한 표현이나 통계 처방 전부를 절대 규칙으로 옮기지 않음 |
| [Levin–Redell, 1983](https://www.usenix.org/legacy/publications/library/proceedings/dsl97/good_paper.html), 저자 조언 | 문제·기여·선택 이유·구현 상태와 독자에게 남는 교훈 | [section-editing.md](section-editing.md)의 논증·Design |
| [Gopen–Swan, The Science of Scientific Writing, 1990](https://www.usenix.org/sites/default/files/gopen_and_swan_science_of_scientific_writing.pdf), 저자 조언 | 독자의 기존 정보와 새 정보, 주제와 강조 위치, 가까운 주어·동사 | 문장·문단의 정보 흐름. 고정 어순이나 수동태 금지로 사용하지 않음 |
| [Brown et al., The Many Faces of Systems Research, HotOS 2005](https://usenix.org/legacy/events/hotos05/final_papers/full_papers/red_team/red_html/paper.html), 연구 관점 논문 | 기여의 성격에 맞는 평가 판단 | 모든 연구에 동일 실험 목록을 강제하지 않음 |
| [ASPLOS 2027 For Reviewers](https://www.asplos-conference.org/asplos2027/for-reviewers/), **artifact 심사 안내** | 실행 환경·문서·결과 재현과 협력적 문제 해결 | artifact 요청에만 사용. 논문의 새로움·채택 여부 심사표로 사용하지 않음 |

SIGPLAN이 외부 조언을 소개하는 페이지는 [Guidelines for Referees](https://www.sigplan.org/Resources/Guidelines/Referees/)다. 링크된 에세이의 모든 문장이 SIGPLAN의 강제 정책이 되는 것은 아니다.

## 5. 이번 분석에서 도출한 작업 규칙

다음은 공식 문서의 복사본이 아니라 이 스킬의 합성 절차다.

1. **기여표:** 선행 접근 대비 새 지식과 이를 지지하는 자료를 연결한다.
2. **Introduction 역방향 읽기:** 소개에 실제 적힌 문장만으로 문제·한계·아이디어·근거를 복원한다.
3. **Evaluation 감사:** 대표 결과가 전체 측정 범위와 비용·제약을 공정하게 드러내는지 확인한다.
4. **건설적 리뷰:** 강점, 결론에 중요한 문제, 설명·검증 보완, 선택적 확장을 구분한다.
5. **범위 보존:** 연구 유형과 학회 판본을 먼저 확인하며, 부족한 자료를 반증으로 취급하지 않는다.

학회 문서의 장문·심사 양식 전체·외부 저자의 예문은 묶음에 복제하지 않았다. 사실·수치·LaTeX 불변성 절차와 가상 예문은 이 스킬의 독자적 작업 설계다.

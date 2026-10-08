# 원문 분석과 출처

확인일: Strunk·학회 자료 2026-10-08, Simon Peyton Jones 자료 2026-10-09. 이 파일의 한국어 설명, 시스템 논문용 규칙, 예시는 새로 작성한 해석이다. 아래 짧은 영어 규칙명은 Strunk의 퍼블릭 도메인 1920년판을 식별하기 위한 표제다.

## 1. 분석의 범위

직접 대조한 기준 텍스트는 **William Strunk Jr., The Elements of Style, 1920**의 Project Gutenberg 전사본이다. Wikisource의 1920년판 표제·판권·목차를 교차 확인했다. 그 판권면에는 Strunk의 1918·1919년과 출판사의 1920년이 함께 표시된다. 1918년판 전 페이지를 1920년판과 대조한 판본 연구는 아니다. 규칙 번호와 아래 쪽수는 **1920년판 인쇄 쪽수**이며 최신 Strunk & White 판에 그대로 적용하지 않는다. [원문](https://www.gutenberg.org/files/37134/37134-h/37134-h.htm), [판권·목차](https://en.wikisource.org/wiki/The_Elements_of_Style_(1920))

1959년 Macmillan 판은 White가 개정·서문·새 장을 더한 판본으로 서지에 나타난다. Pearson의 제4판 목차에도 별도의 문체 장이 있다. 이 묶음은 그 추가 장의 전체 원칙 목록, 장문 발췌, 번역, 고유 예문을 수록하지 않는다. 현대판의 모든 내용을 분석했다고 주장하지 않는다. [1959년판 서지](https://books.google.com/books/about/The_Elements_of_Style.html?id=VDi6AAAAIAAJ), [Pearson 제4판 안내](https://www.pearson.com/en-nz/subject-catalog/p/elements-of-style-the/P200000002160)

Project Gutenberg는 해당 Strunk 원문을 미국에서 public domain으로 표시한다. 여기에는 책 전문, 전사본 파일, 현대판의 추가 내용, 기존 한국어 번역을 포함하지 않았다. 원문의 짧은 표제와 출처, 새 해설과 새 예시로 구성했다. 현대판의 권리까지 퍼블릭 도메인으로 취급하지 마라. [Gutenberg 서지·권리 표시](https://www.gutenberg.org/ebooks/37134)

## 2. 이 책을 시스템 논문에 적용하는 해석

원문에서 특히 유용한 것은 개별 단어의 취향보다 **독자가 생각의 관계를 복원하기 쉽게 만드는 구조**다. 문단은 논점의 단위, 병렬 구조는 비교의 단서, 단어 배치는 수식 범위의 단서다. 이를 시스템 논문에서는 ‘어떤 조건에서 무엇을 주장하고 어떤 근거가 있는가’를 명확히 드러내는 방향으로 적용한다. 이것은 본 스킬의 해석이며, Strunk가 현대 시스템 실험 방법론을 제시했다는 뜻이 아니다.

원문 자체에도 예외가 있다. §10은 수동태가 편리하거나 필요한 경우를 설명하고, §13은 모든 문장을 짧게 만들라는 뜻이 아니라고 명시한다. 따라서 능동태 비율, 평균 문장 길이, 삭제 단어 수를 품질 목표로 삼으면 원문의 취지도 좁히게 된다. [1920년판 III장](https://www.gutenberg.org/files/37134/37134-h/37134-h.htm)

## 3. III장 원칙과 적용 경계

아래 ‘적용’과 ‘경계’ 열은 시스템 논문을 위해 작성한 지침이다.

| 1920년 번호·쪽 | 원문 표제 | 시스템 논문에 적용 | 적용 경계 |
|---|---|---|---|
| §8, p.15 | Make the paragraph the unit of composition: one paragraph to each topic | 문단마다 하나의 질문·논점을 정하고 근거를 묶는다. | 한 문단에 한 문장만 허용한다는 뜻이 아니다. 필요한 전환 문단도 허용한다. |
| §9, p.17 | As a rule, begin each paragraph with a topic sentence; end it in conformity with the beginning | 앞부분에서 문단의 역할을 밝히고 뒤에서 근거·함의를 전개한다. | 전환 문장이 앞에 올 수 있다. 마지막 문장에 기계적인 요약을 덧붙이지 않는다. |
| §10, p.19 | Use the active voice | 책임·작동 주체가 중요하면 주어와 동작을 명확히 쓴다. | 실험 대상이 문단 주제이거나 행위자가 불명확하면 수동태를 유지한다. |
| §11, p.21 | Put statements in positive form | 회피·완곡 표현을 정확한 진술로 고친다. | 부정 결과, 지원하지 않는 기능, 비보장, 불확실성을 없애지 않는다. |
| §12, p.22 | Use definite, specific, concrete language | performance 대신 정확한 지표·대상·조건을 쓴다. | 없는 숫자·원인·구현 세부사항은 구체화하지 않는다. |
| §13, p.24 | Omit needless words | 내용 없는 도입, 반복 평가, 장황한 명사화를 덜어낸다. | 실험 조건과 정당한 한정어는 의미의 일부다. 모든 문장을 단문으로 만들지 않는다. |
| §14, p.25 | Avoid a succession of loose sentences | `and`로 나열된 사실들의 논리적 관계를 드러낸다. | `because`나 `therefore`를 넣을 때 새 인과관계를 만들지 않는다. |
| §15, p.26 | Express co-ordinate ideas in similar form | contribution 목록, baseline 비교, RQ를 병렬 형태로 맞춘다. | 서로 다른 주장·지표를 같은 것으로 만들지 않는다. |
| §16, p.28 | Keep related words together | 수식어·조건·인용을 해당 대상 가까이에 둔다. | `only`, `all`, 부정의 범위가 바뀌지 않게 한다. |
| §17, p.29 | In summaries, keep to one tense | 같은 시간 관계와 서술 기능에서는 시제를 일관되게 쓴다. | 원문은 주로 문학 줄거리 요약 문맥이다. 논문 전체의 시제를 강제하지 않는다. |
| §18, p.31 | Place the emphatic words of a sentence at the end | 문맥상 새롭고 중요한 결과를 눈에 띄는 위치에 둔다. | 문두 강조도 가능하다. 의미를 제한하는 조건을 숨기지 않는다. |

표의 근거: [1920년 목차](https://en.wikisource.org/wiki/The_Elements_of_Style_(1920)) 및 [III장 본문](https://www.gutenberg.org/files/37134/37134-h/37134-h.htm).

## 4. 다른 장에서 선택적으로 가져올 것

- II장 §3의 삽입구·관계절 구분은 어떤 노드·요청·실험을 가리키는지 보존하는 데 유용하다. 쉼표를 더하거나 없애면서 집합의 범위를 바꾸지 마라.
- II장 §§4–6을 적용해 독립절 연결과 문장 경계를 명확히 하라. 도표 제목·목록 항목까지 완전한 문장으로 바꾸지 마라.
- II장 §7의 분사구문 주어 관계를 확인하라. “Using four GPUs, latency fell …”에서 실제 사용 주체를 모르면 문장 구조로 해결하라.
- IV장의 원고 형식이나 VI장의 철자 목록은 현대 투고처 규정보다 우선하지 않는다. V장의 어법 목록도 자동 금지어 사전으로 사용하지 마라. 분야에서 정확한 전문 용어는 유지하라.

이 항목의 출처는 [1920년 II·IV·V·VI장](https://www.gutenberg.org/files/37134/37134-h/37134-h.htm)이다. 시스템 예와 적용 경계는 본 묶음의 확장이다.

## 5. 시스템 논문에 추가한 규칙의 출처 구분

Levin과 Redell은 문제·새 아이디어·관련 연구와의 차이를 명확히 하고, 구현 상태, 가정, 설계 선택의 이유와 일반화 범위를 드러내라고 논한다. 또한 구현 논문과 이론 논문 등에 같은 평가 기준을 일률적으로 적용할 수 없다고 설명한다. 이 관점만 참고하고 기존 예문과 체크리스트를 복제하지 않았다. [Roy Levin and David D. Redell, 1983, USENIX 재게시](https://www.usenix.org/legacy/publications/library/proceedings/dsl97/good_paper.html)

수치·분모·집계 방식의 불변성, 인과 주장 보호, LaTeX 보존은 **본 스킬을 위한 실무 설계**다. 이후 공개 학회 문서 분석을 반영하여 기여표, 소개의 역방향 읽기, 평가 감사, 건설적 리뷰 절차를 보강했다. 이 표와 절차 전체를 Strunk·White의 원문이나 학회의 공식 심사표로 인용하지 마라.

추가 출처와 권한 구분은 [conference-guidance.md](conference-guidance.md)에 기록했다. OSDI·ASPLOS·EuroSys·SOSP·ATC의 지정 연도 CFP/저자 안내, ATC의 1차 공개 심사 양식, SIGPLAN의 평가·리뷰 지침, Gopen–Swan·Hill–McKinley·Heiser 등의 저자 조언을 구분한다. [평가 절차](empirical-evaluation.md)는 SIGPLAN의 일곱 관점을 바탕으로 한 재구성이며 모든 학회가 같은 실험을 요구한다는 뜻이 아니다. 통계 검정·표본 수·평가 방법은 연구 질문과 실험 설계에 맞춰 판단하라.

## 6. Simon Peyton Jones의 연구 글쓰기 조언

Microsoft Research의 [How to write a great research paper](https://www.microsoft.com/en-us/research/academic-program/write-great-research-paper/)와 연결된 [52쪽 슬라이드 PDF](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/07/How-to-write-a-great-research-paper.pdf)를 확인했다. 아래 쪽수는 해당 PDF의 첫 페이지를 1로 센 번호다. 이는 **저자의 집필 조언**이며 학회의 공식 요구가 아니다. 연결된 영상은 분석 근거로 사용하지 않았다.

| 근거 쪽 | 채택한 관점 | 이 스킬의 적용 |
|---|---|---|
| 3–7, 10–11 | 연구 도중 글을 쓰며 생각을 발전시킨다. | 잠정 기여를 써 보고 빈틈을 구체적 연구 질문과 필요한 근거로 전환한다. 미측정 결과는 만들지 않는다. |
| 9, 12–13 | 독자가 가져갈 핵심 아이디어를 분명히 한다. | 조건을 포함한 한 문장의 통찰 아래 서로 연결된 여러 기여를 설명한다. |
| 19–20, 35–39 | 구체적 예제로 직관을 만든 후 일반화한다. | 작은 동작 예제에서 설계 규칙으로 확장하되 설명용 예제와 실험·증명을 구분한다. |
| 40–44 | 독자가 막힌 부분을 찾아 글을 고친다. | 독자의 해석과 의도·근거를 대조하고 원고의 실제 수정으로 연결한다. |

앞의 세 절차는 [section-editing.md](section-editing.md), 피드백 절차는 [review-checklist.md](review-checklist.md)에 있다. 구체적인 기여와 근거 위치 연결(21–24쪽), 선행 연구에 대한 공정한 인정과 한계 설명(31–32쪽)은 기존 규칙을 보강하는 근거로 사용했다. 표와 절차는 본 스킬의 재구성이며 슬라이드 원문 규칙을 그대로 재현한 목록이 아니다.

다음 조언은 문맥에 따라 적용한다.

- **분량·문장 수:** 16·18쪽 등의 예시를 Introduction 1쪽, Abstract 4문장 같은 고정 규칙으로 만들지 않는다. 슬라이드의 독자 수 예시도 실제 조사 통계로 인용하지 않는다.
- **Related Work 위치:** 26–30쪽의 조언은 앞부분의 과도한 문헌 나열을 줄이는 데 활용한다. 새로움을 판단하는 데 필요한 선행 연구 비교·인용은 초반에 남기며, 항상 맨 뒤로 옮기지 않는다.
- **핵심 아이디어:** 하나의 전달 메시지가 정확히 하나의 기술적 기여만 허용한다는 뜻은 아니다. 일관된 시스템 연구를 기계적으로 분할하지 않는다.
- **문체·탐색:** 50쪽의 강한 수동태 회피 조언보다 이 스킬의 정확성·주제 연속성 예외를 우선한다. 25쪽의 일반적인 구성 안내 비판은 유용한 탐색 문장까지 금지하는 규칙으로 쓰지 않는다.
- **피드백 요청:** 42쪽의 동료·관련 연구자 피드백 조언은 자동 공유·연락 권한을 부여하지 않는다. 실제 외부 연락은 사용자 지시와 해당 익명화·접촉 정책을 따른다.

슬라이드 전문·장문 번역·고유 예문은 묶음에 포함하지 않았다. 예시와 테스트는 이 스킬을 위해 별도로 작성했다.

## 7. 참고 문헌

1. William Strunk Jr. *The Elements of Style*. 1920. 기준 본문: [Project Gutenberg #37134](https://www.gutenberg.org/files/37134/37134-h/37134-h.htm). [서지](https://www.gutenberg.org/ebooks/37134).
2. *The Elements of Style (1920)*. [Wikisource 표제·판권·목차](https://en.wikisource.org/wiki/The_Elements_of_Style_(1920)). 번호·쪽수 교차 확인용.
3. William Strunk Jr., with revisions, introduction, and new writing material by E. B. White. *The Elements of Style*. Macmillan, 1959. [Google Books 서지](https://books.google.com/books/about/The_Elements_of_Style.html?id=VDi6AAAAIAAJ). 서지 확인용이며 본문 분석 대상으로 사용하지 않음.
4. Strunk and White. *The Elements of Style*, 4th ed. [Pearson 출판사 안내](https://www.pearson.com/en-nz/subject-catalog/p/elements-of-style-the/P200000002160). 현대판 구분과 목차 확인용.
5. Roy Levin and David D. Redell. “An Evaluation of the Ninth SOSP Submissions; or, How (and How Not) to Write a Good Systems Paper.” *ACM SIGOPS Operating Systems Review* 17(3), 1983, pp.35–40. [USENIX 제공 본문](https://www.usenix.org/legacy/publications/library/proceedings/dsl97/good_paper.html).
6. Simon Peyton Jones. *How to write a great research paper*. [Microsoft Research 자료 페이지](https://www.microsoft.com/en-us/research/academic-program/write-great-research-paper/), [슬라이드 PDF](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/07/How-to-write-a-great-research-paper.pdf). 확인일 2026-10-09; 저자 조언.

학회별 페이지 제한·익명화·제출·아티팩트 요구는 해당 연도의 공식 안내를 별도로 확인하라. 이 스킬의 학회 카드는 확인한 판본과 날짜를 기록한 참고 자료이며 미래 투고의 규정 준수를 보증하지 않는다.

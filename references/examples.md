# Before / After 예시

**아래 시스템·상황·수치는 모두 이 스킬을 위해 만든 가상 자료다.** 실제 논문의 실험 결과로 재사용하지 마라. 각 예시의 ‘주어진 사실’이 충족될 때만 해당 수정을 적용하라. 표현이 달라도 의미가 보존되면 좋은 수정일 수 있다.

## 1. 장황한 표현 줄이기 — 문체 수정

Before:

> In order to avoid the repetition of work, the scheduler performs a check of the queue before dispatching each request.

After:

> To avoid repeating work, the scheduler checks the queue before dispatching each request.

이유: 목적과 처리 순서는 그대로 두고 불필요한 명사화를 줄였다. 검사가 중복 실행을 **항상 방지한다**는 새 보장은 추가하지 않았다.

## 2. 정확한 행위자로 능동태 쓰기 — 문체 수정

주어진 사실: tokenizer가 요청을 토큰으로 변환한다.

Before:

> Each request is converted into tokens by the tokenizer.

After:

> The tokenizer converts each request into tokens.

이유: 행위자가 주어진 경우에만 앞으로 옮겼다. 요청을 계속 주제로 삼는 문단이면 원래 수동태도 적절하다.

## 3. 수동태와 부정을 유지하기 — 수정 불필요

Before / After:

> Each configuration was evaluated five times. The prototype does not support recovery after a coordinator failure.

이유: 평가 대상이 주제이고, 두 번째 문장의 비지원 조건은 핵심 기술 정보다. `We evaluated …`를 강제하거나 `The prototype supports reliable execution`처럼 바꾸면 안 된다.

## 4. 비교의 병렬 구조 — 문체 수정

Before:

> System A batches requests before transmission, whereas in System B each request is sent immediately.

After:

> System A batches requests before transmission, whereas System B sends each request immediately.

이유: 같은 차원의 동작을 같은 문법 구조로 비교했다. batching이 더 빠르다는 결과는 덧붙이지 않았다.

## 5. `only`와 조건의 범위 — 의미를 확인한 수정

주어진 사실: CPU 사용률이 70% 미만일 때만 admission이 가능하며, 그 조건이 admission을 보장하지는 않는다.

Before:

> The scheduler only admits a request when CPU utilization is below 70%.

After:

> The scheduler admits a request only when CPU utilization is below 70%.

보존: admission의 필요조건, strict inequality, 70%. `whenever CPU utilization is below 70%`는 충분조건을 추가하므로 허용하지 않는다. 의도가 주어지지 않았다면 먼저 모호성을 표시하라.

## 6. 분사구문의 주체 — 구조 수정

주어진 사실: 4 GPU 설정에서 관찰한 p99 latency는 40 ms에서 32 ms로 낮아졌다. 원인은 분리하지 않았다.

Before:

> Using four GPUs, p99 latency fell from 40 ms to 32 ms.

After:

> In the four-GPU configuration, p99 latency fell from 40 ms to 32 ms.

이유: latency가 GPU를 사용한다는 잘못된 연결을 제거했다. GPU 수가 변화의 원인이라고 쓰지 않았다.

## 7. 모호한 지표 구체화 — 제공된 근거로 명료화

주어진 사실: 고정된 설정에서 세 workload 모두의 평균 요청 지연을 측정했고, baseline B 대비 workload별 감소율 중 최댓값이 35%다. 전체 평균 감소율은 제공되지 않았다.

Before:

> The system improves performance by up to 35%.

After:

> Across the three evaluated workloads, the system reduces mean request latency by up to 35% relative to baseline B.

보존: mean request latency, 비교 대상 B, 세 평가 workload, 최대 감소율. `reduces average latency by 35% across workloads`로 바꾸면 집계 의미가 달라진다. 주어진 근거가 없으면 이 After를 지어내지 말고 지표를 확인하라.

한계: 이 수정은 지표와 최대값의 의미를 명확히 할 뿐, 대표적인 개선을 입증하지는 않는다. 전체 workload별 결과가 없으므로 나머지 분포와 악화 여부는 미확인으로 남겨라. Abstract의 대표 결과로 쓰려면 이를 별도로 점검하라.

## 8. 인과 주장 약화 — 문체가 아닌 주장 정정

주어진 사실: 같은 설정에서 system A와 baseline B를 비교했다. A의 전송량은 18% 적고 평균 지연은 7% 낮았으나 원인을 분리하는 실험은 없다.

Before:

> System A reduces mean latency by 7% by transferring 18% less data than baseline B.

After:

> Compared with baseline B, System A transfers 18% less data and has 7% lower mean latency in this configuration.

별도 코멘트: “전송량 감소가 지연 감소의 원인이라는 구절은 제공된 비교만으로 확인되지 않아 관찰 수준으로 수정했습니다. 해당 원인 주장을 유지하려면 이를 분리하는 근거가 필요합니다.”

## 9. Evaluation 문단 — 구조와 근거 범위 보존

주어진 사실: workload W, baseline B, 동일한 8-core 설정. 세 run에서 각각 계산한 p99를 산술평균하면 B는 100 ms, system A는 80 ms다. run별 값은 없다.

Before:

> We evaluated workload W on eight cores. The average of the per-run p99 latencies was 100 ms for B and 80 ms for A. There were three runs for each system. Both systems used the same configuration. A is therefore consistently faster.

After:

> On workload W, the arithmetic mean of the per-run p99 latencies over three runs was 100 ms for baseline B and 80 ms for system A, using the same eight-core configuration. These aggregates do not establish whether A had lower p99 latency in every run.

이유: 핵심 결과와 설정을 모았다. 마지막 문장은 ‘항상 개선’이라는 근거 없는 주장에 대한 정정이다. 100 ms와 80 ms를 전체 요청을 합친 p99로 바꾸거나, 자료에 없는 CI와 유의성을 추가하지 않았다.

## 10. Introduction 문단 — 문제와 목표 연결

주어진 사실: 작은 요청이 큰 요청의 전송 완료를 기다리는 FIFO sender를 대상으로 한다. 제안은 전송 크기를 제한하는 chunking이며 결과는 아직 없다.

Before:

> Modern systems are increasingly important. Our system is a novel solution. In the FIFO sender we study, small requests wait for an ongoing large transfer to finish. We propose dividing large transfers into bounded chunks so that small requests can be scheduled between chunks.

After:

> In the FIFO sender we study, small requests wait for an ongoing large transfer to finish. We propose dividing large transfers into bounded chunks so that the sender can schedule small requests between chunks. The design aims to reduce this waiting time; its performance has not yet been evaluated.

이유: 구체적 문제와 메커니즘을 먼저 놓았다. 새로 덧붙인 마지막 문장은 주어진 ‘미평가’ 상태를 명시한다. 최초·최적·정량 개선을 만들지 않았다.

## 11. Design 문단 — 동작 순서·불변조건 유지

주어진 사실: single-writer 구조이며, 이 writer가 descriptor를 초기화한 후 publish한다. reader는 published descriptor만 읽는다. atomic publication 방식이나 메모리 모델은 제공되지 않았다.

Before:

> There is one writer. Readers read published descriptors. Initialization is done by the writer. Publication is performed after initialization. This is the protocol.

After:

> The single writer initializes each descriptor before publishing it. Readers access only published descriptors.

별도 확인 사항: “완전히 초기화된 값의 가시성까지 보장한다고 쓰려면 publication 방식과 메모리 순서 근거가 필요합니다.”

이유: 설명 순서를 정리했지만 `lock-free`, `linearizable`, `race-free` 등의 보장을 추가하지 않았다.

## 12. 시제 혼용이 올바른 경우 — 수정 불필요

Before / After:

> The scheduler assigns each request to a queue. We evaluated the prototype on eight servers. Figure 4 reports the measured throughput.

이유: 설계 동작, 완료된 실험, 현재 본문 참조가 다른 서술 기능을 가진다. 한 시제로 맞추면 오히려 의미가 흐려질 수 있다.

## 13. 백분율의 의미 — 계산을 드러낸 정정

주어진 사실: hit rate가 80%에서 84%로 올랐다.

Before:

> The hit rate increased by 4%.

After:

> The hit rate increased from 80% to 84%, a gain of 4 percentage points.

별도 코멘트: “84 − 80 = 4 percentage points이며, 상대 증가율은 (84 − 80) / 80 = 5%입니다.” 숫자 4를 보존하는 것만으로 사실 불변성이 충족되는 것은 아니다.

## 14. 통계적 불확실성 — 부정과 한정 보존

Before:

> We did not observe a statistically significant difference under the reported test.

After:

> We did not observe a statistically significant difference under the reported test.

이유: `The systems are equivalent`나 `There is no difference`로 바꾸지 않는다. 검정 정보가 실제 자료에 없으면 이 문장 자체의 근거를 별도로 확인해야 한다.

## 15. 최대값이 맞아도 대표성을 확인하기 — 주장 범위 보완

주어진 사실: 동일한 설정에서 baseline B 대비 평균 요청 지연이 W1에서는 30%, W2에서는 2% 감소했고 W3에서는 8% 증가했다. 이것이 평가한 세 workload 전부다.

Before:

> A reduces mean request latency by up to 30% compared with B.

After:

> Compared with B under the same configuration, A reduces mean request latency by 30% on W1 and 2% on W2, but increases it by 8% on W3.

이유: 최대값은 참이어도 전체 결과를 대표하는 요약으로는 불충분했다. 실제 있는 regression을 함께 드러냈다. workload별 비율을 임의로 평균 내어 ‘평균 개선’으로 보고하지 않았다. 긴 목록이 있는 실제 논문에서는 적절한 집계와 주요 악화 조건을 고르고 전체 결과 위치를 함께 제시할 수 있다.

## 16. 대리 지표와 직접 결과 구분 — 과장 정정

주어진 사실: workload W에서 baseline B 대비 LLC miss가 20% 적다. 실행시간과 에너지 측정은 없다.

Before:

> A improves performance and energy efficiency by 20% over B.

After:

> On workload W, A incurs 20% fewer LLC misses than B.

별도 코멘트: “20%는 LLC miss에 대한 수치입니다. 성능·에너지 개선을 유지하려면 해당 지표의 근거가 필요합니다. 지금 제공된 결과는 에너지 효과가 없다는 증거도 아닙니다.”

## 17. 운영 경험의 기여를 쓰기 — 새 알고리즘을 발명하지 않기

주어진 사실: 기존 스케줄러를 세 클러스터에서 6개월 운영한 기록이 있다. overload가 발생한 구간에 quota 설정 불일치가 관찰되었으며, 둘의 인과성은 분리하지 않았다. 새 알고리즘은 없다.

Before:

> We introduce a novel scheduling algorithm that eliminates overload in production.

After:

> We report a six-month operational study of an existing scheduler across three clusters. The study documents quota-configuration mismatches observed during overload episodes.

이유: 기존 시스템에서 얻은 관찰을 실제 기여로 표현했다. overload 제거, 인과관계, 새 알고리즘은 만들지 않았다. 유용한 일반적 교훈으로 발전시키려면 발생 조건·빈도·비교·전이 가능성을 제공된 기록에서 확인해야 하며, 운영 트랙이라는 이유만으로 이미 충분한 기여라고 보증하지 않는다.

## 18. 리뷰 우려와 선택적 확장 구분 — 구체적 수정 요청

주어진 사실: 초안은 평가 범위를 2–128 nodes로 명시하고, 표도 그 범위를 다룬다. 실행 설정은 있지만 반복 run 수와 오차 막대의 정의가 없다. 1,024 nodes에 대한 주장은 없다.

Before:

> The evaluation is weak. The authors must run at 1,024 nodes and add more experiments.

After:

> The evaluation covers the stated 2–128-node range. Please report the number of independent runs and define the error bars so readers can assess variability. Results at 1,024 nodes would extend the scope, but are not required by the paper's current scale claim.

이유: 확인한 강점, 판단에 필요한 설명, 현재 범위 밖 확장을 구별했다. 반복 정보가 없다고 결과 자체가 틀렸다고 단정하지 않았다. 변동성 판단이 핵심 결론에 영향을 주는지는 실제 결과와 함께 평가해야 한다.

## 19. 작은 동작 예제에서 설계 규칙으로 — 설명과 실험 구분

주어진 설계: 단일 sender가 큰 전송을 bounded chunk로 나눈다. 진행 중인 chunk는 선점하지 않고, 매 chunk 경계에서 대기 중인 높은 우선순위의 짧은 요청을 나머지 큰 전송보다 먼저 선택한다. 아래 trace는 설명을 위해 만든 상황이며 구현·성능 측정 결과가 아니다.

Before:

> Our scheduler uses chunking and prioritization to improve latency.

After:

> Consider an illustrative trace in which a short, high-priority request arrives while the sender is transmitting a chunk of a large transfer. The short request waits for the current chunk to finish. At the next chunk boundary, the sender selects the short request before continuing the large transfer. This trace illustrates the scheduling rule: at each chunk boundary, waiting short requests with higher priority take precedence over the remaining large transfer. It does not report measured latency.

이유: 구체적 도착·대기·선택 순서로 규칙을 설명했다. 경계 전 선점, 모든 workload의 개선, 수치, starvation 부재를 주장하지 않는다. 실제 논문에서는 예제 뒤에 정확한 우선순위 정의·동률 처리·공정성·비용 등 제공된 설계와 적용 범위를 설명해야 한다. 이 한 trace가 일반적 correctness나 성능 효과의 근거는 아니다.

## 20. 독자의 오해를 실제 문장 수정으로 — 필요조건 보존

주어진 사실: occupancy < 64는 admission의 필요조건이지만 충분조건은 아니다. 이 조건을 만족해도 admission은 다른 이유로 실패할 수 있다. 다른 이유의 구체적 메커니즘은 제공되지 않았다. 독자는 아래 문장이 occupancy가 64보다 작으면 항상 admission이 성공한다는 뜻인지 물었다.

Before:

> Admission depends on whether occupancy is below 64.

After:

> Admission requires occupancy to be below 64. This condition is necessary but not sufficient: admission may still fail when occupancy is below 64.

이유: 독자의 해석을 기술적 사실로 받아들이거나 반박 답변만 작성하지 않고, 본문의 모호한 관계를 고쳤다. `<`를 `≤`로 바꾸거나 미제공 실패 원인을 만들지 않았다. 어떤 추가 조건이 필요한지는 별도 확인 사항으로 남긴다.

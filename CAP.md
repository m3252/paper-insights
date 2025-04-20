# CAP 정리 발표 후 12년 - '규칙'은 어떻게 변했는가

---

## 📌 TL;DR

CAP 정리 이후 12년이 지난 시점에서 Eric Brewer가 오해를 바로잡고, 실제 시스템 설계에서의 현실적인 트레이드오프를 설명한 회고 논문.

---

## 핵심 요약

### 1. CAP에 대한 흔한 오해

- C, A, P 중에서 **둘만 선택하는 게 아님**
- **"네트워크 파티션이 발생했을 때"에만 C와 A를 동시에 만족할 수 없음**

### 2. P(Partition tolerance)는 기본 전제

- 파티션은 현실적으로 피할 수 없음 → **항상 고려 대상**
- CAP은 결국 **"C vs A"의 선택 문제**로 귀결됨

### 3. 실제 시스템은 이분법으로 나뉘지 않음

- CA/CP/AP로 정확히 나눌 수 없음
- 대부분의 시스템은 **일관성과 가용성 사이의 스펙트럼** 어딘가에 위치함

### 4. 일관성(Consistency)은 단일하지 않다

- Strong consistency vs Eventual consistency 외에도 다양한 중간 모델 존재:
    - Causal consistency, Monotonic reads, Read-your-writes 등

### 5. 가용성(Availability)도 절대적인 개념이 아님

- "응답 있음"이 끝이 아니라, **정확하고 시의적절한 응답 여부**도 중요
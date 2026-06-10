# Safety Training Platform (STS)

> Unity 기반 메타버스 안전 교육 플랫폼

---

## 프로젝트 개요

| 항목 | 내용 |
|------|------|
| 개발 기간 | 2023.09 ~ 2023.11 (약 3개월) |
| 개발 인원 | 5명 (팀 프로젝트) |
| 역할 | Raycast 기반 상호작용 및 UI 기능 구현, 이벤트 로직 설계 참여 |
| 플랫폼 | Unity 기반 메타버스 |

---

## 기술 스택

| 구분 | 기술 |
|------|------|
| Engine | Unity |
| Language | C# |
| Tools | Visual Studio |

---

## 주요 기능

- CPR 및 화재 상황 시나리오 구현
- 사용자 이동 및 상호작용 기능
- 이벤트 기반 학습 진행 구조

---

## 문제 정의

<p align="center">
  <img src="./images/sts-problem1.PNG" width="45%">
  <img src="./images/sts-problem2.PNG" width="45%">
</p>

- 이론 중심 교육으로 실전 대응 능력 부족
- 실습 환경 부족으로 체험형 학습 어려움

---

## 핵심 구현

### 1. 시스템 구조 설계

<p align="center">
  <img src="./images/sts-architecture.PNG" width="50%">
</p>

- Unity 기반 기능 구조 설계
- 사용자 행동 중심 이벤트 흐름 구성

---

### 2. 사용자 인터랙션 환경 구현

<p align="center">
  <img src="./images/sts-ui1.PNG" width="45%">
  <img src="./images/sts-ui2.PNG" width="45%">
</p>

- 사용자 캐릭터 및 3D 환경 구성
- Unity 공간 내 이동 및 상호작용 구현
- 텍스트 안내 UI 기반 사용자 행동 유도
- 단계별 학습 흐름 제어 구조 설계

---

### 3. Raycast 기반 상호작용 구현

<p align="center">
  <img src="./images/sts-raycast.PNG" width="50%">
</p>
<p align="center">화재 진압 인터랙션</p>

- Raycast를 활용하여 사용자 시점에서 오브젝트 감지
- 소화기 오브젝트에 Raycast 적용 및 거리 기반 충돌 판정
- 불꽃 오브젝트와 충돌 시 Particle System을 탐색하여 자동으로 정지되도록 처리
- 사용자 행동 → 시스템 반응 구조 설계

---

## 트러블슈팅

### 이벤트 동시 발생으로 인한 흐름 충돌

**문제**
이벤트가 동시에 발생하면서 학습 흐름이 꼬이고 기능 충돌 발생

**해결**
이벤트 로직을 단계별로 분리하고 상태값 기반으로 이벤트 흐름 제어

**결과**
안정적인 인터랙션 구조 확보 및 사용자 경험 개선

---

## 데이터 흐름

```
사용자 행동 입력
      ↓
Raycast 기반 오브젝트 감지
      ↓
조건에 따른 이벤트 실행
      ↓
UI 안내 및 피드백 제공
```

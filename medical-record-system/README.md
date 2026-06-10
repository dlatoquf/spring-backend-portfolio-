# Admin Management System

> 가맹점 및 영업점의 기본 정보를 효율적으로 관리하고 대량 데이터 처리까지 고려한 웹 기반 관리자 시스템

---

## 프로젝트 개요

| 항목 | 내용 |
|------|------|
| 개발 기간 | 2025.03 ~ 2025.05 (약 3개월) |
| 개발 인원 | 1인 (단독 개발) |
| 역할 | 기획, 화면 설계, 프론트엔드·백엔드 개발, DB 설계, 배포 및 운영 |
| 플랫폼 | Web |

---

## 기술 스택

| 구분 | 기술 |
|------|------|
| Backend | Java 17, Spring Framework, MyBatis |
| Frontend | HTML5, CSS3, JavaScript |
| Database | MariaDB, Oracle |
| Infra | Linux, Tomcat |
| Tools | Git |

---

## 주요 기능

- 영업점 정보 등록 / 수정 / 조회
- 조건별 검색 기능
- Excel 업로드 기반 대량 데이터 등록
- 데이터 유효성 검증
- 운영 환경 배포 및 유지보수

---

## 핵심 구현

### 1. 화면 설계 및 프론트엔드 개발

<p align="center">
  <img src="./images/list.PNG" width="50%">
</p>
<p align="center">가맹점 조회 및 리스트 화면</p>

<p align="center">
  <img src="./images/form-create-1.PNG" width="45%">
  <img src="./images/form-create-2.PNG" width="45%">
</p>
<p align="center">가맹점 등록 화면</p>

<p align="center">
  <img src="./images/form-create-3.PNG" width="50%">
</p>
<p align="center">결제모듈 등록 화면</p>

<p align="center">
  <img src="./images/form-create-4.PNG" width="50%">
</p>
<p align="center">영업점 등록 화면</p>

- 등록 / 조회 / 수정 화면 UI 직접 설계 및 구현
- 사용자 입력 흐름을 고려한 화면 구성
- JavaScript 기반 입력 검증 및 이벤트 처리

---

### 2. 데이터 처리 및 조회 로직

<p align="center">
  <img src="./images/search.PNG" width="50%">
</p>
<p align="center">조건별 검색 기능</p>

- MyBatis 기반 동적 쿼리로 조건별 검색 구현
- Controller / Service / Repository 구조로 역할 분리
- 다중 조건 검색 및 페이징 처리

---

### 3. Excel 대량 업로드 처리

<p align="center">
  <img src="./images/excel-template.PNG" width="45%">
  <img src="./images/excel-upload.PNG" width="45%">
</p>
<p align="center">엑셀 대량등록 템플릿 및 업로드</p>

- Excel 데이터 파싱 후 DB 일괄 저장
- 필수값 및 형식 유효성 검증 로직 구현
- 잘못된 데이터가 DB에 저장되지 않도록 예외 처리

---

### 4. Linux 서버 배포 및 운영

- Linux 환경에서 애플리케이션 배포 및 실행 환경 구성
- 로그 분석을 통한 오류 원인 파악 및 문제 해결
- 운영 중 발생한 이슈 대응 및 서비스 안정성 유지

---

## 트러블슈팅

### Excel 업로드 데이터 검증 문제

**문제**
Excel 업로드 시 데이터 형식 오류 또는 필수값 누락으로 인해 정상 처리되지 않는 문제 발생

**해결**
업로드 단계에서 유효성 검증 로직을 추가하여 잘못된 데이터가 DB에 저장되지 않도록 처리

**결과**
데이터 정합성을 유지하면서 안정적인 대량 데이터 처리 가능

---

## 데이터 흐름

```
사용자 입력 / Excel 업로드
        ↓
  데이터 유효성 검증
        ↓
   검증된 데이터 DB 저장
        ↓
  조건 기반 데이터 검색 및 반환
```

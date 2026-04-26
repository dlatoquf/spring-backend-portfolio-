# 🧑‍💻 Admin Management System
> 가맹점 및 영업점의 기본 정보를 효율적으로 관리하고  
대량 데이터 처리까지 고려한 웹 기반 관리자 시스템 (End-to-End 개발)

---

## 📌 프로젝트 개요

* 프로젝트명: Admin Management System  
* 개발 기간: 2025.03 ~ 2025.05 (약 3개월)  
* 개발 인원: 1명 (단독 프로젝트)  
* 역할: 기획, 화면 설계, 프론트엔드 및 백엔드 개발, DB 설계, 배포 및 운영  
* 플랫폼: Web  

---

## 🛠 개발 환경

* Language: Java 17, JavaScript  
* Frontend: HTML5, CSS3, JavaScript  
* Framework: Spring Framework, MyBatis  
* DB: MariaDB / Oracle  
* Server: Linux (직접 배포 및 운영)  
* WAS: Tomcat  
* 형상관리: Git  

---

## 🚀 핵심 성과
- Excel 대량 업로드 기능 구현으로 반복 입력 업무 효율 개선  
- 데이터 유효성 검증 로직을 통해 잘못된 데이터 입력 방지  
- 화면 설계부터 프론트엔드, 백엔드, 배포까지 전 과정 직접 수행  
- Linux 환경에서 배포 및 운영 유지보수 경험  
- Git을 활용한 코드 버전 관리  

---

## 📌 프로젝트 소개
가맹점과 영업점의 기본 정보를 등록, 수정, 조회할 수 있는 웹 기반 관리 시스템입니다.  

단순 기능 구현을 넘어  
👉 화면 UI 설계 → 프론트엔드 → 백엔드 → 서버 배포 및 운영까지  
전 과정을 직접 수행하며 서비스 흐름을 전체적으로 경험했습니다.  

특히 반복적인 수작업 입력의 비효율을 개선하기 위해  
👉 **Excel 대량 업로드 기능을 구현하여 데이터 처리 효율을 개선했습니다.**

---

## ⚙️ 주요 기능
- 영업점 정보 등록 / 수정 / 조회  
- 조건별 검색 기능  
- Excel 업로드 기반 대량 데이터 등록  
- 데이터 유효성 검증  
- 운영 환경 배포 및 유지보수  

---

## 🔥 핵심 구현

### 1. 화면 설계 및 프론트엔드 개발

<p align="center">
  <img src="./images/list.PNG" width="50%">
</p>
<p align="center">가맹점 조회 및 리스트 화면</p>
<div style="display:flex; justify-content:center; gap:10px;">
  <img src="./images/form-create-1.PNG" width="42%">
  <img src="./images/form-create-2.PNG" width="42%">
</div>

<div style="display:flex; justify-content:center; gap:10px; margin-top:10px;">
  <img src="./images/form-create-3.PNG" width="42%">
  <img src="./images/form-create-4.PNG" width="42%">
</div>

- 등록 / 조회 / 수정 화면 UI 직접 설계 및 구현  
- 사용자 입력 흐름을 고려한 화면 구성  
- JavaScript 기반 입력 검증 및 이벤트 처리  

---

### 2. 데이터 처리 및 조회 로직

<p align="center">
  <img src="./images/search.PNG" width="50%">
</p>
<p align="center">조건별 검색 기능</p>

- MyBatis 기반 SQL 작성  
- 조건별 검색 기능 구현  
- 동적 쿼리를 활용한 데이터 조회 구조 설계  

---

### 3. Excel 대량 업로드 처리

<p align="center">
  <img src="./images/excel-template.PNG" width="45%">
  <img src="./images/excel-upload.PNG" width="45%">
</p>

- Excel 데이터를 파싱하여 DB에 일괄 저장  
- 필수값 및 형식 검증 로직 구현  
- 잘못된 데이터 입력을 사전에 방지  

---

### 4. Linux 서버 배포 및 운영

- Linux 환경에서 애플리케이션 배포 및 실행 환경 구성  
- 로그 분석을 통한 오류 원인 파악 및 문제 해결  
- 운영 중 발생한 이슈 대응 및 서비스 안정성 유지  

---

### 5. Git 기반 코드 관리

- Git을 활용한 버전 관리 및 기능 단위 커밋 수행  
- 변경 이력 추적을 통한 안정적인 유지보수  
- 체계적인 코드 관리 경험 확보  

---

## 💥 트러블 슈팅

### 문제
Excel 업로드 시 데이터 형식 오류 또는 필수값 누락으로 인해  
정상 처리되지 않는 문제 발생  

### 해결
업로드 단계에서 데이터 유효성 검증 로직을 추가하여  
잘못된 데이터가 DB에 저장되지 않도록 처리  

### 결과
데이터 정합성을 유지하면서 안정적인 대량 데이터 처리 가능  

---

## 📊 데이터 흐름
1. 사용자 입력 또는 Excel 업로드  
2. 데이터 유효성 검증  
3. 검증된 데이터 DB 저장  
4. 조회 요청 시 조건 기반 데이터 검색 및 반환  

---

## 👨‍💻 개발 회고

이 프로젝트를 통해 단순 CRUD 구현을 넘어  
👉 **데이터 처리 + 사용자 경험 + 운영 안정성을 함께 고려하는 개발의 중요성**을 체감했습니다.  

---

### 🚀 Spring 기반 설계 경험

- Controller / Service / Repository 구조로 역할 분리  
- MyBatis 기반 데이터 처리 로직 설계  

👉 **유지보수성과 확장성을 고려한 개발 방식 이해**

---

### 📊 데이터 처리 경험

- 다중 조건 검색 및 페이징 처리  
- 동적 쿼리 기반 데이터 조회 설계  

👉 **성능과 유지보수성 고려한 데이터 처리 경험 확보**

---

### 🔒 데이터 정합성

- 입력 단계 유효성 검증 적용  
- Excel 업로드 시 데이터 검증 및 예외 처리  

👉 **운영 환경 기준 데이터 안정성 확보**

---

### 🎯 성장 방향

👉 **운영 환경을 고려한 백엔드 개발자로 성장**  
앞으로는  
👉 Spring Boot / JPA 기반 확장 가능한 구조 설계 역량 강화 예정

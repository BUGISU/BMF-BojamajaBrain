# 🧠 보자마자 브레인 (BOJAMAJA BRAIN)

인지력 향상 및 치매 예방을 위한 시니어 대상 인터랙티브 드래그 앤 드롭 콘텐츠입니다. Unity 기반으로 제작되어 있으며 Leap Motion 및 안면 인식 시스템을 활용하여 몰입감 있는 사용자 경험을 제공합니다.

---

## 프로젝트 개요

* **프로젝트명**: 보자마자 브레인 / 라이트 / M / ENG
* **개발 기간**: 2022.06 \~ 2023.03 (10개월)
* **플랫폼**: Windows (PC), Android (모바일), Mini PC (Lite 버전)
* **기술 스택**:

  * `Unity3D`
  * `C#`
  * `Leap Motion SDK`
  * `OpenCV (Face Recognition)`
  * `Android Build Support`

---

## 프로젝트 구조 정보

### 주요 CSV 데이터

* `ProverbList.csv`, `CalculationList.csv`, `ColorList.csv`, `FourWordList.csv`, `ObjectList.csv` 등 각 게임의 문제 프리셋 데이터로 사용

### English\_ver 디렉토리

#### 공통 시스템 스크립트

* `GameAppManager.cs`, `FinishManager.cs`, `BreakTimeUIManager.cs`
* `CSVReader.cs`, `CSVFile.cs` 등 텍스트 및 데이터 로드 관리 기능

#### Leap Motion 손동작 게임

* `GestureManager.cs`, `LeftHandSelect.cs`, `RightHandSelect.cs`
* `FlagUpChecker.cs`, `FlagDownChecker.cs`, `FlagCenterChecker.cs`

#### Touch 게임

* `Touch/Touch_TextBoldChange.cs`, `Touch_TimerManager.cs`
* `DementiaGameX_UIManager.cs`, `BrainGameX_DataManager.cs`

#### 체조

* `Gymnastics/Gymnasics_UIManager.cs`

---

## 🧪 빌드 및 실행

### 1. 개발 환경

* Unity Version: `2021.3.x LTS` 또는 `2022.3.x LTS`
* Android Build Support / Windows Standalone 지원
* Leap Motion SDK (v4 이상 권장)

### 2. 실행 방법

#### ▶ PC (Windows)

1. Unity 에디터에서 프로젝트 열기
2. `Scenes/Main.unity` 실행
3. `Build Settings > Platform: PC, Mac & Linux` 선택 후 Build

#### ▶ Android

1. `Player Settings > Android`로 전환
2. 안면 인식 / Leap 관련 기능 제거된 버전 사용
3. APK 빌드 후 모바일 디바이스 설치

---

## 🔧 버전별 차이

| 버전             | 특징                        |
| -------------- | ------------------------- |
| **기본**         | Leap Motion + 안면 인식 전체 포함 |
| **LITE**       | Leap Motion 제거, 미니PC 최적화  |
| **ENG**        | 영문화 버전, 개정된 게임 구조         |
| **M(Android)** | 모바일 최적화, 체조 콘텐츠 제거        |

---

## 👨‍💼 기여 내용

* 전체 게임 시스템 및 UI 구조 설계
* 콘텐츠별 씬 구성 및 게임 로직 구현
* 손 인식 입력 처리 및 제스처 기반 UX 적용
* 영문화 적용을 위한 텍스트 시스템 개선
* 사용자 튜토리얼 / 휴식 기능 추가

---

## 🤔 주요 게임 목록

<details>
<summary>뇌훈련 게임</summary>

* 표에서 단어 찾기
* 음식값 계산하기
* 숫자판 순서대로 터치하기
* 단어 색깔 맞추기
* 반전된 글자 맞추기
* 거울 시계 시간 맞추기

</details>

<details>
<summary>치매예방 게임</summary>

* 속담-그림 맞추기
* 남아있는 글자를 넣어 단어 완성하기
* 미로 찾기
* 연속 숫자 계산 등

</details>

<details>
<summary>Leap Motion 손게임</summary>

* 가위바위보 (승/패)
* 청기백기
* 손가락 셈하기

</details>

---

## 📦 제품 정보

* [📦 네이버 스마트스토어 링크](https://smartstore.naver.com/gateways/products/7826529818)

---

## 📜 참고 이미지 / 경로

<details>
<summary>게임 및 UI 예시 스크린샷</summary>

### 메인 UI 및 게임 선택

<img src="https://github.com/JISUSAMA/JISUSAMA/assets/38304918/706d6e9b-8317-4a0a-907b-65a67d2ae2d3" width="600">

### 손동작 게임 (가위바위보)

<img src="https://github.com/JISUSAMA/JISUSAMA/assets/38304918/f3d91247-9776-4d26-a369-ee4bb1861e06" width="600">

### 인지 게임 진행 중 예시

<img src="https://github.com/JISUSAMA/JISUSAMA/assets/38304918/f4747049-83f1-4c50-8e20-8878045d2a08" width="600">

### 튜토리얼 ON/OFF 토글 적용 UI

<img src="https://github.com/JISUSAMA/JISUSAMA/assets/38304918/e3bcb219-b2a0-4892-8d6d-829aa5cae865" width="600">

### 체조 콘텐츠 예시 화면

<img src="https://github.com/JISUSAMA/JISUSAMA/assets/38304918/a144bbad-40e6-4aaa-819b-47cecfa5191c" width="600">

### Leap Motion 제외 Lite 버전

<img src="https://github.com/JISUSAMA/JISUSAMA/assets/38304918/f8ab14d3-22ab-496d-9803-873a5a8c54f5" width="600">

### ENG 버전 콘텐츠 예시

<img src="https://github.com/JISUSAMA/JISUSAMA/assets/38304918/e1a8433c-9cdf-4945-bbec-df4a3fbff8b1" width="600">

### Gabor Eye Training 콘텐츠 예시

<img src="https://github.com/JISUSAMA/JISUSAMA/assets/38304918/8a847fa6-8973-4003-849c-f1b528fe645a" width="600">

### 전체 기능 설계 이미지

<img src="https://github.com/JISUSAMA/JISUSAMA/assets/38304918/04b0fc8b-57f1-47a5-94c5-8e5905adc8b0" width="600">

</details>

---

## 📩 문의

developer contact: **[j2su0218@gmail.com](mailto:j2su0218@gmail.com)**

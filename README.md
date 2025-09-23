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

## 🔍 주요 기술 세부 설명

### 🎮 Unity3D 기반 모듈화 구조

* PC/Android/미니PC 버전별 기능 분기 처리
* 씬 단위 독립 설계 + 공통 매니저(`GameAppManager`, `FinishManager` 등) 기반 흐름 제어

### 📋 CSV 기반 콘텐츠 구성 시스템

* 외부 CSV 파일 기반 문제 프리셋 로드
* 다국어 대응을 고려한 텍스트 외부화

```csharp
string[][] csvData = CSVReader.Read("ColorList.csv");
foreach (string[] line in csvData)
{
    // 문제 및 선택지 로딩 처리
}
```

### ✋ Leap Motion 손 제스처 인식

* 손가락 개별 인식 (엄지/검지/소지) 기반 제스처 처리
* 게임별 제스처 분기 (`GestureManager.cs` 중심)

### 👁 OpenCV 기반 얼굴 인식 (Windows)

* 로그인 및 사용자별 맞춤 게임 자동 분기
* `PlayerPrefs` 또는 SQLite 기반 정보 저장·불러오기

### 📱 플랫폼 차등화

| 버전          | 특징                              |
| ----------- | ------------------------------- |
| **ENG**     | 전체 UI·튜토리얼 영문화                  |
| **Lite**    | Leap Motion/체조 기능 제거, 저사양 PC 대응 |
| **Android** | 터치 입력 대응, 체조 기능 제거              |

---

## 🔁 게임 공통 흐름

```
데이터 로딩 → 문제 셋업 → 입력 처리 → 피드백 → 점수 계산 → 종료 처리
```

---

## 👨‍💼 My Contributions

* 뇌훈련게임(7종), 치매예방게임(8종), 손게임(5종) **UI 수정 및 재구현**
* **가보르아이 트레이닝 콘텐츠** 신규 설계 및 제작
* **튜토리얼 시스템** 설계 및 ON/OFF 기능 추가
* 사용자 테스트 분석 기반 **UI/UX 개선 및 로직 수정**
* **영문 버전 제작 및 다국어(Localization) 지원**
* **모바일 전용 앱 개발**로 플랫폼 확장 및 접근성 강화

---

## 게임 목록 정리

| 카테고리            | 게임 이름         | 설명                    | 이미지                                                            |
| --------------- | ------------- | --------------------- | -------------------------------------------------------------- |
| 뇌훈련 게임          | 표에서 단어 찾기     | 글자 표에서 단어를 찾아 클릭하는 게임 | <img src="Screenshots/1_표를 보고 단어 찾아 터치하기_2.png" width="200"/>  |
| 뇌훈련 게임          | 음식값 계산하기      | 주어진 메뉴와 가격으로 계산하는 게임  | <img src="Screenshots/2_음식값 계산하기_2 _ 2.png" width="200"/>      |
| 뇌훈련 게임          | 숫자판 순서대로 터치하기 | 숫자를 작은 것부터 순서대로 터치    | <img src="Screenshots/4_숫자판 순서대로 터치하기.png" width="200"/>       |
| 뇌훈련 게임          | 단어 색깔 맞추기     | 글자와 색이 일치하는지 판단       | <img src="Screenshots/5_단어 색깔 맞추기 _ 1.png" width="200"/>       |
| 뇌훈련 게임          | 반전된 글자 맞추기    | 거꾸로 쓰인 글자를 맞추는 게임     | <img src="Screenshots/6_반전 틀린 글자 맞추기 _ 1.png" width="200"/>    |
| 뇌훈련 게임          | 거울 시계 시간 맞추기  | 반전된 시계 시간을 맞추는 게임     | <img src="Screenshots/7_거울 시계 시간 맞추기 _ 1.png" width="200"/>    |
| 치매예방 게임         | 속담-그림 맞추기     | 속담과 어울리는 그림을 연결       | <img src="Screenshots/2.png" width="200"/>                     |
| 치매예방 게임         | 글자 채워 단어 완성   | 빈칸에 글자를 넣어 단어 완성      | <img src="Screenshots/1_빈칸에 글자 채워 낱말 완성하기_3.png" width="200"/> |
| 치매예방 게임         | 미로 찾기         | 출발점에서 도착점까지 길 찾기      | <img src="Screenshots/maze.png" width="200"/>                  |
| 치매예방 게임         | 연속 숫자 계산      | 규칙에 맞는 연속 숫자 계산하기     | <img src="Screenshots/8_연속숫자계산하기_3.png" width="200"/>          |
| Leap Motion 손게임 | 가위바위보         | 손동작 인식으로 승패 결정        | <img src="Screenshots/1_가위바위보이기기_4.png" width="200"/>          |
| Leap Motion 손게임 | 청기백기          | 지시에 맞게 손을 들어 올리기      | <img src="Screenshots/5_청기백기 게임_2.png" width="200"/>           |
| Leap Motion 손게임 | 손가락 셈하기       | 손가락 개수를 인식해 숫자 맞추기    | <img src="Screenshots/3_손가락 셈 하기(숫자)_3.png" width="200"/>      |

### Gabor Eye Training 콘텐츠 예시

| 난이도 선택                                      | 가보르 아이 트레이닝                                 | 같은 그림 찾기                                    |
| ------------------------------------------- | ------------------------------------------- | ------------------------------------------- |
| <img src="Screenshots/17.png" width="250"/> | <img src="Screenshots/16.png" width="250"/> | <img src="Screenshots/18.png" width="250"/> |


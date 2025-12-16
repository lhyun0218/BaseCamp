# 🎨 BaseCamp 3회차: CSS 기본 및 박스 모델 학습 (프론트엔드)

안녕하세요. 프론트엔드 부트캠프 BaseCamp 3회차 학습을 환영합니다!
이번 회차에서는 HTML로 만든 구조에 **스타일**을 입히는 **CSS의 기본 사용법, 선택자, 그리고 핵심 개념인 박스 모델**을 집중적으로 다루었습니다.

---

### 📁 실습 파일 구조

이번 학습에서 다룬 CSS 관련 파일 목록입니다.

BaseCamp/ 
├── 3회차/ │ 
├── 19_CSS문서_사용하기.html # CSS 적용 방식 (Inline, Internal, External) │ 
├── 19_CSS문서_사용하기.css # 외부 CSS 파일 │ 
├── 20.html # 선택자 (Selector) 및 우선순위 │ 
├── 21.html # 박스 모델 - width/height │ 
├── 22.html # 박스 모델 - border (테두리) │ 
├── 23.html # 박스 모델 - margin/padding (여백) │ 
├── 24.html # 배경 (Background) 속성 │ 
├── 25.html # 색상 지정 방법 (RGB, Hex, HSL) │ 
├── 26.html # 텍스트 및 폰트 스타일 │ 
|
├── css_profile.html # CSS 적용 프로필 페이지 (HTML) │ 
└── styles.css # CSS 적용 프로필 페이지 (CSS)

### 🎯 학습 목표

* 웹 문서에 CSS를 **적용하는 3가지 방식**을 이해하고 사용할 수 있습니다.
* **선택자(Selector)**를 활용하여 원하는 HTML 요소에 정확하게 스타일을 적용할 수 있습니다.
* CSS의 핵심 개념인 **박스 모델(Box Model)**을 이해하고, 크기(width/height) 및 여백(margin/padding)을 제어할 수 있습니다.
* 다양한 속성(배경, 색상, 폰트)을 사용하여 요소를 시각적으로 꾸밀 수 있습니다.

---

### 📚 주요 학습 내용 및 실습 코드 분석

#### 1. CSS 적용 방식 (`19_CSS문서_사용하기.html` 분석)

CSS를 HTML에 적용하는 방법은 **인라인**, **내부**, **외부** 3가지가 있으며, 적용 우선순위가 있습니다. 인라인 스타일이 가장 우선하며, 그 외에는 나중에 선언된 스타일이 적용됩니다.

#### 2. CSS 선택자 (Selector) 및 우선순위 (`20.html` 분석)

* **전체 선택자** (`*`)
* **태그 선택자** (`li`)
* **클래스 선택자** (`.hiphop`)
* **아이디 선택자** (`#poppin`)
* **그룹 선택자** (`h2, p, li`)

> **선택자 우선순위**: ID > 클래스 > 태그 (우선순위가 같으면 나중에 작성된 것이 적용됩니다.)

#### 3. 박스 모델 (Box Model)

모든 HTML 요소는 Content, Padding, Border, Margin으로 구성된 사각형 박스로 간주됩니다. 

##### 크기 및 테두리 (`21.html`, `22.html` 분석)

* `width`, `height`: **Content** 영역의 크기를 지정합니다. (`px`, `%` 사용)
* `border`: 테두리 설정 (`border: 3px solid green;`와 같은 단축 속성 사용)
* `border-radius`: 테두리를 둥글게 처리합니다.

##### 여백 설정 (`23.html` 분석)

* `padding`: **안쪽 여백** (Content와 Border 사이)을 설정합니다.
* `margin`: **바깥쪽 여백** (Border 바깥)을 설정합니다.
    * `margin: auto;`를 사용하여 **블록 요소**를 부모 요소 중앙에 배치할 수 있습니다 (너비가 지정되어 있을 경우).
* `box-sizing`: 박스 크기 계산 기준을 `content-box` (기본값) 또는 `border-box`로 설정하여 `width`/`height`가 padding과 border를 포함할지 결정합니다.

#### 4. 배경 및 색상 (`24.html`, `25.html` 분석)

* **배경 속성**: `background-color`, `background-image`, `background-repeat`, `background-size` 등으로 배경을 꾸밉니다.
* **색상 표기법**:
    * **RGB/RGBA**: `rgb(R, G, B)` (예: `rgb(0%, 50%, 0%)`)
    * **HEX**: 16진수 코드 (예: `#FF00FF99`)
    * **HSL/HSLA**: 색상, 채도, 명도 기반 (예: `hsla(300, 50%, 50%, 0.3)`)

#### 5. 텍스트 및 폰트 스타일 (`26.html` 분석)

* `font-family`: 글꼴 지정. (외부 폰트도 연결하여 사용)
* `font-size`: 글자 크기. (`px`, `em`, `rem` 단위 이해)
* `line-height`: 줄 간격 설정.
* `text-align`: 텍스트 정렬.

### 💡 종합 실습: `css_profile.html` 및 `styles.css` 분석

이 실습에서는 1회차에 만든 HTML 프로필 페이지에 외부 CSS 파일(`styles.css`)을 연결하여 스타일을 적용했습니다.

| 요소 | `styles.css` 주요 스타일 적용 | 학습 내용 연결 |
| :--- | :--- | :--- |
| `body` | `width: 640px;`, `margin: auto;` | **박스 모델: `width`와 중앙 정렬** |
| `nav` | `background-color`, `border-radius`, `box-shadow` | **배경, 테두리, 시각 효과** |
| `nav a` | `margin: 45px;`, `text-decoration: none;` | **여백 설정, 텍스트 스타일** |
| `a:hover` | `color: rgb(206, 255, 255);` | **가상 클래스 선택자** (`:hover`) |
| `*` (전체) | `font-family: "Gamja Flower", sans-serif;` | **폰트 적용** |

#### 주요 코드 분석 (styles.css)

```css
/* 페이지 전체 텍스트를 중앙 정렬하고 폰트 적용 */
* {
    text-align: center; 
    font-family: "Gamja Flower", sans-serif;
    /* ... */
}

/* body에 너비를 주고 좌우 margin을 auto로 설정하여 중앙에 배치 */
body {
    width: 640px;
    margin: auto; 
}

/* nav 메뉴에 배경색, 둥근 모서리, 그림자 효과 적용 */
nav {
    background-color: rgb(158, 158, 158);
    border-bottom-left-radius: 5px ;
    border-bottom-right-radius: 5px ;
    box-shadow: 0 3px 10px rgb(80, 80, 80);
}

/* a 태그에 마우스를 올렸을 때(hover) 색상 변경 */
a:hover{
    color: rgb(206, 255, 255);
}

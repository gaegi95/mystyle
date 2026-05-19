# 🏠 김종한의 HTML 포트폴리오 복습 노트

> **GitHub:** [gaegi95/mystyle](https://github.com/gaegi95/mystyle)  
> **언어 구성:** HTML 72.7% / CSS 27.3%  
> **총 커밋:** 16회 | **총 작품:** 6개

---

## 📂 프로젝트 구조

```
mystyle/
├── kjhcss/          ← CSS 스타일시트 폴더
│   ├── style.css    ← index 전용 스타일
│   └── animal.css   ← animal 전용 스타일
├── index.html       ← 메인 포트폴리오 허브
├── animal.html      ← 동물 소개 (기초)
├── book.html        ← 독서 목록 (기초)
├── movie.html       ← 영화 리뷰 (기초)
├── recipe.html      ← 레시피 (기초)
├── timetable.html   ← 시간표 (심화)
└── boxoffice.html   ← 박스오피스 (심화)
```

---

## 📄 작품별 상세 복습

---

### 1️⃣ index.html — 메인 포트폴리오 허브

**핵심 구조:**
```html
<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>index</title>
  <link rel="stylesheet" href="kjhcss/style.css">
</head>
<body>
  <header>...</header>
  <main>
    <section>작품 목록 테이블</section>
    <section>배운 태그 목록</section>
    <section>유용한 링크</section>
    <form>방문자 메모</form>
  </main>
  <footer>...</footer>
</body>
</html>
```

**사용한 태그 정리:**

| 태그 | 역할 | 사용 예시 |
|------|------|-----------|
| `<header>` | 페이지 상단 영역 | 제목 + 프로필 이미지 |
| `<main>` | 본문 핵심 영역 | 작품목록, 태그, 링크, 폼 |
| `<section>` | 주제별 구분 | 각 섹션을 의미 있게 분리 |
| `<footer>` | 페이지 하단 | 저작권 표기 |
| `<h1>~<h2>` | 제목 태그 | 계층 구조 표현 |
| `<strong>` | 굵게 강조 | 이름 강조 |
| `<em>` | 기울임 강조 | 자기소개 문구 |
| `<hr>` | 수평선 구분선 | 섹션 사이 구분 |
| `<img>` | 이미지 삽입 | 프로필 사진 |

**테이블 구조 (핵심 포인트!):**
```html
<table border="1" class="nav">
  <caption><strong>HTML 실습 작품 모음</strong></caption>
  <thead>
    <tr>
      <th colspan="4">나의 HTML 작품 포트폴리오</th>  ← 4칸 병합!
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="4">기초과정</td>  ← 4행 세로 병합!
      <td>🐾 동물 소개</td>
      <td>좋아하는 동물 소개 페이지</td>
      <td><a href="..." target="_blank">보기</a></td>
    </tr>
    <!-- 나머지 3개 행: td가 3개씩 (rowspan된 칸 제외) -->
  </tbody>
  <tfoot>
    <tr>
      <th colspan="3">총 작품 수</th>
      <th>6개</th>
    </tr>
  </tfoot>
</table>
```

> 💡 **rowspan/colspan 핵심 규칙**
> - `rowspan="4"` → 해당 셀이 아래로 4행을 차지
> - `colspan="4"` → 해당 셀이 옆으로 4칸을 차지
> - rowspan된 셀이 있는 행은 그만큼 `<td>` 개수가 줄어들어야 함!

**폼(Form) 구조:**
```html
<form action="">
  <label for="">이름</label><br>
  <input type="text" placeholder="이름을 입력하세요"><br>

  <label for="">방문 경로</label><br>
  <select name="" id="">
    <option value="">직접 방문</option>
    <option value="">검색</option>
    <option value="">추천</option>
  </select><br>

  <label for="">메모</label><br>
  <textarea name="" id="" cols="40" rows="5" placeholder="방문 소감을 남겨주세요 😊"></textarea><br>

  <button type="submit">메모 남기기 ✉️</button>
</form>
```

---

### 2️⃣ animal.html — 고양이 소개 페이지 (기초)

**사용한 태그:**

| 태그 | 역할 | 실제 사용 |
|------|------|-----------|
| `<h1 id="main-title">` | 제목 + ID 속성 | 고양이 제목 |
| `<img src alt width title>` | 이미지 (속성 4개) | 고양이 사진 |
| `<h2 class="animal-name">` | 소제목 + class 속성 | 특징, 사는곳, 먹이 |
| `<ul><li>` | 순서없는 목록 | 특징 3가지 |
| `<strong>` | 굵게 | "독립적인" |
| `<u>` | 밑줄 | 털 색깔 |
| `<mark>` | 형광펜 강조 | "야행성" |
| `<em>` | 기울임 | 감상 문구 |
| `<p>` | 단락 | 설명 텍스트 |
| `<hr>` | 구분선 | 섹션 분리 |

**코드 구조:**
```html
<header>
  <h1 id="main-title">🐱고양이</h1>
  <img src="이미지URL" alt="고양이" width="150" title="괭이">
</header>

<main>
  <h2 class="animal-name">특징</h2>
  <ul>
    <li><strong>독립적인</strong> 성격이에요.</li>
    <li>털 색깔은 <u>주황, 흰색, 검정</u> 등 다양해요.</li>
    <li><mark>야행성</mark> 동물이에요.</li>
  </ul>
  <p><em>정말 귀엽고 사랑스럽죠!</em></p>
</main>
```

> 💡 **img 속성 4총사**
> - `src` : 이미지 경로 (필수)
> - `alt` : 대체 텍스트, 이미지 못 불러올 때 표시
> - `width` : 너비 (px)
> - `title` : 마우스 올렸을 때 툴팁 텍스트

---

### 3️⃣ timetable.html — 주간 시간표 (심화)

**rowspan + colspan 종합 활용 예제!**

```html
<table border="1">
  <caption><b>2025년 1학기 시간표</b></caption>
  <thead>
    <tr>
      <th>교시</th><th>월</th><th>화</th><th>수</th><th>목</th><th>금</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1교시</td>
      <td rowspan="2"><mark>체육</mark></td>  ← 1~2교시 월요일 합침
      <td><mark>수학</mark></td>
      <td>국어</td>
      <td>영어</td>
      <td><em>사회</em></td>
    </tr>
    <tr>
      <td>2교시</td>
      <!-- 월요일 td 없음! rowspan이 차지 중 -->
      <td>영어</td>
      <td rowspan="2"><mark>수학</mark></td>  ← 2~3교시 수요일 합침
      <td>미술</td>
      <td>국어</td>
    </tr>
    <tr>
      <td colspan="6">🍱 점심시간 (12:00 ~ 13:00)</td>  ← 6칸 전부 합침
    </tr>
  </tbody>
</table>
```

> 💡 **시간표 만들 때 핵심 체크리스트**
> - rowspan이 적용된 행에서는 해당 열의 `<td>` 생략할 것
> - colspan으로 전체 열을 합칠 때 열 개수를 정확히 셀 것 (여기선 6)
> - thead, tbody 구분을 명확하게 할 것

---

## 🛠️ 전체 학습 태그 총정리

### 텍스트 태그
| 태그 | 의미 | 예시 |
|------|------|------|
| `<h1>~<h6>` | 제목 (크기 순) | `<h1>제목</h1>` |
| `<p>` | 단락 | `<p>내용</p>` |
| `<strong>` | 굵게 (의미 강조) | `<strong>중요</strong>` |
| `<em>` | 기울임 (의미 강조) | `<em>강조</em>` |
| `<u>` | 밑줄 | `<u>밑줄</u>` |
| `<mark>` | 형광펜 | `<mark>하이라이트</mark>` |
| `<small>` | 작은 글씨 | `<small>주석</small>` |
| `<b>` | 굵게 (시각만) | `<b>굵게</b>` |
| `<br>` | 줄바꿈 | 단독 태그 |
| `<hr>` | 수평선 | 단독 태그 |

### 목록 태그
| 태그 | 의미 | 특징 |
|------|------|------|
| `<ul>` | 순서없는 목록 | 점(●) 으로 표시 |
| `<ol>` | 순서있는 목록 | 번호로 표시 |
| `<li>` | 목록 항목 | ul/ol 안에 사용 |

### 링크/미디어 태그
| 태그 | 의미 | 주요 속성 |
|------|------|-----------|
| `<a>` | 하이퍼링크 | `href`, `target="_blank"` |
| `<img>` | 이미지 | `src`, `alt`, `width`, `title` |

### 테이블 태그 (★ 핵심!)
| 태그 | 의미 | 역할 |
|------|------|------|
| `<table>` | 표 전체 | `border` 속성으로 테두리 |
| `<caption>` | 표 제목 | 표 위에 표시 |
| `<thead>` | 표 머리 | 헤더 행 그룹 |
| `<tbody>` | 표 본문 | 데이터 행 그룹 |
| `<tfoot>` | 표 하단 | 합계/요약 행 그룹 |
| `<tr>` | 행(row) | 가로 줄 |
| `<th>` | 헤더 셀 | 굵게+가운데 정렬 |
| `<td>` | 데이터 셀 | 일반 셀 |
| `colspan="n"` | 가로 병합 | n칸 옆으로 합치기 |
| `rowspan="n"` | 세로 병합 | n행 아래로 합치기 |

### 구조/폼 태그
| 태그 | 의미 | 특징 |
|------|------|------|
| `<header>` | 상단 영역 | 제목, 로고 등 |
| `<main>` | 본문 핵심 | 페이지 주요 내용 |
| `<footer>` | 하단 영역 | 저작권, 연락처 등 |
| `<section>` | 주제별 구분 | 의미 있는 섹션 |
| `<div>` | 레이아웃 구분 | 의미 없는 묶음 |
| `<span>` | 인라인 묶음 | 텍스트 일부 스타일링 |
| `<form>` | 입력 폼 | `action` 속성 |
| `<input>` | 입력 필드 | `type`, `placeholder` |
| `<select>` | 드롭다운 | `name`, `id` |
| `<option>` | 선택 항목 | `value` 속성 |
| `<textarea>` | 여러줄 입력 | `cols`, `rows` |
| `<button>` | 버튼 | `type="submit"` |
| `<label>` | 입력 설명 | `for` 속성 |

---

## 🔗 유용한 링크 (작품에서 사용)

- [GitHub](https://github.com/) — 코드 저장소 및 버전 관리
- [Gemini](https://gemini.google.com/app?hl=ko) — AI 협업 및 브레인스토밍
- [Figma](https://www.figma.com/ko-kr/) — UI/UX 디자인 및 기획

---

## ✅ 복습 체크리스트

- [ ] `<!DOCTYPE html>` 선언의 역할을 설명할 수 있다
- [ ] `<meta charset="UTF-8">` 이 왜 필요한지 안다
- [ ] `<thead>` / `<tbody>` / `<tfoot>` 차이를 안다
- [ ] `rowspan` 과 `colspan` 을 직접 써볼 수 있다
- [ ] `<strong>` 과 `<b>` 의 차이를 안다 (의미 vs 시각)
- [ ] `<em>` 과 `<i>` 의 차이를 안다
- [ ] `<a target="_blank">` 가 새 탭에서 열리는 이유를 안다
- [ ] `<img>` 의 4가지 속성(src, alt, width, title)을 안다
- [ ] `<form>` 안의 `<input>`, `<select>`, `<textarea>`, `<button>` 역할을 안다
- [ ] CSS 파일을 `<link>` 태그로 연결하는 방법을 안다

---

> 작성자: 김종한 | 2026 © All Rights Reserved  
> 포트폴리오: [gaegi95.github.io/mystyle](https://gaegi95.github.io/mystyle/index.html)

---
marp: true
title: Marp 작성법
header: header
footer: footer
paginate: true
theme: custom

---
<!-- _paginate: false -->

# Marp로 ppt 만들기
<span style='color: blue'>작성자: 김동규</span>

작성일자: 2024-08-13

---
# 목차

1. MARP란

2. MARP 활용법

3. MARP 스타일링

---
# MARP란

마크다운 언어로 작성된 .md파일을 쉽고 빠르게 **프리젠테이션 문서**로 변환할 수 있도록 도와주는 툴입니다.

## 장점

- 짧은 시간동안 사용해본 결과, **빠르게** 원하는 내용을 ppt 파일로 전달하기 좋습니다.
- 코드나 수식을 활용하여 만들기 좋습니다.
- css 파일을 만들어 **원하는 템플릿**, 글자 크기, 색상, 테이블이나 사진 크기 등을 저장하여 간편하게 만들 수 있습니다.

## 단점

- 위 장점은 ppt도 갖고 있습니다. 굳이 이걸 썼을 때의 장점은 코드 블럭을 활용할 수 있는 것 정도...?
- css로 커스터마이징해야 하는데 **상당히 많은 시간이 필요**합니다.
- ppt로 하면 금방할 걸 css로 따로 요소를 만들고 하면 오래 걸릴 것 같습니다.

---
# VS Code로 Marp 활용법

1. Marp for VS Code 익스텐션 설치합니다.

2. 마크다운 형식의 파일을 생성한 뒤 아래 코드를 입력하여 marp을 시작합니다.
```md
---
marp: true
---
```
3. 잘 나오는지 ctrl + k v를 눌러 확인합니다.
(Ctrl + Shift + V의 경우, 새 창을 열어 확인)

4. `---` 을 이용하여 페이지를 구분할 수 있습니다.

5. 이제 마크다운 문법으로 작성하면 알아서 ppt에 노출이 되게 됩니다.

---
# Marp 기본 스타일링

아래 리스트는 처음 marp: true를 작성했던 곳에 들어갑니다.

- title: 제목
- header: 상단에 들어갈 내용
- footer: 하단에 들어갈 내용
- paginate: ture -> 쪽 수 매기기
- theme: default 등 원하는 테마를 설정할 수 있습니다.

---
# Marp 이미지

오른쪽 사진처럼 위치와 크기를 지정할 수 있습니다.

```md
![bg right height:300px](cute_hamster.jpg)
```

![bg right height:300px](cute_hamster.jpg)

---
# HTML 스타일 적용

1. .vscode 폴더를 생성하여 settings.json파일을 만듭니다.
2. themes 폴더를 생성하여 원하는 css 파일을 올립니다.

settings.json 파일에 다음과 같이 코드를 작성합니다. 
```
{
    "markdown.marp.themes": [
      "./themes/파일명"
    ]
```

css 파일의 경우, 상단에 /* @theme 테마이름 */를 입력하여
md파일에 theme: 테마이름 을 지정하면 css 파일을 읽을 수 있습니다.
<br>

# 파일 추출

마지막으로 vscode 기준 상단 바에 오른쪽의 marp 로고를 클릭하여 export하면 ppt, HTML, pdf 등으로 추출할 수 있게 됩니다.

---
# 프로젝트 WBS

<div class="mermaid">
graph TD
    A[프로젝트] --> B[기획 단계]
    A --> C[개발 단계]
    A --> D[테스트 단계]
    B --> B1[요구사항 분석]
    B --> B2[설계]
    C --> C1[프론트엔드 개발]
    C --> C2[백엔드 개발]
    D --> D1[단위 테스트]
    D --> D2[통합 테스트]
</div>

---

# 앱 구조도
<div class="mermaid">
graph TD
    A[사용자 인터페이스] --> B[비즈니스 로직]
    B --> C[데이터 액세스 계층]
    C --> D[데이터베이스]
</div>

---

# 감사합니다
# Grid
## 정의
> CSS Grid는 웹 디자인에서 요소를 그리드 형태로 배치하고 레이아웃을 구성하기 위한 강력한 레이아웃 시스템입니다. Grid를 사용하면 웹 페이지의 요소들을 행과 열의 그리드로 구성하고, 이를 통해 요소들을 정렬하고 배치할 수 있습니다.

<br></br>
## Grid의 주요 속성들
- grid container
Grid를 적용할 요소를 컨테이너로 정의합니다. 이 컨테이너에 display: grid;를 적용하여 그리드 컨테이너로 만듭니다.
<br></br>
- grid item
Grid 컨테이너 내에서 배치하려는 요소들을 그리드 아이템으로 정의합니다.
<br></br>
- grid template
그리드 컨테이너의 행과 열 구조를 정의합니다. grid-template-columns 및 grid-template-rows 속성을 사용하여 템플릿을 만듭니다.
<br></br>
- grid gap
그리드 아이템 사이의 간격을 설정합니다. grid-gap 속성을 사용하여 열과 행 간격을 정의합니다.
<br></br>
- grid line
그리드 템플릿에서 열과 행의 가상 라인을 참조합니다. grid-column 및 grid-row 속성을 사용하여 요소를 특정 라인에 배치합니다.
<br></br>
- grid auto
자동 크기를 가진 그리드 아이템은 컨테이너의 남은 공간을 자동으로 채우거나 내용에 맞게 크기를 조정합니다.
<br></br>
- grid placement
grid-area, grid-column, grid-row 등의 속성을 사용하여 그리드 아이템을 특정 위치에 배치합니다.
<br></br>

## 활용 예시
```html
<div class="grid-container">
  <div class="grid-item">1</div>
  <div class="grid-item">2</div>
  <div class="grid-item">3</div>
  <div class="grid-item">4</div>
  <div class="grid-item">5</div>
  <div class="grid-item">6</div>
  <div class="grid-item">7</div>
  <div class="grid-item">8</div>
  <div class="grid-item">9</div>
</div>
```
<br></br>

## Properties
**1) column-gap**: column 간 간격 설정
```css
.grid-container {
  display: grid;
  column-gap: 50px;
}
```
**2) row-gap**: row 간 간격 설정
```css
.grid-container {
  display: grid;
  row-gap: 50px;
}
```
**3) gap**: 둘 다 설정
```css
.grid-container {
  display: grid;
  gap: 50px 100px;
}
```
**4) grid lines**: 라인의 column/row 시작/끝 등을 정의
```css
.item1 {
  grid-column-start: 1;
  grid-column-end: 3;
}
```

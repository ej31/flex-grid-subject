# Flex
## 정의
> CSS의 flex 속성은 웹 디자인에서 레이아웃을 관리하는 데 사용되는 중요한 속성 중 하나입니다. Flexbox(유연한 박스 레이아웃)는 요소 간의 공간 배분 및 정렬을 단순하게 만들어주며, 반응형 디자인을 구현하는 데 특히 유용합니다.

<br></br>
## Flex의 주요 속성들
- flex-grow
요소가 부모 컨테이너 내에서 얼마나 많은 공간을 확장할 수 있는지를 결정합니다. 이 값은 양의 정수 또는 기본값인 0이 될 수 있으며, 값이 큰 요소가 다른 요소보다 더 많은 공간을 차지합니다. 예를 들어, flex-grow: 2;는 같은 컨테이너 내에서 다른 요소에 비해 두 배 더 많은 공간을 차지하려고 시도할 것입니다.
<br></br>
- flex-shrink
요소가 부모 컨테이너 내에서 얼마나 많은 공간을 줄일 수 있는지를 결정합니다. 이 값도 양의 정수 또는 기본값인 1이 될 수 있으며, 값이 큰 요소가 다른 요소보다 더 많은 공간을 차지하려고 시도할 것입니다. 예를 들어, flex-shrink: 3;은 같은 컨테이너 내에서 다른 요소에 비해 세 배 더 많은 공간을 줄이려고 시도할 것입니다.
<br></br>
- flex-grow 및 flex-shrink는 보통 같은 요소에 적용됩니다. 이러한 두 속성을 결합하여 요소의 크기 조절을 관리할 수 있습니다. 또한, 기본적으로 모든 요소의 flex-shrink 값은 1이므로, 컨테이너 내에서 부족한 공간이 있을 때 모든 요소가 동일하게 축소됩니다.

<br></br>
## 활용 예시
```html
<div class="flex-container">
  <div>1</div>
  <div>2</div>
  <div>3</div>
</div>
```

```css
.container {
  display: flex;
}

.item {
  flex-grow: 1; /* 모든 아이템이 동일하게 확장됩니다. */
  flex-shrink: 1; /* 모든 아이템이 동일하게 축소됩니다. */
}

```
<br></br>
## Properties
**1) flex-direction**: flex-item들을 어떻게 쌓을지 결정
```css
.flex-container {
  display: flex;
  flex-direction: column;
  flex-direction: column-reverse;
  flex-direction: row;
  flex-direction: row-reverse;
}
```

**2) flex-wrap** : flex-item들이 wrap할지 아닐지를 결정
```css
.flex-container {
  display: flex;
  flex-wrap: wrap;
  flex-wrap: nowrap;
  flex-wrap: wrap-reverse;
}
```

**3) flex-flow**: flex-direction과 flex-wrap을 세팅하기 위한 직접적인 방법
```css
.flex-container {
  display: flex;
  flex-flow: row wrap;
}
```

**4) justify-content**: flex-item을 정렬하는데 사용
```css
.flex-container {
  display: flex;
  justify-content: center;
  justify-content: flex-start;
  justify-content: flex-end;
  justify-content: space-around;
  justify-content: space-between;
}
```
**5) align-items**: flex item들을 align하는 데 사용
```css
.flex-container {
  display: flex;
  height: 200px;
  align-items: center;
  align-items: flex-start;
  align-items: flex-end;
  align-items: stretch;
  align-items: baseline;
}
```
**6) align-content**: flex line들을 align하는 데 사용
```css
.flex-container {
  display: flex;
  height: 600px;
  flex-wrap: wrap;
  align-content: space-between;
  align-content: space-around;
  align-content: stretch;
  align-content: center;
  align-content: flex-start;
  align-content: flex-end;
}
```
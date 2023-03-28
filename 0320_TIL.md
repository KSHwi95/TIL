# DOM

> **Document Object Model**

- Html 웹 구조를 쉽게 파악할 수 있음.
- Dom에서 관계 (자식, 자손)의 관계는 '크롤링' 할 때 중요해짐.

**복습** <br>

1. `<Tag>`를 가지고 'Element'를 만든다.
2. 내가 지금 HTML을 배우는 것은 꾸미기 위함이 아니라 데이터를 가져오기 위함이다.

# 속성

1. id <br>
   **고유값**

- 전체 문서에서 '고유한' 단 하나만 부여 (**중복된 ID값 존재 X**)
  > 보이는 것을 위해 같게 설정을 할 수는 있지만, 개발에서 충돌이 일어남.

2. class <br>
   **묶어서 동일한 속성 부여**
   ≠ 파이썬의 클래스

- 중복이 가능하게 부여 가능
- 여러 개 부여 가능

# CSS

**C**ascading **S**tyle **S**heet <br>

**C**ascading

- 상위 요소의 스타일 속성을 바꿔주면 DOM 트리구조의 자손요소에게 **폭포수처럼 내려가듯(Cascading)** 상속됨.
  (마진, 패딩, 보더와 같은 박스모델 속성 제외)

  **S**tyle

  **S**heet

# 선택자

## **엘리먼트를 선택하기 위한 방법**

> "_선택을 해야 스타일을 바꾸던 말던 할거아냐? "_

사용법 :

1. Head에서 `<style>`탭
2. 탭 안에 `선택자 {}` 의방식으로 사용하고, `{속성명 : 값}` 으로 저장.

(1) id 선택자(#)
id를 이용해서 선택 / 또는 getElementById (**JS**)
(2) Class 선택자(,)
class를 이용해서 선택 / 또는 getElementsByClass
(3) 태그 선택자 : '태그명'
Tag를 이용해서 선택 / 또는 getElementsByTag

## **1. ID/ Class 선택자**

```html
<!DOCTYPE html>
<html lang="ko">
  <head>
  ...
    <!-- 일반적으로 Style Sheet는 Head 에서 작업 -->
    <style>
      /* 태그 선택자(태그명 {}) */
      /*  */
      div {
        color: red;
        /* div 태그를 선택해서 컬러를 변경한 것 */
      }
    /* id 선택자(#___ {}) */
      #main {
        color: darkkhaki;
        background-color: black;
      }
    /* 'main' 아이디를 선택해서 속성 변경 */
    /* class 선택자(.___ {}) */
    .talk_1 {
        color: tomato;
        background-color: transparent;
        /* transparent : 투명 */
      }
    /* 'talk_1' 클래스를 선택해서 속성 변경 */

```

## **2. CSS의 특징 : Cascading**

```html
    <style>
      /* Cascading : 부모 Element의 성질이 자손에게 정해진다. */
      div {
        color: red;
        font-weight: 50;
      }
    </style>
  </head>
  <body>
    <div>
      Outline
      <p>Introduction</p>
      <p>Inline Styles</p>
      <p>Embedded Style Sheets</p>
     ....
    </div>

  </body>
```

![cascading](https://image.slideserve.com/458478/cascading-style-sheets-css-l.jpg)

<br><br>

# [Bootstrap](https://getbootstrap.kr/docs/5.2/getting-started/introduction/)

**오픈 소스 프론트엔드 프레임워크**<br>

**· 디자인을 못하는 개발자들을 위한 프론트엔드 도구상자**

## **1. 레이아웃**

표시해야 할 항목

**(1) 그리드시스템**

레이아웃을 어떻게 관리하는가?

**부트스트탭 레이아웃 그리드 시스템**

어떤 디바이스의 가로길이던지 무관하게 하나의 `row`에 12개의 그리드를 사용.

순서

```markdown
1. div. container
2. div.row
3. div.col-?
4. form (경로, 방식)
5. div.form-group
6. 라벨, input
```

**(2) 컨테이너**

**부트스트랩을 적용하기 위한 환경**

## **☞ 컨테이너를 두고, 가로길이를 **무조건** 12개로 나눈다.**

**(3) 폼**

**`<form>` 태그**

> 사용자의 입력을 받아주는 태그

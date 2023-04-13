# 복습

Django에서는 프로젝트를 APP단위로 관리한다.

App은 독립적으로 동작이 가능한 작은 서비스.

서비스는 데이터와 페이지를 Response 할 수 있다.

데이터 Response는 SQL로 하지만, 페이지 Response는 웹 서비스로 한다.
(SQL의 '쿼리' 역할을 웹 서비스가)
<br><br>

# 템플릿

```
<여담>
웹 디자이너
- UI UX 기획
- 포토샵,일러스트

웹 퍼블리셔
- 웹 개발
- HTML,CSS,JS

프론트엔드 개발자
- 퍼블리셔 + 데이터 통신
- React, JS ..

Q. 장고는?
-데이터 분석, AI 머신러닝 구현
> 웹 서비스

```

# Http 요청 Method

## **1. Get Method:**<br>

URL에 데이터를 실어 보낸다.
**검색 내용 전달, 조회**

- 가볍고 빠르다.
- 보안에 취약
- 큰 데이터 전송은 힘들다
- Text 데이터만 전달

```markdown
# 웹의 '식별자' 정리

# URI

- 스킴 + Host(도메인) + Path
- https://www.naver.com/webtoon/wed

# URL

- Host + Path
- www.naver.com/webtoon/wed

# URN

- Path
- /webtoon/wed
```

Url (Host 도메인 주소)
Path (요청사항)
QueryString(parameter) (요청내용/파라미터)

> 최근 추세는 path에 parameter를 사용하는 path parameter 방식을 사용. <br> > **예) API 개발할 때.**

## **2. POST 방식**

사용자가 입력하는 내용들을 서버에 전달하는 방식.

- 무겁지만, 대용량 데이터 전달이 용이하다.

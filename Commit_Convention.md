# Commit Convention

## Index

### [1.Message structure](###1.Message-structure)

### [2.Type](###2.Type)

### [3.Body](###3.Body)

### [4.Footer](###4.Footer)

### [5.Examples](###5.Examples)

<br>
<br>

## 1.Message structure

    type(option): [#issueNumber - ]Subject // Title

    Body(option) // -> body

    Footer(option) // -> footer

<br>

> ### Definition

- type : 어떤 의도로 커밋했는지를 type에 명시합니다.
- subject : 최대 50글자가 넘지 않도록 하고 마침표는 찍지 않습니다. 영문으로 표기하는 경우 동사(원형)를 가장 앞에 두고 첫 글자는 대문자로 표기합니다.
- body : 추가적인 설명이 필요한 경우에 작성합니다. 어떻게 했는지가 아니라, 무엇을 왜 했는지를 작성합니다. 최대 75자를 넘기지 않도록 합니다.
- footer : issue tracker ID를 명시하고 싶은 경우에 작성합니다.

<br>
<br>

## 2.Type

타입은 태그와 제목으로 구성되고, 태그의 첫 문자는 대문자로 합니다.
<br>"태그(옵션): 제목"의 형태이며, : 뒤에만 space가 있음에 유의합니다.
<br>옵션은 추가적인 문맥 상황을 필요한 경우 명시합니다. ex) "Feat(sidebar): ", "Fix(database): "

|       Tag        |                                description                                |
| :--------------: | :-----------------------------------------------------------------------: |
|    　 Feat 　    |                       　새로운 기능을 추가할 경우　                       |
|       Fix        |                            　버그를 고친 경우                             |
|   　 Design 　   |                       CSS 등 사용자 UI 디자인 변경                        |
| !BREAKING CHANGE |                          커다란 API 변경의 경우                           |
|     !HOTFIX      |                  급하게 치명적인 버그를 고쳐야하는 경우                   |
|      Style       |           코드 포맷 변경, 세미 콜론 누락, 코드 수정이 없는 경우           |
|     Refactor     |                          프로덕션 코드 리팩토링                           |
|     Comment      |                         필요한 주석 추가 및 변경                          |
|       Docs       |                            문서를 수정한 경우                             |
|       Test       |            테스트 추가, 테스트 리팩토링(프로덕션 코드 변경 X)             |
|      Chore       | 빌드 태스트 업데이트, 패키지 매니저를 설정하는 경우(프로덕션 코드 변경 X) |
|      Rename      |            파일 혹은 폴더명을 수정하거나 옮기는 작업만인 경우             |
|      Remove      |                    파일을 삭제하는 작업만 수행한 경우                     |

### Tag

> #### Function

- Feat: 새로운 기능을 추가할 경우
- Fix: 버그를 고친 경우
- Design: CSS 등 사용자 UI 디자인 변경
- !BREAKING CHANGE: 커다란 API 변경의 경우 (ex API의 arguments, return- 값의 변경, DB 테이블 변경, 급하게 치명적인 버그를 고쳐야 하는 경우)

> #### Improvement

- Style: 코드 포맷 변경, 세미 콜론 누락, 코드 수정이 없는 경우
- Refactor: 프로덕션 코드 리팩토링, 새로운 기능이나 버그 수정없이 현재 구현을 개선한 경우
- Comment: 필요한 주석 추가 및 변경

> #### et

- Docs: 문서를 수정한 경우
- Test: 테스트 추가, 테스트 리팩토링 (프로덕션 코드 변경 없음)
- Chore: 빌드 태스크 업데이트, 패키지 매니저 설정할 경우 (프로덕션 코드 변경 없음)
- Rename: 파일 혹은 폴더명을 수정하는 경우
- Remove: 사용하지 않는 파일 혹은 폴더를 삭제하는 경우

<br>

### Title

> 1.제목의 처음은 동사 원형으로 시작합니다.
>
> 2.총 글자 수는 50자 이내로 작성합니다.
>
> 3.마지막에 특수문자는 삽입하지 않습니다. 예) 마침표(.), 느낌표(!), 물음표(?)
>
> 4.제목은 개조식 구문으로 작성합니다.
>
> 5.첫 글자는 대문자로 작성합니다.
>
> 6."Fix", "Add", "Change"의 명령어로 시작합니다.

<br>
<br>

## 3.Body

> #### 1. 본문은 한 줄 당 72자 내로 작성합니다.
>
> #### 2. 본문 내용은 양에 구애받지 않고 최대한 상세히 작성합니다.
>
> #### 3. 본문 내용은 어떻게 변경했는지 보다 무엇을 변경했는지 또는 왜 변경했는지를 설명합니다.

<br>
<br>

## 4.Footer

> #### 1. 본문은 한 줄 당 72자 내로 작성합니다.
>
> #### 꼬리말은 optional이고 이슈 트래커 ID를 작성합니다.
>
> #### 꼬리말은 "유형: #이슈 번호" 형식으로 사용합니다.
>
> #### 여러 개의 이슈 번호를 적을 때는 쉼표로 구분합니다.
>
> #### 이슈 트래커 유형은 다음 중 하나를 사용합니다.<br> > \- Fixes: 이슈 수정중 (아직 해결되지 않은 경우)<br> > \- Resolves: 이슈를 해결했을 때 사용<br> > \- Ref: 참고할 이슈가 있을 때 사용<br> > \- Related to: 해당 커밋에 관련된 이슈번호 (아직 해결되지 않은 경우)<br>ex) Fixes: #45 Related to: #34, #23

<br>
<br>

## 5.Examples

    Feat: "Add login function"

    로그인 API 개발

    Resolves: #123
    Ref: #456
    Related to: #48, #45

## 1xx Informational Codes

---

### 100 Continue

### 101 Switching Protocols

### 102 Processing

## 2xx Success Codes

---

### 200 OK

### 201 Created

### 202 Accepted

### 203 Non-Authoritative Information

### 204 No Content

### 205 Reset Content

### 206 Partial Content

### 207 Multi-Status

### 208 Already Reported

### 226 IM Used

## 3xx Redirection Codes

---

### 300 Multiple Choices

### 301 Moved Permanently

### 302 Found

### 303 See Other

### 304 Not Modified

### 305 Use Proxy

### 306 Switch Proxy

### 307 Temporary Redirect

### 308 Permanent Redirect

## 4xx Client Error Codes

---

### 400 Bad Request

### 401 Unauthorized

### 402 Payment Required

### 403 Forbidden

### 404 Not Found

### 405 Method Not Allowed

### 406 Not Acceptable

### 407 Proxy Authentication Required

### 408 Request Timeout

### 409 Conflict

### 410 Gone

### 411 Length Required

### 412 Precondition Failed

### 413 Request Entity Too Large

### 414 Request-URI Too Long

### 415 Unsupported Media Type

### 416 Requested Range Not Satisfiable

### 417 Expectation Failed

### 418 I'm a teapot

### 419 Authentication Timeout

### 420 Method Failure (Spring Framework)

### 420 Enhance Your Calm (Twitter)

### 422 Unprocessable Entity

### 423 Locked

### 424 Failed Dependency

### 425 Upgrade Required

### 426 Precondition Required

### 428 Precondition Required

### 429 Too Many Requests

### 431 Request Header Fields Too Large

### 440 Login Timeout (Microsoft)

### 444 No Response (Nginx)

### 449 Retry With (Microsoft)

### 450 Blocked by Windows Parental Controls (Microsoft)

### 451 Unavailable For Legal Reasons

### 451 Redirect (Microsoft)

### 494 Request Header Too Large (Nginx)

### 495 Cert Error (Nginx)

### 496 No Cert (Nginx)

### 497 HTTP to HTTPS (Nginx)

### 498 Token expired/invalid (Esri)

### 499 Client Closed Request (Nginx)

### 499 Token required (Esri)

## 5xx Server Error Codes

---

### 500 Internal Server Error

### 501 Not Implemented

### 502 Bad Gateway

### 503 Service Unavailable

### 504 Gateway Timeout

### 505 HTTP Version Not Supported

### 506 Variant Also Negotiates

### 507 Insufficient Storage

### 508 Loop Detected

### 509 Bandwidth Limit Exceeded

### 510 Not Extended

### 511 Network Authentication Required

### 598 Network read timeout error

### 599 Network connect timeout error

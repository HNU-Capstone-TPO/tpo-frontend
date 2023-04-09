# Git - 커밋 메세지 컨벤션(Commit Message Convention)

Git을 협업할 때 일관성있고 가독성을 가질수 있게 커밋 메세지에 대한 규칙을 정하는 것을 커밋 메세지 컨벤션이라고 한다.

## 1. 커밋 메세지 구조(Commit Message Structure)

```
Type[optional scope]: Subject # 타입(): 제목
(한줄 띄우기)
[optional body] # 본문 (생략가능)
(한줄 띄우기)
[optional footer(s)] # 꼬리말 (생략가능)
```

## 2. 커밋 타입(Commit Type)

- Feat: 새로운 기능 생성(A new feature)
- Fix: 버그 수정(A bug fix)
- Docs: 문서 변경(Changes to documentation)
- Style: 코드 스타일 변경, 세미콜론 추가 등 기능에 영향이 없는 코드(Formatting, missing semi colons, etc; no code change)
- Refactor: 실제 코드 리팩토링(Refactoring production code)
- Test: 테스트 추가, 테스트 리팩토링, 기능에 영향을 안주는 테스트(Adding tests, refactoring test; no production code change)
- Chore: 위 타입에 없는 기타 변경사항(Updating build tasks, package manager configs, etc; no production code change)
- BREAKING CHANGE: 대규모 API 변경이 있을 때 사용(Breaking API change to correlating with MAJOR in semantic versioning)
- Rename: 파일 혹은 폴더명 변경
- Remove: 파일 혹은 폴더 삭제
- Move: 파일 혹은 폴더 이동

## 3. 주제(Subject)

- 제목은 50자 이내여야 한다.
- 대문자로 시작한다.
- 마침표로 끝나지 않아야 한다.
- 시제를 사용하지 않는다. (Changed 혹은 Changes 말고 Change ~~)
- 동사를 우선시 사용한다.
- 필요시 스코프를 추가할 수 있다.

## 4. 본문(Body)

- 선택 사항이다.
- 본문은 72자 이내여야 한다.
- 커밋에 약간의 설명과 맥락이 필요한 경우에만 사용된다.
- 방법이 아니라 내용과 이유를 설명하기 위해 본문을 사용한다.

## 5. 꼬리말(Footer)

- 선택 사항이다.
- 이슈번호를 남기는데 사용한다.

## 6. 예제(Example)

### 본문과 꼬리말 없는 커밋 메세지(Commit message with no body)

```
docs: correct spelling of CHANGELOG
```

### 스코프를 추가한 커밋 메세지(Commit message with scope)

```
feat(lang): add Polish language
```

### 본문과 꼬리말이 있는 커밋 메세지(Commit message with multi-paragraph body and multiple footers)

```
fix: prevent racing of requests

Introduce a request id and a reference to latest request. Dismiss
incoming responses other than from latest request.

Remove timeouts which were used to mitigate the racing issue but are
obsolete now.

Reviewed-by: Z
Refs: #123
```

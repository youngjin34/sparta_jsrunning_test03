# 달리기반 3회차 실습 과제

달리기반 3회차 실습 과제입니다.  
전날 배운 DOM 조작, 동기/비동기 내용들을 토대로 풀 수 있도록 구성되어 있습니다.

&nbsp;

## 1. Promise 다뤄보기
1. `getData` 라는 주어진 url을 인자로 받는 함수를 만들어주세요.
2. `getData` 는 3초 후 url이 기준 url과 동일할 경우 성공적으로 데이터를 반환하고, 틀릴 경우 에러를 발생시킵니다.
3. `then`과 `catch`를 이용하여 데이터를 처리하는 방법과 에러를 처리하는 방법 두 가지를 각각 보여주세요.

```javascript
    const API_URL = "https://open.api.com/v1/data";
    const WRONG_URL = "https://open.api.com/v1/wrong;

    function getData(url) {
        // 3초 뒤 url 이 API_URL과 같다면 성공으로 처리를, 아닐 경우 실패로 처리를 하게 해주세요
    }

    // ...

    // getData(API_URL), getData(WRONG_URL) 각각 성공과 실패에 대한 처리를 코드작성해주세요.
    
```

&nbsp;

## 2. Async / Await 다뤄보기

위 1번 문제에서 다루었던 비동기 처리를 `async`, `await` 키워드를 사용하여 코드를 수정해서 작성해주세요.

```javascript
// async await 를 사용한 코드로 변경해보기
```

&nbsp;

## 3. DOM 제어와 함께 비동기 처리하기

html 파일을 하나 만들고 openAPI 를 활용해 고양이 사진을 불러오는 api를 요청하려 합니다.
받아온 고양이 사진 url을 img 태그를 생성하고, `imageContainer` 라는 이름의 div에 동적으로 생성해주세요.
3번 문제는 03.js가 아닌, 아래 코드를 참고하여 03.html (혹은 index.html 등 이름은 자유) 로 진행해 주시기 바랍니다.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>랜덤 고양이 사진</title>
  </head>
  <body>

    <div id="imageContainer"></div>

    <script>
      let API_URL = `https://api.thecatapi.com/v1/images/search`;

      let options = {
        method: "GET",
        headers: {
          accept: "application/json",
          "x-api-key":
            "live_8GfbTk0GMtgRdbxUB7XcuYzuMmfShEHGHNSnDo26DDgJDVUHDWqzJ25rJKpsSqud",
        },
      };

      // API_URL 과 options를 사용해 fetch 로 API 요청을 한 후, 해당 데이터를 통해 img 태그를 생성하여 주세요.
    </script>
  </body>
</html>

```
 
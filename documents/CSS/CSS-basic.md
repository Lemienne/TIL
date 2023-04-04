# CSS
## Selector
CSS에서 특정 HTML 태그를 선택할 때는 선택자를 사용한다
### Why Selector? 
특정 HTML 태그를 선택하여, **원하는 스타일이나 스크립트를 적용**하기 위하여 
```HTML
<!DOCTYPE html>
<html lang="en">
    <head>
        <title>CSS3 Selector</title>
        <style>
            h1 {
                color: red;
                background-color: blue;
            }
        </style>
    </head>
    <body>
        <h1>CSS3 선택자</h1>
    </body>
</html>
```

- style 태크 내부에 CSS 블록을 입력해 작성한 코드를 '스타일시트' 라 부른다. 
- CSS 선택자는 스타일시트뿐만 아니라 JavaScript에서도 사용되기에 기억 필요.

## 기본 선택자
### 전체 선택자 
- `*`을 사용하여 모든 태그의 color 스타일 속성 변경 가능 
```HTMl
<style>
    * { color: red; }
</style>
```
***
### 태그 선택자
- `p, h1, body` 같은 태그를 입력하여 스타일 속성 변경
```HTML
<style>
    h1 { color: red ;}
    p { color: blue; }
</style>
```
- 한꺼번에 선택자를 여러 개 입력해 스타일 속성 적용?
    * 쉼표를 사용하여 태그 선택자 연결

```HTML
<style>
    body, p, h1, h2, h3, h4, h5, h6 { margin:0; padding: 0;}
</style>
```
- 태그 선택자 뿐만 아니라 모든 선택자에도 적용 가능
***
### id 선택자
공간 분할 태그에 아이디 선택자를 사용해 id 속성을 적용하고 레이아웃을 구성한다. 
```HTML
<head>
    <title>CSS Selector</title>
    <style>
        #header {
            width: 800px; margin: 0 auto;
            background: red;
        }
    </style>
</head>
<body>
    <div id="header">
        <h1>#header 태그</h1>
    </div>
</body>
```
### class 선택자 


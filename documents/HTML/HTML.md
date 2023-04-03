# HTML5

## 미디어 태그
- 웹 페이지에 멀티미디어를 넣을 때 사용하는 태그 
### img 태그
표시하고 싶은 이미지 파일을 프로젝트에 추가 후 코드 작성
> img 태그 속성
> - src : 이미지의 경로 지정
> - alt : 이미지가 없을 때 나오는 글자 지정
> - width : 이미지의 너비 지정
> - height : 이미지의 높이 지정
```HTML
<body>
    <!-- 같은 폴더에 있을 때 -->
    <img src="markdown.jpg" alt="markdown" width="300">
    <!-- 다른 폴더에 위치하여 상대 위치 사용 -->
    <img src="../assets/img/markdown.jpg" alt="markdown" width="300">
    <img src="nothing" alt="그림이 존재하지 않습니다." width="300"
</body>
```

***
### audio 태그
삽입하고 싶은 오디오 파일을 프로젝트에 추가 후 코드 작성
> audio 태그 속성
> - src : 음악 파일의 경로 지정
> - preload : 음악을 준비 중일때 데이터를 모두 불러올지 여부 지정
> - autoplay : 음악의 자동 재생 여부 지정
> - loop : 음악의 반복 여부 지정
> - controls : 음악 재생 도구 출력 여부 지정
```HTML
<body>
    <audio src="Piano.mp3" controls="controls"></audio>
</body>
```
웹 브라우저에 제약 없이 오디오 파일 삽입하는 방법
```HTML
<body>
    <audio controls="controls">
        <source src="Piano.mp3" type="audio/mp3">
        <source src="Piano.ogg" type="audio/ogg">
    </audio>
</body>
```
웹 페이지마다 지원하는 확장자가 모두 다르다.   
위 문제를 해결하기 위해서는 source 태그를 사용하여 해결할 수 있다.
- type 속성을 사용하여 브라우저에 파일 확장자를 알릴 수 있음
- 사용하지 않을 경우 웹 브라우저가 음악 파일을 다운로드 후 재생가능 여부를 확인하는 절차가 필요함.
***
### video 태그 
삽입하고 싶은 비디오 파일을 프로젝트에 추가 후 코드 작성
> video 태그 속성
> - src : 비디오 파일의 경로 지정
> - preload : 비디오를 준비 중일때 데이터를 모두 불러올지 여부 지정
> - autoplay : 비디오의 자동 재생 여부 지정
> - loop : 비디오의 반복 여부 지정
> - controls : 비디오 재생 도구 출력 여부 지정
> - width : 비디오의 너비 지정
> - height : 비디오의 높이 지정
```HTML
<body>
    <video controls="controls">
        <source src="Wildlife.mp4" type="video/mp4">
        <source src="Wildlife.ogg" type="video/ogg">
    </video>
</body>
```
poster 속성을 사용하여 동영상을 불러오는 동안 사용자에게 보여 줄 이미지를 지정할 수 있음
```HTML
<body>
    <video controls="controls" poster="http://via.placeholder.com/680x360">
        <source src="Wildlife.mp4" type="video/mp4">
        <source src="Wildlife.ogg" type="video/ogg">
    </video>
</body>
```
> 예제에서는 http://via.placeholder.com/680x360 를 사용하였다.   
> 이 웹 사이트는 주소 다음에 너비x높이를 입력하면 해당 크기의 이미지를 제공한다. 

## 입력 양식 태그
- 입력 양식?
    * 사용자에게 정보를 입력받는 요소
    * 입력 양식 태그를 사용하여 만든다

## 1. 기본 입력 방식
### 1.1. form 태그
- 입력 양식의 시작과 끝을 표시한다.
- 속성
    * 보이지 않음
    * method, action 속성을 사용 
```HTML
<form action="(전송 위치)" method="(get/post)"
```
> action 태그 : 데이터를 전달할 목적지 설정   
> method 태그 : 데이터 전송 방식 설정
- GET: 주소에 데이터를 직접 입력해 전달 
    * 데이터의 크기가 한정되어 있음
- POST: 별도의 방법을 사용해 데이터를 해당 주소로 전달
    * 데이터 용량에 제한 없음 
***
### 1.2. input 태그
- type : 입력 태그의 유형 지정
    * 다양한 종류의 기본 입력 양식 생성 가능
- value : 입력 태그의 초기값을 설정
    * 사용자가 변경 가능
- name : 서버로 전달되는 이름을 말한다. 
    * 사용자 임의 지정 가능
```HTML
<body>
    <form>
        <!-- 사용자가 입력하는 입력 양식 -->
        <input type="text" name="text" value="text"><br>
        <input type="password" name="password" value="password"><br>
        <input type="file" name="file" value="file"><br>
        <input type="checkbox" name="checkbox" value="checkbox"><br>
        <input type="radio" name="radio" value="radio"><br>
        
        <!-- 보이지 않는 입력 양식 -->
        <input type="hidden" name="hidden" value="hidden"><br>
        
        <!-- 버튼 -->
        <input type="button" value="button"><br>
        <input type="reset" value="reset"><br>
        <input type="submit" value="submit"><br>
        <input type="image" src="http://placehold.it/100x100">
    </form>
</body>
```
- 자주 사용되는 type 속성들   
- 위에 쓰인 속성들 이외에도, 다양한 속성들이 존재한다.
***
### 1.2.1. label 태그
* input 태그를 설명할 때 사용
* 연결 후, label 태그를 클릭했을 때, input 태그에 자동으로 포커스가 간다.
```HTML
<form>
    <label for="name">이름</label>
    <input id="name" type="text">
</form>
```
***
### 1.2.2. name 태그
- 라디오 버튼의 name 속성을 사용하여 여러 대상 중 하나만 선택하는 형태 구현 가능
```HTML
<body>
    <form>
        <tr>
            <td>성별</td>
            <td>
                <input id="man" type="radio" name="gender" value="m">
                <label for="man">남자</label>
                <input id="woman" type="radio" name="gender" value="w">
                <label for="woman">여자</label>
            </td>
        </tr>
    </form>
</body>
```
radio 버튼은 name 속성을 같게 입력해야 여러 항목 중 하나만 선택됩니다.
***
### 1.3. 선택 가능한 입력 양식
### 1.3.1. select 태그
- 목록으로 보여주는 항목 중 하나 또는 여러 개를 선택할 때 사용
  - 속성 : multiple
```HTML
<body>
    <select>
        <option>HTML</option>
        <option>CSS</option>
        <option>JavaScript</option>
        <option>TypeScript</option>
    </select>
</body>
```
***
### 1.3.2. multiple 속성
- 여러 항목 선택 가능
- 스마트폰에서는 깔끔하게 출력,  데스크톱에서는 별로...
    * 따라서 데스크톱 웹페이지에서는 잘 사용하지 않음
```HTML
<body>
    <select multiple="multiple">
        <option>HTML</option>
        <option>CSS</option>
        <option>JavaScript</option>
        <option>TypeScript</option>
    </select>
</body>
```
***
### 1.3.3. optgroup 태그
선택 옵션을 그룹으로 묶을 수 있다. 
```HTML
<body>
    <select>
        <optgroup label="HTML5">
            <option>Multimedia Tag</option>
            <option>Connectivity</option>
            <option>Device Access</option>
        </optgroup>
        <optgroup label="CSS">
            <option>Animation</option>
            <option>3D Transform</option>
        </optgroup>
    </select>
</body>
```

> - 최근에는 잘 사용하지 않는 편
>   * select 태그 대신 JavaScript를 사용하여, 웹 페이지와 어울리게 "옵션 선택"을 구현
***
### 1.3.4. fieldset, legend 태그
- fieldset 태그 : 입력 양식을 그룹으로 묶을 수 있음
- legend 태그 : 묶인 입력 양식에 이름을 지정할 수 있음
    * fieldset 태그 내부에서 사용한다. 
    * 다른 곳에서도 쓸 수는 있지만 효과가 없음.
```HTML
<body>
    <form>
        <fieldset>
            <legend>입력 양식</legend>
            <table>
                <tr>
                    <td><label for="name">이름</label></td>
                    <td><input id="name" type="text"></td>
                </tr>
                <tr>
                    <td><label for="mail">이메일</label></td>
                    <td><input id="mail" type="email"></td>
                </tr>
            </table>
            <input type="submit">
        </fieldset>
    </form>
</body>
```

## HTML 문서 구조화
## 1. 공간 분할 태그 
- 공간을 분할하는 이유
    * CSS로 원하는 레이아웃을 구성하기 위해서
- 공간 분할 태그
    * **div 태그** : 블록 형식으로 공간 분할
    * **span 태그** : 인라인 형식으로 공간 분할
```HTML
<body>
    <div>div 태그 - block 형식</div>
    <span>span 태그 - inline 형식</span>
</body>
```

## 2. 시맨틱 태그
**시맨틱 웹** : 컴퓨터 프로그램이 코드를 읽고 의미를 인식할 수 있는 지능형 웹
> - 시맨틱 태그 
>    * header : 머리말(페이지 제목, 페이지 소개)
>    * nav : 하이퍼링크들을 모아 둔 내비게이션
>    * aside : 본문 흐름에 벗어나는 노트나 팁
>    * section : 문서의 장이나 절에 해당되는 내용
>    * article : 본문과 독립적인 콘텐츠 영역
>    * footer : 꼬리말(저자나 저작권 정보)
```HTML
<body>
    <div>
        <h1>HTML5 기본</h1>
    </div>
    <div>
        <ul>
            <li><a href="#">메뉴 - 1</a></li>
            <li><a href="#">메뉴 - 2</a></li>
            <li><a href="#">메뉴 - 3</a></li>
        </ul>
    </div>
    <div>
        <div>
            <h1>Lorem ipsum dolor sit amet</h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </div>
        <div>
            <h1>Lorem ipsum dolor sit amet</h1>
            <p>Lorem ipsum dolor sit amet, sonsectetur adipiscing elit.</p>
        </div>
    </div>
    <div>
        <span>서울특별시 강서구 마곡동</span>
    </div>
</body>
```

div 태그를 활용한 웹 페이지 레이아웃 구성
```HTML
<body>
    <header>
        <h1>HTML5 기본</h1>
    </header>
    <nav>
        <ul>
            <li><a href="#">메뉴 - 1</a></li>
            <li><a href="#">메뉴 - 2</a></li>
            <li><a href="#">메뉴 - 3</a></li>
        </ul>
    </nav>
    <section>
        <article>
            <h1>Lorem ipsum dolor sit amet</h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </article>
        <article>
            <h1>Lorem ipsum dolor sit amet</h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
        </article>
    </section>
    <footer>
        <address>서울특별시 강서구 마곡동</address>
    </footer>
</body>
```

시맨틱 태그를 활용한 웹 페이지 레이아웃 구성
- 시맨틱 태그를 사용하여 각 태그에 의미 부여
- 가독성이 이전 코드 보다 좋다. 
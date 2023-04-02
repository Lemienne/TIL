# HTML5
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
> <body>
>    <form>
>        사용자가 입력하는 입력 양식<br>
>        <input type="text" name="text" value="text"><br>
>        <input type="password" name="password" value="password"><br>
>        <input type="file" name="file" value="file"><br>
>        <input type="checkbox" name="checkbox" value="checkbox"><br>
>        <input type="radio" name="radio" value="radio"><br>
>        보이지 않는 입력 양식<br>
>        <input type="hidden" name="hidden" value="hidden"><br>
>        버튼<br>
>        <input type="button" value="button"><br>
>        <input type="reset" value="reset"><br>
>        <input type="submit" value="submit"><br>
>        <input type="image" src="http://placehold.it/100x100">
>    </form>
> </body>

### 1.2.1. label 태그
* input 태그를 설명할 때 사용
* 연결 후, label 태그를 클릭했을 때, input 태그에 자동으로 포커스가 간다.
```HTML
<form>
    <label for="name">이름</label>
    <input id="name" type="text">
</form>
```
<form>
    <label for="name">이름</label>
    <input id="name" type="text">
</form>

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
<body>
    <form>
        <fieldset>
            <tr>
                <td>성별</td><br>
                <td>
                    <input id="man" type="radio" name="gender" value="m">
                    <label for="man">남자</label>
                    <input id="woman" type="radio" name="gender" value="w">
                    <label for="woman">여자</label>
                </td>
            </tr>
        </fieldset>
    </form>
</body>

radio 버튼은 name 속성을 같게 입력해야 여러 항목 중 하나만 선택됩니다.

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
<body>
    <select>
        <option>HTML</option>
        <option>CSS</option>
        <option>JavaScript</option>
        <option>TypeScript</option>
    </select>
</body>

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
<body>
    <select multiple="multiple">
        <option>HTML</option>
        <option>CSS</option>
        <option>JavaScript</option>
        <option>TypeScript</option>
    </select>
</body>

> 일반 데스크톱 환경이면 알 수 있다시피, 항목들을 선택 방식이 명확하지 않다. 

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

> - 최근에는 잘 사용하지 않는 편
>   * select 태그 대신 JavaScript를 사용하여, 웹 페이지와 어울리게 "옵션 선택"을 구현
  
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

- 시맨틱 태그를 사용하여 각 태그에 의미 부여
- 가독성이 이전 코드 보다 좋다. 
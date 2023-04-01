# 마크다운

## 1. 헤더 Headers
* #의 개수에 따라 글머리 결정
    * 글머리는 1~6까지만 지원
```agsl
# H1
## H2
### H3
#### H4
##### H5
###### H6
```
# H1
## H2
### H3
#### H4
##### H5
###### H6

## 2. 줄바꿈
3칸 이상 띄어쓰기{`   `)룰 하면 줄이 바뀐다.
```agsl
* 줄 바꿈을 하기 위해서는 문장 마지막에서 3칸 이상을 띄어쓰기해야 한다. 
이렇게
* 줄 바꿈을 하기 위해서는 문장 마지막에서 3칸 이상을 띄어쓰기해야 한다.___\\ 띄어쓰기
이렇게
```
* 줄 바꿈을 하기 위해서는 문장 마지막에서 3칸 이상을 띄어쓰기해야 한다.
  이렇게
* 줄 바꿈을 하기 위해서는 문장 마지막에서 3칸 이상을 띄어쓰기해야 한다.   
  이렇게

## 3. 코드<hr/>
4개의 공백 또는 하나의 탭으로 들여쓰기가 진행되면 변환을 시작, 들여쓰지 않은 행을 만날때까지 변환 지속.

### 3.1. 들여쓰기
```agsl
This is a normal paragraph : 
    This is a code block.
end code block.
```
This is a normal paragraph:

    This is a code block.

end code block.
> 한줄 띄어쓰지 않으면 인식이 제대로 안되는 문제가 발생.
> > 코드 블럭 적용할 문구 이전과 이후에 반드시 한줄 띄어쓸 것.

### 3.2. 코드블럭
코드블럭은 2가지 방식으로 사용할 수 있음.
***
#### 3.2.1 `<pre><code>{code}</code></pre>`
* ("``") 의 출력이 필요할 때 사용
* 공백이 위아래로 생김
```
<pre>
<code>
#include <stdio.h>

int main()
{
    printf("Hello, world!");
    
    return 0;
}
</code>
</pre>
```
<pre>
<code>
#include <stdio.h>

int main()
{
    printf("Hello, world!");
    
    return 0;
}
</code>
</pre>
#### 3.2.2 코드 블럭 코드("``") 를 이용하는 방법
<pre>
<code>
```
#include <stdio.h>

int main()
{
    printf("Hello, world!");
    
    return 0;
}
```
</code>
</pre>
```
#include <stdio.h>

int main()
{
printf("Hello, world!");

    return 0;
}
```
***
* GitHub에서는 코드블럭코드("``") 시작점에 사용하는 언어를 선언하여 문법강조가 가능하다.
<pre>
<code>
```java
public class BootSpringBootApplication {
  public static void main(String[] args) {
    System.out.println("Hello, Honeymon");
  }
}
```
</code>
</pre>
```java
public class BootSpringBootApplication {
  public static void main(String[] args) {
    System.out.println("Hello, Honeymon");
  }
}
```

## 4. 목록

### 4.1. 순서있는 목록(번호)
순서 있는 목록은 숫자와 점을 사용한다.
```
1. 첫번째 
2. 두번째 
3. 세번째 
```
1. 첫번째
2. 두번째
3. 세번째  
   여담으로 순서로 글머리론 어떤 번호를 입력하더라도 내림차순으로 정의된다.

### 4.2. 순서없는 목록(글머리 기호: `*`, `+`, `-` 지원)
```agsl
* 빨강
    *녹색
        *파랑
+ 빨강
    + 녹색
        + 파랑
- 빨강
    - 녹색
        - 파랑
```
* 빨강
    * 녹색
        * 파랑
+ 빨깅
    + 녹색
        + 파랑
- 빨강
    - 녹색
        - 파랑

기호들을 호환해서 사용해도 된다.


## 5. Block Quote<hr/>
이메일에서 사용하는 `>`블럭인용문자를 이용
```
> This is a first blockquote.  
>> This is a second blockquote.  
>>> This is a third blockquote.
```
> This is a first blockquote.
>> This is a second blockquote.
>>> This is a third blockquote.

이 안에는 다른 마크다운 요소를 포함할 수 있다. 
> This is a H3   
> - List   
> `code`

## 6. 수평선 `<hr/>`
아래 줄은 모두 수평선을 만든다. 마크다운 문서를 미리보기로 출력할 때 페이지 나누기 용도로 많이 사용한다. 
```agsl
* * *

***

*****

- - -

---------------------------------------
```
* * *

***

*****

- - -

--------------------------------------- 

## 7. 링크
* 참조 링크
```agsl
[link keyword][id]
[id]: URL "Optional Title here"

// code
Link: [Google][googlelink]

[googlelink]: https://google.com "Go google"
```
Link: [Google][googlelink]

[googlelink]: https://google.com "Go google"
> **예시**   
> 
>> 출처는 [구글][google]입니다.

[google]: https://www.google.com/ "Go google"
***
* 외부 링크 
```agsl
사용 문법: [Title](link)
적용예: [Google](https://google.com, "google link")
```
[Google](https://google.com, "google link")
***
* 자동연결
```agsl
일반적인 URL 혹은 이메일 주소인 경우 적절한 형식으로 링크를 형성한다. 
* 외부 링크: <https://example.com/>
* 이메일 링크: <address@example.com>
```
- 외부 링크: <https://google.com>
- 이메일 링크: <address@example.com>

## 8. 강조
```agsl
*single asterisks*
_single underscores_
**double asterisks**
__double underscores__
~~cancelline~~
```
- *single asterisks*   
- _single underscores_   
- **double asterisks**   
- __double underscores__   
- ~~cancelline~~
> `문장 중간에 사용할 경우에는 **띄어쓰기** 를 사용하는 것이 좋다.`   
> 문장 중간에 사용할 경우에는 **띄어쓰기**를 사용하는 것이 좋다. 
> 
## 9. 이미지
```agsl
![Alt text](/path/to/img.jpg)
![Alt text](/path/to/img.jpg "img name")
```
![markdown](../assets/img/markdown.jpg)
![markdown](../assets/img/markdown.jpg "Markdown")    
> 사이즈 조절 기능은 없기에 `<img width="" height=""></img>`를 이용한다.   
예
```
<img src="/path/to/img.jpg" width="450px" height="300px" title="px(픽셀) 크기 설정" alt="키리기리"></img><br/>
<img src="/path/to/img.jpg" width="40%" height="30%" title="px(픽셀) 크기 설정" alt="키리기리"></img>
```
<img src="../assets/img/markdown.jpg" width="450px" height="300px" title="px(픽셀) 크기 설정" alt="Markdown"></img><br/>
<img src="../assets/img/markdown.jpg" width="40%" height="30%" title="px(픽셀) 크기 설정" alt="Markdown"></img><br/>


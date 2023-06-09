# TIL🌟
- 당일 학습한 내용을 정리합니다.

## 2023-03-27
- git bash 설치
- 기초 리눅스 명령어
- vim 사용법

## 2023-03-28
- commit 개념
  - 개념
  - 커밋을 언제 만드는지
  - 커밋 크기
- 저장소
  - 개념
  - 일반 폴더와 저장소의 차이(`.git`폴터 유무)
  - `git init`명령어로 저장소 만들기

## 2023-03-29
- 커밋 만들기
  - `git commit -m`
- 스테이징 영역
  - `git add` 명령어로 커밋에 포함시키고 싶은 파일만 스테이징 영역에 추가

## 2023-03-31 
- HTML 미디어 태그 
  - 이미지 삽입하기 
    ```HTML
    <img src="CONTENT" alt="NAME" width="SIZE">
    ```
  - 음악 삽입하기
    ```HTML 
    <audio controls="controls"> 
        <source src="FILE.mp3" type="audio/mp3">
    ```
  - 동영상 삽입하기
    ```HTML
    <video controls="controls">
        <source src="FILE.mp4" type="video/mp4">
    ```
    
## 2023-04-02
- Markdown 
  * [Markdown 기초](https://github.com/Lemienne/TIL/blob/main/documents/Markdown/markdown-basic.md)
- HTML 입력 양식 태그와 구조화 태그 
  * [HTML 문법](https://github.com/Lemienne/TIL/blob/main/documents/HTML/HTML.md)

## 2023-04-03
- CSS 선택자 
- git branch 

## 2023-04-04
- git branch
- GitHub "Pull Request"
- git merge
> git push 취소하기 
> 1. 워킹 디렉토리에서 commit 되돌린다. 
>   * 가장 최근의 commit을 취소하고 워킹 디렉터리를 되돌린다.
>   * `$ git reset HEAD^`
> 2. 되돌려진 상태에서 다시 commit을 한다. 
>   * `$ git commit -m "Write commit messages"`
> 3. 원격 저장소에 강제로 push 한다. 
>   * `$ git push origin [branch name] -f`
>   * `$ git push origin +[branch name]`
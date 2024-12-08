깃 배우기 - 팀 개발을 위한 Git, GitHub 시작하기


> [터미널 명령 참조](https://github.com/0nn0/terminal-mac-cheatsheet/blob/master/한국어/README.markdown "Go to https://github.com/0nn0/terminal-mac-cheatsheet/blob/master/한국어/README.markdown")

1. 로컬 저장소 만들기
    ```bash
    $ git init
    ```

    **<u>Output</u>**
    ```
    Initialized empty Git repository in {path}
    ```
    

2. 첫번째 커밋 만들기
    1. 정보 등록
        ```bash
        $ git config --global user.email "star2kis@nate.com"
        $ git config --global user.name "KangHwan-Cha"
        ```

    2. 파일 추가
        ```bash
        $ git add README.md
        또는 
        $ git add .
        ```

    3. 커밋하기
        ```bash
        $ git commit -m "My first commit"
        ```

3. 다른 커밋으로 시간여행하기
    1. `git log`: 커밋 확인
        - git log 명령은 최신 커밋부터 보여줌
    2. hello world

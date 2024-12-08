<!-- *NOTE* for writting up markdown -->
<!-- 
  ## => chapter
  ### => section in chapter

1. => section number in section

★ : Importance
-->

# 깃 배우기 - 팀 개발을 위한 Git, GitHub 시작하기

> [터미널 명령 참조](https://github.com/0nn0/terminal-mac-cheatsheet/blob/master/한국어/README.markdown "Go to https://github.com/0nn0/terminal-mac-cheatsheet/blob/master/한국어/README.markdown")

## Table of Contents
- [깃 배우기 - 팀 개발을 위한 Git, GitHub 시작하기](#깃-배우기---팀-개발을-위한-git-github-시작하기)
  - [Table of Contents](#table-of-contents)
  - [Chapter 0 : 빠른 실습으로 Git, GitHub 감 익히기](#chapter-0--빠른-실습으로-git-github-감-익히기)
    - [로컬저장소에서 커밋 관리하기](#로컬저장소에서-커밋-관리하기)
    - [다른 커밋으로 시간여행하기](#다른-커밋으로-시간여행하기)
    - [GitHub 원격 저장소에 커밋 올리기](#github-원격-저장소에-커밋-올리기)
    - [GitHub 원격 저장소의 커밋을 로컬 저장소에 내려받기](#github-원격-저장소의-커밋을-로컬-저장소에-내려받기)
    - [단어정리](#단어정리)
  - [Chapter 1 : GUI를 위한 버전 관리 환경 구축하기](#chapter-1--gui를-위한-버전-관리-환경-구축하기)
    - [소스트리 설치하기](#소스트리-설치하기)
    - [비주얼 스튜디오 코드 설치하기](#비주얼-스튜디오-코드-설치하기)
    - [GitHub 둘러보기](#github-둘러보기)
  - [Chapter 2 : 혼자서 Git으로 버전 관리하기](#chapter-2--혼자서-git으로-버전-관리하기)


## Chapter 0 : 빠른 실습으로 Git, GitHub 감 익히기
###  로컬저장소에서 커밋 관리하기
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

### 다른 커밋으로 시간여행하기
1. `git log`: 커밋 확인
    - git log 명령은 최신 커밋부터 보여줌
2. `git checkout {커밋 ID}`
3. `git checkout -`: 최근에 있던 브랜치로 이동

<br>

> 최근 `switch` / `restore`명령어로 나누어짐
> 1. `switch`: 브랜치 간 이동
> 2. `restore`: 커밋에서 파일들을 복구

### GitHub 원격 저장소에 커밋 올리기

1. 레포지토리: 원격 저장소
2. 원격저장소 만들기
    > [Git 레포지토리](https://github.com/KangHwan-Cha?tab=repositories "Go to https://github.com/KangHwan-Cha?tab=repositories")
3. 원격 저장소 url: https://github.com/KangHwan-Cha/Study_Git.git

4. ★ **원격 저장소에 커밋 올리기**
    ```bash
    # 원격 저장소 주소 입력
    $ git remote add origin https://github.com/KangHwan-Cha/Study_Git.git
    # 브랜치 만들기
    $ git branch -M main
    # 원격 저장소에 리기
    $ git push origin main
    ```

### GitHub 원격 저장소의 커밋을 로컬 저장소에 내려받기
1. 클론<sup>clone</sup>: 코드와 버전 전체를 내려받기
    > [Download ZIP] 으로 받으면 원격 저장소와 버전정보가 제외되므로 `git clone`을 사용
    
    ```bash
    # 주소 뒤에 한칸 띄고 마침표
    # 마침표를 붙이면 현재 위치에 clone
    $ git clone {원격 저장소 주소} .  
    ```

2. 원격 저장소의 새로운 커밋을 로컬 저장소에 갱신하기
    
    ```bash
    $ git pull origin main
    ```


### 단어정리

- **Git**: 분산 버전 관리 시스템으로, 파일 변경 이력 관리 및 협업을 위한 도구.
- **GitHub**: Git을 기반으로 한 웹 서비스로, 소스 코드 호스팅 및 협업 기능을 제공.
- **GUI** (Graphical User Interface): 그래픽 사용자 인터페이스로, 명령어 대신 그래픽 요소로 시스템과 상호작용하는 방식.
- **CLI** (Command Line Interface): 명령어를 입력해 시스템과 상호작용하는 텍스트 기반 인터페이스.
- **Git Bash**: Git을 명령어 기반으로 사용할 수 있게 해주는 터미널 프로그램. Git과 Bash 쉘을 지원.
- **commit**: Git에서 파일의 변경 사항을 저장하는 단위. 각 커밋은 고유한 ID를 가짐.
- **log**: Git에서 커밋 이력을 확인할 수 있는 명령어. `git log` 명령어를 사용해 커밋 내역을 볼 수 있음.
- **checkout**: 특정 브랜치나 커밋으로 작업 공간을 변경하는 Git 명령어. `git checkout <브랜치명>`으로 사용.
- **로컬 저장소**: 사용자의 컴퓨터에 저장된 Git 레포지토리로, 소스 코드와 이력을 포함.
- **원격 저장소**: GitHub, GitLab 등 외부 서버에 호스팅된 Git 레포지토리로, 협업을 위한 공유 공간.
- **repository**: 프로젝트의 소스 코드 및 변경 이력을 저장하는 Git 저장소. 로컬과 원격 저장소가 있음.
- **push**: 로컬 저장소의 변경 사항을 원격 저장소로 전송하는 Git 명령어. `git push`를 사용.
- **pull**: 원격 저장소에서 변경 사항을 로컬 저장소로 가져오는 Git 명령어. `git pull`을 사용.

## Chapter 1 : GUI를 위한 버전 관리 환경 구축하기
### 소스트리 설치하기
1. Sourcetree([Click](https://www.sourcetreeapp.com "Go to https://www.sourcetreeapp.com"))

<p style="text-align: center;">
    <img width="600" height="" src="image/Sourcetree.png">
</p>

### 비주얼 스튜디오 코드 설치하기
> 이미 사용하고있으므로 Pass

### GitHub 둘러보기
> 책 참조

## Chapter 2 : 혼자서 Git으로 버전 관리하기



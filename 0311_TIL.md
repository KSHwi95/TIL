# 복습 (0309)

## 1. 파일이름 수정하는 CLI 명령어 

```
mv `파일명` `변경할 파일명`
```
<br>
<br>

# 복습(0310)
`Ctrl + ` ` : 터미널

`Ctrl` + `Shift` + `p` : 도구 모음

`Ctrl` + `K` > `S` : 열린 파일 전부 저장저장

## 1. git · github 내용정리



`;q` : 터미널키로 이동
### **(1) git**
<br>

## Commit은 파일을 저장하는 것이 아니라 ## **기록을 저장하는것이다.**

![git의 이동경로](https://velog.velcdn.com/images%2Finjoon2019%2Fpost%2Fb2d9d9ce-72b4-41d4-9208-c802b7b3b309%2Fimage.png)

> 아래는 `git` 의 명령어이다.
 
```bash
1. git init 
> .git 폴더가 생성되고 git의 관리에 들어간다. 


2. git add ~ 
> working Directory 에서 Staging Area로 이동

git add *           # 모든 커밋 이동
git add .           # gitignore 제외한 모든 커밋 이동
ㄴ> .gitignore 파일은 git이 add해도 이동하지 않는 파일이다.
git add '파일명'    # git에 하나만 커밋하고 싶을 때


3. git commit -m 커밋사유 
> Staging Area에서 Git directory(Repository)로 이동


4. git status 
> Working Directory와 Staging Area에 남은 기록이 있을때


5. git log 
> 커밋 로그 표시 명령어

git log            #커밋사유외, 일련번호 , 수정자, 날짜를 자세히 볼수 있는 명령어
git log --oneline  #일련번호, 커밋사유를 한줄로 
git log --oneline --all -graph #시점, 커밋사유를 한줄로, 모든 브랜치를, 그래프 형태로


6. ★ git branch : 가지치기 ★
git branch       # 현재 branch 확인
git branch ____  # ___ 라는 브랜치 생성
git branch -d ____ # 브랜치 제거
git branch -D ____ # 브랜치 '완전'제거

git switch ____  # 만들어진 ____ 브랜치로 이동
git switch -c ____ # ____라는 브랜치를 만들고 이동.


7. git merge ____ # 현재 브랜치와 ____ 브랜치의 병합

```

![fast_forward](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2F2hSvT%2FbtqCkPJbfFD%2FKVCcLkKKmpJdAKqmBGeJv0%2Fimg.png)

## **Merge (1) fast forward**
```bash
git switch master
git merge hotfix
> master 브랜치에 C4 커밋을 head한다.
# 그럼 master와 hotfix가 동일한 커밋을헤드하니 hotfix를 제거.
git branch -d hotifx
```  
## **Merge (2) 3 way merge**
## **Merge (3) Conflict** 
> 이 둘 너무 헷갈림

>아래는 따로 공부한 기타 git 명령어
```bash
git reset (복원지점) --hard #복구 불가, 이후 commit 모두 제거.

git revert (복원지점) # 복원
```

### **(2) github**

> 아래는 `github 연결 관련` 명령어이다.

```
1. 최초 연결
git remote add origin ___.git 


2. 연결 해제
git remote rm origin

3. github에 전송
git push origin master

4. 원격 저장소에서 복제
git clone ___.git
> .git 폴더도 같이 전송

5. 원격 저장소 내용을 갱신
git pull origin master

```
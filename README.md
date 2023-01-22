# javaJungseok
자바의 정석 개인공부 레포지토리

## 사용방법

1. 이클립스로 자바 프로젝트 생성
2. gitbash 실행해서 현재 작업중인 경로로 이동
  - 기본적인 CLI (터미널 환경) 명령어
    - `pwd : 현재 디렉토리 확인`
    - `ls : 파일 목록`
    - `ls -al : 숨김 파일 포함 목록`
    - `cd : 디렉토리 이동 `
      - `cd .. ` 하면 이전 디렉토리
    - `vim 파일이름 : cli 환경에서 파일 편집`
      - `a`, `i` : 내용 입력 시작, 끝나면 esc
      - `:` 누르면 다른 명령 가능 `:wq` 저장하고 나가기
      - `:w` 저장 `:q` 나가기
      - 근데 파일 수정해서 저장할게 있으면 그냥 안나가짐. 이때는 `:q!`로 강제로 나가기
      
3. git init으로 git 디렉토리라고 지정해주기
4. `git config --global -e`로 필요한 세팅 해주기

```bash
[user]
	name = sean515
	email = tlgjs4169@gmail.com
[init]
	defaultBranch = main
[push]
	default = current
[pull]
	rebase = true
[core]
	editor = code --wait
	autocrlf = true
[diff]
	tool = vscode
[difftool "vscode"]
	cmd = code --wait --diff $LOCAL $REMOTE
[alias]
	hist = log —graph —all —pretty=format:'%C(yellow)[%ad]%C(reset) %C(green)[%h]%C(reset) | %C(white)%s %C(bold red){{%an}}%C(reset) %C(blue)%d%C(reset)' —date=short
[merge]
	tool = vscode
[mergetool "vscode"]
	cmd = code —wait $MERGED
[mergetool]
	keepBackup = false
```

5. `vim .gitignore`로 파일 만들고 필요한 내용은 [사이트](gitignore.io)에서 확인하기
  - 필요한 세팅은 `eclipse`, `java`, `windows`정도가 있음
  
6. 다음으로 `git remote add origin 레포지토리주소`로 remote 추가해주기
  - remote 확인 명령어는 `git remote -v`
  - 만약 잘못 만들었으면 `git remote rm origin`으로 지우고 다시 만들어주기
 
7. 깃허브에서 레포지토리 생성한거 먼저 `git pull origin main`으로 땡겨와주기. 리드미 파일이 생성되었기 때문
 
8. 세팅 끝났으면 작업하고 git 사용하기!!

<br>

- `git add . : 현재 작업중인 폴더의 모든 파일을 추가하기`
- `git commit -m "메세지내용" : git add 한 것을 커밋한것`
- `git push origin main : 깃허브에 푸쉬하기. 처음 한 번만 해놓으면 다음부터는 git push만 해도 올라감`
- 앞으로 푸쉬하기전에 꼭 `git pull origin main`으로 한 번 땡겨오고 이상 없으면 push 

# Git 기본 명령어

### ✅User Setting
```bash
git config --global user.name ""  #이름 설정
git config --global user.email ""  #메일 설정
```

### ✅Check Status
```bash
git status  #래퍼지토리 상태 확인하기(브랜치, 커밋내용 등)
git ls  #모든 파일 보기
git ls al  #숨긴 파일도 보기
```
##### 🤔 ls 명령어가 안 먹힌다면?  
```bash
git ls-files  #모든 파일 보기
git ls-files 옵션  #option에 따라 보기
```
| `--stage` | `--deleted` | `--others` | `--ignored` | 
|:---:|:---:|:---:|:---:|
| 스테이징에 있는 | 삭제된 | 추적안되는 | 숨겨져있는 |

### ✅History Manage
```bash
git log  #모든 이력 보기
git logt -p  #자세한 이력 보기 (나가길 원하면 q 입력)
git log -숫자  #최신 이력중 '몇'번째까지 이력만 보이기
git log --oneline  #이력 요약보기 (각 이력별 해시_7글자_확인 가능함)
git checkout 커밋해시 or 브랜치명  #특정 과거 이력 또는 브랜치로 돌아가거나 이동하기
git reflog  #HEAD_현재 위치를 의미_가 이동한 이력보기
```

### ✅Create(Modify) & Commit
```bash
git touch .gitignore  #touch: 파일 생성/ .gitignore: git에서 무시할 파일들 모음집
git nano 파일명  #cmd 에서 직접 파일 수정하는 텍스트 편집기가 열림 (입력시 shift+I 로 시작)

git add  #스테이징에 추가하기
git add .  #스테이징에 모든 파일 추가하기
git commit -m "커밋 코멘트"  #스테이징에서 래퍼지토리로 올리기 (+커밋 코멘트)
```

### ✅Branch Manage
```bash
git branch  #브랜치 목록 확인하기
git branch 브랜치명  #생성하기
git checkout 브랜치명  #브랜치간 이동하기 (※이력으로 이동하기도 가능)
git merge 브랜치명  #현재 위치에서 특정 브랜치 병합하기
git brandh -d 브랜치명  #삭제하기
```

### ✅Use GitHub
```bash
git remote -v  #git 연결상태 확인
git remote add origin 원격저장소url  #원격저장소 연결(일반적으로 origin으로 지정함)
git push  #로컬 래퍼지토리에서 원격저장소로 작업파일 올리기
git push -u origin main  #origin에 main 브랜치를 업스트림하기. 그래야 push가 가능해짐
git pull  #원격저장소를 로컬 래퍼지토리에 내려받기
git clone  #원격저장소를 로컬로 그대로 옮겨오기
```

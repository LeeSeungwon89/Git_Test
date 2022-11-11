# 깃 연습장
깃을 연습하는 저장소입니다. 불필요한 커밋은 삭제합니다.

Git을 공부하기에 좋은 서적은 **팀 개발을 위한 Git, GitHub 시작하기(한빛미디어)** 입니다.
설명이 매우 쉽고 구체적입니다. 차근차근 읽고 실습하다 보면 현업에서 깃을 사용하기에 부족하지 않은(충분한) 수준에 도달할 것입니다.

# 깃 명령어

자주 쓰이는 CLI 명령어를 목록화합니다. `[옵션인자]`는 생략 가능, `<필수인자>`는 생략 불가능입니다. 지속적으로 업데이트 중입니다.

명령어 사용에 숙달해지면 작업 속도를 높이거나 세세하게 제어하기 위해 소스트리보다는 CLI를 사용하는 편이 낫습니다.

## 폴더 확인, 생성, 이동하기

- 현재 폴더 위치를 확인합니다.
```
pwd
```

- 현재 폴더 내 파일 목록을 확인합니다.
```
# `-a` 옵션으로 숨김 파일 
ls -a
```

- 홈 폴더로 이동합니다.
```
cd
```

- 특정 디렉토리로 이동합니다.
```
cd <폴더명>
```

- 현재 폴더의 상위 폴더로 이동합니다.
```
cd ../
```

- 현재 폴더에 새 폴더를 만듭니다.
```
mkdir <폴더명>
```

- 화면에 문장을 표시합니다.
```
echo "문장"
```

- Git 저장소(워킹트리) 상태를 확인합니다.
```
git status
```

- Git 저장소(워킹트리) 상태를 요약하여 확인합니다.
```
git status -s
```

- 폴더에서 버전 관리를 시작합니다. `.git`이라는 숨김 폴더(로컬저장소)가 생성됩니다.
```
git init
```

## 옵션 설정하기

- 전역 옵션 내용을 확인합니다. 전역 옵션은 개인 PC에서 많이 사용합니다.
```
git config --global <옵션명>
```

- 전역 옵션 값을 새로 설정합니다.
```
git config --global <옵션명> <새로운값>
```

- 전역 옵션을 삭제합니다.
```
git config --global --unset <옵션명>
```

- 지역 옵션 내용을 확인합니다. 지역 옵션은 공용 PC를 사용하거나 Git을 잠시 사용할 때 설정합니다.
```
git config --local <옵션명>
```

- 지역 옵션 값을 새로 설정합니다.
```
git config --local <옵션명> <새로운값>
```

- 지역 옵션 값을 삭제합니다.
```
git config --local --unset <옵션명>
```

- 시스템 옵션 내용을 확인합니다. 
```
git config --system <옵션명>
```

- 시스템 옵션 값을 새로 설정합니다.
```
git config --system <옵션명> <새로운값>
```

- 시스템 옵션 값을 삭제합니다.
```
git config --system --unset <옵션명> <값>
```

- 현 프로젝트의 모든 옵션을 확인합니다.
```
git config --list
```

- Git의 기본 에디터를 확인합니다. 기본 에디터를 설정할 때는 Git을 재설치하여 설정하는 편이 좋습니다.
```
git config core.editor
git config --global core.editor
git config --local core.editor
```

- 현재 사용 중인 유저명을 확인합니다.
```
git config --global user.name
```

- 현재 사용 중인 유저의 메일 주소를 확인합니다.
```
git config --global user.email
```

- 깃에 계정을 연동합니다.
```
git config --global user.email "메일주소"
git config --global user.name "계정명"
```

## 스테이징 및 커밋하기(수정 중)

- 커밋에 추가할(스테이지에 추가할) 파일을 선택합니다.
```
git add 파일1 파일2 ...
```

- 커밋합니다.
```
git commit
```

- `add` 명령을 생략하고 바로 커밋합니다. 변경된 파일과 삭제된 파일을 자동으로 스테이징하고 커밋합니다. 단, `untracked` 파일은 커밋하지 않습니다.
```
git commit -a
```

- 상세설명을 추가하여 커밋합니다.
```
# `m`은 massage의 약자입니다. 
git commit -m "설명"
```

- 커밋 목록을 확인합니다.
```
git log
```

- 이전 커밋으로 돌아갑니다.
```
git checkout 커밋 코드 앞 부분 7자리
```

- 최신 커밋으로 돌아갑니다.
```
git checkout -
```

- 로컬 저장소의 커밋을 원격 저장소에 올립니다(push).
```
git push origin master
```

- 현재 브랜치에서 새로 생성한 커밋들을 원격 저장소에 올립니다. `-u` 옵션을 설정하면 브랜치의 업스트림을 등록하며 한번 등록한 후에는 `git push`만 입력해도 됩니다.
```
git push [-u] [원격저장소별명] [브랜치명]
```

- 원격 저장소의 변경사항을 워킹트리에 반영합니다.
```
git pull
```

- 원격 저장소의 커밋을 로컬 저장소에 내려받습니다(pull).
```
git pull origin master
```

- 원격 저장소의 브랜치와 커밋들을 로컬 저장소와 동기화합니다. 옵션을 생략하면 모든 원격 저장소에서 모든 브랜치를 동기화합니다.
```
git fetch [원격저장소별명] [브랜치명]
```

- 지정한 프랜치의 커밋들을 현재 브랜치 및 워킹트리에 반영합니다.
```
git merge 브랜치명
```

- 깃허브 원격 저장소에 연동합니다.
```
git remote add origin 원격 저장소 주소
```

- 원격 저장소의 커밋을 로컬 저장소에 복제(clone)합니다.
```
# 원격 저장소 주소 뒤에 ' .'을 붙이면 폴더 안에 있는 파일만 복사합니다.
# 예컨대 https://github.com/LeeSeungwon89/Git_Test.git .형태입니다.
git clone 원격 저장소 주소
```

- 추가 예정

# 소스트리

사실 소스트리는 GUI라서 굳이 메모가 필요할까? 사용법이 간단해서 음. 일단 고민해보도록 하겠습니다. 소스트리 설치 방법은 [링크](https://www.youtube.com/watch?v=f2qHHLZr3ME&t=439s)를 참고하시기 바랍니다. 별도의 계정 가입 절차 없이 깃허브 계정만  바로 사용할 수 있습니다.

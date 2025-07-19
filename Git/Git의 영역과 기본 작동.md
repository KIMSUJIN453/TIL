# Git의 영역과 기본 작동
## Git의 영역
### 1.Working Directory
실제 **작업 중인 파일들이 위치하는 영역**  
작업하고 무엇을 추가할지 정리해서 넘기면 Staging Area로 간다.  

### 2.Staging Area
Working Directory에서 변경된 파일 중 다음 버전에 포함시킬 파일들을 선택적으로 추가하거나 제외할 수 있는 **중간 준비 영역**  
변경할 내용들이 다 모은 후 실제 적용할 것들을 저장하면 Repository에 저장된다.  

### 3. Repository
**버전 이력과 파일들이 영구적으로 저장되는 영역**  
모든 버전과 변경 이력이 기록된다.  
- 버전 = **Commit**  
    Git에서는 버전을 Commit이라고 한다.  
    **Commit은 변경된 파일들을 저장하는 행위**이며,  
    마치 사진을 찍듯이 기록한다 하여 snapshot이라고도 한다.  

## Git의 기본 작동
### 1. git add
```
git add <file>
```
Working Dircetory에서 작업한 파일을 Staging Area로 보낼 때 사용하는 명령어이다.  
Working Directory에서는 'Untracked' 혹은 'Modified'라고 표시되던 파일이  
Staging Area로 넘어가면 'New file' 혹은 'Modified'라고 표시된다.  
```
git add .
```
만약 파일 한 개씩 추가하기 귀찮고, 현 위치의 모든 것을 추가하고 싶다면 git add 이후 . 한 개만 붙이면 된다.  


### 2. git commit
```
git commit -m "first commit"
```
Staging Area에 있는 파일을 Repository로 보낼 때 사용하는 명령어이다.  
Repository로 넘어간 파일은 'Nothing to commit, working tree clean'이라고 표시된다.  
commit의 이름을 설정해주고 싶다면 **git commit -m "commit 메시지"** 로 명령해주면 된다.  
(대부분 commit의 이름을 붙여서 저장하는 경우가 많다.)  


### 3. git init
```
git init
```
git을 사용할 때는 해당 명령어(git init)을 통해 **로컬 저장소 초기화**를 해준다.  
이를 통해 git의 관리를 받기 시작한 디렉토리 내에서는 (master) or (main)이 표시된다.  
  
**주의사항**  
git 로컬 저장소인 디렉토리 내부에 또다른 디렉토리를 만들고 git init 명령어를 입력하면 안 된다.  
git 저장소 안에 git 저장소가 있으면 가장 바깥 쪽의 git 저장소가 안쪽의 git 저장소의 변경사항을 추적할 수 없기 때문이다.  

### 4. commit 작성자 정보 설정
처음으로 commit을 생성하려고 할 때 commit 작성자 정보가 설정되어있지 않으면 작성자 정보를 요구하는 내용이 뜬다.  
그럴 때는 요청하는 양식에 맞춰 정보를 보내주면 된다.  
```
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```
정보 등록 후 다시 commit 생성하면 정상적으로 작동한다.  
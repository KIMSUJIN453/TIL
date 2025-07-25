# CLI
## Command Line Interface
컴퓨터와 대화하는 것으로, 검은 화면에 명령어를 타이핑하여 소통하는 터미널 또는 명령 프롬프트(cmd)

## CLI 특징
효율적이고, 정밀 제어와 자동화가 가능하다
서버, 클라우드 등 그래픽이 없는 개발 환경의 필수 도구이다.

## CLI 기초 문법
- **touch** : 파일 만들기
- **mkdir** : 새로운 디렉토리 만들기 (make directory)
    -> 새 폴더 만들기
    - **dir** : 폴더 (directory)
- **cd** : 디렉토리 경로 변경 (change directory)
    -> 폴더 경로 변경
    - **cd .** : 현재 내가 있는 폴더 위치
    - **cd ..** : 현재 내가 있는 위치에서 상위 폴더로 이동
- **rm** : 파일 삭제 (remove)
    - **rmdir** : 폴더 삭제
- **ls** : 현재 작업 중인 디렉토리 내부 폴더/파일 목록 출력
- **pwd** : 현재 작업 중인 폴더의 절대 경로를 출력

### CLI에서 가장 중요한 것
**경로 잘 파악하기!!!**

## 경로 관련 개념
- **루트 디렉토리 (/)** : 모든 주소의 시작점
- **홈 디렉토리 (~)** : 터미널을 처음 켰을 때 시작하는 나의 기본 공간
- **절대 경로** : 시작점부터 목적지까지의 전체 주소
    - 누가 어디에서 보나 항상 똑같다.
    - ex) /Users/Desktop
- **상대 경로** : *현재 내 위치*를 기준으로 한 주소
    - ex) cd .. : 나의 현재 위치 기준 상위 폴더로 이동
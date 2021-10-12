# git bash 에서 tmux 접속

### tmux
- 세션 멀티 플렉서, 세션 관리기능
- bash 를 통해 여러명이 동시에 코드작업을 가능하게 해준다.

### 방법
```
$ ./ubuntu_start.sh : 우분투 서버 접속 (쥬피터 노트북 접속할 디렉토리로 이동)
$ tmux new -s dss : dss 세션 만들기
$ tmux ls : 현재 만들어진 tmux 세션 정보 확인, 현재 w0 생성
$ tmux 창에서 ctrl + b, c : w1 추가 생성 됨, 누를때마다 새로운 윈도우가 생성됨
$ tmux ls 확인하면 :
=> dss: 2 windows (created Fri Sep 18 16:55:53 2020) [104x27] (attached) : dss 세션에 2개 윈도우 나옴
$ ctrl + b, 0 1 2 3 ... : 각 윈도우로 이동, 이동하면 해당 윈도우에 * 생김

$ jupyter notebook : 접속하고 다른 윈도우로 이동하면 bash 사용이 가능하다.

$ tmux attach -t dss : tmux의 dss 세션에 접속, w0 에 연결됨
$ 한쪽 창에서 입력하면 다른 창에서도 똑같이 입력됨
$ exit : 현재 윈도우 종료
```

# MySQL 설정법

## Prerequisite(전제 조건)

```make
기존 Vue 설치시 작업했던 node.js 설정에서 설치했던
C/C++ Native 라이브러리와 python 등등의 설치가 올바르게 되어 있어야함

만약 nodejs 설치시 C/C++ Native 설정을 하지 못한 경우
포맷하지 않는 이상 다시 설정할 수 없을 수도 있다.
혹은 레지스트리 설정을 다 까뒤집어야해서 포맷이 차라리 속 편할 수 있는데
우선 아래 사이트에서 호환 라이브러리를 다운받아 설치한다.
```

https://support.microsoft.com/en-us/topic/the-latest-supported-visual-c-downloads-2647da03-1eea-4433-9aff-95f26a218cc0

```make
임시방편일 뿐이므로 향후 다른 문제가 발생할 수 있고
시간이 있을때 미리 포맷하고 다시 설정을 해두는 것이 좋을 수 있다.
추가적으로 Python 3.9 버전도 수동으로 설치하도록 한다.
이 부분도 nodejs 설치시 자동으로 설치하므로
만약 포맷하고 다시 하는 사람이라면 수동으로 할 필요는 없다.
```

## 용량이 부족한 경우

```make
아래 링크를 참고합니다.

https://dang-dang12.tistory.com/7
```

## brew 가 없는 경우 (MAC 한정)

```make
https://brew.sh/index_ko
```

## MySQL Shell 설치 안될 경우 (Windows 한정)

```make
https://dev.mysql.com/downloads/shell/
```

## How to install MySQL on Windows

```make
1. Google에서 MySQL을 검색한다.
2. 공식 사이트에 진입한다.
3. 다운로드를 누른다.
   https://www.mysql.com/downloads/
4. https://dev.mysql.com/downloads/mysql/ 페이지로 이동하자!
5. Windows (x86, 64-bit), ZIP Archive가 아닌 MSI를 다운로드한다.
6. No thanks, just start my download. <<<<<< 누르면 오라클 회원가입 필요없음
7. 다운로드가 꽤 길기 때문에 티타임을 가지도록 합니다.
8. 다운이 완료되면 클릭하여 설치하도록 한다.
9. 설치 준비를 한다고 하면서 뭔가 좀 오랫동안 작업을 한다.

1) Developer Default 선택
2) VS를 위한 MySQL 설정이 있는데 건드리지 않고 Next
3) 뭔가 비어 있는것이 있어 설치가 제대로 되지 않을수도 있다고 하지만 일단 yes하고 설치한다.
4) 서버가 들어있는지 확인하고 Execute를 누르도록 한다.
5) 또 한참 설치한다 ... 커피를 가져오라 ...
6) 모두 Complete가 되었다면 Next로 진행한다.
   여기서 중요한 부분은 Server, Shell, ODBC, C++, J, Python 에 해당한다.
7) 이후 Next
8) Config Type: Development Computer
   TCP/IP Port: 3306 <<<--- MySQL이 사용하는 Port임
   확인후 Next
9) Use Legacy Authentication Method (Retain MySQL 5.x Compatibility) 선택
10) 비밀번호를 학원 맞춤형으로 khWeb@123
11) 시스템 구동시 MySQL 서버 시작 체크하고 Next
12) 어떤 내용들이 진행되는지 간략한 요약을 보여주는데 Execute를 누른다.
13) 설치가 완료되면 Finish를 누른다.
14) Next를 누른다.
15) Bootstrap 부분에 문제가 생기므로 차후 수동 설정으로 진행 -> Finish 클릭
16) Next
17) root 계정 비밀번호 넣으란 자리에 설정한 비번 설정해서
    Connection Succeeded가 나와야 함
    나오면 Next
18) Execute 클릭
19) Finish
20) Next
21) Finish
22) Workbench와 Shell 올라오면 성공!
23) \quit 으로 mysqldsh를 종료하고 workbench도 끈다.
24) 시작에서 MySQL 8.0 Command Line Client - Unicode를 사용하도록 한다.
25) 설정한 비밀번호를 입력하면 mysql> 쉘이 뜬다.
26) 내부에서 show databases;
27) select version(); 등이 잘 동작하면 모든것이 clear한 상태!
```

## MySQL 비밀번호를 잘못 입력했을 경우

```make
https://jjeongil.tistory.com/1484
```

## How to install MySQL on Linux & Unix(MAC)

```make
sudo apt-get install mysql
```

아래와 같은 에러 발생시!  

```make
ERROR 1045 (28000): Access denied for user 'root'@'localhost' (using password: YES)
```

mysql_secure_installation <<<  

## How to install MySQL on Unix(MAC)

```make
https://devyurim.github.io/data%20base/mysql/2018/08/13/mysql-1.html
```

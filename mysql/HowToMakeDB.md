# MySQL DB Control

## How to Control DB ?

1. 먼저 DB 계정으로 로그인한다.  
2. 이후 아래 명령을 입력하여 새로운 스키마를 작성한다.  

```make
create schema `non_jpa_db` default character set utf8mb4;
```

3. 이제 다시 아래의 명령을 입력하여 새로운 스키마 작성을 확인한다.

```make
show databases;
```

4. 현재 문자열 셋을 보기 위해 아래 명령을 통해 utf8이 박혀있는지 확인한다.  

```make
status;
```

* 사용자 계정 생성시 보안 문제 발생하는 경우 (MAC에서 발생하는 문제임)  

```make
비밀번호 정책 다운 그레이드
현재 정책값 보기
show variables like 'validate_password%';
낮추기
set global validate_password.policy=LOW;
```

5. 이제 사용자 계정을 생성한다.  
   root 계정 사용하면 컴퓨터 털어가세요란 뜻이라 절대로 하면 안됨  
   
```make
create user eddi@localhost identified by 'eddi@123';
```

6. 사용자 계정이 DB를 활용할 수 있도록 권한을 위임한다.  

```make
grant all privileges on non_jpa_db.* to eddi@localhost;
```

7. 현재 상태 저장  

```make
flush privileges;
```

8. 권한이 잘 설정되었는지 체크한다.  

```make
show grants for 'eddi'@'localhost';
```

9. 이제 실제 테이블을 만들어보자!

```make
use non_jpa_db;
create table board(
   board_no int not null auto_increment,
   title varchar(200) not null,
   content text null,
   writer varchar(50) not null,
   reg_date timestamp not null default now(),
   primary key(board_no)
);

use를 통해 어떤 DB(스키마)를 사용할지 지정함[앞서 만든게 non_jpa_db임
create table을 통해 테이블을 생성할 수 있음
현재 table 이름은 board 에 해당함
테이블 내부에는 column(열)이 구성됨
첫 번째 열로 board_no라는 이름이 왔고
int not null auto_increment로 0이 되어선 안되며 숫자값이고 자동으로 1씩 증가함을 의미함
두 번째 열로 title이라는 이름이 왔고
varchar(200)으로 문자 200개를 받으며 not null을 통해 null이 되면 안된다고 한다.
세 번째 열로 content는 text로 상당히 많은 수의 문자열을 커버할 수 있고 null 이어도 된다고 한다.
네 번째는 writer 로 varchar(50)에 not null 이다.
다섯 번째는 reg_date이며 timestamp로 시간을 표현한다.
default 를 통해 기본값을 지정하는데 now() 이므로 현재 시간을 뜻한다.
primary key(board_no)를 통해 이 테이블의 고유한 정보를 board_no가 관리함을 명시해준다.
```

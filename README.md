# SpringDB-1

### H2 데이터베이스 설정

1. [다운로드 링크](https://www.h2database.com/html/main.html)
2. 윈도우 사용자 실행: ./bin/h2.bat
3. 데이터베이스 파일 생성 방법
   - 사용자명은 **sa** 입력
   - JDBC URL에 다음 입력,
   - **jdbc:h2:~/test** (최초 한번) -> 이 경우 연결 시험을 호출하면 오류가 발생한다. 연결을 직접 눌러주어야 한다.
   - ~/test.mv.db 파일 생성 확인
   - 이후부터는 **jdbc:h2:tcp://localhost/~/test** 이렇게 접속
4. 테이블 생성하기
   ```sql
   drop table member if exists cascade;
   create table member (
   member_id varchar(10),
   money integer not null default 0,
   primary key (member_id)
   );
   insert into member(member_id, money) values ('hi1',10000);
   insert into member(member_id, money) values ('hi2',20000);
   ```

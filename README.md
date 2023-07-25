# DB-Practice
DB공부한 것(07/25)

![실습스크립트](https://github.com/HeoHoJun/DB-Practice/assets/116245224/99f5431e-fbef-4fec-bcbc-b660a47eb5af)

실습스크립트를 통해서 예제를 공부하였다.

테이블에서 특정 열(COLUMN) 선택하기

SELECT empno, ename, sal
  
FROM emp;

<출력결과>

![출력결과](https://github.com/HeoHoJun/DB-Practice/assets/116245224/98824a69-b680-4ef8-9a19-f763ec28329e)

테이블에서 모든 열(COLUMN) 출력하기

SELECT *

FROM emp;

<출력결과>

![출력결과1](https://github.com/HeoHoJun/DB-Practice/assets/116245224/27e0a87d-eec0-4530-877c-3a13b6f37e28)

컬럼 별칭을 사용하ㅏ여 출력되는 컬럼명 변경하기

SELECT empno as 사원번호, ename as 사원이름, sal as "Salary"

FROM emp;

<출력결과>

![출력결과2](https://github.com/HeoHoJun/DB-Practice/assets/116245224/2bf298d3-c199-4d36-a0fc-7aa8f53de276)

-> 사원 테이블의 사원 번호와 이름과 월급을 출력하는데 컬럼명을 한글로 '사원번호', '사원이름'으로 출력

연결 연산자 사용하기(||)

SELECT ename || sal

FROM emp;

<출력결과>

![출력결과3](https://github.com/HeoHoJun/DB-Practice/assets/116245224/a5f19b37-816b-46a1-998f-a351553ec299)

-> 사원 테이블의 이름과 월급을 서로 붙여서 출력

SELECT ename || '의 월급은 ' || sal || '입니다 ' as 월급정보

FROM emp;

<출력결과>

![출력결과4](https://github.com/HeoHoJun/DB-Practice/assets/116245224/8c9b4b7a-a4f7-417c-be91-12e00f5145a9)

SELECT ename || '의 직업은 ' || job || '입니다 ' as 직업정보

FROM emp;

<출력결과>

![출력결과5](https://github.com/HeoHoJun/DB-Practice/assets/116245224/5319e27e-d67c-419e-855b-8e922c0b16f2)

중복된 데이터를 제거해서 출력하기(DISTINCT)

SELECT DISTINCT job

FROM emp;

<출력결과>

![출력결과6](https://github.com/HeoHoJun/DB-Practice/assets/116245224/51df0f52-f085-4a4c-aa07-ce7f17552cf7)

-> 사원 테이블에서 직업을 출력하는데 중복된 데이터를 제외하고 출력

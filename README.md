# DB-Practice
DB공부한 것

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


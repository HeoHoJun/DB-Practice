# DB-Practice

- 7월 27일 공부한 내용

**날짜형으로 데이터 유형 변환하기(TO_DATE)**

SELECT ename, hiredate

FROM emp

WHERE hiredate = TO_DATE('81/11/17','RR/MM/DD');

<출력 결과>

![출력결과27](https://github.com/HeoHoJun/DB-Practice/assets/116245224/3ad18ee9-4a30-4a27-9aa7-76a17e3da6b9)

-> 81년 11월 17일에 입사한 사원의 이름과 입사일 출력


**NULL 값 대신 다른 데이터 출력하기(NVL, NVL2)**

SELECT ename, comm, NVL(comm, 0)

FROM emp;

<출력 결과>

![출력결과28](https://github.com/HeoHoJun/DB-Practice/assets/116245224/13cc9eba-f4cc-4550-bb95-017953981b35)

-> 이름과 커미션을 출력하는데 커미션이 NULL인 사원들은 0으로 출력


**IF문을 SQL로 구현하기(DECODE)**

SELECT ename, deptno, DECODE(deptno,10,300,20,400,0) as 보너스

FROM emp;

<출력 결과>

![출력결과29](https://github.com/HeoHoJun/DB-Practice/assets/116245224/7a1cf248-23c8-48b2-81e1-b267ae339a5e)

-> 이름과 부서 번호와 보너스를 출력


**IF문을 SQL로 구현하기(CASE)**

SELECT ename, job, sal, CASE WHEN sal >= 3000 THEN 500

WHEN sal >= 2000 THEN 300

WHEN sal >= 1000 THEN 200
                             
ELSE 0 END AS BONUS

FROM emp

WHERE job IN ('SALESMAN','ANALYST');

<출력 결과>

![출력결과30](https://github.com/HeoHoJun/DB-Practice/assets/116245224/a348f6d6-53a3-4567-aed5-6609c927d6ce)

-> 이름, 직업, 월급, 보너스를 출력

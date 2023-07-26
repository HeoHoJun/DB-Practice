# DB-Practice
- 7월 26일 공부한 내용
  

**WHERE절 배우기 (숫자 데이터 검색)**

SELECT ename, sal, job

FROM emp

WHERE sal = 3000;

<출력결과>

![출력결과1](https://github.com/HeoHoJun/DB-Practice/assets/116245224/a2f1205f-050a-4143-802a-fa2b64867dce)

-> 월급이 3000인 사원들의 이름, 월급, 직업 출력

SELECT ename as 이름, sal as 월급

FROM emp

WHERE sal >= 3000;

<출력결과>

![출력결과2](https://github.com/HeoHoJun/DB-Practice/assets/116245224/2b6b8397-dc39-4495-85a3-b88d36d1f3fa)

-> 비교 연산자를 사용하여 월급이 3000 이상인 사원들의 이름과 월급 출력


**WHERE절 배우기 (문자와 날짜 검색)**

SELECT ename, sal, job, hiredate, deptno

FROM emp

WHERE ename='SCOTT';

<출력결과>

![출력결과3](https://github.com/HeoHoJun/DB-Practice/assets/116245224/3077321d-32c0-4ad8-9e64-e6b4de9bfee5)

-> 이름이 SCOTT인 직원의 이름, 월급, 직업, 입사일, 부서번호 출력

SELECT ename, hiredate

FROM emp

WHERE hiredate ='81/11/17';

<출력결과>

![출력결과4](https://github.com/HeoHoJun/DB-Practice/assets/116245224/e444c946-6d62-4e1f-a2d6-72f6a5e0b5de)

-> 81년 11월 17일에 입사한 사원의 이름과 입사일 출력



**산술 연산자 배우기(*, /, +, -)**

SELECT ename, sal*12 as 연봉

FROM emp

WHERE sal*12 >= 36000;

<출력결과>

![출력결과5](https://github.com/HeoHoJun/DB-Practice/assets/116245224/6ec8fc36-1ec1-4d80-a75d-5b8b2f6827fe)

-> 연봉이 36000 이상인 사원들의 이름과 연봉 출력



**비교 연산자 배우기 (>, <, >=, <=, = , !=, <>, ^=)**

SELECT ename, sal, job, deptno

FROM emp

WHERE sal <= 1200;

<출력결과>

![출력결과6](https://github.com/HeoHoJun/DB-Practice/assets/116245224/61830a82-9584-49fb-b5bc-902ae65b37df)


**비교 연산자 배우기(BETWEEN AND)**

SELECT ename, sal

FROM emp

WHERE sal BETWEEN 1000 AND 3000;

<출력결과>

![출력결과7](https://github.com/HeoHoJun/DB-Practice/assets/116245224/4e18818c-0f93-4675-b005-6b0cc424cb6d)


**비교 연산자 배우기(LIKE)**

SELECT Ename, sal

FROM emp

WHERE ename LIKE 'S%';

<출력결과>

![출력결과8](https://github.com/HeoHoJun/DB-Practice/assets/116245224/18035473-e0a2-4b08-b531-925c58a049aa)

-> 이름의 첫 글자가 S로 시작하는 사원들의 이름과 월급 출력


**비교 연산자 배우기(IS NULL)**

SELECT ename, comm

FROM emp

WHERE comm is null;

<출력결과>

![출력결과9](https://github.com/HeoHoJun/DB-Practice/assets/116245224/c8b371bd-1f18-417d-a7df-e793dbaeaa43)

-> 커미션이 NULL인 사원들의 이름과 커미션 출력


**비교 연산자 배우기(IN)**

SELECT ename, sal, job

FROM emp

WHERE jon in ('SALESMAN', 'ANALYST', 'MANAGER');

<출력결과>

![출력결과10](https://github.com/HeoHoJun/DB-Practice/assets/116245224/47fd6231-6c6d-4bb4-9b68-95bad50b989e)

-> 직업이 SALESMAN, ANALYST, MANAGER인 사원들의 이름, 월급, 직업 출력


**논리 연산자 배우기(AND, OR, NOT)**

SELECT ename, sal, job

FROM emp

WHERE job='SALESMAN' AND sal >= 1200;

<출력결과>

![출력결과11](https://github.com/HeoHoJun/DB-Practice/assets/116245224/73f4b874-b5df-4a1e-9327-3c2ea1a9334f)

-> 직업이 SALESMAN이고 월급이 1200 이상인 사원들의 이름, 월급, 직업 출력

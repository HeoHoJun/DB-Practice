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


**대소문자 변환 함수 배우기(UPPER, LOWER, INITCAP)**

SELECT UPPER(ename), LOWER(ename), INITCAP(ename)

FROM emp;

<출력 결과>

![출력결과12](https://github.com/HeoHoJun/DB-Practice/assets/116245224/1af8a0df-eb7c-4e0c-8779-2dc81d14d6b5)

-> 사원 테이블의 이름을 출력하는데 첫 번째 컬럼은 이름을 대문자로 출력하고 두 번째 컬럼은 이름을 소문자로 출력, 세 번째 컬럼은 이름의 첫 번째 철자는 대문자로 하고 나머지는 소문자로 출력


**문자에서 특정 철자 추출하기(SUBSTR)**

SELECT SUBSTR('SMITH',1,3)

FROM DUAL;

<출력 결과>

![출력결과13](https://github.com/HeoHoJun/DB-Practice/assets/116245224/47e65689-3152-434c-bda2-a18bb9707480)

-> 영어 단어 SMITH에서 SMI만 잘라내서 출력


**문자열의 길이를 출력하기**

SELECT ename, LENGTH(ename)

FROM emp;

<출력 결과>

![출력결과14](https://github.com/HeoHoJun/DB-Practice/assets/116245224/34e79e33-7ea4-4f5a-ae7c-fd3d41df362c)

-> 이름을 출력하고 그 옆에 이름의 철자 개수를 출력


**문자에서 특정 철자의 위치 출력하기(INSTR)**

SELECT INSTR('SMITH','M')

FROM DUAL;

<출력 결과>

![출력결과15](https://github.com/HeoHoJun/DB-Practice/assets/116245224/d4044d2e-f974-40b3-a3e1-09f5cc2e837b)

-> 사원 이름 SMITH에서 알파벳 철자 M이 몇 번째 자리에 있는지 출력


**특정 철자를 다른 철자로 변경하기(REPLACE)**

SELECT ename, REPLACE(sal, 0, '*')

FROM emp;

<출력 결과>

![출력결과16](https://github.com/HeoHoJun/DB-Practice/assets/116245224/d2791b83-bb31-43ef-b130-4ed8fa7fa0fe)

-> 이름과 월급을 출력하는데 월급을 출력할 때 숫자 0을 *(별표)로 출력


**특정 철자를 N개 만큼 채우기(LPAD, RPAD)**

SELECT ename, LPAD(sal,10,'*') as salary1, RPAD(sal,10,'*') as salary2

FROM emp;

<출력 결과>

![출력결과17](https://github.com/HeoHoJun/DB-Practice/assets/116245224/3342edfd-978c-46eb-b102-8d71903867e0)

-> 이름과 월급을 출력하는데 월급 컬럼의 자릿수를 10자리로 하고 월급을 출력하고 남은 나머지 자리에 별표(*)를 채워서 출력


**특정 철자 잘라내기(TRIM, RTRIM, LTRIM)**

SELECT 'smith', LTRIM('smith','s'), RTRIM('smith','h'), TRIM('s' from 'smiths')

FROM dual;

<출력 결과>

![출력결과18](https://github.com/HeoHoJun/DB-Practice/assets/116245224/a8a7d740-97b3-40f8-8ce7-e80ba85e0a36)

-> 첫 번째 컬럼은 영어 단어 smith 철자를 출력하고 두 번째 컬럼은 영어 단어 smith에서 s를 잘라서 출력하고 세 번째 컬럼은 영어 단어 smith에서 h를 잘라서 출력하고 네 번째 컬럼은 영어 단어 smiths의 양쪽에 s를 잘라서 출력


**반올림해서 출력하기(ROUND)**

SELECT '876.567' as 숫자, ROUND(876.567,1)

FROM dual;

<출력 결과>

![출력결과19](https://github.com/HeoHoJun/DB-Practice/assets/116245224/7d03fe4b-ea0c-4728-8a5c-5537f43e2e8d)

-> 876.567 숫자를 출력하는데 소수점 두 번째 자리인 6에서 반올림해서 출력


**숫자를 버리고 출력하기(TRUNC)**

SELECT '876.567' as 숫자, TRUNC(876.567,1)

FROM dual;

<출력 결과>

![출력결과20](https://github.com/HeoHoJun/DB-Practice/assets/116245224/bc2c10b8-bdac-4934-8be7-4993321767be)

-> 876.567 숫자를 출력하는데 소수점 두 번째 자리인 6과 그 이후의 숫자들을 모두 버리고 출력


**나눈 나머지 값 출력하기(MOD)**

SELECT MOD(10,3)

FROM DUAL;

<출력 결과>

![출력결과21](https://github.com/HeoHoJun/DB-Practice/assets/116245224/e2eb4121-c7a9-426a-b9fb-d9db71682e1f)

-> 숫자 10을 3으로 나눈 나머지값이 어떻게 되는지 출력


**날짜 간 개월 수 출력하기(MONTHS_BETWEEN)**

SELECT ename, MONTHS_BETWEEN(sysdate,hiredate)

FROM emp;

<출력 결과>

![출력결과22](https://github.com/HeoHoJun/DB-Practice/assets/116245224/c6a4c18c-57cb-466e-837a-0aeb471ee04d)

-> 이름을 출력하고 입사한 날짜부터 오늘까지 총 몇 달을 근무했는지 출력


**개월 수 더한 날짜 출력하기(ADD_MONTHS)**

SELECT ADD_MONTHS(TO_DATE('2019-05-01','RRRR-MM-DD'), 100)

FROM DUAL;

<출력 결과>

![출력결과23](https://github.com/HeoHoJun/DB-Practice/assets/116245224/6d225180-c4c2-4596-8a53-be8f988ec1cc)

-> 2019년 5월 1일로부터 100달 뒤의 날짜는 어떻게 되는지 출력


**특정 날짜 뒤에 오는 요일 날짜 출력하기(NEXT_DAY)**

SELECT '2019/05/22' as 날짜, NEXT_DAY('2019/05/22', '월요일')

FROM DUAL;

<출력 결과>

![출력결과24](https://github.com/HeoHoJun/DB-Practice/assets/116245224/84f7ed15-9ff4-46be-892a-e15ed1a18069)

-> 2019년 5월 22일로부터 바로 돌아올 월요일의 날짜가 어떻게 되는지 출력


**특정 날짜가 있는 달의 마지막 날짜 출력하기(LAST_DAY)**

SELECT "2019/05/22' as 날짜, LAST_DAY('2019/05/22') as "마지막 날짜"

FROM DUAL;

<출력 결과>

![출력결과25](https://github.com/HeoHoJun/DB-Practice/assets/116245224/e43fb90c-1752-4d6d-a001-5b9398938208)

-> 2019년 5월 22일 해당 달의 마지막 날짜가 어떻게 되는지 출력


**문자형으로 데이터 유형 변환하기(TO_CHAR)**

SELECT ename, TO_CHAR(hiredate,'DAY') as 요일, TO_CHAR(sal,'999,999') as 월급

FROM emp

WHERE ename='SCOTT';

<출력 결과>

![출력결과26](https://github.com/HeoHoJun/DB-Practice/assets/116245224/32d54fa7-d78b-4604-9d3d-35dc3f5b4fdc)

-> 이름이 SCOTT인 사원의 이름과 입사한 요일을 출력하고 SCOTT의 월급에 천 단위를 구분할 수 있는 콤마를 붙여 출력

# DB-Practice

- ## 7월 30일 학습 내용

- #### 최대값 출력하기(MAX), 최소값 출력하기(MIN), 평균값 출력하기(AVG), 토탈값 출력하기(SUM), 건수 출력하기(COUNT), 데이터 분석 함수로 순위 출력하기(RANK), 데이터 분석 함수로 순위 출력하기(DENSE_RANK), 데이터 분석 함수로 등급 출력하기(NTILE), 데이터 분석 함수로 순위의 비율 출력하기(CUME_DIST)

1. 최대값 출력하기(MAX)

   사원 테이블에서 최대 월급 출력하기

   SELECT MAX(sal)
   
   FROM emp;

   <출력 결과>
   
   ![화면 캡처 2023-07-30 072646](https://github.com/HeoHoJun/DB-Practice/assets/116245224/443904fd-2b04-48af-89e1-0288d042374e)

   MAX 함수를 이용하면 최대값을 출력할 수 있다.

2. 최소값 출력하기(MIN)

   직업이 SALESMAN인 사원들 중 최소 월급을 출력하기

   SELECT MIN(sal)
   
   FROM emp
   
   WHERE JOb='SALESMAN';

   <출력 결과>

   ![화면 캡처 2023-07-30 073347](https://github.com/HeoHoJun/DB-Practice/assets/116245224/2d6e3aa9-6696-4c57-920b-7b4f7ff4ea32)

   FROM절에서 사원 테이블을 가져오고 WHERE절을 실행하면 직업이 SALESMAN인 사원들로 데이터를 제한한다. SELECT절을 실행하면서 그 중 최소 월급을 출력한다.

3. 평균값 출력하기(AVG)

   사원 테이블의 평균 월급 출력하기

   SELECT AVG(comm)
   
   FROM emp;

   <출력 결과>

   ![화면 캡처 2023-07-30 074629](https://github.com/HeoHoJun/DB-Practice/assets/116245224/82dee8d7-7092-4d2c-9758-c62fc07b7ecb)

4. 토탈값 출력하기(SUM)

   부서 번호와 부서 번호별 토탈 월급을 출력하기

   SELECT deptno, SUM(sal)

   FROM emp

   GROUP BY deptno;

   <출력 결과>

   ![화면 캡처 2023-07-30 074925](https://github.com/HeoHoJun/DB-Practice/assets/116245224/027b250c-28d9-420c-8caf-cd480b1e2b50)

5. 건수 출력하기(COUNT)

   SELECT COUNT(empno)

   FROM emp;

   <출력 결과>

   ![화면 캡처 2023-07-30 075527](https://github.com/HeoHoJun/DB-Practice/assets/116245224/478d2a47-73bd-4845-908c-d080b4b138ff)

   CONUT 함수는 건수를 세는 함수이다.

6. 데이터 분석 함수로 순위 출력하기(RANK)

   직업이 ANALYST, MANAGER인 사원들의 이름, 직업, 월급, 월급의 순위 출력하기

   SELECT ename, job, sal, RANK() over (ORDER BY sal DESC) 순위

   FROM emp

   WHERE job in ('ANALYST','MANAGER');

   <출력 결과>

   ![화면 캡처 2023-07-30 075927](https://github.com/HeoHoJun/DB-Practice/assets/116245224/24a72f3b-0193-46f8-9aff-f28e1f97319f)

   RANK()는 순위를 출력하는 데이터 분석 함수이다. RANK() 뒤에 OVER 다음에 나오는 괄호 안에 출력하고 싶은 데이터를 정렬하면 SQL 문장을 넣으면 그 컬럼 값에 대한 데이터의 순위가 출력된다.

7. 데이처 분석 함수로 순위 출력하기(DENsE_RANK)

   직업이 ANALYST, MANAGER인 사람들의 이름, 직업, 월급, 월급의 순위를 출력하는데 순위 1위인 사원이 두 명이 있을 경우 다음 순위가 3위로 출력되지 않고 2위로 출력하기

   SELECT ename, job, sal, RANK() over (ORDER BY sal DESC) AS RANK, DENSE_RANK() over (ORDER BY sal DESC) AS DENSE_RANK

   FROM emp

   WHERE job in ('ANALYST','MANAGER");

   <출력 결과>

   ![화면 캡처 2023-07-30 080829](https://github.com/HeoHoJun/DB-Practice/assets/116245224/35224d30-07f9-4bc5-be48-8e70f6352ff9)

   RANK 함수는 순위 1위가 두 명이어서 다음에 바로 3위를 출력했지만, DENSE_RANK는 2위로 출력한다.

8. 데이터 분석 함수로 등급 출력하기(NTILE)

   이름과 월급, 직업, 월급의 등급 출력하기 (월급의 등급은 4등급으로 나눠 1등급(0~25%), 2등급(25~50%), 3등급(50~75%), 4등급(75~100%)으로 출력)

   SELECT ename, job, sal, NTILE(4) over (order by sal desc nulls last) 등급

   FROM emp

   WHERE job in ('ANALYST','MANAGER','CLERK');

   <출력 결과>

   ![화면 캡처 2023-07-30 081414](https://github.com/HeoHoJun/DB-Practice/assets/116245224/f623a12b-3360-4632-9991-5aa6a8a4168c)

9. 데이터 분석 함수로 순위의 비율 출력하기(CUME_DIST)

   이름과 월급, 월급의 순위, 월급의 순위 비율을 출력하기

   SELECT ename, sal, RANK() over (order by sal desc) as RANK, DENSE_RANK() over (order by sal desc) as DENSE_RANK, CUME_DIST() over (Order by sal desc) as CUM_DIST

   FROM emp;

   <출력 결과>

   ![화면 캡처 2023-07-30 081819](https://github.com/HeoHoJun/DB-Practice/assets/116245224/b53ac0df-31a1-4775-841b-9f0c64919911)

   

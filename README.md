# Join
SQL<br>
## Join란?
두 개 이상의 테이블을 서로 연결하여 데이터를 검색할 때 사용하는 방법<br>
두 개의 테이블을 마치 하나의 테이블인 것처럼 보여준다.<br>

## 기본구조
select 테이블.컬럼, 테이블.컬럼<br>
from 테이블1, 테이블2<br>
where 조건<br>

## Join문(연습문제)
### J-1) 급여가 3000이상인 사원번호, LAST_NAME, SALARY, 부서명, 도시명을 조회하시오.
![image](https://user-images.githubusercontent.com/126844692/228698054-74d577bb-8103-4153-beb5-0857a70ce54d.png)<br>

#### 결과
![image](https://user-images.githubusercontent.com/126844692/228699447-3994ad38-3d93-41de-85a0-ffe8ade81ce5.png)<br>

### J-2) 급여가 2500 이하이고 사원번호가 200이하인 사원의 LAST_NAME, 부서명을 조회하시오.
![image](https://user-images.githubusercontent.com/126844692/228698807-29f03b7d-53da-4078-a95e-0aa258ba144f.png)<br>

#### 결과
![image](https://user-images.githubusercontent.com/126844692/228699542-de2b2f69-ed10-4eeb-ac2e-cfc074667018.png)<br>

### J-3) 급여범위가 JOBS 테이블의 최소급여(MIN_SALARY)와 최대급여(MAX_SALARY) 사이에 있는 사원의 LAST_NAME, JOB_ID를 조회하시오.
![image](https://user-images.githubusercontent.com/126844692/228699304-6502884a-d77d-48cc-ab93-c1a00529738c.png)<br>

#### 결과
![image](https://user-images.githubusercontent.com/126844692/228699603-575a6e41-43e0-43be-9376-f813322ed76b.png)<br>

내부조인으로 만든것이며 내부조인은 기준 테이블과 조인 테이블 모두에 조인 컬럼 데이터가 존재해야 조회된다.(ON절)<br><br>

등가조인:조인 조건에 '='를 이용하는 조인<br>
비등가조인:부등호가 포함된 조인 조건<br>

### 예시
![image](https://user-images.githubusercontent.com/126844692/228698314-6c461117-3e7a-45f3-90ab-39036c268c0c.png)<br>
SELECT Sales.*, Countries.Country<br>
FROM Sales<br>
JOIN Countries<br>
ON Sales.CountryID = Countries.ID<br>

### J-4) 자신의 매니저보다 먼저 고용된 사원들의 LAST_NAME 및 고용일을 조회한다.
![image](https://user-images.githubusercontent.com/126844692/228699810-3722970f-3e8d-47ee-95b3-e1f3b618cec0.png)<br>

#### 결과
![image](https://user-images.githubusercontent.com/126844692/228699899-a37f4803-7fd0-4db4-a54d-8a52c7ae46b8.png)












# sql_Most_imp_basic_for_revision

# SUBQUERY
### subquery type => <br>
1-->   SCALAR <br>
2--> MULTI ROW MULTI COLUMN <br>
3--> CORRELATED <br>

## 1--> SCALAR =>> 
scalar subquery will return only 1row 1 col <br>
#### select name,(select avg(sal) from emp) from emp;
## 2--> MULTI ROW MULTI COL
this subquery will return more than 1 row and 1 col,means multiple row with multi column can be returnd <br>

## key POINT
in (where) we can use  "in()" for matching sub query with multiple row and col. <br>

### select * from emp where name in (select name from emp where name ='raju'); 
## 3--> correlated
it is a type of sub qurey which is related to its outer query <br>

##### lets find employess having more salary than avg salary of there department
### select * from employee e1 where sal> (select avg(sal) from employee e2 where e2.name=e1.name)
the subquery will depend on outer query and the outer query will return the whole record and inner query will match name with evrey record from the same department.


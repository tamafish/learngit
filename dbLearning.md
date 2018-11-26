# Data Base #
各种连接memo：
##1.内连接
左表右表皆做限制，仅显示满足on后面条件的数据

    select * from tb1 t1 inner join tb2 t2 on tb1.id=tb2.id;
    select * from tb1 t1 join tb2 t2 on tb1.id=tb2.id;
##2.外连接
###2.1左外连接
以左表为基础，结果是左表中的全部数据加上两表匹配后的数据。右表记录不足的地方全部为null

    select * from tb1 t1，tb2 t2 where tb1.id=tb2.id(+);
    
(+)可看做补充，哪个不足就写在哪边。
##3.oracle 系统查询
###3.1查找table由哪个procedure生成
    select distinct name from USER_SOURCE where type = 'PROCEDURE' 
    and text like '%pc_tb_index_target%'
###3.2查找系统中所有为‘ABC’的栏位
    select table_name from DBA_TAB_COLUMNS where COLUMN_NAME='ABC' 
  
 
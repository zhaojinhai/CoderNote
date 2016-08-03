SQLServer
=
## 1. Sql操作
### 1.  ` select * from sys.objects where type='U'`  
查询数据库里里所有的表.详见 <https://msdn.microsoft.com/en-us/library/ms190324.aspx>  
type:    
 - **P**   存储过程
 - **S** [System base table] 系统表
 - **U** 表
 - **V** 视图

### 2. ` select * from sys.columns where object_id=[object_id] `
查看表的字段,【object_id】是sys.objects 中对应的表名 **_id_**  
    例:`select * from sys.columns where object_id in (select object_id from sys.objects where name='CurGetData')`  
    详见<https://msdn.microsoft.com/en-us/library/ms176106.aspx>
### 3.  sys.systypes 
    数据库的类型定义 详见:<https://msdn.microsoft.com/en-us/library/ms188021.aspx>
### 4. sys.extended_properties
当前数据库的扩展属性  
详见:<https://msdn.microsoft.com/en-us/library/ms177541.aspx>



    


   




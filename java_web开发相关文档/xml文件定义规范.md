1. 同包同名

   mapper接口所在的包

   在resources下新建一个目录

   ```
   com/jiang/mapper
   ```

2. mybatis中文网约束

3. mapper标签namespace属性与mapper接口的全类名保持一致（做法复制类名路径）

   ```xml
   <mapper namespace="com.jiang.mapper.EmpMapper">
   ```

4. 标签id与接口方法名一致

   ```xml
   <delete id="delete">
   <select id="insert" resultType="com.jiang.pojo.Emp">//返回的是类的路径
   ```

   
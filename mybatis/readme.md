## 1 注解版，实体属性是数据库关键字的解决方案
###
    @Column(name = "`key`")
    private String key;
###
增加\`

## 2 做字段重复性验证时，配置字段为候选码即可，不必进行查询  
  问题 ：多条件或者复杂条件时无法做duplicate 字段验证
  还是安安稳稳去写单独的查询吧！
## 3 做事务处理 使用@Transactionals
  https://blog.csdn.net/nextyu/article/details/78669997

## 4 Mybatis动态语句
###
    // 已有Condition condition的情况，在统一接口追加参数
    condition.and()
        .andIsNull("deletedAt");
        
    SqlHelper 提供了很多sql语句模板
    
    符号<     >    需要转义 &lt;   &gt;
###

## 1 注解版，实体属性是数据库关键字的解决方案
###
    @Column(name = "`key`")
    private String key;
###
增加\`

## 2 做字段重复性验证时，配置字段为候选码即可，不必进行查询  

## 3 做事务处理 使用@Transactional
  https://blog.csdn.net/nextyu/article/details/78669997

  

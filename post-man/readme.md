### 1 发送请求默认 Content-Type 为  application/x-www-form-urlencoded
 ---   现代框架多为json，需要修改application/json
### 2 
```
@RequestBody这个一般处理的是在ajax请求中声明contentType: "application/json; charset=utf-8"时候。也就是json数据或者xml(我没用过这个，用的是json)

@RequestParam这个一般就是在ajax里面没有声明contentType的时候，为默认的。。。
```

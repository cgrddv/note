# spring-cloud
https://www.springcloud.cc/spring-cloud-dalston.html#spring-cloud-feign

pom.xml
```
<!-- 导入配置文件 -->
<properties resource="**.properties"/>

之后的属性可以使用 **.prepertie 定义的变量 如：
"${spring.datasource.driver-class-name}"
```
### swagger 404 问题
springboot 指定本地资源路径，使用静态资源导致。不支持加载动态如上传的资源，需要指定绝对路径。此时指定路径后swagger无法找到自己的metainfo下的资源。
在代码中增加资源路径
```
public class FileHandlerConfig implements WebMvcConfigurer {
    @Value("${file.uploadUrl}")
    private String staticResource;

    @Override
    public void addResourceHandlers(ResourceHandlerRegistry registry) {
        //配置server虚拟路径，handler为前台访问的目录，locations为files相对应的本地路径
        registry.addResourceHandler("/**").addResourceLocations(staticResource);
        registry.addResourceHandler("swagger-ui.html")
                .addResourceLocations("classpath:/META-INF/resources/");
        registry.addResourceHandler("/webjars/**")
                .addResourceLocations("classpath:/META-INF/resources/webjars/");
    }
}
```

# Spring Boot 中文文档：
http://oopsguy.com/documents/springboot-docs/1.5.4/index.html#boot-features
# Spring Boot 英文官方文档：
https://docs.spring.io/spring-boot/docs/1.5.2.RELEASE/reference/htmlsingle/
# mybatis plus的文档:
 https://mp.baomidou.com/guide/
# oracle jdk 各个版本的下载网址
 http://injdk.cn
# open jdk各个版本的下载网址
 https://openjdk.java.net/
# datafx学习 
http://www.guigarage.com/2014/05/datafx-8-0-tutorials/
https://blog.csdn.net/s_ghost/article/details/7406800
http://www.xntutor.com/javafx/javafx-stackpane-layout.html (javafx布局)

#廖雪峰博客

https://www.liaoxuefeng.com/wiki/1252599548343744/1306580844806178

        String XHTTPMETHOD = req.getHeader("X-HTTP-METHOD");
        String XHTTPMethodOverride=req.getHeader("X-HTTP-Method-Override");
        String XMETHODOVERRIDE= req.getHeader("X-METHOD-OVERRIDE");
        if (XHTTPMETHOD != null||XHTTPMethodOverride!=null||XMETHODOVERRIDE!=null) {
            resp.sendError(HttpServletResponse.SC_FORBIDDEN);
            return;
        }

        chain.doFilter(req, resp);
        
#maven
https://how2j.cn/k/maven/maven-introduction/1328.html?p=81777        

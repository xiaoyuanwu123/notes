# Spring Boot 中文文档：
http://oopsguy.com/documents/springboot-docs/1.5.4/index.html#boot-features
# Spring Boot 英文官方文档：
https://docs.spring.io/spring-boot/docs/1.5.2.RELEASE/reference/htmlsingle/
# @Transactional的使用:
 https://www.jianshu.com/p/befc2d73e487
# mybatis plus的文档:
 https://mp.baomidou.com/guide/
# vlc播放
 https://www.jianshu.com/p/2c61e3c6aa70
# javafx学习 
https://blog.csdn.net/abc_12366/article/details/79966055

https://blog.csdn.net/abc_12366/article/details/79968136

https://blog.csdn.net/abc_12366/article/details/79973198?utm_source=blogxgwz5

https://blog.csdn.net/abc_12366/article/details/79980211

https://blog.csdn.net/abc_12366/article/details/79982058
# datafx学习 
http://www.guigarage.com/2014/05/datafx-8-0-tutorials/
https://blog.csdn.net/s_ghost/article/details/7406800
http://www.xntutor.com/javafx/javafx-stackpane-layout.html (javafx布局)

#src->build.gradle

    compile 'org.kordamp.ikonli:ikonli-fontawesome5-pack:2.4.0'
    // https://mvnrepository.com/artifact/net.java.dev.jna/platform
    compile 'net.java.dev.jna:platform:3.5.2'
    // https://mvnrepository.com/artifact/net.java.dev.jna/jna
    compile 'net.java.dev.jna:jna:3.5.2'
    // https://mvnrepository.com/artifact/uk.co.caprica/vlcj
    compile 'uk.co.caprica:vlcj:3.8.0'
    // https://mvnrepository.com/artifact/org.slf4j/slf4j-log4j12
    testCompile 'org.slf4j:slf4j-log4j12:1.7.10'
    // https://mvnrepository.com/artifact/org.slf4j/slf4j-nop
    testCompile  'org.slf4j:slf4j-nop:1.7.24'
#media player不播放也不报错：

https://cloud.tencent.com/developer/ask/221715

#java调用sdl播放视频:

https://www.cnblogs.com/liuling/p/2013-12-20.html (java调用c)

https://www.cnblogs.com/gisblogs/p/5504124.html (以sdl为例说java动态加载)

https://www.cnblogs.com/jhlong/p/5433839.html (SDL简介)

https://blog.csdn.net/weixin_42462202/article/details/88370091 (使用SDL实现一个简单的YUV播放器)

http://www.libsdl.org/download-1.2.php (下载sdl)

https://blog.csdn.net/subfate/article/details/47832985 (yuv播放器)

https://blog.csdn.net/huachao1001/article/details/53906237 (IDEA平台下JNI编程（一）—HelloWorld篇)

https://blog.csdn.net/wsxzhbzl/article/details/82727034 (idea 2018 平台下JNI编程调用C++算法)

https://nuwen.net/mingw.html (下载MinGW)

<?xml version="1.0" encoding="UTF-8"?>

<?import javafx.scene.control.*?>
<?import java.lang.*?>
<?import javafx.scene.layout.*?>


<StackPane maxHeight="-Infinity" maxWidth="-Infinity" minHeight="-Infinity" minWidth="-Infinity" prefHeight="400.0" prefWidth="600.0" style="-fx-padding: 10;" xmlns="http://javafx.com/javafx/8" xmlns:fx="http://javafx.com/fxml/1">
   <children>
      <HBox opacity="0.95" prefHeight="100.0" prefWidth="200.0">
         <children>
            <ComboBox prefHeight="23.0" prefWidth="119.0" />
            <ComboBox prefHeight="23.0" prefWidth="118.0" />
            <Button depthTest="DISABLE" lineSpacing="10.0" mnemonicParsing="false" text="匹配测试" />
            <Button mnemonicParsing="false" text="设置" />
            <Button mnemonicParsing="false" text="求助" />
            <Button mnemonicParsing="false" text="提交" />
         </children>
      </HBox>
   </children>
</StackPane>


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

#BUILD.GRADLE
buildscript {
    repositories {
        maven { url 'https://artnj.zte.com.cn:443/artifactory/public-maven-virtual' }
        jcenter()
        mavenCentral()
    }
}

plugins {
    id 'com.jfrog.bintray' version '1.7.3' apply false
    id 'com.github.ben-manes.versions' version '0.15.0' apply false
    id 'me.tatarka.retrolambda' version '3.7.0' apply false
    id 'com.github.hierynomus.license' version '0.14.0' apply false
    id 'net.nemerosa.versioning' version '2.6.1' apply false
    id 'org.sonarqube' version '2.5'
}

subprojects {
    apply plugin: 'java'
    apply plugin: 'com.github.ben-manes.versions'
    apply plugin: 'net.nemerosa.versioning'


    repositories {
        maven { url 'https://artnj.zte.com.cn:443/artifactory/public-maven-virtual' }
        jcenter()
        mavenCentral()
        maven { url 'http://sevntu-checkstyle.github.com/sevntu.checkstyle/maven2' }
        maven { url 'http://maven.aliyun.com/nexus/content/repositories/google' }
        maven { url 'http://maven.aliyun.com/nexus/content/repositories/jcenter'}

    }

    if (JavaVersion.current().isJava8Compatible()) {
        tasks.withType(Javadoc) {
            options.addStringOption('Xdoclint:none', '-quiet')
        }
    }

    apply from: rootProject.file('gradle/code-coverage.gradle')
    apply from: rootProject.file('gradle/checkstyle.gradle')
    apply from: rootProject.file('gradle/findbugs.gradle')
    apply from: rootProject.file('gradle/javafx.gradle')

    sourceCompatibility = 1.8
    targetCompatibility = 1.8

    tasks.withType(JavaCompile) {
        options.incremental = true
    }
}
# setting.xml
<?xml version="1.0" encoding="UTF-8"?>
<settings>
  <!--offline>true</offline-->
  <localRepository>D:\maven\localRepository</localRepository>
	<mirrors>
		<mirror>
			<id>public</id>
			<mirrorOf>central</mirrorOf>
			<name>JFrog Artifactory</name>
			<url>https://artnj.zte.com.cn/artifactory/public-maven-virtual</url>
			<!-- https://artnj.zte.com.cn/artifactory/webapp/#/artifacts/browse/tree/General/public-maven-virtual -->
		</mirror>
		<mirror>
			<id>ipeg-alpha</id>
			<mirrorOf>*</mirrorOf>
			<name>zxge-ipeg</name>
			<url>https://artnj.zte.com.cn/artifactory/ipeg-alpha-maven</url>
			<!-- https://artnj.zte.com.cn/artifactory/webapp/#/artifacts/browse/tree/General/public-maven-virtual -->
		</mirror> 		
	</mirrors>
	<pluginGroups>
		<pluginGroup>com.zte.ums.maven.plugins</pluginGroup>
		<pluginGroup>org.mortbay.jetty</pluginGroup>
		<pluginGroup>org.codehaus.cargo</pluginGroup>
	</pluginGroups>
	<profiles>
		<profile>
			<id>env-settings</id>
			<activation>
				<property>
					<name>env</name>
				</property>
			</activation>
			<repositories>
				<repository>
					<id>ipeg-alpha</id>
					<url>https://artnj.zte.com.cn/artifactory/ipeg-alpha-maven</url>
					<releases>
						<enabled>true</enabled>
					</releases>
					<snapshots>
						<enabled>false</enabled>
					</snapshots>
				</repository>
				<repository>
					<id>public</id>
					<url>https://artnj.zte.com.cn/artifactory/public-maven-virtual</url>
					<releases>
						<enabled>false</enabled>
					</releases>
					<snapshots>
						<enabled>true</enabled>
					</snapshots>
				</repository>
			</repositories>
			<pluginRepositories>
				<pluginRepository>
					<id>ipeg-alpha</id>
					<url>https://artnj.zte.com.cn/artifactory/ipeg-alpha-maven</url>
					<releases>
						<enabled>true</enabled>
					</releases>
					<snapshots>
						<enabled>false</enabled>
					</snapshots>
				</pluginRepository>
				<pluginRepository>
					<id>public</id>
					<url>https://artnj.zte.com.cn/artifactory/public-maven-virtual</url>
					<releases>
						<enabled>false</enabled>
					</releases>
					<snapshots>
						<enabled>true</enabled>
					</snapshots>
				</pluginRepository>
			</pluginRepositories>
			<properties>
				<!-- ******************************************************************************************************************* -->
				<!-- ===== 下面的属性在新建一个管理区域范围内的构建系统环境时需要进行定制 ===== -->
				<!-- repos 站点IP -->
				<netnumen.project.repos.ip>artnj.zte.com.cn</netnumen.project.repos.ip>
				<!-- 组件发布版本站点 IP 地址 -->
				<netnumen.project.release.repos.ip>artnj.zte.com.cn</netnumen.project.release.repos.ip>
				<!-- 组件每日构建版本站点 IP 地址 -->
				<netnumen.project.snapshot.repos.ip>artnj.zte.com.cn</netnumen.project.snapshot.repos.ip>
				<!-- 组件项目信息发布站点 IP 地址 -->
				<netnumen.project.site.ip>10.41.103.97</netnumen.project.site.ip>
				<netnumen.project.svn.ip>10.41.103.97</netnumen.project.svn.ip>
				<!-- ******************************************************************************************************************* -->
				<!-- ==== 下面属性，根据个人开发环境可进行定制。
                          需要新建一个 settings.xml 文件放置到 ${SystemDrive}/.m2/ 目录，
                          此文件中重新定义下面的属性值。 -->
				<!-- 系统构建组装根路径，.win WINDOWS 环境下默认路径；.unix UNIX 环境下默认路径 -->
				<netnumen.project.assoutdir.win>${env.HOMEDRIVE}/netnumen/${netnumen.project.id}${project.version}</netnumen.project.assoutdir.win>
				<netnumen.project.assoutdir.unix>~/netnumen/${netnumen.project.id}${project.version}</netnumen.project.assoutdir.unix>
				<uep.project.assembly.outputdir>d:/product_tmp</uep.project.assembly.outputdir>
				<uep-version>${project.version}</uep-version>
			</properties>
		</profile>
		<profile>
			<!-- windows 环境预定义 -->
			<id>env-windows</id>
			<activation>
				<os>
					<family>windows</family>
				</os>
			</activation>
			<properties>
				<!-- 区域变量，系统装配后的输出目录 -->
				<netnumen.project.assout.path>${netnumen.project.assoutdir.win}</netnumen.project.assout.path>
			</properties>
		</profile>
		<profile>
			<!-- unix 环境预定义 -->
			<id>env-unix</id>
			<activation>
				<os>
					<family>unix</family>
				</os>
			</activation>
			<properties>
				<!-- assoutdir 系统装配后的输出目录 -->
				<netnumen.project.assout.path>${netnumen.project.assoutdir.unix}</netnumen.project.assout.path>
			</properties>
		</profile>
	</profiles>
	<activeProfiles>
		<activeProfile>env-settings</activeProfile>
		<activeProfile>env-common</activeProfile>
		<!--activeProfile>env-app</activeProfile-->
	</activeProfiles>
	<servers>
		<server>
			<id>ipeg-alpha</id>
			<username>zxge_ipeg-ci</username>
			<password>IPEG_dap1234$</password>
		</server><server>
			<id>public</id>
			<username>zxge_ipeg-ci</username>
			<password>IPEG_dap1234$</password>
		</server>
	</servers>
</settings>


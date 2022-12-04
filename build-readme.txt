源码构建过程：
1.下载 gradle-bin安装包， https://services.gradle.org/distributions/
2.配置环境
 - GRADLE_HOME，path中增加%GRADLE_HOME%/bin
 - GRADLE_USER_HOME，路径配置成需要的本地仓库路径即可
3.配置
 - $project/gradle/warpper/gradle-wrapper.properties    distributionUrl=file\:///D\:/app/gradle-5.6.4-bin.zip
 - $project/build.gradle	repositories
   		maven{ url 'https://maven.aliyun.com/nexus/content/groups/public/'}
		maven{ url 'https://maven.aliyun.com/nexus/content/repositories/jcenter'}
			
4.在spring目录执行 .\gradlew :spring-oxm:compileTestJava（执行失败多执行几遍）
5.导入idea工程: 
 - 配置Use local gradle distribution（使用本地gradle编译）
 - 配置Gradle home： 环境变量配置的home地址
 - 配置Service directory path：gradle的本地仓库

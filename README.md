[![Build Status](https://travis-ci.org/Wechat-Group/weixin-java-mp-demo.svg?branch=master)](https://travis-ci.org/Wechat-Group/weixin-java-mp-demo)

### 本项目为weixin-java-tools的Demo演示程序，更多Demo请查阅：https://github.com/Wechat-Group/weixin-java-tools
## 包括三个demo

# Spring MVC Demo

#### 本Demo使用Spring MVC 框架实现微信公众号开发功能，欢迎帮忙维护添加新功能，或提供更好的实现。

## 使用步骤：
1. 配置: 复制/src/main/resources/wx.properties.template 生成 wx.properties 文件，填写相关配置;		
1. 使用maven运行demo程序: `mvn jetty:run`  或者自己打war包发布到tomcat运行；
1. 配置微信公众号中的接口地址：http://xxx/wechat/portal （注意XXX需要是外网可访问的域名，需要符合微信官方的要求）；
1. 根据自己需要修改各个handler的实现，加入自己的业务逻辑。
	 
	
# Spring Boot Demo
### 本Demo基于Spring Boot构建，实现微信公众号开发功能。
-----------------------

## 使用步骤：
1. 配置：复制`/src/main/resources/application.yml.template` 生成application.yml文件，根据自己需要填写相关配置（需要注意的是：yml文件内的属性冒号后面的文字之前需要加空格，可参考已有配置，否则属性会设置不成功）；	
1. 运行Java程序：`com.github.binarywang.demo.wechat.WxMpDemoApplication`；
1. 打开shell或cmd，进入ngrok目录，运行 `ngrok -config ngrok.cfg -subdomain my-domain 8080` 如果运行失败，请更换my-domain为其它字符串，直至连接成功；
1. 配置微信公众号中的接口地址：http://my-domain.tunnel.qydev.com/wechat/portal （注意my-domain要跟上面的一致，需要符合微信官方的要求）；
1. 根据自己需要修改各个handler的实现，加入自己的业务逻辑。
	
# Spring MVC 多公众号支持 Demo
 
#### 本Demo使用Spring MVC 框架实现微信公众号开发功能，支持多公众号，欢迎帮忙维护添加新功能，或提供更好的实现。
1. 如果想使用更多公众号，请复制相关配置文件，修改spring配置文件添加相应配置，同时还需要增加相应的controller和service，具体可以参考已有源码进行操作。
1. 如果只是使用一个公众号，建议使用另外的项目：
https://github.com/wechat-group/weixin-java-mp-demo 或者 https://github.com/wechat-group/weixin-java-mp-demo-springboot 。

## 使用步骤：
1. 配置:
	1. 复制/src/main/resources/wx-gzh1.properties.template 生成wx-gzh1.properties 文件，填写相关配置;
	2. 复制/src/main/resources/wx-gzh2.properties.template 生成wx-gzh2.properties 文件，填写相关配置。		
1. 使用maven运行demo程序: `mvn jetty:run`  或者自己打 war包发布到tomcat运行；
1. 配置微信公众号中的接口地址：http://xxx/api/gzh1/portal 或 http://xxx/api/gzh2/portal （注意XXX需要是外网可访问的域名，需要符合微信官方的要求）
1. 根据自己需要修改各个handler的实现，加入自己的业务逻辑
	
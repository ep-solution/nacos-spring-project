
如何同步标签到 Fork 仓库？
方法 1：通过命令行手动同步
添加原仓库为远程仓库

git remote add upstream <原仓库的URL>
（例如：git remote add upstream https://github.com/original/repo.git）

从原仓库拉取所有标签

git fetch upstream --tags
将标签推送到你的 Fork 仓库

git push origin --tags


20250418
解决nacos-spring-context鱼snakeyaml2.x的冲突
java.lang.NoSuchMethodError: org.yaml.snakeyaml.constructor.Constructor: method <init>()V not found
	at com.alibaba.nacos.spring.util.parse.DefaultYamlConfigParse$MapAppenderConstructor.<init>(DefaultYamlConfigParse.java:180) ~[nsf-agent-springboot2-0.jar:na]
	at com.alibaba.nacos.spring.util.parse.DefaultYamlConfigParse.createYaml(DefaultYamlConfigParse.java:51) ~[nsf-agent-springboot2-0.jar:na]
	at com.alibaba.nacos.spring.util.parse.DefaultYamlConfigParse.parse(DefaultYamlConfigParse.java:158) ~[nsf-agent-springboot2-0.jar:na]
	at com.alibaba.nacos.spring.util.ConfigParseUtils.toProperties(ConfigParseUtils.java:95) ~[nsf-agent-springboot2-0.jar:na]
	at com.alibaba.nacos.spring.util.ConfigParseUtils.toProperties(ConfigParseUtils.java:115) ~[nsf-agent-springboot2-0.jar:na]
	at com.alibaba.nacos.spring.util.NacosUtils.toProperties(NacosUtils.java:542) ~[nsf-agent-springboot2-0.jar:na]
	at com.alibaba.nacos.spring.core.env.NacosPropertySource.<init>(NacosPropertySource.java:62) ~[nsf-agent-springboot2-0.jar:na]
	at com.alibaba.nacos.spring.core.env.AbstractNacosPropertySourceBuilder.doBuild(AbstractNacosPropertySourceBuilder.java:198) ~[nsf-agent-springboot2-0.jar:na]
	at com.alibaba.nacos.spring.core.env.AbstractNacosPropertySourceBuilder.build(AbstractNacosPropertySourceBuilder.java:114) ~[nsf-agent-springboot2-0.jar:na]
	at com.alibaba.nacos.spring.core.env.NacosPropertySourcePostProcessor.buildNacosPropertySources(NacosPropertySourcePostProcessor.java:201) ~[nsf-agent-springboot2-0.jar:na]
	at com.alibaba.nacos.spring.core.env.NacosPropertySourcePostProcessor.processPropertySource(NacosPropertySourcePostProcessor.java:183) ~[nsf-agent-springboot2-0.jar:na]
	at com.alibaba.nacos.spring.core.env.NacosPropertySourcePostProcessor.postProcessBeanFactory(NacosPropertySourcePostProcessor.java:168) ~[nsf-agent-springboot2-0.jar:na]
	at com.alibaba.nacos.spring.util.NacosBeanUtils.invokeNacosPropertySourcePostProcessor(NacosBeanUtils.java:416) ~[nsf-agent-springboot2-0.jar:na]
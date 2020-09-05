
入门Dubbo的简单Demo

Dubbo之我的理解
1、Dubbo可以使用zookeeper作为注册中心，Dubbo服务需要注册到zookeeper
2、Dobbo-admin是用于运维的，因此不启动该项目也能正确运行
3、服务提供者需要启动Provider容器，在启动类上使用Main.main(args)，注意这里的 Main 是 com.alibaba.dubbo.container 包下的
4、服务熔断可以使用Hystrix，但是每个方法都加上Hystrix注解，并需要提供一个fallback方法
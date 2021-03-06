## 访问服务中心  
系统通过服务中心实现服务之间的发现。服务启动过程中，会向服务中心进行注册。在调用其他服务的时候，会从服务中心查询其他服务的实例信息，比如访问地址、使用的协议以及其他参数。服务中心支持使用PULL和PUSH两种模式通知实例变化。


## 应用性能监控
 一、Metrics介绍  
 二、统计项汇总  
 三、使用方法  


## 微服务调用链  
微服务架构解决了很多单体应用带来的问题，但同时也需要我们付出额外的代价。由于网络的不稳定性带来的请求处理延迟就是代价之一。  

在单体应用中，所有模块都在同一个进程中运行，所以并没有模块间互通的问题。但微服务架构中，服务间通过网络沟通，因此我们不得不处理和网络有关的 问题，例如：延迟、超时、网络分区等。  

另外，随着业务的扩展服务增多，我们很难洞察数据如何在蛛网般复杂的服务结构中流转。我们如何才能有效的监控网络延迟并且可视化服务中的数据流转呢？  

分布式调用链追踪用于有效地监控微服务的网络延时并可视化微服务中的数据流转。  

## 自定义调用链打点
分布式调用链追踪提供了服务间调用的时序信息，但服务内部的链路调用信息对开发者同样重要，如果能将两者合二为一，就能提供更完整的调用链，更容易定位错误和潜在性能问题。

## 本地开发和测试  
本小节介绍如何在开发者本地进行消费者/提供者应用的开发调试。开发服务提供者请参考3 开发服务提供者章节，开发服务消费者请参考4 开发服务消费者。服务提供者和消费提供者均需要连接到在远程的服务中心，为了本地微服务的开发和调试，本小节介绍了两种搭建本地服务中心的方法进行本地微服务调试：  


## Http Filter
某些场景中，业务使用http而不是https，作为网络传输通道，此时为了防止被伪造或篡改请求，需要提供consumer、producer之间对http码流的签名功能。


## 文件上传  
文件上传，当前支持在vertx rest通道和servlet rest中使用。  
文件上传使用标准的http form格式，可与浏览器的上传直接对接。  

## 文件下载  
文件下载，当前在vertx rest通道和servlet rest中可用。


## Reactive
简单同步模式、嵌套同步调用、纯Reactive机制、混合Reactive机制之间的对比及说明。


## DNS自定义配置
用户使用域名连接华为公有云或者三方系统时，需要使用到域名解析系统。在不同的系统、不同的框架使用的域名解析机制都可能不太一样。所以我们有必要提供一个统一的配置入口，以便开发运维人员可以自定义DNS解析机制，而不完全受制于系统配置。  

## 代理设置
作为一名开发者，在公司开发环境，可能是通过公司代理网络接入到因特网。如果调试服务时还必须依赖网上资源，比如直接连接华为共有云服务中心，那么就必须配置代理。


## 框架上报版本号
为方便治理，使用ServiceComb进行开发，会将当前使用的ServiceComb版本号上报至服务中心，并且支持其他框架集成ServiceComb时上报其他框架的版本号。

## 跨应用调用
应用是微服务实例隔离层次中的一层，一个应用包含多个微服务。默认情况下，只允许同应用的微服务实例相互调用。


## 定制序列化和反序列化方法
由于HTTP协议的非安全性，在网络中传输的数据能轻易被各种抓包工具监听。在实际应用中，业务对应用或服务间传输的敏感数据有较高的安全要求，这类数据需要特别的加密保护（业务不同对算法要求不同），这样即使内容被截获，也可以保护其中的敏感数据不被轻易获取。


## 使用Context传递控制消息
ServiceComb提供了Context在微服务之间传递数据。Context是key/value对，只能够使用String类型的数据。由于Context会序列化为json格式并通过HTTP Header传递，因此也不支持ASCII之外的字符，其他字符需要开发者先自行编码再传递。Context在一次请求中，会在请求链上传递，不需要重新设置。access log的trace id等功能都基于这个特性实现的。


## 返回值序列化扩展
当前REST通道返回值支持application/json和text/plain两种格式，支持开发人员扩展和重写，服务提供者通过produces声明可提供序列化能力，服务消费者通过请求的Accept头指明返回值序列化方式，默认返回application/json格式的数据。


## CORS机制
跨域资源共享(CORS, Cross-Origin Resource Sharing)允许Web服务器进行跨域访问控制，使浏览器可以更安全地进行跨域数据传输。


## 获取熔断与实例隔离告警事件信息
在微服务运行期间熔断或实例隔离状态发生变化时，需要监听到相关事件，获取相关信息并进行处理

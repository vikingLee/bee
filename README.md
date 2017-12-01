* 环境配置：在被测环境的hosts里加  127.0.0.1   localhost

* 简介
Bee是基于对elenide和Selenium原生接口进行的二次封装，旨在简化接口，方便使用。Bee支持Web和Wap页面的元素操作，其中Selenide用来支持Web页面，Selenium用来支持Wap页面。以下从四个方面作简要阐述。

组织结构：driver层二次封装Selenide和Selenium的接口，是操作页面元素的核心；
         pageObject层用于封装业务流程中需要使用的每一个页面元素，是业务流程实现的核心；
         dataprovider层自定义测试数据，实现测试数据的隔离；
         service层用于定义各模块之间的公共业务流程，实现模块间业务的调用。
用例组织：从账户登入到一个业务流程结束作为一个完整的UI自动化用例。用例由每一个pageObject接口的调用来实现业务流程。所有测试用例使用testng进行管理。
报告展示：使用reportng收集测试数据，可结合jenkins插件呈现测试报告。
环境支持：当前版本只支持MAC环境的chrome浏览器，支持扩展
功能描述：Bee接口解决了方法调用过程中元素加载、页面加载等常见问题
         Bee在框架层实现失败用例重试，提高用例结果的可靠性
         
* 版本


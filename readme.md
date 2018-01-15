## Welcome to HugeGraph

### Summary

HugeGraph是一款图数据库（Graph Database）系统，可以存储海量的顶点（Vertex）和边（Edge），
实现了[Apache TinkerPop 3](https://tinkerpop.apache.org)框架，
支持[Gremlin](https://tinkerpop.apache.org/gremlin.html)查询语言。
HugeGraph可以支持多用户并行操作操作，用户可以输入Gremlin查询语句，并及时得到Graph查询结果。

本系统首先要解决百度安全事业部金融反欺诈、威胁情报、黑产打击等核心业务的关联数据存储和建模分析需求，
在此基础上形成成熟的商业化解决方案支持外部客户。

随着系统逐步成熟稳定，HugeGraph最终可以以开源的方式捐赠给开源基金会，填补国内图数据库市场空白。

### Features  

HugeGraph是一款离线环境下，面向分析型，支持批量操作的图数据库系统，它能够与大数据平台无缝集成。本系统具备如下特点：  

* 基于Tinker Pop 3 API实现，支持Gremlin图查询语言 
 
* 具备单独的meta元数据信息，方便第三方系统集成  

* 支持用户自定义边和顶点ID  

* 可以在边和顶点建立索引，支持精确查询、范围查询和模糊查询  

* 具备可视化操作界面，降低用户使用门槛  

* 存储系统采用插件方式，支持HBase、Cassandra、ScyllaDB等多种后端  

* 与Hadoop、Spark等大数据系统集成，支持Bulk Load操作  

### Modules

- [HugeGraph-Server](./quickstart/hugeserver.md): HugeGraph-Server是HugeGraph项目的核心部分，包含Core、Backend、API等子模块；
  
  - Core：是Tinkerpop接口的实现，元数据管理，事务处理，序列化/反序列化，向下连接Backend模块，向上连接API模块；
  
  - Backend：实现将图数据存储到后端，支持的后端包括：Memory、Cassandra、ScyllaDB以及RocksDB（0.4版本支持），用户根据实际情况选择一种即可；
  
  - API：内置Rest-Server，向用户提供Restful API，同时可兼容gremlin查询，将客户端的HTTP请求转化为对Core代码的调用。

- [HugeGraph-Client](./quickstart/hugeclient.md)：HugeGraph-Client提供了RestAPI的客户端，用于连接HugeGraph-Server，目前仅实现Java版，其他语言用户可自行实现；

- [HugeGraph-Loader](./quickstart/hugeloader.md)：HugeGraph-Loader是基于HugeGraph-Client的数据导入工具，将普通文本数据转化为图形的顶点和边并插入图形数据库中；

- [HugeGraph-Spark](./quickstart/hugespark.md)：HugeGraph-Spark能在图上做并行计算，例如PageRank算法等；

- [HugeGraph-Studio](./quickstart/hugestudio.md)：HugeStudio是HugeGraph的Web可视化工具，可用于执行gremlin语句及展示图。

### Contact Us

* 负责人：[刘杰](mailto:liujie23@baidu.com), [季石磊](mailto:jishilei@baidu.com)

* 接口人：[李章梅](mailto:lizhangmei@baidu.com)，张义[邮箱](mailto:zhangyi51@baidu.com)|[Hi](baidu://message/?id=zhangyi89817)，[李凝瑞](liningrui@baidu.com)

* 反馈邮箱：[hugegraph@baidu.com](mailto:hugegraph@baidu.com)
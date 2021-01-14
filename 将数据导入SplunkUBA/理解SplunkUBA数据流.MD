# 理解Splunk UBA中的数据流

Splunk UBA的整个数据流向如下图所示：
![图示](https://docs.splunk.com/images/thumb/4/4f/UBA_Data_Flow_v5.png/1050px-UBA_Data_Flow_v5.png)

|步骤|过程|描述|
|----|----|----|
|1|来自splunk平台的生数据和已解析的数据|splunk UBA可以提取解析符合[CIM(Common Information Model)](https://docs.splunk.com/Documentation/Splunk/8.1.1/Knowledge/UnderstandandusetheCommonInformationModel)的数据或生数据。你必须选择合适的连接器(connector)类型。使用**Splunk Direct**连接器在splunk上面解析数据之后再进入Splunk UBA。使用**Splunk Raw Events**连接器使用Splunk UBA本地的解析器来解析数据。 |
|2|账户规范化和身份解析|Splunk UBA分析来自Splunk的数据，并将数据中的字段映射到UBA中的特定字段，正确映射的数据字段可以使Splunk UBA能够执行如下操作：1、规范化设备和域名，并将其HR数据中标识的所有帐户与单个人工账户相关联。2、执行身份解析以查找IP地址，主机名和用户之间的实时关联，并随着时间的推移保持这些关联|

### mybatis-generator-demo

spring boot 整合 mybatis generator，实现自动生成 domain、dao、mapping 等文件。

### 使用指南

将本项目下载到本地，解压，导入到eclipse中，修改`application.properties`的内容为自己的相关内容，再在`generatorConfig.xml`修改44行的`tableName`为自己数据库的表名，`domainObjectName`改为自己想要的实体类名，49行的`column`的值改为对应表的主键名即可。如果有多张表，则每张表都要对应一段44行到50行的代码，依然需要改动`tableName`、`domainObjectName`、`column`。也可以使用通配符`%`匹配，将`tableName`的值改为`%`，去掉`domainObjectName`属性，删掉49行，即可生成所有的表，但是文件的名字需要在生成后自己改为想要的。

> **注意**：此项目只在MySQL上测过，Oracle的请自己另找资料。

**运行方式**：选中项目-->右键-->`run as`-->`maven bulid...`-->弹出对话框-->在`goals`中输入`mybatis-generator:generate`-->`run`即可。

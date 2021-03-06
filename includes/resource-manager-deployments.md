## 增量部署和完整部署

默认情况下，资源管理器会将部署视为对资源组的增量更新。进行增量部署时，资源管理器将会：

- 使资源组中存在的、但未在模板中指定的资源**保留不变**
- **添加**模板中指定的、但不在资源组中的资源
- **不会重新预配**资源组中存在的、与模板中定义的条件相同的资源
- **重新预配**已更新模板设置的现有资源

进行完整部署时，资源管理器将会：

- **删除**资源组中存在的、但未在模板中指定的资源
- **添加**模板中指定的、但不在资源组中的资源
- **不会重新预配**资源组中存在的、与模板中定义的条件相同的资源
- **重新预配**已更新模板设置的现有资源
 
可以通过 **Mode** 属性指定部署的类型。

<!---HONumber=Mooncake_0725_2016-->
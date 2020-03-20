# 业务面API使用限制<a name="ges_03_0139"></a>

用户访问业务面API有三种方式：

-   通过ECS访问，且创建ECS的VPC和创建图选定的VPC是同一个。如果安全组选择的是同一个，则可以直接访问；如果安全组不是同一个，要在创建图的安全组开通该ECS的访问限制，即放开80和443端口（分别对应支持HTTP和HTTPS访问）。这种场景，API的SERVER\_URL为GES Console图详情的内网访问地址或者管理面API查询图详情返回体的"privateIp"字段的值。
-   通过ECS访问，但创建ECS的VPC和创建图选定的VPC不是同一个。需要对ECS所在的VPC和建图用的VPC创建VPC对等连接，创建VPC对等连接请参考[创建对等连接](https://support.huaweicloud.com/api-vpc/vpc_peering_0003.html)。同时要在创建图的安全组开通该ECS的访问限制，即放开80和443端口。这种场景，API的SERVER\_URL为GES Console图详情的内网访问地址或者管理面API查询图详情返回体的"privateIp"字段的值。
-   通过公网访问。此时要求创建弹性公网IP（EIP），且要在创建图的安全组开通客户端的访问限制，即放开80和443端口。这种场景，API的SERVER\_URL为GES Console图详情的公网访问地址或者管理面API查询图详情返回体的"publicIp"字段的值，也即用户绑定或者自动创建的弹性公网IP地址。


# 管理面API错误码<a name="ges_03_0040"></a>

调用接口出错后，将不会返回结果数据。调用方可根据每个接口对应的错误码来定位错误原因。当调用出错时，HTTP 请求返回一个 4xx 或 5xx 的 HTTP 状态码。返回的消息体中是具体的错误代码及错误信息。在调用方找不到错误原因时，可以联系企业技术人员，并提供错误码，以便我们尽快帮您解决问题。

当您调用API时，如果遇到“APIGW”开头的错误码，请参见[API网关错误码](https://support.huaweicloud.com/devg-apisign/api-sign-errorcode.html)进行处理。

**表 1**  错误码

<a name="table13150194944219"></a>
<table><thead align="left"><tr id="row1515018490427"><th class="cellrowborder" valign="top" width="10.36103610361036%" id="mcps1.2.5.1.1"><p id="p215064994216"><a name="p215064994216"></a><a name="p215064994216"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="15.721572157215721%" id="mcps1.2.5.1.2"><p id="p12150749164219"><a name="p12150749164219"></a><a name="p12150749164219"></a>错误码</p>
</th>
<th class="cellrowborder" valign="top" width="22.472247224722473%" id="mcps1.2.5.1.3"><p id="p151501049144216"><a name="p151501049144216"></a><a name="p151501049144216"></a>错误信息</p>
</th>
<th class="cellrowborder" valign="top" width="51.44514451445145%" id="mcps1.2.5.1.4"><p id="p1715010494422"><a name="p1715010494422"></a><a name="p1715010494422"></a>处理措施</p>
</th>
</tr>
</thead>
<tbody><tr id="row16150144924212"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p9899922144317"><a name="p9899922144317"></a><a name="p9899922144317"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p7899102218438"><a name="p7899102218438"></a><a name="p7899102218438"></a>GES.0001</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p12899822164320"><a name="p12899822164320"></a><a name="p12899822164320"></a>参数错误</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><a name="ol440911188910"></a><a name="ol440911188910"></a><ol id="ol440911188910"><li>检查URL中的ProjectID或者GraphID是否正确</li><li>检查请求头是否正确，比如X-Auth-Token是否正确</li></ol>
</td>
</tr>
<tr id="row4150134910425"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p2150124916420"><a name="p2150124916420"></a><a name="p2150124916420"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p215094964217"><a name="p215094964217"></a><a name="p215094964217"></a>GES.7000</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p14150134912428"><a name="p14150134912428"></a><a name="p14150134912428"></a>图不存在或者已被删除</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><a name="ol153144281292"></a><a name="ol153144281292"></a><ol id="ol153144281292"><li>调用图查询接口，查询所有的图</li><li>检查URL中的ProjectID或者GraphID是否正确</li></ol>
</td>
</tr>
<tr id="row15150174974219"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p2015018496424"><a name="p2015018496424"></a><a name="p2015018496424"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p1215134924217"><a name="p1215134924217"></a><a name="p1215134924217"></a>GES.7001</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p12151174984217"><a name="p12151174984217"></a><a name="p12151174984217"></a>图不在运行状态</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><a name="ol1874117370914"></a><a name="ol1874117370914"></a><ol id="ol1874117370914"><li>调用图查询接口，查询所有的图</li><li>查询上述返回图列表，检查URL中的GraphID对应的图状态是否为200</li></ol>
</td>
</tr>
<tr id="row11151164974212"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p815184914425"><a name="p815184914425"></a><a name="p815184914425"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p1015134924220"><a name="p1015134924220"></a><a name="p1015134924220"></a>GES.7002</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p12151204974220"><a name="p12151204974220"></a><a name="p12151204974220"></a>图正在备份</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><a name="ol729164515917"></a><a name="ol729164515917"></a><ol id="ol729164515917"><li>调用图查询接口，查询所有的图</li><li>查询上述返回图列表，检查URL中的GraphID对应的图状态是否为903</li></ol>
</td>
</tr>
<tr id="row124214141212"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p14581451214"><a name="p14581451214"></a><a name="p14581451214"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p13691431218"><a name="p13691431218"></a><a name="p13691431218"></a>GES.7003</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p8621411217"><a name="p8621411217"></a><a name="p8621411217"></a>图正在停止或者处于停止状态</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><a name="ol060618541592"></a><a name="ol060618541592"></a><ol id="ol060618541592"><li>调用图查询接口，查询所有的图</li><li>查询上述返回图列表，检查URL中的GraphID对应的图状态是否为900或者901</li></ol>
</td>
</tr>
<tr id="row47310343137"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p18731193471316"><a name="p18731193471316"></a><a name="p18731193471316"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p1673243411313"><a name="p1673243411313"></a><a name="p1673243411313"></a>GES.7004</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p18732434111312"><a name="p18732434111312"></a><a name="p18732434111312"></a>IAAS层组件故障</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p159091320151413"><a name="p159091320151413"></a><a name="p159091320151413"></a>查看IAM、VPC、ECS、OBS等IAAS层组件是否有故障</p>
</td>
</tr>
<tr id="row6509358151413"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p13509158201415"><a name="p13509158201415"></a><a name="p13509158201415"></a>408</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p750965816146"><a name="p750965816146"></a><a name="p750965816146"></a>GES.7005</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p85101058161412"><a name="p85101058161412"></a><a name="p85101058161412"></a>图引擎底层服务不可用</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p6510175817143"><a name="p6510175817143"></a><a name="p6510175817143"></a>请稍后重试或者企业技术人员</p>
</td>
</tr>
<tr id="row477422251919"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p14774922201920"><a name="p14774922201920"></a><a name="p14774922201920"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p19774172221915"><a name="p19774172221915"></a><a name="p19774172221915"></a>GES.7006</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p47741022121914"><a name="p47741022121914"></a><a name="p47741022121914"></a>图引擎底层服务内部错误</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p2774622161916"><a name="p2774622161916"></a><a name="p2774622161916"></a>请稍后重试或者企业技术人员</p>
</td>
</tr>
<tr id="row84163474207"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p641714712019"><a name="p641714712019"></a><a name="p641714712019"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p19417647112017"><a name="p19417647112017"></a><a name="p19417647112017"></a>GES.7007</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p14417114716203"><a name="p14417114716203"></a><a name="p14417114716203"></a>Job不存在</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p1241716474202"><a name="p1241716474202"></a><a name="p1241716474202"></a>检查URL中的JobID是否正确</p>
</td>
</tr>
<tr id="row14891715143319"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p2048951543317"><a name="p2048951543317"></a><a name="p2048951543317"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p19489101514337"><a name="p19489101514337"></a><a name="p19489101514337"></a>GES.7008</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p1748991516339"><a name="p1748991516339"></a><a name="p1748991516339"></a>Job已停止</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p449021593311"><a name="p449021593311"></a><a name="p449021593311"></a>Job不能重复执行停止操作</p>
</td>
</tr>
<tr id="row1270415180346"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p17704111818344"><a name="p17704111818344"></a><a name="p17704111818344"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p1704518133416"><a name="p1704518133416"></a><a name="p1704518133416"></a>GES.7009</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p1670411810347"><a name="p1670411810347"></a><a name="p1670411810347"></a>Job操作不支持</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p15705131820344"><a name="p15705131820344"></a><a name="p15705131820344"></a>Job操作不支持</p>
</td>
</tr>
<tr id="row45644443350"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p14564134419354"><a name="p14564134419354"></a><a name="p14564134419354"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p18564154410350"><a name="p18564154410350"></a><a name="p18564154410350"></a>GES.7010</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p356494473520"><a name="p356494473520"></a><a name="p356494473520"></a>图模式文件和数据校文件验失败</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p956414417352"><a name="p956414417352"></a><a name="p956414417352"></a>请检查图模式文件和边、点数据集文件是否匹配</p>
</td>
</tr>
<tr id="row62837309365"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p4283930123610"><a name="p4283930123610"></a><a name="p4283930123610"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p92833308360"><a name="p92833308360"></a><a name="p92833308360"></a>GES.7011</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p1828353011361"><a name="p1828353011361"></a><a name="p1828353011361"></a>图模式文件或数据文件路径或者名字不合法</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p17283123016368"><a name="p17283123016368"></a><a name="p17283123016368"></a>请检查图模式文件、点数据集文件、边数据集文件名称是否合法，只能由英文字母、数字、下划线、感叹号、中划线、点号、星号、左括号、右符号、斜线组成</p>
</td>
</tr>
<tr id="row13172614375"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p1831526203710"><a name="p1831526203710"></a><a name="p1831526203710"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p831126103716"><a name="p831126103716"></a><a name="p831126103716"></a>GES.7012</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p193182616372"><a name="p193182616372"></a><a name="p193182616372"></a>图名称校验失败</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p163162611374"><a name="p163162611374"></a><a name="p163162611374"></a>请检查图名称，只能以字母开头，由英文字母、数字、下划线组成，且长度位于4~64之间</p>
</td>
</tr>
<tr id="row14161106163820"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p1616176163818"><a name="p1616176163818"></a><a name="p1616176163818"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p11161166143818"><a name="p11161166143818"></a><a name="p11161166143818"></a>GES.7013</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p10161116173819"><a name="p10161116173819"></a><a name="p10161116173819"></a>图名称已存在</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><a name="ol1461369171012"></a><a name="ol1461369171012"></a><ol id="ol1461369171012"><li>调用图查询接口，查询所有的图</li><li>查询上述返回图列表，检查请求体里面的name字段的值是否已经存在</li></ol>
</td>
</tr>
<tr id="row1469681916399"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p76967197399"><a name="p76967197399"></a><a name="p76967197399"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p669611973913"><a name="p669611973913"></a><a name="p669611973913"></a>GES.7014</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p10648132116549"><a name="p10648132116549"></a><a name="p10648132116549"></a>校验元数据接口报错</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p1669631953917"><a name="p1669631953917"></a><a name="p1669631953917"></a>请检查action_id等号后面的值是否为check-schema等。</p>
</td>
</tr>
<tr id="row7452016405"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p54152094012"><a name="p54152094012"></a><a name="p54152094012"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p154172014409"><a name="p154172014409"></a><a name="p154172014409"></a>GES.7015</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p134720124017"><a name="p134720124017"></a><a name="p134720124017"></a>图不在运行或者处于停止状态</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><a name="ol1423119181106"></a><a name="ol1423119181106"></a><ol id="ol1423119181106"><li>调用图查询接口，查询所有的图</li><li>查询上述返回图列表，检查URL中的GraphID对应的图是否存在或者状态是否为900</li></ol>
</td>
</tr>
<tr id="row36611857114117"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p16661357124112"><a name="p16661357124112"></a><a name="p16661357124112"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p76621057154112"><a name="p76621057154112"></a><a name="p76621057154112"></a>GES.7016</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p1966205714119"><a name="p1966205714119"></a><a name="p1966205714119"></a>请求体或者请求头不合法</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p1866295710413"><a name="p1866295710413"></a><a name="p1866295710413"></a>请检查API参考文档，确保请求体和请求头中的每个配置项都严格按照参考文档来</p>
</td>
</tr>
<tr id="row545020233439"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p9450202314315"><a name="p9450202314315"></a><a name="p9450202314315"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p745042334320"><a name="p745042334320"></a><a name="p745042334320"></a>GES.7017</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p1845062324316"><a name="p1845062324316"></a><a name="p1845062324316"></a>对象不存在，检查桶名或者对象名是否正确</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p74515235433"><a name="p74515235433"></a><a name="p74515235433"></a>检查请求体中的图样式文件、点数据集文件或者边数据集文件是否在OBS上存在</p>
</td>
</tr>
<tr id="row11376183815448"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p637719386443"><a name="p637719386443"></a><a name="p637719386443"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p103771338134415"><a name="p103771338134415"></a><a name="p103771338134415"></a>GES.7018</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p1237763814447"><a name="p1237763814447"></a><a name="p1237763814447"></a>图个数或者边个数达到配额</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p163771838184411"><a name="p163771838184411"></a><a name="p163771838184411"></a>请调用查询配额接口，查看图是否还有可用配额</p>
</td>
</tr>
<tr id="row141536289457"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p215362817455"><a name="p215362817455"></a><a name="p215362817455"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p11531728144513"><a name="p11531728144513"></a><a name="p11531728144513"></a>GES.7019</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p61532028154518"><a name="p61532028154518"></a><a name="p61532028154518"></a>图备份个数达到配额</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p18154728104510"><a name="p18154728104510"></a><a name="p18154728104510"></a>请调用查询配额接口，查看图备份是否还有可用配额</p>
</td>
</tr>
<tr id="row824621710466"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p624617174462"><a name="p624617174462"></a><a name="p624617174462"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p92461417194614"><a name="p92461417194614"></a><a name="p92461417194614"></a>GES.7020</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p0246161784610"><a name="p0246161784610"></a><a name="p0246161784610"></a>VPC不存在</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p6246111714618"><a name="p6246111714618"></a><a name="p6246111714618"></a>查看请求体的虚拟私有云ID是否存在</p>
</td>
</tr>
<tr id="row1594319184716"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p4943791473"><a name="p4943791473"></a><a name="p4943791473"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p11943129104712"><a name="p11943129104712"></a><a name="p11943129104712"></a>GES.7021</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p15943298479"><a name="p15943298479"></a><a name="p15943298479"></a>指定的VPC下子网不存在</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p1894319964713"><a name="p1894319964713"></a><a name="p1894319964713"></a>查看请求体的子网ID是否不存在，或者是否不属于上述的虚拟私有云</p>
</td>
</tr>
<tr id="row9169414194819"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p916961418481"><a name="p916961418481"></a><a name="p916961418481"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p5169614134813"><a name="p5169614134813"></a><a name="p5169614134813"></a>GES.7022</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p19169814104814"><a name="p19169814104814"></a><a name="p19169814104814"></a>安全组不存在</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p616911413486"><a name="p616911413486"></a><a name="p616911413486"></a>查看请求体的安全组ID是否存在</p>
</td>
</tr>
<tr id="row6519129204914"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p195191391490"><a name="p195191391490"></a><a name="p195191391490"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p115201599498"><a name="p115201599498"></a><a name="p115201599498"></a>GES.7023</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p1052069104914"><a name="p1052069104914"></a><a name="p1052069104914"></a>图规模类型索引不合法</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p16520139144912"><a name="p16520139144912"></a><a name="p16520139144912"></a>查看请求体的图规模类型索引是否合法</p>
</td>
</tr>
<tr id="row1185794319498"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p685717432499"><a name="p685717432499"></a><a name="p685717432499"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p198571643144918"><a name="p198571643144918"></a><a name="p198571643144918"></a>GES.7024</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p198571643174912"><a name="p198571643174912"></a><a name="p198571643174912"></a>图备份不存在或已删除</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><a name="ol85041279105"></a><a name="ol85041279105"></a><ol id="ol85041279105"><li>调用备份查询接口，查询指定图下所有的备份</li><li>检查URL中的BackupID或者GraphID是否正确</li></ol>
</td>
</tr>
<tr id="row8291178479"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p17308754718"><a name="p17308754718"></a><a name="p17308754718"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p1330127104711"><a name="p1330127104711"></a><a name="p1330127104711"></a>GES.7027</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p53012744711"><a name="p53012744711"></a><a name="p53012744711"></a>委托创建失败</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p16301474475"><a name="p16301474475"></a><a name="p16301474475"></a>查看errorMessage获取具体信息</p>
</td>
</tr>
<tr id="row11691926133015"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p8170152683015"><a name="p8170152683015"></a><a name="p8170152683015"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p1117072623010"><a name="p1117072623010"></a><a name="p1117072623010"></a>GES.7028</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p1017052613013"><a name="p1017052613013"></a><a name="p1017052613013"></a>委托授权失败</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p62208187316"><a name="p62208187316"></a><a name="p62208187316"></a>查看errorMessage获取具体信息</p>
</td>
</tr>
<tr id="row0366102417315"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p4366142420311"><a name="p4366142420311"></a><a name="p4366142420311"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p83661624203111"><a name="p83661624203111"></a><a name="p83661624203111"></a>GES.7029</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p3366122473117"><a name="p3366122473117"></a><a name="p3366122473117"></a>委托超过配额限制</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p1536642463110"><a name="p1536642463110"></a><a name="p1536642463110"></a>在IAM界面查看委托是否达到配额限制</p>
</td>
</tr>
<tr id="row1257183416323"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p9571534153218"><a name="p9571534153218"></a><a name="p9571534153218"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p185715343320"><a name="p185715343320"></a><a name="p185715343320"></a>GES.7030</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p757118346323"><a name="p757118346323"></a><a name="p757118346323"></a>委托查询出错</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p0932121223319"><a name="p0932121223319"></a><a name="p0932121223319"></a>查看errorMessage获取具体信息</p>
</td>
</tr>
<tr id="row5151531123316"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p11151131133314"><a name="p11151131133314"></a><a name="p11151131133314"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p101511310335"><a name="p101511310335"></a><a name="p101511310335"></a>GES.7031</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p1915143123311"><a name="p1915143123311"></a><a name="p1915143123311"></a>弹性IP绑定类型不合法</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p12813427265"><a name="p12813427265"></a><a name="p12813427265"></a>确认弹性IP绑定类型，取值如下：</p>
<a name="ul168138271969"></a><a name="ul168138271969"></a><ul id="ul168138271969"><li>auto_assign：自动绑定</li><li>bind_existing：使用已有</li></ul>
</td>
</tr>
<tr id="row547135753419"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p1448195723416"><a name="p1448195723416"></a><a name="p1448195723416"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p74875715342"><a name="p74875715342"></a><a name="p74875715342"></a>GES.7032</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p20481957143415"><a name="p20481957143415"></a><a name="p20481957143415"></a>弹性IP超过配额限制</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p148175713346"><a name="p148175713346"></a><a name="p148175713346"></a>在VPC弹性公网IP界面查看是否达到配额限制</p>
</td>
</tr>
<tr id="row1084905612358"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p985015643512"><a name="p985015643512"></a><a name="p985015643512"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p48509566350"><a name="p48509566350"></a><a name="p48509566350"></a>GES.7033</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p18501856183515"><a name="p18501856183515"></a><a name="p18501856183515"></a>弹性IP ID不合法</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p14850956113514"><a name="p14850956113514"></a><a name="p14850956113514"></a>如果弹性IP绑定类型选择"bind_existing",请确保eipId真实存在</p>
</td>
</tr>
<tr id="row963174010374"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p163640183717"><a name="p163640183717"></a><a name="p163640183717"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p26384010379"><a name="p26384010379"></a><a name="p26384010379"></a>GES.7034</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p196324043719"><a name="p196324043719"></a><a name="p196324043719"></a>当前available zone已售罄</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p14631440193713"><a name="p14631440193713"></a><a name="p14631440193713"></a>请切换别的available zone后重试</p>
</td>
</tr>
<tr id="row314815325385"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p8149143219388"><a name="p8149143219388"></a><a name="p8149143219388"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p141498327380"><a name="p141498327380"></a><a name="p141498327380"></a>GES.7035</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p71491132153818"><a name="p71491132153818"></a><a name="p71491132153818"></a>Region编码不合法</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p814919328386"><a name="p814919328386"></a><a name="p814919328386"></a>确保输入正确的Region编码</p>
</td>
</tr>
<tr id="row4392111743912"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p239261716397"><a name="p239261716397"></a><a name="p239261716397"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p83921717143910"><a name="p83921717143910"></a><a name="p83921717143910"></a>GES.7036</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p23920176394"><a name="p23920176394"></a><a name="p23920176394"></a>升级版本低于当前版本</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p173929176394"><a name="p173929176394"></a><a name="p173929176394"></a>升级图时还能升级到高版本</p>
</td>
</tr>
<tr id="row1884011819407"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p1484038114015"><a name="p1484038114015"></a><a name="p1484038114015"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p128407894012"><a name="p128407894012"></a><a name="p128407894012"></a>GES.7037</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p48402089401"><a name="p48402089401"></a><a name="p48402089401"></a>图不在停止状态</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p1284018114012"><a name="p1284018114012"></a><a name="p1284018114012"></a>查看图是否处于停止状态</p>
</td>
</tr>
<tr id="row1044154912409"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p34429495404"><a name="p34429495404"></a><a name="p34429495404"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p194421149174010"><a name="p194421149174010"></a><a name="p194421149174010"></a>GES.7038</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p7442184904014"><a name="p7442184904014"></a><a name="p7442184904014"></a>图不能重复绑定EIP</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p1610072619418"><a name="p1610072619418"></a><a name="p1610072619418"></a>图不能重复绑定EIP</p>
</td>
</tr>
<tr id="row10291030124110"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p030130144113"><a name="p030130144113"></a><a name="p030130144113"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p1730123014119"><a name="p1730123014119"></a><a name="p1730123014119"></a>GES.7039</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p53013308414"><a name="p53013308414"></a><a name="p53013308414"></a>没有绑定图的EIP不能执行解绑EIP操作</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p1048145144419"><a name="p1048145144419"></a><a name="p1048145144419"></a>没有绑定图的EIP不能执行解绑EIP操作</p>
</td>
</tr>
<tr id="row1175011904413"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p19750091447"><a name="p19750091447"></a><a name="p19750091447"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p8750179144413"><a name="p8750179144413"></a><a name="p8750179144413"></a>GES.7040</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p875019164412"><a name="p875019164412"></a><a name="p875019164412"></a>图备份没有成功</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p587517518475"><a name="p587517518475"></a><a name="p587517518475"></a>从备份恢复图时，选择的备份没有成功</p>
</td>
</tr>
<tr id="row12289125011479"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p228985019476"><a name="p228985019476"></a><a name="p228985019476"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p3289135011475"><a name="p3289135011475"></a><a name="p3289135011475"></a>GES.7041</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p82891950204713"><a name="p82891950204713"></a><a name="p82891950204713"></a>账号权限不足</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p3491161217486"><a name="p3491161217486"></a><a name="p3491161217486"></a>账号权限不足</p>
</td>
</tr>
<tr id="row355181664817"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p105531618481"><a name="p105531618481"></a><a name="p105531618481"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p25510169485"><a name="p25510169485"></a><a name="p25510169485"></a>GES.7042</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p455111684818"><a name="p455111684818"></a><a name="p455111684818"></a>图在创建中</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p135521624814"><a name="p135521624814"></a><a name="p135521624814"></a>图仍在创建中</p>
</td>
</tr>
<tr id="row15111735105511"><td class="cellrowborder" valign="top" width="10.36103610361036%" headers="mcps1.2.5.1.1 "><p id="p16512123535513"><a name="p16512123535513"></a><a name="p16512123535513"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.721572157215721%" headers="mcps1.2.5.1.2 "><p id="p19871042195515"><a name="p19871042195515"></a><a name="p19871042195515"></a>GES.7048</p>
</td>
<td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.2.5.1.3 "><p id="p1751319356555"><a name="p1751319356555"></a><a name="p1751319356555"></a>图操作不合法</p>
</td>
<td class="cellrowborder" valign="top" width="51.44514451445145%" headers="mcps1.2.5.1.4 "><p id="p12513173513558"><a name="p12513173513558"></a><a name="p12513173513558"></a>请检查action_id等号后面的值是否为start,stop,import-graph,export-graph,clear-graph,upgrade等。</p>
</td>
</tr>
</tbody>
</table>


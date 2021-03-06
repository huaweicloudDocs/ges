# 业务面API错误码<a name="ges_03_0110"></a>

调用接口出错后，将不会返回结果数据。调用方可根据每个接口对应的错误码来定位错误原因。当调用出错时，HTTP 请求返回一个 4xx 或 5xx 的 HTTP 状态码。返回的消息体中是具体的错误代码及错误信息。在调用方找不到错误原因时，可以联系企业技术人员，并提供错误码，以便我们尽快帮您解决问题。

当您调用API时，如果遇到“APIGW”开头的错误码，请参见[API网关错误码](https://support.huaweicloud.com/devg-apisign/api-sign-errorcode.html)进行处理。

**表 1**  错误码

<a name="zh-cn_topic_0094388422_table13150194944219"></a>
<table><thead align="left"><tr id="zh-cn_topic_0094388422_row1515018490427"><th class="cellrowborder" valign="top" width="10.59105910591059%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0094388422_p215064994216"><a name="zh-cn_topic_0094388422_p215064994216"></a><a name="zh-cn_topic_0094388422_p215064994216"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="15.421542154215423%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0094388422_p12150749164219"><a name="zh-cn_topic_0094388422_p12150749164219"></a><a name="zh-cn_topic_0094388422_p12150749164219"></a>错误码</p>
</th>
<th class="cellrowborder" valign="top" width="31.663166316631663%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0094388422_p151501049144216"><a name="zh-cn_topic_0094388422_p151501049144216"></a><a name="zh-cn_topic_0094388422_p151501049144216"></a>错误信息</p>
</th>
<th class="cellrowborder" valign="top" width="42.32423242324232%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0094388422_p1715010494422"><a name="zh-cn_topic_0094388422_p1715010494422"></a><a name="zh-cn_topic_0094388422_p1715010494422"></a>处理措施</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0094388422_row16150144924212"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0094388422_p9899922144317"><a name="zh-cn_topic_0094388422_p9899922144317"></a><a name="zh-cn_topic_0094388422_p9899922144317"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0094388422_p7899102218438"><a name="zh-cn_topic_0094388422_p7899102218438"></a><a name="zh-cn_topic_0094388422_p7899102218438"></a>GES.8000</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0094388422_p12899822164320"><a name="zh-cn_topic_0094388422_p12899822164320"></a><a name="zh-cn_topic_0094388422_p12899822164320"></a>参数格式错误</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p1773119171318"><a name="p1773119171318"></a><a name="p1773119171318"></a>检查请求body体是否和文档描述一致</p>
</td>
</tr>
<tr id="row89083222129"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p7908162231217"><a name="p7908162231217"></a><a name="p7908162231217"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p390892219123"><a name="p390892219123"></a><a name="p390892219123"></a>GES.8001</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p6909192241214"><a name="p6909192241214"></a><a name="p6909192241214"></a>图统计信息查询失败</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p69095222124"><a name="p69095222124"></a><a name="p69095222124"></a>根据errorMessage查看错误信息</p>
</td>
</tr>
<tr id="row19985113131515"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p13985513171516"><a name="p13985513171516"></a><a name="p13985513171516"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p179852133159"><a name="p179852133159"></a><a name="p179852133159"></a>GES.8002</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p6708830141516"><a name="p6708830141516"></a><a name="p6708830141516"></a>图统计信息查询错误</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p154736124174"><a name="p154736124174"></a><a name="p154736124174"></a>根据errorMessage查看错误信息</p>
</td>
</tr>
<tr id="row4132182112176"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p111328213172"><a name="p111328213172"></a><a name="p111328213172"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p141331621121720"><a name="p141331621121720"></a><a name="p141331621121720"></a>GES.8005</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p7133221131713"><a name="p7133221131713"></a><a name="p7133221131713"></a>参数错误</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><a name="ol440911188910"></a><a name="ol440911188910"></a><ol id="ol440911188910"><li>检查URL中的ProjectID是否正确</li><li>检查请求头是否正确，比如X-Auth-Token是否正确</li></ol>
</td>
</tr>
<tr id="row2016784061915"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p71670402192"><a name="p71670402192"></a><a name="p71670402192"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p316764031919"><a name="p316764031919"></a><a name="p316764031919"></a>GES.8006</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p1992212802015"><a name="p1992212802015"></a><a name="p1992212802015"></a>资源访问不合法</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p11671240131914"><a name="p11671240131914"></a><a name="p11671240131914"></a>检查URL中的ProjectID是否正确</p>
</td>
</tr>
<tr id="row18306135312015"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p1730605342019"><a name="p1730605342019"></a><a name="p1730605342019"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p13306135312208"><a name="p13306135312208"></a><a name="p13306135312208"></a>GES.8007</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p1230614531204"><a name="p1230614531204"></a><a name="p1230614531204"></a>Token不合法</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p63061953142010"><a name="p63061953142010"></a><a name="p63061953142010"></a>检查Token是否正确</p>
</td>
</tr>
<tr id="row1615413582117"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p141548356215"><a name="p141548356215"></a><a name="p141548356215"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p71552352213"><a name="p71552352213"></a><a name="p71552352213"></a>GES.8008</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p1115514358212"><a name="p1115514358212"></a><a name="p1115514358212"></a>底层认证系统出错</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p775014388227"><a name="p775014388227"></a><a name="p775014388227"></a>请稍后重试或联系技术人员</p>
</td>
</tr>
<tr id="row951375522214"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p15513105562216"><a name="p15513105562216"></a><a name="p15513105562216"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p18513455162214"><a name="p18513455162214"></a><a name="p18513455162214"></a>GES.8011</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p165081667245"><a name="p165081667245"></a><a name="p165081667245"></a>导出图失败</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><a name="ol660693513211"></a><a name="ol660693513211"></a><ol id="ol660693513211"><li>检查图名是否正确。</li><li>查看导出文件路径是否正确。</li><li>检查该账号有无OBS写入权限。</li></ol>
</td>
</tr>
<tr id="row312815239241"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p13128323172415"><a name="p13128323172415"></a><a name="p13128323172415"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p14128523172411"><a name="p14128523172411"></a><a name="p14128523172411"></a>GES.8012</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p11129823172413"><a name="p11129823172413"></a><a name="p11129823172413"></a>清空图失败</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p2379114222413"><a name="p2379114222413"></a><a name="p2379114222413"></a>根据errorMessage查看错误信息</p>
</td>
</tr>
<tr id="row5593445122411"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p6593445162416"><a name="p6593445162416"></a><a name="p6593445162416"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p12593745102414"><a name="p12593745102414"></a><a name="p12593745102414"></a>GES.8013</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p2593114542411"><a name="p2593114542411"></a><a name="p2593114542411"></a>增量导入图失败</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p107918594445"><a name="p107918594445"></a><a name="p107918594445"></a>根据errorMessage查看错误信息</p>
</td>
</tr>
<tr id="row192021274513"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p120211264514"><a name="p120211264514"></a><a name="p120211264514"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p112021527457"><a name="p112021527457"></a><a name="p112021527457"></a>GES.8101</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p59142419469"><a name="p59142419469"></a><a name="p59142419469"></a>边过滤查询条件不合法</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p720219220451"><a name="p720219220451"></a><a name="p720219220451"></a>检查边过滤条件格式是否正确</p>
</td>
</tr>
<tr id="row19241681083"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p1892415820814"><a name="p1892415820814"></a><a name="p1892415820814"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p7924198585"><a name="p7924198585"></a><a name="p7924198585"></a>GES.8102</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p11924281987"><a name="p11924281987"></a><a name="p11924281987"></a>边过滤查询Label不合法</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p03411153172418"><a name="p03411153172418"></a><a name="p03411153172418"></a>检查labels是不是正常的josn体</p>
</td>
</tr>
<tr id="row1494216520912"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p199431515914"><a name="p199431515914"></a><a name="p199431515914"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p13943452915"><a name="p13943452915"></a><a name="p13943452915"></a>GES.8103</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p17943451096"><a name="p17943451096"></a><a name="p17943451096"></a>边过滤查询条件和Label同时为空</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p193581572101"><a name="p193581572101"></a><a name="p193581572101"></a>边过滤查询条件和Label不能同时为空</p>
</td>
</tr>
<tr id="row432610186101"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p432671814103"><a name="p432671814103"></a><a name="p432671814103"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p18326151817109"><a name="p18326151817109"></a><a name="p18326151817109"></a>GES.8104</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p032651813102"><a name="p032651813102"></a><a name="p032651813102"></a>边过滤排序输入不合法</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p18326618121020"><a name="p18326618121020"></a><a name="p18326618121020"></a>检查边过滤排序输入是否合法</p>
</td>
</tr>
<tr id="row14136142131115"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p6771123991719"><a name="p6771123991719"></a><a name="p6771123991719"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p913764221112"><a name="p913764221112"></a><a name="p913764221112"></a>GES.8105</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p12137842191110"><a name="p12137842191110"></a><a name="p12137842191110"></a>边过滤查询执行失败</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p181115396441"><a name="p181115396441"></a><a name="p181115396441"></a>根据errorMessage查看错误信息</p>
</td>
</tr>
<tr id="row52115259122"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p1380493916174"><a name="p1380493916174"></a><a name="p1380493916174"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p15211125131212"><a name="p15211125131212"></a><a name="p15211125131212"></a>GES.8106</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p13211225131214"><a name="p13211225131214"></a><a name="p13211225131214"></a>边详情起点或终点为空</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p92113253122"><a name="p92113253122"></a><a name="p92113253122"></a>边详情起点和终点不能为空</p>
</td>
</tr>
<tr id="row8158185461218"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p1281114393179"><a name="p1281114393179"></a><a name="p1281114393179"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p20143181016138"><a name="p20143181016138"></a><a name="p20143181016138"></a>GES.8107</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p131431910191313"><a name="p131431910191313"></a><a name="p131431910191313"></a>边详情查询失败</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p1620134112446"><a name="p1620134112446"></a><a name="p1620134112446"></a>根据errorMessage查看错误信息</p>
</td>
</tr>
<tr id="row618615578124"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p17821183915172"><a name="p17821183915172"></a><a name="p17821183915172"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p17900145617132"><a name="p17900145617132"></a><a name="p17900145617132"></a>GES.8108</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p149001056141311"><a name="p149001056141311"></a><a name="p149001056141311"></a>边详情查询内部错误</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p924695614316"><a name="p924695614316"></a><a name="p924695614316"></a>请稍后重试或联系技术人员</p>
</td>
</tr>
<tr id="row14620111421313"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p883143951718"><a name="p883143951718"></a><a name="p883143951718"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p1255416514147"><a name="p1255416514147"></a><a name="p1255416514147"></a>GES.8109</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p6554151151416"><a name="p6554151151416"></a><a name="p6554151151416"></a>边过滤查询算子不合法</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p1262001419135"><a name="p1262001419135"></a><a name="p1262001419135"></a>边过滤查询算子取值为 in、out、both、edge</p>
</td>
</tr>
<tr id="row103557185134"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p484233901712"><a name="p484233901712"></a><a name="p484233901712"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p035516184139"><a name="p035516184139"></a><a name="p035516184139"></a>GES.8110</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p1355718171317"><a name="p1355718171317"></a><a name="p1355718171317"></a>参数edges不能为空</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p18418152794813"><a name="p18418152794813"></a><a name="p18418152794813"></a>批量边查询请求体中edges是否为空</p>
</td>
</tr>
<tr id="row829042151315"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p1985414391174"><a name="p1985414391174"></a><a name="p1985414391174"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p9827253173"><a name="p9827253173"></a><a name="p9827253173"></a>GES.8201</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p882819591718"><a name="p882819591718"></a><a name="p882819591718"></a>点过滤查询Label不合法</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p83523144250"><a name="p83523144250"></a><a name="p83523144250"></a>检查labels是不是正常的josn体</p>
</td>
</tr>
<tr id="row26231127131315"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p6864153961719"><a name="p6864153961719"></a><a name="p6864153961719"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p128285510175"><a name="p128285510175"></a><a name="p128285510175"></a>GES.8202</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p1282865131716"><a name="p1282865131716"></a><a name="p1282865131716"></a>点过滤查询条件不合法</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p17884144716441"><a name="p17884144716441"></a><a name="p17884144716441"></a>根据errorMessage查看错误信息</p>
</td>
</tr>
<tr id="row78431524111316"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p98701639121716"><a name="p98701639121716"></a><a name="p98701639121716"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p88281553178"><a name="p88281553178"></a><a name="p88281553178"></a>GES.8203</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p582817551713"><a name="p582817551713"></a><a name="p582817551713"></a>点过滤查询条件和Label同时为空</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p084472481316"><a name="p084472481316"></a><a name="p084472481316"></a>点过滤条件和Label不能同时为空</p>
</td>
</tr>
<tr id="row5618193041318"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p15880203913178"><a name="p15880203913178"></a><a name="p15880203913178"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p178282514179"><a name="p178282514179"></a><a name="p178282514179"></a>GES.8204</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p14828165161710"><a name="p14828165161710"></a><a name="p14828165161710"></a>点过滤查询执行失败</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p15619230181319"><a name="p15619230181319"></a><a name="p15619230181319"></a>根据errorMessage查看错误信息</p>
</td>
</tr>
<tr id="row1437743314135"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p1310743121714"><a name="p1310743121714"></a><a name="p1310743121714"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p9828258171"><a name="p9828258171"></a><a name="p9828258171"></a>GES.8205</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p128299521710"><a name="p128299521710"></a><a name="p128299521710"></a>点过滤排序输入不合法</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p1736116544394"><a name="p1736116544394"></a><a name="p1736116544394"></a>点过滤查询API中orderValue必须在“incr”和“decr”</p>
</td>
</tr>
<tr id="row1555736171312"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p133239430178"><a name="p133239430178"></a><a name="p133239430178"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p2082911517178"><a name="p2082911517178"></a><a name="p2082911517178"></a>GES.8206</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p3829458172"><a name="p3829458172"></a><a name="p3829458172"></a>vertexid和vertextids同时存在</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p18491130164320"><a name="p18491130164320"></a><a name="p18491130164320"></a>vertexid和vertextids不能同时存在</p>
</td>
</tr>
<tr id="row845174411318"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p1233614312177"><a name="p1233614312177"></a><a name="p1233614312177"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p1282925141712"><a name="p1282925141712"></a><a name="p1282925141712"></a>GES.8207</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p198295518171"><a name="p198295518171"></a><a name="p198295518171"></a>vertexid和vertextids同时为空</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p649183024310"><a name="p649183024310"></a><a name="p649183024310"></a>vertexid或vertextids为空</p>
</td>
</tr>
<tr id="row38531147131313"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p19344243121713"><a name="p19344243121713"></a><a name="p19344243121713"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p11829450171"><a name="p11829450171"></a><a name="p11829450171"></a>GES.8208</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p382955131714"><a name="p382955131714"></a><a name="p382955131714"></a>vertextids格式错误</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p08533472137"><a name="p08533472137"></a><a name="p08533472137"></a>vertextids是否 json array</p>
</td>
</tr>
<tr id="row146491840161311"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p103571243141713"><a name="p103571243141713"></a><a name="p103571243141713"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p15829557176"><a name="p15829557176"></a><a name="p15829557176"></a>GES.8209</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p198291754175"><a name="p198291754175"></a><a name="p198291754175"></a>点详情查询失败</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p6751916173313"><a name="p6751916173313"></a><a name="p6751916173313"></a>检查图名是否存在</p>
</td>
</tr>
<tr id="row43583141716"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p6366194311172"><a name="p6366194311172"></a><a name="p6366194311172"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p198301457175"><a name="p198301457175"></a><a name="p198301457175"></a>GES.8210</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p138301656170"><a name="p138301656170"></a><a name="p138301656170"></a>点详情查询内部错误</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p48905208396"><a name="p48905208396"></a><a name="p48905208396"></a>请稍后重试或联系技术人员</p>
</td>
</tr>
<tr id="row17606656121719"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p673832187"><a name="p673832187"></a><a name="p673832187"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p3733391820"><a name="p3733391820"></a><a name="p3733391820"></a>GES.8211</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p17738311188"><a name="p17738311188"></a><a name="p17738311188"></a>点过滤查询算子不合法</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p160655618171"><a name="p160655618171"></a><a name="p160655618171"></a>点过滤查询算子取值为 inV、outV、bothV、vertex</p>
</td>
</tr>
<tr id="row330803061811"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p29501634171819"><a name="p29501634171819"></a><a name="p29501634171819"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p1495014347183"><a name="p1495014347183"></a><a name="p1495014347183"></a>GES.8212</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p15950334101818"><a name="p15950334101818"></a><a name="p15950334101818"></a>删除点Label失败</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p63081430101812"><a name="p63081430101812"></a><a name="p63081430101812"></a>Label是否存在</p>
</td>
</tr>
<tr id="row02253204196"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p7691144951914"><a name="p7691144951914"></a><a name="p7691144951914"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p569114981917"><a name="p569114981917"></a><a name="p569114981917"></a>GES.8213</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p569164911910"><a name="p569164911910"></a><a name="p569164911910"></a>增加点Label失败</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p1422532051915"><a name="p1422532051915"></a><a name="p1422532051915"></a>Label是否存在</p>
</td>
</tr>
<tr id="row1832617717208"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p7716201017207"><a name="p7716201017207"></a><a name="p7716201017207"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p3716111010202"><a name="p3716111010202"></a><a name="p3716111010202"></a>GES.8214</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p16716610132017"><a name="p16716610132017"></a><a name="p16716610132017"></a>参数vertices不能空</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p11326107182012"><a name="p11326107182012"></a><a name="p11326107182012"></a>批量点查询请求体中vertices是否为空</p>
</td>
</tr>
<tr id="row1911195414206"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p19112125472013"><a name="p19112125472013"></a><a name="p19112125472013"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p63647166212"><a name="p63647166212"></a><a name="p63647166212"></a>GES.8220</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p143651916112112"><a name="p143651916112112"></a><a name="p143651916112112"></a>更新点属性失败</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p11191164745116"><a name="p11191164745116"></a><a name="p11191164745116"></a>根据errorMessage查看错误信息</p>
</td>
</tr>
<tr id="row151511482211"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p2086485310210"><a name="p2086485310210"></a><a name="p2086485310210"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p13864165314213"><a name="p13864165314213"></a><a name="p13864165314213"></a>GES.8221</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p7865195312213"><a name="p7865195312213"></a><a name="p7865195312213"></a>更新边属性失败</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p12206154745114"><a name="p12206154745114"></a><a name="p12206154745114"></a>根据errorMessage查看错误信息</p>
</td>
</tr>
<tr id="row161951613122218"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p1519511362216"><a name="p1519511362216"></a><a name="p1519511362216"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p9122164332219"><a name="p9122164332219"></a><a name="p9122164332219"></a>GES.8301</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p1712274322215"><a name="p1712274322215"></a><a name="p1712274322215"></a>作业查询失败</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p0223147135113"><a name="p0223147135113"></a><a name="p0223147135113"></a>根据errorMessage查看错误信息</p>
</td>
</tr>
<tr id="row7775133117224"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p843215364287"><a name="p843215364287"></a><a name="p843215364287"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p1512264314227"><a name="p1512264314227"></a><a name="p1512264314227"></a>GES.8302</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p31224439222"><a name="p31224439222"></a><a name="p31224439222"></a>作业查询内部错误</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p4830111513913"><a name="p4830111513913"></a><a name="p4830111513913"></a>请稍后重试或联系技术人员</p>
</td>
</tr>
<tr id="row1794183618222"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p1472123616282"><a name="p1472123616282"></a><a name="p1472123616282"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p41229430222"><a name="p41229430222"></a><a name="p41229430222"></a>GES.8303</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p10122154392210"><a name="p10122154392210"></a><a name="p10122154392210"></a>作业终止失败</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p199514362225"><a name="p199514362225"></a><a name="p199514362225"></a>根据errorMessage查看错误信息</p>
</td>
</tr>
<tr id="row612010395228"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p748843632814"><a name="p748843632814"></a><a name="p748843632814"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p171222043192210"><a name="p171222043192210"></a><a name="p171222043192210"></a>GES.8304</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p912219435226"><a name="p912219435226"></a><a name="p912219435226"></a>作业终止内部错误</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p1237951713917"><a name="p1237951713917"></a><a name="p1237951713917"></a>请稍后重试或联系技术人员</p>
</td>
</tr>
<tr id="row148531875236"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p250318367285"><a name="p250318367285"></a><a name="p250318367285"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p5551482417"><a name="p5551482417"></a><a name="p5551482417"></a>GES.8401</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p1362142247"><a name="p1362142247"></a><a name="p1362142247"></a>算法名或者图名不能为空</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p685311772317"><a name="p685311772317"></a><a name="p685311772317"></a>算法名或者图名不能为空</p>
</td>
</tr>
<tr id="row24185116237"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p165142360287"><a name="p165142360287"></a><a name="p165142360287"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p13611411246"><a name="p13611411246"></a><a name="p13611411246"></a>GES.8402</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p1163145244"><a name="p1163145244"></a><a name="p1163145244"></a>算法执行失败</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p16418111113237"><a name="p16418111113237"></a><a name="p16418111113237"></a>根据errorMessage查看错误信息</p>
</td>
</tr>
<tr id="row93248147238"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p9526143619289"><a name="p9526143619289"></a><a name="p9526143619289"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p16631410248"><a name="p16631410248"></a><a name="p16631410248"></a>GES.8403</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p19651417241"><a name="p19651417241"></a><a name="p19651417241"></a>算法执行内部错误</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p07249147397"><a name="p07249147397"></a><a name="p07249147397"></a>请稍后重试或联系技术人员</p>
</td>
</tr>
<tr id="row248616179234"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p14538133615286"><a name="p14538133615286"></a><a name="p14538133615286"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p795011299244"><a name="p795011299244"></a><a name="p795011299244"></a>GES.8404</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p69501229122413"><a name="p69501229122413"></a><a name="p69501229122413"></a>算法执行模式不合法</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p114861317152320"><a name="p114861317152320"></a><a name="p114861317152320"></a>根据errorMessage查看错误信息</p>
</td>
</tr>
<tr id="row5153477248"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p5552133622820"><a name="p5552133622820"></a><a name="p5552133622820"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p20772734112512"><a name="p20772734112512"></a><a name="p20772734112512"></a>GES.8501</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p377263419251"><a name="p377263419251"></a><a name="p377263419251"></a>Gremlin查询命令不支持</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p13151475247"><a name="p13151475247"></a><a name="p13151475247"></a>不支持Gremlin的tryNext、explain、tree语句</p>
</td>
</tr>
<tr id="row1155651418258"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p356253619289"><a name="p356253619289"></a><a name="p356253619289"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p1477223472512"><a name="p1477223472512"></a><a name="p1477223472512"></a>GES.8502</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p147721634162510"><a name="p147721634162510"></a><a name="p147721634162510"></a>Gremlin配置文件找不到</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p7557114172517"><a name="p7557114172517"></a><a name="p7557114172517"></a>请稍后重试或联系技术人员</p>
</td>
</tr>
<tr id="row16589717182517"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p1157653602819"><a name="p1157653602819"></a><a name="p1157653602819"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p177223414251"><a name="p177223414251"></a><a name="p177223414251"></a>GES.8503</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p11772133482515"><a name="p11772133482515"></a><a name="p11772133482515"></a>Gremlin查询执行失败</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p9590121712518"><a name="p9590121712518"></a><a name="p9590121712518"></a>根据errorMessage查看错误信息</p>
</td>
</tr>
<tr id="row52671522182510"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p3591036172818"><a name="p3591036172818"></a><a name="p3591036172818"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p1772173417256"><a name="p1772173417256"></a><a name="p1772173417256"></a>GES.8504</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p1677219340258"><a name="p1677219340258"></a><a name="p1677219340258"></a>Gremlin查询内部错误</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p191213110531"><a name="p191213110531"></a><a name="p191213110531"></a>请稍后重试或联系技术人员</p>
</td>
</tr>
<tr id="row12438162562511"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p7606236132817"><a name="p7606236132817"></a><a name="p7606236132817"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p1081625420259"><a name="p1081625420259"></a><a name="p1081625420259"></a>GES.8505</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p1981625410256"><a name="p1981625410256"></a><a name="p1981625410256"></a>Gremlin查询语句没有command字段</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p19438142532517"><a name="p19438142532517"></a><a name="p19438142532517"></a>Gremlin查询语句没有command字段</p>
</td>
</tr>
<tr id="row8606133032511"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p46214366286"><a name="p46214366286"></a><a name="p46214366286"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p1592195813259"><a name="p1592195813259"></a><a name="p1592195813259"></a>GES.8506</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p1759345817251"><a name="p1759345817251"></a><a name="p1759345817251"></a>Gremlin查询请求语句超过限制</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p06071730132520"><a name="p06071730132520"></a><a name="p06071730132520"></a>当前限制为64MB</p>
</td>
</tr>
<tr id="row1541334142720"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p1641314482719"><a name="p1641314482719"></a><a name="p1641314482719"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p1326811164274"><a name="p1326811164274"></a><a name="p1326811164274"></a>GES.8601</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p14268131619277"><a name="p14268131619277"></a><a name="p14268131619277"></a>Gremlin服务不可用</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p841312414276"><a name="p841312414276"></a><a name="p841312414276"></a>请稍后重试或联系技术人员</p>
</td>
</tr>
<tr id="row2055659152716"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p7556189172713"><a name="p7556189172713"></a><a name="p7556189172713"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p11268191618274"><a name="p11268191618274"></a><a name="p11268191618274"></a>GES.8602</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p1726891610270"><a name="p1726891610270"></a><a name="p1726891610270"></a>Engine服务不可用</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p1939024133914"><a name="p1939024133914"></a><a name="p1939024133914"></a>请稍后重试或联系技术人员</p>
</td>
</tr>
<tr id="row1871081342917"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p14710313132913"><a name="p14710313132913"></a><a name="p14710313132913"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p4710151315297"><a name="p4710151315297"></a><a name="p4710151315297"></a>GES.8603</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p1471001342914"><a name="p1471001342914"></a><a name="p1471001342914"></a>索引创建失败</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p816034915311"><a name="p816034915311"></a><a name="p816034915311"></a>根据errorMessage查看错误信息</p>
</td>
</tr>
<tr id="row21651516113014"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p1674521163012"><a name="p1674521163012"></a><a name="p1674521163012"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p8674192173010"><a name="p8674192173010"></a><a name="p8674192173010"></a>GES.8604</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p2067482119301"><a name="p2067482119301"></a><a name="p2067482119301"></a>索引删除失败</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p42002049135320"><a name="p42002049135320"></a><a name="p42002049135320"></a>根据errorMessage查看错误信息</p>
</td>
</tr>
<tr id="row3139537193016"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p191391337123015"><a name="p191391337123015"></a><a name="p191391337123015"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p1998654218301"><a name="p1998654218301"></a><a name="p1998654218301"></a>GES.8605</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p613953783013"><a name="p613953783013"></a><a name="p613953783013"></a>索引查询失败</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p121264915316"><a name="p121264915316"></a><a name="p121264915316"></a>根据errorMessage查看错误信息</p>
</td>
</tr>
<tr id="row1023983312313"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p01221527375"><a name="p01221527375"></a><a name="p01221527375"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p1323963314311"><a name="p1323963314311"></a><a name="p1323963314311"></a>GES.8609</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p10239113317316"><a name="p10239113317316"></a><a name="p10239113317316"></a>查询路径详情请求体不合法</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p112481649135315"><a name="p112481649135315"></a><a name="p112481649135315"></a>根据errorMessage查看错误信息</p>
</td>
</tr>
<tr id="row106361238203115"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p9138552153712"><a name="p9138552153712"></a><a name="p9138552153712"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p563610389317"><a name="p563610389317"></a><a name="p563610389317"></a>GES.8610</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p963693811315"><a name="p963693811315"></a><a name="p963693811315"></a>查询路径详情请求体path参数不合法</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p82641849125311"><a name="p82641849125311"></a><a name="p82641849125311"></a>根据errorMessage查看错误信息</p>
</td>
</tr>
<tr id="row4717341103115"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p171551452153716"><a name="p171551452153716"></a><a name="p171551452153716"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p271774103112"><a name="p271774103112"></a><a name="p271774103112"></a>GES.8611</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p1571719413311"><a name="p1571719413311"></a><a name="p1571719413311"></a>查询路径详情失败</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p1727644985312"><a name="p1727644985312"></a><a name="p1727644985312"></a>根据errorMessage查看错误信息</p>
</td>
</tr>
<tr id="row1470415462315"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p11168552143718"><a name="p11168552143718"></a><a name="p11168552143718"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p2705194618316"><a name="p2705194618316"></a><a name="p2705194618316"></a>GES.8612</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p770544617314"><a name="p770544617314"></a><a name="p770544617314"></a>查询路径详情操作不支持</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p16291124965312"><a name="p16291124965312"></a><a name="p16291124965312"></a>根据errorMessage查看错误信息</p>
</td>
</tr>
<tr id="row1997215431314"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p818415215374"><a name="p818415215374"></a><a name="p818415215374"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p11972154353115"><a name="p11972154353115"></a><a name="p11972154353115"></a>GES.8801</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p1497212434311"><a name="p1497212434311"></a><a name="p1497212434311"></a>元数据添加label失败</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p203059491534"><a name="p203059491534"></a><a name="p203059491534"></a>根据errorMessage查看错误信息</p>
</td>
</tr>
<tr id="row1146024843210"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p1019775211371"><a name="p1019775211371"></a><a name="p1019775211371"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p12460174843220"><a name="p12460174843220"></a><a name="p12460174843220"></a>GES.8803</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p18460194812325"><a name="p18460194812325"></a><a name="p18460194812325"></a>元数据查询失败</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p1831794945316"><a name="p1831794945316"></a><a name="p1831794945316"></a>根据errorMessage查看错误信息</p>
</td>
</tr>
<tr id="row18192754183213"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p201921954153213"><a name="p201921954153213"></a><a name="p201921954153213"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p1919316549322"><a name="p1919316549322"></a><a name="p1919316549322"></a>GES.8804</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p919365403210"><a name="p919365403210"></a><a name="p919365403210"></a>元数据查询内部错误</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p3676151113390"><a name="p3676151113390"></a><a name="p3676151113390"></a>请稍后重试或联系技术人员</p>
</td>
</tr>
<tr id="row1460815483318"><td class="cellrowborder" valign="top" width="10.59105910591059%" headers="mcps1.2.5.1.1 "><p id="p26097433311"><a name="p26097433311"></a><a name="p26097433311"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="15.421542154215423%" headers="mcps1.2.5.1.2 "><p id="p1560916493316"><a name="p1560916493316"></a><a name="p1560916493316"></a>GES.8806</p>
</td>
<td class="cellrowborder" valign="top" width="31.663166316631663%" headers="mcps1.2.5.1.3 "><p id="p166094416333"><a name="p166094416333"></a><a name="p166094416333"></a>带过滤的khop查询执行失败</p>
</td>
<td class="cellrowborder" valign="top" width="42.32423242324232%" headers="mcps1.2.5.1.4 "><p id="p644710528535"><a name="p644710528535"></a><a name="p644710528535"></a>根据errorMessage查看错误信息</p>
</td>
</tr>
</tbody>
</table>


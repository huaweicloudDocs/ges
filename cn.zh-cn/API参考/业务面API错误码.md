# 业务面API错误码<a name="ges_03_0110"></a>

调用接口出错后，将不会返回结果数据。调用方可根据每个接口对应的错误码来定位错误原因。当调用出错时，HTTP 请求返回一个 4xx 或 5xx 的 HTTP 状态码。返回的消息体中是具体的错误代码及错误信息。在调用方找不到错误原因时，可以联系技术人员，并提供错误码，以便我们尽快帮您解决问题。

当您调用API时，如果遇到“APIGW”开头的错误码，请参见[API网关错误码](https://support.huaweicloud.com/devg-apisign/api-sign-errorcode.html)进行处理。

**表 1**  错误码

<a name="zh-cn_topic_0094388422_table13150194944219"></a>
<table><thead align="left"><tr id="zh-cn_topic_0094388422_row1515018490427"><th class="cellrowborder" valign="top" width="9.79097909790979%" id="mcps1.2.6.1.1"><p id="zh-cn_topic_0094388422_p215064994216"><a name="zh-cn_topic_0094388422_p215064994216"></a><a name="zh-cn_topic_0094388422_p215064994216"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="11.29112911291129%" id="mcps1.2.6.1.2"><p id="zh-cn_topic_0094388422_p12150749164219"><a name="zh-cn_topic_0094388422_p12150749164219"></a><a name="zh-cn_topic_0094388422_p12150749164219"></a>错误码</p>
</th>
<th class="cellrowborder" valign="top" width="21.42214221422142%" id="mcps1.2.6.1.3"><p id="p71608211557"><a name="p71608211557"></a><a name="p71608211557"></a>错误信息</p>
</th>
<th class="cellrowborder" valign="top" width="18.591859185918594%" id="mcps1.2.6.1.4"><p id="zh-cn_topic_0094388422_p151501049144216"><a name="zh-cn_topic_0094388422_p151501049144216"></a><a name="zh-cn_topic_0094388422_p151501049144216"></a>描述</p>
</th>
<th class="cellrowborder" valign="top" width="38.90389038903891%" id="mcps1.2.6.1.5"><p id="zh-cn_topic_0094388422_p1715010494422"><a name="zh-cn_topic_0094388422_p1715010494422"></a><a name="zh-cn_topic_0094388422_p1715010494422"></a>处理措施</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0094388422_row16150144924212"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="zh-cn_topic_0094388422_p9899922144317"><a name="zh-cn_topic_0094388422_p9899922144317"></a><a name="zh-cn_topic_0094388422_p9899922144317"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="zh-cn_topic_0094388422_p7899102218438"><a name="zh-cn_topic_0094388422_p7899102218438"></a><a name="zh-cn_topic_0094388422_p7899102218438"></a>GES.8000</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="en-us_topic_0094388422_p12899822164320"><a name="en-us_topic_0094388422_p12899822164320"></a><a name="en-us_topic_0094388422_p12899822164320"></a>Incorrect parameter format.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="zh-cn_topic_0094388422_p12899822164320"><a name="zh-cn_topic_0094388422_p12899822164320"></a><a name="zh-cn_topic_0094388422_p12899822164320"></a>参数格式错误</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p1773119171318"><a name="p1773119171318"></a><a name="p1773119171318"></a>检查请求body体是否和文档描述一致。</p>
</td>
</tr>
<tr id="row89083222129"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p7908162231217"><a name="p7908162231217"></a><a name="p7908162231217"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p390892219123"><a name="p390892219123"></a><a name="p390892219123"></a>GES.8001</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p123163429562"><a name="p123163429562"></a><a name="p123163429562"></a>Failed to query graph statistics.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p6909192241214"><a name="p6909192241214"></a><a name="p6909192241214"></a>图统计信息查询失败</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol15187639184417"></a><a name="ol15187639184417"></a><ol id="ol15187639184417"><li>网络波动问题建议重试下。</li><li>若继续失败，则根据errorMessage查看错误信息联系技术支持人员。</li></ol>
</td>
</tr>
<tr id="row19985113131515"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p13985513171516"><a name="p13985513171516"></a><a name="p13985513171516"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p179852133159"><a name="p179852133159"></a><a name="p179852133159"></a>GES.8002</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p1131624218561"><a name="p1131624218561"></a><a name="p1131624218561"></a>Graph statistics query error.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p6708830141516"><a name="p6708830141516"></a><a name="p6708830141516"></a>图统计信息查询错误</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol881393822816"></a><a name="ol881393822816"></a><ol id="ol881393822816"><li>检查token是否过期，重新获取token。</li><li>若继续失败，则根据errorMessage查看错误信息联系技术支持人员。</li></ol>
</td>
</tr>
<tr id="row4132182112176"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p111328213172"><a name="p111328213172"></a><a name="p111328213172"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p141331621121720"><a name="p141331621121720"></a><a name="p141331621121720"></a>GES.8005</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p73161842135614"><a name="p73161842135614"></a><a name="p73161842135614"></a>Incorrect parameter.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p7133221131713"><a name="p7133221131713"></a><a name="p7133221131713"></a>参数错误</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol440911188910"></a><a name="ol440911188910"></a><ol id="ol440911188910"><li>检查URL中的project_id是否正确。</li><li>检查请求头是否正确，比如X-Auth-Token是否正确。</li></ol>
</td>
</tr>
<tr id="row2016784061915"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p71670402192"><a name="p71670402192"></a><a name="p71670402192"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p316764031919"><a name="p316764031919"></a><a name="p316764031919"></a>GES.8006</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p183166421567"><a name="p183166421567"></a><a name="p183166421567"></a>Invalid resource access.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p1992212802015"><a name="p1992212802015"></a><a name="p1992212802015"></a>资源访问不合法</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p11671240131914"><a name="p11671240131914"></a><a name="p11671240131914"></a>检查URL中的project_id是否正确。</p>
</td>
</tr>
<tr id="row18306135312015"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p1730605342019"><a name="p1730605342019"></a><a name="p1730605342019"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p13306135312208"><a name="p13306135312208"></a><a name="p13306135312208"></a>GES.8007</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p19316174245618"><a name="p19316174245618"></a><a name="p19316174245618"></a>Invalid token.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p1230614531204"><a name="p1230614531204"></a><a name="p1230614531204"></a>Token不合法</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p63061953142010"><a name="p63061953142010"></a><a name="p63061953142010"></a>检查Token是否正确。</p>
</td>
</tr>
<tr id="row1615413582117"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p141548356215"><a name="p141548356215"></a><a name="p141548356215"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p71552352213"><a name="p71552352213"></a><a name="p71552352213"></a>GES.8008</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p131610426566"><a name="p131610426566"></a><a name="p131610426566"></a>An error occurs in the underlying authentication system.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p1115514358212"><a name="p1115514358212"></a><a name="p1115514358212"></a>底层认证系统出错</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p775014388227"><a name="p775014388227"></a><a name="p775014388227"></a>请稍后重试或联系技术支持人员。</p>
</td>
</tr>
<tr id="row951375522214"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p15513105562216"><a name="p15513105562216"></a><a name="p15513105562216"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p18513455162214"><a name="p18513455162214"></a><a name="p18513455162214"></a>GES.8011</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p1031684216568"><a name="p1031684216568"></a><a name="p1031684216568"></a>Failed to export a graph.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p165081667245"><a name="p165081667245"></a><a name="p165081667245"></a>导出图失败</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol660693513211"></a><a name="ol660693513211"></a><ol id="ol660693513211"><li>检查图名是否正确。</li><li>查看导出文件路径是否正确。</li><li>检查该账号有无OBS写入权限。</li></ol>
</td>
</tr>
<tr id="row312815239241"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p13128323172415"><a name="p13128323172415"></a><a name="p13128323172415"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p14128523172411"><a name="p14128523172411"></a><a name="p14128523172411"></a>GES.8012</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p123169425567"><a name="p123169425567"></a><a name="p123169425567"></a>Failed to clear a graph.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p11129823172413"><a name="p11129823172413"></a><a name="p11129823172413"></a>清空图失败</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol1829135711429"></a><a name="ol1829135711429"></a><ol id="ol1829135711429"><li>网络波动问题建议重试下。</li><li>若继续失败，则根据errorMessage查看错误信息联系技术支持人员。</li></ol>
</td>
</tr>
<tr id="row5593445122411"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p6593445162416"><a name="p6593445162416"></a><a name="p6593445162416"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p12593745102414"><a name="p12593745102414"></a><a name="p12593745102414"></a>GES.8013</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p2316542155613"><a name="p2316542155613"></a><a name="p2316542155613"></a>Failed to incrementally import data to the graph.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p2593114542411"><a name="p2593114542411"></a><a name="p2593114542411"></a>增量导入图失败</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol20596227164317"></a><a name="ol20596227164317"></a><ol id="ol20596227164317"><li>网络波动问题建议重试下。</li><li>若继续失败，则根据errorMessage查看错误信息联系技术支持人员。</li></ol>
</td>
</tr>
<tr id="row99191333124417"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p1192003310445"><a name="p1192003310445"></a><a name="p1192003310445"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p4920933154415"><a name="p4920933154415"></a><a name="p4920933154415"></a>GES.8020</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p16921103313448"><a name="p16921103313448"></a><a name="p16921103313448"></a>The current user does not have permission.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p4921933104415"><a name="p4921933104415"></a><a name="p4921933104415"></a>（细粒度授权时）当前用户没权限</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p7892310552"><a name="p7892310552"></a><a name="p7892310552"></a>使用具有Security Administrator权限的用户进行授权。</p>
</td>
</tr>
<tr id="row192021274513"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p120211264514"><a name="p120211264514"></a><a name="p120211264514"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p112021527457"><a name="p112021527457"></a><a name="p112021527457"></a>GES.8101</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p183161642105616"><a name="p183161642105616"></a><a name="p183161642105616"></a>Invalid filter criteria for edge queries.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p59142419469"><a name="p59142419469"></a><a name="p59142419469"></a>边过滤查询条件不合法</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p720219220451"><a name="p720219220451"></a><a name="p720219220451"></a>检查边过滤条件格式是否正确。</p>
</td>
</tr>
<tr id="row19241681083"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p1892415820814"><a name="p1892415820814"></a><a name="p1892415820814"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p7924198585"><a name="p7924198585"></a><a name="p7924198585"></a>GES.8102</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p15316114214563"><a name="p15316114214563"></a><a name="p15316114214563"></a>Invalid label for edge filtering queries.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p11924281987"><a name="p11924281987"></a><a name="p11924281987"></a>边过滤查询Label不合法</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p03411153172418"><a name="p03411153172418"></a><a name="p03411153172418"></a>检查labels是不是正常的josn体。</p>
</td>
</tr>
<tr id="row1494216520912"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p199431515914"><a name="p199431515914"></a><a name="p199431515914"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p13943452915"><a name="p13943452915"></a><a name="p13943452915"></a>GES.8103</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p173171242155611"><a name="p173171242155611"></a><a name="p173171242155611"></a>Both the condition and label of edge filtering queries are empty.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p17943451096"><a name="p17943451096"></a><a name="p17943451096"></a>边过滤查询条件和Label同时为空</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p193581572101"><a name="p193581572101"></a><a name="p193581572101"></a>边过滤查询条件和Label不能同时为空。</p>
</td>
</tr>
<tr id="row432610186101"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p432671814103"><a name="p432671814103"></a><a name="p432671814103"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p18326151817109"><a name="p18326151817109"></a><a name="p18326151817109"></a>GES.8104</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p5317104275610"><a name="p5317104275610"></a><a name="p5317104275610"></a>Invalid edge filtering query sequence.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p032651813102"><a name="p032651813102"></a><a name="p032651813102"></a>边过滤排序输入不合法</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p18326618121020"><a name="p18326618121020"></a><a name="p18326618121020"></a>检查边过滤排序输入是否合法。</p>
</td>
</tr>
<tr id="row14136142131115"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p6771123991719"><a name="p6771123991719"></a><a name="p6771123991719"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p913764221112"><a name="p913764221112"></a><a name="p913764221112"></a>GES.8105</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p1131717428561"><a name="p1131717428561"></a><a name="p1131717428561"></a>Failed to query edges that meet filter criteria.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p12137842191110"><a name="p12137842191110"></a><a name="p12137842191110"></a>边过滤查询执行失败</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol83731742104419"></a><a name="ol83731742104419"></a><ol id="ol83731742104419"><li>网络波动问题建议重试下。</li><li>若继续失败，则根据errorMessage查看错误信息联系技术支持人员。</li></ol>
</td>
</tr>
<tr id="row52115259122"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p1380493916174"><a name="p1380493916174"></a><a name="p1380493916174"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p15211125131212"><a name="p15211125131212"></a><a name="p15211125131212"></a>GES.8106</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p231774216561"><a name="p231774216561"></a><a name="p231774216561"></a>The source vertex or target vertex in the edge details is empty.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p13211225131214"><a name="p13211225131214"></a><a name="p13211225131214"></a>边详情起点或终点为空</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p92113253122"><a name="p92113253122"></a><a name="p92113253122"></a>边详情起点和终点不能为空。</p>
</td>
</tr>
<tr id="row8158185461218"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p1281114393179"><a name="p1281114393179"></a><a name="p1281114393179"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p20143181016138"><a name="p20143181016138"></a><a name="p20143181016138"></a>GES.8107</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p1731764218566"><a name="p1731764218566"></a><a name="p1731764218566"></a>Failed to query edge details.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p131431910191313"><a name="p131431910191313"></a><a name="p131431910191313"></a>边详情查询失败</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol109214499441"></a><a name="ol109214499441"></a><ol id="ol109214499441"><li>网络波动问题建议重试下。</li><li>若继续失败，则根据errorMessage查看错误信息联系技术支持人员。</li></ol>
</td>
</tr>
<tr id="row618615578124"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p17821183915172"><a name="p17821183915172"></a><a name="p17821183915172"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p17900145617132"><a name="p17900145617132"></a><a name="p17900145617132"></a>GES.8108</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p231711424565"><a name="p231711424565"></a><a name="p231711424565"></a>Edge details query error.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p149001056141311"><a name="p149001056141311"></a><a name="p149001056141311"></a>边详情查询内部错误</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p924695614316"><a name="p924695614316"></a><a name="p924695614316"></a>请稍后重试或联系技术人员。</p>
</td>
</tr>
<tr id="row14620111421313"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p883143951718"><a name="p883143951718"></a><a name="p883143951718"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p1255416514147"><a name="p1255416514147"></a><a name="p1255416514147"></a>GES.8109</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p15317642185615"><a name="p15317642185615"></a><a name="p15317642185615"></a>Invalid edge filtering query operator.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p6554151151416"><a name="p6554151151416"></a><a name="p6554151151416"></a>边过滤查询算子不合法</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p1262001419135"><a name="p1262001419135"></a><a name="p1262001419135"></a>边过滤查询算子取值为 in、out、both、edge。</p>
</td>
</tr>
<tr id="row103557185134"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p484233901712"><a name="p484233901712"></a><a name="p484233901712"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p035516184139"><a name="p035516184139"></a><a name="p035516184139"></a>GES.8110</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p931719425564"><a name="p931719425564"></a><a name="p931719425564"></a>Parameter edges cannot be left blank.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p1355718171317"><a name="p1355718171317"></a><a name="p1355718171317"></a>参数edges不能为空</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p18418152794813"><a name="p18418152794813"></a><a name="p18418152794813"></a>批量边查询请求体中edges是否为空。</p>
</td>
</tr>
<tr id="row829042151315"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p1985414391174"><a name="p1985414391174"></a><a name="p1985414391174"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p9827253173"><a name="p9827253173"></a><a name="p9827253173"></a>GES.8201</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p431814235615"><a name="p431814235615"></a><a name="p431814235615"></a>Invalid label for vertex filtering queries.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p882819591718"><a name="p882819591718"></a><a name="p882819591718"></a>点过滤查询Label不合法</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p83523144250"><a name="p83523144250"></a><a name="p83523144250"></a>检查labels是不是正常的josn体。</p>
</td>
</tr>
<tr id="row26231127131315"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p6864153961719"><a name="p6864153961719"></a><a name="p6864153961719"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p128285510175"><a name="p128285510175"></a><a name="p128285510175"></a>GES.8202</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p2318154215561"><a name="p2318154215561"></a><a name="p2318154215561"></a>Invalid filter criteria for vertex queries.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p1282865131716"><a name="p1282865131716"></a><a name="p1282865131716"></a>点过滤查询条件不合法</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol9667192784514"></a><a name="ol9667192784514"></a><ol id="ol9667192784514"><li>检查点过滤查询API中propertyName（属性名称）是否为空。</li><li>检查点过滤查询API中values（属性值）是否为空。</li><li>若继续失败，则根据errorMessage查看错误信息联系技术支持人员。</li></ol>
</td>
</tr>
<tr id="row78431524111316"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p98701639121716"><a name="p98701639121716"></a><a name="p98701639121716"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p88281553178"><a name="p88281553178"></a><a name="p88281553178"></a>GES.8203</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p7318184295612"><a name="p7318184295612"></a><a name="p7318184295612"></a>Both the condition and label of vertex filtering queries are empty.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p582817551713"><a name="p582817551713"></a><a name="p582817551713"></a>点过滤查询条件和Label同时为空</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p084472481316"><a name="p084472481316"></a><a name="p084472481316"></a>点过滤条件和Label不能同时为空。</p>
</td>
</tr>
<tr id="row5618193041318"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p15880203913178"><a name="p15880203913178"></a><a name="p15880203913178"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p178282514179"><a name="p178282514179"></a><a name="p178282514179"></a>GES.8204</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p3318242145615"><a name="p3318242145615"></a><a name="p3318242145615"></a>Failed to query vertices that meet filter criteria.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p14828165161710"><a name="p14828165161710"></a><a name="p14828165161710"></a>点过滤查询执行失败</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol144661826124611"></a><a name="ol144661826124611"></a><ol id="ol144661826124611"><li>网络波动问题建议重试下。</li><li>若继续失败，则根据errorMessage查看错误信息联系技术支持人员。</li></ol>
</td>
</tr>
<tr id="row1437743314135"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p1310743121714"><a name="p1310743121714"></a><a name="p1310743121714"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p9828258171"><a name="p9828258171"></a><a name="p9828258171"></a>GES.8205</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p631844213569"><a name="p631844213569"></a><a name="p631844213569"></a>Invalid vertex filtering query sequence.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p128299521710"><a name="p128299521710"></a><a name="p128299521710"></a>点过滤排序输入不合法</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p1736116544394"><a name="p1736116544394"></a><a name="p1736116544394"></a>点过滤查询API中orderValue必须在“incr”和“decr”。</p>
</td>
</tr>
<tr id="row1555736171312"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p133239430178"><a name="p133239430178"></a><a name="p133239430178"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p2082911517178"><a name="p2082911517178"></a><a name="p2082911517178"></a>GES.8206</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p831844215611"><a name="p831844215611"></a><a name="p831844215611"></a>Both vertexid and vertextids exist.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p3829458172"><a name="p3829458172"></a><a name="p3829458172"></a>vertexid和vertextids同时存在</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p18491130164320"><a name="p18491130164320"></a><a name="p18491130164320"></a>vertexid和vertextids不能同时存在。</p>
</td>
</tr>
<tr id="row845174411318"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p1233614312177"><a name="p1233614312177"></a><a name="p1233614312177"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p1282925141712"><a name="p1282925141712"></a><a name="p1282925141712"></a>GES.8207</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p14318204295615"><a name="p14318204295615"></a><a name="p14318204295615"></a>Both vertexid and vertextids are empty.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p198295518171"><a name="p198295518171"></a><a name="p198295518171"></a>vertexid和vertextids同时为空</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p649183024310"><a name="p649183024310"></a><a name="p649183024310"></a>vertexid或vertextids为空。</p>
</td>
</tr>
<tr id="row38531147131313"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p19344243121713"><a name="p19344243121713"></a><a name="p19344243121713"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p11829450171"><a name="p11829450171"></a><a name="p11829450171"></a>GES.8208</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p3319134215617"><a name="p3319134215617"></a><a name="p3319134215617"></a>Incorrect vertextids format.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p382955131714"><a name="p382955131714"></a><a name="p382955131714"></a>vertextids格式错误</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p08533472137"><a name="p08533472137"></a><a name="p08533472137"></a>vertextids是否 json array。</p>
</td>
</tr>
<tr id="row146491840161311"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p103571243141713"><a name="p103571243141713"></a><a name="p103571243141713"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p15829557176"><a name="p15829557176"></a><a name="p15829557176"></a>GES.8209</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p831914427562"><a name="p831914427562"></a><a name="p831914427562"></a>Failed to query vertex details.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p198291754175"><a name="p198291754175"></a><a name="p198291754175"></a>点详情查询失败</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p6751916173313"><a name="p6751916173313"></a><a name="p6751916173313"></a>检查图名是否存在。</p>
</td>
</tr>
<tr id="row43583141716"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p6366194311172"><a name="p6366194311172"></a><a name="p6366194311172"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p198301457175"><a name="p198301457175"></a><a name="p198301457175"></a>GES.8210</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p123191742175616"><a name="p123191742175616"></a><a name="p123191742175616"></a>Vertex details query error.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p138301656170"><a name="p138301656170"></a><a name="p138301656170"></a>点详情查询内部错误</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p48905208396"><a name="p48905208396"></a><a name="p48905208396"></a>请稍后重试或联系技术支持人员。</p>
</td>
</tr>
<tr id="row17606656121719"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p673832187"><a name="p673832187"></a><a name="p673832187"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p3733391820"><a name="p3733391820"></a><a name="p3733391820"></a>GES.8211</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p73221242175611"><a name="p73221242175611"></a><a name="p73221242175611"></a>Invalid vertex filtering query operator.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p17738311188"><a name="p17738311188"></a><a name="p17738311188"></a>点过滤查询算子不合法</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p160655618171"><a name="p160655618171"></a><a name="p160655618171"></a>点过滤查询算子取值为 inV、outV、bothV、vertex。</p>
</td>
</tr>
<tr id="row330803061811"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p29501634171819"><a name="p29501634171819"></a><a name="p29501634171819"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p1495014347183"><a name="p1495014347183"></a><a name="p1495014347183"></a>GES.8212</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p5322124235612"><a name="p5322124235612"></a><a name="p5322124235612"></a>Failed to delete the vertex label.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p15950334101818"><a name="p15950334101818"></a><a name="p15950334101818"></a>删除点Label失败</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p63081430101812"><a name="p63081430101812"></a><a name="p63081430101812"></a>Label是否存在。</p>
</td>
</tr>
<tr id="row02253204196"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p7691144951914"><a name="p7691144951914"></a><a name="p7691144951914"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p569114981917"><a name="p569114981917"></a><a name="p569114981917"></a>GES.8213</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p8323154217562"><a name="p8323154217562"></a><a name="p8323154217562"></a>Failed to add the vertex label.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p569164911910"><a name="p569164911910"></a><a name="p569164911910"></a>增加点Label失败</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p1422532051915"><a name="p1422532051915"></a><a name="p1422532051915"></a>Label是否存在。</p>
</td>
</tr>
<tr id="row1832617717208"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p7716201017207"><a name="p7716201017207"></a><a name="p7716201017207"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p3716111010202"><a name="p3716111010202"></a><a name="p3716111010202"></a>GES.8214</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p193231042175615"><a name="p193231042175615"></a><a name="p193231042175615"></a>Parameter vertices cannot be left blank.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p16716610132017"><a name="p16716610132017"></a><a name="p16716610132017"></a>参数vertices不能空</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p11326107182012"><a name="p11326107182012"></a><a name="p11326107182012"></a>批量点查询请求体中vertices是否为空。</p>
</td>
</tr>
<tr id="row1911195414206"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p19112125472013"><a name="p19112125472013"></a><a name="p19112125472013"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p63647166212"><a name="p63647166212"></a><a name="p63647166212"></a>GES.8220</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p163233428566"><a name="p163233428566"></a><a name="p163233428566"></a>Failed to update the vertex properties.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p143651916112112"><a name="p143651916112112"></a><a name="p143651916112112"></a>更新点属性失败</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol34087464467"></a><a name="ol34087464467"></a><ol id="ol34087464467"><li>网络波动问题建议重试下。</li><li>若继续失败，则根据errorMessage查看错误信息联系技术支持人员。</li></ol>
</td>
</tr>
<tr id="row151511482211"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p2086485310210"><a name="p2086485310210"></a><a name="p2086485310210"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p13864165314213"><a name="p13864165314213"></a><a name="p13864165314213"></a>GES.8221</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p1932374215565"><a name="p1932374215565"></a><a name="p1932374215565"></a>Failed to update the edge properties.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p7865195312213"><a name="p7865195312213"></a><a name="p7865195312213"></a>更新边属性失败</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol1868175216464"></a><a name="ol1868175216464"></a><ol id="ol1868175216464"><li>网络波动问题建议重试下。</li><li>若继续失败，则根据errorMessage查看错误信息联系技术支持人员。</li></ol>
</td>
</tr>
<tr id="row161951613122218"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p1519511362216"><a name="p1519511362216"></a><a name="p1519511362216"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p9122164332219"><a name="p9122164332219"></a><a name="p9122164332219"></a>GES.8301</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p2032344210562"><a name="p2032344210562"></a><a name="p2032344210562"></a>Failed to query a job.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p1712274322215"><a name="p1712274322215"></a><a name="p1712274322215"></a>作业查询失败</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol9986175894614"></a><a name="ol9986175894614"></a><ol id="ol9986175894614"><li>网络波动问题建议重试下。</li><li>若继续失败，则根据errorMessage查看错误信息联系技术支持人员。</li></ol>
</td>
</tr>
<tr id="row7775133117224"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p843215364287"><a name="p843215364287"></a><a name="p843215364287"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p1512264314227"><a name="p1512264314227"></a><a name="p1512264314227"></a>GES.8302</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p1932314205614"><a name="p1932314205614"></a><a name="p1932314205614"></a>Job query error.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p31224439222"><a name="p31224439222"></a><a name="p31224439222"></a>作业查询内部错误</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p4830111513913"><a name="p4830111513913"></a><a name="p4830111513913"></a>请稍后重试或联系技术支持人员。</p>
</td>
</tr>
<tr id="row1794183618222"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p1472123616282"><a name="p1472123616282"></a><a name="p1472123616282"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p41229430222"><a name="p41229430222"></a><a name="p41229430222"></a>GES.8303</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p143234427569"><a name="p143234427569"></a><a name="p143234427569"></a>Failed to terminate a job.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p10122154392210"><a name="p10122154392210"></a><a name="p10122154392210"></a>作业终止失败</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol386443194717"></a><a name="ol386443194717"></a><ol id="ol386443194717"><li>网络波动问题建议重试下。</li><li>若继续失败，则根据errorMessage查看错误信息联系技术支持人员。</li></ol>
</td>
</tr>
<tr id="row612010395228"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p748843632814"><a name="p748843632814"></a><a name="p748843632814"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p171222043192210"><a name="p171222043192210"></a><a name="p171222043192210"></a>GES.8304</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p12324164216569"><a name="p12324164216569"></a><a name="p12324164216569"></a>Job termination error.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p912219435226"><a name="p912219435226"></a><a name="p912219435226"></a>作业终止内部错误</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p1237951713917"><a name="p1237951713917"></a><a name="p1237951713917"></a>请稍后重试或联系技术支持人员。</p>
</td>
</tr>
<tr id="row148531875236"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p250318367285"><a name="p250318367285"></a><a name="p250318367285"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p5551482417"><a name="p5551482417"></a><a name="p5551482417"></a>GES.8401</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p632416424562"><a name="p632416424562"></a><a name="p632416424562"></a>The algorithm or graph name cannot be empty.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p1362142247"><a name="p1362142247"></a><a name="p1362142247"></a>算法名或者图名不能为空</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p685311772317"><a name="p685311772317"></a><a name="p685311772317"></a>算法名或者图名不能为空。</p>
</td>
</tr>
<tr id="row24185116237"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p165142360287"><a name="p165142360287"></a><a name="p165142360287"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p13611411246"><a name="p13611411246"></a><a name="p13611411246"></a>GES.8402</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p18324134212564"><a name="p18324134212564"></a><a name="p18324134212564"></a>Failed to run the algorithm.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p1163145244"><a name="p1163145244"></a><a name="p1163145244"></a>算法执行失败</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol1643072119489"></a><a name="ol1643072119489"></a><ol id="ol1643072119489"><li>网络波动问题建议重试下。</li><li>检查执行算法API图名是否填写正确。</li><li>若继续失败，则根据errorMessage查看错误信息联系技术支持人员。</li></ol>
</td>
</tr>
<tr id="row93248147238"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p9526143619289"><a name="p9526143619289"></a><a name="p9526143619289"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p16631410248"><a name="p16631410248"></a><a name="p16631410248"></a>GES.8403</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p10324842165616"><a name="p10324842165616"></a><a name="p10324842165616"></a>Algorithm running error.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p19651417241"><a name="p19651417241"></a><a name="p19651417241"></a>算法执行内部错误</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p07249147397"><a name="p07249147397"></a><a name="p07249147397"></a>请稍后重试或联系技术支持人员。</p>
</td>
</tr>
<tr id="row248616179234"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p14538133615286"><a name="p14538133615286"></a><a name="p14538133615286"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p795011299244"><a name="p795011299244"></a><a name="p795011299244"></a>GES.8404</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p4324842165620"><a name="p4324842165620"></a><a name="p4324842165620"></a>Invalid algorithm running format.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p69501229122413"><a name="p69501229122413"></a><a name="p69501229122413"></a>算法执行模式不合法</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol1489412734911"></a><a name="ol1489412734911"></a><ol id="ol1489412734911"><li>网络波动问题建议重试下。</li><li>若继续失败，则根据errorMessage查看错误信息联系技术支持人员。</li></ol>
</td>
</tr>
<tr id="row5153477248"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p5552133622820"><a name="p5552133622820"></a><a name="p5552133622820"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p20772734112512"><a name="p20772734112512"></a><a name="p20772734112512"></a>GES.8501</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p193241342115615"><a name="p193241342115615"></a><a name="p193241342115615"></a>The Gremlin command is not supported.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p377263419251"><a name="p377263419251"></a><a name="p377263419251"></a>Gremlin查询命令不支持</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p13151475247"><a name="p13151475247"></a><a name="p13151475247"></a>不支持Gremlin的tryNext、explain、tree语句。</p>
</td>
</tr>
<tr id="row1155651418258"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p356253619289"><a name="p356253619289"></a><a name="p356253619289"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p1477223472512"><a name="p1477223472512"></a><a name="p1477223472512"></a>GES.8502</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p332404214564"><a name="p332404214564"></a><a name="p332404214564"></a>Failed to find the Gremlin configuration file.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p147721634162510"><a name="p147721634162510"></a><a name="p147721634162510"></a>Gremlin配置文件找不到</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p7557114172517"><a name="p7557114172517"></a><a name="p7557114172517"></a>请稍后重试或联系技术支持人员。</p>
</td>
</tr>
<tr id="row16589717182517"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p1157653602819"><a name="p1157653602819"></a><a name="p1157653602819"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p177223414251"><a name="p177223414251"></a><a name="p177223414251"></a>GES.8503</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p1325124216560"><a name="p1325124216560"></a><a name="p1325124216560"></a>Gremlin query failed.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p11772133482515"><a name="p11772133482515"></a><a name="p11772133482515"></a>Gremlin查询执行失败</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol51723316499"></a><a name="ol51723316499"></a><ol id="ol51723316499"><li>网络波动问题建议重试下。</li><li>若继续失败，则根据errorMessage查看错误信息联系技术支持人员。</li></ol>
</td>
</tr>
<tr id="row52671522182510"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p3591036172818"><a name="p3591036172818"></a><a name="p3591036172818"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p1772173417256"><a name="p1772173417256"></a><a name="p1772173417256"></a>GES.8504</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p163251442185617"><a name="p163251442185617"></a><a name="p163251442185617"></a>Gremlin query error.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p1677219340258"><a name="p1677219340258"></a><a name="p1677219340258"></a>Gremlin查询内部错误</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p191213110531"><a name="p191213110531"></a><a name="p191213110531"></a>请稍后重试或联系技术支持人员。</p>
</td>
</tr>
<tr id="row12438162562511"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p7606236132817"><a name="p7606236132817"></a><a name="p7606236132817"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p1081625420259"><a name="p1081625420259"></a><a name="p1081625420259"></a>GES.8505</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p3325164295611"><a name="p3325164295611"></a><a name="p3325164295611"></a>The Gremlin query statement does not contain the command field.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p1981625410256"><a name="p1981625410256"></a><a name="p1981625410256"></a>Gremlin查询语句没有command字段</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p19438142532517"><a name="p19438142532517"></a><a name="p19438142532517"></a>Gremlin查询语句没有command字段。</p>
</td>
</tr>
<tr id="row8606133032511"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p46214366286"><a name="p46214366286"></a><a name="p46214366286"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p1592195813259"><a name="p1592195813259"></a><a name="p1592195813259"></a>GES.8506</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p0325142185619"><a name="p0325142185619"></a><a name="p0325142185619"></a>The size of the Gremlin query request statements exceeds the upper limit.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p1759345817251"><a name="p1759345817251"></a><a name="p1759345817251"></a>Gremlin查询请求语句超过限制</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p06071730132520"><a name="p06071730132520"></a><a name="p06071730132520"></a>当前限制为64MB。</p>
</td>
</tr>
<tr id="row1541334142720"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p1641314482719"><a name="p1641314482719"></a><a name="p1641314482719"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p1326811164274"><a name="p1326811164274"></a><a name="p1326811164274"></a>GES.8601</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p13251642105612"><a name="p13251642105612"></a><a name="p13251642105612"></a>Gremlin service unavailable.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p14268131619277"><a name="p14268131619277"></a><a name="p14268131619277"></a>Gremlin服务不可用</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p841312414276"><a name="p841312414276"></a><a name="p841312414276"></a>请稍后重试或联系技术支持人员。</p>
</td>
</tr>
<tr id="row2055659152716"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p7556189172713"><a name="p7556189172713"></a><a name="p7556189172713"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p11268191618274"><a name="p11268191618274"></a><a name="p11268191618274"></a>GES.8602</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p20325194213565"><a name="p20325194213565"></a><a name="p20325194213565"></a>Engine service unavailable.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p1726891610270"><a name="p1726891610270"></a><a name="p1726891610270"></a>Engine服务不可用</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p1939024133914"><a name="p1939024133914"></a><a name="p1939024133914"></a>请稍后重试或联系技术支持人员。</p>
</td>
</tr>
<tr id="row1871081342917"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p14710313132913"><a name="p14710313132913"></a><a name="p14710313132913"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p4710151315297"><a name="p4710151315297"></a><a name="p4710151315297"></a>GES.8603</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p53257421563"><a name="p53257421563"></a><a name="p53257421563"></a>Failed to create an index</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p1471001342914"><a name="p1471001342914"></a><a name="p1471001342914"></a>索引创建失败</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol381220100501"></a><a name="ol381220100501"></a><ol id="ol381220100501"><li>检查索引名称是否只包含字母,数字,-和_。</li><li>检查索引参数类型是否符合GES API规定的格式。</li></ol>
</td>
</tr>
<tr id="row21651516113014"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p1674521163012"><a name="p1674521163012"></a><a name="p1674521163012"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p8674192173010"><a name="p8674192173010"></a><a name="p8674192173010"></a>GES.8604</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p1532624219569"><a name="p1532624219569"></a><a name="p1532624219569"></a>Failed to delete an index</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p2067482119301"><a name="p2067482119301"></a><a name="p2067482119301"></a>索引删除失败</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol861822614150"></a><a name="ol861822614150"></a><ol id="ol861822614150"><li>检查图名是否填写正确。</li><li>检查索引名称是否填写正确。</li><li>检查请求Method type是否为delete。</li></ol>
</td>
</tr>
<tr id="row3139537193016"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p191391337123015"><a name="p191391337123015"></a><a name="p191391337123015"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p1998654218301"><a name="p1998654218301"></a><a name="p1998654218301"></a>GES.8605</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p1232615428561"><a name="p1232615428561"></a><a name="p1232615428561"></a>Failed to query an index</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p613953783013"><a name="p613953783013"></a><a name="p613953783013"></a>索引查询失败</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol13449723195111"></a><a name="ol13449723195111"></a><ol id="ol13449723195111"><li>网络波动问题建议重试下。</li><li>若继续失败，则根据errorMessage查看错误信息联系技术支持人员。</li></ol>
</td>
</tr>
<tr id="row1023983312313"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p01221527375"><a name="p01221527375"></a><a name="p01221527375"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p1323963314311"><a name="p1323963314311"></a><a name="p1323963314311"></a>GES.8609</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p18326134215616"><a name="p18326134215616"></a><a name="p18326134215616"></a>The request body for querying path details is invalid.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p10239113317316"><a name="p10239113317316"></a><a name="p10239113317316"></a>查询路径详情请求体不合法</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol586717411519"></a><a name="ol586717411519"></a><ol id="ol586717411519"><li>检查图名是否填写正确。</li><li>检查查询路径详情API参数格式是否填写正确。</li><li>若继续失败，则根据errorMessage查看错误信息联系技术支持人员。</li></ol>
</td>
</tr>
<tr id="row106361238203115"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p9138552153712"><a name="p9138552153712"></a><a name="p9138552153712"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p563610389317"><a name="p563610389317"></a><a name="p563610389317"></a>GES.8610</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p1326742175612"><a name="p1326742175612"></a><a name="p1326742175612"></a>The path parameter of the request body for querying path details is invalid.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p963693811315"><a name="p963693811315"></a><a name="p963693811315"></a>查询路径详情请求体path参数不合法</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol096222020175"></a><a name="ol096222020175"></a><ol id="ol096222020175"><li>检查查询路径详情API参数格式是否填写正确。</li><li>检查查询路径详情API必选参数是否缺失。</li><li>若继续失败，则根据errorMessage查看错误信息联系技术支持人员。</li></ol>
</td>
</tr>
<tr id="row4717341103115"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p171551452153716"><a name="p171551452153716"></a><a name="p171551452153716"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p271774103112"><a name="p271774103112"></a><a name="p271774103112"></a>GES.8611</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p532654205614"><a name="p532654205614"></a><a name="p532654205614"></a>Failed to query path details.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p1571719413311"><a name="p1571719413311"></a><a name="p1571719413311"></a>查询路径详情失败</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol4615167539"></a><a name="ol4615167539"></a><ol id="ol4615167539"><li>网络波动问题建议重试下。</li><li>若继续失败，则根据errorMessage查看错误信息联系技术支持人员。</li></ol>
</td>
</tr>
<tr id="row1470415462315"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p11168552143718"><a name="p11168552143718"></a><a name="p11168552143718"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p2705194618316"><a name="p2705194618316"></a><a name="p2705194618316"></a>GES.8612</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p15326242135612"><a name="p15326242135612"></a><a name="p15326242135612"></a>The operation of querying path details is not supported.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p770544617314"><a name="p770544617314"></a><a name="p770544617314"></a>查询路径详情操作不支持</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol8721823135315"></a><a name="ol8721823135315"></a><ol id="ol8721823135315"><li>网络波动问题建议重试下。</li><li>若继续失败，则根据errorMessage查看错误信息联系技术支持人员。</li></ol>
</td>
</tr>
<tr id="row1997215431314"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p818415215374"><a name="p818415215374"></a><a name="p818415215374"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p11972154353115"><a name="p11972154353115"></a><a name="p11972154353115"></a>GES.8801</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p2327154225618"><a name="p2327154225618"></a><a name="p2327154225618"></a>Failed to add a label to metadata.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p1497212434311"><a name="p1497212434311"></a><a name="p1497212434311"></a>元数据添加label失败</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol11861952173010"></a><a name="ol11861952173010"></a><ol id="ol11861952173010"><li>检查要添加的label是否已经存在。</li><li>检查添加labelAPI参数格式是否正确。</li><li>检查添加labelAPI必选参数是否都有值。</li></ol>
</td>
</tr>
<tr id="row1146024843210"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p1019775211371"><a name="p1019775211371"></a><a name="p1019775211371"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p12460174843220"><a name="p12460174843220"></a><a name="p12460174843220"></a>GES.8803</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p15327134275618"><a name="p15327134275618"></a><a name="p15327134275618"></a>Failed to query the metadata.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p18460194812325"><a name="p18460194812325"></a><a name="p18460194812325"></a>元数据查询失败</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol1724431785410"></a><a name="ol1724431785410"></a><ol id="ol1724431785410"><li>检查要查询的图是否存在。</li><li>检查查询图元数据详情API的graph_name是否填写正确。</li></ol>
</td>
</tr>
<tr id="row18192754183213"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p201921954153213"><a name="p201921954153213"></a><a name="p201921954153213"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p1919316549322"><a name="p1919316549322"></a><a name="p1919316549322"></a>GES.8804</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p1327042165620"><a name="p1327042165620"></a><a name="p1327042165620"></a>Metadata query error.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p919365403210"><a name="p919365403210"></a><a name="p919365403210"></a>元数据查询内部错误</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><p id="p3676151113390"><a name="p3676151113390"></a><a name="p3676151113390"></a>请稍后重试或联系技术支持人员。</p>
</td>
</tr>
<tr id="row1460815483318"><td class="cellrowborder" valign="top" width="9.79097909790979%" headers="mcps1.2.6.1.1 "><p id="p26097433311"><a name="p26097433311"></a><a name="p26097433311"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="11.29112911291129%" headers="mcps1.2.6.1.2 "><p id="p1560916493316"><a name="p1560916493316"></a><a name="p1560916493316"></a>GES.8806</p>
</td>
<td class="cellrowborder" valign="top" width="21.42214221422142%" headers="mcps1.2.6.1.3 "><p id="p932724213568"><a name="p932724213568"></a><a name="p932724213568"></a>K-Hop query with filter criteria failed.</p>
</td>
<td class="cellrowborder" valign="top" width="18.591859185918594%" headers="mcps1.2.6.1.4 "><p id="p166094416333"><a name="p166094416333"></a><a name="p166094416333"></a>带过滤的khop查询执行失败</p>
</td>
<td class="cellrowborder" valign="top" width="38.90389038903891%" headers="mcps1.2.6.1.5 "><a name="ol163748426546"></a><a name="ol163748426546"></a><ol id="ol163748426546"><li>网络波动问题建议重试下。</li><li>若继续失败，则根据errorMessage查看错误信息联系技术支持人员。</li></ol>
</td>
</tr>
</tbody>
</table>


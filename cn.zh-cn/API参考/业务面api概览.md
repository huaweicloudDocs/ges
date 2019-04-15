# 业务面API概览<a name="ges_03_0003"></a>

## 业务面API概览<a name="section491485815517"></a>

GES业务面API包括点操作相关接口、边操作相关接口、元数据操作相关接口、索引操作相关接口、Gremlin查询相关接口、算法相关接口、图统计相关接口、Job管理相关接口八类。

**表 1**  点操作API

<a name="table7304174193110"></a>
<table><thead align="left"><tr id="row153051646317"><th class="cellrowborder" valign="top" width="5.489999999999999%" id="mcps1.2.6.1.1"><p id="p53050493116"><a name="p53050493116"></a><a name="p53050493116"></a>序号</p>
</th>
<th class="cellrowborder" valign="top" width="8.67%" id="mcps1.2.6.1.2"><p id="p830519413120"><a name="p830519413120"></a><a name="p830519413120"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="5.06%" id="mcps1.2.6.1.3"><p id="p1324346122710"><a name="p1324346122710"></a><a name="p1324346122710"></a>版本</p>
</th>
<th class="cellrowborder" valign="top" width="49.519999999999996%" id="mcps1.2.6.1.4"><p id="p173057463116"><a name="p173057463116"></a><a name="p173057463116"></a>URL</p>
</th>
<th class="cellrowborder" valign="top" width="31.259999999999998%" id="mcps1.2.6.1.5"><p id="p5916189283"><a name="p5916189283"></a><a name="p5916189283"></a>功能描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row530514411314"><td class="cellrowborder" valign="top" width="5.489999999999999%" headers="mcps1.2.6.1.1 "><p id="p1830511418318"><a name="p1830511418318"></a><a name="p1830511418318"></a>1</p>
</td>
<td class="cellrowborder" valign="top" width="8.67%" headers="mcps1.2.6.1.2 "><p id="p6518171521318"><a name="p6518171521318"></a><a name="p6518171521318"></a>点过滤查询</p>
</td>
<td class="cellrowborder" valign="top" width="5.06%" headers="mcps1.2.6.1.3 "><p id="p42514460277"><a name="p42514460277"></a><a name="p42514460277"></a><a href="点过滤查询(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="49.519999999999996%" headers="mcps1.2.6.1.4 "><p id="p18517191513133"><a name="p18517191513133"></a><a name="p18517191513133"></a>POST /ges/v1.0/{projectId}/graphs/{graphName}/vertices/action?action_id=query</p>
</td>
<td class="cellrowborder" valign="top" width="31.259999999999998%" headers="mcps1.2.6.1.5 "><p id="p69160917820"><a name="p69160917820"></a><a name="p69160917820"></a>根据某个过滤条件查询点，比如点元数据中含有age属性，过滤条件可以为age&gt;18。</p>
</td>
</tr>
<tr id="row23061417313"><td class="cellrowborder" valign="top" width="5.489999999999999%" headers="mcps1.2.6.1.1 "><p id="p430619413315"><a name="p430619413315"></a><a name="p430619413315"></a>2</p>
</td>
<td class="cellrowborder" valign="top" width="8.67%" headers="mcps1.2.6.1.2 "><p id="p16659381555"><a name="p16659381555"></a><a name="p16659381555"></a>查询点详情</p>
</td>
<td class="cellrowborder" valign="top" width="5.06%" headers="mcps1.2.6.1.3 "><p id="p7254464271"><a name="p7254464271"></a><a name="p7254464271"></a><a href="查询点详情(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="49.519999999999996%" headers="mcps1.2.6.1.4 "><p id="p968610941012"><a name="p968610941012"></a><a name="p968610941012"></a>GET /ges/v1.0/{projectId}/graphs/{graphName}/vertices/detail?vertexIds={vertexIds}</p>
</td>
<td class="cellrowborder" valign="top" width="31.259999999999998%" headers="mcps1.2.6.1.5 "><p id="p69161498811"><a name="p69161498811"></a><a name="p69161498811"></a>给定一个点或者一组点的集合，查询这些点的详情，包括Label信息。</p>
</td>
</tr>
<tr id="row11104164913510"><td class="cellrowborder" valign="top" width="5.489999999999999%" headers="mcps1.2.6.1.1 "><p id="p20104144918513"><a name="p20104144918513"></a><a name="p20104144918513"></a>3</p>
</td>
<td class="cellrowborder" valign="top" width="8.67%" headers="mcps1.2.6.1.2 "><p id="p15955254558"><a name="p15955254558"></a><a name="p15955254558"></a>添加点</p>
</td>
<td class="cellrowborder" valign="top" width="5.06%" headers="mcps1.2.6.1.3 "><p id="p13257466276"><a name="p13257466276"></a><a name="p13257466276"></a><a href="添加点(1-0-6).md">1.0.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="49.519999999999996%" headers="mcps1.2.6.1.4 "><p id="p157416347201"><a name="p157416347201"></a><a name="p157416347201"></a>POST /ges/v1.0/{projectId}/graphs/{graphName}/vertices</p>
</td>
<td class="cellrowborder" valign="top" width="31.259999999999998%" headers="mcps1.2.6.1.5 "><p id="p189166911812"><a name="p189166911812"></a><a name="p189166911812"></a>添加一个点。</p>
</td>
</tr>
<tr id="row11577611614"><td class="cellrowborder" valign="top" width="5.489999999999999%" headers="mcps1.2.6.1.1 "><p id="p35771911612"><a name="p35771911612"></a><a name="p35771911612"></a>4</p>
</td>
<td class="cellrowborder" valign="top" width="8.67%" headers="mcps1.2.6.1.2 "><p id="p8851965610"><a name="p8851965610"></a><a name="p8851965610"></a>删除点</p>
</td>
<td class="cellrowborder" valign="top" width="5.06%" headers="mcps1.2.6.1.3 "><p id="p1525204662720"><a name="p1525204662720"></a><a name="p1525204662720"></a><a href="删除点(1-0-6).md">1.0.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="49.519999999999996%" headers="mcps1.2.6.1.4 "><p id="p17577111660"><a name="p17577111660"></a><a name="p17577111660"></a>DELETE /ges/v1.0/{projectId}/graphs/{graphName}/vertices/{vertexId}</p>
</td>
<td class="cellrowborder" valign="top" width="31.259999999999998%" headers="mcps1.2.6.1.5 "><p id="p8916159483"><a name="p8916159483"></a><a name="p8916159483"></a>删除一个点。</p>
</td>
</tr>
<tr id="row1933713101769"><td class="cellrowborder" valign="top" width="5.489999999999999%" headers="mcps1.2.6.1.1 "><p id="p20337111015612"><a name="p20337111015612"></a><a name="p20337111015612"></a>5</p>
</td>
<td class="cellrowborder" valign="top" width="8.67%" headers="mcps1.2.6.1.2 "><p id="p73783151767"><a name="p73783151767"></a><a name="p73783151767"></a>更新点属性</p>
</td>
<td class="cellrowborder" valign="top" width="5.06%" headers="mcps1.2.6.1.3 "><p id="p0251246102712"><a name="p0251246102712"></a><a name="p0251246102712"></a><a href="更新点属性(1-1-6).md">1.1.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="49.519999999999996%" headers="mcps1.2.6.1.4 "><p id="p1933818105617"><a name="p1933818105617"></a><a name="p1933818105617"></a>POST /ges/v1.0/{projectId}/graphs/{graphName}/vertices/{vertexId}/properties/action?action_id={actionId}</p>
</td>
<td class="cellrowborder" valign="top" width="31.259999999999998%" headers="mcps1.2.6.1.5 "><p id="p139161991814"><a name="p139161991814"></a><a name="p139161991814"></a>对点属性进行修改，包括新增、修改和删除。</p>
</td>
</tr>
<tr id="row66084241478"><td class="cellrowborder" valign="top" width="5.489999999999999%" headers="mcps1.2.6.1.1 "><p id="p5609724272"><a name="p5609724272"></a><a name="p5609724272"></a>6</p>
</td>
<td class="cellrowborder" valign="top" width="8.67%" headers="mcps1.2.6.1.2 "><p id="p36091324773"><a name="p36091324773"></a><a name="p36091324773"></a>批量点查询</p>
</td>
<td class="cellrowborder" valign="top" width="5.06%" headers="mcps1.2.6.1.3 "><p id="p1026134611277"><a name="p1026134611277"></a><a name="p1026134611277"></a><a href="批量点查(1-1-9).md">1.1.9</a></p>
</td>
<td class="cellrowborder" valign="top" width="49.519999999999996%" headers="mcps1.2.6.1.4 "><p id="p122031856102018"><a name="p122031856102018"></a><a name="p122031856102018"></a>POST /ges/v1.0/{projectId}/graphs/{graphName}/vertices/action?action_id=batch-query</p>
</td>
<td class="cellrowborder" valign="top" width="31.259999999999998%" headers="mcps1.2.6.1.5 "><p id="p129132298191"><a name="p129132298191"></a><a name="p129132298191"></a>批量查询点的详情。</p>
</td>
</tr>
</tbody>
</table>

**表 2**  边操作API

<a name="table184931239202318"></a>
<table><thead align="left"><tr id="row194951839182313"><th class="cellrowborder" valign="top" width="5.579442055794421%" id="mcps1.2.6.1.1"><p id="p949663920233"><a name="p949663920233"></a><a name="p949663920233"></a>序号</p>
</th>
<th class="cellrowborder" valign="top" width="9.47905209479052%" id="mcps1.2.6.1.2"><p id="p16709218307"><a name="p16709218307"></a><a name="p16709218307"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="5.669433056694331%" id="mcps1.2.6.1.3"><p id="p164961395239"><a name="p164961395239"></a><a name="p164961395239"></a>版本</p>
</th>
<th class="cellrowborder" valign="top" width="48.38516148385161%" id="mcps1.2.6.1.4"><p id="p1049633911233"><a name="p1049633911233"></a><a name="p1049633911233"></a>URL</p>
</th>
<th class="cellrowborder" valign="top" width="30.886911308869113%" id="mcps1.2.6.1.5"><p id="p84961239152317"><a name="p84961239152317"></a><a name="p84961239152317"></a>功能描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row849653992318"><td class="cellrowborder" valign="top" width="5.579442055794421%" headers="mcps1.2.6.1.1 "><p id="p1060114232914"><a name="p1060114232914"></a><a name="p1060114232914"></a>1</p>
</td>
<td class="cellrowborder" valign="top" width="9.47905209479052%" headers="mcps1.2.6.1.2 "><p id="p761642152911"><a name="p761642152911"></a><a name="p761642152911"></a>边过滤查询</p>
</td>
<td class="cellrowborder" valign="top" width="5.669433056694331%" headers="mcps1.2.6.1.3 "><p id="p164965391238"><a name="p164965391238"></a><a name="p164965391238"></a><a href="边过滤查询(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="48.38516148385161%" headers="mcps1.2.6.1.4 "><p id="p3490035152112"><a name="p3490035152112"></a><a name="p3490035152112"></a>POST /ges/v1.0/{projectId}/graphs/{graphName}/edges/action?action_id=query</p>
</td>
<td class="cellrowborder" valign="top" width="30.886911308869113%" headers="mcps1.2.6.1.5 "><p id="p8496239102318"><a name="p8496239102318"></a><a name="p8496239102318"></a>根据边的属性上的过滤条件进行过滤，查询符合过滤条件的边。</p>
</td>
</tr>
<tr id="row1049683919234"><td class="cellrowborder" valign="top" width="5.579442055794421%" headers="mcps1.2.6.1.1 "><p id="p361154213298"><a name="p361154213298"></a><a name="p361154213298"></a>2</p>
</td>
<td class="cellrowborder" valign="top" width="9.47905209479052%" headers="mcps1.2.6.1.2 "><p id="p56134213296"><a name="p56134213296"></a><a name="p56134213296"></a>查询边详情</p>
</td>
<td class="cellrowborder" valign="top" width="5.669433056694331%" headers="mcps1.2.6.1.3 "><p id="p1449623962312"><a name="p1449623962312"></a><a name="p1449623962312"></a><a href="查询边详情(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="48.38516148385161%" headers="mcps1.2.6.1.4 "><p id="p176531446102112"><a name="p176531446102112"></a><a name="p176531446102112"></a>GET /ges/v1.0/{projectId}/graphs/{graphName}/edges/detail?source={sourceVertex}&amp;target={targetVertex}&amp;index={index}</p>
</td>
<td class="cellrowborder" valign="top" width="30.886911308869113%" headers="mcps1.2.6.1.5 "><p id="p24961739192316"><a name="p24961739192316"></a><a name="p24961739192316"></a>根据边的源点和目的点查询边的详情，包括边的Label信息。</p>
</td>
</tr>
<tr id="row154063278295"><td class="cellrowborder" valign="top" width="5.579442055794421%" headers="mcps1.2.6.1.1 "><p id="p1161042162914"><a name="p1161042162914"></a><a name="p1161042162914"></a>3</p>
</td>
<td class="cellrowborder" valign="top" width="9.47905209479052%" headers="mcps1.2.6.1.2 "><p id="p26118429292"><a name="p26118429292"></a><a name="p26118429292"></a>添加边</p>
</td>
<td class="cellrowborder" valign="top" width="5.669433056694331%" headers="mcps1.2.6.1.3 "><p id="p12407152722912"><a name="p12407152722912"></a><a name="p12407152722912"></a><a href="添加边(1-0-6).md">1.0.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="48.38516148385161%" headers="mcps1.2.6.1.4 "><p id="p1560165542111"><a name="p1560165542111"></a><a name="p1560165542111"></a>POST /ges/v1.0/{projectId}/graphs/{graphName}/edges</p>
</td>
<td class="cellrowborder" valign="top" width="30.886911308869113%" headers="mcps1.2.6.1.5 "><p id="p16407132713291"><a name="p16407132713291"></a><a name="p16407132713291"></a>添加一条边。</p>
</td>
</tr>
<tr id="row11901331295"><td class="cellrowborder" valign="top" width="5.579442055794421%" headers="mcps1.2.6.1.1 "><p id="p161842152917"><a name="p161842152917"></a><a name="p161842152917"></a>4</p>
</td>
<td class="cellrowborder" valign="top" width="9.47905209479052%" headers="mcps1.2.6.1.2 "><p id="p16164292912"><a name="p16164292912"></a><a name="p16164292912"></a>删除边</p>
</td>
<td class="cellrowborder" valign="top" width="5.669433056694331%" headers="mcps1.2.6.1.3 "><p id="p819143322911"><a name="p819143322911"></a><a name="p819143322911"></a><a href="删除边(1-0-6).md">1.0.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="48.38516148385161%" headers="mcps1.2.6.1.4 "><p id="p16771513193712"><a name="p16771513193712"></a><a name="p16771513193712"></a>DELETE /ges/v1.0/{projectId}/graphs/{graphName}/edges?source<em id="i15677713163719"><a name="i15677713163719"></a><a name="i15677713163719"></a>={sourceVertex}</em>&amp;target<em id="i18677413153716"><a name="i18677413153716"></a><a name="i18677413153716"></a>={targetVertex}</em>&amp;index=<em id="i146772133373"><a name="i146772133373"></a><a name="i146772133373"></a>{index}</em></p>
</td>
<td class="cellrowborder" valign="top" width="30.886911308869113%" headers="mcps1.2.6.1.5 "><p id="p3191153392910"><a name="p3191153392910"></a><a name="p3191153392910"></a>删除一条边。</p>
</td>
</tr>
<tr id="row7437375295"><td class="cellrowborder" valign="top" width="5.579442055794421%" headers="mcps1.2.6.1.1 "><p id="p361154210294"><a name="p361154210294"></a><a name="p361154210294"></a>5</p>
</td>
<td class="cellrowborder" valign="top" width="9.47905209479052%" headers="mcps1.2.6.1.2 "><p id="p261144212913"><a name="p261144212913"></a><a name="p261144212913"></a>更新边属性</p>
</td>
<td class="cellrowborder" valign="top" width="5.669433056694331%" headers="mcps1.2.6.1.3 "><p id="p14441937112913"><a name="p14441937112913"></a><a name="p14441937112913"></a><a href="更新边属性(1-1-6).md">1.1.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="48.38516148385161%" headers="mcps1.2.6.1.4 "><p id="p15454974225"><a name="p15454974225"></a><a name="p15454974225"></a>POST /ges/v1.0/{projectId}/graphs/{graphName}/edges/properties/action?action_id={actionId}&amp;source={sourceVertex}&amp;target={targetVertex}&amp;index={index}</p>
</td>
<td class="cellrowborder" valign="top" width="30.886911308869113%" headers="mcps1.2.6.1.5 "><p id="p1944137152911"><a name="p1944137152911"></a><a name="p1944137152911"></a>对边属性进行修改，包括新增、修改和删除。</p>
</td>
</tr>
<tr id="row05331730112912"><td class="cellrowborder" valign="top" width="5.579442055794421%" headers="mcps1.2.6.1.1 "><p id="p156134219293"><a name="p156134219293"></a><a name="p156134219293"></a>6</p>
</td>
<td class="cellrowborder" valign="top" width="9.47905209479052%" headers="mcps1.2.6.1.2 "><p id="p126154219296"><a name="p126154219296"></a><a name="p126154219296"></a>批量边查询</p>
</td>
<td class="cellrowborder" valign="top" width="5.669433056694331%" headers="mcps1.2.6.1.3 "><p id="p2533193017292"><a name="p2533193017292"></a><a name="p2533193017292"></a><a href="批量边查(1-1-6).md">1.1.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="48.38516148385161%" headers="mcps1.2.6.1.4 "><p id="p13533030122913"><a name="p13533030122913"></a><a name="p13533030122913"></a>POST /ges/v1.0/{projectId}/graphs/{graphName}/edges/action?action_id=batch-query</p>
</td>
<td class="cellrowborder" valign="top" width="30.886911308869113%" headers="mcps1.2.6.1.5 "><p id="p1253313072913"><a name="p1253313072913"></a><a name="p1253313072913"></a>批量查询边的详情。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  元数据操作API

<a name="table330153173719"></a>
<table><thead align="left"><tr id="row103011734372"><th class="cellrowborder" valign="top" width="5.669433056694331%" id="mcps1.2.6.1.1"><p id="p194061632133715"><a name="p194061632133715"></a><a name="p194061632133715"></a>序号</p>
</th>
<th class="cellrowborder" valign="top" width="12.078792120787922%" id="mcps1.2.6.1.2"><p id="p94066323371"><a name="p94066323371"></a><a name="p94066323371"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="5.139486051394861%" id="mcps1.2.6.1.3"><p id="p12238185123115"><a name="p12238185123115"></a><a name="p12238185123115"></a>版本</p>
</th>
<th class="cellrowborder" valign="top" width="52.91470852914708%" id="mcps1.2.6.1.4"><p id="p10406193283719"><a name="p10406193283719"></a><a name="p10406193283719"></a>URL</p>
</th>
<th class="cellrowborder" valign="top" width="24.197580241975803%" id="mcps1.2.6.1.5"><p id="p940613243719"><a name="p940613243719"></a><a name="p940613243719"></a>功能描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row930114318371"><td class="cellrowborder" valign="top" width="5.669433056694331%" headers="mcps1.2.6.1.1 "><p id="p1930193153713"><a name="p1930193153713"></a><a name="p1930193153713"></a>1</p>
</td>
<td class="cellrowborder" valign="top" width="12.078792120787922%" headers="mcps1.2.6.1.2 "><p id="p11301153133710"><a name="p11301153133710"></a><a name="p11301153133710"></a>添加label</p>
</td>
<td class="cellrowborder" valign="top" width="5.139486051394861%" headers="mcps1.2.6.1.3 "><p id="p1323815593112"><a name="p1323815593112"></a><a name="p1323815593112"></a><a href="添加label(1-1-6).md">1.1.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="52.91470852914708%" headers="mcps1.2.6.1.4 "><p id="p16315764239"><a name="p16315764239"></a><a name="p16315764239"></a>POST /ges/v1.0/{projectId}/graphs/{graphName}/schema/labels</p>
</td>
<td class="cellrowborder" valign="top" width="24.197580241975803%" headers="mcps1.2.6.1.5 "><p id="p1830119318372"><a name="p1830119318372"></a><a name="p1830119318372"></a>添加label。</p>
</td>
</tr>
<tr id="row19301173203710"><td class="cellrowborder" valign="top" width="5.669433056694331%" headers="mcps1.2.6.1.1 "><p id="p1430118353710"><a name="p1430118353710"></a><a name="p1430118353710"></a>2</p>
</td>
<td class="cellrowborder" valign="top" width="12.078792120787922%" headers="mcps1.2.6.1.2 "><p id="p153011333370"><a name="p153011333370"></a><a name="p153011333370"></a>添加点label</p>
</td>
<td class="cellrowborder" valign="top" width="5.139486051394861%" headers="mcps1.2.6.1.3 "><p id="p1023885103116"><a name="p1023885103116"></a><a name="p1023885103116"></a><a href="添加点label(1-1-6).md">1.1.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="52.91470852914708%" headers="mcps1.2.6.1.4 "><p id="p1130113318374"><a name="p1130113318374"></a><a name="p1130113318374"></a>POST /ges/v1.0/{projectId}/graphs/{graphName}/vertices/{vertexId}/labels</p>
</td>
<td class="cellrowborder" valign="top" width="24.197580241975803%" headers="mcps1.2.6.1.5 "><p id="p13013317372"><a name="p13013317372"></a><a name="p13013317372"></a>添加点label。</p>
</td>
</tr>
<tr id="row1837938103813"><td class="cellrowborder" valign="top" width="5.669433056694331%" headers="mcps1.2.6.1.1 "><p id="p1183820382382"><a name="p1183820382382"></a><a name="p1183820382382"></a>3</p>
</td>
<td class="cellrowborder" valign="top" width="12.078792120787922%" headers="mcps1.2.6.1.2 "><p id="p12838113810389"><a name="p12838113810389"></a><a name="p12838113810389"></a>删除点label</p>
</td>
<td class="cellrowborder" valign="top" width="5.139486051394861%" headers="mcps1.2.6.1.3 "><p id="p023817593112"><a name="p023817593112"></a><a name="p023817593112"></a><a href="删除点label(1-1-6).md">1.1.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="52.91470852914708%" headers="mcps1.2.6.1.4 "><p id="p1514224012407"><a name="p1514224012407"></a><a name="p1514224012407"></a>DELETE /ges/v1.0/{projectId}/graphs/{graphName}/vertices/{vertexId}/labels/{labelName}</p>
</td>
<td class="cellrowborder" valign="top" width="24.197580241975803%" headers="mcps1.2.6.1.5 "><p id="p2838838153819"><a name="p2838838153819"></a><a name="p2838838153819"></a>删除点label。</p>
</td>
</tr>
<tr id="row128136537387"><td class="cellrowborder" valign="top" width="5.669433056694331%" headers="mcps1.2.6.1.1 "><p id="p1481335312382"><a name="p1481335312382"></a><a name="p1481335312382"></a>4</p>
</td>
<td class="cellrowborder" valign="top" width="12.078792120787922%" headers="mcps1.2.6.1.2 "><p id="p9813105317387"><a name="p9813105317387"></a><a name="p9813105317387"></a>查询元数据详情</p>
</td>
<td class="cellrowborder" valign="top" width="5.139486051394861%" headers="mcps1.2.6.1.3 "><p id="p11239135143113"><a name="p11239135143113"></a><a name="p11239135143113"></a><a href="查询图元数据详情(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="52.91470852914708%" headers="mcps1.2.6.1.4 "><p id="p155357257412"><a name="p155357257412"></a><a name="p155357257412"></a>GET /ges/v1.0/{projectId}/graphs/{graphName}/schema</p>
</td>
<td class="cellrowborder" valign="top" width="24.197580241975803%" headers="mcps1.2.6.1.5 "><p id="p1481395363811"><a name="p1481395363811"></a><a name="p1481395363811"></a>查询元数据详情。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  Gremlin操作API

<a name="table11921448105220"></a>
<table><thead align="left"><tr id="row59229488522"><th class="cellrowborder" valign="top" width="6.2%" id="mcps1.2.6.1.1"><p id="p3957101414532"><a name="p3957101414532"></a><a name="p3957101414532"></a>序号</p>
</th>
<th class="cellrowborder" valign="top" width="13.25%" id="mcps1.2.6.1.2"><p id="p4958101410537"><a name="p4958101410537"></a><a name="p4958101410537"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="7.6499999999999995%" id="mcps1.2.6.1.3"><p id="p1695818141531"><a name="p1695818141531"></a><a name="p1695818141531"></a>版本</p>
</th>
<th class="cellrowborder" valign="top" width="46.97%" id="mcps1.2.6.1.4"><p id="p795811415535"><a name="p795811415535"></a><a name="p795811415535"></a>URL</p>
</th>
<th class="cellrowborder" valign="top" width="25.929999999999996%" id="mcps1.2.6.1.5"><p id="p199587145532"><a name="p199587145532"></a><a name="p199587145532"></a>功能描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1292320486520"><td class="cellrowborder" valign="top" width="6.2%" headers="mcps1.2.6.1.1 "><p id="p19230485529"><a name="p19230485529"></a><a name="p19230485529"></a>1</p>
</td>
<td class="cellrowborder" valign="top" width="13.25%" headers="mcps1.2.6.1.2 "><p id="p1989461645415"><a name="p1989461645415"></a><a name="p1989461645415"></a>执行Gremlin查询</p>
</td>
<td class="cellrowborder" valign="top" width="7.6499999999999995%" headers="mcps1.2.6.1.3 "><p id="p1492344865211"><a name="p1492344865211"></a><a name="p1492344865211"></a><a href="执行gremlin查询(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="46.97%" headers="mcps1.2.6.1.4 "><p id="p15900154575419"><a name="p15900154575419"></a><a name="p15900154575419"></a>POST /ges/v1.0/{projectId}/graphs/{graphName}/action?action_id=execute-gremlin-query</p>
</td>
<td class="cellrowborder" valign="top" width="25.929999999999996%" headers="mcps1.2.6.1.5 "><p id="p6923948195212"><a name="p6923948195212"></a><a name="p6923948195212"></a>执行Gremlin查询。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  算法API

<a name="table155439525540"></a>
<table><thead align="left"><tr id="row165438525544"><th class="cellrowborder" valign="top" width="6.01939806019398%" id="mcps1.2.6.1.1"><p id="p025017515511"><a name="p025017515511"></a><a name="p025017515511"></a>序号</p>
</th>
<th class="cellrowborder" valign="top" width="10.54894510548945%" id="mcps1.2.6.1.2"><p id="p42500515518"><a name="p42500515518"></a><a name="p42500515518"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="6.509349065093491%" id="mcps1.2.6.1.3"><p id="p6118948163410"><a name="p6118948163410"></a><a name="p6118948163410"></a>版本</p>
</th>
<th class="cellrowborder" valign="top" width="50.65493450654935%" id="mcps1.2.6.1.4"><p id="p18250115175517"><a name="p18250115175517"></a><a name="p18250115175517"></a>URL</p>
</th>
<th class="cellrowborder" valign="top" width="26.267373262673733%" id="mcps1.2.6.1.5"><p id="p22507545512"><a name="p22507545512"></a><a name="p22507545512"></a>功能描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row155441952165412"><td class="cellrowborder" valign="top" width="6.01939806019398%" headers="mcps1.2.6.1.1 "><p id="p1854435295412"><a name="p1854435295412"></a><a name="p1854435295412"></a>1</p>
</td>
<td class="cellrowborder" valign="top" width="10.54894510548945%" headers="mcps1.2.6.1.2 "><p id="p105447522544"><a name="p105447522544"></a><a name="p105447522544"></a>执行算法</p>
</td>
<td class="cellrowborder" valign="top" width="6.509349065093491%" headers="mcps1.2.6.1.3 "><p id="p121181848193410"><a name="p121181848193410"></a><a name="p121181848193410"></a><a href="执行算法(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="50.65493450654935%" headers="mcps1.2.6.1.4 "><p id="p9327573551"><a name="p9327573551"></a><a name="p9327573551"></a>POST /ges/v1.0/{projectId}/graphs/{graphName}/action?action_id=execute-algorithm</p>
</td>
<td class="cellrowborder" valign="top" width="26.267373262673733%" headers="mcps1.2.6.1.5 "><p id="p18444182417014"><a name="p18444182417014"></a><a name="p18444182417014"></a>执行算法。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  路径API

<a name="table735132320325"></a>
<table><thead align="left"><tr id="row1736132323219"><th class="cellrowborder" valign="top" width="6.01939806019398%" id="mcps1.2.6.1.1"><p id="p10368239328"><a name="p10368239328"></a><a name="p10368239328"></a>序号</p>
</th>
<th class="cellrowborder" valign="top" width="10.54894510548945%" id="mcps1.2.6.1.2"><p id="p123612311321"><a name="p123612311321"></a><a name="p123612311321"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="6.509349065093491%" id="mcps1.2.6.1.3"><p id="p63682363218"><a name="p63682363218"></a><a name="p63682363218"></a>版本</p>
</th>
<th class="cellrowborder" valign="top" width="50.65493450654935%" id="mcps1.2.6.1.4"><p id="p193662313326"><a name="p193662313326"></a><a name="p193662313326"></a>URL</p>
</th>
<th class="cellrowborder" valign="top" width="26.267373262673733%" id="mcps1.2.6.1.5"><p id="p136723103214"><a name="p136723103214"></a><a name="p136723103214"></a>功能描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row537162363213"><td class="cellrowborder" valign="top" width="6.01939806019398%" headers="mcps1.2.6.1.1 "><p id="p33732313325"><a name="p33732313325"></a><a name="p33732313325"></a>1</p>
</td>
<td class="cellrowborder" valign="top" width="10.54894510548945%" headers="mcps1.2.6.1.2 "><p id="p103782317322"><a name="p103782317322"></a><a name="p103782317322"></a>查询路径详情</p>
</td>
<td class="cellrowborder" valign="top" width="6.509349065093491%" headers="mcps1.2.6.1.3 "><p id="p10371623143211"><a name="p10371623143211"></a><a name="p10371623143211"></a><a href="查询路径详情(1-1-6).md">1.1.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="50.65493450654935%" headers="mcps1.2.6.1.4 "><p id="p8381323123211"><a name="p8381323123211"></a><a name="p8381323123211"></a>POST /ges/v1.0/{projectId}/graphs/{graphName}/paths/action?action_id=query-detail</p>
</td>
<td class="cellrowborder" valign="top" width="26.267373262673733%" headers="mcps1.2.6.1.5 "><p id="p43862393215"><a name="p43862393215"></a><a name="p43862393215"></a>查询路径详情。</p>
</td>
</tr>
</tbody>
</table>

**表 7**  图统计API

<a name="table1178265135611"></a>
<table><thead align="left"><tr id="row6783105135614"><th class="cellrowborder" valign="top" width="5.79%" id="mcps1.2.6.1.1"><p id="p33061439205719"><a name="p33061439205719"></a><a name="p33061439205719"></a>序号</p>
</th>
<th class="cellrowborder" valign="top" width="13.29%" id="mcps1.2.6.1.2"><p id="p1830693955714"><a name="p1830693955714"></a><a name="p1830693955714"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="7.33%" id="mcps1.2.6.1.3"><p id="p9306123919573"><a name="p9306123919573"></a><a name="p9306123919573"></a>版本</p>
</th>
<th class="cellrowborder" valign="top" width="47.77%" id="mcps1.2.6.1.4"><p id="p1530613925710"><a name="p1530613925710"></a><a name="p1530613925710"></a>URL</p>
</th>
<th class="cellrowborder" valign="top" width="25.82%" id="mcps1.2.6.1.5"><p id="p33061739185718"><a name="p33061739185718"></a><a name="p33061739185718"></a>功能描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1578385110566"><td class="cellrowborder" valign="top" width="5.79%" headers="mcps1.2.6.1.1 "><p id="p678311515568"><a name="p678311515568"></a><a name="p678311515568"></a>1</p>
</td>
<td class="cellrowborder" valign="top" width="13.29%" headers="mcps1.2.6.1.2 "><p id="p378375118567"><a name="p378375118567"></a><a name="p378375118567"></a>查询图概要信息</p>
</td>
<td class="cellrowborder" valign="top" width="7.33%" headers="mcps1.2.6.1.3 "><p id="p978318518567"><a name="p978318518567"></a><a name="p978318518567"></a><a href="查询图概要信息(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="47.77%" headers="mcps1.2.6.1.4 "><p id="p1887131115612"><a name="p1887131115612"></a><a name="p1887131115612"></a>GET /ges/v1.0/{projectId}/graphs/{graphName}/summary</p>
</td>
<td class="cellrowborder" valign="top" width="25.82%" headers="mcps1.2.6.1.5 "><p id="p387631816014"><a name="p387631816014"></a><a name="p387631816014"></a>查询图概要信息。</p>
</td>
</tr>
<tr id="row187831151195619"><td class="cellrowborder" valign="top" width="5.79%" headers="mcps1.2.6.1.1 "><p id="p11783145155610"><a name="p11783145155610"></a><a name="p11783145155610"></a>2</p>
</td>
<td class="cellrowborder" valign="top" width="13.29%" headers="mcps1.2.6.1.2 "><p id="p16783155112568"><a name="p16783155112568"></a><a name="p16783155112568"></a>查询图版本</p>
</td>
<td class="cellrowborder" valign="top" width="7.33%" headers="mcps1.2.6.1.3 "><p id="p1478395112568"><a name="p1478395112568"></a><a name="p1478395112568"></a><a href="查询图版本（2-0-0）.md">2.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="47.77%" headers="mcps1.2.6.1.4 "><p id="p181471614125612"><a name="p181471614125612"></a><a name="p181471614125612"></a>GET /ges/v1.0/{projectId}/graphs/{graphName}/version</p>
</td>
<td class="cellrowborder" valign="top" width="25.82%" headers="mcps1.2.6.1.5 "><p id="p087611815011"><a name="p087611815011"></a><a name="p087611815011"></a>查询图版本。</p>
</td>
</tr>
</tbody>
</table>

**表 8**  Job管理相关接口

<a name="table18909727165717"></a>
<table><thead align="left"><tr id="row3910192716570"><th class="cellrowborder" valign="top" width="5.6705670567056705%" id="mcps1.2.6.1.1"><p id="p15730141135912"><a name="p15730141135912"></a><a name="p15730141135912"></a>序号</p>
</th>
<th class="cellrowborder" valign="top" width="13.691369136913693%" id="mcps1.2.6.1.2"><p id="p15730141155919"><a name="p15730141155919"></a><a name="p15730141155919"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="7.240724072407241%" id="mcps1.2.6.1.3"><p id="p073013115598"><a name="p073013115598"></a><a name="p073013115598"></a>版本</p>
</th>
<th class="cellrowborder" valign="top" width="48.04480448044804%" id="mcps1.2.6.1.4"><p id="p13730511195917"><a name="p13730511195917"></a><a name="p13730511195917"></a>URL</p>
</th>
<th class="cellrowborder" valign="top" width="25.352535253525353%" id="mcps1.2.6.1.5"><p id="p6730151165919"><a name="p6730151165919"></a><a name="p6730151165919"></a>功能描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row16910112755719"><td class="cellrowborder" valign="top" width="5.6705670567056705%" headers="mcps1.2.6.1.1 "><p id="p1491012755719"><a name="p1491012755719"></a><a name="p1491012755719"></a>1</p>
</td>
<td class="cellrowborder" valign="top" width="13.691369136913693%" headers="mcps1.2.6.1.2 "><p id="p591092713577"><a name="p591092713577"></a><a name="p591092713577"></a>查询Job状态</p>
</td>
<td class="cellrowborder" valign="top" width="7.240724072407241%" headers="mcps1.2.6.1.3 "><p id="p29101827105716"><a name="p29101827105716"></a><a name="p29101827105716"></a><a href="查询job状态(1-0-0)-3.md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="48.04480448044804%" headers="mcps1.2.6.1.4 "><p id="p129841312134016"><a name="p129841312134016"></a><a name="p129841312134016"></a>GET /ges/v1.0/{projectId}/graphs/{graphName}/jobs/{jobId}/status?offset=<em id="i9984201214012"><a name="i9984201214012"></a><a name="i9984201214012"></a>offset</em>&amp;limit=<em id="i5984912184017"><a name="i5984912184017"></a><a name="i5984912184017"></a>limit</em></p>
</td>
<td class="cellrowborder" valign="top" width="25.352535253525353%" headers="mcps1.2.6.1.5 "><p id="p174320287110"><a name="p174320287110"></a><a name="p174320287110"></a>查询Job状态。</p>
</td>
</tr>
<tr id="row2317724115910"><td class="cellrowborder" valign="top" width="5.6705670567056705%" headers="mcps1.2.6.1.1 "><p id="p131716248591"><a name="p131716248591"></a><a name="p131716248591"></a>2</p>
</td>
<td class="cellrowborder" valign="top" width="13.691369136913693%" headers="mcps1.2.6.1.2 "><p id="p143172024125918"><a name="p143172024125918"></a><a name="p143172024125918"></a>取消Job</p>
</td>
<td class="cellrowborder" valign="top" width="7.240724072407241%" headers="mcps1.2.6.1.3 "><p id="p7318152475916"><a name="p7318152475916"></a><a name="p7318152475916"></a><a href="取消job(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="48.04480448044804%" headers="mcps1.2.6.1.4 "><p id="p320117497564"><a name="p320117497564"></a><a name="p320117497564"></a>DELETE http://Endpoint/ges/v1.0/{projectId}/graphs/{graphName}/jobs/{jobId}</p>
</td>
<td class="cellrowborder" valign="top" width="25.352535253525353%" headers="mcps1.2.6.1.5 "><p id="p1543214284116"><a name="p1543214284116"></a><a name="p1543214284116"></a>取消Job。</p>
</td>
</tr>
</tbody>
</table>


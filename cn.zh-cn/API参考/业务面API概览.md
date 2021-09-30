# 业务面API概览<a name="ges_03_0003"></a>

GES业务面API包括点操作、边操作、元数据操作、Gremlin操作、算法、路径、图统计、子图操作和Job管理。

**表 1**  点操作API

<a name="table7304174193110"></a>
<table><thead align="left"><tr id="row153051646317"><th class="cellrowborder" valign="top" width="10.93890610938906%" id="mcps1.2.5.1.1"><p id="p830519413120"><a name="p830519413120"></a><a name="p830519413120"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="6.869313068693131%" id="mcps1.2.5.1.2"><p id="p1324346122710"><a name="p1324346122710"></a><a name="p1324346122710"></a>版本</p>
</th>
<th class="cellrowborder" valign="top" width="51.7948205179482%" id="mcps1.2.5.1.3"><p id="p173057463116"><a name="p173057463116"></a><a name="p173057463116"></a>URL</p>
</th>
<th class="cellrowborder" valign="top" width="30.3969603039696%" id="mcps1.2.5.1.4"><p id="p5916189283"><a name="p5916189283"></a><a name="p5916189283"></a>功能描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row530514411314"><td class="cellrowborder" valign="top" width="10.93890610938906%" headers="mcps1.2.5.1.1 "><p id="p6518171521318"><a name="p6518171521318"></a><a name="p6518171521318"></a>点过滤查询</p>
</td>
<td class="cellrowborder" valign="top" width="6.869313068693131%" headers="mcps1.2.5.1.2 "><p id="p42514460277"><a name="p42514460277"></a><a name="p42514460277"></a><a href="点过滤查询(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="51.7948205179482%" headers="mcps1.2.5.1.3 "><p id="p18517191513133"><a name="p18517191513133"></a><a name="p18517191513133"></a>POST/ges/v1.0/{project_id}/graphs/{graph_name}/vertices/action?action_id=query</p>
</td>
<td class="cellrowborder" valign="top" width="30.3969603039696%" headers="mcps1.2.5.1.4 "><p id="p69160917820"><a name="p69160917820"></a><a name="p69160917820"></a>根据某个过滤条件查询点，比如点元数据中含有age属性，过滤条件可以为age&gt;18。</p>
</td>
</tr>
<tr id="row23061417313"><td class="cellrowborder" valign="top" width="10.93890610938906%" headers="mcps1.2.5.1.1 "><p id="p16659381555"><a name="p16659381555"></a><a name="p16659381555"></a>查询点详情</p>
</td>
<td class="cellrowborder" valign="top" width="6.869313068693131%" headers="mcps1.2.5.1.2 "><p id="p7254464271"><a name="p7254464271"></a><a name="p7254464271"></a><a href="查询点详情(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="51.7948205179482%" headers="mcps1.2.5.1.3 "><p id="p968610941012"><a name="p968610941012"></a><a name="p968610941012"></a>GET/ges/v1.0/{project_id}/graphs/{graph_name}/vertices/detail?vertexIds={vertex_ids}</p>
</td>
<td class="cellrowborder" valign="top" width="30.3969603039696%" headers="mcps1.2.5.1.4 "><p id="p69161498811"><a name="p69161498811"></a><a name="p69161498811"></a>给定一个点或者一组点的集合，查询这些点的详情，包括Label信息。</p>
</td>
</tr>
<tr id="row11104164913510"><td class="cellrowborder" valign="top" width="10.93890610938906%" headers="mcps1.2.5.1.1 "><p id="p15955254558"><a name="p15955254558"></a><a name="p15955254558"></a>添加点</p>
</td>
<td class="cellrowborder" valign="top" width="6.869313068693131%" headers="mcps1.2.5.1.2 "><p id="p13257466276"><a name="p13257466276"></a><a name="p13257466276"></a><a href="添加点(1-0-6).md">1.0.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="51.7948205179482%" headers="mcps1.2.5.1.3 "><p id="p157416347201"><a name="p157416347201"></a><a name="p157416347201"></a>POST /ges/v1.0/{project_id}/graphs/{graph_name}/vertices</p>
</td>
<td class="cellrowborder" valign="top" width="30.3969603039696%" headers="mcps1.2.5.1.4 "><p id="p189166911812"><a name="p189166911812"></a><a name="p189166911812"></a>添加一个点。</p>
</td>
</tr>
<tr id="row11577611614"><td class="cellrowborder" valign="top" width="10.93890610938906%" headers="mcps1.2.5.1.1 "><p id="p8851965610"><a name="p8851965610"></a><a name="p8851965610"></a>删除点</p>
</td>
<td class="cellrowborder" valign="top" width="6.869313068693131%" headers="mcps1.2.5.1.2 "><p id="p1525204662720"><a name="p1525204662720"></a><a name="p1525204662720"></a><a href="删除点(1-0-6).md">1.0.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="51.7948205179482%" headers="mcps1.2.5.1.3 "><p id="p17577111660"><a name="p17577111660"></a><a name="p17577111660"></a>DELETE/ges/v1.0/{project_id}/graphs/{graph_name}/vertices/{vertex_id}</p>
</td>
<td class="cellrowborder" valign="top" width="30.3969603039696%" headers="mcps1.2.5.1.4 "><p id="p8916159483"><a name="p8916159483"></a><a name="p8916159483"></a>删除一个点。</p>
</td>
</tr>
<tr id="row1933713101769"><td class="cellrowborder" valign="top" width="10.93890610938906%" headers="mcps1.2.5.1.1 "><p id="p73783151767"><a name="p73783151767"></a><a name="p73783151767"></a>更新点属性</p>
</td>
<td class="cellrowborder" valign="top" width="6.869313068693131%" headers="mcps1.2.5.1.2 "><p id="p0251246102712"><a name="p0251246102712"></a><a name="p0251246102712"></a><a href="更新点属性(1-1-6).md">1.1.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="51.7948205179482%" headers="mcps1.2.5.1.3 "><p id="p1933818105617"><a name="p1933818105617"></a><a name="p1933818105617"></a>POST/ges/v1.0/{project_id}/graphs/{graph_name}/vertices/{vertex_id}/properties/action?action_id={actionId}</p>
</td>
<td class="cellrowborder" valign="top" width="30.3969603039696%" headers="mcps1.2.5.1.4 "><p id="p139161991814"><a name="p139161991814"></a><a name="p139161991814"></a>对点属性进行修改，包括新增、修改和删除。</p>
</td>
</tr>
<tr id="row66084241478"><td class="cellrowborder" valign="top" width="10.93890610938906%" headers="mcps1.2.5.1.1 "><p id="p36091324773"><a name="p36091324773"></a><a name="p36091324773"></a>批量点查询</p>
</td>
<td class="cellrowborder" valign="top" width="6.869313068693131%" headers="mcps1.2.5.1.2 "><p id="p1026134611277"><a name="p1026134611277"></a><a name="p1026134611277"></a><a href="批量点查(1-1-9).md">1.1.9</a></p>
</td>
<td class="cellrowborder" valign="top" width="51.7948205179482%" headers="mcps1.2.5.1.3 "><p id="p122031856102018"><a name="p122031856102018"></a><a name="p122031856102018"></a>POST/ges/v1.0/{project_id}/graphs/{graph_name}/vertices/action?action_id=batch-query</p>
</td>
<td class="cellrowborder" valign="top" width="30.3969603039696%" headers="mcps1.2.5.1.4 "><p id="p129132298191"><a name="p129132298191"></a><a name="p129132298191"></a>批量查询点的详情。</p>
</td>
</tr>
<tr id="row5965395019"><td class="cellrowborder" valign="top" width="10.93890610938906%" headers="mcps1.2.5.1.1 "><p id="p139663912012"><a name="p139663912012"></a><a name="p139663912012"></a>批量添加点</p>
</td>
<td class="cellrowborder" valign="top" width="6.869313068693131%" headers="mcps1.2.5.1.2 "><p id="p49661194019"><a name="p49661194019"></a><a name="p49661194019"></a><a href="批量添加点(2-1-16).md">2.1.16</a></p>
</td>
<td class="cellrowborder" valign="top" width="51.7948205179482%" headers="mcps1.2.5.1.3 "><p id="p69662911015"><a name="p69662911015"></a><a name="p69662911015"></a>POST /ges/v1.0/{project_id}/graphs/{graph_name}/vertices/action?action_id=batch-add</p>
</td>
<td class="cellrowborder" valign="top" width="30.3969603039696%" headers="mcps1.2.5.1.4 "><p id="p139661595013"><a name="p139661595013"></a><a name="p139661595013"></a>批量添加点的操作。</p>
</td>
</tr>
<tr id="row69011651501"><td class="cellrowborder" valign="top" width="10.93890610938906%" headers="mcps1.2.5.1.1 "><p id="p99011451609"><a name="p99011451609"></a><a name="p99011451609"></a>批量删除点</p>
</td>
<td class="cellrowborder" valign="top" width="6.869313068693131%" headers="mcps1.2.5.1.2 "><p id="p290112515011"><a name="p290112515011"></a><a name="p290112515011"></a><a href="批量删除点(2-1-9).md">2.1.9</a></p>
</td>
<td class="cellrowborder" valign="top" width="51.7948205179482%" headers="mcps1.2.5.1.3 "><p id="p186548243216"><a name="p186548243216"></a><a name="p186548243216"></a>POST /ges/v1.0/{project_id}/graphs/{graph_name}/vertices/action?action_id=batch-delete</p>
</td>
<td class="cellrowborder" valign="top" width="30.3969603039696%" headers="mcps1.2.5.1.4 "><p id="p663012242348"><a name="p663012242348"></a><a name="p663012242348"></a>根据批量节点ID删除节点。</p>
</td>
</tr>
<tr id="row17859554703"><td class="cellrowborder" valign="top" width="10.93890610938906%" headers="mcps1.2.5.1.1 "><p id="p28596542011"><a name="p28596542011"></a><a name="p28596542011"></a>批量更新点属性</p>
</td>
<td class="cellrowborder" valign="top" width="6.869313068693131%" headers="mcps1.2.5.1.2 "><p id="p9859115418015"><a name="p9859115418015"></a><a name="p9859115418015"></a><a href="更新点属性(1-1-6).md">2.1.10</a></p>
</td>
<td class="cellrowborder" valign="top" width="51.7948205179482%" headers="mcps1.2.5.1.3 "><p id="p585945410012"><a name="p585945410012"></a><a name="p585945410012"></a>POST /ges/v1.0/{project_id}/graphs/{graph_name}/vertices/properties/action?action_id={actionId}</p>
</td>
<td class="cellrowborder" valign="top" width="30.3969603039696%" headers="mcps1.2.5.1.4 "><p id="p185955416015"><a name="p185955416015"></a><a name="p185955416015"></a>批量更新点的属性。</p>
</td>
</tr>
<tr id="row5533151418715"><td class="cellrowborder" valign="top" width="10.93890610938906%" headers="mcps1.2.5.1.1 "><p id="p13533914479"><a name="p13533914479"></a><a name="p13533914479"></a>添加点label</p>
</td>
<td class="cellrowborder" valign="top" width="6.869313068693131%" headers="mcps1.2.5.1.2 "><p id="p153315145717"><a name="p153315145717"></a><a name="p153315145717"></a><a href="添加点label(1-1-6).md">1.1.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="51.7948205179482%" headers="mcps1.2.5.1.3 "><p id="p853316141574"><a name="p853316141574"></a><a name="p853316141574"></a>POST /ges/v1.0/{project_id}/graphs/{graph_name}/vertices/{vertex_id}/labels</p>
</td>
<td class="cellrowborder" valign="top" width="30.3969603039696%" headers="mcps1.2.5.1.4 "><p id="p453311420712"><a name="p453311420712"></a><a name="p453311420712"></a>添加点的标签。</p>
</td>
</tr>
<tr id="row35715235815"><td class="cellrowborder" valign="top" width="10.93890610938906%" headers="mcps1.2.5.1.1 "><p id="p657214231689"><a name="p657214231689"></a><a name="p657214231689"></a>删除点label</p>
</td>
<td class="cellrowborder" valign="top" width="6.869313068693131%" headers="mcps1.2.5.1.2 "><p id="p17572152320811"><a name="p17572152320811"></a><a name="p17572152320811"></a><a href="删除点label(1-1-6).md">1.1.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="51.7948205179482%" headers="mcps1.2.5.1.3 "><p id="p1557213231689"><a name="p1557213231689"></a><a name="p1557213231689"></a>DELETE /ges/v1.0/{project_id}/graphs/{graph_name}/vertices/{vertex_id}/labels/{label_name}</p>
</td>
<td class="cellrowborder" valign="top" width="30.3969603039696%" headers="mcps1.2.5.1.4 "><p id="p857242313817"><a name="p857242313817"></a><a name="p857242313817"></a>删除点的标签。</p>
</td>
</tr>
<tr id="row919464512820"><td class="cellrowborder" valign="top" width="10.93890610938906%" headers="mcps1.2.5.1.1 "><p id="p20195144592814"><a name="p20195144592814"></a><a name="p20195144592814"></a>导出过滤后的点</p>
</td>
<td class="cellrowborder" valign="top" width="6.869313068693131%" headers="mcps1.2.5.1.2 "><p id="p81951454289"><a name="p81951454289"></a><a name="p81951454289"></a><a href="导出过滤后的点(2-2-7).md">2.2.7</a></p>
</td>
<td class="cellrowborder" valign="top" width="51.7948205179482%" headers="mcps1.2.5.1.3 "><pre class="screen" id="screen16797996175049"><a name="screen16797996175049"></a><a name="screen16797996175049"></a>POST /ges/v1.0/{project_id}/graphs/{graph_name}/vertices/action?action_id=export</pre>
</td>
<td class="cellrowborder" valign="top" width="30.3969603039696%" headers="mcps1.2.5.1.4 "><p id="p51961945132818"><a name="p51961945132818"></a><a name="p51961945132818"></a>导出满足过滤条件的顶点集合。</p>
</td>
</tr>
<tr id="row4935194882812"><td class="cellrowborder" valign="top" width="10.93890610938906%" headers="mcps1.2.5.1.1 "><p id="p1993617488286"><a name="p1993617488286"></a><a name="p1993617488286"></a>删除过滤后的点</p>
</td>
<td class="cellrowborder" valign="top" width="6.869313068693131%" headers="mcps1.2.5.1.2 "><p id="p16936144810282"><a name="p16936144810282"></a><a name="p16936144810282"></a><a href="删除过滤后的点(2-2-7).md">2.2.7</a></p>
</td>
<td class="cellrowborder" valign="top" width="51.7948205179482%" headers="mcps1.2.5.1.3 "><pre class="screen" id="screen94741259173018"><a name="screen94741259173018"></a><a name="screen94741259173018"></a>POST /ges/v1.0/{project_id}/graphs/{graph_name}/vertices/action?action_id=delete</pre>
</td>
<td class="cellrowborder" valign="top" width="30.3969603039696%" headers="mcps1.2.5.1.4 "><p id="p16936348192818"><a name="p16936348192818"></a><a name="p16936348192818"></a>删除满足过滤条件的顶点集合。</p>
</td>
</tr>
</tbody>
</table>

**表 2**  边操作API

<a name="table184931239202318"></a>
<table><thead align="left"><tr id="row194951839182313"><th class="cellrowborder" valign="top" width="11.06%" id="mcps1.2.5.1.1"><p id="p16709218307"><a name="p16709218307"></a><a name="p16709218307"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="6.64%" id="mcps1.2.5.1.2"><p id="p164961395239"><a name="p164961395239"></a><a name="p164961395239"></a>版本</p>
</th>
<th class="cellrowborder" valign="top" width="52.61%" id="mcps1.2.5.1.3"><p id="p1049633911233"><a name="p1049633911233"></a><a name="p1049633911233"></a>URL</p>
</th>
<th class="cellrowborder" valign="top" width="29.69%" id="mcps1.2.5.1.4"><p id="p84961239152317"><a name="p84961239152317"></a><a name="p84961239152317"></a>功能描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row849653992318"><td class="cellrowborder" valign="top" width="11.06%" headers="mcps1.2.5.1.1 "><p id="p761642152911"><a name="p761642152911"></a><a name="p761642152911"></a>边过滤查询</p>
</td>
<td class="cellrowborder" valign="top" width="6.64%" headers="mcps1.2.5.1.2 "><p id="p164965391238"><a name="p164965391238"></a><a name="p164965391238"></a><a href="边过滤查询(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="52.61%" headers="mcps1.2.5.1.3 "><p id="p3490035152112"><a name="p3490035152112"></a><a name="p3490035152112"></a>POST/ges/v1.0/{project_id}/graphs/{graph_name}/edges/action?action_id=query</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.5.1.4 "><p id="p8496239102318"><a name="p8496239102318"></a><a name="p8496239102318"></a>根据边的属性上的过滤条件进行过滤，查询符合过滤条件的边。</p>
</td>
</tr>
<tr id="row1049683919234"><td class="cellrowborder" valign="top" width="11.06%" headers="mcps1.2.5.1.1 "><p id="p56134213296"><a name="p56134213296"></a><a name="p56134213296"></a>查询边详情</p>
</td>
<td class="cellrowborder" valign="top" width="6.64%" headers="mcps1.2.5.1.2 "><p id="p1449623962312"><a name="p1449623962312"></a><a name="p1449623962312"></a><a href="查询边详情(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="52.61%" headers="mcps1.2.5.1.3 "><p id="p176531446102112"><a name="p176531446102112"></a><a name="p176531446102112"></a>GET /ges/v1.0/{project_id}/graphs/{graph_name}/edges/detail?source={sourceVertex}&amp;target={targetVertex}&amp;index={index}</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.5.1.4 "><p id="p24961739192316"><a name="p24961739192316"></a><a name="p24961739192316"></a>根据边的源点和目的点查询边的详情，包括边的Label信息。</p>
</td>
</tr>
<tr id="row154063278295"><td class="cellrowborder" valign="top" width="11.06%" headers="mcps1.2.5.1.1 "><p id="p26118429292"><a name="p26118429292"></a><a name="p26118429292"></a>添加边</p>
</td>
<td class="cellrowborder" valign="top" width="6.64%" headers="mcps1.2.5.1.2 "><p id="p12407152722912"><a name="p12407152722912"></a><a name="p12407152722912"></a><a href="添加边(1-0-6).md">1.0.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="52.61%" headers="mcps1.2.5.1.3 "><p id="p1560165542111"><a name="p1560165542111"></a><a name="p1560165542111"></a>POST /ges/v1.0/{project_id}/graphs/{graph_name}/edges</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.5.1.4 "><p id="p16407132713291"><a name="p16407132713291"></a><a name="p16407132713291"></a>添加一条边。</p>
</td>
</tr>
<tr id="row11901331295"><td class="cellrowborder" valign="top" width="11.06%" headers="mcps1.2.5.1.1 "><p id="p16164292912"><a name="p16164292912"></a><a name="p16164292912"></a>删除边</p>
</td>
<td class="cellrowborder" valign="top" width="6.64%" headers="mcps1.2.5.1.2 "><p id="p819143322911"><a name="p819143322911"></a><a name="p819143322911"></a><a href="删除边(1-0-6).md">1.0.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="52.61%" headers="mcps1.2.5.1.3 "><p id="p16771513193712"><a name="p16771513193712"></a><a name="p16771513193712"></a>DELETE /ges/v1.0/{project_id}/graphs/{graph_name}/edges?source<em id="i15677713163719"><a name="i15677713163719"></a><a name="i15677713163719"></a>={sourceVertex}</em>&amp;target<em id="i18677413153716"><a name="i18677413153716"></a><a name="i18677413153716"></a>={targetVertex}</em>&amp;index=<em id="i146772133373"><a name="i146772133373"></a><a name="i146772133373"></a>{index}</em></p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.5.1.4 "><p id="p3191153392910"><a name="p3191153392910"></a><a name="p3191153392910"></a>删除一条边。</p>
</td>
</tr>
<tr id="row7437375295"><td class="cellrowborder" valign="top" width="11.06%" headers="mcps1.2.5.1.1 "><p id="p261144212913"><a name="p261144212913"></a><a name="p261144212913"></a>更新边属性</p>
</td>
<td class="cellrowborder" valign="top" width="6.64%" headers="mcps1.2.5.1.2 "><p id="p14441937112913"><a name="p14441937112913"></a><a name="p14441937112913"></a><a href="更新边属性(1-1-6).md">1.1.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="52.61%" headers="mcps1.2.5.1.3 "><p id="p15454974225"><a name="p15454974225"></a><a name="p15454974225"></a>POST/ges/v1.0/{project_id}/graphs/{graph_name}/edges/properties/action?action_id={actionId}&amp;source={sourceVertex}&amp;target={targetVertex}&amp;index={index}</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.5.1.4 "><p id="p1944137152911"><a name="p1944137152911"></a><a name="p1944137152911"></a>对边属性进行修改，包括新增、修改和删除。</p>
</td>
</tr>
<tr id="row05331730112912"><td class="cellrowborder" valign="top" width="11.06%" headers="mcps1.2.5.1.1 "><p id="p126154219296"><a name="p126154219296"></a><a name="p126154219296"></a>批量边查询</p>
</td>
<td class="cellrowborder" valign="top" width="6.64%" headers="mcps1.2.5.1.2 "><p id="p2533193017292"><a name="p2533193017292"></a><a name="p2533193017292"></a><a href="批量边查(1-1-6).md">1.1.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="52.61%" headers="mcps1.2.5.1.3 "><p id="p13533030122913"><a name="p13533030122913"></a><a name="p13533030122913"></a>POST/ges/v1.0/{project_id}/graphs/{graph_name}/edges/action?action_id=batch-query</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.5.1.4 "><p id="p1253313072913"><a name="p1253313072913"></a><a name="p1253313072913"></a>批量查询边的详情。</p>
</td>
</tr>
<tr id="row166918419104"><td class="cellrowborder" valign="top" width="11.06%" headers="mcps1.2.5.1.1 "><p id="p669174101020"><a name="p669174101020"></a><a name="p669174101020"></a>批量添加边</p>
</td>
<td class="cellrowborder" valign="top" width="6.64%" headers="mcps1.2.5.1.2 "><p id="p17691042107"><a name="p17691042107"></a><a name="p17691042107"></a><a href="批量添加边(2-1-16).md">2.1.16</a></p>
</td>
<td class="cellrowborder" valign="top" width="52.61%" headers="mcps1.2.5.1.3 "><p id="p10692451011"><a name="p10692451011"></a><a name="p10692451011"></a>POST /ges/v1.0/{project_id}/graphs/{graph_name}/edges/action?action_id=batch-add</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.5.1.4 "><p id="p66910414107"><a name="p66910414107"></a><a name="p66910414107"></a>批量添加边的操作。</p>
</td>
</tr>
<tr id="row171691618118"><td class="cellrowborder" valign="top" width="11.06%" headers="mcps1.2.5.1.1 "><p id="p3169862116"><a name="p3169862116"></a><a name="p3169862116"></a>批量删除边</p>
</td>
<td class="cellrowborder" valign="top" width="6.64%" headers="mcps1.2.5.1.2 "><p id="p216946131111"><a name="p216946131111"></a><a name="p216946131111"></a><a href="批量删除边(2-1-9).md">2.1.9</a></p>
</td>
<td class="cellrowborder" valign="top" width="52.61%" headers="mcps1.2.5.1.3 "><p id="p9169136151114"><a name="p9169136151114"></a><a name="p9169136151114"></a>POST /ges/v1.0/{project_id}/graphs/{graph_name}/edges/action?action_id=batch-delete</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.5.1.4 "><p id="p1116915651117"><a name="p1116915651117"></a><a name="p1116915651117"></a>根据批量边的起点、终点以及索引，删除这些边。</p>
</td>
</tr>
<tr id="row12678184951117"><td class="cellrowborder" valign="top" width="11.06%" headers="mcps1.2.5.1.1 "><p id="p567814910113"><a name="p567814910113"></a><a name="p567814910113"></a>批量更新边属性</p>
</td>
<td class="cellrowborder" valign="top" width="6.64%" headers="mcps1.2.5.1.2 "><p id="p36782497118"><a name="p36782497118"></a><a name="p36782497118"></a><a href="批量更新边属性(2-1-10).md">2.1.10</a></p>
</td>
<td class="cellrowborder" valign="top" width="52.61%" headers="mcps1.2.5.1.3 "><p id="p46791849151115"><a name="p46791849151115"></a><a name="p46791849151115"></a>POST /ges/v1.0/{project_id}/graphs/{graph_name}/edges/properties/action?action_id={actionId}</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.5.1.4 "><p id="p1267944917117"><a name="p1267944917117"></a><a name="p1267944917117"></a>批量更新边属性。</p>
</td>
</tr>
<tr id="row106381924173214"><td class="cellrowborder" valign="top" width="11.06%" headers="mcps1.2.5.1.1 "><p id="p166384248321"><a name="p166384248321"></a><a name="p166384248321"></a>导出过滤后的边</p>
</td>
<td class="cellrowborder" valign="top" width="6.64%" headers="mcps1.2.5.1.2 "><p id="p156381924203218"><a name="p156381924203218"></a><a name="p156381924203218"></a><a href="导出过滤后的边(2-2-7).md">2.2.7</a></p>
</td>
<td class="cellrowborder" valign="top" width="52.61%" headers="mcps1.2.5.1.3 "><p id="p17639132414324"><a name="p17639132414324"></a><a name="p17639132414324"></a>POST /ges/v1.0/{project_id}/graphs/{graph_name}/edges/action?action_id=export</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.5.1.4 "><p id="p76391243325"><a name="p76391243325"></a><a name="p76391243325"></a>导出满足过滤条件的边集合。</p>
</td>
</tr>
<tr id="row14312228193213"><td class="cellrowborder" valign="top" width="11.06%" headers="mcps1.2.5.1.1 "><p id="p3312102853217"><a name="p3312102853217"></a><a name="p3312102853217"></a>删除过滤后的边</p>
</td>
<td class="cellrowborder" valign="top" width="6.64%" headers="mcps1.2.5.1.2 "><p id="p6312828163212"><a name="p6312828163212"></a><a name="p6312828163212"></a><a href="删除过滤后的边(2-2-7).md">2.2.7</a></p>
</td>
<td class="cellrowborder" valign="top" width="52.61%" headers="mcps1.2.5.1.3 "><p id="p20786165293418"><a name="p20786165293418"></a><a name="p20786165293418"></a>POST /ges/v1.0/{project_id}/graphs/{graph_name}/edges/action?action_id=delete</p>
</td>
<td class="cellrowborder" valign="top" width="29.69%" headers="mcps1.2.5.1.4 "><p id="p1928912304185"><a name="p1928912304185"></a><a name="p1928912304185"></a>删除满足过滤条件的边集合。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  元数据操作API

<a name="table330153173719"></a>
<table><thead align="left"><tr id="row103011734372"><th class="cellrowborder" valign="top" width="13.741374137413743%" id="mcps1.2.5.1.1"><p id="p94066323371"><a name="p94066323371"></a><a name="p94066323371"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="6.8706870687068715%" id="mcps1.2.5.1.2"><p id="p12238185123115"><a name="p12238185123115"></a><a name="p12238185123115"></a>版本</p>
</th>
<th class="cellrowborder" valign="top" width="64.13641364136414%" id="mcps1.2.5.1.3"><p id="p10406193283719"><a name="p10406193283719"></a><a name="p10406193283719"></a>URL</p>
</th>
<th class="cellrowborder" valign="top" width="15.251525152515253%" id="mcps1.2.5.1.4"><p id="p940613243719"><a name="p940613243719"></a><a name="p940613243719"></a>功能描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row930114318371"><td class="cellrowborder" valign="top" width="13.741374137413743%" headers="mcps1.2.5.1.1 "><p id="p11301153133710"><a name="p11301153133710"></a><a name="p11301153133710"></a>添加label</p>
</td>
<td class="cellrowborder" valign="top" width="6.8706870687068715%" headers="mcps1.2.5.1.2 "><p id="p1323815593112"><a name="p1323815593112"></a><a name="p1323815593112"></a><a href="添加label(1-1-6).md">1.1.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="64.13641364136414%" headers="mcps1.2.5.1.3 "><p id="p16315764239"><a name="p16315764239"></a><a name="p16315764239"></a>POST /ges/v1.0/{project_id}/graphs/{graph_name}/schema/labels</p>
</td>
<td class="cellrowborder" valign="top" width="15.251525152515253%" headers="mcps1.2.5.1.4 "><p id="p1830119318372"><a name="p1830119318372"></a><a name="p1830119318372"></a>添加label。</p>
</td>
</tr>
<tr id="row19301173203710"><td class="cellrowborder" valign="top" width="13.741374137413743%" headers="mcps1.2.5.1.1 "><p id="p153011333370"><a name="p153011333370"></a><a name="p153011333370"></a>添加点label</p>
</td>
<td class="cellrowborder" valign="top" width="6.8706870687068715%" headers="mcps1.2.5.1.2 "><p id="p1023885103116"><a name="p1023885103116"></a><a name="p1023885103116"></a><a href="添加点label(1-1-6).md">1.1.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="64.13641364136414%" headers="mcps1.2.5.1.3 "><p id="p1130113318374"><a name="p1130113318374"></a><a name="p1130113318374"></a>POST /ges/v1.0/{project_id}/graphs/{graph_name}/vertices/{vertex_id}/labels</p>
</td>
<td class="cellrowborder" valign="top" width="15.251525152515253%" headers="mcps1.2.5.1.4 "><p id="p13013317372"><a name="p13013317372"></a><a name="p13013317372"></a>添加点label。</p>
</td>
</tr>
<tr id="row128136537387"><td class="cellrowborder" valign="top" width="13.741374137413743%" headers="mcps1.2.5.1.1 "><p id="p9813105317387"><a name="p9813105317387"></a><a name="p9813105317387"></a>查询元数据详情</p>
</td>
<td class="cellrowborder" valign="top" width="6.8706870687068715%" headers="mcps1.2.5.1.2 "><p id="p11239135143113"><a name="p11239135143113"></a><a name="p11239135143113"></a><a href="查询图元数据详情(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="64.13641364136414%" headers="mcps1.2.5.1.3 "><p id="p155357257412"><a name="p155357257412"></a><a name="p155357257412"></a>GET /ges/v1.0/{project_id}/graphs/{graph_name}/schema</p>
</td>
<td class="cellrowborder" valign="top" width="15.251525152515253%" headers="mcps1.2.5.1.4 "><p id="p1481395363811"><a name="p1481395363811"></a><a name="p1481395363811"></a>查询元数据详情。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  索引操作API

<a name="table1118427174912"></a>
<table><thead align="left"><tr id="row13119152710491"><th class="cellrowborder" valign="top" width="9.86%" id="mcps1.2.5.1.1"><p id="p957784412493"><a name="p957784412493"></a><a name="p957784412493"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="5.91%" id="mcps1.2.5.1.2"><p id="p14577944114917"><a name="p14577944114917"></a><a name="p14577944114917"></a>版本</p>
</th>
<th class="cellrowborder" valign="top" width="62.86000000000001%" id="mcps1.2.5.1.3"><p id="p19577184416490"><a name="p19577184416490"></a><a name="p19577184416490"></a>URL</p>
</th>
<th class="cellrowborder" valign="top" width="21.37%" id="mcps1.2.5.1.4"><p id="p65779445495"><a name="p65779445495"></a><a name="p65779445495"></a>功能描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row01191627184913"><td class="cellrowborder" valign="top" width="9.86%" headers="mcps1.2.5.1.1 "><p id="p1611962711494"><a name="p1611962711494"></a><a name="p1611962711494"></a>新建索引</p>
</td>
<td class="cellrowborder" valign="top" width="5.91%" headers="mcps1.2.5.1.2 "><p id="p11119142754913"><a name="p11119142754913"></a><a name="p11119142754913"></a><a href="新建索引(1-1-6).md">1.1.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="62.86000000000001%" headers="mcps1.2.5.1.3 "><p id="p1623885116452"><a name="p1623885116452"></a><a name="p1623885116452"></a>POST /ges/v1.0/{project_id}/graphs/{graph_name}/indices</p>
</td>
<td class="cellrowborder" valign="top" width="21.37%" headers="mcps1.2.5.1.4 "><p id="p1518573615218"><a name="p1518573615218"></a><a name="p1518573615218"></a>新建索引。</p>
</td>
</tr>
<tr id="row1011912270490"><td class="cellrowborder" valign="top" width="9.86%" headers="mcps1.2.5.1.1 "><p id="p611992714494"><a name="p611992714494"></a><a name="p611992714494"></a>删除索引</p>
</td>
<td class="cellrowborder" valign="top" width="5.91%" headers="mcps1.2.5.1.2 "><p id="p083131317919"><a name="p083131317919"></a><a name="p083131317919"></a><a href="删除索引(1-1-6).md">1.1.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="62.86000000000001%" headers="mcps1.2.5.1.3 "><p id="p15335195934516"><a name="p15335195934516"></a><a name="p15335195934516"></a>DELETE /ges/v1.0/{project_id}/graphs/{graph_name}/indices/{indexName}</p>
</td>
<td class="cellrowborder" valign="top" width="21.37%" headers="mcps1.2.5.1.4 "><p id="p818573645219"><a name="p818573645219"></a><a name="p818573645219"></a>删除索引。</p>
</td>
</tr>
<tr id="row497616107501"><td class="cellrowborder" valign="top" width="9.86%" headers="mcps1.2.5.1.1 "><p id="p1097781095010"><a name="p1097781095010"></a><a name="p1097781095010"></a>查询索引</p>
</td>
<td class="cellrowborder" valign="top" width="5.91%" headers="mcps1.2.5.1.2 "><p id="p0100513897"><a name="p0100513897"></a><a name="p0100513897"></a><a href="查询索引(1-1-6).md">1.1.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="62.86000000000001%" headers="mcps1.2.5.1.3 "><p id="p75082913464"><a name="p75082913464"></a><a name="p75082913464"></a>GET /ges/v1.0/{project_id}/graphs/{graph_name}/indices</p>
</td>
<td class="cellrowborder" valign="top" width="21.37%" headers="mcps1.2.5.1.4 "><p id="p118513619522"><a name="p118513619522"></a><a name="p118513619522"></a>查询索引。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  Gremlin操作API

<a name="table11921448105220"></a>
<table><thead align="left"><tr id="row59229488522"><th class="cellrowborder" valign="top" width="14.13%" id="mcps1.2.5.1.1"><p id="p4958101410537"><a name="p4958101410537"></a><a name="p4958101410537"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="8.16%" id="mcps1.2.5.1.2"><p id="p1695818141531"><a name="p1695818141531"></a><a name="p1695818141531"></a>版本</p>
</th>
<th class="cellrowborder" valign="top" width="50.07%" id="mcps1.2.5.1.3"><p id="p795811415535"><a name="p795811415535"></a><a name="p795811415535"></a>URL</p>
</th>
<th class="cellrowborder" valign="top" width="27.639999999999997%" id="mcps1.2.5.1.4"><p id="p199587145532"><a name="p199587145532"></a><a name="p199587145532"></a>功能描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1292320486520"><td class="cellrowborder" valign="top" width="14.13%" headers="mcps1.2.5.1.1 "><p id="p1989461645415"><a name="p1989461645415"></a><a name="p1989461645415"></a>执行Gremlin查询</p>
</td>
<td class="cellrowborder" valign="top" width="8.16%" headers="mcps1.2.5.1.2 "><p id="p1492344865211"><a name="p1492344865211"></a><a name="p1492344865211"></a><a href="执行Gremlin查询(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="50.07%" headers="mcps1.2.5.1.3 "><p id="p15900154575419"><a name="p15900154575419"></a><a name="p15900154575419"></a>POST /ges/v1.0/{project_id}/graphs/{graph_name}/action?action_id=execute-gremlin-query</p>
</td>
<td class="cellrowborder" valign="top" width="27.639999999999997%" headers="mcps1.2.5.1.4 "><p id="p6923948195212"><a name="p6923948195212"></a><a name="p6923948195212"></a>执行Gremlin查询。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  算法API

<a name="table155439525540"></a>
<table><thead align="left"><tr id="row165438525544"><th class="cellrowborder" valign="top" width="11.219999999999999%" id="mcps1.2.5.1.1"><p id="p42500515518"><a name="p42500515518"></a><a name="p42500515518"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="6.93%" id="mcps1.2.5.1.2"><p id="p6118948163410"><a name="p6118948163410"></a><a name="p6118948163410"></a>版本</p>
</th>
<th class="cellrowborder" valign="top" width="53.900000000000006%" id="mcps1.2.5.1.3"><p id="p18250115175517"><a name="p18250115175517"></a><a name="p18250115175517"></a>URL</p>
</th>
<th class="cellrowborder" valign="top" width="27.950000000000003%" id="mcps1.2.5.1.4"><p id="p22507545512"><a name="p22507545512"></a><a name="p22507545512"></a>功能描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row155441952165412"><td class="cellrowborder" valign="top" width="11.219999999999999%" headers="mcps1.2.5.1.1 "><p id="p105447522544"><a name="p105447522544"></a><a name="p105447522544"></a>执行算法</p>
</td>
<td class="cellrowborder" valign="top" width="6.93%" headers="mcps1.2.5.1.2 "><p id="p121181848193410"><a name="p121181848193410"></a><a name="p121181848193410"></a><a href="执行算法(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="53.900000000000006%" headers="mcps1.2.5.1.3 "><p id="p9327573551"><a name="p9327573551"></a><a name="p9327573551"></a>POST /ges/v1.0/{project_id}/graphs/{graph_name}/action?action_id=execute-algorithm</p>
</td>
<td class="cellrowborder" valign="top" width="27.950000000000003%" headers="mcps1.2.5.1.4 "><p id="p18444182417014"><a name="p18444182417014"></a><a name="p18444182417014"></a>执行算法。</p>
</td>
</tr>
</tbody>
</table>

**表 7**  路径API

<a name="table735132320325"></a>
<table><thead align="left"><tr id="row1736132323219"><th class="cellrowborder" valign="top" width="11.219999999999999%" id="mcps1.2.5.1.1"><p id="p123612311321"><a name="p123612311321"></a><a name="p123612311321"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="6.4%" id="mcps1.2.5.1.2"><p id="p63682363218"><a name="p63682363218"></a><a name="p63682363218"></a>版本</p>
</th>
<th class="cellrowborder" valign="top" width="54.43%" id="mcps1.2.5.1.3"><p id="p193662313326"><a name="p193662313326"></a><a name="p193662313326"></a>URL</p>
</th>
<th class="cellrowborder" valign="top" width="27.950000000000003%" id="mcps1.2.5.1.4"><p id="p136723103214"><a name="p136723103214"></a><a name="p136723103214"></a>功能描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row537162363213"><td class="cellrowborder" valign="top" width="11.219999999999999%" headers="mcps1.2.5.1.1 "><p id="p103782317322"><a name="p103782317322"></a><a name="p103782317322"></a>查询路径详情</p>
</td>
<td class="cellrowborder" valign="top" width="6.4%" headers="mcps1.2.5.1.2 "><p id="p10371623143211"><a name="p10371623143211"></a><a name="p10371623143211"></a><a href="查询路径详情(1-1-6).md">1.1.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="54.43%" headers="mcps1.2.5.1.3 "><p id="p8381323123211"><a name="p8381323123211"></a><a name="p8381323123211"></a>POST /ges/v1.0/{project_id}/graphs/{graph_name}/paths/action?action_id=query-detail</p>
</td>
<td class="cellrowborder" valign="top" width="27.950000000000003%" headers="mcps1.2.5.1.4 "><p id="p43862393215"><a name="p43862393215"></a><a name="p43862393215"></a>查询路径详情。</p>
</td>
</tr>
</tbody>
</table>

**表 8**  图统计API

<a name="table1178265135611"></a>
<table><thead align="left"><tr id="row6783105135614"><th class="cellrowborder" valign="top" width="14.108589141085892%" id="mcps1.2.5.1.1"><p id="p1830693955714"><a name="p1830693955714"></a><a name="p1830693955714"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="7.7792220777922205%" id="mcps1.2.5.1.2"><p id="p9306123919573"><a name="p9306123919573"></a><a name="p9306123919573"></a>版本</p>
</th>
<th class="cellrowborder" valign="top" width="50.70492950704929%" id="mcps1.2.5.1.3"><p id="p1530613925710"><a name="p1530613925710"></a><a name="p1530613925710"></a>URL</p>
</th>
<th class="cellrowborder" valign="top" width="27.407259274072594%" id="mcps1.2.5.1.4"><p id="p33061739185718"><a name="p33061739185718"></a><a name="p33061739185718"></a>功能描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1578385110566"><td class="cellrowborder" valign="top" width="14.108589141085892%" headers="mcps1.2.5.1.1 "><p id="p378375118567"><a name="p378375118567"></a><a name="p378375118567"></a>查询图概要信息</p>
</td>
<td class="cellrowborder" valign="top" width="7.7792220777922205%" headers="mcps1.2.5.1.2 "><p id="p978318518567"><a name="p978318518567"></a><a name="p978318518567"></a><a href="查询图概要信息(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="50.70492950704929%" headers="mcps1.2.5.1.3 "><p id="p1887131115612"><a name="p1887131115612"></a><a name="p1887131115612"></a>GET /ges/v1.0/{project_id}/graphs/{graph_name}/summary</p>
</td>
<td class="cellrowborder" valign="top" width="27.407259274072594%" headers="mcps1.2.5.1.4 "><p id="p387631816014"><a name="p387631816014"></a><a name="p387631816014"></a>查询图概要信息。</p>
</td>
</tr>
<tr id="row187831151195619"><td class="cellrowborder" valign="top" width="14.108589141085892%" headers="mcps1.2.5.1.1 "><p id="p16783155112568"><a name="p16783155112568"></a><a name="p16783155112568"></a>查询图版本</p>
</td>
<td class="cellrowborder" valign="top" width="7.7792220777922205%" headers="mcps1.2.5.1.2 "><p id="p1478395112568"><a name="p1478395112568"></a><a name="p1478395112568"></a><a href="查询图版本（2-0-0）.md">2.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="50.70492950704929%" headers="mcps1.2.5.1.3 "><p id="p181471614125612"><a name="p181471614125612"></a><a name="p181471614125612"></a>GET /ges/v1.0/{project_id}/graphs/{graph_name}/version</p>
</td>
<td class="cellrowborder" valign="top" width="27.407259274072594%" headers="mcps1.2.5.1.4 "><p id="p087611815011"><a name="p087611815011"></a><a name="p087611815011"></a>查询图版本。</p>
</td>
</tr>
</tbody>
</table>

**表 9**  子图操作API

<a name="table1585612113416"></a>
<table><thead align="left"><tr id="row98571021183413"><th class="cellrowborder" valign="top" width="11.95%" id="mcps1.2.5.1.1"><p id="p188571621183413"><a name="p188571621183413"></a><a name="p188571621183413"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="7.62%" id="mcps1.2.5.1.2"><p id="p1678314017335"><a name="p1678314017335"></a><a name="p1678314017335"></a>版本</p>
</th>
<th class="cellrowborder" valign="top" width="33.47%" id="mcps1.2.5.1.3"><p id="p2857142143413"><a name="p2857142143413"></a><a name="p2857142143413"></a>URL</p>
</th>
<th class="cellrowborder" valign="top" width="46.96%" id="mcps1.2.5.1.4"><p id="p317710911203"><a name="p317710911203"></a><a name="p317710911203"></a>功能描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row14705182925719"><td class="cellrowborder" valign="top" width="11.95%" headers="mcps1.2.5.1.1 "><p id="p10705429105714"><a name="p10705429105714"></a><a name="p10705429105714"></a>子图查询</p>
</td>
<td class="cellrowborder" valign="top" width="7.62%" headers="mcps1.2.5.1.2 "><p id="p1470511294575"><a name="p1470511294575"></a><a name="p1470511294575"></a><a href="子图查询(2-1-13).md">2.1.13</a></p>
</td>
<td class="cellrowborder" valign="top" width="33.47%" headers="mcps1.2.5.1.3 "><p id="p370552913578"><a name="p370552913578"></a><a name="p370552913578"></a>POST/ges/v1.0/{project_id}/graphs/{graph_name}/subgraphs/action?action_id=query</p>
</td>
<td class="cellrowborder" valign="top" width="46.96%" headers="mcps1.2.5.1.4 "><p id="p170516293572"><a name="p170516293572"></a><a name="p170516293572"></a>查询输入的节点和它们之间所有边所构成的子图。</p>
</td>
</tr>
</tbody>
</table>

**表 10**  Job管理相关接口

<a name="table18909727165717"></a>
<table><thead align="left"><tr id="row3910192716570"><th class="cellrowborder" valign="top" width="14.510000000000002%" id="mcps1.2.5.1.1"><p id="p15730141155919"><a name="p15730141155919"></a><a name="p15730141155919"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="7.68%" id="mcps1.2.5.1.2"><p id="p073013115598"><a name="p073013115598"></a><a name="p073013115598"></a>版本</p>
</th>
<th class="cellrowborder" valign="top" width="50.93%" id="mcps1.2.5.1.3"><p id="p13730511195917"><a name="p13730511195917"></a><a name="p13730511195917"></a>URL</p>
</th>
<th class="cellrowborder" valign="top" width="26.88%" id="mcps1.2.5.1.4"><p id="p6730151165919"><a name="p6730151165919"></a><a name="p6730151165919"></a>功能描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row16910112755719"><td class="cellrowborder" valign="top" width="14.510000000000002%" headers="mcps1.2.5.1.1 "><p id="p591092713577"><a name="p591092713577"></a><a name="p591092713577"></a>查询Job状态</p>
</td>
<td class="cellrowborder" valign="top" width="7.68%" headers="mcps1.2.5.1.2 "><p id="p29101827105716"><a name="p29101827105716"></a><a name="p29101827105716"></a><a href="查询Job状态(1-0-0)-业务面.md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="50.93%" headers="mcps1.2.5.1.3 "><p id="p129841312134016"><a name="p129841312134016"></a><a name="p129841312134016"></a>GET/ges/v1.0/{project_id}/graphs/{graph_name}/jobs/{job_id}/status?offset=<em id="i9984201214012"><a name="i9984201214012"></a><a name="i9984201214012"></a>offset</em>&amp;limit=<em id="i5984912184017"><a name="i5984912184017"></a><a name="i5984912184017"></a>limit</em></p>
</td>
<td class="cellrowborder" valign="top" width="26.88%" headers="mcps1.2.5.1.4 "><p id="p174320287110"><a name="p174320287110"></a><a name="p174320287110"></a>查询Job状态。</p>
</td>
</tr>
<tr id="row2317724115910"><td class="cellrowborder" valign="top" width="14.510000000000002%" headers="mcps1.2.5.1.1 "><p id="p143172024125918"><a name="p143172024125918"></a><a name="p143172024125918"></a>取消Job</p>
</td>
<td class="cellrowborder" valign="top" width="7.68%" headers="mcps1.2.5.1.2 "><p id="p7318152475916"><a name="p7318152475916"></a><a name="p7318152475916"></a><a href="取消Job(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="50.93%" headers="mcps1.2.5.1.3 "><p id="p320117497564"><a name="p320117497564"></a><a name="p320117497564"></a>DELETE https://Endpoint/ges/v1.0/{project_id}/graphs/{graph_name}/jobs/{job_id}</p>
</td>
<td class="cellrowborder" valign="top" width="26.88%" headers="mcps1.2.5.1.4 "><p id="p1543214284116"><a name="p1543214284116"></a><a name="p1543214284116"></a>取消Job。</p>
</td>
</tr>
<tr id="row13543124418392"><td class="cellrowborder" valign="top" width="14.510000000000002%" headers="mcps1.2.5.1.1 "><p id="p25431744113917"><a name="p25431744113917"></a><a name="p25431744113917"></a>导出job返回结果到文件</p>
</td>
<td class="cellrowborder" valign="top" width="7.68%" headers="mcps1.2.5.1.2 "><p id="p125431944183914"><a name="p125431944183914"></a><a name="p125431944183914"></a><a href="导出job返回结果到文件(2-2-1).md">2.2.1</a></p>
</td>
<td class="cellrowborder" valign="top" width="50.93%" headers="mcps1.2.5.1.3 "><p id="p105431944163911"><a name="p105431944163911"></a><a name="p105431944163911"></a>POST /ges/v1.0/{project_id}/graphs/{graph_name}/jobs/{job_id}/action?action_id=export-result</p>
</td>
<td class="cellrowborder" valign="top" width="26.88%" headers="mcps1.2.5.1.4 "><p id="p10543144113916"><a name="p10543144113916"></a><a name="p10543144113916"></a>用于将异步任务（job_id）的执行结果（result）导出到文件。</p>
</td>
</tr>
<tr id="row198619414395"><td class="cellrowborder" valign="top" width="14.510000000000002%" headers="mcps1.2.5.1.1 "><p id="p1088124163917"><a name="p1088124163917"></a><a name="p1088124163917"></a>查询job列表</p>
</td>
<td class="cellrowborder" valign="top" width="7.68%" headers="mcps1.2.5.1.2 "><p id="p2888411395"><a name="p2888411395"></a><a name="p2888411395"></a><a href="查询job列表(2-2-13).md">2.2.13</a></p>
</td>
<td class="cellrowborder" valign="top" width="50.93%" headers="mcps1.2.5.1.3 "><p id="p13881241163911"><a name="p13881241163911"></a><a name="p13881241163911"></a>GET /ges/v1.0/{project_id}/graphs/{graph_name}/jobs/status?limit={limit}&amp;offset={offset}</p>
</td>
<td class="cellrowborder" valign="top" width="26.88%" headers="mcps1.2.5.1.4 "><p id="p12609929152211"><a name="p12609929152211"></a><a name="p12609929152211"></a>异步任务jobId返回后，若jobId业务层丢失无法通过接口重新获取，现在提供一个新的接口用于查询engine中保存的所有异步任务，返回每个任务的jobId、job状态、原始请求。</p>
</td>
</tr>
</tbody>
</table>

**表 11**  其他业务面API

<a name="table196021581419"></a>
<table><thead align="left"><tr id="row1160255161414"><th class="cellrowborder" valign="top" width="24.39%" id="mcps1.2.5.1.1"><p id="p161212281413"><a name="p161212281413"></a><a name="p161212281413"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="12.770000000000001%" id="mcps1.2.5.1.2"><p id="p7612132216144"><a name="p7612132216144"></a><a name="p7612132216144"></a>版本</p>
</th>
<th class="cellrowborder" valign="top" width="37.84%" id="mcps1.2.5.1.3"><p id="p18612122221415"><a name="p18612122221415"></a><a name="p18612122221415"></a>URL</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="p461214228148"><a name="p461214228148"></a><a name="p461214228148"></a>功能描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row3603357142"><td class="cellrowborder" valign="top" width="24.39%" headers="mcps1.2.5.1.1 "><p id="p116032561411"><a name="p116032561411"></a><a name="p116032561411"></a>Filtered-query API</p>
</td>
<td class="cellrowborder" valign="top" width="12.770000000000001%" headers="mcps1.2.5.1.2 "><p id="p1160312512140"><a name="p1160312512140"></a><a name="p1160312512140"></a><a href="Filtered-query-API(2-2-13).md">2.2.15</a></p>
</td>
<td class="cellrowborder" valign="top" width="37.84%" headers="mcps1.2.5.1.3 "><p id="p166034571416"><a name="p166034571416"></a><a name="p166034571416"></a>POST /ges/v1.0/{project_id}/graphs/{graph_name}/action?action_id=filtered-query</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p17603165191417"><a name="p17603165191417"></a><a name="p17603165191417"></a>对k跳过程进行逐层过滤，列出满足过滤条件的第k跳节点或边。</p>
</td>
</tr>
<tr id="row260395121411"><td class="cellrowborder" valign="top" width="24.39%" headers="mcps1.2.5.1.1 "><p id="p16037513144"><a name="p16037513144"></a><a name="p16037513144"></a>通过导入文件更新点边的指定属性</p>
</td>
<td class="cellrowborder" valign="top" width="12.770000000000001%" headers="mcps1.2.5.1.2 "><p id="p2603145181415"><a name="p2603145181415"></a><a name="p2603145181415"></a><a href="通过导入文件更新点边的指定属性(2-2-13).md">2.2.13</a></p>
</td>
<td class="cellrowborder" valign="top" width="37.84%" headers="mcps1.2.5.1.3 "><p id="p8603359146"><a name="p8603359146"></a><a name="p8603359146"></a>POST  /v1.0/{project_id}/graphs/{graph_name}/action?action_id=import-properties</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p26037531413"><a name="p26037531413"></a><a name="p26037531413"></a>通过导入文件更新点边的指定属性。</p>
</td>
</tr>
</tbody>
</table>


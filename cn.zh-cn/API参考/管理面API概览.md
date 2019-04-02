# 管理面API概览<a name="ges_03_0113"></a>

GES管理面API包括系统管理，图管理，备份管理，元数据管理和任务中心五类。

**表 1**  系统管理API

<a name="table7304174193110"></a>
<table><thead align="left"><tr id="row153051646317"><th class="cellrowborder" valign="top" width="6.050228310502283%" id="mcps1.2.6.1.1"><p id="p53050493116"><a name="p53050493116"></a><a name="p53050493116"></a>序号</p>
</th>
<th class="cellrowborder" valign="top" width="11.120624048706238%" id="mcps1.2.6.1.2"><p id="p830519413120"><a name="p830519413120"></a><a name="p830519413120"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="5.717275494672754%" id="mcps1.2.6.1.3"><p id="p16968121125"><a name="p16968121125"></a><a name="p16968121125"></a>版本</p>
</th>
<th class="cellrowborder" valign="top" width="33.63774733637747%" id="mcps1.2.6.1.4"><p id="p173057463116"><a name="p173057463116"></a><a name="p173057463116"></a>URL</p>
</th>
<th class="cellrowborder" valign="top" width="43.47412480974124%" id="mcps1.2.6.1.5"><p id="p18782114810321"><a name="p18782114810321"></a><a name="p18782114810321"></a>功能描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row530514411314"><td class="cellrowborder" valign="top" width="6.050228310502283%" headers="mcps1.2.6.1.1 "><p id="p1830511418318"><a name="p1830511418318"></a><a name="p1830511418318"></a>1</p>
</td>
<td class="cellrowborder" valign="top" width="11.120624048706238%" headers="mcps1.2.6.1.2 "><p id="p43066403111"><a name="p43066403111"></a><a name="p43066403111"></a>查询配额</p>
</td>
<td class="cellrowborder" valign="top" width="5.717275494672754%" headers="mcps1.2.6.1.3 "><p id="p49687211420"><a name="p49687211420"></a><a name="p49687211420"></a><a href="查询配额(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="33.63774733637747%" headers="mcps1.2.6.1.4 "><p id="p79219119479"><a name="p79219119479"></a><a name="p79219119479"></a>GET /v1.0/{projectId}/graphs/quotas</p>
</td>
<td class="cellrowborder" valign="top" width="43.47412480974124%" headers="mcps1.2.6.1.5 "><p id="p144781316552"><a name="p144781316552"></a><a name="p144781316552"></a>查询图个数、边数以及备份个数配额。创建图或者图备份操作时，可以调用该API查看配额，避免报错配额不足。</p>
</td>
</tr>
<tr id="row23061417313"><td class="cellrowborder" valign="top" width="6.050228310502283%" headers="mcps1.2.6.1.1 "><p id="p430619413315"><a name="p430619413315"></a><a name="p430619413315"></a>2</p>
</td>
<td class="cellrowborder" valign="top" width="11.120624048706238%" headers="mcps1.2.6.1.2 "><p id="p430611414311"><a name="p430611414311"></a><a name="p430611414311"></a>校验元数据文件</p>
</td>
<td class="cellrowborder" valign="top" width="5.717275494672754%" headers="mcps1.2.6.1.3 "><p id="p79691521928"><a name="p79691521928"></a><a name="p79691521928"></a><a href="校验元数据文件(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="33.63774733637747%" headers="mcps1.2.6.1.4 "><p id="p16419151612479"><a name="p16419151612479"></a><a name="p16419151612479"></a>POST /v1.0/{projectId}/graphs/action?action_id=check-schema</p>
</td>
<td class="cellrowborder" valign="top" width="43.47412480974124%" headers="mcps1.2.6.1.5 "><p id="p68713276247"><a name="p68713276247"></a><a name="p68713276247"></a>校验元数据文件和点、边数据集是否匹配。创建有初始数据的图或者增量导入图时，可以调用该API校验点、边数据集和元数据是否匹配。</p>
</td>
</tr>
</tbody>
</table>

**表 2**  图管理API

<a name="table1585612113416"></a>
<table><thead align="left"><tr id="row98571021183413"><th class="cellrowborder" valign="top" width="6.683215581439756%" id="mcps1.2.6.1.1"><p id="p685792173412"><a name="p685792173412"></a><a name="p685792173412"></a>序号</p>
</th>
<th class="cellrowborder" valign="top" width="11.151422570173763%" id="mcps1.2.6.1.2"><p id="p188571621183413"><a name="p188571621183413"></a><a name="p188571621183413"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="7.1128508688180245%" id="mcps1.2.6.1.3"><p id="p1678314017335"><a name="p1678314017335"></a><a name="p1678314017335"></a>版本</p>
</th>
<th class="cellrowborder" valign="top" width="31.22971166698491%" id="mcps1.2.6.1.4"><p id="p2857142143413"><a name="p2857142143413"></a><a name="p2857142143413"></a>URL</p>
</th>
<th class="cellrowborder" valign="top" width="43.82279931258354%" id="mcps1.2.6.1.5"><p id="p317710911203"><a name="p317710911203"></a><a name="p317710911203"></a>功能描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row11858721113419"><td class="cellrowborder" valign="top" width="6.683215581439756%" headers="mcps1.2.6.1.1 "><p id="p68589215346"><a name="p68589215346"></a><a name="p68589215346"></a>1</p>
</td>
<td class="cellrowborder" valign="top" width="11.151422570173763%" headers="mcps1.2.6.1.2 "><p id="p78581211346"><a name="p78581211346"></a><a name="p78581211346"></a>查询图列表</p>
</td>
<td class="cellrowborder" valign="top" width="7.1128508688180245%" headers="mcps1.2.6.1.3 "><p id="p147834015334"><a name="p147834015334"></a><a name="p147834015334"></a><a href="查询图列表(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="31.22971166698491%" headers="mcps1.2.6.1.4 "><p id="p139041836161116"><a name="p139041836161116"></a><a name="p139041836161116"></a>GET  /v1.0/{projectId}/graphs?offset=<em id="i13904133601115"><a name="i13904133601115"></a><a name="i13904133601115"></a>{offset}</em>&amp;limit=<em id="i10904103661110"><a name="i10904103661110"></a><a name="i10904103661110"></a>{limit}</em></p>
</td>
<td class="cellrowborder" valign="top" width="43.82279931258354%" headers="mcps1.2.6.1.5 "><p id="p744761385510"><a name="p744761385510"></a><a name="p744761385510"></a>查看已经创建的所有图的列表。</p>
</td>
</tr>
<tr id="row13858521183413"><td class="cellrowborder" valign="top" width="6.683215581439756%" headers="mcps1.2.6.1.1 "><p id="p6858521123417"><a name="p6858521123417"></a><a name="p6858521123417"></a>2</p>
</td>
<td class="cellrowborder" valign="top" width="11.151422570173763%" headers="mcps1.2.6.1.2 "><p id="p18591621123417"><a name="p18591621123417"></a><a name="p18591621123417"></a>查询图详情</p>
</td>
<td class="cellrowborder" valign="top" width="7.1128508688180245%" headers="mcps1.2.6.1.3 "><p id="p15783130173313"><a name="p15783130173313"></a><a name="p15783130173313"></a><a href="查询图详情(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="31.22971166698491%" headers="mcps1.2.6.1.4 "><p id="p1961915192120"><a name="p1961915192120"></a><a name="p1961915192120"></a>GET /v1.0/{projectId}/graphs/{graphId}</p>
</td>
<td class="cellrowborder" valign="top" width="43.82279931258354%" headers="mcps1.2.6.1.5 "><p id="p204471913165512"><a name="p204471913165512"></a><a name="p204471913165512"></a>查询某个图的详情，包括图内网、公网访问地址，图版本号，图已经导入的点、边数据集。</p>
</td>
</tr>
<tr id="row2571642143417"><td class="cellrowborder" valign="top" width="6.683215581439756%" headers="mcps1.2.6.1.1 "><p id="p9572154211342"><a name="p9572154211342"></a><a name="p9572154211342"></a>3</p>
</td>
<td class="cellrowborder" valign="top" width="11.151422570173763%" headers="mcps1.2.6.1.2 "><p id="p145721142163415"><a name="p145721142163415"></a><a name="p145721142163415"></a>创建图</p>
</td>
<td class="cellrowborder" valign="top" width="7.1128508688180245%" headers="mcps1.2.6.1.3 "><p id="p12784110143314"><a name="p12784110143314"></a><a name="p12784110143314"></a><a href="创建图(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="31.22971166698491%" headers="mcps1.2.6.1.4 "><p id="p2573184614129"><a name="p2573184614129"></a><a name="p2573184614129"></a>POST /v1.0/{projectId}/graphs</p>
</td>
<td class="cellrowborder" valign="top" width="43.82279931258354%" headers="mcps1.2.6.1.5 "><p id="p64472013105513"><a name="p64472013105513"></a><a name="p64472013105513"></a>用户定义好图的元数据和点、边数据集后，下一步就是创建一个图。</p>
</td>
</tr>
<tr id="row257315426342"><td class="cellrowborder" valign="top" width="6.683215581439756%" headers="mcps1.2.6.1.1 "><p id="p9573134203418"><a name="p9573134203418"></a><a name="p9573134203418"></a>4</p>
</td>
<td class="cellrowborder" valign="top" width="11.151422570173763%" headers="mcps1.2.6.1.2 "><p id="p1257304223412"><a name="p1257304223412"></a><a name="p1257304223412"></a>关闭图</p>
</td>
<td class="cellrowborder" valign="top" width="7.1128508688180245%" headers="mcps1.2.6.1.3 "><p id="p1278417083320"><a name="p1278417083320"></a><a name="p1278417083320"></a><a href="关闭图(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="31.22971166698491%" headers="mcps1.2.6.1.4 "><p id="p41101158181210"><a name="p41101158181210"></a><a name="p41101158181210"></a>POST /v1.0/{projectId}/graphs/{graphId}/action?action_id=stop</p>
</td>
<td class="cellrowborder" valign="top" width="43.82279931258354%" headers="mcps1.2.6.1.5 "><p id="p4357151414316"><a name="p4357151414316"></a><a name="p4357151414316"></a>用户的业务不需要连续性，可以随时关闭图。停止后，图停止计费。</p>
</td>
</tr>
<tr id="row532741611352"><td class="cellrowborder" valign="top" width="6.683215581439756%" headers="mcps1.2.6.1.1 "><p id="p832731611352"><a name="p832731611352"></a><a name="p832731611352"></a>5</p>
</td>
<td class="cellrowborder" valign="top" width="11.151422570173763%" headers="mcps1.2.6.1.2 "><p id="p7328111693515"><a name="p7328111693515"></a><a name="p7328111693515"></a>启动图</p>
</td>
<td class="cellrowborder" valign="top" width="7.1128508688180245%" headers="mcps1.2.6.1.3 "><p id="p47841000339"><a name="p47841000339"></a><a name="p47841000339"></a><a href="启动图(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="31.22971166698491%" headers="mcps1.2.6.1.4 "><p id="p39535239138"><a name="p39535239138"></a><a name="p39535239138"></a>POST /v1.0/{projectId}/graphs/{graphId}/action?action_id=start</p>
</td>
<td class="cellrowborder" valign="top" width="43.82279931258354%" headers="mcps1.2.6.1.5 "><p id="p3300102063116"><a name="p3300102063116"></a><a name="p3300102063116"></a>用户关闭图后要再次使用图，可以把数据恢复到上次关闭状态或者恢复到某个备份时间点。</p>
</td>
</tr>
<tr id="row14656711182318"><td class="cellrowborder" valign="top" width="6.683215581439756%" headers="mcps1.2.6.1.1 "><p id="p6657151113235"><a name="p6657151113235"></a><a name="p6657151113235"></a>6</p>
</td>
<td class="cellrowborder" valign="top" width="11.151422570173763%" headers="mcps1.2.6.1.2 "><p id="p1865741102320"><a name="p1865741102320"></a><a name="p1865741102320"></a>删除图</p>
</td>
<td class="cellrowborder" valign="top" width="7.1128508688180245%" headers="mcps1.2.6.1.3 "><p id="p147845053318"><a name="p147845053318"></a><a name="p147845053318"></a><a href="删除图(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="31.22971166698491%" headers="mcps1.2.6.1.4 "><p id="p7914841191312"><a name="p7914841191312"></a><a name="p7914841191312"></a>DELETE /v1.0/{projectId}/graphs/{graphId}</p>
</td>
<td class="cellrowborder" valign="top" width="43.82279931258354%" headers="mcps1.2.6.1.5 "><p id="p7202591377"><a name="p7202591377"></a><a name="p7202591377"></a>用户不需要时可以删除图，删除后图停止计费。</p>
</td>
</tr>
<tr id="row9328181616355"><td class="cellrowborder" valign="top" width="6.683215581439756%" headers="mcps1.2.6.1.1 "><p id="p53281716103513"><a name="p53281716103513"></a><a name="p53281716103513"></a>7</p>
</td>
<td class="cellrowborder" valign="top" width="11.151422570173763%" headers="mcps1.2.6.1.2 "><p id="p173281716173511"><a name="p173281716173511"></a><a name="p173281716173511"></a>增量导入图</p>
</td>
<td class="cellrowborder" valign="top" width="7.1128508688180245%" headers="mcps1.2.6.1.3 "><p id="p16784708331"><a name="p16784708331"></a><a name="p16784708331"></a><a href="增量导入图(1-0-5).md">1.0.5</a></p>
</td>
<td class="cellrowborder" valign="top" width="31.22971166698491%" headers="mcps1.2.6.1.4 "><p id="p75231857191313"><a name="p75231857191313"></a><a name="p75231857191313"></a>POST  /v1.0/{projectId}/graphs/{graphId}/action?action_id=import-graph</p>
</td>
<td class="cellrowborder" valign="top" width="43.82279931258354%" headers="mcps1.2.6.1.5 "><p id="p466221311375"><a name="p466221311375"></a><a name="p466221311375"></a>用户需要批量导入数据。</p>
</td>
</tr>
<tr id="row63281716123519"><td class="cellrowborder" valign="top" width="6.683215581439756%" headers="mcps1.2.6.1.1 "><p id="p8329616123512"><a name="p8329616123512"></a><a name="p8329616123512"></a>8</p>
</td>
<td class="cellrowborder" valign="top" width="11.151422570173763%" headers="mcps1.2.6.1.2 "><p id="p1932941693512"><a name="p1932941693512"></a><a name="p1932941693512"></a>导出图</p>
</td>
<td class="cellrowborder" valign="top" width="7.1128508688180245%" headers="mcps1.2.6.1.3 "><p id="p87845073317"><a name="p87845073317"></a><a name="p87845073317"></a><a href="导出图(1-0-5).md">1.0.5</a></p>
</td>
<td class="cellrowborder" valign="top" width="31.22971166698491%" headers="mcps1.2.6.1.4 "><p id="p41821936121410"><a name="p41821936121410"></a><a name="p41821936121410"></a>POST /v1.0/{projectId}/graphs/{graphId}/action?action_id=export-graph</p>
</td>
<td class="cellrowborder" valign="top" width="43.82279931258354%" headers="mcps1.2.6.1.5 "><p id="p27213964113"><a name="p27213964113"></a><a name="p27213964113"></a>用户需要把图的所有数据导出为文本文件。</p>
</td>
</tr>
<tr id="row6329016103510"><td class="cellrowborder" valign="top" width="6.683215581439756%" headers="mcps1.2.6.1.1 "><p id="p63291416153512"><a name="p63291416153512"></a><a name="p63291416153512"></a>9</p>
</td>
<td class="cellrowborder" valign="top" width="11.151422570173763%" headers="mcps1.2.6.1.2 "><p id="p33291316153516"><a name="p33291316153516"></a><a name="p33291316153516"></a>清空图</p>
</td>
<td class="cellrowborder" valign="top" width="7.1128508688180245%" headers="mcps1.2.6.1.3 "><p id="p3784160153312"><a name="p3784160153312"></a><a name="p3784160153312"></a><a href="清空图(1-1-6).md">1.1.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="31.22971166698491%" headers="mcps1.2.6.1.4 "><p id="p43421051510"><a name="p43421051510"></a><a name="p43421051510"></a>POST /v1.0/{projectId}/graphs/{graphId}/action?action_id=clear-graph</p>
</td>
<td class="cellrowborder" valign="top" width="43.82279931258354%" headers="mcps1.2.6.1.5 "><p id="p1488511346440"><a name="p1488511346440"></a><a name="p1488511346440"></a>用户要把图的所有数据清空，包括点、边数据。</p>
<div class="note" id="note1880854513819"><a name="note1880854513819"></a><a name="note1880854513819"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p98099451689"><a name="p98099451689"></a><a name="p98099451689"></a>当前清空图不清除元数据。</p>
</div></div>
</td>
</tr>
<tr id="row119761512133613"><td class="cellrowborder" valign="top" width="6.683215581439756%" headers="mcps1.2.6.1.1 "><p id="p14976141223616"><a name="p14976141223616"></a><a name="p14976141223616"></a>10</p>
</td>
<td class="cellrowborder" valign="top" width="11.151422570173763%" headers="mcps1.2.6.1.2 "><p id="p197631263620"><a name="p197631263620"></a><a name="p197631263620"></a>升级图</p>
</td>
<td class="cellrowborder" valign="top" width="7.1128508688180245%" headers="mcps1.2.6.1.3 "><p id="p107841700334"><a name="p107841700334"></a><a name="p107841700334"></a><a href="升级图(1-0-5).md">1.0.5</a></p>
</td>
<td class="cellrowborder" valign="top" width="31.22971166698491%" headers="mcps1.2.6.1.4 "><p id="p168801769156"><a name="p168801769156"></a><a name="p168801769156"></a>POST  /v1.0/{projectId}/graphs/{graphId}/action?action_id=upgrade</p>
</td>
<td class="cellrowborder" valign="top" width="43.82279931258354%" headers="mcps1.2.6.1.5 "><p id="p1922594213468"><a name="p1922594213468"></a><a name="p1922594213468"></a>老版本的图有Bug或者需要增加新功能时，需要把老版本的图升级到新版本。</p>
</td>
</tr>
<tr id="row179763123363"><td class="cellrowborder" valign="top" width="6.683215581439756%" headers="mcps1.2.6.1.1 "><p id="p189771212123615"><a name="p189771212123615"></a><a name="p189771212123615"></a>11</p>
</td>
<td class="cellrowborder" valign="top" width="11.151422570173763%" headers="mcps1.2.6.1.2 "><p id="p8977131243612"><a name="p8977131243612"></a><a name="p8977131243612"></a>绑定EIP</p>
</td>
<td class="cellrowborder" valign="top" width="7.1128508688180245%" headers="mcps1.2.6.1.3 "><p id="p07841906333"><a name="p07841906333"></a><a name="p07841906333"></a><a href="绑定EIP(1-0-6).md">1.0.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="31.22971166698491%" headers="mcps1.2.6.1.4 "><p id="p12141315131511"><a name="p12141315131511"></a><a name="p12141315131511"></a>POST  /v1.0/{projectId}/graphs/{graphId}/action?action_id=bindEip</p>
</td>
<td class="cellrowborder" valign="top" width="43.82279931258354%" headers="mcps1.2.6.1.5 "><p id="p1917819175570"><a name="p1917819175570"></a><a name="p1917819175570"></a>用户需要在公网访问图时，需要绑定一个弹性公网IP。</p>
</td>
</tr>
<tr id="row1497713128367"><td class="cellrowborder" valign="top" width="6.683215581439756%" headers="mcps1.2.6.1.1 "><p id="p10977112183618"><a name="p10977112183618"></a><a name="p10977112183618"></a>12</p>
</td>
<td class="cellrowborder" valign="top" width="11.151422570173763%" headers="mcps1.2.6.1.2 "><p id="p139771212133618"><a name="p139771212133618"></a><a name="p139771212133618"></a>解绑EIP</p>
</td>
<td class="cellrowborder" valign="top" width="7.1128508688180245%" headers="mcps1.2.6.1.3 "><p id="p12785110103317"><a name="p12785110103317"></a><a name="p12785110103317"></a><a href="解绑EIP(1-0-6).md">1.0.6</a></p>
</td>
<td class="cellrowborder" valign="top" width="31.22971166698491%" headers="mcps1.2.6.1.4 "><p id="p9433102216151"><a name="p9433102216151"></a><a name="p9433102216151"></a>POST  /v1.0/{projectId}/graphs/{graphId}/action?action_id=unbindEip</p>
</td>
<td class="cellrowborder" valign="top" width="43.82279931258354%" headers="mcps1.2.6.1.5 "><p id="p05661959165017"><a name="p05661959165017"></a><a name="p05661959165017"></a>用户不需要在公网访问图时，可以把该图绑定的弹性公网IP解绑。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  备份管理API

<a name="table960610763713"></a>
<table><thead align="left"><tr id="row1860620723714"><th class="cellrowborder" valign="top" width="6.671749904689288%" id="mcps1.2.6.1.1"><p id="p12606177203719"><a name="p12606177203719"></a><a name="p12606177203719"></a>序号</p>
</th>
<th class="cellrowborder" valign="top" width="11.056042699199391%" id="mcps1.2.6.1.2"><p id="p360616713372"><a name="p360616713372"></a><a name="p360616713372"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="5.480365993137629%" id="mcps1.2.6.1.3"><p id="p638159414"><a name="p638159414"></a><a name="p638159414"></a>版本</p>
</th>
<th class="cellrowborder" valign="top" width="36.98055661456348%" id="mcps1.2.6.1.4"><p id="p1660727183720"><a name="p1660727183720"></a><a name="p1660727183720"></a>URL</p>
</th>
<th class="cellrowborder" valign="top" width="39.81128478841022%" id="mcps1.2.6.1.5"><p id="p714142102615"><a name="p714142102615"></a><a name="p714142102615"></a>功能描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1360707103714"><td class="cellrowborder" valign="top" width="6.671749904689288%" headers="mcps1.2.6.1.1 "><p id="p66071674373"><a name="p66071674373"></a><a name="p66071674373"></a>1</p>
</td>
<td class="cellrowborder" valign="top" width="11.056042699199391%" headers="mcps1.2.6.1.2 "><p id="p172908353375"><a name="p172908353375"></a><a name="p172908353375"></a>查看所有备份列表</p>
</td>
<td class="cellrowborder" valign="top" width="5.480365993137629%" headers="mcps1.2.6.1.3 "><p id="p16301554119"><a name="p16301554119"></a><a name="p16301554119"></a><a href="查看所有备份列表(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="36.98055661456348%" headers="mcps1.2.6.1.4 "><p id="p49354293377"><a name="p49354293377"></a><a name="p49354293377"></a>GET  /v1.0/{projectId}/graphs/backups?offset=<em id="i563613014535"><a name="i563613014535"></a><a name="i563613014535"></a>{offset}</em>&amp;limit=<em id="i93087349531"><a name="i93087349531"></a><a name="i93087349531"></a>{limit}</em></p>
</td>
<td class="cellrowborder" valign="top" width="39.81128478841022%" headers="mcps1.2.6.1.5 "><p id="p13980113411590"><a name="p13980113411590"></a><a name="p13980113411590"></a>查看所有图的所有备份详情。</p>
</td>
</tr>
<tr id="row1760715743717"><td class="cellrowborder" valign="top" width="6.671749904689288%" headers="mcps1.2.6.1.1 "><p id="p1260767163718"><a name="p1260767163718"></a><a name="p1260767163718"></a>2</p>
</td>
<td class="cellrowborder" valign="top" width="11.056042699199391%" headers="mcps1.2.6.1.2 "><p id="p492711291379"><a name="p492711291379"></a><a name="p492711291379"></a>查看某个图的备份列表</p>
</td>
<td class="cellrowborder" valign="top" width="5.480365993137629%" headers="mcps1.2.6.1.3 "><p id="p2318150411"><a name="p2318150411"></a><a name="p2318150411"></a><a href="查看某个图的备份列表(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="36.98055661456348%" headers="mcps1.2.6.1.4 "><p id="p33754919352"><a name="p33754919352"></a><a name="p33754919352"></a>GET  /v1.0/{projectId}/graphs/{graphId}/backups?offset=<em id="i203784953515"><a name="i203784953515"></a><a name="i203784953515"></a>{offset}</em>&amp;limit=<em id="i103724918357"><a name="i103724918357"></a><a name="i103724918357"></a>{limit}</em></p>
</td>
<td class="cellrowborder" valign="top" width="39.81128478841022%" headers="mcps1.2.6.1.5 "><p id="p13169152316113"><a name="p13169152316113"></a><a name="p13169152316113"></a>查看某个图下所有备份的详情，包括备份开始、结束时间等。</p>
</td>
</tr>
<tr id="row1153562443716"><td class="cellrowborder" valign="top" width="6.671749904689288%" headers="mcps1.2.6.1.1 "><p id="p95351424123712"><a name="p95351424123712"></a><a name="p95351424123712"></a>3</p>
</td>
<td class="cellrowborder" valign="top" width="11.056042699199391%" headers="mcps1.2.6.1.2 "><p id="p3535162413710"><a name="p3535162413710"></a><a name="p3535162413710"></a>新增备份</p>
</td>
<td class="cellrowborder" valign="top" width="5.480365993137629%" headers="mcps1.2.6.1.3 "><p id="p131015194117"><a name="p131015194117"></a><a name="p131015194117"></a><a href="新增备份(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="36.98055661456348%" headers="mcps1.2.6.1.4 "><p id="p35356240374"><a name="p35356240374"></a><a name="p35356240374"></a>POST  /v1.0/{projectId}/graphs/{graphId}/backups</p>
</td>
<td class="cellrowborder" valign="top" width="39.81128478841022%" headers="mcps1.2.6.1.5 "><p id="p691894318211"><a name="p691894318211"></a><a name="p691894318211"></a>备份用于增加数据可靠性，同时可以作为一个图的快照，方便恢复到该快照。</p>
</td>
</tr>
<tr id="row71911653387"><td class="cellrowborder" valign="top" width="6.671749904689288%" headers="mcps1.2.6.1.1 "><p id="p1619110517383"><a name="p1619110517383"></a><a name="p1619110517383"></a>4</p>
</td>
<td class="cellrowborder" valign="top" width="11.056042699199391%" headers="mcps1.2.6.1.2 "><p id="p1219112519383"><a name="p1219112519383"></a><a name="p1219112519383"></a>删除备份</p>
</td>
<td class="cellrowborder" valign="top" width="5.480365993137629%" headers="mcps1.2.6.1.3 "><p id="p53131512416"><a name="p53131512416"></a><a name="p53131512416"></a><a href="删除备份(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="36.98055661456348%" headers="mcps1.2.6.1.4 "><p id="p245053512151"><a name="p245053512151"></a><a name="p245053512151"></a>DELETE /v1.0/{projectId}/graphs/{graphId}/backups/{backupId}</p>
</td>
<td class="cellrowborder" valign="top" width="39.81128478841022%" headers="mcps1.2.6.1.5 "><p id="p15120642634"><a name="p15120642634"></a><a name="p15120642634"></a>删除某个图的备份。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  元数据管理API

<a name="table1818992893815"></a>
<table><thead align="left"><tr id="row1019018284387"><th class="cellrowborder" valign="top" width="6.825938566552901%" id="mcps1.2.6.1.1"><p id="p19190132893818"><a name="p19190132893818"></a><a name="p19190132893818"></a>序号</p>
</th>
<th class="cellrowborder" valign="top" width="10.970258410531446%" id="mcps1.2.6.1.2"><p id="p719019283383"><a name="p719019283383"></a><a name="p719019283383"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="5.5290102389078495%" id="mcps1.2.6.1.3"><p id="p13527133913501"><a name="p13527133913501"></a><a name="p13527133913501"></a>版本</p>
</th>
<th class="cellrowborder" valign="top" width="37.1526084836665%" id="mcps1.2.6.1.4"><p id="p519022815382"><a name="p519022815382"></a><a name="p519022815382"></a>URL</p>
</th>
<th class="cellrowborder" valign="top" width="39.522184300341294%" id="mcps1.2.6.1.5"><p id="p3685124313272"><a name="p3685124313272"></a><a name="p3685124313272"></a>功能描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1619192815383"><td class="cellrowborder" valign="top" width="6.825938566552901%" headers="mcps1.2.6.1.1 "><p id="p419122813811"><a name="p419122813811"></a><a name="p419122813811"></a>1</p>
</td>
<td class="cellrowborder" valign="top" width="10.970258410531446%" headers="mcps1.2.6.1.2 "><p id="p319152818381"><a name="p319152818381"></a><a name="p319152818381"></a>查询元数据列表</p>
</td>
<td class="cellrowborder" valign="top" width="5.5290102389078495%" headers="mcps1.2.6.1.3 "><p id="p1752813915019"><a name="p1752813915019"></a><a name="p1752813915019"></a><a href="查询元数据列表(1-0-2).md">1.0.2</a></p>
</td>
<td class="cellrowborder" valign="top" width="37.1526084836665%" headers="mcps1.2.6.1.4 "><p id="p5513191110367"><a name="p5513191110367"></a><a name="p5513191110367"></a>GET /v1.0/{projectId}/graphs/metadatas?offset=<em id="i14513411133611"><a name="i14513411133611"></a><a name="i14513411133611"></a>{offset}</em>&amp;limit=<em id="i1451391133617"><a name="i1451391133617"></a><a name="i1451391133617"></a>{limit}</em></p>
</td>
<td class="cellrowborder" valign="top" width="39.522184300341294%" headers="mcps1.2.6.1.5 "><p id="p17923212546"><a name="p17923212546"></a><a name="p17923212546"></a>查询所有元数据详情，包括状态、OBS存储路径。</p>
</td>
</tr>
<tr id="row1919120280385"><td class="cellrowborder" valign="top" width="6.825938566552901%" headers="mcps1.2.6.1.1 "><p id="p13191202863818"><a name="p13191202863818"></a><a name="p13191202863818"></a>2</p>
</td>
<td class="cellrowborder" valign="top" width="10.970258410531446%" headers="mcps1.2.6.1.2 "><p id="p1119192863814"><a name="p1119192863814"></a><a name="p1119192863814"></a>查询元数据</p>
</td>
<td class="cellrowborder" valign="top" width="5.5290102389078495%" headers="mcps1.2.6.1.3 "><p id="p0528163955012"><a name="p0528163955012"></a><a name="p0528163955012"></a><a href="查询元数据(1-0-2).md">1.0.2</a></p>
</td>
<td class="cellrowborder" valign="top" width="37.1526084836665%" headers="mcps1.2.6.1.4 "><p id="p7672200181719"><a name="p7672200181719"></a><a name="p7672200181719"></a>GET /v1.0/{projectId}/graphs/metadatas/{metadataId}</p>
</td>
<td class="cellrowborder" valign="top" width="39.522184300341294%" headers="mcps1.2.6.1.5 "><p id="p2090725914515"><a name="p2090725914515"></a><a name="p2090725914515"></a>查询某个元数据详情。</p>
</td>
</tr>
<tr id="row181928288385"><td class="cellrowborder" valign="top" width="6.825938566552901%" headers="mcps1.2.6.1.1 "><p id="p1219252873820"><a name="p1219252873820"></a><a name="p1219252873820"></a>3</p>
</td>
<td class="cellrowborder" valign="top" width="10.970258410531446%" headers="mcps1.2.6.1.2 "><p id="p219212289381"><a name="p219212289381"></a><a name="p219212289381"></a>新增元数据</p>
</td>
<td class="cellrowborder" valign="top" width="5.5290102389078495%" headers="mcps1.2.6.1.3 "><p id="p195281439115012"><a name="p195281439115012"></a><a name="p195281439115012"></a><a href="新增元数据(1-0-2).md">1.0.2</a></p>
</td>
<td class="cellrowborder" valign="top" width="37.1526084836665%" headers="mcps1.2.6.1.4 "><p id="p12222147191719"><a name="p12222147191719"></a><a name="p12222147191719"></a>POST /v1.0/{projectId}/graphs/metadatas</p>
</td>
<td class="cellrowborder" valign="top" width="39.522184300341294%" headers="mcps1.2.6.1.5 "><p id="p35534307619"><a name="p35534307619"></a><a name="p35534307619"></a>新增元数据为创建图之前的准备操作，用户必须先创建元数据才能创建图。</p>
</td>
</tr>
<tr id="row51931028143812"><td class="cellrowborder" valign="top" width="6.825938566552901%" headers="mcps1.2.6.1.1 "><p id="p119362816386"><a name="p119362816386"></a><a name="p119362816386"></a>4</p>
</td>
<td class="cellrowborder" valign="top" width="10.970258410531446%" headers="mcps1.2.6.1.2 "><p id="p14193142810385"><a name="p14193142810385"></a><a name="p14193142810385"></a>删除元数据</p>
</td>
<td class="cellrowborder" valign="top" width="5.5290102389078495%" headers="mcps1.2.6.1.3 "><p id="p105286397501"><a name="p105286397501"></a><a name="p105286397501"></a><a href="删除元数据(1-0-2).md">1.0.2</a></p>
</td>
<td class="cellrowborder" valign="top" width="37.1526084836665%" headers="mcps1.2.6.1.4 "><p id="p1769741441719"><a name="p1769741441719"></a><a name="p1769741441719"></a>DELETE /v1.0/{projectId}/graphs/metadatas/{metadataId}</p>
</td>
<td class="cellrowborder" valign="top" width="39.522184300341294%" headers="mcps1.2.6.1.5 "><p id="p1461312456610"><a name="p1461312456610"></a><a name="p1461312456610"></a>删除一个元数据。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  任务中心API

<a name="table1376523653912"></a>
<table><thead align="left"><tr id="row15766336153915"><th class="cellrowborder" valign="top" width="6.609339066093391%" id="mcps1.2.6.1.1"><p id="p16766436173915"><a name="p16766436173915"></a><a name="p16766436173915"></a>序号</p>
</th>
<th class="cellrowborder" valign="top" width="11.50884911508849%" id="mcps1.2.6.1.2"><p id="p1776619361391"><a name="p1776619361391"></a><a name="p1776619361391"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="5.669433056694331%" id="mcps1.2.6.1.3"><p id="p114297165149"><a name="p114297165149"></a><a name="p114297165149"></a>版本</p>
</th>
<th class="cellrowborder" valign="top" width="36.6963303669633%" id="mcps1.2.6.1.4"><p id="p176613614390"><a name="p176613614390"></a><a name="p176613614390"></a>URL</p>
</th>
<th class="cellrowborder" valign="top" width="39.51604839516049%" id="mcps1.2.6.1.5"><p id="p164743462817"><a name="p164743462817"></a><a name="p164743462817"></a>功能描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row107665363398"><td class="cellrowborder" valign="top" width="6.609339066093391%" headers="mcps1.2.6.1.1 "><p id="p207671736123912"><a name="p207671736123912"></a><a name="p207671736123912"></a>1</p>
</td>
<td class="cellrowborder" valign="top" width="11.50884911508849%" headers="mcps1.2.6.1.2 "><p id="p1083764711396"><a name="p1083764711396"></a><a name="p1083764711396"></a>查询Job状态</p>
</td>
<td class="cellrowborder" valign="top" width="5.669433056694331%" headers="mcps1.2.6.1.3 "><p id="p14429181621418"><a name="p14429181621418"></a><a name="p14429181621418"></a><a href="查询Job状态(1-0-0).md">1.0.0</a></p>
</td>
<td class="cellrowborder" valign="top" width="36.6963303669633%" headers="mcps1.2.6.1.4 "><p id="p1648846192"><a name="p1648846192"></a><a name="p1648846192"></a>GET /v1.0/{projectId}/graphs/{graphId}/jobs/{jobId}/status</p>
</td>
<td class="cellrowborder" valign="top" width="39.51604839516049%" headers="mcps1.2.6.1.5 "><p id="p15328941686"><a name="p15328941686"></a><a name="p15328941686"></a>图删除、关闭、启动、恢复、增量导入、清空、升级等API为异步任务，API会返回jobId，可以通过该接口查看异步任务执行状态。</p>
</td>
</tr>
<tr id="row576711364392"><td class="cellrowborder" valign="top" width="6.609339066093391%" headers="mcps1.2.6.1.1 "><p id="p476712365390"><a name="p476712365390"></a><a name="p476712365390"></a>2</p>
</td>
<td class="cellrowborder" valign="top" width="11.50884911508849%" headers="mcps1.2.6.1.2 "><p id="p198221647123920"><a name="p198221647123920"></a><a name="p198221647123920"></a>查询任务中心</p>
</td>
<td class="cellrowborder" valign="top" width="5.669433056694331%" headers="mcps1.2.6.1.3 "><p id="p12430131618142"><a name="p12430131618142"></a><a name="p12430131618142"></a><a href="查询任务中心(1-1-8).md">1.1.8</a></p>
</td>
<td class="cellrowborder" valign="top" width="36.6963303669633%" headers="mcps1.2.6.1.4 "><p id="p13316102521914"><a name="p13316102521914"></a><a name="p13316102521914"></a>GET /v1.0/{projectId}/graphs/jobs?offset=<em id="i131632541917"><a name="i131632541917"></a><a name="i131632541917"></a>{offset}</em>&amp;limit=<em id="i2316525191913"><a name="i2316525191913"></a><a name="i2316525191913"></a>{limit}</em></p>
</td>
<td class="cellrowborder" valign="top" width="39.51604839516049%" headers="mcps1.2.6.1.5 "><p id="p1543041919112"><a name="p1543041919112"></a><a name="p1543041919112"></a>用户查看所有的异步任务。</p>
</td>
</tr>
</tbody>
</table>


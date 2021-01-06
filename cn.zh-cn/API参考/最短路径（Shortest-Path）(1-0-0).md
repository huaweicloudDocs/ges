# 最短路径（Shortest Path）\(1.0.0\)<a name="ges_03_0081"></a>

**表 1**  parameters参数说明

<a name="table19248182611368"></a>
<table><thead align="left"><tr id="row126392663619"><th class="cellrowborder" valign="top" width="13.861386138613863%" id="mcps1.2.7.1.1"><p id="p126419262361"><a name="p126419262361"></a><a name="p126419262361"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="11.881188118811881%" id="mcps1.2.7.1.2"><p id="p1426852683619"><a name="p1426852683619"></a><a name="p1426852683619"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="17.82178217821782%" id="mcps1.2.7.1.3"><p id="p152731626153611"><a name="p152731626153611"></a><a name="p152731626153611"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="10.702970297029703%" id="mcps1.2.7.1.4"><p id="p119692498180"><a name="p119692498180"></a><a name="p119692498180"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="33.85148514851485%" id="mcps1.2.7.1.5"><p id="p14279162618361"><a name="p14279162618361"></a><a name="p14279162618361"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="11.881188118811881%" id="mcps1.2.7.1.6"><p id="p19958237181732"><a name="p19958237181732"></a><a name="p19958237181732"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row1028513263367"><td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.1 "><p id="p7287626113618"><a name="p7287626113618"></a><a name="p7287626113618"></a>source</p>
</td>
<td class="cellrowborder" valign="top" width="11.881188118811881%" headers="mcps1.2.7.1.2 "><p id="p14291026203615"><a name="p14291026203615"></a><a name="p14291026203615"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.7.1.3 "><p id="p12294142611362"><a name="p12294142611362"></a><a name="p12294142611362"></a>输入路径的起点ID。</p>
</td>
<td class="cellrowborder" valign="top" width="10.702970297029703%" headers="mcps1.2.7.1.4 "><p id="p19969174991814"><a name="p19969174991814"></a><a name="p19969174991814"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="33.85148514851485%" headers="mcps1.2.7.1.5 "><p id="p19637130201011"><a name="p19637130201011"></a><a name="p19637130201011"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.881188118811881%" headers="mcps1.2.7.1.6 "><p id="p6004471181732"><a name="p6004471181732"></a><a name="p6004471181732"></a>-</p>
</td>
</tr>
<tr id="row8305162610365"><td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.1 "><p id="p153088268366"><a name="p153088268366"></a><a name="p153088268366"></a>target</p>
</td>
<td class="cellrowborder" valign="top" width="11.881188118811881%" headers="mcps1.2.7.1.2 "><p id="p1131042614369"><a name="p1131042614369"></a><a name="p1131042614369"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.7.1.3 "><p id="p13312102617361"><a name="p13312102617361"></a><a name="p13312102617361"></a>输入路径的终点ID。</p>
</td>
<td class="cellrowborder" valign="top" width="10.702970297029703%" headers="mcps1.2.7.1.4 "><p id="p1896954920183"><a name="p1896954920183"></a><a name="p1896954920183"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="33.85148514851485%" headers="mcps1.2.7.1.5 "><p id="p1731912266365"><a name="p1731912266365"></a><a name="p1731912266365"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="11.881188118811881%" headers="mcps1.2.7.1.6 "><p id="p16600125181732"><a name="p16600125181732"></a><a name="p16600125181732"></a>-</p>
</td>
</tr>
<tr id="row38613385112333"><td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.1 "><p id="p40676518112333"><a name="p40676518112333"></a><a name="p40676518112333"></a>weight</p>
</td>
<td class="cellrowborder" valign="top" width="11.881188118811881%" headers="mcps1.2.7.1.2 "><p id="p6463651112333"><a name="p6463651112333"></a><a name="p6463651112333"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.7.1.3 "><p id="p53793704112333"><a name="p53793704112333"></a><a name="p53793704112333"></a>边上权重。</p>
</td>
<td class="cellrowborder" valign="top" width="10.702970297029703%" headers="mcps1.2.7.1.4 "><p id="p1496924971820"><a name="p1496924971820"></a><a name="p1496924971820"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="33.85148514851485%" headers="mcps1.2.7.1.5 "><p id="p1666044011283"><a name="p1666044011283"></a><a name="p1666044011283"></a>空或字符串。</p>
<a name="ul27814585182326"></a><a name="ul27814585182326"></a><ul id="ul27814585182326"><li>空：边上的权重、距离默认为<span class="parmname" id="parmname64281841182434"><a name="parmname64281841182434"></a><a name="parmname64281841182434"></a>“1”</span>。</li><li>字符串：对应的边上的属性将作为权重，当某边没有对应属性时，权重将默认为1。<div class="note" id="note1763697295448"><a name="note1763697295448"></a><a name="note1763697295448"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p6598326895457"><a name="p6598326895457"></a><a name="p6598326895457"></a>边上权重应大于0。</p>
</div></div>
</li></ul>
</td>
<td class="cellrowborder" valign="top" width="11.881188118811881%" headers="mcps1.2.7.1.6 "><p id="p2432921181732"><a name="p2432921181732"></a><a name="p2432921181732"></a>-</p>
</td>
</tr>
<tr id="row18578822113145"><td class="cellrowborder" valign="top" width="13.861386138613863%" headers="mcps1.2.7.1.1 "><p id="p28489604113145"><a name="p28489604113145"></a><a name="p28489604113145"></a>directed</p>
</td>
<td class="cellrowborder" valign="top" width="11.881188118811881%" headers="mcps1.2.7.1.2 "><p id="p25956591113145"><a name="p25956591113145"></a><a name="p25956591113145"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.7.1.3 "><p id="p22109102113145"><a name="p22109102113145"></a><a name="p22109102113145"></a>是否考虑边的方向。</p>
</td>
<td class="cellrowborder" valign="top" width="10.702970297029703%" headers="mcps1.2.7.1.4 "><p id="p4969649161820"><a name="p4969649161820"></a><a name="p4969649161820"></a>Bool</p>
</td>
<td class="cellrowborder" valign="top" width="33.85148514851485%" headers="mcps1.2.7.1.5 "><p id="p46006826113145"><a name="p46006826113145"></a><a name="p46006826113145"></a>true或false。</p>
</td>
<td class="cellrowborder" valign="top" width="11.881188118811881%" headers="mcps1.2.7.1.6 "><p id="p62848880181732"><a name="p62848880181732"></a><a name="p62848880181732"></a>false</p>
</td>
</tr>
</tbody>
</table>

**表 2**  response\_data参数说明

<a name="table57091914174612"></a>
<table><thead align="left"><tr id="row170991414610"><th class="cellrowborder" valign="top" width="23.732373237323735%" id="mcps1.2.4.1.1"><p id="p137091714114617"><a name="p137091714114617"></a><a name="p137091714114617"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="18.64186418641864%" id="mcps1.2.4.1.2"><p id="p0709101418461"><a name="p0709101418461"></a><a name="p0709101418461"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="57.625762576257635%" id="mcps1.2.4.1.3"><p id="p0709414134613"><a name="p0709414134613"></a><a name="p0709414134613"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row67091514124616"><td class="cellrowborder" valign="top" width="23.732373237323735%" headers="mcps1.2.4.1.1 "><p id="p1570971444617"><a name="p1570971444617"></a><a name="p1570971444617"></a>path</p>
</td>
<td class="cellrowborder" valign="top" width="18.64186418641864%" headers="mcps1.2.4.1.2 "><p id="p1724014144615"><a name="p1724014144615"></a><a name="p1724014144615"></a>List</p>
</td>
<td class="cellrowborder" valign="top" width="57.625762576257635%" headers="mcps1.2.4.1.3 "><p id="p11470316153614"><a name="p11470316153614"></a><a name="p11470316153614"></a>最短路径，格式：</p>
<p id="p751814202362"><a name="p751814202362"></a><a name="p751814202362"></a>[vertexId,...]</p>
<p id="p83008413714"><a name="p83008413714"></a><a name="p83008413714"></a>其中,</p>
<p id="p276931513620"><a name="p276931513620"></a><a name="p276931513620"></a>vertexId：string类型</p>
</td>
</tr>
<tr id="row3300326103714"><td class="cellrowborder" valign="top" width="23.732373237323735%" headers="mcps1.2.4.1.1 "><p id="p1930015260371"><a name="p1930015260371"></a><a name="p1930015260371"></a>source</p>
</td>
<td class="cellrowborder" valign="top" width="18.64186418641864%" headers="mcps1.2.4.1.2 "><p id="p14300112613716"><a name="p14300112613716"></a><a name="p14300112613716"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="57.625762576257635%" headers="mcps1.2.4.1.3 "><p id="p11300102620372"><a name="p11300102620372"></a><a name="p11300102620372"></a>起点ID</p>
</td>
</tr>
<tr id="row1472461414465"><td class="cellrowborder" valign="top" width="23.732373237323735%" headers="mcps1.2.4.1.1 "><p id="p27242014124617"><a name="p27242014124617"></a><a name="p27242014124617"></a>target</p>
</td>
<td class="cellrowborder" valign="top" width="18.64186418641864%" headers="mcps1.2.4.1.2 "><p id="p3724171418468"><a name="p3724171418468"></a><a name="p3724171418468"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="57.625762576257635%" headers="mcps1.2.4.1.3 "><p id="p472451414463"><a name="p472451414463"></a><a name="p472451414463"></a>终点ID</p>
</td>
</tr>
</tbody>
</table>


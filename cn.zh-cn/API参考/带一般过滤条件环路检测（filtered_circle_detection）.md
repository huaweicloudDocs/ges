# 带一般过滤条件环路检测（filtered\_circle\_detection）<a name="ges_03_0217"></a>

## 请求样例<a name="section1890495020228"></a>

```
Post http://{}/ges/v1.0/1/graphs/movie/action?action_id=execute-algorithm
{
    "algorithmName": "filtered_circle_detection",
    "parameters": {
        "n": 10,
        "statistics": true,
        "output_format":"edgeId"
    },
    "filters": [
        {
        },
        {
            "operator": "out",
            "edge_filter": {
                "property_filter": {
                    "leftvalue": {
                        "label_name": "labelName"
                    },
                    "predicate": "=",
                    "rightvalue": {
                        "value": "transfer"
                    }
                }
            },
            "times":5
        }
    ]
}
```

## 参数说明<a name="section789315103243"></a>

**表 1**  parameters参数说明

<a name="table1869112610263"></a>
<table><thead align="left"><tr id="row869132618268"><th class="cellrowborder" valign="top" width="16.666666666666664%" id="mcps1.2.7.1.1"><p id="p206911226192619"><a name="p206911226192619"></a><a name="p206911226192619"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10.827834433113377%" id="mcps1.2.7.1.2"><p id="p969242672619"><a name="p969242672619"></a><a name="p969242672619"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="26.7746450709858%" id="mcps1.2.7.1.3"><p id="p156920264262"><a name="p156920264262"></a><a name="p156920264262"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="10.207958408318337%" id="mcps1.2.7.1.4"><p id="p1269262692617"><a name="p1269262692617"></a><a name="p1269262692617"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="18.66626674665067%" id="mcps1.2.7.1.5"><p id="p176928260268"><a name="p176928260268"></a><a name="p176928260268"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="16.85662867426515%" id="mcps1.2.7.1.6"><p id="p769292612269"><a name="p769292612269"></a><a name="p769292612269"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row1569282692618"><td class="cellrowborder" valign="top" width="16.666666666666664%" headers="mcps1.2.7.1.1 "><p id="p1769252612617"><a name="p1769252612617"></a><a name="p1769252612617"></a>sources</p>
</td>
<td class="cellrowborder" valign="top" width="10.827834433113377%" headers="mcps1.2.7.1.2 "><p id="p16692132612620"><a name="p16692132612620"></a><a name="p16692132612620"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="26.7746450709858%" headers="mcps1.2.7.1.3 "><p id="p869262642614"><a name="p869262642614"></a><a name="p869262642614"></a>查询的起始节点ID集合</p>
</td>
<td class="cellrowborder" valign="top" width="10.207958408318337%" headers="mcps1.2.7.1.4 "><p id="p869210268260"><a name="p869210268260"></a><a name="p869210268260"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="18.66626674665067%" headers="mcps1.2.7.1.5 "><p id="p1869213264269"><a name="p1869213264269"></a><a name="p1869213264269"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="16.85662867426515%" headers="mcps1.2.7.1.6 "><p id="p1269220267267"><a name="p1269220267267"></a><a name="p1269220267267"></a>标准csv格式，ID之间以英文逗号分隔，例如:“Alice,Nana”</p>
</td>
</tr>
<tr id="row18692192615267"><td class="cellrowborder" valign="top" width="16.666666666666664%" headers="mcps1.2.7.1.1 "><p id="p069212261266"><a name="p069212261266"></a><a name="p069212261266"></a>n</p>
</td>
<td class="cellrowborder" valign="top" width="10.827834433113377%" headers="mcps1.2.7.1.2 "><p id="p206929268264"><a name="p206929268264"></a><a name="p206929268264"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="26.7746450709858%" headers="mcps1.2.7.1.3 "><p id="p14692102612265"><a name="p14692102612265"></a><a name="p14692102612265"></a>枚举的满足过滤条件的圈的个数的上限</p>
</td>
<td class="cellrowborder" valign="top" width="10.207958408318337%" headers="mcps1.2.7.1.4 "><p id="p1069211266266"><a name="p1069211266266"></a><a name="p1069211266266"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="18.66626674665067%" headers="mcps1.2.7.1.5 "><p id="p669211268268"><a name="p669211268268"></a><a name="p669211268268"></a>[1,100000]</p>
</td>
<td class="cellrowborder" valign="top" width="16.85662867426515%" headers="mcps1.2.7.1.6 "><p id="p13692172612616"><a name="p13692172612616"></a><a name="p13692172612616"></a>100</p>
</td>
</tr>
<tr id="row7692162615263"><td class="cellrowborder" valign="top" width="16.666666666666664%" headers="mcps1.2.7.1.1 "><p id="p669214267263"><a name="p669214267263"></a><a name="p669214267263"></a>statistics</p>
</td>
<td class="cellrowborder" valign="top" width="10.827834433113377%" headers="mcps1.2.7.1.2 "><p id="p1569242632614"><a name="p1569242632614"></a><a name="p1569242632614"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="26.7746450709858%" headers="mcps1.2.7.1.3 "><p id="p1969219269268"><a name="p1969219269268"></a><a name="p1969219269268"></a>是否输出所有满足过滤条件的圈的个数</p>
</td>
<td class="cellrowborder" valign="top" width="10.207958408318337%" headers="mcps1.2.7.1.4 "><p id="p56931326202614"><a name="p56931326202614"></a><a name="p56931326202614"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="18.66626674665067%" headers="mcps1.2.7.1.5 "><p id="p11693152662611"><a name="p11693152662611"></a><a name="p11693152662611"></a>true或false</p>
</td>
<td class="cellrowborder" valign="top" width="16.85662867426515%" headers="mcps1.2.7.1.6 "><p id="p26938262261"><a name="p26938262261"></a><a name="p26938262261"></a>false</p>
</td>
</tr>
<tr id="row6693102632619"><td class="cellrowborder" valign="top" width="16.666666666666664%" headers="mcps1.2.7.1.1 "><p id="p146931226142614"><a name="p146931226142614"></a><a name="p146931226142614"></a>batch_number</p>
</td>
<td class="cellrowborder" valign="top" width="10.827834433113377%" headers="mcps1.2.7.1.2 "><p id="p1469310263268"><a name="p1469310263268"></a><a name="p1469310263268"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="26.7746450709858%" headers="mcps1.2.7.1.3 "><p id="p186931326122610"><a name="p186931326122610"></a><a name="p186931326122610"></a>批量处理的起始节点的个数</p>
</td>
<td class="cellrowborder" valign="top" width="10.207958408318337%" headers="mcps1.2.7.1.4 "><p id="p18693182615266"><a name="p18693182615266"></a><a name="p18693182615266"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="18.66626674665067%" headers="mcps1.2.7.1.5 "><p id="p96931526102615"><a name="p96931526102615"></a><a name="p96931526102615"></a>[1,1000]</p>
</td>
<td class="cellrowborder" valign="top" width="16.85662867426515%" headers="mcps1.2.7.1.6 "><p id="p569372682616"><a name="p569372682616"></a><a name="p569372682616"></a>10</p>
</td>
</tr>
<tr id="row19693202692619"><td class="cellrowborder" valign="top" width="16.666666666666664%" headers="mcps1.2.7.1.1 "><p id="p1169312615268"><a name="p1169312615268"></a><a name="p1169312615268"></a>output_format</p>
</td>
<td class="cellrowborder" valign="top" width="10.827834433113377%" headers="mcps1.2.7.1.2 "><p id="p13693152612616"><a name="p13693152612616"></a><a name="p13693152612616"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="26.7746450709858%" headers="mcps1.2.7.1.3 "><p id="p36931926162618"><a name="p36931926162618"></a><a name="p36931926162618"></a>输出结果的格式</p>
</td>
<td class="cellrowborder" valign="top" width="10.207958408318337%" headers="mcps1.2.7.1.4 "><p id="p2693182617267"><a name="p2693182617267"></a><a name="p2693182617267"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="18.66626674665067%" headers="mcps1.2.7.1.5 "><p id="p169392632616"><a name="p169392632616"></a><a name="p169392632616"></a>vertexId,edgeId或edgeObject</p>
</td>
<td class="cellrowborder" valign="top" width="16.85662867426515%" headers="mcps1.2.7.1.6 "><p id="p8693182612612"><a name="p8693182612612"></a><a name="p8693182612612"></a>edgeObject</p>
</td>
</tr>
<tr id="row186939266263"><td class="cellrowborder" valign="top" width="16.666666666666664%" headers="mcps1.2.7.1.1 "><p id="p5693142682611"><a name="p5693142682611"></a><a name="p5693142682611"></a>filters</p>
</td>
<td class="cellrowborder" valign="top" width="10.827834433113377%" headers="mcps1.2.7.1.2 "><p id="p569392672617"><a name="p569392672617"></a><a name="p569392672617"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="26.7746450709858%" headers="mcps1.2.7.1.3 "><p id="p17693826152614"><a name="p17693826152614"></a><a name="p17693826152614"></a>过滤条件列表，数组的每个元素分别对应每一层要做的查询和过滤条件。</p>
</td>
<td class="cellrowborder" valign="top" width="10.207958408318337%" headers="mcps1.2.7.1.4 "><p id="p146931526112618"><a name="p146931526112618"></a><a name="p146931526112618"></a>Json</p>
<p id="p26931526112619"><a name="p26931526112619"></a><a name="p26931526112619"></a></p>
</td>
<td class="cellrowborder" valign="top" width="18.66626674665067%" headers="mcps1.2.7.1.5 "><p id="p14693172616262"><a name="p14693172616262"></a><a name="p14693172616262"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="16.85662867426515%" headers="mcps1.2.7.1.6 "><p id="p66931126102613"><a name="p66931126102613"></a><a name="p66931126102613"></a>-</p>
</td>
</tr>
</tbody>
</table>

**表 2**  filters元素格式

<a name="table1729539161413"></a>
<table><thead align="left"><tr id="row42961292141"><th class="cellrowborder" valign="top" width="15.476904619076185%" id="mcps1.2.7.1.1"><p id="p121971143161418"><a name="p121971143161418"></a><a name="p121971143161418"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="9.568086382723456%" id="mcps1.2.7.1.2"><p id="p219712436148"><a name="p219712436148"></a><a name="p219712436148"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="29.24415116976605%" id="mcps1.2.7.1.3"><p id="p8197114351416"><a name="p8197114351416"></a><a name="p8197114351416"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="9.798040391921617%" id="mcps1.2.7.1.4"><p id="p151975432144"><a name="p151975432144"></a><a name="p151975432144"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="19.246150769846032%" id="mcps1.2.7.1.5"><p id="p111976432146"><a name="p111976432146"></a><a name="p111976432146"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="16.666666666666664%" id="mcps1.2.7.1.6"><p id="p151971343181415"><a name="p151971343181415"></a><a name="p151971343181415"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row329619911142"><td class="cellrowborder" valign="top" width="15.476904619076185%" headers="mcps1.2.7.1.1 "><p id="p1429619901411"><a name="p1429619901411"></a><a name="p1429619901411"></a>operator</p>
</td>
<td class="cellrowborder" valign="top" width="9.568086382723456%" headers="mcps1.2.7.1.2 "><p id="p329689101414"><a name="p329689101414"></a><a name="p329689101414"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="29.24415116976605%" headers="mcps1.2.7.1.3 "><p id="p186329442154"><a name="p186329442154"></a><a name="p186329442154"></a>表示当前层要做的查询的方向</p>
</td>
<td class="cellrowborder" valign="top" width="9.798040391921617%" headers="mcps1.2.7.1.4 "><p id="p2296189161411"><a name="p2296189161411"></a><a name="p2296189161411"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="19.246150769846032%" headers="mcps1.2.7.1.5 "><p id="p351074619165"><a name="p351074619165"></a><a name="p351074619165"></a>out,in 或both</p>
</td>
<td class="cellrowborder" valign="top" width="16.666666666666664%" headers="mcps1.2.7.1.6 "><p id="p1629718901418"><a name="p1629718901418"></a><a name="p1629718901418"></a>out</p>
</td>
</tr>
<tr id="row529729131413"><td class="cellrowborder" valign="top" width="15.476904619076185%" headers="mcps1.2.7.1.1 "><p id="p14297169141412"><a name="p14297169141412"></a><a name="p14297169141412"></a>edge_filter</p>
</td>
<td class="cellrowborder" valign="top" width="9.568086382723456%" headers="mcps1.2.7.1.2 "><p id="p3297129141417"><a name="p3297129141417"></a><a name="p3297129141417"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="29.24415116976605%" headers="mcps1.2.7.1.3 "><p id="p19538156171519"><a name="p19538156171519"></a><a name="p19538156171519"></a>表示当前层查询时边的过滤条件。具体格式请见 Filtered-query API中的<a href="Filtered-query-API(2-2-13).md#table1138175053111">表6 property_filter元素格式</a>。</p>
</td>
<td class="cellrowborder" valign="top" width="9.798040391921617%" headers="mcps1.2.7.1.4 "><p id="p1629729131410"><a name="p1629729131410"></a><a name="p1629729131410"></a>Json</p>
</td>
<td class="cellrowborder" valign="top" width="19.246150769846032%" headers="mcps1.2.7.1.5 "><p id="p4297294146"><a name="p4297294146"></a><a name="p4297294146"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="16.666666666666664%" headers="mcps1.2.7.1.6 "><p id="p329715910142"><a name="p329715910142"></a><a name="p329715910142"></a>-</p>
</td>
</tr>
<tr id="row19297119171419"><td class="cellrowborder" valign="top" width="15.476904619076185%" headers="mcps1.2.7.1.1 "><p id="p2029714931414"><a name="p2029714931414"></a><a name="p2029714931414"></a>vertex_filter</p>
</td>
<td class="cellrowborder" valign="top" width="9.568086382723456%" headers="mcps1.2.7.1.2 "><p id="p1229789121415"><a name="p1229789121415"></a><a name="p1229789121415"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="29.24415116976605%" headers="mcps1.2.7.1.3 "><p id="p135345711611"><a name="p135345711611"></a><a name="p135345711611"></a>表示当前层查询时点的过滤条件。具体格式请见 Filtered-query API中的<a href="Filtered-query-API(2-2-13).md#table1138175053111">表6 property_filter元素格式</a>。</p>
</td>
<td class="cellrowborder" valign="top" width="9.798040391921617%" headers="mcps1.2.7.1.4 "><p id="p16297596145"><a name="p16297596145"></a><a name="p16297596145"></a>Json</p>
</td>
<td class="cellrowborder" valign="top" width="19.246150769846032%" headers="mcps1.2.7.1.5 "><p id="p4297139201412"><a name="p4297139201412"></a><a name="p4297139201412"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="16.666666666666664%" headers="mcps1.2.7.1.6 "><p id="p829714951410"><a name="p829714951410"></a><a name="p829714951410"></a>-</p>
</td>
</tr>
<tr id="row8297209141418"><td class="cellrowborder" valign="top" width="15.476904619076185%" headers="mcps1.2.7.1.1 "><p id="p429716941416"><a name="p429716941416"></a><a name="p429716941416"></a>times</p>
</td>
<td class="cellrowborder" valign="top" width="9.568086382723456%" headers="mcps1.2.7.1.2 "><p id="p1329799191418"><a name="p1329799191418"></a><a name="p1329799191418"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="29.24415116976605%" headers="mcps1.2.7.1.3 "><p id="p8715181316168"><a name="p8715181316168"></a><a name="p8715181316168"></a>以相同的过滤条件查询的层数</p>
</td>
<td class="cellrowborder" valign="top" width="9.798040391921617%" headers="mcps1.2.7.1.4 "><p id="p14297189161412"><a name="p14297189161412"></a><a name="p14297189161412"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="19.246150769846032%" headers="mcps1.2.7.1.5 "><p id="p1929729171414"><a name="p1929729171414"></a><a name="p1929729171414"></a>[1,10]</p>
</td>
<td class="cellrowborder" valign="top" width="16.666666666666664%" headers="mcps1.2.7.1.6 "><p id="p202977916149"><a name="p202977916149"></a><a name="p202977916149"></a>1</p>
</td>
</tr>
</tbody>
</table>

>![](public_sys-resources/icon-note.gif) **说明：** 
>-   第一层的过滤条件是对初始节点的过滤，因此仅vertex\_filter参数有效。
>-   最后一层的点过滤条件也是对初始节点的过滤。
>-   环路的长度范围是 3-10，因此过滤层数是 4-11 层。

**表 3**  response\_data 参数说明

<a name="table855010774213"></a>
<table><thead align="left"><tr id="row13551574423"><th class="cellrowborder" valign="top" width="16.18%" id="mcps1.2.5.1.1"><p id="p95511473423"><a name="p95511473423"></a><a name="p95511473423"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="13.600000000000001%" id="mcps1.2.5.1.2"><p id="p175521874421"><a name="p175521874421"></a><a name="p175521874421"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="13.41%" id="mcps1.2.5.1.3"><p id="p1552197114212"><a name="p1552197114212"></a><a name="p1552197114212"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="56.81%" id="mcps1.2.5.1.4"><p id="p16552976429"><a name="p16552976429"></a><a name="p16552976429"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row455215713426"><td class="cellrowborder" valign="top" width="16.18%" headers="mcps1.2.5.1.1 "><p id="p1510119112442"><a name="p1510119112442"></a><a name="p1510119112442"></a>circles</p>
</td>
<td class="cellrowborder" valign="top" width="13.600000000000001%" headers="mcps1.2.5.1.2 "><p id="p1955213714425"><a name="p1955213714425"></a><a name="p1955213714425"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="13.41%" headers="mcps1.2.5.1.3 "><p id="p115525754217"><a name="p115525754217"></a><a name="p115525754217"></a>List</p>
</td>
<td class="cellrowborder" valign="top" width="56.81%" headers="mcps1.2.5.1.4 "><p id="p1044595904320"><a name="p1044595904320"></a><a name="p1044595904320"></a>找到的圈集合。格式： [[circle1],[circle2],…]， 其中circle的格式：</p>
<a name="ul241918593439"></a><a name="ul241918593439"></a><ul id="ul241918593439"><li>若output_format=edgeObject，则为 [{“source”: sourceId,“target”: targetId, “index”:edgeIndex},…]，其中，sourceId、targetId和edgeIndex均为string类型。</li><li>若output_format=edgeId，则为 [sourceId-targetId-edgeIndex,…]，其中sourceId-targetId-edgeIndex为string类型。</li><li>若output_format=vertexId，则为[vertexId,…]，其中vertexId为string类型。</li></ul>
</td>
</tr>
<tr id="row9552167104210"><td class="cellrowborder" valign="top" width="16.18%" headers="mcps1.2.5.1.1 "><p id="p1155213719420"><a name="p1155213719420"></a><a name="p1155213719420"></a>runtime</p>
</td>
<td class="cellrowborder" valign="top" width="13.600000000000001%" headers="mcps1.2.5.1.2 "><p id="p555213713425"><a name="p555213713425"></a><a name="p555213713425"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="13.41%" headers="mcps1.2.5.1.3 "><p id="p1955213717428"><a name="p1955213717428"></a><a name="p1955213717428"></a>Double</p>
</td>
<td class="cellrowborder" valign="top" width="56.81%" headers="mcps1.2.5.1.4 "><p id="p3552772429"><a name="p3552772429"></a><a name="p3552772429"></a>算法运行时间。</p>
</td>
</tr>
<tr id="row255257154214"><td class="cellrowborder" valign="top" width="16.18%" headers="mcps1.2.5.1.1 "><p id="p135528720429"><a name="p135528720429"></a><a name="p135528720429"></a>n</p>
</td>
<td class="cellrowborder" valign="top" width="13.600000000000001%" headers="mcps1.2.5.1.2 "><p id="p05531274425"><a name="p05531274425"></a><a name="p05531274425"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="13.41%" headers="mcps1.2.5.1.3 "><p id="p20553577425"><a name="p20553577425"></a><a name="p20553577425"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="56.81%" headers="mcps1.2.5.1.4 "><p id="p655311716429"><a name="p655311716429"></a><a name="p655311716429"></a>枚举圈的个数的上限。</p>
</td>
</tr>
<tr id="row10553107124212"><td class="cellrowborder" valign="top" width="16.18%" headers="mcps1.2.5.1.1 "><p id="p145537712423"><a name="p145537712423"></a><a name="p145537712423"></a>circle_number</p>
</td>
<td class="cellrowborder" valign="top" width="13.600000000000001%" headers="mcps1.2.5.1.2 "><p id="p135534717421"><a name="p135534717421"></a><a name="p135534717421"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="13.41%" headers="mcps1.2.5.1.3 "><p id="p2553673423"><a name="p2553673423"></a><a name="p2553673423"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="56.81%" headers="mcps1.2.5.1.4 "><p id="p1255347134211"><a name="p1255347134211"></a><a name="p1255347134211"></a>当statistics=true时，输出所有满足条件的圈的个数。</p>
</td>
</tr>
</tbody>
</table>


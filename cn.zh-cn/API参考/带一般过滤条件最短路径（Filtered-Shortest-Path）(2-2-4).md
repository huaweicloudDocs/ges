# 带一般过滤条件最短路径（Filtered Shortest Path）\(2.2.4\)<a name="ges_03_0179"></a>

-   [请求](#section694171413216)
-   [响应](#section1654094255413)

## 请求<a name="section694171413216"></a>

-   参数说明

**表 1**  parameters参数说明

<a name="table1819914264221"></a>
<table><thead align="left"><tr id="row2199122617227"><th class="cellrowborder" valign="top" width="17%" id="mcps1.2.5.1.1"><p id="p41991426102220"><a name="p41991426102220"></a><a name="p41991426102220"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="17.21%" id="mcps1.2.5.1.2"><p id="p51993268221"><a name="p51993268221"></a><a name="p51993268221"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="14.52%" id="mcps1.2.5.1.3"><p id="p1119972613229"><a name="p1119972613229"></a><a name="p1119972613229"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="51.27%" id="mcps1.2.5.1.4"><p id="p1019912662219"><a name="p1019912662219"></a><a name="p1019912662219"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row1519972662216"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.5.1.1 "><p id="p1119952613223"><a name="p1119952613223"></a><a name="p1119952613223"></a>source</p>
</td>
<td class="cellrowborder" valign="top" width="17.21%" headers="mcps1.2.5.1.2 "><p id="p18199192617221"><a name="p18199192617221"></a><a name="p18199192617221"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.52%" headers="mcps1.2.5.1.3 "><p id="p191992268226"><a name="p191992268226"></a><a name="p191992268226"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.27%" headers="mcps1.2.5.1.4 "><p id="p0199112632212"><a name="p0199112632212"></a><a name="p0199112632212"></a>输入路径的起点ID。</p>
</td>
</tr>
<tr id="row13199152611225"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.5.1.1 "><p id="p18199326112219"><a name="p18199326112219"></a><a name="p18199326112219"></a>target</p>
</td>
<td class="cellrowborder" valign="top" width="17.21%" headers="mcps1.2.5.1.2 "><p id="p1119932622220"><a name="p1119932622220"></a><a name="p1119932622220"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="14.52%" headers="mcps1.2.5.1.3 "><p id="p0200112617220"><a name="p0200112617220"></a><a name="p0200112617220"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="51.27%" headers="mcps1.2.5.1.4 "><p id="p8200626192215"><a name="p8200626192215"></a><a name="p8200626192215"></a>输入路径的终点ID。</p>
</td>
</tr>
<tr id="row220011261227"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.5.1.1 "><p id="p42009264222"><a name="p42009264222"></a><a name="p42009264222"></a>directed</p>
</td>
<td class="cellrowborder" valign="top" width="17.21%" headers="mcps1.2.5.1.2 "><p id="p3200126162212"><a name="p3200126162212"></a><a name="p3200126162212"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="14.52%" headers="mcps1.2.5.1.3 "><p id="p72005261224"><a name="p72005261224"></a><a name="p72005261224"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="51.27%" headers="mcps1.2.5.1.4 "><p id="p92001126142216"><a name="p92001126142216"></a><a name="p92001126142216"></a>是否考虑边的方向。默认值为“false”。</p>
</td>
</tr>
</tbody>
</table>

-   请求样例

    -   同步

        ```
        {
            "executionMode": "sync",
            "algorithmName": "filtered_shortest_path",
            "edge_filter": {
                "property_filter": {
                    "leftvalue": {
                        "label_name": "labelName"
                    },
                    "predicate": "IN",
                    "rightvalue": {
                        "value": [
                            "xxx",
                            "rate"
                        ]
                    }
                }
            },
            "vertex_filter": {
                "property_filter": {
                    "leftvalue": {
                        "property_name": "title"
                    },
                    "predicate": "PREFIX",
                    "rightvalue": {
                        "value": "tr_"
                    }
                }
            },
            "parameters": {
                "source": "tr_1",
                "target": "tr_117",
                "directed": true
            }
        }
        ```


    -   异步

        ```
        {
            "executionMode": "async",
            "algorithmName": "filtered_shortest_path",
            "edge_filter": {
                "property_filter": {
                    "leftvalue": {
                        "label_name": "labelName"
                    },
                    "predicate": "IN",
                    "rightvalue": {
                        "value": [
                            "xxx",
                            "rate"
                        ]
                    }
                }
            },
            "vertex_filter": {
                "property_filter": {
                    "leftvalue": {
                        "property_name": "title"
                    },
                    "predicate": "PREFIX",
                    "rightvalue": {
                        "value": "tr_"
                    }
                }
            },
            "parameters": {
                "source": "tr_1",
                "target": "tr_117",
                "directed": true
            }
        }
        ```



## 响应<a name="section1654094255413"></a>

-   同步参数说明

    **表 2**  response\_data参数说明

    <a name="table2950104212540"></a>
    <table><thead align="left"><tr id="row179503428546"><th class="cellrowborder" valign="top" width="11.61%" id="mcps1.2.5.1.1"><p id="p12949942185418"><a name="p12949942185418"></a><a name="p12949942185418"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="11.62%" id="mcps1.2.5.1.2"><p id="p89501442115413"><a name="p89501442115413"></a><a name="p89501442115413"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.86%" id="mcps1.2.5.1.3"><p id="p1095054217543"><a name="p1095054217543"></a><a name="p1095054217543"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="63.91%" id="mcps1.2.5.1.4"><p id="p1495015427547"><a name="p1495015427547"></a><a name="p1495015427547"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1156724325514"><td class="cellrowborder" valign="top" width="11.61%" headers="mcps1.2.5.1.1 "><p id="p495124211548"><a name="p495124211548"></a><a name="p495124211548"></a>path</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.62%" headers="mcps1.2.5.1.2 "><p id="p095154255411"><a name="p095154255411"></a><a name="p095154255411"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.86%" headers="mcps1.2.5.1.3 "><p id="p39512042175414"><a name="p39512042175414"></a><a name="p39512042175414"></a>List</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.91%" headers="mcps1.2.5.1.4 "><p id="p18951134216545"><a name="p18951134216545"></a><a name="p18951134216545"></a>点的结果集合。filters最后一层为点过滤时，data中将包含vertices。</p>
    </td>
    </tr>
    <tr id="row15567194395513"><td class="cellrowborder" valign="top" width="11.61%" headers="mcps1.2.5.1.1 "><p id="p1495184265414"><a name="p1495184265414"></a><a name="p1495184265414"></a>source</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.62%" headers="mcps1.2.5.1.2 "><p id="p19951164216542"><a name="p19951164216542"></a><a name="p19951164216542"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.86%" headers="mcps1.2.5.1.3 "><p id="p2951154219540"><a name="p2951154219540"></a><a name="p2951154219540"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.91%" headers="mcps1.2.5.1.4 "><p id="p1795118420548"><a name="p1795118420548"></a><a name="p1795118420548"></a>源节点ID。</p>
    </td>
    </tr>
    <tr id="row1856612436557"><td class="cellrowborder" valign="top" width="11.61%" headers="mcps1.2.5.1.1 "><p id="p795234225420"><a name="p795234225420"></a><a name="p795234225420"></a>target</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.62%" headers="mcps1.2.5.1.2 "><p id="p6952144225417"><a name="p6952144225417"></a><a name="p6952144225417"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.86%" headers="mcps1.2.5.1.3 "><p id="p59522425546"><a name="p59522425546"></a><a name="p59522425546"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.91%" headers="mcps1.2.5.1.4 "><p id="p189521042105410"><a name="p189521042105410"></a><a name="p189521042105410"></a>目标节点ID。</p>
    </td>
    </tr>
    <tr id="row1556584312559"><td class="cellrowborder" valign="top" width="11.61%" headers="mcps1.2.5.1.1 "><p id="p1695214295416"><a name="p1695214295416"></a><a name="p1695214295416"></a>runtime</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.62%" headers="mcps1.2.5.1.2 "><p id="p69521742125416"><a name="p69521742125416"></a><a name="p69521742125416"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.86%" headers="mcps1.2.5.1.3 "><p id="p1495219428548"><a name="p1495219428548"></a><a name="p1495219428548"></a>Double</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.91%" headers="mcps1.2.5.1.4 "><p id="p895254295410"><a name="p895254295410"></a><a name="p895254295410"></a>算法运行时间 。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   响应样例
    -   同步成功响应样例

        ```
        {
            "data": {
                "outputs": {
                    "path": [
                        "tr_1",
                        "tr_5",
                        "tr_26",
                        "tr_117"
                    ],
                    "runtime": 0.735766,
                    "source": "tr_1",
                    "target": "tr_117"
                }
            }
        }
        ```


    -   同步失败响应样例

        ```
        {
        "errorMessage": "graph [tesdt_117] is not found",
        "errorCode": "GES.8402"
        }
        ```



-   异步返回参数

    **表 3**  异步返回参数说明

    <a name="table916015196401"></a>
    <table><thead align="left"><tr id="row249018194406"><th class="cellrowborder" valign="top" width="17.64%" id="mcps1.2.5.1.1"><p id="p949018195403"><a name="p949018195403"></a><a name="p949018195403"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.389999999999999%" id="mcps1.2.5.1.2"><p id="p20490141974015"><a name="p20490141974015"></a><a name="p20490141974015"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.54%" id="mcps1.2.5.1.3"><p id="p20490111915405"><a name="p20490111915405"></a><a name="p20490111915405"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="51.43%" id="mcps1.2.5.1.4"><p id="p749110197407"><a name="p749110197407"></a><a name="p749110197407"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row3491319144016"><td class="cellrowborder" valign="top" width="17.64%" headers="mcps1.2.5.1.1 "><p id="p1549121954018"><a name="p1549121954018"></a><a name="p1549121954018"></a>errorMessage</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.389999999999999%" headers="mcps1.2.5.1.2 "><p id="p17491619134017"><a name="p17491619134017"></a><a name="p17491619134017"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.54%" headers="mcps1.2.5.1.3 "><p id="p449111194409"><a name="p449111194409"></a><a name="p449111194409"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.43%" headers="mcps1.2.5.1.4 "><p id="p34911319134016"><a name="p34911319134016"></a><a name="p34911319134016"></a>系统提示信息，执行成功时，字段可能为空。执行失败时，用于显示错误信息。</p>
    </td>
    </tr>
    <tr id="row14916198401"><td class="cellrowborder" valign="top" width="17.64%" headers="mcps1.2.5.1.1 "><p id="p194911192409"><a name="p194911192409"></a><a name="p194911192409"></a>errorCode</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.389999999999999%" headers="mcps1.2.5.1.2 "><p id="p134912193408"><a name="p134912193408"></a><a name="p134912193408"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.54%" headers="mcps1.2.5.1.3 "><p id="p104921198407"><a name="p104921198407"></a><a name="p104921198407"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.43%" headers="mcps1.2.5.1.4 "><p id="p1349271914014"><a name="p1349271914014"></a><a name="p1349271914014"></a>系统提示信息，执行成功时，字段可能为空。执行失败时，用于显示错误码。</p>
    </td>
    </tr>
    <tr id="row144921196405"><td class="cellrowborder" valign="top" width="17.64%" headers="mcps1.2.5.1.1 "><p id="p849281934018"><a name="p849281934018"></a><a name="p849281934018"></a>jobId</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.389999999999999%" headers="mcps1.2.5.1.2 "><p id="p20492319164013"><a name="p20492319164013"></a><a name="p20492319164013"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.54%" headers="mcps1.2.5.1.3 "><p id="p1049281915404"><a name="p1049281915404"></a><a name="p1049281915404"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.43%" headers="mcps1.2.5.1.4 "><p id="p16492141917406"><a name="p16492141917406"></a><a name="p16492141917406"></a>执行算法任务ID。请求失败时，字段为空。</p>
    </td>
    </tr>
    <tr id="row0492319194014"><td class="cellrowborder" valign="top" width="17.64%" headers="mcps1.2.5.1.1 "><p id="p1049241924020"><a name="p1049241924020"></a><a name="p1049241924020"></a>jobType</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.389999999999999%" headers="mcps1.2.5.1.2 "><p id="p194921019204014"><a name="p194921019204014"></a><a name="p194921019204014"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.54%" headers="mcps1.2.5.1.3 "><p id="p1949213198407"><a name="p1949213198407"></a><a name="p1949213198407"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="51.43%" headers="mcps1.2.5.1.4 "><p id="p194927199409"><a name="p194927199409"></a><a name="p194927199409"></a>任务类型。请求失败时，字段为空。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   响应样例
    -   异步成功响应样例

        ```
        {
        "jobId": "500dea8f-9651-41fe-8299-c20f13a032ea",
        "jobType": 2
        }
        ```

    -   异步失败响应样例

        ```
        {
        "errorMessage": "graph [test_117d] is not found",
        "errorCode": "GES.8402"
        }
        ```




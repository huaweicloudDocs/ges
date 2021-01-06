# Filtered-query API<a name="ges_03_0175"></a>

-   [功能介绍](#section3623114715018)
-   [URI](#section56494056202011)
-   [请求](#section62446078202011)
-   [响应](#section14834278202011)
-   [返回值](#section3824743202011)

## 功能介绍<a name="section3623114715018"></a>

对k跳过程进行逐层过滤，列出满足过滤条件的第k跳节点或边。

## URI<a name="section56494056202011"></a>

-   URI 格式

    ```
    POST /ges/v1.0/{projectId}/graphs/{graphName}/action?action_id=filtered-query
    ```

-   参数说明

    **表 1**  URI参数说明

    <a name="table66283993202424"></a>
    <table><thead align="left"><tr id="row59205483202424"><th class="cellrowborder" valign="top" width="16.71%" id="mcps1.2.5.1.1"><p id="p59805966202438"><a name="p59805966202438"></a><a name="p59805966202438"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="15.629999999999999%" id="mcps1.2.5.1.2"><p id="p12445038202438"><a name="p12445038202438"></a><a name="p12445038202438"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.78%" id="mcps1.2.5.1.3"><p id="p1415130202438"><a name="p1415130202438"></a><a name="p1415130202438"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="48.88%" id="mcps1.2.5.1.4"><p id="p47516731202438"><a name="p47516731202438"></a><a name="p47516731202438"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row20271122202424"><td class="cellrowborder" valign="top" width="16.71%" headers="mcps1.2.5.1.1 "><p id="p36605179202438"><a name="p36605179202438"></a><a name="p36605179202438"></a>projectId</p>
    </td>
    <td class="cellrowborder" valign="top" width="15.629999999999999%" headers="mcps1.2.5.1.2 "><p id="p12229546202438"><a name="p12229546202438"></a><a name="p12229546202438"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.78%" headers="mcps1.2.5.1.3 "><p id="p51069165202438"><a name="p51069165202438"></a><a name="p51069165202438"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.88%" headers="mcps1.2.5.1.4 "><p id="p51708449194548"><a name="p51708449194548"></a><a name="p51708449194548"></a>项目编号，用于资源隔离。请参考<a href="获取项目ID.md">获取项目ID</a>。</p>
    </td>
    </tr>
    <tr id="row33038495115"><td class="cellrowborder" valign="top" width="16.71%" headers="mcps1.2.5.1.1 "><p id="p204402484117"><a name="p204402484117"></a><a name="p204402484117"></a>graphName</p>
    </td>
    <td class="cellrowborder" valign="top" width="15.629999999999999%" headers="mcps1.2.5.1.2 "><p id="p16442124819110"><a name="p16442124819110"></a><a name="p16442124819110"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.78%" headers="mcps1.2.5.1.3 "><p id="p1644484812118"><a name="p1644484812118"></a><a name="p1644484812118"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="48.88%" headers="mcps1.2.5.1.4 "><p id="p1444614482118"><a name="p1444614482118"></a><a name="p1444614482118"></a>图名称。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求<a name="section62446078202011"></a>

-   请求样例
    -   同步

        ```
        POST /ges/v1.0/{projectId}/graphs/{graphName}/action?action_id=filtered-query
        {
            "executionMode": "sync",
            "visulized": "false",
            "filters": [
                {
                    "operator": "outV"
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
                                "value": "rate"
                            }
                        }
                    }
                }
            ],
            "with_path": false,
            "full_path": false,
            "vertices": [
                "tr_10"
            ]
        }
        ```

    -   异步

        ```
        POST /ges/v1.0/{projectId}/graphs/{graphName}/action?action_id=filtered-query
        {
            "executionMode": "async",
            "visulized": "false",
            "filters": [
                {
                    "operator": "outV"
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
                                "value": "rate"
                            }
                        }
                    }
                }
            ],
            "with_path": false,
            "full_path": false,
            "vertices": [
                "tr_10"
            ]
        }
        ```

    -   嵌套property\_filter

        ```
        {
            "executionMode": "sync",
            "filters": [
                {
                    "operator": "outV",
                     "vertex_filter": {
                        "property_filter": {
                            "leftvalue": {
                         "property_filter": {
                            "leftvalue": {
                                "property_name": "genres"
                             },
                          "predicate": "PREFIX",
                          "rightvalue": {
                          "value": "A|"
                    }
                  }
                },
                       "predicate": "&",
                       "rightvalue": {
                       "property_filter": {
                       "leftvalue": {
                       "label_name": "labelName"
                    },
                       "predicate": "=",
                        "rightvalue": {
                         "value": "movie"
                      }
                    }
                  }
               }
             } 
            }
          ],
                "vertices": [
                "tr_3"
          ]
        }
        ```



-   Body参数说明

    **表 2**  Body参数说明

    <a name="table22545074195633"></a>
    <table><thead align="left"><tr id="row60806065195633"><th class="cellrowborder" valign="top" width="15.39%" id="mcps1.2.5.1.1"><p id="p44837705195650"><a name="p44837705195650"></a><a name="p44837705195650"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.120000000000001%" id="mcps1.2.5.1.2"><p id="p7975482195650"><a name="p7975482195650"></a><a name="p7975482195650"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="14.66%" id="mcps1.2.5.1.3"><p id="p42034271195650"><a name="p42034271195650"></a><a name="p42034271195650"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="57.830000000000005%" id="mcps1.2.5.1.4"><p id="p49332768195650"><a name="p49332768195650"></a><a name="p49332768195650"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row34935955195633"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p1433418114143"><a name="p1433418114143"></a><a name="p1433418114143"></a>executionMode</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p1033415121411"><a name="p1033415121411"></a><a name="p1033415121411"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.3 "><p id="p933410191414"><a name="p933410191414"></a><a name="p933410191414"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.830000000000005%" headers="mcps1.2.5.1.4 "><a name="ul17334121191420"></a><a name="ul17334121191420"></a><ul id="ul17334121191420"><li>sync：同步</li><li>async：异步<p id="p633413111419"><a name="p633413111419"></a><a name="p633413111419"></a>默认为“sync ”同步返回。</p>
    </li></ul>
    </td>
    </tr>
    <tr id="row13700543195511"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p103351216140"><a name="p103351216140"></a><a name="p103351216140"></a>vertices</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p63357116147"><a name="p63357116147"></a><a name="p63357116147"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.3 "><p id="p123359114143"><a name="p123359114143"></a><a name="p123359114143"></a>Array of Json</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.830000000000005%" headers="mcps1.2.5.1.4 "><p id="p6335613143"><a name="p6335613143"></a><a name="p6335613143"></a>查询的起始节点ID列表。</p>
    </td>
    </tr>
    <tr id="row13708191123318"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p1870911117331"><a name="p1870911117331"></a><a name="p1870911117331"></a>query_type</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p470919133315"><a name="p470919133315"></a><a name="p470919133315"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.3 "><p id="p1370911113310"><a name="p1370911113310"></a><a name="p1370911113310"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.830000000000005%" headers="mcps1.2.5.1.4 "><p id="p733345693410"><a name="p733345693410"></a><a name="p733345693410"></a>可选：['Default'，AllVertices'，'SimpleEdges',‘Path’]</p>
    <a name="ul1230435614345"></a><a name="ul1230435614345"></a><ul id="ul1230435614345"><li>Default为默认模式，即返回用户查询第k跳内容。</li><li>AllVertices返回用户路径查询k跳以内所有点详情。</li><li>SimpleEdges返回用户路径查询k跳以内所有边，仅包含边的id和label信息。</li><li>Path返回用户路径查询的路径信息，即path的集合。</li></ul>
    </td>
    </tr>
    <tr id="row689112634214"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p989215268427"><a name="p989215268427"></a><a name="p989215268427"></a>by</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p28921526114210"><a name="p28921526114210"></a><a name="p28921526114210"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.3 "><p id="p06495436422"><a name="p06495436422"></a><a name="p06495436422"></a>Array of Json</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.830000000000005%" headers="mcps1.2.5.1.4 "><p id="p36441234313"><a name="p36441234313"></a><a name="p36441234313"></a>用于控制输出字段，当query_type为Default或AllVertices时有效。当前仅支持一层。当字段不存在时，默认为输出所有内容。</p>
    </td>
    </tr>
    <tr id="row9281187195012"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p12287197155011"><a name="p12287197155011"></a><a name="p12287197155011"></a>edges</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p17290197165014"><a name="p17290197165014"></a><a name="p17290197165014"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.3 "><p id="p42901679506"><a name="p42901679506"></a><a name="p42901679506"></a>Array of Json</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.830000000000005%" headers="mcps1.2.5.1.4 "><p id="p729016716503"><a name="p729016716503"></a><a name="p729016716503"></a>查询的起始边列表，与vertices二选一，具体格式见<a href="#table8182420155110">表3</a>。</p>
    </td>
    </tr>
    <tr id="row8598200115620"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p0335514146"><a name="p0335514146"></a><a name="p0335514146"></a>filters</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p123352171413"><a name="p123352171413"></a><a name="p123352171413"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.3 "><p id="p433515151415"><a name="p433515151415"></a><a name="p433515151415"></a>Array of Json</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.830000000000005%" headers="mcps1.2.5.1.4 "><p id="p1233511171415"><a name="p1233511171415"></a><a name="p1233511171415"></a>过滤条件列表，数组的每个元素分别对应每一层要做的查询和过滤条件。具体格式见<a href="#table944401254">表4</a>。</p>
    </td>
    </tr>
    <tr id="row1734293711319"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p173350171412"><a name="p173350171412"></a><a name="p173350171412"></a>full_path</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p83351016145"><a name="p83351016145"></a><a name="p83351016145"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.3 "><p id="p73369120142"><a name="p73369120142"></a><a name="p73369120142"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.830000000000005%" headers="mcps1.2.5.1.4 "><p id="p3172191917249"><a name="p3172191917249"></a><a name="p3172191917249"></a>返回的路径信息是否是完整路径，默认为“false”。</p>
    <a name="ul922172916248"></a><a name="ul922172916248"></a><ul id="ul922172916248"><li>为“true”时，返回从起始节点到所有叶子节点的路径。</li><li>为“false”时，返回从起始节点到第k层叶子节点的路径。</li></ul>
    </td>
    </tr>
    <tr id="row1634323771319"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p18336418141"><a name="p18336418141"></a><a name="p18336418141"></a>visualized</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p33364118142"><a name="p33364118142"></a><a name="p33364118142"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.3 "><p id="p1633651171418"><a name="p1633651171418"></a><a name="p1633651171418"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.830000000000005%" headers="mcps1.2.5.1.4 "><p id="p13647132173316"><a name="p13647132173316"></a><a name="p13647132173316"></a>是否可视化，默认为“false”。在异步模式下：</p>
    <a name="ul16416182873311"></a><a name="ul16416182873311"></a><ul id="ul16416182873311"><li><span class="parmname" id="parmname19202142323320"><a name="parmname19202142323320"></a><a name="parmname19202142323320"></a>“visualized”</span>为<span class="parmvalue" id="parmvalue6202423183311"><a name="parmvalue6202423183311"></a><a name="parmvalue6202423183311"></a>“false”</span>时，查询job结果分页返回。</li><li><span class="parmname" id="parmname11932134623219"><a name="parmname11932134623219"></a><a name="parmname11932134623219"></a>“visualized”</span>为<span class="parmvalue" id="parmvalue722558324"><a name="parmvalue722558324"></a><a name="parmvalue722558324"></a>“true”</span>时，查询job结果不分页。</li></ul>
    </td>
    </tr>
    </tbody>
    </table>

    **表 3**  edges元素格式

    <a name="table8182420155110"></a>
    <table><thead align="left"><tr id="row518332065120"><th class="cellrowborder" valign="top" width="15.39%" id="mcps1.2.5.1.1"><p id="p11183112019512"><a name="p11183112019512"></a><a name="p11183112019512"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.120000000000001%" id="mcps1.2.5.1.2"><p id="p218322017512"><a name="p218322017512"></a><a name="p218322017512"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="14.66%" id="mcps1.2.5.1.3"><p id="p1518372045118"><a name="p1518372045118"></a><a name="p1518372045118"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="57.830000000000005%" id="mcps1.2.5.1.4"><p id="p81841920135119"><a name="p81841920135119"></a><a name="p81841920135119"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1218417202517"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p17184120125116"><a name="p17184120125116"></a><a name="p17184120125116"></a>source</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p1184132015519"><a name="p1184132015519"></a><a name="p1184132015519"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.3 "><p id="p20184172055119"><a name="p20184172055119"></a><a name="p20184172055119"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.830000000000005%" headers="mcps1.2.5.1.4 "><p id="p917177165213"><a name="p917177165213"></a><a name="p917177165213"></a>源节点ID。</p>
    </td>
    </tr>
    <tr id="row1518842045114"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p71887201510"><a name="p71887201510"></a><a name="p71887201510"></a>target</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p13188122095113"><a name="p13188122095113"></a><a name="p13188122095113"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.3 "><p id="p118882012516"><a name="p118882012516"></a><a name="p118882012516"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.830000000000005%" headers="mcps1.2.5.1.4 "><p id="p1018822045112"><a name="p1018822045112"></a><a name="p1018822045112"></a>目标节点ID。</p>
    </td>
    </tr>
    <tr id="row2188520155120"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p131881020195113"><a name="p131881020195113"></a><a name="p131881020195113"></a>index</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p91881520145113"><a name="p91881520145113"></a><a name="p91881520145113"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.3 "><p id="p718822015110"><a name="p718822015110"></a><a name="p718822015110"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.830000000000005%" headers="mcps1.2.5.1.4 "><p id="p12188192025118"><a name="p12188192025118"></a><a name="p12188192025118"></a>此边在源节点边集合中的索引。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 4**  Filters元素格式

    <a name="table944401254"></a>
    <table><thead align="left"><tr id="row3446013254"><th class="cellrowborder" valign="top" width="15.39%" id="mcps1.2.5.1.1"><p id="p54412032511"><a name="p54412032511"></a><a name="p54412032511"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.120000000000001%" id="mcps1.2.5.1.2"><p id="p94511092515"><a name="p94511092515"></a><a name="p94511092515"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="14.66%" id="mcps1.2.5.1.3"><p id="p1745901252"><a name="p1745901252"></a><a name="p1745901252"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="57.830000000000005%" id="mcps1.2.5.1.4"><p id="p11457011255"><a name="p11457011255"></a><a name="p11457011255"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row12451020259"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p57631214112616"><a name="p57631214112616"></a><a name="p57631214112616"></a>operator</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p576313140262"><a name="p576313140262"></a><a name="p576313140262"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.3 "><p id="p1076381416266"><a name="p1076381416266"></a><a name="p1076381416266"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.830000000000005%" headers="mcps1.2.5.1.4 "><p id="p8763191413269"><a name="p8763191413269"></a><a name="p8763191413269"></a>表示要做的查询类型，可选的值有：</p>
    <a name="ul18938152542710"></a><a name="ul18938152542710"></a><ul id="ul18938152542710"><li>inV：入点</li><li>outV：出点</li><li>bothV：入点和出点</li><li>vertex：所有节点。第一层filter可用，若起始传入节点，则第一层输出为传入的节点；若起始传入节点为空，则第一层输出为所有节点</li><li>in：入边</li><li>out：出边</li><li>both：入边和出边</li><li>edge：所有边，仅第一层filter可用，使用方式与vertex类似</li></ul>
    <p id="p3202447143414"><a name="p3202447143414"></a><a name="p3202447143414"></a>后一层的查询操作以前一层的查询结果为输入：</p>
    <a name="ul10421180103511"></a><a name="ul10421180103511"></a><ul id="ul10421180103511"><li>若前一层的结果是点，则对应的操作可以有（inV，outV，bothV，in，out，both）。</li><li>若前一层的结果是边，则对应的操作可以有（inV，outV，bothV）。</li></ul>
    </td>
    </tr>
    <tr id="row54518012517"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p1776410142266"><a name="p1776410142266"></a><a name="p1776410142266"></a>vertex_filter</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p17764514202615"><a name="p17764514202615"></a><a name="p17764514202615"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.3 "><p id="p137641514112618"><a name="p137641514112618"></a><a name="p137641514112618"></a>JSON String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.830000000000005%" headers="mcps1.2.5.1.4 "><p id="p157646141265"><a name="p157646141265"></a><a name="p157646141265"></a>在“operator”为“ inV”或“outV”或“bothV”时可选，具体格式见<a href="#table1138175053111">表6</a>。</p>
    </td>
    </tr>
    <tr id="row1246140102510"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p187647148268"><a name="p187647148268"></a><a name="p187647148268"></a>edge_filter</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p1176401411265"><a name="p1176401411265"></a><a name="p1176401411265"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.3 "><p id="p147641214182618"><a name="p147641214182618"></a><a name="p147641214182618"></a>JSON String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.830000000000005%" headers="mcps1.2.5.1.4 "><p id="p2764514112616"><a name="p2764514112616"></a><a name="p2764514112616"></a>在“operator”为“in”或“out”或“both”时可选，具体格式见<a href="#table1138175053111">表6</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 5**  by元素格式

    <a name="table672017519313"></a>
    <table><thead align="left"><tr id="row127217514312"><th class="cellrowborder" valign="top" width="20.9%" id="mcps1.2.5.1.1"><p id="p1040813774419"><a name="p1040813774419"></a><a name="p1040813774419"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="13.11%" id="mcps1.2.5.1.2"><p id="p640815764420"><a name="p640815764420"></a><a name="p640815764420"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="15.39%" id="mcps1.2.5.1.3"><p id="p1240915719440"><a name="p1240915719440"></a><a name="p1240915719440"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="50.6%" id="mcps1.2.5.1.4"><p id="p94094724420"><a name="p94094724420"></a><a name="p94094724420"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row672145113117"><td class="cellrowborder" valign="top" width="20.9%" headers="mcps1.2.5.1.1 "><p id="p1372135163111"><a name="p1372135163111"></a><a name="p1372135163111"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.11%" headers="mcps1.2.5.1.2 "><p id="p9721115114319"><a name="p9721115114319"></a><a name="p9721115114319"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.3 "><p id="p147225510314"><a name="p147225510314"></a><a name="p147225510314"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.6%" headers="mcps1.2.5.1.4 "><p id="p6722145163119"><a name="p6722145163119"></a><a name="p6722145163119"></a>是否输出id。默认为false。</p>
    </td>
    </tr>
    <tr id="row554812595439"><td class="cellrowborder" valign="top" width="20.9%" headers="mcps1.2.5.1.1 "><p id="p205481594434"><a name="p205481594434"></a><a name="p205481594434"></a>label</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.11%" headers="mcps1.2.5.1.2 "><p id="p354835984316"><a name="p354835984316"></a><a name="p354835984316"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.3 "><p id="p15481259154310"><a name="p15481259154310"></a><a name="p15481259154310"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.6%" headers="mcps1.2.5.1.4 "><p id="p165481659124315"><a name="p165481659124315"></a><a name="p165481659124315"></a>是否输出label。默认为false。</p>
    </td>
    </tr>
    <tr id="row644485724319"><td class="cellrowborder" valign="top" width="20.9%" headers="mcps1.2.5.1.1 "><p id="p1244465764311"><a name="p1244465764311"></a><a name="p1244465764311"></a>properties</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.11%" headers="mcps1.2.5.1.2 "><p id="p14444357194311"><a name="p14444357194311"></a><a name="p14444357194311"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.3 "><p id="p44442572436"><a name="p44442572436"></a><a name="p44442572436"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.6%" headers="mcps1.2.5.1.4 "><p id="p1544418577433"><a name="p1544418577433"></a><a name="p1544418577433"></a>是否输出properties。默认为false。</p>
    </td>
    </tr>
    <tr id="row59413156445"><td class="cellrowborder" valign="top" width="20.9%" headers="mcps1.2.5.1.1 "><p id="p129410153441"><a name="p129410153441"></a><a name="p129410153441"></a>selectedProperties</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.11%" headers="mcps1.2.5.1.2 "><p id="p69510151440"><a name="p69510151440"></a><a name="p69510151440"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.3 "><p id="p695101511442"><a name="p695101511442"></a><a name="p695101511442"></a>Array of String</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.6%" headers="mcps1.2.5.1.4 "><p id="p833417174716"><a name="p833417174716"></a><a name="p833417174716"></a>当properties字段为true时，可以选择输出的属性项。</p>
    <p id="p833517114712"><a name="p833517114712"></a><a name="p833517114712"></a>字段为空时输出所有属性字段。默认为空。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 6**  property\_filter元素格式

    <a name="table1138175053111"></a>
    <table><thead align="left"><tr id="row1413816505314"><th class="cellrowborder" valign="top" width="15.39%" id="mcps1.2.5.1.1"><p id="p313965083117"><a name="p313965083117"></a><a name="p313965083117"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.120000000000001%" id="mcps1.2.5.1.2"><p id="p12139950163115"><a name="p12139950163115"></a><a name="p12139950163115"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="14.66%" id="mcps1.2.5.1.3"><p id="p0141115017316"><a name="p0141115017316"></a><a name="p0141115017316"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="57.830000000000005%" id="mcps1.2.5.1.4"><p id="p1214220507310"><a name="p1214220507310"></a><a name="p1214220507310"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row6142105013318"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p9395823163215"><a name="p9395823163215"></a><a name="p9395823163215"></a>leftvalue</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p6395123133212"><a name="p6395123133212"></a><a name="p6395123133212"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.3 "><p id="p113952234322"><a name="p113952234322"></a><a name="p113952234322"></a>JSON String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.830000000000005%" headers="mcps1.2.5.1.4 "><p id="p839516237326"><a name="p839516237326"></a><a name="p839516237326"></a>左值，具体格式见<a href="#table635611513340">表7</a>。</p>
    </td>
    </tr>
    <tr id="row8143350113116"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p63961123133214"><a name="p63961123133214"></a><a name="p63961123133214"></a>predicate</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p9397123143216"><a name="p9397123143216"></a><a name="p9397123143216"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.3 "><p id="p18397142312322"><a name="p18397142312322"></a><a name="p18397142312322"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.830000000000005%" headers="mcps1.2.5.1.4 "><p id="p640082313328"><a name="p640082313328"></a><a name="p640082313328"></a>表示过滤类型，支持的操作如下：</p>
    <a name="ul137213412"></a><a name="ul137213412"></a><ul id="ul137213412"><li>=：等于</li><li>!=：不等于</li><li>&lt;：小于</li><li>&lt;=：小于等于</li><li>&gt;：大于</li><li>&gt;=：大于等于</li><li>&amp;：与</li><li>|：或</li><li>HAS/HASNOT：是否有此属性</li><li>CONTAIN/NOTCONTAIN：属性值中是否含有右值</li><li>SUBSET：右值是属性值的子集</li><li>IN/NOTIN：左值与右值是否有交集</li><li>PREFIX：右值是左值的前缀</li><li>FUZZY：模糊匹配</li><li>REGEX：正则匹配</li><li>SUBSTRING：右值是左值的子字符串</li><li>CISUBSTRING：忽略大小写的子字符串</li></ul>
    </td>
    </tr>
    <tr id="row111431950113117"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p9403823133214"><a name="p9403823133214"></a><a name="p9403823133214"></a>rightvalue</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p7403132353211"><a name="p7403132353211"></a><a name="p7403132353211"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.3 "><p id="p1940332314327"><a name="p1940332314327"></a><a name="p1940332314327"></a>JSON String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.830000000000005%" headers="mcps1.2.5.1.4 "><p id="p5403112316325"><a name="p5403112316325"></a><a name="p5403112316325"></a>右值，具体格式见<a href="#table410075413418">表8</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 7**  leftvalue元素格式

    <a name="table635611513340"></a>
    <table><thead align="left"><tr id="row1356165111343"><th class="cellrowborder" valign="top" width="15.39%" id="mcps1.2.5.1.1"><p id="p93561151203418"><a name="p93561151203418"></a><a name="p93561151203418"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.120000000000001%" id="mcps1.2.5.1.2"><p id="p163561351113410"><a name="p163561351113410"></a><a name="p163561351113410"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.24%" id="mcps1.2.5.1.3"><p id="p19356105114346"><a name="p19356105114346"></a><a name="p19356105114346"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="60.25%" id="mcps1.2.5.1.4"><p id="p163561351193420"><a name="p163561351193420"></a><a name="p163561351193420"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1135725163412"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p172621040153512"><a name="p172621040153512"></a><a name="p172621040153512"></a>label_name</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p1026219405358"><a name="p1026219405358"></a><a name="p1026219405358"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.24%" headers="mcps1.2.5.1.3 "><p id="p62621640163516"><a name="p62621640163516"></a><a name="p62621640163516"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60.25%" headers="mcps1.2.5.1.4 "><p id="p18262204013350"><a name="p18262204013350"></a><a name="p18262204013350"></a>若过滤“label”，可选“label_name”，值为“labelName”。rightvalue的value字段填具体的label的名称。</p>
    </td>
    </tr>
    <tr id="row135785112344"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p13262140153520"><a name="p13262140153520"></a><a name="p13262140153520"></a>property_name</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p15262144003511"><a name="p15262144003511"></a><a name="p15262144003511"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.24%" headers="mcps1.2.5.1.3 "><p id="p17262164013355"><a name="p17262164013355"></a><a name="p17262164013355"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60.25%" headers="mcps1.2.5.1.4 "><p id="p192621940113513"><a name="p192621940113513"></a><a name="p192621940113513"></a>若过滤“property”，可选“property_name”，值为属性名称，rightvalue的value字段填属性的值。</p>
    </td>
    </tr>
    <tr id="row17989142917312"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p109901029138"><a name="p109901029138"></a><a name="p109901029138"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p199908295316"><a name="p199908295316"></a><a name="p199908295316"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.24%" headers="mcps1.2.5.1.3 "><p id="p4990929937"><a name="p4990929937"></a><a name="p4990929937"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60.25%" headers="mcps1.2.5.1.4 "><p id="p776311301645"><a name="p776311301645"></a><a name="p776311301645"></a>若对节点ID做过滤，可选id，值可不填。</p>
    </td>
    </tr>
    <tr id="row12991192917317"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p1399119298317"><a name="p1399119298317"></a><a name="p1399119298317"></a>property_filter</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p7991102912314"><a name="p7991102912314"></a><a name="p7991102912314"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.24%" headers="mcps1.2.5.1.3 "><p id="p11991529536"><a name="p11991529536"></a><a name="p11991529536"></a>JSON String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60.25%" headers="mcps1.2.5.1.4 "><p id="p17763830942"><a name="p17763830942"></a><a name="p17763830942"></a>若<span class="parmname" id="parmname1677752019518"><a name="parmname1677752019518"></a><a name="parmname1677752019518"></a>“predicate”</span>为“&amp;”或者“|”，可在<span class="parmname" id="parmname15189189952"><a name="parmname15189189952"></a><a name="parmname15189189952"></a>“leftvalue”</span>和<span class="parmname" id="parmname346314151520"><a name="parmname346314151520"></a><a name="parmname346314151520"></a>“rightvalue”</span>中嵌套使用<span class="parmname" id="parmname104713271152"><a name="parmname104713271152"></a><a name="parmname104713271152"></a>“property_filter”</span>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 8**  rightvalue元素格式

    <a name="table410075413418"></a>
    <table><thead align="left"><tr id="row171001854103412"><th class="cellrowborder" valign="top" width="15.39%" id="mcps1.2.5.1.1"><p id="p1510025493415"><a name="p1510025493415"></a><a name="p1510025493415"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.120000000000001%" id="mcps1.2.5.1.2"><p id="p131001954143414"><a name="p131001954143414"></a><a name="p131001954143414"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="14.66%" id="mcps1.2.5.1.3"><p id="p1410020543347"><a name="p1410020543347"></a><a name="p1410020543347"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="57.830000000000005%" id="mcps1.2.5.1.4"><p id="p201016548344"><a name="p201016548344"></a><a name="p201016548344"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row310112547346"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p227105711400"><a name="p227105711400"></a><a name="p227105711400"></a>value</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p127105718403"><a name="p127105718403"></a><a name="p127105718403"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.3 "><p id="p1927135714405"><a name="p1927135714405"></a><a name="p1927135714405"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.830000000000005%" headers="mcps1.2.5.1.4 "><a name="ul1374165784115"></a><a name="ul1374165784115"></a><ul id="ul1374165784115"><li>若过滤“label”，值为label的名称。</li><li>若过滤“property”，值为属性名称。</li></ul>
    </td>
    </tr>
    <tr id="row82115421650"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p485812014619"><a name="p485812014619"></a><a name="p485812014619"></a>property_filter</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.5.1.2 "><p id="p1085860162"><a name="p1085860162"></a><a name="p1085860162"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.66%" headers="mcps1.2.5.1.3 "><p id="p13858301968"><a name="p13858301968"></a><a name="p13858301968"></a>JSON String</p>
    </td>
    <td class="cellrowborder" valign="top" width="57.830000000000005%" headers="mcps1.2.5.1.4 "><p id="p8858101263"><a name="p8858101263"></a><a name="p8858101263"></a>若<span class="parmname" id="parmname28581008611"><a name="parmname28581008611"></a><a name="parmname28581008611"></a>“predicate”</span>为“&amp;”或者“|”，可在<span class="parmname" id="parmname138594012611"><a name="parmname138594012611"></a><a name="parmname138594012611"></a>“leftvalue”</span>和<span class="parmname" id="parmname15859160868"><a name="parmname15859160868"></a><a name="parmname15859160868"></a>“rightvalue”</span>中嵌套使用<span class="parmname" id="parmname58591405612"><a name="parmname58591405612"></a><a name="parmname58591405612"></a>“property_filter”</span>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 9**  predicate使用场景

    <a name="table11762850068"></a>
    <table><thead align="left"><tr id="row1976317507612"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.6.1.1"><p id="p985817241376"><a name="p985817241376"></a><a name="p985817241376"></a>predicate</p>
    </th>
    <th class="cellrowborder" valign="top" width="20%" id="mcps1.2.6.1.2"><p id="p198588240714"><a name="p198588240714"></a><a name="p198588240714"></a>label_name</p>
    </th>
    <th class="cellrowborder" valign="top" width="20%" id="mcps1.2.6.1.3"><p id="p188587241274"><a name="p188587241274"></a><a name="p188587241274"></a>id</p>
    </th>
    <th class="cellrowborder" valign="top" width="20%" id="mcps1.2.6.1.4"><p id="p1985932417712"><a name="p1985932417712"></a><a name="p1985932417712"></a>property_name</p>
    </th>
    <th class="cellrowborder" valign="top" width="20%" id="mcps1.2.6.1.5"><p id="p3859324177"><a name="p3859324177"></a><a name="p3859324177"></a>嵌套filter</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1476315503611"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.1 "><p id="p48591524472"><a name="p48591524472"></a><a name="p48591524472"></a>&amp;</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.2 "><p id="p108597241378"><a name="p108597241378"></a><a name="p108597241378"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.3 "><p id="p1685914241576"><a name="p1685914241576"></a><a name="p1685914241576"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.4 "><p id="p085912241773"><a name="p085912241773"></a><a name="p085912241773"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.5 "><p id="p985982411716"><a name="p985982411716"></a><a name="p985982411716"></a>是</p>
    </td>
    </tr>
    <tr id="row876475013617"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.1 "><p id="p68591243710"><a name="p68591243710"></a><a name="p68591243710"></a>|</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.2 "><p id="p28590249710"><a name="p28590249710"></a><a name="p28590249710"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.3 "><p id="p285917241278"><a name="p285917241278"></a><a name="p285917241278"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.4 "><p id="p18860224473"><a name="p18860224473"></a><a name="p18860224473"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.5 "><p id="p3860624676"><a name="p3860624676"></a><a name="p3860624676"></a>是</p>
    </td>
    </tr>
    <tr id="row976414500612"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.1 "><p id="p1486042411718"><a name="p1486042411718"></a><a name="p1486042411718"></a>HAS/HASNOT</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.2 "><p id="p586082414712"><a name="p586082414712"></a><a name="p586082414712"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.3 "><p id="p138601624876"><a name="p138601624876"></a><a name="p138601624876"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.4 "><p id="p13860824275"><a name="p13860824275"></a><a name="p13860824275"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.5 "><p id="p2860132418711"><a name="p2860132418711"></a><a name="p2860132418711"></a>否</p>
    </td>
    </tr>
    <tr id="row776514508610"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.1 "><p id="p1386032415715"><a name="p1386032415715"></a><a name="p1386032415715"></a>CONTAIN/NOTCONTAIN</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.2 "><p id="p386013241074"><a name="p386013241074"></a><a name="p386013241074"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.3 "><p id="p48610241173"><a name="p48610241173"></a><a name="p48610241173"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.4 "><p id="p886122412714"><a name="p886122412714"></a><a name="p886122412714"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.5 "><p id="p08614241772"><a name="p08614241772"></a><a name="p08614241772"></a>否</p>
    </td>
    </tr>
    <tr id="row776565010619"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.1 "><p id="p148627241175"><a name="p148627241175"></a><a name="p148627241175"></a>SUBSET</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.2 "><p id="p986218246718"><a name="p986218246718"></a><a name="p986218246718"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.3 "><p id="p19862102412713"><a name="p19862102412713"></a><a name="p19862102412713"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.4 "><p id="p188621724779"><a name="p188621724779"></a><a name="p188621724779"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.5 "><p id="p98622241720"><a name="p98622241720"></a><a name="p98622241720"></a>是（仅支持右值为集合，若为single，则无过滤作用直接匹配）</p>
    </td>
    </tr>
    <tr id="row177654501566"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.1 "><p id="p886213241971"><a name="p886213241971"></a><a name="p886213241971"></a>IN/NOTIN</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.2 "><p id="p10862324679"><a name="p10862324679"></a><a name="p10862324679"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.3 "><p id="p198621524974"><a name="p198621524974"></a><a name="p198621524974"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.4 "><p id="p4862122417712"><a name="p4862122417712"></a><a name="p4862122417712"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.5 "><p id="p108620241173"><a name="p108620241173"></a><a name="p108620241173"></a>是（仅支持右值为集合，若为single，则不匹配）</p>
    </td>
    </tr>
    <tr id="row376510501469"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.1 "><p id="p38631224171"><a name="p38631224171"></a><a name="p38631224171"></a>PREFIX</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.2 "><p id="p786392410710"><a name="p786392410710"></a><a name="p786392410710"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.3 "><p id="p18634240715"><a name="p18634240715"></a><a name="p18634240715"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.4 "><p id="p386317242712"><a name="p386317242712"></a><a name="p386317242712"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.5 "><p id="p1486312416711"><a name="p1486312416711"></a><a name="p1486312416711"></a>否</p>
    </td>
    </tr>
    <tr id="row376617501262"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.1 "><p id="p2863324376"><a name="p2863324376"></a><a name="p2863324376"></a>FUZZY</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.2 "><p id="p2086314241714"><a name="p2086314241714"></a><a name="p2086314241714"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.3 "><p id="p58647241178"><a name="p58647241178"></a><a name="p58647241178"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.4 "><p id="p138645241174"><a name="p138645241174"></a><a name="p138645241174"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.5 "><p id="p18641924378"><a name="p18641924378"></a><a name="p18641924378"></a>否</p>
    </td>
    </tr>
    <tr id="row107667501863"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.1 "><p id="p1786432420716"><a name="p1786432420716"></a><a name="p1786432420716"></a>REGEX</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.2 "><p id="p086418243713"><a name="p086418243713"></a><a name="p086418243713"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.3 "><p id="p1586414241377"><a name="p1586414241377"></a><a name="p1586414241377"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.4 "><p id="p168640241974"><a name="p168640241974"></a><a name="p168640241974"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.5 "><p id="p1286411241574"><a name="p1286411241574"></a><a name="p1286411241574"></a>否</p>
    </td>
    </tr>
    <tr id="row1576810503617"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.1 "><p id="p1186418241477"><a name="p1186418241477"></a><a name="p1186418241477"></a>SUBSTRING</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.2 "><p id="p1286417241078"><a name="p1286417241078"></a><a name="p1286417241078"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.3 "><p id="p16864122414715"><a name="p16864122414715"></a><a name="p16864122414715"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.4 "><p id="p486510241717"><a name="p486510241717"></a><a name="p486510241717"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.5 "><p id="p178654240718"><a name="p178654240718"></a><a name="p178654240718"></a>否</p>
    </td>
    </tr>
    <tr id="row197681450565"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.1 "><p id="p286517247716"><a name="p286517247716"></a><a name="p286517247716"></a>CISUBSTRING</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.2 "><p id="p686511240715"><a name="p686511240715"></a><a name="p686511240715"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.3 "><p id="p1486592416710"><a name="p1486592416710"></a><a name="p1486592416710"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.4 "><p id="p4866224278"><a name="p4866224278"></a><a name="p4866224278"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.5 "><p id="p198666241778"><a name="p198666241778"></a><a name="p198666241778"></a>否</p>
    </td>
    </tr>
    <tr id="row476811501164"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.1 "><p id="p10866162413717"><a name="p10866162413717"></a><a name="p10866162413717"></a>=/!=/&lt;/&lt;=/&gt;/&gt;=</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.2 "><p id="p198661524770"><a name="p198661524770"></a><a name="p198661524770"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.3 "><p id="p188661824776"><a name="p188661824776"></a><a name="p188661824776"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.4 "><p id="p1486622413720"><a name="p1486622413720"></a><a name="p1486622413720"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.6.1.5 "><p id="p1866224774"><a name="p1866224774"></a><a name="p1866224774"></a>否</p>
    </td>
    </tr>
    </tbody>
    </table>

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >-   支持左值是集合：body体中左值为string。
    >-   支持右值是集合：选择否，说明即使支持也仅匹配集合中第一个字符串。
    >-   boolean值匹配，当右值输入为”true”时，将被识别为“true”进行匹配，否则识别为“false”进行匹配。


## 响应<a name="section14834278202011"></a>

-   同步返回
    -   要素说明

        **表 10**  要素说明

        <a name="table9618153202456"></a>
        <table><thead align="left"><tr id="row19256001202456"><th class="cellrowborder" valign="top" width="14.2%" id="mcps1.2.5.1.1"><p id="p4115707020258"><a name="p4115707020258"></a><a name="p4115707020258"></a>参数</p>
        </th>
        <th class="cellrowborder" valign="top" width="15.45%" id="mcps1.2.5.1.2"><p id="p4538840820258"><a name="p4538840820258"></a><a name="p4538840820258"></a>是否必选</p>
        </th>
        <th class="cellrowborder" valign="top" width="9.790000000000001%" id="mcps1.2.5.1.3"><p id="p5258245920258"><a name="p5258245920258"></a><a name="p5258245920258"></a>类型</p>
        </th>
        <th class="cellrowborder" valign="top" width="60.56%" id="mcps1.2.5.1.4"><p id="p3132076620258"><a name="p3132076620258"></a><a name="p3132076620258"></a>说明</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="row65005079202456"><td class="cellrowborder" valign="top" width="14.2%" headers="mcps1.2.5.1.1 "><p id="p820509320258"><a name="p820509320258"></a><a name="p820509320258"></a>errorMessage</p>
        </td>
        <td class="cellrowborder" valign="top" width="15.45%" headers="mcps1.2.5.1.2 "><p id="p6063279320258"><a name="p6063279320258"></a><a name="p6063279320258"></a>否</p>
        </td>
        <td class="cellrowborder" valign="top" width="9.790000000000001%" headers="mcps1.2.5.1.3 "><p id="p1230923020258"><a name="p1230923020258"></a><a name="p1230923020258"></a>String</p>
        </td>
        <td class="cellrowborder" valign="top" width="60.56%" headers="mcps1.2.5.1.4 "><p id="p5752359620258"><a name="p5752359620258"></a><a name="p5752359620258"></a>系统提示信息，执行成功时，字段可能为空。执行失败时，用于显示错误信息。</p>
        </td>
        </tr>
        <tr id="row12849645202456"><td class="cellrowborder" valign="top" width="14.2%" headers="mcps1.2.5.1.1 "><p id="p5877047420258"><a name="p5877047420258"></a><a name="p5877047420258"></a>errorCode</p>
        </td>
        <td class="cellrowborder" valign="top" width="15.45%" headers="mcps1.2.5.1.2 "><p id="p6278797220258"><a name="p6278797220258"></a><a name="p6278797220258"></a>否</p>
        </td>
        <td class="cellrowborder" valign="top" width="9.790000000000001%" headers="mcps1.2.5.1.3 "><p id="p5266096220258"><a name="p5266096220258"></a><a name="p5266096220258"></a>String</p>
        </td>
        <td class="cellrowborder" valign="top" width="60.56%" headers="mcps1.2.5.1.4 "><p id="p3767953320258"><a name="p3767953320258"></a><a name="p3767953320258"></a>系统提示信息，执行成功时，字段可能为空。执行失败时，用于显示错误码。</p>
        </td>
        </tr>
        <tr id="row19451529144512"><td class="cellrowborder" valign="top" width="14.2%" headers="mcps1.2.5.1.1 "><p id="p118153914515"><a name="p118153914515"></a><a name="p118153914515"></a>data</p>
        </td>
        <td class="cellrowborder" valign="top" width="15.45%" headers="mcps1.2.5.1.2 "><p id="p918939174517"><a name="p918939174517"></a><a name="p918939174517"></a>否</p>
        </td>
        <td class="cellrowborder" valign="top" width="9.790000000000001%" headers="mcps1.2.5.1.3 "><p id="p418183918458"><a name="p418183918458"></a><a name="p418183918458"></a>JSON</p>
        </td>
        <td class="cellrowborder" valign="top" width="60.56%" headers="mcps1.2.5.1.4 "><p id="p918839194520"><a name="p918839194520"></a><a name="p918839194520"></a>查询结果。查询失败时，字段为空。</p>
        </td>
        </tr>
        </tbody>
        </table>

        **表 11**  data参数说明

        <a name="table189348255462"></a>
        <table><thead align="left"><tr id="row17935132504613"><th class="cellrowborder" valign="top" width="14.2%" id="mcps1.2.5.1.1"><p id="p9935142514466"><a name="p9935142514466"></a><a name="p9935142514466"></a>参数</p>
        </th>
        <th class="cellrowborder" valign="top" width="15.45%" id="mcps1.2.5.1.2"><p id="p17935102564619"><a name="p17935102564619"></a><a name="p17935102564619"></a>是否必选</p>
        </th>
        <th class="cellrowborder" valign="top" width="9.790000000000001%" id="mcps1.2.5.1.3"><p id="p1793517254469"><a name="p1793517254469"></a><a name="p1793517254469"></a>类型</p>
        </th>
        <th class="cellrowborder" valign="top" width="60.56%" id="mcps1.2.5.1.4"><p id="p1493512511461"><a name="p1493512511461"></a><a name="p1493512511461"></a>说明</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="row109361525104613"><td class="cellrowborder" valign="top" width="14.2%" headers="mcps1.2.5.1.1 "><p id="p163216618479"><a name="p163216618479"></a><a name="p163216618479"></a>vertices</p>
        </td>
        <td class="cellrowborder" valign="top" width="15.45%" headers="mcps1.2.5.1.2 "><p id="p53212614475"><a name="p53212614475"></a><a name="p53212614475"></a>否</p>
        </td>
        <td class="cellrowborder" valign="top" width="9.790000000000001%" headers="mcps1.2.5.1.3 "><p id="p1932466475"><a name="p1932466475"></a><a name="p1932466475"></a>List</p>
        </td>
        <td class="cellrowborder" valign="top" width="60.56%" headers="mcps1.2.5.1.4 "><p id="p173219634718"><a name="p173219634718"></a><a name="p173219634718"></a>点的结果集合。filters最后一层为点过滤时，data中将包含vertices。</p>
        </td>
        </tr>
        <tr id="row1393652510469"><td class="cellrowborder" valign="top" width="14.2%" headers="mcps1.2.5.1.1 "><p id="p93286154712"><a name="p93286154712"></a><a name="p93286154712"></a>edges</p>
        </td>
        <td class="cellrowborder" valign="top" width="15.45%" headers="mcps1.2.5.1.2 "><p id="p8328694715"><a name="p8328694715"></a><a name="p8328694715"></a>否</p>
        </td>
        <td class="cellrowborder" valign="top" width="9.790000000000001%" headers="mcps1.2.5.1.3 "><p id="p6321964475"><a name="p6321964475"></a><a name="p6321964475"></a>List</p>
        </td>
        <td class="cellrowborder" valign="top" width="60.56%" headers="mcps1.2.5.1.4 "><p id="p73296164717"><a name="p73296164717"></a><a name="p73296164717"></a>边的结果集合。filters最后一层为边过滤时，data中将包含edges。</p>
        </td>
        </tr>
        <tr id="row1066691081"><td class="cellrowborder" valign="top" width="14.2%" headers="mcps1.2.5.1.1 "><p id="p93943221786"><a name="p93943221786"></a><a name="p93943221786"></a>paths</p>
        </td>
        <td class="cellrowborder" valign="top" width="15.45%" headers="mcps1.2.5.1.2 "><p id="p039413221087"><a name="p039413221087"></a><a name="p039413221087"></a>否</p>
        </td>
        <td class="cellrowborder" valign="top" width="9.790000000000001%" headers="mcps1.2.5.1.3 "><p id="p183943221884"><a name="p183943221884"></a><a name="p183943221884"></a>List</p>
        </td>
        <td class="cellrowborder" valign="top" width="60.56%" headers="mcps1.2.5.1.4 "><p id="p1039411221284"><a name="p1039411221284"></a><a name="p1039411221284"></a>路径信息集合。with_path为true时可输出。格式见<a href="#table567611528814">表12</a>。</p>
        </td>
        </tr>
        </tbody>
        </table>

        **表 12**  path参数说明

        <a name="table567611528814"></a>
        <table><thead align="left"><tr id="row196771552582"><th class="cellrowborder" valign="top" width="14.2%" id="mcps1.2.5.1.1"><p id="p15677452680"><a name="p15677452680"></a><a name="p15677452680"></a>参数</p>
        </th>
        <th class="cellrowborder" valign="top" width="10.97%" id="mcps1.2.5.1.2"><p id="p467795219817"><a name="p467795219817"></a><a name="p467795219817"></a>是否必选</p>
        </th>
        <th class="cellrowborder" valign="top" width="14.27%" id="mcps1.2.5.1.3"><p id="p196778529818"><a name="p196778529818"></a><a name="p196778529818"></a>类型</p>
        </th>
        <th class="cellrowborder" valign="top" width="60.56%" id="mcps1.2.5.1.4"><p id="p167718527818"><a name="p167718527818"></a><a name="p167718527818"></a>说明</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="row20677135215814"><td class="cellrowborder" valign="top" width="14.2%" headers="mcps1.2.5.1.1 "><p id="p151043699"><a name="p151043699"></a><a name="p151043699"></a>source</p>
        </td>
        <td class="cellrowborder" valign="top" width="10.97%" headers="mcps1.2.5.1.2 "><p id="p1467815523814"><a name="p1467815523814"></a><a name="p1467815523814"></a>是</p>
        </td>
        <td class="cellrowborder" valign="top" width="14.27%" headers="mcps1.2.5.1.3 "><p id="p967815521811"><a name="p967815521811"></a><a name="p967815521811"></a>String</p>
        </td>
        <td class="cellrowborder" valign="top" width="60.56%" headers="mcps1.2.5.1.4 "><p id="p5417428121018"><a name="p5417428121018"></a><a name="p5417428121018"></a>源点ID</p>
        </td>
        </tr>
        <tr id="row267813520811"><td class="cellrowborder" valign="top" width="14.2%" headers="mcps1.2.5.1.1 "><p id="p1813431593"><a name="p1813431593"></a><a name="p1813431593"></a>target</p>
        </td>
        <td class="cellrowborder" valign="top" width="10.97%" headers="mcps1.2.5.1.2 "><p id="p1437920641017"><a name="p1437920641017"></a><a name="p1437920641017"></a>是</p>
        </td>
        <td class="cellrowborder" valign="top" width="14.27%" headers="mcps1.2.5.1.3 "><p id="p837920614103"><a name="p837920614103"></a><a name="p837920614103"></a>String</p>
        </td>
        <td class="cellrowborder" valign="top" width="60.56%" headers="mcps1.2.5.1.4 "><p id="p194171928191012"><a name="p194171928191012"></a><a name="p194171928191012"></a>终点ID</p>
        </td>
        </tr>
        <tr id="row1367916523817"><td class="cellrowborder" valign="top" width="14.2%" headers="mcps1.2.5.1.1 "><p id="p5114316914"><a name="p5114316914"></a><a name="p5114316914"></a>index</p>
        </td>
        <td class="cellrowborder" valign="top" width="10.97%" headers="mcps1.2.5.1.2 "><p id="p17899961018"><a name="p17899961018"></a><a name="p17899961018"></a>是</p>
        </td>
        <td class="cellrowborder" valign="top" width="14.27%" headers="mcps1.2.5.1.3 "><p id="p208920921011"><a name="p208920921011"></a><a name="p208920921011"></a>String</p>
        </td>
        <td class="cellrowborder" valign="top" width="60.56%" headers="mcps1.2.5.1.4 "><p id="p9417928111011"><a name="p9417928111011"></a><a name="p9417928111011"></a>边index</p>
        </td>
        </tr>
        <tr id="row9646531894"><td class="cellrowborder" valign="top" width="14.2%" headers="mcps1.2.5.1.1 "><p id="p3174317915"><a name="p3174317915"></a><a name="p3174317915"></a>label</p>
        </td>
        <td class="cellrowborder" valign="top" width="10.97%" headers="mcps1.2.5.1.2 "><p id="p6871311151017"><a name="p6871311151017"></a><a name="p6871311151017"></a>是</p>
        </td>
        <td class="cellrowborder" valign="top" width="14.27%" headers="mcps1.2.5.1.3 "><p id="p1187101116104"><a name="p1187101116104"></a><a name="p1187101116104"></a>String</p>
        </td>
        <td class="cellrowborder" valign="top" width="60.56%" headers="mcps1.2.5.1.4 "><p id="p6418202813100"><a name="p6418202813100"></a><a name="p6418202813100"></a>边label</p>
        </td>
        </tr>
        </tbody>
        </table>


    -   请求成功样例

        ```
        Http Status Code: 200
        {
            "data": {
                "edges": [
                    {
                        "index": "1",
                        "source": "tr_1",
                        "label": "rate",
                        "properties": {
                            "Rating": [
                                0
                            ],
                            "Datetime": [
                                ""
                            ]
                        },
                        "target": "tr_3"
                    },
                    ……,
                    {
                        "index": "199998",
                        "source": "tr_1",
                        "label": "rate",
                        "properties": {
                            "Rating": [
                                0
                            ],
                            "Datetime": [
                                ""
                            ]
                        },
                        "target": "tr_200000"
                    }
                ]
            }
        }
        
        ```

    -   请求失败样例

        ```
        Http Status Code: 400
        {
            "errorMessage": "graph [tesdt_117] is not found",
            "errorCode": "GES.8806"
        }
        ```



-   异步返回
    -   要素说明

        **表 13**  要素说明

        <a name="table1462119174918"></a>
        <table><thead align="left"><tr id="row15463171919496"><th class="cellrowborder" valign="top" width="14.2%" id="mcps1.2.5.1.1"><p id="p13463219194917"><a name="p13463219194917"></a><a name="p13463219194917"></a>参数</p>
        </th>
        <th class="cellrowborder" valign="top" width="15.45%" id="mcps1.2.5.1.2"><p id="p184637199490"><a name="p184637199490"></a><a name="p184637199490"></a>是否必选</p>
        </th>
        <th class="cellrowborder" valign="top" width="9.790000000000001%" id="mcps1.2.5.1.3"><p id="p9463201914919"><a name="p9463201914919"></a><a name="p9463201914919"></a>类型</p>
        </th>
        <th class="cellrowborder" valign="top" width="60.56%" id="mcps1.2.5.1.4"><p id="p1846321994913"><a name="p1846321994913"></a><a name="p1846321994913"></a>说明</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="row946311193499"><td class="cellrowborder" valign="top" width="14.2%" headers="mcps1.2.5.1.1 "><p id="p124639193495"><a name="p124639193495"></a><a name="p124639193495"></a>errorMessage</p>
        </td>
        <td class="cellrowborder" valign="top" width="15.45%" headers="mcps1.2.5.1.2 "><p id="p346461954917"><a name="p346461954917"></a><a name="p346461954917"></a>否</p>
        </td>
        <td class="cellrowborder" valign="top" width="9.790000000000001%" headers="mcps1.2.5.1.3 "><p id="p3464319104919"><a name="p3464319104919"></a><a name="p3464319104919"></a>String</p>
        </td>
        <td class="cellrowborder" valign="top" width="60.56%" headers="mcps1.2.5.1.4 "><p id="p44641193496"><a name="p44641193496"></a><a name="p44641193496"></a>系统提示信息，执行成功时，字段可能为空。执行失败时，用于显示错误信息。</p>
        </td>
        </tr>
        <tr id="row19464131964915"><td class="cellrowborder" valign="top" width="14.2%" headers="mcps1.2.5.1.1 "><p id="p14464319134920"><a name="p14464319134920"></a><a name="p14464319134920"></a>errorCode</p>
        </td>
        <td class="cellrowborder" valign="top" width="15.45%" headers="mcps1.2.5.1.2 "><p id="p14652193499"><a name="p14652193499"></a><a name="p14652193499"></a>否</p>
        </td>
        <td class="cellrowborder" valign="top" width="9.790000000000001%" headers="mcps1.2.5.1.3 "><p id="p3465101944914"><a name="p3465101944914"></a><a name="p3465101944914"></a>String</p>
        </td>
        <td class="cellrowborder" valign="top" width="60.56%" headers="mcps1.2.5.1.4 "><p id="p104651719104915"><a name="p104651719104915"></a><a name="p104651719104915"></a>系统提示信息，执行成功时，字段可能为空。执行失败时，用于显示错误码。</p>
        </td>
        </tr>
        <tr id="row446512193492"><td class="cellrowborder" valign="top" width="14.2%" headers="mcps1.2.5.1.1 "><p id="p512425054918"><a name="p512425054918"></a><a name="p512425054918"></a>jobId</p>
        </td>
        <td class="cellrowborder" valign="top" width="15.45%" headers="mcps1.2.5.1.2 "><p id="p612511504497"><a name="p612511504497"></a><a name="p612511504497"></a>否</p>
        </td>
        <td class="cellrowborder" valign="top" width="9.790000000000001%" headers="mcps1.2.5.1.3 "><p id="p0125115017498"><a name="p0125115017498"></a><a name="p0125115017498"></a>String</p>
        </td>
        <td class="cellrowborder" valign="top" width="60.56%" headers="mcps1.2.5.1.4 "><p id="p91257500494"><a name="p91257500494"></a><a name="p91257500494"></a>执行算法任务ID。请求失败时，字段为空。</p>
        </td>
        </tr>
        <tr id="row18701381494"><td class="cellrowborder" valign="top" width="14.2%" headers="mcps1.2.5.1.1 "><p id="p19125155014492"><a name="p19125155014492"></a><a name="p19125155014492"></a>jobType</p>
        </td>
        <td class="cellrowborder" valign="top" width="15.45%" headers="mcps1.2.5.1.2 "><p id="p912565044918"><a name="p912565044918"></a><a name="p912565044918"></a>否</p>
        </td>
        <td class="cellrowborder" valign="top" width="9.790000000000001%" headers="mcps1.2.5.1.3 "><p id="p131253509497"><a name="p131253509497"></a><a name="p131253509497"></a>Integer</p>
        </td>
        <td class="cellrowborder" valign="top" width="60.56%" headers="mcps1.2.5.1.4 "><p id="p71251450184915"><a name="p71251450184915"></a><a name="p71251450184915"></a>任务类型。请求失败时，字段为空。</p>
        </td>
        </tr>
        </tbody>
        </table>


    -   请求成功样例

        ```
        Http Status Code: 200
        {
            "jobId": "6622f13c-4b88-45f5-89a9-eaa096647c4a",
            "jobType": 1
        }
        ```

    -   请求失败样例

        ```
        Http Status Code: 400
        {
            "errorMessage": "executionMode is not correct, it should be sync or async",
            "errorCode": "GES.8806"
        }
        ```



## 返回值<a name="section3824743202011"></a>

-   正常

    200

-   异常

    **表 14**  异常返回值说明

    <a name="table7140218185450"></a>
    <table><thead align="left"><tr id="row1329614185450"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p3495986518551"><a name="p3495986518551"></a><a name="p3495986518551"></a>返回值</p>
    </th>
    <th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p1317678318551"><a name="p1317678318551"></a><a name="p1317678318551"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row22356742185450"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1665962118551"><a name="p1665962118551"></a><a name="p1665962118551"></a>400 Bad Request</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p725208518551"><a name="p725208518551"></a><a name="p725208518551"></a>请求错误。</p>
    </td>
    </tr>
    <tr id="row44828867185450"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p5227908718551"><a name="p5227908718551"></a><a name="p5227908718551"></a>401 Unauthorized</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p674761518551"><a name="p674761518551"></a><a name="p674761518551"></a>鉴权失败。</p>
    </td>
    </tr>
    <tr id="row57737827185450"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p2006437818551"><a name="p2006437818551"></a><a name="p2006437818551"></a>403 Forbidden</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1460190818551"><a name="p1460190818551"></a><a name="p1460190818551"></a>没有操作权限。</p>
    </td>
    </tr>
    <tr id="row29364829185450"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p4159095618551"><a name="p4159095618551"></a><a name="p4159095618551"></a>404 Not Found</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1342429918551"><a name="p1342429918551"></a><a name="p1342429918551"></a>找不到资源。</p>
    </td>
    </tr>
    <tr id="row4978157185450"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p5552901118551"><a name="p5552901118551"></a><a name="p5552901118551"></a>500 Internal Server Error</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p155603218551"><a name="p155603218551"></a><a name="p155603218551"></a>服务内部错误。</p>
    </td>
    </tr>
    <tr id="row18376792185450"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p6060569918551"><a name="p6060569918551"></a><a name="p6060569918551"></a>503 Service Unavailable</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1011455218551"><a name="p1011455218551"></a><a name="p1011455218551"></a>服务不可用。</p>
    </td>
    </tr>
    </tbody>
    </table>



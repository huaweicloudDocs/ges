# 执行Gremlin查询<a name="ges_03_0029"></a>

## 功能介绍<a name="section50978968191517"></a>

根据Gremlin语句，返回查询结果。

## URI<a name="section52466462191517"></a>

-   URI 格式

    ```
    POST /ges/v1.0/{projectId}/graphs/{graphName}/action?action_id=execute-gremlin-query
    ```

-   参数说明

    **表 1**  URI参数说明

    <a name="table47709151191539"></a>
    <table><thead align="left"><tr id="row39224537191539"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p46922758191555"><a name="p46922758191555"></a><a name="p46922758191555"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="p42647029191555"><a name="p42647029191555"></a><a name="p42647029191555"></a>是否为必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.3"><p id="p31857313191555"><a name="p31857313191555"></a><a name="p31857313191555"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="p30305521191555"><a name="p30305521191555"></a><a name="p30305521191555"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row60191230191539"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p58069150191555"><a name="p58069150191555"></a><a name="p58069150191555"></a>projectId</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p5980748191555"><a name="p5980748191555"></a><a name="p5980748191555"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p14678590191555"><a name="p14678590191555"></a><a name="p14678590191555"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p48115165191555"><a name="p48115165191555"></a><a name="p48115165191555"></a>服务所在域ID。</p>
    </td>
    </tr>
    <tr id="row65057755191539"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p45128597191555"><a name="p45128597191555"></a><a name="p45128597191555"></a>graphName</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p31537730191555"><a name="p31537730191555"></a><a name="p31537730191555"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p4419319191555"><a name="p4419319191555"></a><a name="p4419319191555"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p22420573191555"><a name="p22420573191555"></a><a name="p22420573191555"></a>图名称。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求<a name="section41515012191517"></a>

-   请求样例

    ```
    POST http://Endpoint/ges/v1.0/{projectId}/graphs/{graphName}/action?action_id=execute-gremlin-query
    {       
        "command":"g.V().limit(100)" 
    }
    ```

-   Body参数说明

    **表 2**  Body参数说明

    <a name="table53027413191617"></a>
    <table><thead align="left"><tr id="row24504688191617"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p53255191191648"><a name="p53255191191648"></a><a name="p53255191191648"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="p18703221191648"><a name="p18703221191648"></a><a name="p18703221191648"></a>是否为必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.3"><p id="p38565972191648"><a name="p38565972191648"></a><a name="p38565972191648"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="p36836060191648"><a name="p36836060191648"></a><a name="p36836060191648"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row37220753191617"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p22372356191648"><a name="p22372356191648"></a><a name="p22372356191648"></a>command</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p221557191648"><a name="p221557191648"></a><a name="p221557191648"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p17946158191648"><a name="p17946158191648"></a><a name="p17946158191648"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p44352728191648"><a name="p44352728191648"></a><a name="p44352728191648"></a>查询命令(Gremlin语言)。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 响应<a name="section54598423191517"></a>

-   要素说明

    **表 3**  响应要素说明

    <a name="table22641075191745"></a>
    <table><thead align="left"><tr id="row4372910191745"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p2873064319181"><a name="p2873064319181"></a><a name="p2873064319181"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="p4548073619181"><a name="p4548073619181"></a><a name="p4548073619181"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.3"><p id="p6006098119181"><a name="p6006098119181"></a><a name="p6006098119181"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="p3310130719181"><a name="p3310130719181"></a><a name="p3310130719181"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row62523322191745"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p1339512819181"><a name="p1339512819181"></a><a name="p1339512819181"></a>errorMessage</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p1126361619181"><a name="p1126361619181"></a><a name="p1126361619181"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p3993768819181"><a name="p3993768819181"></a><a name="p3993768819181"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p1372727219181"><a name="p1372727219181"></a><a name="p1372727219181"></a>系统提示信息，执行成功时，字段可能为空。执行失败时，用于显示错误信息。</p>
    </td>
    </tr>
    <tr id="row22384938191745"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p796099719181"><a name="p796099719181"></a><a name="p796099719181"></a>errorCode</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p4086103419181"><a name="p4086103419181"></a><a name="p4086103419181"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p2140944319181"><a name="p2140944319181"></a><a name="p2140944319181"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p5644332119181"><a name="p5644332119181"></a><a name="p5644332119181"></a>系统提示信息，执行成功时，字段可能为空。执行失败时，用于显示错误码。</p>
    </td>
    </tr>
    <tr id="row34709046191745"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p944746919181"><a name="p944746919181"></a><a name="p944746919181"></a>data</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p2704752919181"><a name="p2704752919181"></a><a name="p2704752919181"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p4336623719181"><a name="p4336623719181"></a><a name="p4336623719181"></a>JSON</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p2300433819181"><a name="p2300433819181"></a><a name="p2300433819181"></a>查询结果。请求失败时，字段为空。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   请求成功响应样例

    ```
    Http Status Code: 200
    
    {
        "data": {
    
    
                    
    
    
            "runtime": 0.775425022,
            "vertices": [
                {
                    "id": "Vivian",
                    "label": "user",
                    "properties": {
                        "Occupation": [
                            "artist"
                        ],
                        "ChineseName": [
                            "薇薇安"
                        ],
                        "Zip-code": [
                            "98133"
                        ],
                        "Gender": [
                            "F"
                        ],
                        "Age": [
                            "25-34"
                        ]
                    }
                },
                ......
            ]
        }
    }
    ```

-   请求失败样例

    ```
    Http Status Code: 400
    {
        "errorMessage": "org.apache.tinkerpop.gremlin.driver.exception.ResponseException: No such property: g1 for class: Script4",
        "errorCode": "GES.8503"
    }
    ```


## 返回值<a name="section35138213191517"></a>

-   正常

    200

-   异常

    **表 4**  异常返回值说明

    <a name="table2984752518246"></a>
    <table><thead align="left"><tr id="row1211940418246"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p3980654218254"><a name="p3980654218254"></a><a name="p3980654218254"></a>返回值</p>
    </th>
    <th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p310447318254"><a name="p310447318254"></a><a name="p310447318254"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row4240912018246"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p3446280418254"><a name="p3446280418254"></a><a name="p3446280418254"></a>400 Bad Request</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p4002370018254"><a name="p4002370018254"></a><a name="p4002370018254"></a>请求错误。</p>
    </td>
    </tr>
    <tr id="row4888805618246"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p5203043918254"><a name="p5203043918254"></a><a name="p5203043918254"></a>401 Unauthorized</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p5371601718254"><a name="p5371601718254"></a><a name="p5371601718254"></a>鉴权失败。</p>
    </td>
    </tr>
    <tr id="row3592872518246"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p3450921718254"><a name="p3450921718254"></a><a name="p3450921718254"></a>403 Forbidden</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p4378321618254"><a name="p4378321618254"></a><a name="p4378321618254"></a>没有操作权限。</p>
    </td>
    </tr>
    <tr id="row4281759818246"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p4125438418254"><a name="p4125438418254"></a><a name="p4125438418254"></a>404 Not Found</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p5327079718254"><a name="p5327079718254"></a><a name="p5327079718254"></a>找不到资源。</p>
    </td>
    </tr>
    <tr id="row994303918246"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p4548781618254"><a name="p4548781618254"></a><a name="p4548781618254"></a>500 Internal Server Error</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p6063444518254"><a name="p6063444518254"></a><a name="p6063444518254"></a>服务内部错误。</p>
    </td>
    </tr>
    <tr id="row5822219018246"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p4487805318254"><a name="p4487805318254"></a><a name="p4487805318254"></a>503 Service Unavailable</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1124370918254"><a name="p1124370918254"></a><a name="p1124370918254"></a>服务不可用。</p>
    </td>
    </tr>
    </tbody>
    </table>



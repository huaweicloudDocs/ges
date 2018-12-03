# 添加label<a name="ges_03_0056"></a>

## 功能介绍<a name="section11798179195415"></a>

添加label

## URI<a name="section10938344195415"></a>

-   URI格式

    ```
    POST /ges/v1.0/{projectId}/graphs/{graphName}/schema/labels
    ```


-   参数说明

    **表 1**  URI参数说明

    <a name="table13592207195454"></a>
    <table><thead align="left"><tr id="row11434212195454"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p59741794195512"><a name="p59741794195512"></a><a name="p59741794195512"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="p7247108195512"><a name="p7247108195512"></a><a name="p7247108195512"></a>是否为必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.3"><p id="p50144891195512"><a name="p50144891195512"></a><a name="p50144891195512"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="p35204399195512"><a name="p35204399195512"></a><a name="p35204399195512"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row49352481195454"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p54464108195512"><a name="p54464108195512"></a><a name="p54464108195512"></a>projectId</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p49516613195512"><a name="p49516613195512"></a><a name="p49516613195512"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p51422715195512"><a name="p51422715195512"></a><a name="p51422715195512"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p4490357195512"><a name="p4490357195512"></a><a name="p4490357195512"></a>服务所在域ID。</p>
    </td>
    </tr>
    <tr id="row23325114195454"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p52244987195512"><a name="p52244987195512"></a><a name="p52244987195512"></a>graphName</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p3985551195512"><a name="p3985551195512"></a><a name="p3985551195512"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p54394244195512"><a name="p54394244195512"></a><a name="p54394244195512"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p43857666195512"><a name="p43857666195512"></a><a name="p43857666195512"></a>图名称。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求<a name="section1235739195415"></a>

-   请求样例

    ```
    POST http://Endpoint/ges/v1.0/{projectId}/graphs/{graphName}/schema/labels  
    
    {
        "name":"book",
        "properties":[
            {
                "property":{
                    "name":"Title",
                    "cardinality":"single",
                    "dataType":"string"
                }
            },
            {
                "property":{
                    "name":"Version",
                    "cardinality":"single",
                    "dataType":"string"
                }
            }
        ]
    }
    ```

-   Body参数说明

    **表 2**  Body参数说明

    <a name="table22545074195633"></a>
    <table><thead align="left"><tr id="row60806065195633"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p44837705195650"><a name="p44837705195650"></a><a name="p44837705195650"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="p7975482195650"><a name="p7975482195650"></a><a name="p7975482195650"></a>是否为必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.3"><p id="p42034271195650"><a name="p42034271195650"></a><a name="p42034271195650"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="p49332768195650"><a name="p49332768195650"></a><a name="p49332768195650"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row25605686195633"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p6245529195650"><a name="p6245529195650"></a><a name="p6245529195650"></a>name</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p36125856195650"><a name="p36125856195650"></a><a name="p36125856195650"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p40513252195650"><a name="p40513252195650"></a><a name="p40513252195650"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p60347980195650"><a name="p60347980195650"></a><a name="p60347980195650"></a>label名称。</p>
    </td>
    </tr>
    <tr id="row34935955195633"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p37371979195650"><a name="p37371979195650"></a><a name="p37371979195650"></a>property</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p7231486195650"><a name="p7231486195650"></a><a name="p7231486195650"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p48879473195650"><a name="p48879473195650"></a><a name="p48879473195650"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p66923212195650"><a name="p66923212195650"></a><a name="p66923212195650"></a>属性。</p>
    </td>
    </tr>
    <tr id="row34743307195633"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p65986684195650"><a name="p65986684195650"></a><a name="p65986684195650"></a>name</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p43321155195650"><a name="p43321155195650"></a><a name="p43321155195650"></a>否（若property已选，则必选）</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p19352687195650"><a name="p19352687195650"></a><a name="p19352687195650"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p24063848195650"><a name="p24063848195650"></a><a name="p24063848195650"></a>属性名称。</p>
    </td>
    </tr>
    <tr id="row4190559195633"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p27132099195650"><a name="p27132099195650"></a><a name="p27132099195650"></a>cardinality</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p50216410195650"><a name="p50216410195650"></a><a name="p50216410195650"></a>否（若property已选，则必选）</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p40997401195650"><a name="p40997401195650"></a><a name="p40997401195650"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p32455209195650"><a name="p32455209195650"></a><a name="p32455209195650"></a>属性的复合类型（单值、多值）。</p>
    </td>
    </tr>
    <tr id="row59011224195633"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p37527747195650"><a name="p37527747195650"></a><a name="p37527747195650"></a>dataType</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p19848627195650"><a name="p19848627195650"></a><a name="p19848627195650"></a>否（若property已选，则必选）</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p64234927195650"><a name="p64234927195650"></a><a name="p64234927195650"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p35646624195650"><a name="p35646624195650"></a><a name="p35646624195650"></a>属性的数据类型。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 响应<a name="section31024304195415"></a>

-   要素说明

    **表 3**  要素说明

    <a name="table415208195710"></a>
    <table><thead align="left"><tr id="row62827717195710"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p5798135195724"><a name="p5798135195724"></a><a name="p5798135195724"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="p66995796195724"><a name="p66995796195724"></a><a name="p66995796195724"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.3"><p id="p57950414195724"><a name="p57950414195724"></a><a name="p57950414195724"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="p63471948195724"><a name="p63471948195724"></a><a name="p63471948195724"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row66822716195710"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p28953206195724"><a name="p28953206195724"></a><a name="p28953206195724"></a>errorMessage</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p63508338195724"><a name="p63508338195724"></a><a name="p63508338195724"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p43901714195724"><a name="p43901714195724"></a><a name="p43901714195724"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p66377918195724"><a name="p66377918195724"></a><a name="p66377918195724"></a>系统提示信息，执行成功时，字段可能为空。执行失败时，用于显示错误信息。</p>
    </td>
    </tr>
    <tr id="row41832689195710"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p4011871195724"><a name="p4011871195724"></a><a name="p4011871195724"></a>errorCode</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p56526154195724"><a name="p56526154195724"></a><a name="p56526154195724"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p15215774195724"><a name="p15215774195724"></a><a name="p15215774195724"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p24518145195724"><a name="p24518145195724"></a><a name="p24518145195724"></a>系统提示信息，执行成功时，字段可能为空。执行失败时，用于显示错误码。</p>
    </td>
    </tr>
    <tr id="row65130104195710"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p22770577195724"><a name="p22770577195724"></a><a name="p22770577195724"></a>result</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p32477429195724"><a name="p32477429195724"></a><a name="p32477429195724"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p13426086195724"><a name="p13426086195724"></a><a name="p13426086195724"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p13771147195724"><a name="p13771147195724"></a><a name="p13771147195724"></a>成功时result值为success。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   请求成功样例

    ```
    Http Status Code: 200
    {
    "result": "success"
    }
    ```

-   请求失败样例

    ```
    Http Status Code: 400
    {
    "errorMessage": "label [book] already exists",
    "errorCode": "GES.8009"
    }
    ```


## 返回值<a name="section17428054195415"></a>

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



# 批量添加label\(2.2.21\)<a name="ges_03_0219"></a>

## 功能介绍<a name="section11798179195415"></a>

批量添加label。

## URI<a name="section10938344195415"></a>

-   URI格式

    ```
    POST /ges/v1.0/{project_id}/graphs/{graph_name}/schema/labels/action?action_id=batch-add
    ```


-   参数说明

    **表 1**  URI参数说明

    <a name="table13592207195454"></a>
    <table><thead align="left"><tr id="row11434212195454"><th class="cellrowborder" valign="top" width="15.36%" id="mcps1.2.5.1.1"><p id="p59741794195512"><a name="p59741794195512"></a><a name="p59741794195512"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="14.469999999999999%" id="mcps1.2.5.1.2"><p id="p7247108195512"><a name="p7247108195512"></a><a name="p7247108195512"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.07%" id="mcps1.2.5.1.3"><p id="p50144891195512"><a name="p50144891195512"></a><a name="p50144891195512"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="53.1%" id="mcps1.2.5.1.4"><p id="p35204399195512"><a name="p35204399195512"></a><a name="p35204399195512"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row49352481195454"><td class="cellrowborder" valign="top" width="15.36%" headers="mcps1.2.5.1.1 "><p id="p54464108195512"><a name="p54464108195512"></a><a name="p54464108195512"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.469999999999999%" headers="mcps1.2.5.1.2 "><p id="p49516613195512"><a name="p49516613195512"></a><a name="p49516613195512"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.07%" headers="mcps1.2.5.1.3 "><p id="p51422715195512"><a name="p51422715195512"></a><a name="p51422715195512"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.1%" headers="mcps1.2.5.1.4 "><p id="p51708449194548"><a name="p51708449194548"></a><a name="p51708449194548"></a>项目编号，用于资源隔离。请参考<a href="获取项目ID.md">获取项目ID</a>。</p>
    </td>
    </tr>
    <tr id="row23325114195454"><td class="cellrowborder" valign="top" width="15.36%" headers="mcps1.2.5.1.1 "><p id="p52244987195512"><a name="p52244987195512"></a><a name="p52244987195512"></a>graph_name</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.469999999999999%" headers="mcps1.2.5.1.2 "><p id="p3985551195512"><a name="p3985551195512"></a><a name="p3985551195512"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.07%" headers="mcps1.2.5.1.3 "><p id="p54394244195512"><a name="p54394244195512"></a><a name="p54394244195512"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.1%" headers="mcps1.2.5.1.4 "><p id="p43857666195512"><a name="p43857666195512"></a><a name="p43857666195512"></a>图名称。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求<a name="section1235739195415"></a>

-   请求样例

    ```
    POST http://{SERVER_URL}/ges/v1.0/{project_id}/graphs/{graph_name}/schema/labels/action?action_id=batch-add  
    {
        "labels": [
            {
                "name": "book",
                "properties": [
                    {
                        "property": {
                            "name": "title",
                            "cardinality": "single",
                            "dataType": "string"
                        }
                    }
                ]
            },
            {
                "name": "movie",
                "properties": [
                    {
                        "property": {
                            "name": "movieid",
                            "cardinality": "single",
                            "dataType": "int"
                        }
                    }
                ]
            }
        ]
    }
    
    ```

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >SERVER\_URL：图的访问地址，取值请参考[业务面API使用限制](业务面API使用限制.md)。

    **表 2**  label参数说明

    <a name="table206321733114519"></a>
    <table><thead align="left"><tr id="row1663333314456"><th class="cellrowborder" valign="top" width="12.73%" id="mcps1.2.5.1.1"><p id="p872143720459"><a name="p872143720459"></a><a name="p872143720459"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="11.76%" id="mcps1.2.5.1.2"><p id="p872173714510"><a name="p872173714510"></a><a name="p872173714510"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="14.299999999999999%" id="mcps1.2.5.1.3"><p id="p3721637164519"><a name="p3721637164519"></a><a name="p3721637164519"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="61.21%" id="mcps1.2.5.1.4"><p id="p87273704517"><a name="p87273704517"></a><a name="p87273704517"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1363373319457"><td class="cellrowborder" valign="top" width="12.73%" headers="mcps1.2.5.1.1 "><p id="p773173719450"><a name="p773173719450"></a><a name="p773173719450"></a>name</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.76%" headers="mcps1.2.5.1.2 "><p id="p1573537164517"><a name="p1573537164517"></a><a name="p1573537164517"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.299999999999999%" headers="mcps1.2.5.1.3 "><p id="p373837184517"><a name="p373837184517"></a><a name="p373837184517"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="61.21%" headers="mcps1.2.5.1.4 "><p id="p57911377451"><a name="p57911377451"></a><a name="p57911377451"></a>label名称。</p>
    <p id="p1879173764510"><a name="p1879173764510"></a><a name="p1879173764510"></a>label name的长度不能超过256。</p>
    <p id="p15791374454"><a name="p15791374454"></a><a name="p15791374454"></a>label name只允许字符，数字, 空格，%,@,#,$,:,?,*,.,+,- 和 _符号。</p>
    </td>
    </tr>
    <tr id="row12633933164519"><td class="cellrowborder" valign="top" width="12.73%" headers="mcps1.2.5.1.1 "><p id="p1279173764517"><a name="p1279173764517"></a><a name="p1279173764517"></a>properties</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.76%" headers="mcps1.2.5.1.2 "><p id="p188073710453"><a name="p188073710453"></a><a name="p188073710453"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.299999999999999%" headers="mcps1.2.5.1.3 "><p id="p148043711453"><a name="p148043711453"></a><a name="p148043711453"></a>Json</p>
    </td>
    <td class="cellrowborder" valign="top" width="61.21%" headers="mcps1.2.5.1.4 "><p id="p58012371452"><a name="p58012371452"></a><a name="p58012371452"></a>待添加属性数组。数组元素为property，具体参数介绍请见<u id="u88016374457"><a name="u88016374457"></a><a name="u88016374457"></a><a href="#table41761251154611">表3</a></u>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 3**  property参数说明

    <a name="table41761251154611"></a>
    <table><thead align="left"><tr id="row1517695111465"><th class="cellrowborder" valign="top" width="19.64%" id="mcps1.2.5.1.1"><p id="p698016539464"><a name="p698016539464"></a><a name="p698016539464"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="16.61%" id="mcps1.2.5.1.2"><p id="p1980155314616"><a name="p1980155314616"></a><a name="p1980155314616"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.85%" id="mcps1.2.5.1.3"><p id="p10980105394617"><a name="p10980105394617"></a><a name="p10980105394617"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="50.9%" id="mcps1.2.5.1.4"><p id="p49801353194618"><a name="p49801353194618"></a><a name="p49801353194618"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row131761851194612"><td class="cellrowborder" valign="top" width="19.64%" headers="mcps1.2.5.1.1 "><p id="p19981105354616"><a name="p19981105354616"></a><a name="p19981105354616"></a>name</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.61%" headers="mcps1.2.5.1.2 "><p id="p39811853164612"><a name="p39811853164612"></a><a name="p39811853164612"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.85%" headers="mcps1.2.5.1.3 "><p id="p169811053134619"><a name="p169811053134619"></a><a name="p169811053134619"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.9%" headers="mcps1.2.5.1.4 "><p id="p139818530464"><a name="p139818530464"></a><a name="p139818530464"></a>属性名称。</p>
    <a name="ol178611488416"></a><a name="ol178611488416"></a><ol id="ol178611488416"><li>property name的长度不能超过256。</li><li>property name不允许包含&lt;, &gt;, &amp;, ASCII码14,15和30。</li><li>同一个label下不允许存在相同的property。</li></ol>
    </td>
    </tr>
    <tr id="row151766514466"><td class="cellrowborder" valign="top" width="19.64%" headers="mcps1.2.5.1.1 "><p id="p1998115318468"><a name="p1998115318468"></a><a name="p1998115318468"></a>cardinality</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.61%" headers="mcps1.2.5.1.2 "><p id="p1898155317469"><a name="p1898155317469"></a><a name="p1898155317469"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.85%" headers="mcps1.2.5.1.3 "><p id="p09818537461"><a name="p09818537461"></a><a name="p09818537461"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.9%" headers="mcps1.2.5.1.4 "><p id="p6981853204614"><a name="p6981853204614"></a><a name="p6981853204614"></a>属性的复合类型，包括：</p>
    <a name="ul94954344214"></a><a name="ul94954344214"></a><ul id="ul94954344214"><li>single</li><li>list</li><li>set</li></ul>
    </td>
    </tr>
    <tr id="row71772513468"><td class="cellrowborder" valign="top" width="19.64%" headers="mcps1.2.5.1.1 "><p id="p109819536464"><a name="p109819536464"></a><a name="p109819536464"></a>dataType</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.61%" headers="mcps1.2.5.1.2 "><p id="p89816535460"><a name="p89816535460"></a><a name="p89816535460"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.85%" headers="mcps1.2.5.1.3 "><p id="p17981205316469"><a name="p17981205316469"></a><a name="p17981205316469"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.9%" headers="mcps1.2.5.1.4 "><p id="p2981125318463"><a name="p2981125318463"></a><a name="p2981125318463"></a>属性的数据类型。具体请参考<u id="u199815535466"><a name="u199815535466"></a><a name="u199815535466"></a><a href="约束条件.md#table4745705017248">表1</a></u>中的元数据类型。</p>
    </td>
    </tr>
    <tr id="row117715114464"><td class="cellrowborder" valign="top" width="19.64%" headers="mcps1.2.5.1.1 "><p id="p69811353134611"><a name="p69811353134611"></a><a name="p69811353134611"></a>typeNameCount</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.61%" headers="mcps1.2.5.1.2 "><p id="p99826538467"><a name="p99826538467"></a><a name="p99826538467"></a>否（若dataType为enum，则必选）</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.85%" headers="mcps1.2.5.1.3 "><p id="p3982165313467"><a name="p3982165313467"></a><a name="p3982165313467"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.9%" headers="mcps1.2.5.1.4 "><p id="p5982145304610"><a name="p5982145304610"></a><a name="p5982145304610"></a>enum类型参数的总数。由该选项控制typeName的个数。</p>
    </td>
    </tr>
    <tr id="row1017755119469"><td class="cellrowborder" valign="top" width="19.64%" headers="mcps1.2.5.1.1 "><p id="p69821053134613"><a name="p69821053134613"></a><a name="p69821053134613"></a>typeName*</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.61%" headers="mcps1.2.5.1.2 "><p id="p17982135312463"><a name="p17982135312463"></a><a name="p17982135312463"></a>否（若dataType为enum，则必选）</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.85%" headers="mcps1.2.5.1.3 "><p id="p9982185314617"><a name="p9982185314617"></a><a name="p9982185314617"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="50.9%" headers="mcps1.2.5.1.4 "><p id="p5982353134615"><a name="p5982353134615"></a><a name="p5982353134615"></a>enum类型参数名称。例如typeNameCount为2，则参数包含typeName1:science，typeName2:literature。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 响应<a name="section31024304195415"></a>

-   要素说明

    **表 4**  要素说明

    <a name="table415208195710"></a>
    <table><thead align="left"><tr id="row62827717195710"><th class="cellrowborder" valign="top" width="18.26%" id="mcps1.2.5.1.1"><p id="p2091942720482"><a name="p2091942720482"></a><a name="p2091942720482"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="11.700000000000001%" id="mcps1.2.5.1.2"><p id="p79191927114818"><a name="p79191927114818"></a><a name="p79191927114818"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="9.58%" id="mcps1.2.5.1.3"><p id="p1991972713484"><a name="p1991972713484"></a><a name="p1991972713484"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="60.46%" id="mcps1.2.5.1.4"><p id="p1791932704816"><a name="p1791932704816"></a><a name="p1791932704816"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row66822716195710"><td class="cellrowborder" valign="top" width="18.26%" headers="mcps1.2.5.1.1 "><p id="p1792010277483"><a name="p1792010277483"></a><a name="p1792010277483"></a>errorMessage</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.700000000000001%" headers="mcps1.2.5.1.2 "><p id="p209203279488"><a name="p209203279488"></a><a name="p209203279488"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.58%" headers="mcps1.2.5.1.3 "><p id="p99201227184813"><a name="p99201227184813"></a><a name="p99201227184813"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60.46%" headers="mcps1.2.5.1.4 "><p id="p17920122714483"><a name="p17920122714483"></a><a name="p17920122714483"></a>系统提示信息，执行成功时，字段可能为空。执行失败时，用于显示错误信息。</p>
    </td>
    </tr>
    <tr id="row41832689195710"><td class="cellrowborder" valign="top" width="18.26%" headers="mcps1.2.5.1.1 "><p id="p29204272485"><a name="p29204272485"></a><a name="p29204272485"></a>errorCode</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.700000000000001%" headers="mcps1.2.5.1.2 "><p id="p1192092719488"><a name="p1192092719488"></a><a name="p1192092719488"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.58%" headers="mcps1.2.5.1.3 "><p id="p49207278489"><a name="p49207278489"></a><a name="p49207278489"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60.46%" headers="mcps1.2.5.1.4 "><p id="p1192042744818"><a name="p1192042744818"></a><a name="p1192042744818"></a>系统提示信息，执行成功时，字段可能为空。执行失败时，用于显示错误码。</p>
    </td>
    </tr>
    <tr id="row65130104195710"><td class="cellrowborder" valign="top" width="18.26%" headers="mcps1.2.5.1.1 "><p id="p109202027174815"><a name="p109202027174815"></a><a name="p109202027174815"></a>result</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.700000000000001%" headers="mcps1.2.5.1.2 "><p id="p149202027124816"><a name="p149202027124816"></a><a name="p149202027124816"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.58%" headers="mcps1.2.5.1.3 "><p id="p14920627174819"><a name="p14920627174819"></a><a name="p14920627174819"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60.46%" headers="mcps1.2.5.1.4 "><p id="p17920172715488"><a name="p17920172715488"></a><a name="p17920172715488"></a>成功时result值为success。</p>
    </td>
    </tr>
    <tr id="row1382615072018"><td class="cellrowborder" valign="top" width="18.26%" headers="mcps1.2.5.1.1 "><p id="p597615682019"><a name="p597615682019"></a><a name="p597615682019"></a>data</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.700000000000001%" headers="mcps1.2.5.1.2 "><p id="p89761256122015"><a name="p89761256122015"></a><a name="p89761256122015"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.58%" headers="mcps1.2.5.1.3 "><p id="p3976135642017"><a name="p3976135642017"></a><a name="p3976135642017"></a>Json</p>
    </td>
    <td class="cellrowborder" valign="top" width="60.46%" headers="mcps1.2.5.1.4 "><p id="p29762568202"><a name="p29762568202"></a><a name="p29762568202"></a>当批量添加部分失败时，data字段包含失败的label_name以及失败原因。</p>
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

-   请求部分成功样例

    ```
    Http Status Code: 200
    {
        "result": "partial success",
        "data": {
            "failed": [
                {
                    "cause": "label name is invalid  which can only contain letters, digits, space,%,@,#,$,:,?,*,.,+,- and _",
                    "labelName": "book<"
                }
            ]
        }
    }
    ```

-   请求失败样例

    ```
    Http Status Code: 400
     {
      "errorMessage": "label already exists",
      "errorCode": "GES.8801"
     }
    ```


## 返回值<a name="section17428054195415"></a>

-   正常

    200

-   异常

    **表 5**  异常返回值说明

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



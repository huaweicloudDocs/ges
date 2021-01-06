# 添加label（1.1.6）<a name="ges_03_0056"></a>

-   [功能介绍](#section11798179195415)
-   [URI](#section10938344195415)
-   [请求](#section1235739195415)
-   [响应](#section31024304195415)
-   [返回值](#section17428054195415)

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
    <tbody><tr id="row49352481195454"><td class="cellrowborder" valign="top" width="15.36%" headers="mcps1.2.5.1.1 "><p id="p54464108195512"><a name="p54464108195512"></a><a name="p54464108195512"></a>projectId</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.469999999999999%" headers="mcps1.2.5.1.2 "><p id="p49516613195512"><a name="p49516613195512"></a><a name="p49516613195512"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.07%" headers="mcps1.2.5.1.3 "><p id="p51422715195512"><a name="p51422715195512"></a><a name="p51422715195512"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.1%" headers="mcps1.2.5.1.4 "><p id="p51708449194548"><a name="p51708449194548"></a><a name="p51708449194548"></a>项目编号，用于资源隔离。请参考<a href="获取项目ID.md">获取项目ID</a>。</p>
    </td>
    </tr>
    <tr id="row23325114195454"><td class="cellrowborder" valign="top" width="15.36%" headers="mcps1.2.5.1.1 "><p id="p52244987195512"><a name="p52244987195512"></a><a name="p52244987195512"></a>graphName</p>
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
    POST http://{SERVER_URL}/ges/v1.0/{projectId}/graphs/{graphName}/schema/labels  
    {
      "name": "book",
      "properties": [
        {
          "property": {
            "name": "Title",
            "cardinality": "single",
            "dataType": "string"
          }
        },
        {
          "property": {
            "name": "Version",
            "cardinality": "single",
            "dataType": "string"
          }
        },
        {
          "property": {
            "name": "Category",
            "typeName1": "science",
            "typeName2": "literature",
            "typeNameCount": "2",
            "dataType": "enum"
          }
        }
      ]
    }
    ```

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >SERVER\_URL：图的访问地址，取值请参考[业务面API使用限制](业务面API使用限制.md)。

-   Body参数说明

    **表 2**  Body参数说明

    <a name="table22545074195633"></a>
    <table><thead align="left"><tr id="row60806065195633"><th class="cellrowborder" valign="top" width="14.499999999999998%" id="mcps1.2.5.1.1"><p id="p44837705195650"><a name="p44837705195650"></a><a name="p44837705195650"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="14.01%" id="mcps1.2.5.1.2"><p id="p7975482195650"><a name="p7975482195650"></a><a name="p7975482195650"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.26%" id="mcps1.2.5.1.3"><p id="p42034271195650"><a name="p42034271195650"></a><a name="p42034271195650"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="59.230000000000004%" id="mcps1.2.5.1.4"><p id="p49332768195650"><a name="p49332768195650"></a><a name="p49332768195650"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row25605686195633"><td class="cellrowborder" valign="top" width="14.499999999999998%" headers="mcps1.2.5.1.1 "><p id="p6245529195650"><a name="p6245529195650"></a><a name="p6245529195650"></a>name</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.01%" headers="mcps1.2.5.1.2 "><p id="p36125856195650"><a name="p36125856195650"></a><a name="p36125856195650"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.26%" headers="mcps1.2.5.1.3 "><p id="p40513252195650"><a name="p40513252195650"></a><a name="p40513252195650"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="59.230000000000004%" headers="mcps1.2.5.1.4 "><p id="p60347980195650"><a name="p60347980195650"></a><a name="p60347980195650"></a>label名称。</p>
    <p id="p157091332155"><a name="p157091332155"></a><a name="p157091332155"></a>label name的长度不能超过256。</p>
    <p id="p22621848145912"><a name="p22621848145912"></a><a name="p22621848145912"></a>label name只允许字符，数字, 空格，%,@,#,$,:,?,*,.,+,- 和 _符号。</p>
    </td>
    </tr>
    <tr id="row34935955195633"><td class="cellrowborder" valign="top" width="14.499999999999998%" headers="mcps1.2.5.1.1 "><p id="p37371979195650"><a name="p37371979195650"></a><a name="p37371979195650"></a>properties</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.01%" headers="mcps1.2.5.1.2 "><p id="p7231486195650"><a name="p7231486195650"></a><a name="p7231486195650"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.26%" headers="mcps1.2.5.1.3 "><p id="p48879473195650"><a name="p48879473195650"></a><a name="p48879473195650"></a>Json</p>
    </td>
    <td class="cellrowborder" valign="top" width="59.230000000000004%" headers="mcps1.2.5.1.4 "><p id="p66923212195650"><a name="p66923212195650"></a><a name="p66923212195650"></a>待添加属性数组。数组元素为property，具体参数介绍请见<a href="#table71249321157">表3</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 3**  property参数说明

    <a name="table71249321157"></a>
    <table><thead align="left"><tr id="row1112314328157"><th class="cellrowborder" valign="top" width="16.48%" id="mcps1.2.5.1.1"><p id="p1712383231511"><a name="p1712383231511"></a><a name="p1712383231511"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="20.52%" id="mcps1.2.5.1.2"><p id="p5123332121511"><a name="p5123332121511"></a><a name="p5123332121511"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="9.76%" id="mcps1.2.5.1.3"><p id="p1123173261518"><a name="p1123173261518"></a><a name="p1123173261518"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="53.239999999999995%" id="mcps1.2.5.1.4"><p id="p3123432121520"><a name="p3123432121520"></a><a name="p3123432121520"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row35188919527"><td class="cellrowborder" valign="top" width="16.48%" headers="mcps1.2.5.1.1 "><p id="p17323123495210"><a name="p17323123495210"></a><a name="p17323123495210"></a>name</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.52%" headers="mcps1.2.5.1.2 "><p id="p1232323455215"><a name="p1232323455215"></a><a name="p1232323455215"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.76%" headers="mcps1.2.5.1.3 "><p id="p153231734105212"><a name="p153231734105212"></a><a name="p153231734105212"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.239999999999995%" headers="mcps1.2.5.1.4 "><p id="p53231534165219"><a name="p53231534165219"></a><a name="p53231534165219"></a>属性名称。</p>
    <a name="ol4323133455214"></a><a name="ol4323133455214"></a><ol id="ol4323133455214"><li>property name的长度不能超过256。</li><li>property name不允许包含&lt;, &gt;, &amp;, ascci码14,15和30。</li><li>同一个label下不允许存在相同的property。</li></ol>
    </td>
    </tr>
    <tr id="row116859173528"><td class="cellrowborder" valign="top" width="16.48%" headers="mcps1.2.5.1.1 "><p id="p143241534165216"><a name="p143241534165216"></a><a name="p143241534165216"></a>cardinality</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.52%" headers="mcps1.2.5.1.2 "><p id="p16324534115218"><a name="p16324534115218"></a><a name="p16324534115218"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.76%" headers="mcps1.2.5.1.3 "><p id="p103241734115217"><a name="p103241734115217"></a><a name="p103241734115217"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.239999999999995%" headers="mcps1.2.5.1.4 "><p id="p1032473418522"><a name="p1032473418522"></a><a name="p1032473418522"></a>属性的复合类型，包括：</p>
    <a name="ul12324123485217"></a><a name="ul12324123485217"></a><ul id="ul12324123485217"><li>single</li><li>list</li><li>set</li></ul>
    </td>
    </tr>
    <tr id="row9124173219152"><td class="cellrowborder" valign="top" width="16.48%" headers="mcps1.2.5.1.1 "><p id="p1432413349524"><a name="p1432413349524"></a><a name="p1432413349524"></a>dataType</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.52%" headers="mcps1.2.5.1.2 "><p id="p7324173413522"><a name="p7324173413522"></a><a name="p7324173413522"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.76%" headers="mcps1.2.5.1.3 "><p id="p7324183455212"><a name="p7324183455212"></a><a name="p7324183455212"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.239999999999995%" headers="mcps1.2.5.1.4 "><p id="p16324934115220"><a name="p16324934115220"></a><a name="p16324934115220"></a>属性的数据类型。具体请参考<a href="约束条件.md#table4745705017248">表1</a>中的元数据类型。</p>
    </td>
    </tr>
    <tr id="row1812413291518"><td class="cellrowborder" valign="top" width="16.48%" headers="mcps1.2.5.1.1 "><p id="p203241134105219"><a name="p203241134105219"></a><a name="p203241134105219"></a>typeNameCount</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.52%" headers="mcps1.2.5.1.2 "><p id="p6324123417526"><a name="p6324123417526"></a><a name="p6324123417526"></a>否（若dataType为enum，则必选）</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.76%" headers="mcps1.2.5.1.3 "><p id="p93244342527"><a name="p93244342527"></a><a name="p93244342527"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.239999999999995%" headers="mcps1.2.5.1.4 "><p id="p2324934165214"><a name="p2324934165214"></a><a name="p2324934165214"></a>enum类型参数的总数。由该选项控制typeName的个数。</p>
    </td>
    </tr>
    <tr id="row10124232171517"><td class="cellrowborder" valign="top" width="16.48%" headers="mcps1.2.5.1.1 "><p id="p143241434175217"><a name="p143241434175217"></a><a name="p143241434175217"></a>typeName*</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.52%" headers="mcps1.2.5.1.2 "><p id="p1332443415520"><a name="p1332443415520"></a><a name="p1332443415520"></a>否（若dataType为enum，则必选）</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.76%" headers="mcps1.2.5.1.3 "><p id="p73241734105212"><a name="p73241734105212"></a><a name="p73241734105212"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.239999999999995%" headers="mcps1.2.5.1.4 "><p id="p12325143410525"><a name="p12325143410525"></a><a name="p12325143410525"></a>enum类型参数名称。例如typeNameCount为2，则参数包含typeName1:science，typeName2:literature。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 响应<a name="section31024304195415"></a>

-   要素说明

    **表 4**  要素说明

    <a name="table415208195710"></a>
    <table><thead align="left"><tr id="row62827717195710"><th class="cellrowborder" valign="top" width="13.66%" id="mcps1.2.5.1.1"><p id="p5798135195724"><a name="p5798135195724"></a><a name="p5798135195724"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="9.969999999999999%" id="mcps1.2.5.1.2"><p id="p66995796195724"><a name="p66995796195724"></a><a name="p66995796195724"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="8.63%" id="mcps1.2.5.1.3"><p id="p57950414195724"><a name="p57950414195724"></a><a name="p57950414195724"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="67.74%" id="mcps1.2.5.1.4"><p id="p63471948195724"><a name="p63471948195724"></a><a name="p63471948195724"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row66822716195710"><td class="cellrowborder" valign="top" width="13.66%" headers="mcps1.2.5.1.1 "><p id="p28953206195724"><a name="p28953206195724"></a><a name="p28953206195724"></a>errorMessage</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.969999999999999%" headers="mcps1.2.5.1.2 "><p id="p63508338195724"><a name="p63508338195724"></a><a name="p63508338195724"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.63%" headers="mcps1.2.5.1.3 "><p id="p43901714195724"><a name="p43901714195724"></a><a name="p43901714195724"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="67.74%" headers="mcps1.2.5.1.4 "><p id="p66377918195724"><a name="p66377918195724"></a><a name="p66377918195724"></a>系统提示信息，执行成功时，字段可能为空。执行失败时，用于显示错误信息。</p>
    </td>
    </tr>
    <tr id="row41832689195710"><td class="cellrowborder" valign="top" width="13.66%" headers="mcps1.2.5.1.1 "><p id="p4011871195724"><a name="p4011871195724"></a><a name="p4011871195724"></a>errorCode</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.969999999999999%" headers="mcps1.2.5.1.2 "><p id="p56526154195724"><a name="p56526154195724"></a><a name="p56526154195724"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.63%" headers="mcps1.2.5.1.3 "><p id="p15215774195724"><a name="p15215774195724"></a><a name="p15215774195724"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="67.74%" headers="mcps1.2.5.1.4 "><p id="p24518145195724"><a name="p24518145195724"></a><a name="p24518145195724"></a>系统提示信息，执行成功时，字段可能为空。执行失败时，用于显示错误码。</p>
    </td>
    </tr>
    <tr id="row65130104195710"><td class="cellrowborder" valign="top" width="13.66%" headers="mcps1.2.5.1.1 "><p id="p22770577195724"><a name="p22770577195724"></a><a name="p22770577195724"></a>result</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.969999999999999%" headers="mcps1.2.5.1.2 "><p id="p32477429195724"><a name="p32477429195724"></a><a name="p32477429195724"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="8.63%" headers="mcps1.2.5.1.3 "><p id="p13426086195724"><a name="p13426086195724"></a><a name="p13426086195724"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="67.74%" headers="mcps1.2.5.1.4 "><p id="p13771147195724"><a name="p13771147195724"></a><a name="p13771147195724"></a>成功时result值为success。</p>
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



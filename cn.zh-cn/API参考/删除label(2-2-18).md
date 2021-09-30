# 删除label\(2.2.18\)<a name="ges_03_0218"></a>

## 功能介绍<a name="section11798179195415"></a>

删除label，同时删除该label相关的点、边。

## URI<a name="section10938344195415"></a>

-   URI格式

    ```
    DELETE /ges/v1.0/{project_id}/graphs/{graph_name}/schema/labels/{labelName}
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
    <tr id="row159657353247"><td class="cellrowborder" valign="top" width="15.36%" headers="mcps1.2.5.1.1 "><p id="p1959410429245"><a name="p1959410429245"></a><a name="p1959410429245"></a>label_name</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.469999999999999%" headers="mcps1.2.5.1.2 "><p id="p859404212419"><a name="p859404212419"></a><a name="p859404212419"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.07%" headers="mcps1.2.5.1.3 "><p id="p559419424244"><a name="p559419424244"></a><a name="p559419424244"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="53.1%" headers="mcps1.2.5.1.4 "><p id="p959434218244"><a name="p959434218244"></a><a name="p959434218244"></a>label名称。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求<a name="section1235739195415"></a>

-   请求样例

    ```
    DELETE http://{SERVER_URL}/ges/v1.0/{project_id}/graphs/{graph_name}/schema/labels/{labelName}
    ```

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >SERVER\_URL：图的访问地址，取值请参考[业务面API使用限制](业务面API使用限制.md)。


## 响应<a name="section31024304195415"></a>

-   要素说明

    **表 2**  要素说明

    <a name="table415208195710"></a>
    <table><thead align="left"><tr id="row62827717195710"><th class="cellrowborder" valign="top" width="18.26%" id="mcps1.2.5.1.1"><p id="p5798135195724"><a name="p5798135195724"></a><a name="p5798135195724"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="11.700000000000001%" id="mcps1.2.5.1.2"><p id="p66995796195724"><a name="p66995796195724"></a><a name="p66995796195724"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="9.59%" id="mcps1.2.5.1.3"><p id="p57950414195724"><a name="p57950414195724"></a><a name="p57950414195724"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="60.45%" id="mcps1.2.5.1.4"><p id="p63471948195724"><a name="p63471948195724"></a><a name="p63471948195724"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row66822716195710"><td class="cellrowborder" valign="top" width="18.26%" headers="mcps1.2.5.1.1 "><p id="p28953206195724"><a name="p28953206195724"></a><a name="p28953206195724"></a>errorMessage</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.700000000000001%" headers="mcps1.2.5.1.2 "><p id="p63508338195724"><a name="p63508338195724"></a><a name="p63508338195724"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.59%" headers="mcps1.2.5.1.3 "><p id="p43901714195724"><a name="p43901714195724"></a><a name="p43901714195724"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60.45%" headers="mcps1.2.5.1.4 "><p id="p66377918195724"><a name="p66377918195724"></a><a name="p66377918195724"></a>系统提示信息，执行成功时，字段可能为空。执行失败时，用于显示错误信息。</p>
    </td>
    </tr>
    <tr id="row41832689195710"><td class="cellrowborder" valign="top" width="18.26%" headers="mcps1.2.5.1.1 "><p id="p4011871195724"><a name="p4011871195724"></a><a name="p4011871195724"></a>errorCode</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.700000000000001%" headers="mcps1.2.5.1.2 "><p id="p56526154195724"><a name="p56526154195724"></a><a name="p56526154195724"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.59%" headers="mcps1.2.5.1.3 "><p id="p15215774195724"><a name="p15215774195724"></a><a name="p15215774195724"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="60.45%" headers="mcps1.2.5.1.4 "><p id="p24518145195724"><a name="p24518145195724"></a><a name="p24518145195724"></a>系统提示信息，执行成功时，字段可能为空。执行失败时，用于显示错误码。</p>
    </td>
    </tr>
    <tr id="row65130104195710"><td class="cellrowborder" valign="top" width="18.26%" headers="mcps1.2.5.1.1 "><p id="p145242053182611"><a name="p145242053182611"></a><a name="p145242053182611"></a>data</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.700000000000001%" headers="mcps1.2.5.1.2 "><p id="p125241353152616"><a name="p125241353152616"></a><a name="p125241353152616"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="9.59%" headers="mcps1.2.5.1.3 "><p id="p952435317268"><a name="p952435317268"></a><a name="p952435317268"></a>Json</p>
    </td>
    <td class="cellrowborder" valign="top" width="60.45%" headers="mcps1.2.5.1.4 "><p id="p0524205332617"><a name="p0524205332617"></a><a name="p0524205332617"></a>查询结果。请求失败时字段为空。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 3**  data参数说明

    <a name="table1641211119275"></a>
    <table><thead align="left"><tr id="row164131611112710"><th class="cellrowborder" valign="top" width="18.421842184218423%" id="mcps1.2.4.1.1"><p id="p134162192718"><a name="p134162192718"></a><a name="p134162192718"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="16.861686168616863%" id="mcps1.2.4.1.2"><p id="p54192142710"><a name="p54192142710"></a><a name="p54192142710"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="64.71647164716472%" id="mcps1.2.4.1.3"><p id="p84122115278"><a name="p84122115278"></a><a name="p84122115278"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1141351182719"><td class="cellrowborder" valign="top" width="18.421842184218423%" headers="mcps1.2.4.1.1 "><p id="p1741192162718"><a name="p1741192162718"></a><a name="p1741192162718"></a>outputs</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.861686168616863%" headers="mcps1.2.4.1.2 "><p id="p104122112277"><a name="p104122112277"></a><a name="p104122112277"></a>int</p>
    </td>
    <td class="cellrowborder" valign="top" width="64.71647164716472%" headers="mcps1.2.4.1.3 "><p id="p541102162714"><a name="p541102162714"></a><a name="p541102162714"></a>删除label时，被删除的相关点/边数量。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   请求成功样例

    ```
    Http Status Code: 200
    {
        "data": {
            "outputs": 3
        },
        "status": "success"
    }
    
    ```

-   请求失败样例

    ```
    Http Status Code: 400
    {
      "errorMessage": "graph [demo] is not found",
      "errorCode": "GES.8003"
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



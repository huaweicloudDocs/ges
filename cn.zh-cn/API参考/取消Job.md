# 取消Job<a name="ges_03_0038"></a>

## 功能介绍<a name="section57431131202011"></a>

用于取消已经提交的作业。

对点过滤查询、边过滤查询、执行算法和增加索引4种类型的异步API返回的jobId，支持取消。若作业已经执行结束或失败则无法取消。

>![](public_sys-resources/icon-note.gif) **说明：**   
>只有点过滤查询、边过滤查询、执行算法、增加索引返回的Job支持取消。其他类型的会报“Unsupported Operation”异常。  

## URI<a name="section56494056202011"></a>

-   URI 格式

    ```
    DELETE /ges/v1.0/{projectId}/graphs/{graphName}/jobs/{jobId}
    ```

-   参数说明

    **表 1**  URI参数说明

    <a name="table66283993202424"></a>
    <table><thead align="left"><tr id="row59205483202424"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p59805966202438"><a name="p59805966202438"></a><a name="p59805966202438"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="p12445038202438"><a name="p12445038202438"></a><a name="p12445038202438"></a>是否为必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.3"><p id="p1415130202438"><a name="p1415130202438"></a><a name="p1415130202438"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="p47516731202438"><a name="p47516731202438"></a><a name="p47516731202438"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row20271122202424"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p36605179202438"><a name="p36605179202438"></a><a name="p36605179202438"></a>projectId</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p12229546202438"><a name="p12229546202438"></a><a name="p12229546202438"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p51069165202438"><a name="p51069165202438"></a><a name="p51069165202438"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p42961709202438"><a name="p42961709202438"></a><a name="p42961709202438"></a>服务所在域ID。</p>
    </td>
    </tr>
    <tr id="row11419839202424"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p46355420202438"><a name="p46355420202438"></a><a name="p46355420202438"></a>jobId</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p63801554202438"><a name="p63801554202438"></a><a name="p63801554202438"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p543392202438"><a name="p543392202438"></a><a name="p543392202438"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p44014831202438"><a name="p44014831202438"></a><a name="p44014831202438"></a>Job ID。</p>
    </td>
    </tr>
    <tr id="row33038495115"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p204402484117"><a name="p204402484117"></a><a name="p204402484117"></a>graphName</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p16442124819110"><a name="p16442124819110"></a><a name="p16442124819110"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p1644484812118"><a name="p1644484812118"></a><a name="p1644484812118"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p1444614482118"><a name="p1444614482118"></a><a name="p1444614482118"></a>图名称。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求<a name="section62446078202011"></a>

-   请求样例

    ```
    DELETE http://Endpoint/ges/v1.0/{projectId}/graphs/{graphName}/jobs/{jobId}
    ```


## 响应<a name="section14834278202011"></a>

-   要素说明

    **表 2**  要素说明

    <a name="table9618153202456"></a>
    <table><thead align="left"><tr id="row19256001202456"><th class="cellrowborder" valign="top" width="18.61%" id="mcps1.2.5.1.1"><p id="p4115707020258"><a name="p4115707020258"></a><a name="p4115707020258"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="23.119999999999997%" id="mcps1.2.5.1.2"><p id="p4538840820258"><a name="p4538840820258"></a><a name="p4538840820258"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="22.18%" id="mcps1.2.5.1.3"><p id="p5258245920258"><a name="p5258245920258"></a><a name="p5258245920258"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="36.09%" id="mcps1.2.5.1.4"><p id="p3132076620258"><a name="p3132076620258"></a><a name="p3132076620258"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row65005079202456"><td class="cellrowborder" valign="top" width="18.61%" headers="mcps1.2.5.1.1 "><p id="p820509320258"><a name="p820509320258"></a><a name="p820509320258"></a>errorMessage</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.119999999999997%" headers="mcps1.2.5.1.2 "><p id="p6063279320258"><a name="p6063279320258"></a><a name="p6063279320258"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.18%" headers="mcps1.2.5.1.3 "><p id="p1230923020258"><a name="p1230923020258"></a><a name="p1230923020258"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.09%" headers="mcps1.2.5.1.4 "><p id="p5752359620258"><a name="p5752359620258"></a><a name="p5752359620258"></a>系统提示信息，执行成功时，字段可能为空。执行失败时，用于显示错误信息。</p>
    </td>
    </tr>
    <tr id="row12849645202456"><td class="cellrowborder" valign="top" width="18.61%" headers="mcps1.2.5.1.1 "><p id="p5877047420258"><a name="p5877047420258"></a><a name="p5877047420258"></a>errorCode</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.119999999999997%" headers="mcps1.2.5.1.2 "><p id="p6278797220258"><a name="p6278797220258"></a><a name="p6278797220258"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.18%" headers="mcps1.2.5.1.3 "><p id="p5266096220258"><a name="p5266096220258"></a><a name="p5266096220258"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="36.09%" headers="mcps1.2.5.1.4 "><p id="p3767953320258"><a name="p3767953320258"></a><a name="p3767953320258"></a>系统提示信息，执行成功时，字段可能为空。执行失败时，用于显示错误码。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   请求成功样例

    ```
    Http Status Code: 200
    {}
    ```

-   请求失败样例

    ```
    Http Status Code: 400
    {
     
    "errorMessage": "can not find job to cancel, id is 9440a7ebXXXXXXXXXXXXXXXXXXXX2d079a67001679122",
     
    "errorCode": "GES.8303"
    }
    ```


## 返回值<a name="section3824743202011"></a>

-   正常

    200

-   异常

    **表 3**  异常返回值说明

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



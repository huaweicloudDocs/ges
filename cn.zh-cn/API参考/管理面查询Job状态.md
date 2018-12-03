# 管理面查询Job状态<a name="ges_03_0061"></a>

## 功能介绍<a name="section191474019367"></a>

查询Job的执行状态。对创建图、关闭图、启动图、删除图、新增备份等异步API命令下发后，会返回jobId，通过jobId查询任务的执行状态。

## URI<a name="section09144402366"></a>

-   URI 格式

    ```
    GET /v1.0/{projectId}/graphs/{graphId}/jobs/{jobId}/status
    ```

-   参数说明

    **表 1**  URI参数说明

    <a name="table242717161697"></a>
    <table><thead align="left"><tr id="row356893751697"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p3108920316930"><a name="p3108920316930"></a><a name="p3108920316930"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.2"><p id="p3519750416930"><a name="p3519750416930"></a><a name="p3519750416930"></a>是否为必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.3"><p id="p3242555716930"><a name="p3242555716930"></a><a name="p3242555716930"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.4"><p id="p922447516930"><a name="p922447516930"></a><a name="p922447516930"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row476603911697"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p5669781616930"><a name="p5669781616930"></a><a name="p5669781616930"></a>projectId</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p2912041616930"><a name="p2912041616930"></a><a name="p2912041616930"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p994348016930"><a name="p994348016930"></a><a name="p994348016930"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p11552816930"><a name="p11552816930"></a><a name="p11552816930"></a>服务所在域ID。</p>
    </td>
    </tr>
    <tr id="row638333811697"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p1711149316930"><a name="p1711149316930"></a><a name="p1711149316930"></a>graphId</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p4385370616930"><a name="p4385370616930"></a><a name="p4385370616930"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p6248928316930"><a name="p6248928316930"></a><a name="p6248928316930"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p2846716116930"><a name="p2846716116930"></a><a name="p2846716116930"></a>图ID。</p>
    </td>
    </tr>
    <tr id="row589729071697"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p1592148516930"><a name="p1592148516930"></a><a name="p1592148516930"></a>jobId</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.2 "><p id="p1457191316930"><a name="p1457191316930"></a><a name="p1457191316930"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.3 "><p id="p3947430116930"><a name="p3947430116930"></a><a name="p3947430116930"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.4 "><p id="p4330184216930"><a name="p4330184216930"></a><a name="p4330184216930"></a>Job ID。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求<a name="section19471640133612"></a>

-   请求样例

    ```
    GET    https://Endpoint/v1.0/{projectId}/graphs/{graphId}/jobs/{jobId}/status
    ```


## 响应<a name="section12947114083614"></a>

-   要素说明

    **表 2**  要素说明

    <a name="table9398030161013"></a>
    <table><thead align="left"><tr id="row26921206161013"><th class="cellrowborder" valign="top" width="22.93%" id="mcps1.2.5.1.1"><p id="p16015104161025"><a name="p16015104161025"></a><a name="p16015104161025"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="20.3%" id="mcps1.2.5.1.2"><p id="p22155036161025"><a name="p22155036161025"></a><a name="p22155036161025"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="22.37%" id="mcps1.2.5.1.3"><p id="p49727452161025"><a name="p49727452161025"></a><a name="p49727452161025"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="34.4%" id="mcps1.2.5.1.4"><p id="p1391784161025"><a name="p1391784161025"></a><a name="p1391784161025"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row49281025161013"><td class="cellrowborder" valign="top" width="22.93%" headers="mcps1.2.5.1.1 "><p id="p4694663161025"><a name="p4694663161025"></a><a name="p4694663161025"></a>errorMessage</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.3%" headers="mcps1.2.5.1.2 "><p id="p44723433161025"><a name="p44723433161025"></a><a name="p44723433161025"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.37%" headers="mcps1.2.5.1.3 "><p id="p65828344161025"><a name="p65828344161025"></a><a name="p65828344161025"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="34.4%" headers="mcps1.2.5.1.4 "><p id="p30495643161025"><a name="p30495643161025"></a><a name="p30495643161025"></a>系统提示信息，执行成功时，字段可能为空。执行失败时，用于显示错误信息。</p>
    </td>
    </tr>
    <tr id="row53676720161013"><td class="cellrowborder" valign="top" width="22.93%" headers="mcps1.2.5.1.1 "><p id="p18290197161025"><a name="p18290197161025"></a><a name="p18290197161025"></a>errorCode</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.3%" headers="mcps1.2.5.1.2 "><p id="p5110970161025"><a name="p5110970161025"></a><a name="p5110970161025"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.37%" headers="mcps1.2.5.1.3 "><p id="p11335440161025"><a name="p11335440161025"></a><a name="p11335440161025"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="34.4%" headers="mcps1.2.5.1.4 "><p id="p45755454161025"><a name="p45755454161025"></a><a name="p45755454161025"></a>系统提示信息，执行成功时，字段可能为空。执行失败时，用于显示错误码。</p>
    </td>
    </tr>
    <tr id="row61256280161013"><td class="cellrowborder" valign="top" width="22.93%" headers="mcps1.2.5.1.1 "><p id="p2621277161025"><a name="p2621277161025"></a><a name="p2621277161025"></a>status</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.3%" headers="mcps1.2.5.1.2 "><p id="p10996847161025"><a name="p10996847161025"></a><a name="p10996847161025"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.37%" headers="mcps1.2.5.1.3 "><p id="p18329430161025"><a name="p18329430161025"></a><a name="p18329430161025"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="34.4%" headers="mcps1.2.5.1.4 "><p id="p8288890161025"><a name="p8288890161025"></a><a name="p8288890161025"></a>查询成功时返回任务状态，可选值有waiting、running和success。查询失败时字段为空。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   请求成功样例

    ```
    Http Status Code: 200
    {
    "status":"success"
    }
    ```

-   请求失败样例

    ```
    Http Status Code: 400
    {
    "errorMessage": "can not find job, jobId is ff808081646e81d40164c5fb414b2b1a1",
    "errorCode": "GES.8301"
    }
    ```


## 返回值<a name="section58124123616"></a>

-   正常

    200

-   异常

    **表 3**  异常返回值说明

    <a name="table62805478161143"></a>
    <table><thead align="left"><tr id="row7600041161143"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p33199408161211"><a name="p33199408161211"></a><a name="p33199408161211"></a>返回值</p>
    </th>
    <th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p4797519161211"><a name="p4797519161211"></a><a name="p4797519161211"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row26509924161143"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p2470184161211"><a name="p2470184161211"></a><a name="p2470184161211"></a>400 Bad Request</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p65867185161211"><a name="p65867185161211"></a><a name="p65867185161211"></a>请求错误。</p>
    </td>
    </tr>
    <tr id="row3149953161143"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p34340117161211"><a name="p34340117161211"></a><a name="p34340117161211"></a>401 Unauthorized</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p30086118161211"><a name="p30086118161211"></a><a name="p30086118161211"></a>鉴权失败。</p>
    </td>
    </tr>
    <tr id="row42956032161143"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p55291065161211"><a name="p55291065161211"></a><a name="p55291065161211"></a>403 Forbidden</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p49391293161211"><a name="p49391293161211"></a><a name="p49391293161211"></a>没有操作权限。</p>
    </td>
    </tr>
    <tr id="row64135773161143"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p35901528161211"><a name="p35901528161211"></a><a name="p35901528161211"></a>404 Not Found</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p22342664161211"><a name="p22342664161211"></a><a name="p22342664161211"></a>找不到资源。</p>
    </td>
    </tr>
    <tr id="row65862429161143"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p47457151161211"><a name="p47457151161211"></a><a name="p47457151161211"></a>500 Internal Server Error</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p18824037161211"><a name="p18824037161211"></a><a name="p18824037161211"></a>服务内部错误。</p>
    </td>
    </tr>
    <tr id="row17696525161143"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p32515139161211"><a name="p32515139161211"></a><a name="p32515139161211"></a>503 Service Unavailable</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p16480634161211"><a name="p16480634161211"></a><a name="p16480634161211"></a>服务不可用。</p>
    </td>
    </tr>
    </tbody>
    </table>



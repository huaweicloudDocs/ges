# Cypher操作API（2.2.16公测）<a name="ges_03_0212"></a>

## 功能介绍<a name="section11581657646"></a>

Cypher是一种被广泛使用的声明式图数据库查询语言，使用Cypher语句可以查询GES中的数据，并返回结果。当前的Cypher实现中使用了图的统计信息，目前Cypher查询编译过程中使用了基于label的点边索引，如需正常使用Cypher，请先参考[Cypher预置条件](#section96831823102810)构建索引。

## URL<a name="section1688218509514"></a>

-   URI 格式

    ```
    POST /ges/v1.0/{project_id}/graphs/{graph_name}/action?action_id=execute-cypher-query
    ```

-   参数说明

    **表 1**  URI参数说明

    <a name="table1810588194531"></a>
    <table><thead align="left"><tr id="row60039522194531"><th class="cellrowborder" valign="top" width="16.24%" id="mcps1.2.5.1.1"><p id="p17147315194548"><a name="p17147315194548"></a><a name="p17147315194548"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="13.139999999999999%" id="mcps1.2.5.1.2"><p id="p46755299194548"><a name="p46755299194548"></a><a name="p46755299194548"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.6%" id="mcps1.2.5.1.3"><p id="p29082892194548"><a name="p29082892194548"></a><a name="p29082892194548"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="52.019999999999996%" id="mcps1.2.5.1.4"><p id="p6904021194548"><a name="p6904021194548"></a><a name="p6904021194548"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row43054002194531"><td class="cellrowborder" valign="top" width="16.24%" headers="mcps1.2.5.1.1 "><p id="p65907560194548"><a name="p65907560194548"></a><a name="p65907560194548"></a>project_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.139999999999999%" headers="mcps1.2.5.1.2 "><p id="p36912130194548"><a name="p36912130194548"></a><a name="p36912130194548"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.6%" headers="mcps1.2.5.1.3 "><p id="p37092573194548"><a name="p37092573194548"></a><a name="p37092573194548"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.019999999999996%" headers="mcps1.2.5.1.4 "><p id="p18457547124515"><a name="p18457547124515"></a><a name="p18457547124515"></a>项目编号，用于资源隔离。</p>
    </td>
    </tr>
    <tr id="row13142191315810"><td class="cellrowborder" valign="top" width="16.24%" headers="mcps1.2.5.1.1 "><p id="p1691521120589"><a name="p1691521120589"></a><a name="p1691521120589"></a>graph_name</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.139999999999999%" headers="mcps1.2.5.1.2 "><p id="p791761175818"><a name="p791761175818"></a><a name="p791761175818"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.6%" headers="mcps1.2.5.1.3 "><p id="p492031115815"><a name="p492031115815"></a><a name="p492031115815"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="52.019999999999996%" headers="mcps1.2.5.1.4 "><p id="p145715471455"><a name="p145715471455"></a><a name="p145715471455"></a>图名称。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求<a name="section024212129238"></a>

-   请求样例

```
POST http://{SERVER_URL}/ges/v1.0/{project_id}/graphs/{graph_name}/action?action_id=execute-cypher-query
{
       "statements": [{
              "statement": "match (n) return n limit 1",
              "parameters": {},
              "resultDataContents": ["row"],
              "includeStats": false
       }]
}

```

-   参数说明

    **表 2**  Body参数说明

    <a name="table15122952104720"></a>
    <table><thead align="left"><tr id="row1411885215473"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p1118185244718"><a name="p1118185244718"></a><a name="p1118185244718"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.36%" id="mcps1.2.5.1.2"><p id="p1311825210479"><a name="p1311825210479"></a><a name="p1311825210479"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="15.27%" id="mcps1.2.5.1.3"><p id="p131181152144717"><a name="p131181152144717"></a><a name="p131181152144717"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="47.370000000000005%" id="mcps1.2.5.1.4"><p id="p11181052124718"><a name="p11181052124718"></a><a name="p11181052124718"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row111184522471"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p58331712490"><a name="p58331712490"></a><a name="p58331712490"></a>statements</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.36%" headers="mcps1.2.5.1.2 "><p id="p158331113492"><a name="p158331113492"></a><a name="p158331113492"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="15.27%" headers="mcps1.2.5.1.3 "><p id="p783341204917"><a name="p783341204917"></a><a name="p783341204917"></a>List</p>
    </td>
    <td class="cellrowborder" valign="top" width="47.370000000000005%" headers="mcps1.2.5.1.4 "><p id="p128341316492"><a name="p128341316492"></a><a name="p128341316492"></a>statements为一个语句组，包含一到多条语句。其中每个元素的格式如<a href="#table201251452114711">表 statement参数说明</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 3**  statement参数说明

    <a name="table201251452114711"></a>
    <table><thead align="left"><tr id="row15123175211475"><th class="cellrowborder" valign="top" width="25.09%" id="mcps1.2.5.1.1"><p id="p712245274719"><a name="p712245274719"></a><a name="p712245274719"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.45%" id="mcps1.2.5.1.2"><p id="p12122552184712"><a name="p12122552184712"></a><a name="p12122552184712"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="13.33%" id="mcps1.2.5.1.3"><p id="p8122195217477"><a name="p8122195217477"></a><a name="p8122195217477"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="49.13%" id="mcps1.2.5.1.4"><p id="p2123152194714"><a name="p2123152194714"></a><a name="p2123152194714"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row0123205220479"><td class="cellrowborder" valign="top" width="25.09%" headers="mcps1.2.5.1.1 "><p id="p1926816422511"><a name="p1926816422511"></a><a name="p1926816422511"></a>statement</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.45%" headers="mcps1.2.5.1.2 "><p id="p1426816422515"><a name="p1426816422515"></a><a name="p1426816422515"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.33%" headers="mcps1.2.5.1.3 "><p id="p6268204275113"><a name="p6268204275113"></a><a name="p6268204275113"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.13%" headers="mcps1.2.5.1.4 "><p id="p426824255117"><a name="p426824255117"></a><a name="p426824255117"></a>Cypher语句。</p>
    </td>
    </tr>
    <tr id="row15125352194713"><td class="cellrowborder" valign="top" width="25.09%" headers="mcps1.2.5.1.1 "><p id="p19268242175112"><a name="p19268242175112"></a><a name="p19268242175112"></a>parameters</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.45%" headers="mcps1.2.5.1.2 "><p id="p15268134235113"><a name="p15268134235113"></a><a name="p15268134235113"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.33%" headers="mcps1.2.5.1.3 "><p id="p5268942135117"><a name="p5268942135117"></a><a name="p5268942135117"></a>Json</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.13%" headers="mcps1.2.5.1.4 "><p id="p82687426515"><a name="p82687426515"></a><a name="p82687426515"></a>Cypher语句参数，在进行参数化查询时使用，默认为空。</p>
    <p id="p68732762013"><a name="p68732762013"></a><a name="p68732762013"></a>如需使用，请参考<a href="#section1885065125812">参数化查询</a>。</p>
    </td>
    </tr>
    <tr id="row101300225512"><td class="cellrowborder" valign="top" width="25.09%" headers="mcps1.2.5.1.1 "><p id="p72681442125113"><a name="p72681442125113"></a><a name="p72681442125113"></a>resultDataContents</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.45%" headers="mcps1.2.5.1.2 "><p id="p1826844245119"><a name="p1826844245119"></a><a name="p1826844245119"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.33%" headers="mcps1.2.5.1.3 "><p id="p4268114217515"><a name="p4268114217515"></a><a name="p4268114217515"></a>String或List</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.13%" headers="mcps1.2.5.1.4 "><p id="p526884214511"><a name="p526884214511"></a><a name="p526884214511"></a>返回的结果样式，可选参数有“row”,”graph”两种样式可选，一次可返回多个样式。</p>
    </td>
    </tr>
    <tr id="row1331572413911"><td class="cellrowborder" valign="top" width="25.09%" headers="mcps1.2.5.1.1 "><p id="p13551637997"><a name="p13551637997"></a><a name="p13551637997"></a>includeStats</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.45%" headers="mcps1.2.5.1.2 "><p id="p185513371198"><a name="p185513371198"></a><a name="p185513371198"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.33%" headers="mcps1.2.5.1.3 "><p id="p0552378918"><a name="p0552378918"></a><a name="p0552378918"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.13%" headers="mcps1.2.5.1.4 "><p id="p1755153711910"><a name="p1755153711910"></a><a name="p1755153711910"></a>控制返回结果是否携带增删改统计信息的开关，若不设置此字段，默认为不携带。</p>
    </td>
    </tr>
    <tr id="row161541253133211"><td class="cellrowborder" valign="top" width="25.09%" headers="mcps1.2.5.1.1 "><p id="p159832055163218"><a name="p159832055163218"></a><a name="p159832055163218"></a>executionMode（2.2.23）</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.45%" headers="mcps1.2.5.1.2 "><p id="p1983155563215"><a name="p1983155563215"></a><a name="p1983155563215"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.33%" headers="mcps1.2.5.1.3 "><p id="p198335519328"><a name="p198335519328"></a><a name="p198335519328"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.13%" headers="mcps1.2.5.1.4 "><p id="p159846554329"><a name="p159846554329"></a><a name="p159846554329"></a>执行模式。同步执行模式填写“sync”，异步执行填写“async”，不写默认同步执行。异步模式下，获取查询结果参见<a href="查询Job状态(1-0-0)-业务面.md">查询Job状态</a>。</p>
    </td>
    </tr>
    <tr id="row1466044813325"><td class="cellrowborder" valign="top" width="25.09%" headers="mcps1.2.5.1.1 "><p id="p16984195512328"><a name="p16984195512328"></a><a name="p16984195512328"></a>limit（2.2.23）</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.45%" headers="mcps1.2.5.1.2 "><p id="p19984115517321"><a name="p19984115517321"></a><a name="p19984115517321"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.33%" headers="mcps1.2.5.1.3 "><p id="p2098475543218"><a name="p2098475543218"></a><a name="p2098475543218"></a>Int</p>
    </td>
    <td class="cellrowborder" valign="top" width="49.13%" headers="mcps1.2.5.1.4 "><p id="p13984105543218"><a name="p13984105543218"></a><a name="p13984105543218"></a>该字段仅在异步模式下生效，表示对异步结果的最大结果数限制，默认值为100000。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 响应<a name="section19473183810432"></a>

-   要素说明

    **表 4**  要素说明

    <a name="table203335934319"></a>
    <table><thead align="left"><tr id="row173355919438"><th class="cellrowborder" valign="top" width="15.39%" id="mcps1.2.5.1.1"><p id="p1113351184419"><a name="p1113351184419"></a><a name="p1113351184419"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.24%" id="mcps1.2.5.1.2"><p id="p1513321118447"><a name="p1513321118447"></a><a name="p1513321118447"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="13.089999999999998%" id="mcps1.2.5.1.3"><p id="p1713331144415"><a name="p1713331144415"></a><a name="p1713331144415"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="59.28%" id="mcps1.2.5.1.4"><p id="p8134211204415"><a name="p8134211204415"></a><a name="p8134211204415"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row13336592434"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p104163220555"><a name="p104163220555"></a><a name="p104163220555"></a>results</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.24%" headers="mcps1.2.5.1.2 "><p id="p154123215553"><a name="p154123215553"></a><a name="p154123215553"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.089999999999998%" headers="mcps1.2.5.1.3 "><p id="p144163219555"><a name="p144163219555"></a><a name="p144163219555"></a>List</p>
    </td>
    <td class="cellrowborder" valign="top" width="59.28%" headers="mcps1.2.5.1.4 "><p id="p11473218557"><a name="p11473218557"></a><a name="p11473218557"></a>一个List，每个元素是一条Cypher语句的返回结果。</p>
    </td>
    </tr>
    <tr id="row19331259104319"><td class="cellrowborder" valign="top" width="15.39%" headers="mcps1.2.5.1.1 "><p id="p1941932185516"><a name="p1941932185516"></a><a name="p1941932185516"></a>errors</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.24%" headers="mcps1.2.5.1.2 "><p id="p64113215557"><a name="p64113215557"></a><a name="p64113215557"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.089999999999998%" headers="mcps1.2.5.1.3 "><p id="p648328550"><a name="p648328550"></a><a name="p648328550"></a>List</p>
    </td>
    <td class="cellrowborder" valign="top" width="59.28%" headers="mcps1.2.5.1.4 "><p id="p15410322559"><a name="p15410322559"></a><a name="p15410322559"></a>一个List，每个元素包含字符串形式的code和message信息。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 5**  参数results中各要素说明

    <a name="table19909163265613"></a>
    <table><thead align="left"><tr id="row29101132195616"><th class="cellrowborder" valign="top" width="15.15%" id="mcps1.2.5.1.1"><p id="p16761113955713"><a name="p16761113955713"></a><a name="p16761113955713"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.479999999999999%" id="mcps1.2.5.1.2"><p id="p1761239125710"><a name="p1761239125710"></a><a name="p1761239125710"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="13.58%" id="mcps1.2.5.1.3"><p id="p1776118397573"><a name="p1776118397573"></a><a name="p1776118397573"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="58.79%" id="mcps1.2.5.1.4"><p id="p17761163914572"><a name="p17761163914572"></a><a name="p17761163914572"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1791073214563"><td class="cellrowborder" valign="top" width="15.15%" headers="mcps1.2.5.1.1 "><p id="p17761123917573"><a name="p17761123917573"></a><a name="p17761123917573"></a>columns</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.479999999999999%" headers="mcps1.2.5.1.2 "><p id="p976133916574"><a name="p976133916574"></a><a name="p976133916574"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.58%" headers="mcps1.2.5.1.3 "><p id="p27611939165717"><a name="p27611939165717"></a><a name="p27611939165717"></a>List</p>
    </td>
    <td class="cellrowborder" valign="top" width="58.79%" headers="mcps1.2.5.1.4 "><p id="p16761183975714"><a name="p16761183975714"></a><a name="p16761183975714"></a>返回的字段名。</p>
    </td>
    </tr>
    <tr id="row1791019327563"><td class="cellrowborder" valign="top" width="15.15%" headers="mcps1.2.5.1.1 "><p id="p4761139105714"><a name="p4761139105714"></a><a name="p4761139105714"></a>data</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.479999999999999%" headers="mcps1.2.5.1.2 "><p id="p37615393575"><a name="p37615393575"></a><a name="p37615393575"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.58%" headers="mcps1.2.5.1.3 "><p id="p576103975712"><a name="p576103975712"></a><a name="p576103975712"></a>List</p>
    </td>
    <td class="cellrowborder" valign="top" width="58.79%" headers="mcps1.2.5.1.4 "><p id="p27611039195719"><a name="p27611039195719"></a><a name="p27611039195719"></a>返回的数据值，每个元素代表一条记录。</p>
    </td>
    </tr>
    <tr id="row153532031133719"><td class="cellrowborder" valign="top" width="15.15%" headers="mcps1.2.5.1.1 "><p id="p52601233103718"><a name="p52601233103718"></a><a name="p52601233103718"></a>stats</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.479999999999999%" headers="mcps1.2.5.1.2 "><p id="p172601433173715"><a name="p172601433173715"></a><a name="p172601433173715"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.58%" headers="mcps1.2.5.1.3 "><p id="p15260733183719"><a name="p15260733183719"></a><a name="p15260733183719"></a>Json</p>
    </td>
    <td class="cellrowborder" valign="top" width="58.79%" headers="mcps1.2.5.1.4 "><p id="p92601433183715"><a name="p92601433183715"></a><a name="p92601433183715"></a>返回的增删改统计信息</p>
    </td>
    </tr>
    <tr id="row27548271379"><td class="cellrowborder" valign="top" width="15.15%" headers="mcps1.2.5.1.1 "><p id="p2260153323717"><a name="p2260153323717"></a><a name="p2260153323717"></a>plan</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.479999999999999%" headers="mcps1.2.5.1.2 "><p id="p10261103353713"><a name="p10261103353713"></a><a name="p10261103353713"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="13.58%" headers="mcps1.2.5.1.3 "><p id="p1226183333711"><a name="p1226183333711"></a><a name="p1226183333711"></a>Json</p>
    </td>
    <td class="cellrowborder" valign="top" width="58.79%" headers="mcps1.2.5.1.4 "><p id="p426193319372"><a name="p426193319372"></a><a name="p426193319372"></a>如果cypher语句带explain前缀，则此字段输出查询计划，否则不显示该字段，正常执行查询。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 6**  参数data中各要素说明：

    <a name="table10759475586"></a>
    <table><thead align="left"><tr id="row07590765812"><th class="cellrowborder" valign="top" width="15.15%" id="mcps1.2.5.1.1"><p id="p3112733145811"><a name="p3112733145811"></a><a name="p3112733145811"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="12.61%" id="mcps1.2.5.1.2"><p id="p9112533125815"><a name="p9112533125815"></a><a name="p9112533125815"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="14.06%" id="mcps1.2.5.1.3"><p id="p41121033175814"><a name="p41121033175814"></a><a name="p41121033175814"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="58.18%" id="mcps1.2.5.1.4"><p id="p1112163375815"><a name="p1112163375815"></a><a name="p1112163375815"></a>含义</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row167609715814"><td class="cellrowborder" valign="top" width="15.15%" headers="mcps1.2.5.1.1 "><p id="p1811203355819"><a name="p1811203355819"></a><a name="p1811203355819"></a>row</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.61%" headers="mcps1.2.5.1.2 "><p id="p4112193316581"><a name="p4112193316581"></a><a name="p4112193316581"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.06%" headers="mcps1.2.5.1.3 "><p id="p1711211336584"><a name="p1711211336584"></a><a name="p1711211336584"></a>List</p>
    </td>
    <td class="cellrowborder" valign="top" width="58.18%" headers="mcps1.2.5.1.4 "><p id="p61131733195818"><a name="p61131733195818"></a><a name="p61131733195818"></a>表示具体一行的内容，每个元素对应该行的一个字段，仅当resultDataContents为空或者包含“row”类型时显示。</p>
    </td>
    </tr>
    <tr id="row576011745813"><td class="cellrowborder" valign="top" width="15.15%" headers="mcps1.2.5.1.1 "><p id="p1911373395814"><a name="p1911373395814"></a><a name="p1911373395814"></a>meta</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.61%" headers="mcps1.2.5.1.2 "><p id="p21131133135813"><a name="p21131133135813"></a><a name="p21131133135813"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.06%" headers="mcps1.2.5.1.3 "><p id="p1611353395815"><a name="p1611353395815"></a><a name="p1611353395815"></a>List</p>
    </td>
    <td class="cellrowborder" valign="top" width="58.18%" headers="mcps1.2.5.1.4 "><p id="p111131133175813"><a name="p111131133175813"></a><a name="p111131133175813"></a>表示该行每个字段的类型信息，仅当resultDataContents为空或者包含“row”类型时显示。</p>
    </td>
    </tr>
    <tr id="row9449831115819"><td class="cellrowborder" valign="top" width="15.15%" headers="mcps1.2.5.1.1 "><p id="p411313315811"><a name="p411313315811"></a><a name="p411313315811"></a>graph</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.61%" headers="mcps1.2.5.1.2 "><p id="p4113433155811"><a name="p4113433155811"></a><a name="p4113433155811"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.06%" headers="mcps1.2.5.1.3 "><p id="p41131333185810"><a name="p41131333185810"></a><a name="p41131333185810"></a>Json</p>
    </td>
    <td class="cellrowborder" valign="top" width="58.18%" headers="mcps1.2.5.1.4 "><p id="p211343310587"><a name="p211343310587"></a><a name="p211343310587"></a>以“graph”样式返回该行信息，仅当resultDataContents包含“graph”类型时显示。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   请求成功样例

    ```
    Http Status Code: 200
    {
        "results": [
            {
                "columns": ["n"],
                "data": [
                    {
                        "row": [
                            {
                                "occupation": "artist",
                                "gender": "F",
                                "Zip-code": "98133",
                                "userid": 0,
                                "age": "25-34"
                            }
                        ],
                        "meta": [
                            {
                                "id": "46",
                                "type": "node",
                                "labels": [
                                    "user"
                                ]
                            }
                        ]
                    }
                ]，
                "stats": {
                    "contains_updates": false,
                    "edges_created": 0,
                    "edges_deleted": 0,
                    "labels_set": 0,
                    "properties_set": 0,
                    "vertices_created": 0,
                    "vertices_deleted": 0
                 }
            
             }
        ],
        "errors": []
    }
    
    ```

    **表 7**  stats各要素响应参数：

    <a name="table1890017131137"></a>
    <table><thead align="left"><tr id="row690151321318"><th class="cellrowborder" valign="top" width="25%" id="mcps1.2.5.1.1"><p id="p12635164615138"><a name="p12635164615138"></a><a name="p12635164615138"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.42%" id="mcps1.2.5.1.2"><p id="p17636204616132"><a name="p17636204616132"></a><a name="p17636204616132"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="19.16%" id="mcps1.2.5.1.3"><p id="p963610466132"><a name="p963610466132"></a><a name="p963610466132"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="37.419999999999995%" id="mcps1.2.5.1.4"><p id="p1963664610135"><a name="p1963664610135"></a><a name="p1963664610135"></a>含义</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row89025130137"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p66361846131318"><a name="p66361846131318"></a><a name="p66361846131318"></a>contains_updates</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.42%" headers="mcps1.2.5.1.2 "><p id="p66361946141313"><a name="p66361946141313"></a><a name="p66361946141313"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.16%" headers="mcps1.2.5.1.3 "><p id="p1863615468139"><a name="p1863615468139"></a><a name="p1863615468139"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="37.419999999999995%" headers="mcps1.2.5.1.4 "><p id="p126362461133"><a name="p126362461133"></a><a name="p126362461133"></a>表示本次查询是否有数据修改</p>
    </td>
    </tr>
    <tr id="row139021133138"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p126361946191313"><a name="p126361946191313"></a><a name="p126361946191313"></a>edges_created</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.42%" headers="mcps1.2.5.1.2 "><p id="p763613465138"><a name="p763613465138"></a><a name="p763613465138"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.16%" headers="mcps1.2.5.1.3 "><p id="p8636134618135"><a name="p8636134618135"></a><a name="p8636134618135"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="37.419999999999995%" headers="mcps1.2.5.1.4 "><p id="p463615463139"><a name="p463615463139"></a><a name="p463615463139"></a>创建的边数目</p>
    </td>
    </tr>
    <tr id="row3902151319133"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p1563611465137"><a name="p1563611465137"></a><a name="p1563611465137"></a>edges_deleted</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.42%" headers="mcps1.2.5.1.2 "><p id="p763611469132"><a name="p763611469132"></a><a name="p763611469132"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.16%" headers="mcps1.2.5.1.3 "><p id="p76361346171310"><a name="p76361346171310"></a><a name="p76361346171310"></a>Int</p>
    </td>
    <td class="cellrowborder" valign="top" width="37.419999999999995%" headers="mcps1.2.5.1.4 "><p id="p1636124613136"><a name="p1636124613136"></a><a name="p1636124613136"></a>删除的边数目</p>
    </td>
    </tr>
    <tr id="row590291319131"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p563614468139"><a name="p563614468139"></a><a name="p563614468139"></a>labels_set</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.42%" headers="mcps1.2.5.1.2 "><p id="p16636104610137"><a name="p16636104610137"></a><a name="p16636104610137"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.16%" headers="mcps1.2.5.1.3 "><p id="p20636346101317"><a name="p20636346101317"></a><a name="p20636346101317"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="37.419999999999995%" headers="mcps1.2.5.1.4 "><p id="p1163614611137"><a name="p1163614611137"></a><a name="p1163614611137"></a>设置的label数目</p>
    </td>
    </tr>
    <tr id="row4902131321311"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p1636194671310"><a name="p1636194671310"></a><a name="p1636194671310"></a>properties_set</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.42%" headers="mcps1.2.5.1.2 "><p id="p1863644617131"><a name="p1863644617131"></a><a name="p1863644617131"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.16%" headers="mcps1.2.5.1.3 "><p id="p1637154615133"><a name="p1637154615133"></a><a name="p1637154615133"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="37.419999999999995%" headers="mcps1.2.5.1.4 "><p id="p1563704681316"><a name="p1563704681316"></a><a name="p1563704681316"></a>设置的属性数目</p>
    </td>
    </tr>
    <tr id="row199036137131"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p1963734661320"><a name="p1963734661320"></a><a name="p1963734661320"></a>vertices_created</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.42%" headers="mcps1.2.5.1.2 "><p id="p7637194618138"><a name="p7637194618138"></a><a name="p7637194618138"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.16%" headers="mcps1.2.5.1.3 "><p id="p19637124691319"><a name="p19637124691319"></a><a name="p19637124691319"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="37.419999999999995%" headers="mcps1.2.5.1.4 "><p id="p1063724620133"><a name="p1063724620133"></a><a name="p1063724620133"></a>创建的点数目</p>
    </td>
    </tr>
    <tr id="row1090391313133"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.5.1.1 "><p id="p1263716462133"><a name="p1263716462133"></a><a name="p1263716462133"></a>vertices_deleted</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.42%" headers="mcps1.2.5.1.2 "><p id="p106371146191314"><a name="p106371146191314"></a><a name="p106371146191314"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.16%" headers="mcps1.2.5.1.3 "><p id="p963724661312"><a name="p963724661312"></a><a name="p963724661312"></a>Integer</p>
    </td>
    <td class="cellrowborder" valign="top" width="37.419999999999995%" headers="mcps1.2.5.1.4 "><p id="p3637114651317"><a name="p3637114651317"></a><a name="p3637114651317"></a>删除的点数目</p>
    </td>
    </tr>
    </tbody>
    </table>

-   请求失败样例

    ```
    Http Status Code: 400
    {
        "results": [],
        "errors": [
            {
                "code": "GES.8904",
                "message": "Label index in vertices is not found."
            }
        ]
    }
    ```


## 返回值<a name="section5966141394619"></a>

-   正常

200

-   异常

    **表 8**  异常返回值说明

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


## Cypher预置条件<a name="section96831823102810"></a>

>![](public_sys-resources/icon-note.gif) **说明：** 
>图规格为一千亿边（公测版）的图暂无此约束。

当前的Cypher查询编译过程中使用了基于label的点边索引，如需正常使用Cypher，请使用[新建索引API](新建索引(1-1-6).md)构建索引，示例如下：

-   点label索引添加命令示例

    ```
    POST http://{SERVER_URL}/ges/v1.0/{project_id}/graphs/{graph_name}/indices
    {
            "indexName": "cypher_vertex_index",
            "indexType": "GlobalCompositeVertexIndex",
            "hasLabel": "true",
            "indexProperty": []
    }
    ```

-   边label索引添加命令示例

    ```
    POST http://{SERVER_URL}/ges/v1.0/{project_id}/graphs/{graph_name}/indices
    {
            "indexName": "cypher_edge_index",
            "indexType": "GlobalCompositeEdgeIndex",
            "hasLabel": "true",
            "indexProperty": []
    }
    ```

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >1.  需要同时添加两个索引（点label索引和边label索引）才能正常使用Cypher查询。
    >2.  不需要构建的情况：如果图中已经存在hasLabel为true, indexProperty为空的点索引或边索引，则不需要重复构建。
    >3.  添加索引API为异步接口，查询索引是否添加成功，请使用[查询Job状态API](查询Job状态(1-0-0)-业务面.md)。


## 基本操作<a name="section874721075619"></a>

<a name="table17321759135613"></a>
<table><thead align="left"><tr id="row1233159145618"><th class="cellrowborder" valign="top" width="28.29%" id="mcps1.1.3.1.1"><p id="p1994174175712"><a name="p1994174175712"></a><a name="p1994174175712"></a>操作名</p>
</th>
<th class="cellrowborder" valign="top" width="71.71%" id="mcps1.1.3.1.2"><p id="p119419414571"><a name="p119419414571"></a><a name="p119419414571"></a>Cypher语句</p>
</th>
</tr>
</thead>
<tbody><tr id="row1533175915566"><td class="cellrowborder" valign="top" width="28.29%" headers="mcps1.1.3.1.1 "><p id="p09484105718"><a name="p09484105718"></a><a name="p09484105718"></a>查点</p>
</td>
<td class="cellrowborder" valign="top" width="71.71%" headers="mcps1.1.3.1.2 "><p id="p159474155719"><a name="p159474155719"></a><a name="p159474155719"></a>match (n) return n</p>
</td>
</tr>
<tr id="row123345919560"><td class="cellrowborder" valign="top" width="28.29%" headers="mcps1.1.3.1.1 "><p id="p13949415712"><a name="p13949415712"></a><a name="p13949415712"></a>查边</p>
</td>
<td class="cellrowborder" valign="top" width="71.71%" headers="mcps1.1.3.1.2 "><p id="p395114155710"><a name="p395114155710"></a><a name="p395114155710"></a>match (n)-[r]-&gt;(m) return n, r, m</p>
</td>
</tr>
<tr id="row1933159175610"><td class="cellrowborder" valign="top" width="28.29%" headers="mcps1.1.3.1.1 "><p id="p17951544579"><a name="p17951544579"></a><a name="p17951544579"></a>查路径</p>
</td>
<td class="cellrowborder" valign="top" width="71.71%" headers="mcps1.1.3.1.2 "><p id="p995148576"><a name="p995148576"></a><a name="p995148576"></a>match (n:user)-[r]-&gt;(m:movie)--&gt;(s:series) return n,r,m,s</p>
</td>
</tr>
<tr id="row113345918561"><td class="cellrowborder" valign="top" width="28.29%" headers="mcps1.1.3.1.1 "><p id="p39517475715"><a name="p39517475715"></a><a name="p39517475715"></a>过滤查询</p>
</td>
<td class="cellrowborder" valign="top" width="71.71%" headers="mcps1.1.3.1.2 "><p id="p16953410578"><a name="p16953410578"></a><a name="p16953410578"></a>match(n:user) where n.userid&gt;=5 return n</p>
</td>
</tr>
<tr id="row183475915565"><td class="cellrowborder" valign="top" width="28.29%" headers="mcps1.1.3.1.1 "><p id="p69510411578"><a name="p69510411578"></a><a name="p69510411578"></a>分组聚集</p>
</td>
<td class="cellrowborder" valign="top" width="71.71%" headers="mcps1.1.3.1.2 "><p id="p89510417575"><a name="p89510417575"></a><a name="p89510417575"></a>match(n:movie) return n.genres, count(*)</p>
</td>
</tr>
<tr id="row23412595562"><td class="cellrowborder" valign="top" width="28.29%" headers="mcps1.1.3.1.1 "><p id="p14958415579"><a name="p14958415579"></a><a name="p14958415579"></a>去重</p>
</td>
<td class="cellrowborder" valign="top" width="71.71%" headers="mcps1.1.3.1.2 "><p id="p10954495712"><a name="p10954495712"></a><a name="p10954495712"></a>match(n:movie) return distinct n.genres</p>
</td>
</tr>
<tr id="row1334125918564"><td class="cellrowborder" valign="top" width="28.29%" headers="mcps1.1.3.1.1 "><p id="p179515419577"><a name="p179515419577"></a><a name="p179515419577"></a>排序</p>
</td>
<td class="cellrowborder" valign="top" width="71.71%" headers="mcps1.1.3.1.2 "><p id="p199584185718"><a name="p199584185718"></a><a name="p199584185718"></a>match(n:movie) return n order by n.movieid</p>
</td>
</tr>
<tr id="row53445914564"><td class="cellrowborder" valign="top" width="28.29%" headers="mcps1.1.3.1.1 "><p id="p99517455720"><a name="p99517455720"></a><a name="p99517455720"></a>创建点</p>
</td>
<td class="cellrowborder" valign="top" width="71.71%" headers="mcps1.1.3.1.2 "><p id="p89515415576"><a name="p89515415576"></a><a name="p89515415576"></a>create (n:user{userid:1}) return n</p>
</td>
</tr>
<tr id="row2784139113212"><td class="cellrowborder" valign="top" width="28.29%" headers="mcps1.1.3.1.1 "><p id="p7459151213323"><a name="p7459151213323"></a><a name="p7459151213323"></a>创建边</p>
</td>
<td class="cellrowborder" valign="top" width="71.71%" headers="mcps1.1.3.1.2 "><p id="p5459912183211"><a name="p5459912183211"></a><a name="p5459912183211"></a>match (n:user{userid:15}),(m:movie{movieid:10}) create (n)-[r:rate]-&gt;(m)</p>
</td>
</tr>
<tr id="row13425911565"><td class="cellrowborder" valign="top" width="28.29%" headers="mcps1.1.3.1.1 "><p id="p39574165719"><a name="p39574165719"></a><a name="p39574165719"></a>删除点</p>
</td>
<td class="cellrowborder" valign="top" width="71.71%" headers="mcps1.1.3.1.2 "><p id="p159516415717"><a name="p159516415717"></a><a name="p159516415717"></a>match (n:user{userid:1}) delete n</p>
</td>
</tr>
<tr id="row193416594565"><td class="cellrowborder" valign="top" width="28.29%" headers="mcps1.1.3.1.1 "><p id="p15951246579"><a name="p15951246579"></a><a name="p15951246579"></a>更改标签</p>
</td>
<td class="cellrowborder" valign="top" width="71.71%" headers="mcps1.1.3.1.2 "><p id="p1951042576"><a name="p1951042576"></a><a name="p1951042576"></a>match (n:user{userid:1}) set n:movie return n</p>
</td>
</tr>
<tr id="row1034205925619"><td class="cellrowborder" valign="top" width="28.29%" headers="mcps1.1.3.1.1 "><p id="p795441572"><a name="p795441572"></a><a name="p795441572"></a>更改属性</p>
</td>
<td class="cellrowborder" valign="top" width="71.71%" headers="mcps1.1.3.1.2 "><p id="p49518411571"><a name="p49518411571"></a><a name="p49518411571"></a>match (n:user{userid:1}) set n.userid=2 return n</p>
</td>
</tr>
</tbody>
</table>

## Cypher实现的兼容性<a name="section1885065125812"></a>

-   Cypher支持的子句列表

    Cypher实现了若干子句，通过对子句进行组合可以实现丰富的查询语义，进而完成点边过滤、多跳查询、排序去重、分组聚集等诸多能力。目前GES支持的Cypher子句如下：

    **表 9**  Cypher支持的子句清单

    <a name="table79051242012"></a>
    <table><thead align="left"><tr id="row290615421816"><th class="cellrowborder" valign="top" width="21.822182218221823%" id="mcps1.2.4.1.1"><p id="p4668102414215"><a name="p4668102414215"></a><a name="p4668102414215"></a>子句</p>
    </th>
    <th class="cellrowborder" valign="top" width="16.001600160016004%" id="mcps1.2.4.1.2"><p id="p76683249217"><a name="p76683249217"></a><a name="p76683249217"></a>支持情况</p>
    </th>
    <th class="cellrowborder" valign="top" width="62.17621762176218%" id="mcps1.2.4.1.3"><p id="p17668162420220"><a name="p17668162420220"></a><a name="p17668162420220"></a>举例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row790604213111"><td class="cellrowborder" valign="top" width="21.822182218221823%" headers="mcps1.2.4.1.1 "><p id="p16668624324"><a name="p16668624324"></a><a name="p16668624324"></a>match</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.001600160016004%" headers="mcps1.2.4.1.2 "><p id="p966819241122"><a name="p966819241122"></a><a name="p966819241122"></a>部分支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.17621762176218%" headers="mcps1.2.4.1.3 "><p id="p76684241827"><a name="p76684241827"></a><a name="p76684241827"></a>match (n:movie) return n</p>
    </td>
    </tr>
    <tr id="row179061842413"><td class="cellrowborder" valign="top" width="21.822182218221823%" headers="mcps1.2.4.1.1 "><p id="p366813241921"><a name="p366813241921"></a><a name="p366813241921"></a>return</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.001600160016004%" headers="mcps1.2.4.1.2 "><p id="p1366816242218"><a name="p1366816242218"></a><a name="p1366816242218"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.17621762176218%" headers="mcps1.2.4.1.3 "><p id="p1666820242217"><a name="p1666820242217"></a><a name="p1666820242217"></a>return [1,2,3] as p</p>
    </td>
    </tr>
    <tr id="row89061042217"><td class="cellrowborder" valign="top" width="21.822182218221823%" headers="mcps1.2.4.1.1 "><p id="p106681924625"><a name="p106681924625"></a><a name="p106681924625"></a>with</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.001600160016004%" headers="mcps1.2.4.1.2 "><p id="p1466862419219"><a name="p1466862419219"></a><a name="p1466862419219"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.17621762176218%" headers="mcps1.2.4.1.3 "><p id="p26697240211"><a name="p26697240211"></a><a name="p26697240211"></a>match (n) with labels(n) as label, count(*) as count</p>
    <p id="p76699241524"><a name="p76699241524"></a><a name="p76699241524"></a>where count &gt; 10 return *</p>
    </td>
    </tr>
    <tr id="row190613429112"><td class="cellrowborder" valign="top" width="21.822182218221823%" headers="mcps1.2.4.1.1 "><p id="p18669324623"><a name="p18669324623"></a><a name="p18669324623"></a>where</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.001600160016004%" headers="mcps1.2.4.1.2 "><p id="p176692242026"><a name="p176692242026"></a><a name="p176692242026"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.17621762176218%" headers="mcps1.2.4.1.3 "><p id="p1466917241027"><a name="p1466917241027"></a><a name="p1466917241027"></a>match (n:movie) where n.movieid &gt; 10 return n</p>
    </td>
    </tr>
    <tr id="row890754210113"><td class="cellrowborder" valign="top" width="21.822182218221823%" headers="mcps1.2.4.1.1 "><p id="p176692024623"><a name="p176692024623"></a><a name="p176692024623"></a>order by</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.001600160016004%" headers="mcps1.2.4.1.2 "><p id="p206696241225"><a name="p206696241225"></a><a name="p206696241225"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.17621762176218%" headers="mcps1.2.4.1.3 "><p id="p4669424723"><a name="p4669424723"></a><a name="p4669424723"></a>match (n:movie) return n order by n.genres</p>
    </td>
    </tr>
    <tr id="row59072422116"><td class="cellrowborder" valign="top" width="21.822182218221823%" headers="mcps1.2.4.1.1 "><p id="p1166915248213"><a name="p1166915248213"></a><a name="p1166915248213"></a>skip</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.001600160016004%" headers="mcps1.2.4.1.2 "><p id="p15669524221"><a name="p15669524221"></a><a name="p15669524221"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.17621762176218%" headers="mcps1.2.4.1.3 "><p id="p76690241325"><a name="p76690241325"></a><a name="p76690241325"></a>match (n:movie) return n order by n.genres skip 5</p>
    </td>
    </tr>
    <tr id="row2090717429110"><td class="cellrowborder" valign="top" width="21.822182218221823%" headers="mcps1.2.4.1.1 "><p id="p366922410214"><a name="p366922410214"></a><a name="p366922410214"></a>limit</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.001600160016004%" headers="mcps1.2.4.1.2 "><p id="p14669624527"><a name="p14669624527"></a><a name="p14669624527"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.17621762176218%" headers="mcps1.2.4.1.3 "><p id="p4669112416217"><a name="p4669112416217"></a><a name="p4669112416217"></a>match (n:movie) return n order by n.genres skip 5 limit 10</p>
    </td>
    </tr>
    <tr id="row690716421017"><td class="cellrowborder" valign="top" width="21.822182218221823%" headers="mcps1.2.4.1.1 "><p id="p56691248214"><a name="p56691248214"></a><a name="p56691248214"></a>create</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.001600160016004%" headers="mcps1.2.4.1.2 "><p id="p0669152416219"><a name="p0669152416219"></a><a name="p0669152416219"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.17621762176218%" headers="mcps1.2.4.1.3 "><p id="p3669172410214"><a name="p3669172410214"></a><a name="p3669172410214"></a>create (n:user{_ID_: 'Jack' }) return n</p>
    </td>
    </tr>
    <tr id="row1990711421012"><td class="cellrowborder" valign="top" width="21.822182218221823%" headers="mcps1.2.4.1.1 "><p id="p96691824727"><a name="p96691824727"></a><a name="p96691824727"></a>delete</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.001600160016004%" headers="mcps1.2.4.1.2 "><p id="p13669102414212"><a name="p13669102414212"></a><a name="p13669102414212"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.17621762176218%" headers="mcps1.2.4.1.3 "><p id="p186695241222"><a name="p186695241222"></a><a name="p186695241222"></a>match (n:movie)&lt;-[r]-(m:user) delete r</p>
    </td>
    </tr>
    <tr id="row5907194210112"><td class="cellrowborder" valign="top" width="21.822182218221823%" headers="mcps1.2.4.1.1 "><p id="p19669132413219"><a name="p19669132413219"></a><a name="p19669132413219"></a>set</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.001600160016004%" headers="mcps1.2.4.1.2 "><p id="p106691524924"><a name="p106691524924"></a><a name="p106691524924"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.17621762176218%" headers="mcps1.2.4.1.3 "><p id="p6669524226"><a name="p6669524226"></a><a name="p6669524226"></a>match (n:user{userid:0}) set n.gender='M' return n</p>
    </td>
    </tr>
    <tr id="row139076421719"><td class="cellrowborder" valign="top" width="21.822182218221823%" headers="mcps1.2.4.1.1 "><p id="p16691224123"><a name="p16691224123"></a><a name="p16691224123"></a>call procedures</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.001600160016004%" headers="mcps1.2.4.1.2 "><p id="p366918249218"><a name="p366918249218"></a><a name="p366918249218"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.17621762176218%" headers="mcps1.2.4.1.3 "><p id="p867011241023"><a name="p867011241023"></a><a name="p867011241023"></a>call db.schema()</p>
    </td>
    </tr>
    <tr id="row5517943194813"><td class="cellrowborder" valign="top" width="21.822182218221823%" headers="mcps1.2.4.1.1 "><p id="p1963954510487"><a name="p1963954510487"></a><a name="p1963954510487"></a>unwind</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.001600160016004%" headers="mcps1.2.4.1.2 "><p id="p1763954517489"><a name="p1763954517489"></a><a name="p1763954517489"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.17621762176218%" headers="mcps1.2.4.1.3 "><p id="p7639114524819"><a name="p7639114524819"></a><a name="p7639114524819"></a>unwind [1, 2, 3] as p return p</p>
    </td>
    </tr>
    </tbody>
    </table>

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >1.  目前暂不支持union、merge、foreach、optional等操作，暂不支持使用Cypher语句增删索引，后续会逐渐开放支持。
    >2.  由于GES的元数据不是Schema Free的，点边label属性等有严格的限制，因此不支持Remove操作。
    >3.  Order by子句不支持List类型的排序，当属性值的Cardinality不为single时，排序结果未知。

-   参数化查询支持

    Cypher支持参数化的查询。通过把查询语句中的数值、字符串等值类型提取为参数，加速查询的编译时间，提高查询速度。

    以下提供几种参数化查询的示例：

    -   参数化查询请求示例1：

        ```
        POST http://{SERVER_URL}/ges/v1.0/{project_id}/graphs/{graph_name}/action?action_id=execute-cypher-query
        {
                 "statements": [{
                           "statement": " match (n:user) where n.occupation = $occupation return n",
                           "parameters": {
                                 "occupation" : "artist"
                            },
                           "resultDataContents": ["row"]
                 }]
        }
        ```

    -   参数化查询请求示例2：

        ```
        POST http://{SERVER_URL}/ges/v1.0/{project_id}/graphs/{graph_name}/action?action_id=execute-cypher-query
        {
                 "statements": [{
                           "statement": " match (n:user {`Zip-code`:'98133'}) set n = $props return n",
                           "parameters": {
                                   "props": {
                                   "gender": "M",
                                   "age": "56+"
                                }
                            },
                           "resultDataContents": ["row"]
                 }]
        }
        ```

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >参数化查询不适用于以下场景，下列查询语句均无法正常执行：
    >-   属性键值，如：match \(n\) where n.$param = 'something'
    >-   点边标签，如：match \(n:user\) set n:$code

-   数据类型支持

    GES目前支持char、char\_array、float、double、Boolean、long、Integer、date、enum、string共10种数据类型，布尔型和数值型在Cypher语法中都能得到支持，其他类型和Cypher存在如下的映射关系，在GES内部实现了类型的转换：

    **表 10**  GES和Cypher的类型映射关系

    <a name="table41064510414"></a>
    <table><thead align="left"><tr id="row410717554117"><th class="cellrowborder" valign="top" width="15.52155215521552%" id="mcps1.2.4.1.1"><p id="p8781151919414"><a name="p8781151919414"></a><a name="p8781151919414"></a>GES类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="21.33213321332133%" id="mcps1.2.4.1.2"><p id="p8781191913410"><a name="p8781191913410"></a><a name="p8781191913410"></a>Cypher类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="63.14631463146314%" id="mcps1.2.4.1.3"><p id="p87812199412"><a name="p87812199412"></a><a name="p87812199412"></a>备注</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1510717512414"><td class="cellrowborder" valign="top" width="15.52155215521552%" headers="mcps1.2.4.1.1 "><p id="p2781191918419"><a name="p2781191918419"></a><a name="p2781191918419"></a>char</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.33213321332133%" headers="mcps1.2.4.1.2 "><p id="p15781111924116"><a name="p15781111924116"></a><a name="p15781111924116"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.14631463146314%" headers="mcps1.2.4.1.3 "><p id="p77814192415"><a name="p77814192415"></a><a name="p77814192415"></a>-</p>
    </td>
    </tr>
    <tr id="row121079510411"><td class="cellrowborder" valign="top" width="15.52155215521552%" headers="mcps1.2.4.1.1 "><p id="p2781719154113"><a name="p2781719154113"></a><a name="p2781719154113"></a>char_array</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.33213321332133%" headers="mcps1.2.4.1.2 "><p id="p36291023193119"><a name="p36291023193119"></a><a name="p36291023193119"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.14631463146314%" headers="mcps1.2.4.1.3 "><p id="p10794161916415"><a name="p10794161916415"></a><a name="p10794161916415"></a>-</p>
    </td>
    </tr>
    <tr id="row121089511415"><td class="cellrowborder" valign="top" width="15.52155215521552%" headers="mcps1.2.4.1.1 "><p id="p177811419194118"><a name="p177811419194118"></a><a name="p177811419194118"></a>string</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.33213321332133%" headers="mcps1.2.4.1.2 "><p id="p818353415315"><a name="p818353415315"></a><a name="p818353415315"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.14631463146314%" headers="mcps1.2.4.1.3 "><p id="p179451934113"><a name="p179451934113"></a><a name="p179451934113"></a>-</p>
    </td>
    </tr>
    <tr id="row6108185184118"><td class="cellrowborder" valign="top" width="15.52155215521552%" headers="mcps1.2.4.1.1 "><p id="p1378191974110"><a name="p1378191974110"></a><a name="p1378191974110"></a>enum</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.33213321332133%" headers="mcps1.2.4.1.2 "><p id="p11781151904113"><a name="p11781151904113"></a><a name="p11781151904113"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.14631463146314%" headers="mcps1.2.4.1.3 "><p id="p1778131934115"><a name="p1778131934115"></a><a name="p1778131934115"></a>由于Cypher语法中未提供枚举相关的语法，在Cypher查询时enum作为String进行输出，使用Cypher设置属性时对于不在枚举列表中的值会设置失败。</p>
    <div class="note" id="note118538495344"><a name="note118538495344"></a><a name="note118538495344"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1085424963415"><a name="p1085424963415"></a><a name="p1085424963415"></a>图规格为一千亿边（公测版）的图暂不支持该参数。</p>
    </div></div>
    </td>
    </tr>
    <tr id="row151089594116"><td class="cellrowborder" valign="top" width="15.52155215521552%" headers="mcps1.2.4.1.1 "><p id="p16781171917419"><a name="p16781171917419"></a><a name="p16781171917419"></a>date</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.33213321332133%" headers="mcps1.2.4.1.2 "><p id="p07821192413"><a name="p07821192413"></a><a name="p07821192413"></a>Temporal</p>
    </td>
    <td class="cellrowborder" valign="top" width="63.14631463146314%" headers="mcps1.2.4.1.3 "><p id="p14782201974117"><a name="p14782201974117"></a><a name="p14782201974117"></a>目前支持Date按GES的日期格式输入和输出，暂不支持调用Cypher日期函数输入日期。</p>
    </td>
    </tr>
    </tbody>
    </table>

    **表 11**  Cypher特殊类型支持情况

    <a name="table1962142294414"></a>
    <table><thead align="left"><tr id="row16621022104412"><th class="cellrowborder" valign="top" width="15.761576157615762%" id="mcps1.2.4.1.1"><p id="p569833418442"><a name="p569833418442"></a><a name="p569833418442"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="19.761976197619763%" id="mcps1.2.4.1.2"><p id="p2069803494415"><a name="p2069803494415"></a><a name="p2069803494415"></a>支持情况</p>
    </th>
    <th class="cellrowborder" valign="top" width="64.47644764476448%" id="mcps1.2.4.1.3"><p id="p17698203419447"><a name="p17698203419447"></a><a name="p17698203419447"></a>查询举例 &amp; 备注</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row362262224419"><td class="cellrowborder" valign="top" width="15.761576157615762%" headers="mcps1.2.4.1.1 "><p id="p16698934104412"><a name="p16698934104412"></a><a name="p16698934104412"></a>Node</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.761976197619763%" headers="mcps1.2.4.1.2 "><p id="p369823404413"><a name="p369823404413"></a><a name="p369823404413"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="64.47644764476448%" headers="mcps1.2.4.1.3 "><p id="p46982346448"><a name="p46982346448"></a><a name="p46982346448"></a>match (n) return n limit 10</p>
    </td>
    </tr>
    <tr id="row16622122224415"><td class="cellrowborder" valign="top" width="15.761576157615762%" headers="mcps1.2.4.1.1 "><p id="p1869818349442"><a name="p1869818349442"></a><a name="p1869818349442"></a>Relationship</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.761976197619763%" headers="mcps1.2.4.1.2 "><p id="p5698123412444"><a name="p5698123412444"></a><a name="p5698123412444"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="64.47644764476448%" headers="mcps1.2.4.1.3 "><p id="p15698123444418"><a name="p15698123444418"></a><a name="p15698123444418"></a>match (n)-[r]-&gt;(m) return r limit 10</p>
    </td>
    </tr>
    <tr id="row762252217444"><td class="cellrowborder" valign="top" width="15.761576157615762%" headers="mcps1.2.4.1.1 "><p id="p76985348442"><a name="p76985348442"></a><a name="p76985348442"></a>List</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.761976197619763%" headers="mcps1.2.4.1.2 "><p id="p136984342440"><a name="p136984342440"></a><a name="p136984342440"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="64.47644764476448%" headers="mcps1.2.4.1.3 "><p id="p569853412448"><a name="p569853412448"></a><a name="p569853412448"></a>return [1,2,3] as li</p>
    </td>
    </tr>
    <tr id="row56221622194410"><td class="cellrowborder" valign="top" width="15.761576157615762%" headers="mcps1.2.4.1.1 "><p id="p569815344448"><a name="p569815344448"></a><a name="p569815344448"></a>Map</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.761976197619763%" headers="mcps1.2.4.1.2 "><p id="p1169853414448"><a name="p1169853414448"></a><a name="p1169853414448"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="64.47644764476448%" headers="mcps1.2.4.1.3 "><p id="p10698123411445"><a name="p10698123411445"></a><a name="p10698123411445"></a>match (n)--&gt;(m) return {start:id(n), end:id(m)}</p>
    </td>
    </tr>
    <tr id="row1062202234417"><td class="cellrowborder" valign="top" width="15.761576157615762%" headers="mcps1.2.4.1.1 "><p id="p169811348445"><a name="p169811348445"></a><a name="p169811348445"></a>Path</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.761976197619763%" headers="mcps1.2.4.1.2 "><p id="p10614518121717"><a name="p10614518121717"></a><a name="p10614518121717"></a>支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="64.47644764476448%" headers="mcps1.2.4.1.3 "><p id="p6614111891715"><a name="p6614111891715"></a><a name="p6614111891715"></a>match p=(n1)-[:friends*1..2]-(n2) return  p limit 10</p>
    <div class="note" id="note1993098131615"><a name="note1993098131615"></a><a name="note1993098131615"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p99301817167"><a name="p99301817167"></a><a name="p99301817167"></a>图规格为一千亿边（公测版）的图暂不支持该参数。</p>
    </div></div>
    </td>
    </tr>
    <tr id="row16221922194416"><td class="cellrowborder" valign="top" width="15.761576157615762%" headers="mcps1.2.4.1.1 "><p id="p469893415441"><a name="p469893415441"></a><a name="p469893415441"></a>Point、Spatial</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.761976197619763%" headers="mcps1.2.4.1.2 "><p id="p14698203414410"><a name="p14698203414410"></a><a name="p14698203414410"></a>暂不支持</p>
    </td>
    <td class="cellrowborder" valign="top" width="64.47644764476448%" headers="mcps1.2.4.1.3 "><p id="p96981634194410"><a name="p96981634194410"></a><a name="p96981634194410"></a>-</p>
    </td>
    </tr>
    </tbody>
    </table>

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >对[表 Cypher特殊类型支持情况](#table1962142294414)中提到的特殊类型，其中除了List用于匹配GES中的多值属性外，其他类型均无法通过set语句设为点边上某个属性的值。

-   表达式

    Cypher查询的where子句支持多种的表达式，可以组合成丰富的过滤条件，目前支持的表达式如下:

    <a name="table20406172153417"></a>
    <table><thead align="left"><tr id="row840652112342"><th class="cellrowborder" valign="top" width="23.522352235223522%" id="mcps1.1.4.1.1"><p id="p84021124133414"><a name="p84021124133414"></a><a name="p84021124133414"></a>运算类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.551755175517552%" id="mcps1.1.4.1.2"><p id="p640213244347"><a name="p640213244347"></a><a name="p640213244347"></a>表达式</p>
    </th>
    <th class="cellrowborder" valign="top" width="58.92589258925892%" id="mcps1.1.4.1.3"><p id="p040216246346"><a name="p040216246346"></a><a name="p040216246346"></a>举例&amp;备注</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row54067210343"><td class="cellrowborder" rowspan="3" valign="top" width="23.522352235223522%" headers="mcps1.1.4.1.1 "><p id="p94021124173420"><a name="p94021124173420"></a><a name="p94021124173420"></a>逻辑运算</p>
    <p id="p542272423418"><a name="p542272423418"></a><a name="p542272423418"></a></p>
    <p id="p154221124163413"><a name="p154221124163413"></a><a name="p154221124163413"></a></p>
    </td>
    <td class="cellrowborder" valign="top" width="17.551755175517552%" headers="mcps1.1.4.1.2 "><p id="p2403162443414"><a name="p2403162443414"></a><a name="p2403162443414"></a>and</p>
    </td>
    <td class="cellrowborder" valign="top" width="58.92589258925892%" headers="mcps1.1.4.1.3 "><p id="p1040312453411"><a name="p1040312453411"></a><a name="p1040312453411"></a>match (n:user) where n.age='Under 18' and n.gender='F' return n</p>
    </td>
    </tr>
    <tr id="row10407172163412"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p5403524173416"><a name="p5403524173416"></a><a name="p5403524173416"></a>or</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p1840392418345"><a name="p1840392418345"></a><a name="p1840392418345"></a>match(n:user) where n.`Zip-code`='22181' or n.userid=6 return n</p>
    </td>
    </tr>
    <tr id="row6407132112349"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p1540372443418"><a name="p1540372443418"></a><a name="p1540372443418"></a>not</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p12403112483420"><a name="p12403112483420"></a><a name="p12403112483420"></a>match(n:movie) where not n.genres contains 'Drama' return n</p>
    </td>
    </tr>
    <tr id="row184076215343"><td class="cellrowborder" rowspan="2" valign="top" width="23.522352235223522%" headers="mcps1.1.4.1.1 "><p id="p12403132416348"><a name="p12403132416348"></a><a name="p12403132416348"></a>空值判断</p>
    <p id="p742117241340"><a name="p742117241340"></a><a name="p742117241340"></a></p>
    </td>
    <td class="cellrowborder" valign="top" width="17.551755175517552%" headers="mcps1.1.4.1.2 "><p id="p3403524133415"><a name="p3403524133415"></a><a name="p3403524133415"></a>is null</p>
    </td>
    <td class="cellrowborder" valign="top" width="58.92589258925892%" headers="mcps1.1.4.1.3 "><p id="p44035247344"><a name="p44035247344"></a><a name="p44035247344"></a>match (n) where n.userid is null return n</p>
    </td>
    </tr>
    <tr id="row174076216347"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p8403924103416"><a name="p8403924103416"></a><a name="p8403924103416"></a>is not null</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p184037244342"><a name="p184037244342"></a><a name="p184037244342"></a>match (n) where n.userid is not null return n</p>
    </td>
    </tr>
    <tr id="row1407162173415"><td class="cellrowborder" valign="top" width="23.522352235223522%" headers="mcps1.1.4.1.1 "><p id="p24030242342"><a name="p24030242342"></a><a name="p24030242342"></a>比较运算</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.551755175517552%" headers="mcps1.1.4.1.2 "><p id="p1440312418348"><a name="p1440312418348"></a><a name="p1440312418348"></a>&gt;,&gt;=,&lt;,&lt;=,=,&lt;&gt;</p>
    </td>
    <td class="cellrowborder" valign="top" width="58.92589258925892%" headers="mcps1.1.4.1.3 "><p id="p15403624163420"><a name="p15403624163420"></a><a name="p15403624163420"></a>match(n:user) where n.userid&gt;=5 return n</p>
    </td>
    </tr>
    <tr id="row240832117341"><td class="cellrowborder" rowspan="3" valign="top" width="23.522352235223522%" headers="mcps1.1.4.1.1 "><p id="p1840320246347"><a name="p1840320246347"></a><a name="p1840320246347"></a>字符串比较</p>
    <p id="p1542115249348"><a name="p1542115249348"></a><a name="p1542115249348"></a></p>
    <p id="p842192418349"><a name="p842192418349"></a><a name="p842192418349"></a></p>
    </td>
    <td class="cellrowborder" valign="top" width="17.551755175517552%" headers="mcps1.1.4.1.2 "><p id="p240342411342"><a name="p240342411342"></a><a name="p240342411342"></a>starts with</p>
    </td>
    <td class="cellrowborder" valign="top" width="58.92589258925892%" headers="mcps1.1.4.1.3 "><p id="p8403132416347"><a name="p8403132416347"></a><a name="p8403132416347"></a>match(n:movie) where n.genres starts with 'Comedy' return n</p>
    </td>
    </tr>
    <tr id="row15408142113344"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p174031624153412"><a name="p174031624153412"></a><a name="p174031624153412"></a>ends with</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p1340362473410"><a name="p1340362473410"></a><a name="p1340362473410"></a>match(n:movie) where n.genres ends with 'Drama' return n</p>
    </td>
    </tr>
    <tr id="row19408721143412"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p840311247347"><a name="p840311247347"></a><a name="p840311247347"></a>contains</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p1440322414345"><a name="p1440322414345"></a><a name="p1440322414345"></a>match(n:movie) where n.genres contains 'Drama' return n</p>
    </td>
    </tr>
    <tr id="row19408142111340"><td class="cellrowborder" rowspan="2" valign="top" width="23.522352235223522%" headers="mcps1.1.4.1.1 "><p id="p11405324143418"><a name="p11405324143418"></a><a name="p11405324143418"></a>List相关运算</p>
    <p id="p680303564411"><a name="p680303564411"></a><a name="p680303564411"></a></p>
    </td>
    <td class="cellrowborder" valign="top" width="17.551755175517552%" headers="mcps1.1.4.1.2 "><p id="p1140511246346"><a name="p1140511246346"></a><a name="p1140511246346"></a>in</p>
    </td>
    <td class="cellrowborder" valign="top" width="58.92589258925892%" headers="mcps1.1.4.1.3 "><p id="p20405924173417"><a name="p20405924173417"></a><a name="p20405924173417"></a>match(n:student) where 'math' in n.courses return n</p>
    </td>
    </tr>
    <tr id="row18222182432"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p1280317354442"><a name="p1280317354442"></a><a name="p1280317354442"></a>[]运算符</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p148051535184416"><a name="p148051535184416"></a><a name="p148051535184416"></a>match(n:user) return n[' userid']</p>
    <p id="p16805113514443"><a name="p16805113514443"></a><a name="p16805113514443"></a>with [1, 2, 3, 4] as list return list[0]</p>
    <p id="p08061935114417"><a name="p08061935114417"></a><a name="p08061935114417"></a>with [1, 2, 3, 4] as list return list[0..1]</p>
    <p id="p8807535194414"><a name="p8807535194414"></a><a name="p8807535194414"></a>match p=(n)--&gt;(m) return [x in nodes(p) where x.gender='F'|id(x)] <span id="ph283444119169"><a name="ph283444119169"></a><a name="ph283444119169"></a>（一千亿边（公测版）暂不支持该条运算符）</span></p>
    </td>
    </tr>
    </tbody>
    </table>

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >Cypher查询的where子句暂不支持case表达式、算数运算符、正则匹配等。

-   函数和过程

    -   函数

    在分组聚集、点边操作时，cypher支持一系列的函数，目前支持的函数如下所示：

    1.  聚集函数

        目前支持count、collect两个聚集函数。

        <a name="table9239162941410"></a>
        <table><thead align="left"><tr id="row13239192913142"><th class="cellrowborder" valign="top" width="22.472247224722473%" id="mcps1.1.4.1.1"><p id="p0239529101412"><a name="p0239529101412"></a><a name="p0239529101412"></a>函数名</p>
        </th>
        <th class="cellrowborder" valign="top" width="27.09270927092709%" id="mcps1.1.4.1.2"><p id="p723952961418"><a name="p723952961418"></a><a name="p723952961418"></a>释义</p>
        </th>
        <th class="cellrowborder" valign="top" width="50.43504350435043%" id="mcps1.1.4.1.3"><p id="p142391029121419"><a name="p142391029121419"></a><a name="p142391029121419"></a>举例</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="row19239192914142"><td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.1.4.1.1 "><p id="p162399293144"><a name="p162399293144"></a><a name="p162399293144"></a>count</p>
        </td>
        <td class="cellrowborder" valign="top" width="27.09270927092709%" headers="mcps1.1.4.1.2 "><p id="p202391129121419"><a name="p202391129121419"></a><a name="p202391129121419"></a>求结果总数</p>
        </td>
        <td class="cellrowborder" valign="top" width="50.43504350435043%" headers="mcps1.1.4.1.3 "><p id="p923992941411"><a name="p923992941411"></a><a name="p923992941411"></a>match (n) return count(*)</p>
        <p id="p1123982931414"><a name="p1123982931414"></a><a name="p1123982931414"></a>match (n) return count(n.userid)</p>
        </td>
        </tr>
        <tr id="row323982901411"><td class="cellrowborder" valign="top" width="22.472247224722473%" headers="mcps1.1.4.1.1 "><p id="p13239202915147"><a name="p13239202915147"></a><a name="p13239202915147"></a>collect(2.2.17)</p>
        </td>
        <td class="cellrowborder" valign="top" width="27.09270927092709%" headers="mcps1.1.4.1.2 "><p id="p223912931413"><a name="p223912931413"></a><a name="p223912931413"></a>将结果聚集为列表</p>
        </td>
        <td class="cellrowborder" valign="top" width="50.43504350435043%" headers="mcps1.1.4.1.3 "><p id="p14239182917148"><a name="p14239182917148"></a><a name="p14239182917148"></a>match (n:movie) return n.genres, collect(n) as movieList</p>
        </td>
        </tr>
        </tbody>
        </table>

    2.  普通函数

        根据入参不同，普通函数分为点边操作类、路径操作类、列表操作类、值操作类等几类函数。

        **表 12**  点边操作类

        <a name="table1897782141517"></a>
        <table><tbody><tr id="row61721422121515"><td class="cellrowborder" valign="top" width="20.67206720672067%"><p id="p817217222159"><a name="p817217222159"></a><a name="p817217222159"></a>函数名</p>
        </td>
        <td class="cellrowborder" valign="top" width="22.182218221822183%"><p id="p11172192218156"><a name="p11172192218156"></a><a name="p11172192218156"></a>释义</p>
        </td>
        <td class="cellrowborder" valign="top" width="57.14571457145715%"><p id="p101721222101517"><a name="p101721222101517"></a><a name="p101721222101517"></a>举例</p>
        </td>
        </tr>
        <tr id="row6172322131519"><td class="cellrowborder" valign="top" width="20.67206720672067%"><p id="p9172122261516"><a name="p9172122261516"></a><a name="p9172122261516"></a>id</p>
        </td>
        <td class="cellrowborder" valign="top" width="22.182218221822183%"><p id="p2172202210155"><a name="p2172202210155"></a><a name="p2172202210155"></a>获取点的id</p>
        </td>
        <td class="cellrowborder" valign="top" width="57.14571457145715%"><p id="p12172132219152"><a name="p12172132219152"></a><a name="p12172132219152"></a>match (n) return id(n)</p>
        </td>
        </tr>
        <tr id="row61721422191514"><td class="cellrowborder" valign="top" width="20.67206720672067%"><p id="p417272271518"><a name="p417272271518"></a><a name="p417272271518"></a>labels</p>
        </td>
        <td class="cellrowborder" valign="top" width="22.182218221822183%"><p id="p15173122261516"><a name="p15173122261516"></a><a name="p15173122261516"></a>获取点的label</p>
        </td>
        <td class="cellrowborder" valign="top" width="57.14571457145715%"><p id="p1617332241515"><a name="p1617332241515"></a><a name="p1617332241515"></a>match (n) return labels(n)</p>
        </td>
        </tr>
        <tr id="row617322216158"><td class="cellrowborder" valign="top" width="20.67206720672067%"><p id="p18173182218156"><a name="p18173182218156"></a><a name="p18173182218156"></a>type</p>
        </td>
        <td class="cellrowborder" valign="top" width="22.182218221822183%"><p id="p181731922171514"><a name="p181731922171514"></a><a name="p181731922171514"></a>获取边的label</p>
        </td>
        <td class="cellrowborder" valign="top" width="57.14571457145715%"><p id="p4173322161514"><a name="p4173322161514"></a><a name="p4173322161514"></a>match(n)-[r]-&gt;(m) return type(r)</p>
        </td>
        </tr>
        </tbody>
        </table>

        **表 13**  路径操作类函数\(2.2.19\)

        <a name="table4323252111714"></a>
        <table><thead align="left"><tr id="row3324115201710"><th class="cellrowborder" valign="top" width="22.86228622862286%" id="mcps1.2.4.1.1"><p id="p1751184142913"><a name="p1751184142913"></a><a name="p1751184142913"></a>函数名</p>
        </th>
        <th class="cellrowborder" valign="top" width="23.65236523652365%" id="mcps1.2.4.1.2"><p id="p11511244297"><a name="p11511244297"></a><a name="p11511244297"></a>释义</p>
        </th>
        <th class="cellrowborder" valign="top" width="53.48534853485349%" id="mcps1.2.4.1.3"><p id="p151274122914"><a name="p151274122914"></a><a name="p151274122914"></a>举例</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="row5324175271719"><td class="cellrowborder" valign="top" width="22.86228622862286%" headers="mcps1.2.4.1.1 "><p id="p85125442912"><a name="p85125442912"></a><a name="p85125442912"></a>nodes</p>
        </td>
        <td class="cellrowborder" valign="top" width="23.65236523652365%" headers="mcps1.2.4.1.2 "><p id="p115121843293"><a name="p115121843293"></a><a name="p115121843293"></a>获取路径上的点列表</p>
        </td>
        <td class="cellrowborder" valign="top" width="53.48534853485349%" headers="mcps1.2.4.1.3 "><p id="p20512124142911"><a name="p20512124142911"></a><a name="p20512124142911"></a>match p=(n)-[:friends*1..2]-&gt;(m) return nodes(p)</p>
        <p id="p01811637304"><a name="p01811637304"></a><a name="p01811637304"></a><span id="ph918117315306"><a name="ph918117315306"></a><a name="ph918117315306"></a>图规格为一千亿边（公测版）的图暂不支持该函数。</span></p>
        </td>
        </tr>
        <tr id="row932465261710"><td class="cellrowborder" valign="top" width="22.86228622862286%" headers="mcps1.2.4.1.1 "><p id="p45127411292"><a name="p45127411292"></a><a name="p45127411292"></a>relationships</p>
        </td>
        <td class="cellrowborder" valign="top" width="23.65236523652365%" headers="mcps1.2.4.1.2 "><p id="p551211472916"><a name="p551211472916"></a><a name="p551211472916"></a>获取路径上的边列表</p>
        </td>
        <td class="cellrowborder" valign="top" width="53.48534853485349%" headers="mcps1.2.4.1.3 "><p id="p151204102911"><a name="p151204102911"></a><a name="p151204102911"></a>match p=(n)-[:friends*1..2]-&gt;(m) return relationships(p)</p>
        <p id="p126531618302"><a name="p126531618302"></a><a name="p126531618302"></a><span id="ph116539612302"><a name="ph116539612302"></a><a name="ph116539612302"></a>图规格为一千亿边（公测版）的图暂不支持该函数。</span></p>
        </td>
        </tr>
        <tr id="row3324205215171"><td class="cellrowborder" valign="top" width="22.86228622862286%" headers="mcps1.2.4.1.1 "><p id="p175123412295"><a name="p175123412295"></a><a name="p175123412295"></a>length</p>
        </td>
        <td class="cellrowborder" valign="top" width="23.65236523652365%" headers="mcps1.2.4.1.2 "><p id="p6512746297"><a name="p6512746297"></a><a name="p6512746297"></a>获取路径长度</p>
        </td>
        <td class="cellrowborder" valign="top" width="53.48534853485349%" headers="mcps1.2.4.1.3 "><p id="p20512144102912"><a name="p20512144102912"></a><a name="p20512144102912"></a>match p=(n)-[:friends*1..2]-&gt;(m) return length(p)</p>
        </td>
        </tr>
        </tbody>
        </table>

        **表 14**  列表操作类函数

        <a name="table192762313181"></a>
        <table><thead align="left"><tr id="row1827713101818"><th class="cellrowborder" valign="top" width="22.86228622862286%" id="mcps1.2.4.1.1"><p id="p623016616199"><a name="p623016616199"></a><a name="p623016616199"></a>函数名</p>
        </th>
        <th class="cellrowborder" valign="top" width="23.65236523652365%" id="mcps1.2.4.1.2"><p id="p9230106131916"><a name="p9230106131916"></a><a name="p9230106131916"></a>释义</p>
        </th>
        <th class="cellrowborder" valign="top" width="53.48534853485349%" id="mcps1.2.4.1.3"><p id="p14230166131918"><a name="p14230166131918"></a><a name="p14230166131918"></a>举例</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="row13277143171817"><td class="cellrowborder" valign="top" width="22.86228622862286%" headers="mcps1.2.4.1.1 "><p id="p1923014618192"><a name="p1923014618192"></a><a name="p1923014618192"></a>head</p>
        </td>
        <td class="cellrowborder" valign="top" width="23.65236523652365%" headers="mcps1.2.4.1.2 "><p id="p123096101919"><a name="p123096101919"></a><a name="p123096101919"></a>获取列表的第一个元素</p>
        </td>
        <td class="cellrowborder" valign="top" width="53.48534853485349%" headers="mcps1.2.4.1.3 "><p id="p1923016671916"><a name="p1923016671916"></a><a name="p1923016671916"></a>with [1,2,3,4] as list return head(list)</p>
        </td>
        </tr>
        <tr id="row12277113112184"><td class="cellrowborder" valign="top" width="22.86228622862286%" headers="mcps1.2.4.1.1 "><p id="p19230965194"><a name="p19230965194"></a><a name="p19230965194"></a>last</p>
        </td>
        <td class="cellrowborder" valign="top" width="23.65236523652365%" headers="mcps1.2.4.1.2 "><p id="p52303615194"><a name="p52303615194"></a><a name="p52303615194"></a>获取列表的最后一个元素</p>
        </td>
        <td class="cellrowborder" valign="top" width="53.48534853485349%" headers="mcps1.2.4.1.3 "><p id="p132303621910"><a name="p132303621910"></a><a name="p132303621910"></a>with [1,2,3,4] as list return last(list)</p>
        </td>
        </tr>
        <tr id="row182773318186"><td class="cellrowborder" valign="top" width="22.86228622862286%" headers="mcps1.2.4.1.1 "><p id="p13230864194"><a name="p13230864194"></a><a name="p13230864194"></a>size</p>
        </td>
        <td class="cellrowborder" valign="top" width="23.65236523652365%" headers="mcps1.2.4.1.2 "><p id="p8230206161913"><a name="p8230206161913"></a><a name="p8230206161913"></a>获取列表长度</p>
        </td>
        <td class="cellrowborder" valign="top" width="53.48534853485349%" headers="mcps1.2.4.1.3 "><p id="p123014617196"><a name="p123014617196"></a><a name="p123014617196"></a>with [1,2,3,4] as list return size(list)</p>
        </td>
        </tr>
        </tbody>
        </table>

        **表 15**  值操作类

        <a name="table16382142841916"></a>
        <table><tbody><tr id="row78120281196"><td class="cellrowborder" valign="top" width="19.31%"><p id="p11812152815194"><a name="p11812152815194"></a><a name="p11812152815194"></a>函数名</p>
        </td>
        <td class="cellrowborder" valign="top" width="31.95%"><p id="p11812328191915"><a name="p11812328191915"></a><a name="p11812328191915"></a>释义</p>
        </td>
        <td class="cellrowborder" valign="top" width="48.74%"><p id="p9812162821917"><a name="p9812162821917"></a><a name="p9812162821917"></a>举例</p>
        </td>
        </tr>
        <tr id="row11812112871915"><td class="cellrowborder" valign="top" width="19.31%"><p id="p20812192831911"><a name="p20812192831911"></a><a name="p20812192831911"></a>toString(2.2.21)</p>
        </td>
        <td class="cellrowborder" valign="top" width="31.95%"><p id="p1681214284192"><a name="p1681214284192"></a><a name="p1681214284192"></a>将其他值类型转换为string</p>
        </td>
        <td class="cellrowborder" valign="top" width="48.74%"><p id="p16812328131915"><a name="p16812328131915"></a><a name="p16812328131915"></a>match (n) where toString(labels(n)) contains 'movi' return n</p>
        </td>
        </tr>
        </tbody>
        </table>

        **表 16**  谓词函数（2.2.19）

        <a name="table17420927172011"></a>
        <table><tbody><tr id="row9814327112016"><td class="cellrowborder" valign="top" width="11.931193119311931%"><p id="p1581492762014"><a name="p1581492762014"></a><a name="p1581492762014"></a>函数名</p>
        </td>
        <td class="cellrowborder" valign="top" width="46.11461146114612%"><p id="p3814527152010"><a name="p3814527152010"></a><a name="p3814527152010"></a>释义</p>
        </td>
        <td class="cellrowborder" valign="top" width="41.95419541954195%"><p id="p13814727162014"><a name="p13814727162014"></a><a name="p13814727162014"></a>举例</p>
        </td>
        </tr>
        <tr id="row7814162762015"><td class="cellrowborder" valign="top" width="11.931193119311931%"><p id="p138141627162018"><a name="p138141627162018"></a><a name="p138141627162018"></a>all</p>
        </td>
        <td class="cellrowborder" valign="top" width="46.11461146114612%"><p id="p08141127132015"><a name="p08141127132015"></a><a name="p08141127132015"></a>全部元素满足表达式，则返回true</p>
        </td>
        <td class="cellrowborder" valign="top" width="41.95419541954195%"><p id="p2814227202018"><a name="p2814227202018"></a><a name="p2814227202018"></a>all (x in p where x&gt;1)</p>
        </td>
        </tr>
        <tr id="row781452718201"><td class="cellrowborder" valign="top" width="11.931193119311931%"><p id="p381472714201"><a name="p381472714201"></a><a name="p381472714201"></a>any</p>
        </td>
        <td class="cellrowborder" valign="top" width="46.11461146114612%"><p id="p18814827172013"><a name="p18814827172013"></a><a name="p18814827172013"></a>任意一个元素满足表达式，则返回true</p>
        </td>
        <td class="cellrowborder" valign="top" width="41.95419541954195%"><p id="p12814122782012"><a name="p12814122782012"></a><a name="p12814122782012"></a>any (x in p where x&gt;1)</p>
        </td>
        </tr>
        <tr id="row1181472716207"><td class="cellrowborder" valign="top" width="11.931193119311931%"><p id="p481420278201"><a name="p481420278201"></a><a name="p481420278201"></a>none</p>
        </td>
        <td class="cellrowborder" valign="top" width="46.11461146114612%"><p id="p13814227132019"><a name="p13814227132019"></a><a name="p13814227132019"></a>全部元素无法满足表达式，返回true</p>
        </td>
        <td class="cellrowborder" valign="top" width="41.95419541954195%"><p id="p128141327202013"><a name="p128141327202013"></a><a name="p128141327202013"></a>none (x in p where x&gt;1)</p>
        </td>
        </tr>
        <tr id="row081412272205"><td class="cellrowborder" valign="top" width="11.931193119311931%"><p id="p2814122772017"><a name="p2814122772017"></a><a name="p2814122772017"></a>single</p>
        </td>
        <td class="cellrowborder" valign="top" width="46.11461146114612%"><p id="p1881442782011"><a name="p1881442782011"></a><a name="p1881442782011"></a>有且仅有1个元素满足表达式，返回true</p>
        </td>
        <td class="cellrowborder" valign="top" width="41.95419541954195%"><p id="p68146271204"><a name="p68146271204"></a><a name="p68146271204"></a>single (x in p where x&gt;1)</p>
        </td>
        </tr>
        </tbody>
        </table>

        >![](public_sys-resources/icon-note.gif) **说明：** 
        >avg\(\)、max\(\)、min\(\)等聚集函数，以及sin\(\)、cos\(\)等数学函数将在后续版本中陆续开放。
        >度数类函数、路径操作类函数在百亿规格和千亿规格暂不开放，toUpper和toLower函数在千亿规格暂不开放。

        -   过程

            目前GES 支持如下过程（Procedure）：

            <a name="table19888154015155"></a>
            <table><thead align="left"><tr id="row188744011156"><th class="cellrowborder" valign="top" width="42.980000000000004%" id="mcps1.1.3.1.1"><p id="p18887194071520"><a name="p18887194071520"></a><a name="p18887194071520"></a>名称</p>
            </th>
            <th class="cellrowborder" valign="top" width="57.02%" id="mcps1.1.3.1.2"><p id="p3887194041517"><a name="p3887194041517"></a><a name="p3887194041517"></a>语句</p>
            </th>
            </tr>
            </thead>
            <tbody><tr id="row1588814061520"><td class="cellrowborder" valign="top" width="42.980000000000004%" headers="mcps1.1.3.1.1 "><p id="p178871440191520"><a name="p178871440191520"></a><a name="p178871440191520"></a>获取图模式相关信息</p>
            </td>
            <td class="cellrowborder" valign="top" width="57.02%" headers="mcps1.1.3.1.2 "><p id="p138882405152"><a name="p138882405152"></a><a name="p138882405152"></a>call db.schema()</p>
            </td>
            </tr>
            <tr id="row2888154016154"><td class="cellrowborder" valign="top" width="42.980000000000004%" headers="mcps1.1.3.1.1 "><p id="p188894012156"><a name="p188894012156"></a><a name="p188894012156"></a>获取点label</p>
            </td>
            <td class="cellrowborder" valign="top" width="57.02%" headers="mcps1.1.3.1.2 "><p id="p1588864014152"><a name="p1588864014152"></a><a name="p1588864014152"></a>call db.labels()</p>
            </td>
            </tr>
            <tr id="row1088834031519"><td class="cellrowborder" valign="top" width="42.980000000000004%" headers="mcps1.1.3.1.1 "><p id="p17888174031512"><a name="p17888174031512"></a><a name="p17888174031512"></a>获取边label</p>
            </td>
            <td class="cellrowborder" valign="top" width="57.02%" headers="mcps1.1.3.1.2 "><p id="p158881240191514"><a name="p158881240191514"></a><a name="p158881240191514"></a>call db.relationshipTypes()</p>
            <p id="p198889405158"><a name="p198889405158"></a><a name="p198889405158"></a><span id="ph2888134051512"><a name="ph2888134051512"></a><a name="ph2888134051512"></a>图规格为一千亿边（公测版）的图暂不支持该过程。</span></p>
            </td>
            </tr>
            <tr id="row128881640111514"><td class="cellrowborder" valign="top" width="42.980000000000004%" headers="mcps1.1.3.1.1 "><p id="p888894016154"><a name="p888894016154"></a><a name="p888894016154"></a>查询当前正在执行的Cypher语句</p>
            </td>
            <td class="cellrowborder" valign="top" width="57.02%" headers="mcps1.1.3.1.2 "><p id="p68886402150"><a name="p68886402150"></a><a name="p68886402150"></a>call dbms.listQueries()</p>
            </td>
            </tr>
            <tr id="row148881440171517"><td class="cellrowborder" valign="top" width="42.980000000000004%" headers="mcps1.1.3.1.1 "><p id="p138883406157"><a name="p138883406157"></a><a name="p138883406157"></a>根据queryId终止某条Cypher语句</p>
            </td>
            <td class="cellrowborder" valign="top" width="57.02%" headers="mcps1.1.3.1.2 "><p id="p18888164091516"><a name="p18888164091516"></a><a name="p18888164091516"></a>call dbms.killQuery('queryId')</p>
            </td>
            </tr>
            </tbody>
            </table>



-   点id的兼容性
    -   Cypher添加点时不提供设置id的语法，GES中添加点需要一个字符串型的id，来唯一的标识一个点。为了兼容Cypher语法**，**当前Create语句实现中，通过使用一个特殊的标识符\_ID\_指定点的id。例如create \(n\{\_ID\_:’123456’\} \)语句，会创建一个id为’123456’的点。
    -   若创建时未指明id，则系统为此点生成一个随机id。

        >![](public_sys-resources/icon-note.gif) **说明：** 
        >标识符“\_ID\_”仅在create语句中支持，match、set等子句均不支持\_ID\_标识。Match子句中可使用函数id\(\)获取点id。


-   添加边时的平行边处理策略：

    通过cypher添加边的时候，允许添加重复边，此处的重复边的定义为<源点，终点\>相同的两条边。



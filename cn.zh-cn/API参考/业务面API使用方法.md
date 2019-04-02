# 业务面API使用方法<a name="ges_03_0121"></a>

## 业务面API介绍<a name="section14658154615276"></a>

GES业务面API提供点、边、元数据的创建、查询、更新、删除等操作方法。

其请求/响应对可以分为五个部分：

-   [请求URI](#section1849899574)
-   [请求消息头](#section1454211155819)
-   [请求消息体](#section14612192315587)
-   [响应消息头](#section7804143005810)
-   [响应消息体](#section034615592583)
-   [发起请求](#section140743661613)

## 请求URI<a name="section1849899574"></a>

图引擎服务业务面API请求URI由如下部分组成。

**\{URI-scheme\} :// \{SERVER\_URL\} / \{resource-path\} ? \{query-string\}**

尽管请求URI包含在请求消息头中，但大多数语言或框架都要求您从请求消息中单独传递它，所以我们在此单独拿出来强调。

**表 1**  URI中的参数说明

<a name="t1797260c744a4e1a85d354f259cae55a"></a>
<table><thead align="left"><tr id="r6dceed05bcc649d2b032accbb2980a31"><th class="cellrowborder" valign="top" width="18.04%" id="mcps1.2.3.1.1"><p id="a3446b6b785cb432bae9f45aef9177041"><a name="a3446b6b785cb432bae9f45aef9177041"></a><a name="a3446b6b785cb432bae9f45aef9177041"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="81.96%" id="mcps1.2.3.1.2"><p id="abe71244a12ac45308e99d4bbf975a9f8"><a name="abe71244a12ac45308e99d4bbf975a9f8"></a><a name="abe71244a12ac45308e99d4bbf975a9f8"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row106982018513"><td class="cellrowborder" valign="top" width="18.04%" headers="mcps1.2.3.1.1 "><p id="p136991001517"><a name="p136991001517"></a><a name="p136991001517"></a>URI-scheme</p>
</td>
<td class="cellrowborder" valign="top" width="81.96%" headers="mcps1.2.3.1.2 "><p id="p56992017520"><a name="p56992017520"></a><a name="p56992017520"></a>表示用于传输请求的协议。GES的API都必须采用https。</p>
</td>
</tr>
<tr id="rb217758afff146a1b40b0dcbb28a4ae1"><td class="cellrowborder" valign="top" width="18.04%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0035614179_p480227019422"><a name="zh-cn_topic_0035614179_p480227019422"></a><a name="zh-cn_topic_0035614179_p480227019422"></a>SERVER_URL</p>
</td>
<td class="cellrowborder" valign="top" width="81.96%" headers="mcps1.2.3.1.2 "><p id="ad82b3484a1be43ddadf436efbe15285e"><a name="ad82b3484a1be43ddadf436efbe15285e"></a><a name="ad82b3484a1be43ddadf436efbe15285e"></a>图的访问地址，取值参考<a href="#section124171305112">业务面API使用限制</a>。</p>
</td>
</tr>
<tr id="refeed61892004ea682639be281a1a707"><td class="cellrowborder" valign="top" width="18.04%" headers="mcps1.2.3.1.1 "><p id="p1797614317513"><a name="p1797614317513"></a><a name="p1797614317513"></a>resource-path</p>
</td>
<td class="cellrowborder" valign="top" width="81.96%" headers="mcps1.2.3.1.2 "><p id="a90409cbb8b1c49c4ad4d3cfee16f475e"><a name="a90409cbb8b1c49c4ad4d3cfee16f475e"></a><a name="a90409cbb8b1c49c4ad4d3cfee16f475e"></a>资源路径，即API访问路径。从具体接口的URI模块获取，例如“ges/v1.0/{projectId}/graphs/{graphName}/vertices/action?action_id=query”。</p>
</td>
</tr>
<tr id="row19939365518"><td class="cellrowborder" valign="top" width="18.04%" headers="mcps1.2.3.1.1 "><p id="p393966455"><a name="p393966455"></a><a name="p393966455"></a>Query string</p>
</td>
<td class="cellrowborder" valign="top" width="81.96%" headers="mcps1.2.3.1.2 "><p id="p159401867517"><a name="p159401867517"></a><a name="p159401867517"></a>可选参数，例如API版本或资源选择标准。</p>
</td>
</tr>
</tbody>
</table>

## 业务面API使用限制<a name="section124171305112"></a>

用户访问业务面API有三种方式：

-   通过ECS访问，且创建ECS的VPC和创建图选定的VPC是同一个。如果安全组选择的是同一个，则可以直接访问；如果安全组不是同一个，要在创建图的安全组开通该ECS的访问限制，即放开80和443端口（分别对应支持HTTP和HTTPS访问）。这种场景，API的SERVER\_URL为GES Console图详情的内网访问地址或者管理面API查询图详情返回体的"privateIp"字段的值。
-   通过ECS访问，但创建ECS的VPC和创建图选定的VPC不是同一个。需要对ECS所在的VPC和建图用的VPC创建VPC对等连接，创建VPC对等连接请参考[创建对等连接](https://support.huaweicloud.com/api-vpc/zh-cn_topic_0075677485.html)。同时要在创建图的安全组开通该ECS的访问限制，即放开80和443端口。这种场景，API的SERVER\_URL为GES Console图详情的内网访问地址或者管理面API查询图详情返回体的"privateIp"字段的值。
-   通过公网访问。此时要求创建弹性公网IP（EIP），且要在创建图的安全组开通客户端的访问限制，即放开80和443端口。这种场景，API的SERVER\_URL为GES Console图详情的公网访问地址或者管理面API查询图详情返回体的"publicIp"字段的值，也即用户绑定或者自动创建的弹性公网IP地址。

## 请求消息头<a name="section1454211155819"></a>

请求消息头包含如下两部分。

-   HTTP方法（也称为操作或动词），它告诉服务你正在请求什么类型的操作。GES的 REST API支持的方法如[表2](#table26515221161)所示。

    **表 2**  HTTP方法

    <a name="table26515221161"></a>
    <table><thead align="left"><tr id="row10728192251616"><th class="cellrowborder" valign="top" width="12.120000000000001%" id="mcps1.2.3.1.1"><p id="p157281422201616"><a name="p157281422201616"></a><a name="p157281422201616"></a>方法</p>
    </th>
    <th class="cellrowborder" valign="top" width="87.88%" id="mcps1.2.3.1.2"><p id="p672872219161"><a name="p672872219161"></a><a name="p672872219161"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1394642154919"><td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.3.1.1 "><p id="p13848247114919"><a name="p13848247114919"></a><a name="p13848247114919"></a>GET</p>
    </td>
    <td class="cellrowborder" valign="top" width="87.88%" headers="mcps1.2.3.1.2 "><p id="p2850147164917"><a name="p2850147164917"></a><a name="p2850147164917"></a>请求服务器返回指定资源。</p>
    </td>
    </tr>
    <tr id="row5728322121617"><td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.3.1.1 "><p id="p97281922111616"><a name="p97281922111616"></a><a name="p97281922111616"></a>PUT</p>
    </td>
    <td class="cellrowborder" valign="top" width="87.88%" headers="mcps1.2.3.1.2 "><p id="p1572882241617"><a name="p1572882241617"></a><a name="p1572882241617"></a>请求服务器更新指定资源。</p>
    </td>
    </tr>
    <tr id="row172872211168"><td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.3.1.1 "><p id="p472820225166"><a name="p472820225166"></a><a name="p472820225166"></a>POST</p>
    </td>
    <td class="cellrowborder" valign="top" width="87.88%" headers="mcps1.2.3.1.2 "><p id="p272812212161"><a name="p272812212161"></a><a name="p272812212161"></a>请求服务器新增资源或执行特殊操作。</p>
    </td>
    </tr>
    <tr id="row8728132231620"><td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.3.1.1 "><p id="p16729422151616"><a name="p16729422151616"></a><a name="p16729422151616"></a>DELETE</p>
    </td>
    <td class="cellrowborder" valign="top" width="87.88%" headers="mcps1.2.3.1.2 "><p id="p10729122261616"><a name="p10729122261616"></a><a name="p10729122261616"></a>请求服务器删除指定资源，如删除对象等。</p>
    </td>
    </tr>
    <tr id="row2157183019175"><td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.3.1.1 "><p id="p15159030201715"><a name="p15159030201715"></a><a name="p15159030201715"></a>HEAD</p>
    </td>
    <td class="cellrowborder" valign="top" width="87.88%" headers="mcps1.2.3.1.2 "><p id="p42261787492"><a name="p42261787492"></a><a name="p42261787492"></a>请求服务器资源头部。</p>
    </td>
    </tr>
    <tr id="row16729182210163"><td class="cellrowborder" valign="top" width="12.120000000000001%" headers="mcps1.2.3.1.1 "><p id="p1772932218162"><a name="p1772932218162"></a><a name="p1772932218162"></a>PATCH</p>
    </td>
    <td class="cellrowborder" valign="top" width="87.88%" headers="mcps1.2.3.1.2 "><p id="p13729192251620"><a name="p13729192251620"></a><a name="p13729192251620"></a>请求服务器更新资源的部分内容。</p>
    <p id="p0729142221616"><a name="p0729142221616"></a><a name="p0729142221616"></a>当资源不存在的时候，PATCH可能会去创建一个新的资源。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   可选的附加请求头字段，如指定的URI和HTTP方法所要求的字段。详细的公共请求消息头字段请参见[表3](#d0e691)，其中请求认证信息请参见[获取请求认证](获取请求认证.md)。

    **表 3**  公共请求消息头

    <a name="d0e691"></a>
    <table><thead align="left"><tr id="row43435224"><th class="cellrowborder" valign="top" width="16.61%" id="mcps1.2.5.1.1"><p id="p28592218"><a name="p28592218"></a><a name="p28592218"></a>参数名</p>
    </th>
    <th class="cellrowborder" valign="top" width="31.869999999999997%" id="mcps1.2.5.1.2"><p id="p34268337"><a name="p34268337"></a><a name="p34268337"></a>说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="23.31%" id="mcps1.2.5.1.3"><p id="p24271941"><a name="p24271941"></a><a name="p24271941"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="28.21%" id="mcps1.2.5.1.4"><p id="p19870205"><a name="p19870205"></a><a name="p19870205"></a>示例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row33821495"><td class="cellrowborder" valign="top" width="16.61%" headers="mcps1.2.5.1.1 "><p id="p55186561"><a name="p55186561"></a><a name="p55186561"></a>Content-type</p>
    </td>
    <td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.2.5.1.2 "><p id="p40926476"><a name="p40926476"></a><a name="p40926476"></a>发送的实体的MIME类型。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.31%" headers="mcps1.2.5.1.3 "><p id="p26710272"><a name="p26710272"></a><a name="p26710272"></a>是。</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.21%" headers="mcps1.2.5.1.4 "><p id="p16048387"><a name="p16048387"></a><a name="p16048387"></a>application/json</p>
    </td>
    </tr>
    <tr id="row26328706"><td class="cellrowborder" valign="top" width="16.61%" headers="mcps1.2.5.1.1 "><p id="p52250442"><a name="p52250442"></a><a name="p52250442"></a>X-Auth-Token</p>
    </td>
    <td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.2.5.1.2 "><p id="p4427423"><a name="p4427423"></a><a name="p4427423"></a>用户Token。</p>
    </td>
    <td class="cellrowborder" valign="top" width="23.31%" headers="mcps1.2.5.1.3 "><p id="p6366124"><a name="p6366124"></a><a name="p6366124"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.21%" headers="mcps1.2.5.1.4 "><p id="p45894015"><a name="p45894015"></a><a name="p45894015"></a>-</p>
    </td>
    </tr>
    <tr id="row10392952"><td class="cellrowborder" valign="top" width="16.61%" headers="mcps1.2.5.1.1 "><p id="p36522766"><a name="p36522766"></a><a name="p36522766"></a>X-Language</p>
    </td>
    <td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.2.5.1.2 "><p id="p5554106"><a name="p5554106"></a><a name="p5554106"></a>请求语言，支持配置如下值：</p>
    <a name="ul49986954"></a><a name="ul49986954"></a><ul id="ul49986954"><li>zh-cn：中文</li><li>en-us：英文</li></ul>
    </td>
    <td class="cellrowborder" valign="top" width="23.31%" headers="mcps1.2.5.1.3 "><p id="p3392477"><a name="p3392477"></a><a name="p3392477"></a>是。</p>
    </td>
    <td class="cellrowborder" valign="top" width="28.21%" headers="mcps1.2.5.1.4 "><p id="p6355195"><a name="p6355195"></a><a name="p6355195"></a>en-us</p>
    </td>
    </tr>
    </tbody>
    </table>

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >其它header属性，请遵照http协议。  


## 请求消息体<a name="section14612192315587"></a>

请求消息体通常以结构化格式（如JSON或XML）发出，与请求消息头中Content-type对应，传递除请求消息头之外的内容。

## 响应消息头<a name="section7804143005810"></a>

响应消息头包含如下两部分。

-   一个HTTP状态代码，从2xx成功代码到4xx或5xx错误代码。或者，可以返回服务定义的状态码，如API文档中所示。
-   附加响应头字段，如支持请求的响应所需，如Content-type响应消息头。详细的公共响应消息头字段请参见[表4](#d0e872)。

    **表 4**  公共响应消息头

    <a name="d0e872"></a>
    <table><thead align="left"><tr id="row30056148"><th class="cellrowborder" valign="top" width="30%" id="mcps1.2.3.1.1"><p id="p18628895"><a name="p18628895"></a><a name="p18628895"></a>参数名</p>
    </th>
    <th class="cellrowborder" valign="top" width="70%" id="mcps1.2.3.1.2"><p id="p32545531"><a name="p32545531"></a><a name="p32545531"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row18942351"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p57935492"><a name="p57935492"></a><a name="p57935492"></a>Content-Length</p>
    </td>
    <td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p62263298"><a name="p62263298"></a><a name="p62263298"></a>响应消息体的字节长度，单位为Byte。</p>
    </td>
    </tr>
    <tr id="row23498771"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p24352304"><a name="p24352304"></a><a name="p24352304"></a>Date</p>
    </td>
    <td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p26379626"><a name="p26379626"></a><a name="p26379626"></a>系统响应的时间。</p>
    </td>
    </tr>
    <tr id="row36090045"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p37612524"><a name="p37612524"></a><a name="p37612524"></a>Content-type</p>
    </td>
    <td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p26715628"><a name="p26715628"></a><a name="p26715628"></a>发送的实体的MIME类型。</p>
    </td>
    </tr>
    <tr id="row8829153383717"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.3.1.1 "><p id="p13830183316376"><a name="p13830183316376"></a><a name="p13830183316376"></a>X-Trace-ID</p>
    </td>
    <td class="cellrowborder" valign="top" width="70%" headers="mcps1.2.3.1.2 "><p id="p10482151517407"><a name="p10482151517407"></a><a name="p10482151517407"></a>请求返回的追踪ID，用于定位问题。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 响应消息体<a name="section034615592583"></a>

响应消息体通常以结构化格式（如JSON或XML）返回，与响应消息头中Content-type对应，传递除响应消息头之外的内容。

## 发起请求<a name="section140743661613"></a>

共有三种方式可以基于已构建好的请求消息发起请求，分别为：

-   cURL

    cURL是一个命令行工具，用来执行各种URL操作和信息传输。cURL充当的是HTTP客户端，可以发送HTTP请求给服务端，并接收响应消息。cURL适用于接口调试。关于cURL详细信息请参见[https://curl.haxx.se/](https://curl.haxx.se/)。

-   编码

    通过编码调用接口，组装请求消息，并发送处理请求消息。

-   REST客户端

    Mozilla、Google都为REST提供了图形化的浏览器插件，发送处理请求消息。针对Firefox，请参见[Firefox REST Client](https://addons.mozilla.org/en-US/firefox/addon/restclient/)。针对Chrome，请参见[Postman](https://chrome.google.com/webstore/detail/postman/fhbjgbiflinjbdggehcddcbncdddomop)。



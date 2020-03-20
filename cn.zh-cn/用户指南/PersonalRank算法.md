# PersonalRank算法<a name="ges_01_0045"></a>

## 概述<a name="section204471932366"></a>

PersonalRank算法又称Personalized PageRank算法。该算法继承了经典PageRank算法的思想，利用图链接结构来递归计算各节点的重要性。与PageRank算法不同的是，为了保证随机行走中各节点的访问概率能够反映出用户的偏好，PersonalRank算法在随机行走中的每次跳转会以（1-alpha）的概率返回到source节点，因此可以基于source节点个性化地计算网络节点的相关性和重要性。（PersonalRank值越高，source节点的相关性/重要性越高）。

## 适用场景<a name="section168801381005"></a>

PersonalRank算法适用于商品推荐、好友推荐和网页推荐等场景。

## 参数说明<a name="section18154105319710"></a>

**表 1**  PersonalRank算法参数说明

<a name="table9438140783"></a>
<table><thead align="left"><tr id="row104385017818"><th class="cellrowborder" valign="top" width="14.34343434343434%" id="mcps1.2.7.1.1"><p id="p164384014819"><a name="p164384014819"></a><a name="p164384014819"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="9.8989898989899%" id="mcps1.2.7.1.2"><p id="p143812016818"><a name="p143812016818"></a><a name="p143812016818"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="18.22222222222222%" id="mcps1.2.7.1.3"><p id="p070711912812"><a name="p070711912812"></a><a name="p070711912812"></a>说明</p>
</th>
<th class="cellrowborder" valign="top" width="9.05050505050505%" id="mcps1.2.7.1.4"><p id="p66074112146"><a name="p66074112146"></a><a name="p66074112146"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="30.303030303030305%" id="mcps1.2.7.1.5"><p id="p4438901986"><a name="p4438901986"></a><a name="p4438901986"></a>取值范围</p>
</th>
<th class="cellrowborder" valign="top" width="18.181818181818183%" id="mcps1.2.7.1.6"><p id="p41583960175619"><a name="p41583960175619"></a><a name="p41583960175619"></a>默认值</p>
</th>
</tr>
</thead>
<tbody><tr id="row7439180683"><td class="cellrowborder" valign="top" width="14.34343434343434%" headers="mcps1.2.7.1.1 "><p id="p13751101797"><a name="p13751101797"></a><a name="p13751101797"></a>source</p>
</td>
<td class="cellrowborder" valign="top" width="9.8989898989899%" headers="mcps1.2.7.1.2 "><p id="p20751701994"><a name="p20751701994"></a><a name="p20751701994"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="18.22222222222222%" headers="mcps1.2.7.1.3 "><p id="p177515011918"><a name="p177515011918"></a><a name="p177515011918"></a>节点的ID</p>
</td>
<td class="cellrowborder" valign="top" width="9.05050505050505%" headers="mcps1.2.7.1.4 "><p id="p1960715115144"><a name="p1960715115144"></a><a name="p1960715115144"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="30.303030303030305%" headers="mcps1.2.7.1.5 "><p id="p17521018916"><a name="p17521018916"></a><a name="p17521018916"></a>-</p>
</td>
<td class="cellrowborder" valign="top" width="18.181818181818183%" headers="mcps1.2.7.1.6 "><p id="p12857639175619"><a name="p12857639175619"></a><a name="p12857639175619"></a>-</p>
</td>
</tr>
<tr id="row1592512201673"><td class="cellrowborder" valign="top" width="14.34343434343434%" headers="mcps1.2.7.1.1 "><p id="p4752150793"><a name="p4752150793"></a><a name="p4752150793"></a>alpha</p>
</td>
<td class="cellrowborder" valign="top" width="9.8989898989899%" headers="mcps1.2.7.1.2 "><p id="p127528012920"><a name="p127528012920"></a><a name="p127528012920"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18.22222222222222%" headers="mcps1.2.7.1.3 "><p id="p5752301191"><a name="p5752301191"></a><a name="p5752301191"></a>权重系数</p>
</td>
<td class="cellrowborder" valign="top" width="9.05050505050505%" headers="mcps1.2.7.1.4 "><p id="p960731119141"><a name="p960731119141"></a><a name="p960731119141"></a>Double</p>
</td>
<td class="cellrowborder" valign="top" width="30.303030303030305%" headers="mcps1.2.7.1.5 "><p id="p8569141114913"><a name="p8569141114913"></a><a name="p8569141114913"></a>0~1，不包括0和1</p>
</td>
<td class="cellrowborder" valign="top" width="18.181818181818183%" headers="mcps1.2.7.1.6 "><p id="p34835871175619"><a name="p34835871175619"></a><a name="p34835871175619"></a>0.85</p>
</td>
</tr>
<tr id="row1883311181175"><td class="cellrowborder" valign="top" width="14.34343434343434%" headers="mcps1.2.7.1.1 "><p id="p07521208912"><a name="p07521208912"></a><a name="p07521208912"></a>convergence</p>
</td>
<td class="cellrowborder" valign="top" width="9.8989898989899%" headers="mcps1.2.7.1.2 "><p id="p137529015913"><a name="p137529015913"></a><a name="p137529015913"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18.22222222222222%" headers="mcps1.2.7.1.3 "><p id="p87521501194"><a name="p87521501194"></a><a name="p87521501194"></a>收敛精度</p>
</td>
<td class="cellrowborder" valign="top" width="9.05050505050505%" headers="mcps1.2.7.1.4 "><p id="p10607111121416"><a name="p10607111121416"></a><a name="p10607111121416"></a>Double</p>
</td>
<td class="cellrowborder" valign="top" width="30.303030303030305%" headers="mcps1.2.7.1.5 "><p id="p12122017093"><a name="p12122017093"></a><a name="p12122017093"></a>0~1，不包括0和1</p>
</td>
<td class="cellrowborder" valign="top" width="18.181818181818183%" headers="mcps1.2.7.1.6 "><p id="p3133287175619"><a name="p3133287175619"></a><a name="p3133287175619"></a>0.00001</p>
</td>
</tr>
<tr id="row136122160711"><td class="cellrowborder" valign="top" width="14.34343434343434%" headers="mcps1.2.7.1.1 "><p id="p20752001591"><a name="p20752001591"></a><a name="p20752001591"></a>max_iterations</p>
</td>
<td class="cellrowborder" valign="top" width="9.8989898989899%" headers="mcps1.2.7.1.2 "><p id="p475210694"><a name="p475210694"></a><a name="p475210694"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18.22222222222222%" headers="mcps1.2.7.1.3 "><p id="p207531801297"><a name="p207531801297"></a><a name="p207531801297"></a>最大迭代次数</p>
</td>
<td class="cellrowborder" valign="top" width="9.05050505050505%" headers="mcps1.2.7.1.4 "><p id="p126077114147"><a name="p126077114147"></a><a name="p126077114147"></a>Int</p>
</td>
<td class="cellrowborder" valign="top" width="30.303030303030305%" headers="mcps1.2.7.1.5 "><p id="p19133729890"><a name="p19133729890"></a><a name="p19133729890"></a>1~2000</p>
</td>
<td class="cellrowborder" valign="top" width="18.181818181818183%" headers="mcps1.2.7.1.6 "><p id="p52469671175619"><a name="p52469671175619"></a><a name="p52469671175619"></a>1000</p>
</td>
</tr>
<tr id="row147071213274"><td class="cellrowborder" valign="top" width="14.34343434343434%" headers="mcps1.2.7.1.1 "><p id="p13753301698"><a name="p13753301698"></a><a name="p13753301698"></a>directed</p>
</td>
<td class="cellrowborder" valign="top" width="9.8989898989899%" headers="mcps1.2.7.1.2 "><p id="p27531901695"><a name="p27531901695"></a><a name="p27531901695"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="18.22222222222222%" headers="mcps1.2.7.1.3 "><p id="p1775316016919"><a name="p1775316016919"></a><a name="p1775316016919"></a>是否考虑边的方向</p>
</td>
<td class="cellrowborder" valign="top" width="9.05050505050505%" headers="mcps1.2.7.1.4 "><p id="p1360721111420"><a name="p1360721111420"></a><a name="p1360721111420"></a>Bool</p>
</td>
<td class="cellrowborder" valign="top" width="30.303030303030305%" headers="mcps1.2.7.1.5 "><p id="p13151535595"><a name="p13151535595"></a><a name="p13151535595"></a>true或false</p>
</td>
<td class="cellrowborder" valign="top" width="18.181818181818183%" headers="mcps1.2.7.1.6 "><p id="p22184968175619"><a name="p22184968175619"></a><a name="p22184968175619"></a>true</p>
</td>
</tr>
</tbody>
</table>

>![](public_sys-resources/icon-note.gif) **说明：**   
>-   alpha决定跳转概率系数，也称为阻尼系数，是算法内的计算控制变量。  
>-   convergence定义每次迭代各个点相较于上次迭代变化的绝对值累加和上限，当小于这个值时认为计算收敛，算法停止。  

## 注意事项<a name="section3956161017109"></a>

收敛精度（convergence）设置较大值时，迭代会较快停止。

## 示例<a name="section9539286457"></a>

输入参数source=Lee，alpha=0.85，converage=0.00001，max\_iterations=1000，directed=true，计算结果中的top节点组成的子图会展示在绘图区，节点大小根据PersonalRank值的大小来区别，JSON结果会展示在查询结果区。


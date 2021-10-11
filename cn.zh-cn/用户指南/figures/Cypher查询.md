# Cypher查询<a name="ges_01_0098"></a>

## 操作场景<a name="section1295371733513"></a>

Cypher是一种声明式图查询语言，使用Cypher语句可以查询和修改GES中的数据，并返回结果。

## 操作步骤<a name="section10559841182415"></a>

1.  进入图引擎编辑器页面，详细操作请参见[访问图引擎编辑器](访问图引擎编辑器.md)。
2.  Cypher查询编译过程中使用了基于label的点边索引。第一次使用Cypher查询，您需要单击结果展示区右上角的“建索引“（后续使用不用进行此操作）。

    **图 1**  建索引<a name="fig1529164518214"></a>  
    ![](figures/建索引.png "建索引")

3.  在图数据查询区，输入查询语句，按“回车“键执行操作。

    常用的查询语句如下表所示：

    -   点查询

        match \(n:movie\) return n ：查询label为movie的点。

        match \(n\{Occupation:'artist'\}\) return id\(n\), n.Gender limit 100 ：查询前100个属性Occupation为artist的点，返回其id以及属性值Gender。

        match \(n\) where id\(n\)='Vivian' return n ：查询id为Vivian的点。

        match \(n\) return n skip 50 limit 100 ：查询全图所有的点,跳过前50个，而后返回100个。

    -   边查询

        match \(n\)-\[r\]-\>\(m\) return r, n, m ：查询所有的边，并返回边和边两端的点。

        match \(n\)-\[r:rate\]-\>\(m\) return r, n, m ： 查询label为Rate的边。

        match \(n\)-\[r:rate|:friends\]-\(m\) where id\(n\)='Vivian' return n,r,m ：查询起点为Vivian，边label为rate或friends的所有边。

    -   路径查询

        match p=\(n:user\)--\(m1:user\)--\(m2:movie\) return p limit 100：查询起点label为user，一跳终点为user，二跳终点为movie的路径，并返回前100条。

    -   分组聚集、去重

        match \(n\) return count\(\*\) ：查询全图点的数目。

        match \(n:user\) return n.Gender, count\(n\) ：对label为user的点，统计不同Gender下各有多少点。

        match \(n:user\) return distinct n.Occupation ：对label为user的点，拿到属性值Occupation，并去重。

    -   排序

        match \(n:user\) return id\(n\) as name order by name ：查询label为user的点的id，命名为name，按照name排序。

    -   创建点

        create \(n:movie\{\_ID\_:'中国机长',ChineseTitle: '中国机长', Year:2019\}\) return n ： 创建一个ID为“中国机长”, label为movie，属性值ChineseTitle为“中国机长”, Year为2019的点并返回。

        create \(n:movie\{\_ID\_:'中国机长',ChineseTitle: '中国机长', Year:2019\}\)-\[r:rate\]-\> \(m:movie\{\_ID\_:'攀登者',ChineseTitle: '攀登者', Year:2019\}\) return r ：创建两个点，以及其关联的边。

    -   创建边

        match \(n\),\(m\) where id\(n\)= '中国机长' and id\(m\)= 'Lethal Weapon' create \(n\)-\[r:rate\]-\>\(m\) return r ：给定两个id，创建一条label为rate的边（建议2.2.21及以上版本使用此查询）。

    -   更改属性

        match \(n\) where id\(n\)= '中国机长' set n.ChineseTitle= '《中国机长》' return n ：查找id为“中国机长”的点，修改点的属性值ChineseTitle为“《中国机长》”。

    -   删除点

        match \(n\) where id\(n\)= '中国机长' delete n ：查找id为“中国机长”的点，并删除。

        match \(n\) where id\(n\)= '中国机长' detach delete n ：查找id为“中国机长”的点，删除点以及其关联的边。




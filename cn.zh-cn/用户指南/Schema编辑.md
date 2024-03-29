# Schema编辑<a name="ges_01_0090"></a>

## 添加label<a name="section18163935143214"></a>

在图引擎编辑器左侧的元数据列表中，单击![](figures/6-3-6加号.png)，可增加一个新的标签。

-   Label Name表示新增标签的名字。
-   Label Type中可以选择设置的标签类型（点或边）、颜色和标记（用于区分各个点）。
-   属性添加，默认实体只展示第一个添加的属性，其余不展示，可手动调整展示哪个属性，画布上会实时响应。

    **图 1**  添加label<a name="fig13231182001411"></a>  
    ![](figures/添加label.png "添加label")


## 隐藏label<a name="section23689412344"></a>

-   隐藏单个label的所有点和边

    在图引擎编辑器的左侧的元数据列表中，单击元数据旁的“眼睛”按钮，可隐藏该元数据的所有点和边。

    **图 2**  隐藏label<a name="fig1361815263715"></a>  
    ![](figures/隐藏label.png "隐藏label")


-   隐藏当前选择的label的点和边

    在绘图区，单击图中任意一个点，被选中的点会显示为![](figures/6-3-2.png)。

    -   ![](figures/6-3-3.png)表示label隐藏。在图数据中默认是全部展示的，单击label旁的“眼睛”按钮，可隐藏当前选择的label的点和边（即在画布中不展示或减淡展示）。
    -   ![](figures/6-3-4.png)表示基于label的实体过滤查询，单击该查询按钮，可以将该标签的点和属性过滤显示出来。


## label的导入和导出<a name="section5221105983419"></a>

将当前图的元数据、点边数据集导入到OBS桶内或者从OBS桶内导出。

-   导入：单击元数据列表中“导入“。在弹出的窗口中，选择要导入的元数据，点边数据集，日志储存路径，边处理以及导入类型后，单击“确定“可将数据从OBS桶内导入到当前图中。

    -   日志储存路径：用于存储导入图过程中不符合元数据定义的点、边数据集和详细日志。
    -   边处理：包括“允许重复边”，“忽略之后的重复边”，“覆盖之前的重复边”和“重复边忽略Label”。重复边默认起点和终点相同，当考虑label时，表示边的起点、终点、label相同才为重复边。

    **图 3**  元数据的导入<a name="fig08321571104"></a>  
    

    ![](figures/6-9-2导入.png)

-   导出：单击元数据列表中“导出“。在弹出的窗口中，设置要导出的元数据、点边数据集的名称和导出的路径，单击“确定“可将数据导出到OBS桶内。

    **图 4**  元数据的导出<a name="fig16202182317520"></a>  
    ![](figures/元数据的导出.png "元数据的导出")



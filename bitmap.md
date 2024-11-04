## 存储方式
- 将用户id或者标签值存储到bitmap中
- 当用户id较多时，需要进行bitmap分组，存储两列，bitmap分组值+bitmap(用户id)

## bitmap函数
- bitmap_union：将多个Bitmap的内容合并到一起，去重。通常用于统计和分析所有参与活动或具备某特征的用户列表
- bitmap_union_count：合并去重后求和。通常用于返回用户数
- bitmap_intersect：求多个bitmap的交集。通常用于找到含有多种标签的用户，人群包

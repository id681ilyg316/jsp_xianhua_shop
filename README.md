## 本项目实现的最终作用是基于JSP鲜花商城网站系统
## 分为2个角色
### 第1个角色为管理员角色，实现了如下功能：
 - 客户信息管理
 - 管理员登录
 - 订单管理
 - 鲜花管理
 - 鲜花类目管理
### 第2个角色为用户角色，实现了如下功能：
 - 修改个人信息
 - 加入购物车
 - 提交订单
 - 查看分类
 - 查看热销
 - 查看订单
 - 查看首页
 - 查看鲜花详情
 - 用户登录与注册
## 数据库设计如下：
# 数据库设计文档

**数据库名：** xianhua_shop

**文档版本：** 


| 表名                  | 说明       |
| :---: | :---: |
| [goods](#goods) |  |
| [liuyan](#liuyan) |  |
| [order](#order) |  |
| [orderitem](#orderitem) | 订单详细表 |
| [recommend](#recommend) |  |
| [type](#type) |  |
| [user](#user) | 用户表 |

**表名：** <a id="goods">goods</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | name |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 名字  |
|  3   | cover |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 主图  |
|  4   | image1 |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 图片1  |
|  5   | image2 |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 图片2  |
|  6   | price |   float   | 13 |   0    |    Y     |  N   |   NULL    | 价格  |
|  7   | intro |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 介绍  |
|  8   | stock |   int   | 10 |   0    |    Y     |  N   |   NULL    | 库存  |
|  9   | type_id |   int   | 10 |   0    |    Y     |  N   |   NULL    | 类型ID  |

**表名：** <a id="liuyan">liuyan</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       |   |
|  2   | title |   varchar   | 500 |   0    |    Y     |  N   |   NULL    |   |
|  3   | content |   varchar   | 500 |   0    |    Y     |  N   |   NULL    |   |
|  4   | time |   varchar   | 500 |   0    |    Y     |  N   |   NULL    |   |
|  5   | user |   varchar   | 500 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="order">order</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | total |   float   | 13 |   0    |    Y     |  N   |   NULL    | 总价格  |
|  3   | amount |   int   | 10 |   0    |    Y     |  N   |   NULL    | 下单数量  |
|  4   | status |   tinyint   | 4 |   0    |    Y     |  N   |   NULL    | 状态  |
|  5   | paytype |   tinyint   | 4 |   0    |    Y     |  N   |   NULL    | 支付类型  |
|  6   | name |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 名字  |
|  7   | phone |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 电话  |
|  8   | address |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 地址  |
|  9   | datetime |   datetime   | 19 |   0    |    Y     |  N   |   NULL    | 创建时间  |
|  10   | user_id |   int   | 10 |   0    |    Y     |  N   |   NULL    | 用户ID  |

**表名：** <a id="orderitem">orderitem</a>

**说明：** 订单详细表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | price |   float   | 13 |   0    |    Y     |  N   |   NULL    | 价格  |
|  3   | amount |   int   | 10 |   0    |    Y     |  N   |   NULL    | 数量  |
|  4   | goods_id |   int   | 10 |   0    |    Y     |  N   |   NULL    | 商品ID  |
|  5   | order_id |   int   | 10 |   0    |    Y     |  N   |   NULL    | 订单ID  |

**表名：** <a id="recommend">recommend</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | type |   tinyint   | 4 |   0    |    Y     |  N   |   NULL    | 类型  |
|  3   | goods_id |   int   | 10 |   0    |    Y     |  N   |   NULL    | 商品ID  |

**表名：** <a id="type">type</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | name |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 名字  |

**表名：** <a id="user">user</a>

**说明：** 用户表

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   int   | 10 |   0    |    N     |  Y   |       | 自增主键  |
|  2   | username |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 用户名  |
|  3   | email |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 邮箱  |
|  4   | password |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 密码  |
|  5   | name |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 名字  |
|  6   | phone |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 电话  |
|  7   | address |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 地址  |
|  8   | isadmin |   bit   | 1 |   0    |    Y     |  N   |   NULL    | 是否管理员  |
|  9   | isvalidate |   bit   | 1 |   0    |    Y     |  N   |   NULL    | 是否合法  |

**运行不出来可以微信 javape 我的公众号：源码码头**

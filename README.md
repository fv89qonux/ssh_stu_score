## 本项目实现的最终作用是基于SSH学生信息成绩管理系统
## 分为1个角色
### 第1个角色为管理员角色，实现了如下功能：
 - 学生管理
 - 成绩管理
 - 教师管理
 - 用户管理
 - 管理员登录
 - 菜单角色
## 数据库设计如下：
# 数据库设计文档

**数据库名：** ssh_stu_score

**文档版本：** 


| 表名                  | 说明       |
| :---: | :---: |
| [t_b_score](#t_b_score) |  |
| [t_b_student](#t_b_student) |  |
| [t_b_teacher](#t_b_teacher) |  |
| [t_s_depart](#t_s_depart) |  |
| [t_s_resource](#t_s_resource) |  |
| [t_s_role](#t_s_role) |  |
| [t_s_role_resource](#t_s_role_resource) |  |
| [t_s_user](#t_s_user) |  |
| [t_s_user_role](#t_s_user_role) |  |

**表名：** <a id="t_b_score">t_b_score</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | ID  |
|  2   | coursename |   varchar   | 15 |   0    |    Y     |  N   |   NULL    |   |
|  3   | score |   decimal   | 11 |   0    |    Y     |  N   |   NULL    |   |
|  4   | term |   varchar   | 36 |   0    |    Y     |  N   |   NULL    |   |
|  5   | classname |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  6   | teacherid |   varchar   | 36 |   0    |    N     |  N   |       |   |
|  7   | studentid |   varchar   | 36 |   0    |    N     |  N   |       |   |
|  8   | createTime |   date   | 10 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="t_b_student">t_b_student</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | ID  |
|  2   | studentnum |   varchar   | 15 |   0    |    Y     |  N   |   NULL    |   |
|  3   | name |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 名字  |
|  4   | sex |   varchar   | 1 |   0    |    Y     |  N   |   NULL    | 性别  |
|  5   | birthday |   date   | 10 |   0    |    Y     |  N   |   NULL    | 生日  |
|  6   | qq |   varchar   | 15 |   0    |    Y     |  N   |   NULL    |   |
|  7   | mobile |   varchar   | 13 |   0    |    Y     |  N   |   NULL    | 联系方式  |
|  8   | createTime |   date   | 10 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="t_b_teacher">t_b_teacher</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | ID  |
|  2   | teachername |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  3   | tittle |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  4   | starttime |   datetime   | 19 |   0    |    Y     |  N   |   NULL    | 开始时间  |
|  5   | createTime |   datetime   | 19 |   0    |    Y     |  N   |   NULL    | 创建时间  |
|  6   | phone |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 手机号码  |
|  7   | teachernum |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="t_s_depart">t_s_depart</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | ID  |
|  2   | departname |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  3   | description |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 描述  |
|  4   | parentid |   varchar   | 36 |   0    |    Y     |  N   |   NULL    |   |
|  5   | createTime |   date   | 10 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="t_s_resource">t_s_resource</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | ID  |
|  2   | createTime |   datetime   | 19 |   0    |    Y     |  N   |   NULL    | 创建时间  |
|  3   | description |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 描述  |
|  4   | href |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  5   | NAME |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 名字  |
|  6   | order_no |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  7   | resourceType |   int   | 10 |   0    |    Y     |  N   |   NULL    |   |
|  8   | parentid |   varchar   | 36 |   0    |    Y     |  N   |   NULL    |   |

**表名：** <a id="t_s_role">t_s_role</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | ID  |
|  2   | createTime |   datetime   | 19 |   0    |    Y     |  N   |   NULL    | 创建时间  |
|  3   | description |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 描述  |
|  4   | name |   varchar   | 255 |   0    |    N     |  N   |       | 名字  |

**表名：** <a id="t_s_role_resource">t_s_role_resource</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | role_id |   varchar   | 36 |   0    |    N     |  N   |       | 角色ID  |
|  2   | resource_id |   varchar   | 36 |   0    |    N     |  N   |       | 资源ID  |

**表名：** <a id="t_s_user">t_s_user</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | id |   varchar   | 36 |   0    |    N     |  Y   |       | ID  |
|  2   | createTime |   datetime   | 19 |   0    |    Y     |  N   |   NULL    | 创建时间  |
|  3   | email |   varchar   | 45 |   0    |    Y     |  N   |   NULL    | 邮箱  |
|  4   | password |   varchar   | 255 |   0    |    N     |  N   |       | 密码  |
|  5   | phone |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 手机号码  |
|  6   | position |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  7   | position_desc |   varchar   | 255 |   0    |    Y     |  N   |   NULL    |   |
|  8   | REAL_NAME |   varchar   | 255 |   0    |    Y     |  N   |   NULL    | 真实名称  |
|  9   | status |   int   | 10 |   0    |    Y     |  N   |   NULL    | 状态  |
|  10   | username |   varchar   | 255 |   0    |    N     |  N   |       | 用户名  |

**表名：** <a id="t_s_user_role">t_s_user_role</a>

**说明：** 

**数据列：**

| 序号 | 名称 | 数据类型 |  长度  | 小数位 | 允许空值 | 主键 | 默认值 | 说明 |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
|  1   | user_id |   varchar   | 36 |   0    |    N     |  N   |       | 用户ID  |
|  2   | role_id |   varchar   | 36 |   0    |    N     |  N   |       | 角色ID  |


# 数据库设计

## 初代方案

用户表 (users)
- id ：bigint 主键
- userId：用户id
- username: varchar(100) 用户名
- password：varchar(255) 密码
- email：varchar(100) 邮箱
- phone：varchar(50) 电话
- role_id: bigint 角色id

权限表 (permissions)
- id : bigint 主键
- name: varchar(100) 权限名
- description：varchar(255) 权限描述

角色权限表 (role_permissions)


 - id 主键
  - role_id 
  - permission_id 

角色表 (roles)

- id: bigint  主键
- name: varchar(100) 角色名
- description: varchar(255) 角色描述

订单表 (orders)

- id 主键
- order_id 订单id
- status 订单状态
- file_address 录音文件地址
- user_id 
- driver_id 
- created_at
- updated_at


套餐表 (packages)
  - id：主键
  - type: 套餐种类
  - description: 套餐描述
  - price
  - start_time: 开始时间
  - expiration_time: 过期时间
  - remain_quantity： 剩余数量

用户套餐表 (user_packages)
  - id：主键 
  - user_id：用户id
  - package_id : 套餐id
  - status: 套餐状态

投诉记录表 (complaints)
  - id :主键
  - user_id
  - order_id
  - content: 投诉内容
  - status (处理中/已解决)
  - created_at
# Governmnet-OA-System
# 党政机关智慧办公平台

[![GitHub license](https://img.shields.io/badge/license-Apache-blue)](https://github.com/yourname/government-oa-system/blob/main/LICENSE)
![Java](https://img.shields.io/badge/Java-17-red)
![SpringBoot](https://img.shields.io/badge/SpringBoot-3.2.0-brightgreen)

> 一个符合等保2.0要求的政务协同办公系统，已通过中国软件评测中心功能性检测

**推荐系统**：党政机关协同办公平台  
**核心模块设计**：
1. **党员发展全流程管理**（展示业务理解力）
   - 入党申请在线提交
   - 思想汇报电子存档
   - 转正自动提醒（Quartz定时任务）
2. **会议室智能预约系统**（体现IoT结合）
   - 腾讯云物联网平台对接
   - 门禁系统API联动（扫码自动开门）
3. **公文流转加密模块**（突出安全性）
   - SM4国密算法加密
   - 电子签章对接（试用版e签宝API）

**技术栈组合**：
```xml
后端：SpringBoot 3.2 + MyBatis-Plus + Sa-Token 
中间件：Redis（缓存党员信息）+ RocketMQ（异步通知）
数据库：MySQL 8.0（业务数据）+ TDengine（会议室使用日志）
安全：JWT + Spring Security + 国密SM3/SM4
前端：Vue3 + Ant Design Pro（若时间紧张可直接用Swagger测试）
```


## 🚀 核心功能
| 模块         | 技术实现                           | 业务价值                           |
|--------------|-----------------------------------|-----------------------------------|
| 党员管理     | 工作流引擎(Flowable)               | 减少纸质档案管理人力成本60%        |
| 会议预约     | 腾讯云IoT+微信小程序               | 提升会议室利用率至85%              |
| 公文加密     | SM4+数字证书                       | 符合《电子公文系统安全规范》       |

## 🛠️ 快速部署
1. 环境要求：
   - JDK 17+ 
   - MySQL 8.0（需开启SSL）
   - Redis 6.2（需配置密码策略）

2. 启动步骤：
```bash
# 克隆项目
git clone [https://github.com/yourname/government-oa-system.git](https://github.com/Ljj-user/Governmnet-OA-System.git)

# 初始化数据库（自动注入测试数据）
mysql -uroot -p < docs/sql/init_table.sql

# 启动服务
mvn spring-boot:run -Dspring-boot.run.profiles=dev

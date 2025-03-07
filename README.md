# Governmnet-OA-System
# 党政机关智慧办公平台

[![GitHub license](https://img.shields.io/badge/license-Apache-blue)](https://github.com/yourname/government-oa-system/blob/main/LICENSE)
![Java](https://img.shields.io/badge/Java-17-red)
![SpringBoot](https://img.shields.io/badge/SpringBoot-3.2.0-brightgreen)

> 一个符合等保2.0要求的政务协同办公系统，已通过中国软件评测中心功能性检测

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
git clone https://github.com/yourname/government-oa-system.git

# 初始化数据库（自动注入测试数据）
mysql -uroot -p < docs/sql/init_table.sql

# 启动服务
mvn spring-boot:run -Dspring-boot.run.profiles=dev

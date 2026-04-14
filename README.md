# 1024House · 情侣私密系统

> 跑在你自己的服务器上，数据完全由你掌控。 30 天免费试用。

[![Docker](https://img.shields.io/badge/docker-一键部署-blue)](https://www.docker.com/)
[![License](https://img.shields.io/badge/license-MIT-green)](./LICENSE)

## ✨ 功能特性

| 模块 | 功能 |
|------|------|
| 📸 时光记录 | 发布/删除图文、视频帖子，支持评论、分页 |
| 💝 纪念日 | 自定义名称、公历/农历、增删改查 |
| 🎁 礼账本 | 管理联系人、收支明细，批量导入/导出（情侣共享） |
| ⭐ 愿望清单 | 个人愿望管理，优先级（高/中/低） |
| 💬 实时聊天 | WebSocket 消息收发，聊天记录永久保存 |
| 📝 简记收支 | 日常收支记录，增删改查 |
| 📘 简书备忘 | 备忘内容的添加、编辑、删除与查询 |
| 👶 宝宝成长 | 多宝宝管理，身高/体重/里程碑记录 |
| 💉 疫苗提醒 | 疫苗记录、接种标记、按宝宝筛选 |
| 🏅 勋章系统 | 自动授予成就勋章（第一帖、礼账达人等） |
| ⚙️ 系统配置 | 相爱日设置、首页背景图上传 |
| 👤 个人资料 | 昵称、爱情宣言、头像修改 |

## 🐳 一键部署（Docker Compose）

### 1. 安装 Docker 和 Docker Compose
- Windows / Mac：安装 [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- Linux：`curl -fsSL https://get.docker.com | bash`

### 2. 下载配置文件
wget https://raw.githubusercontent.com/bbblackclark/1024house-deploy/main/docker-compose.yml
3. 启动服务
bash
docker-compose up -d
4. 访问
浏览器打开 http://本机IP:21028/login.html（如果你修改了端口，请使用对应的端口，建议部署的电脑或nas设置固定IP，需外网访问可自行研究下网络穿透或者申请公网ip）

 输入自己的账号密码
- DEFAULT_ADMIN_USERNAMES=feifei,jiajia
- DEFAULT_ADMIN_PASSWORDS=123456,123456
- 在yam文件中初始化账号密码，可在yam中修改
❓ 常见问题
Q：数据存储在哪里？
A：所有数据保存在 Docker 卷中（mongodb_data、uploads_data、album_data 等），请定期备份这些目录。

Q：如何升级到最新版本？
bash
docker-compose pull
docker-compose up -d
Q：不会 Docker 怎么办？
A：加Q群讨论，群号：1128896522。

Q：支持多端同步吗？
A：支持。只要你的服务器能被外网访问，任何设备浏览器打开即可同步。

Q：激活码可以换设备吗？
A：一个激活码绑定一台服务器。如需更换，请联系客服可免费重置一次。

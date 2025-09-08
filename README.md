👉 ### https://www.youtube.com/watch?v=zuLaPkHmmQA&t=980s

⸻

🔗 资源链接（Resources）
 • BTP Trial 注册：https://www.sap.com/products/technology-platform/trial.html
 • 免费短信接收平台：https://wetalkapp.com/receive-sms/
 • Cloud Foundry CLI 下载：https://github.com/cloudfoundry/cli
 • UUID 生成器：https://www.uuidgenerator.net

⚡ 快速开始（复制即用）
1) 登录（美国 US10-001）
https://api.cf.us10-001.hana.ondemand.com/
   登录（新加坡 AP21）
cf login -a https://api.cf.ap21.hana.ondemand.com/

❗ 注意
 • 区域：api.cf.ap21.hana.ondemand.com 为新加坡 AP21微软Azure云；
   api.cf.us10-001.hana.ondemand.com 为美国US10-001亚马逊AWS云；
   其他区域请替换为你子账号的 SAP CF API。

📌📌📌 📌📌📌

======================================

🚀 🚀 🚀 🔹 ：🔹  🚀 🚀 🚀 

✅ 总结：
👉 

🛠️ 🚩🚩🚩实操命令🚩🚩🚩
1. 拉取最新SAPCF加速VPN命令：

cf push APP_NAME --docker-image ghcr.io/uncleluogithub/sapcf:latest -m 512M -k 512M --health-check-type port --no-route --no-start

2. 设置必须的三个环境参数
cf set-env APP_NAME APP_UUID 你的UUID替换这里
cf set-env APP_NAME VMESS_HOST 你的cloudflare隧道域名替换这里
cf set-env APP_NAME  TUNNEL_TOKEN '你的隧道TOKEN替换这里'

3. 再确认端口健康检查类型
cf set-health-check APP_NAME  port

4. 启动APP
cf start APP_NAME

5. 查询节点信息（日志信息查看）
cf logs APP_NAME --recent

• 配额：Trial 内存有限，建议 -m 512M 起步。
• UUID：务必唯一

🔔 👍📌 🔔

❓ FAQ
 • Trial 会不会每天自动停？→ CF Trial 可能休眠/停机，可配保活/自动拉起

⚖️ 合规与声明
本视频仅用于学习实验与隐私保护；请遵守所在地法律法规与平台条款；严禁用于任何违法、侵权或绕过授权的行为。

鲸鲸的小屋 — PWA 网页版（可装到手机桌面）
==========================================

这是一个纯前端页面，不需要服务器、不需要数据库。
上传到任何静态托管（需要 HTTPS）后，手机上可以"添加到主屏幕"，
像一个独立 App 一样全屏打开，第二次起离线也能用。


文件清单（必须放在同一目录）
----------------------------
index.html      页面本体
three.min.js    3D 渲染引擎
manifest.json   PWA 清单（名字、图标、全屏模式）
sw.js           离线缓存
icon-192.png    应用图标
icon-512.png    应用图标（大）
idle.webm       待机动画
run.webm        走路动画
jump.webm       跳跃动画
think.webm      发呆动画
eat.webm        吃东西动画
sleep.webm      睡觉动画
README.txt      本文件


上传（任选一个，都免费）
------------------------
1) Cloudflare Pages   ← 推荐，国内访问较稳
   dash.cloudflare.com → Pages → Create a project → Direct Upload
   把本文件夹整个拖进去，发布后得到 https://xxx.pages.dev

2) Netlify
   app.netlify.com/drop → 拖文件夹 → 立刻得到地址

3) GitHub Pages
   新建仓库 → 上传这 13 个文件 → Settings → Pages → 选 main → 保存


手机上"安装"成 App
------------------
1. 手机浏览器打开你的 https 地址（必须 HTTPS，PWA 才生效）
2. Android Chrome：右上角菜单 → "安装应用" / "添加到主屏幕"
   iPhone Safari：底部分享 → "添加到主屏幕"
3. 桌面上会出现猫头图标，点开是全屏、没有地址栏

装完之后：
- 第一次打开需要联网加载，之后缓存在本地，断网也能开
- 想更新内容，重新上传一次，手机上再打开会自动更新缓存


操作说明
--------
手机上：
  点地面      她走过去
  拖白猫      换位置，放床上/桌上它会待着
  双击白猫    回地面
  底部按钮    自己乱走 / 白猫 / 关灯

电脑上额外支持：
  WASD 走动 · Shift 跑 · Space 蹦 · E 发呆 · Q 吃饭


时间
----
页面用访客本地时间：
23:30 之后她会自己走到床上睡觉，早上 6:30 起床。
想随时看睡觉的样子，网址后面加 ?night=1


想要真正的 APK
--------------
本目录已经是标准 PWA，可以用 PWABuilder 免费转成 APK：
  1. 先把本目录上传，拿到 https 地址
  2. 打开 pwabuilder.com，输入地址
  3. 选 Android → 生成 APK / AAB，下载安装包

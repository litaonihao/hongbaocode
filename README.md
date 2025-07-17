# hongbaocode
Telegram电报tg红包雷,最新电报tg红包雷,,USDT红包扫雷机器人,最新USDT红包扫雷机器人,红包扫雷机器人源码--自助充值、提现 全功能完整版 多语言 全网最全 假人自动抢包 最新源码
1、安装运行环境（nginx，mysql5.7,php8.0，redis,supervisor)
1.1 宝塔创建lavavel项目教程：https://www.bt.cn/bbs/thread-72066-1-1.html
1.2 php安装redis,imagemagick扩展
1.3  删除禁用函数putenv,proc_open,pcntl_signal,pcntl_alarm后续如果有提示其他禁用函数要删除，
2、导入数据库，后台默认账号密码admin/admin123
3、上传代码，（如果没有vendor,安装扩展，命令composer install)，
（如果没有.env，可以将.env.example改为.env）
目录权限记得设置为www
3.1配置.env中的数据库信息
机器人token：TELEGRAM_BOT_TOKEN和TELEGRAM_WEBHOOK_URL
TELEGRAM_WEBHOOK_KEY可以随便填，改完同时要修改TELEGRAM_WEBHOOK_URL中的相对于的部分，例如，https://xxx.xxx.com/api/abcdef123/webhook中（abcdef123）
3.2如果配置了域名https，ADMIN_HTTPS前面的#要去掉，设置域名：ADMIN_HTTPS=https://xxx.com

4、配置站点
根目录，运行目录public，ssl，伪静态选择laravel
5、后台添加群组，配置相关参数
6、修改红包图片：获取图片:发送图片给机器人可以获取到id，填入群组中的图片id则修改红包图片
7、邀请自动注册：
浏览器访问以下链接：（{机器人token} 改为你的token）
https://api.telegram.org/bot{机器人token}/getUpdates?allowed_updates=["message","edited_message","channel_post","chosen_inline_result","shipping_query","pre_checkout_query","poll","poll_answer","edited_channel_post","callback_query","chat_member","inline_query","my_chat_member","chat_member"]
访问完关掉即可
8、配置机器人 webhook（如果不设置webhook,则命令行在项目目录运行php artisan message）
命令：
php artisan nutgram:hook:set {url}
例如：php artisan nutgram:hook:set https://www.xxx.com/api/xxxx/webhook

移除：php artisan nutgram:hook:remove
9、设置supervisor进程
>目录选择源码目录，用户选择www
购买加安装联系@tg:https://t.me/xitongchu   @xitongchu

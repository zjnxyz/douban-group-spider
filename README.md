# 说明
用于爬取`豆瓣小组`的爬虫。
此爬虫我主要用于了爬取`豆瓣租房小组`的帖子，支持`关键字`搜索以及发帖、更新时间排序。

# 依赖
- gevent
- pymongo
- requests
- lxml
- Flask
具体版本参见`requirements.txt`
前端使用了`boostrap`模板。

# 特别说明
由于豆瓣有防抓机制，故此爬虫使用了代理爬取，防止被封IP。
可从网上收集代理IP，放在项目路径下`proxy_list.txt`，每个一行，程序会自动加载，且可以自动定时加载新代理。
或者参考我的[代理采集器](https://github.com/kaito-kidd/proxy-fetcher)，自动采集代理。

# 使用
- 安装`MongoDB`，具体参考安装文档。
- 建议使用`virtualenv`环境
    pip install -r requirements.txt`
- 启动爬虫
    nohup python spider >> douban_spider.log &
- 启动后台服务
    nohup python app.py >> app.log &
- 查看页面
    http://localhost:5000

# 配置
参数配置见`config.py`，例如`MongoDB地址`、`并发数`、`爬取页数`等。

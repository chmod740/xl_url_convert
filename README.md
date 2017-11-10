# xl_url_convert
迅雷下载地址转换库（Python3）by hupeng
## 0.环境要求 
Python3.5及以上

## 1.安装
命令行输入：
```cmd
pip install xl-url-convert
```

## 2.使用
调用样例1：
```python
from xl_url_convert import download_address_translation
address = download_address_translation("https://www.baidu.com/robots.txt")
print("原始格式链接:" + address.origin)
print("迅雷格式链接:" +address.thunder)
print("qq旋风链接:" + address.qqdl)
```
输出样例1：
> 原始格式链接:https://www.baidu.com/robots.txt<br>
> 迅雷格式链接:thunder://QUFodHRwczovL3d3dy5iYWlkdS5jb20vcm9ib3RzLnR4dFpa<br>
> qq旋风链接:qqdl://aHR0cHM6Ly93d3cuYmFpZHUuY29tL3JvYm90cy50eHQ=

调用样例2：
```python
from xl_url_convert import download_address_translation
address = download_address_translation("thunder://QUFodHRwOi8vZGwxNTAuODBzLmltOjkyMC8xNzEwL1vlkI3kvqbmjqLmn6/ljZdd56ysODkw6ZuG77ya6K+V6KGj6Ze055qE5q276KeS77yI5LiK6ZuG77yJL1vlkI3kvqbmjqLmn6/ljZdd56ysODkw6ZuG77ya6K+V6KGj6Ze055qE5q276KeS77yI5LiK6ZuG77yJX2JkLm1wNFpa")
print("原始格式链接:" + address.origin)
print("迅雷格式链接:" +address.thunder)
print("qq旋风链接:" + address.qqdl)
```

输出样例2：
> 原始格式链接:http://dl150.80s.im:920/1710/[名侦探柯南]第890集：试衣间的死角（上集）/[名侦探柯南]第890集：试衣间的死角（上集）_bd.mp4<br>
> 迅雷格式链接:thunder://QUFodHRwOi8vZGwxNTAuODBzLmltOjkyMC8xNzEwL1vD+9XszL2/wsTPXbXaODkwvK+jusrU0sK85LXEy8C9x6Ooyc+8r6OpL1vD+9XszL2/wsTPXbXaODkwvK+jusrU0sK85LXEy8C9x6Ooyc+8r6OpX2JkLm1wNFpa<br>
> qq旋风链接:qqdl://aHR0cDovL2RsMTUwLjgwcy5pbTo5MjAvMTcxMC9bw/vV7My9v8LEz1212jg5MLyvo7rK1NLCvOS1xMvAvcejqMnPvK+jqS9bw/vV7My9v8LEz1212jg5MLyvo7rK1NLCvOS1xMvAvcejqMnPvK+jqV9iZC5tcDQ=

**通过两个样例可以看到，这个库可以适配不同的下载地址,并导出不同的下载地址**

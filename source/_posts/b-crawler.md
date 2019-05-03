---
title: BeautifulSoup简单使用
date: 2019-04-29 23:50:45
categories: Python
tags: [Python,第一次随便写写]
---
# BeautifulSoup简单使用 ~~（其实只是试试博客啦）~~
#### 一、先导入BeautifulSoup包
from bs4 import BeautifulSoup
#### 二、使用时新建一个BeautifulSoup对象，使用html解析器
soup = BeautifulSoup(<内容>, 'html.parser')
#### 三、常用方法
##### 1、soup.find（）
该方法只能找第一次出现的标签
> soup.find('ul')  
> 查找==标签名==为'ul'的标签  
> soup.find(text='plants')  
> 查找==文本==为'plants'的标签  
>soup.find(id='abc')  
>查找==id==为abc的标签

---

注：访问一个标签内的属性时,如‘herf’
```
<a href="www.xxx">textContent</a>
```
可用a.get('herf')~~/a.attrs[href]~~ 获取

至于标签中的文本，则用a.get_text()~~/a.text~~ 获取  



##### 2、find_all()
用法同上，但可找到符合条件的全部标签，放在一个列表里


#### 四、总结
通过以上方法，则一层层下来，就可以按照html结构用find()&find_all()来获取想要的内容了！~~（也许吧。。）~~
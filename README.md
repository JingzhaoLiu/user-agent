# python 

python爬虫的伪装浏览器头部.

## 使用 


``` python
import urllib.request
import random
from user_agents import agents

print(random.choice(agents))

def url_open(url): 
    '''请求网址用浏览器代理，获得网页内容'''
    req = urllib.request.Request(url)

    req.add_header(
        'User-Agent',
        random.choice(agents)
    )

    response = urllib.request.urlopen(req)
    html = response.read()
    return html


```
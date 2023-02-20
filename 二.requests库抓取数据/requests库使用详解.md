![图灵logo](requests库抓取数据/图灵logo.png)



## requests库的使用  

其他库  urllib   urlib3

请求转换网址： https://curlconverter.com/

```python
"""
def request(method, url,
            params=None, data=None, headers=None, cookies=None,
            auth=None, timeout=None, allow_redirects=True, proxies=None,
           verify=None, json=None):
"""
import requests
#添加请求头
url="http://httpbin.org/get"
headers = {
    'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/107.0.0.0 Safari/537.36',
}
res=requests.get(url=url,headers=headers)
print(res.text)

#添加请求参数
url="http://httpbin.org/get"
params={"key1":"value1","key2":"value2"}#请求参数
res=requests.get(url=url,params=params)
print(res.text)

#添加cookie
url="http://httpbin.org/get"
cookies={"BIDUPSID":"46FEC0FB22FD5A4E7B5B2A17994EC2EA"}
res=requests.get(url,cookies=cookies)
print(res.text)

# 重定向   超时时间
import  requests
url="http://github.com"
res=requests.get(url,allow_redirects=True,headers=headers,timeout=20)
# res_gh=requests.get(url,allow_redirects=False,headers=headers,timeout=20)
print(res.text)
print(res.status_code)

#代理ip
url="http://httpbin.org/get"
proxies={"http":"175.10.24.14:8888","https":"175.10.24.14:8888"}#示例代理ip
res=requests.get(url,proxies=proxies)
print(res.text)


#post请求  表单数据
import requests
data={"data1":"spider","data2":"验证数据"}#form 表单数据 
url="http://httpbin.org/post"
res=requests.post(url,data=data)
print(res.text)

#post请求   json数据
json={"json_style":"json-data"}#json
url="http://httpbin.org/post"#测试url
res=requests.post(url,json=json)
print(res.text)

# 忽略证书验证
requests.urllib3.disable_warnings()#忽略warnning
url="https://ssr2.scrape.center/"
res=requests.get(url,verify=False)
print(res.text)

#响应对象的操作
print(res.headers)          #响应头
print(res.request.headers)  #请求头
print(res.url)              #url
print(res.content)          #字节形式， 媒体文件
print(res.text)             #字符串
```


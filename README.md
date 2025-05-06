### 申请公众号测试账户

使用微信扫码即可
https://mp.weixin.qq.com/debug/cgi-bin/sandbox?t=sandbox/login

进入页面以后我们来获取到这四个值 
#### appID  appSecret openId template_id
![image](https://github.com/tech-shrimp/FreeWechatPush/assets/154193368/bdb27abd-39cb-4e77-9b89-299afabc7330)

想让谁收消息，谁就用微信扫二维码，然后出现在用户列表，获取微信号（openId）
 ![image](https://github.com/tech-shrimp/FreeWechatPush/assets/154193368/1327c6f5-5c92-4310-a10b-6f2956c1dd75)

新增测试模板获得  template_id（模板ID）
 ![image](https://github.com/tech-shrimp/FreeWechatPush/assets/154193368/ec689f4d-6c0b-44c4-915a-6fd7ada17028)

模板标题随便填，模板内容如下，可以根据需求自己定制

模板内容：
```copy
今天：{{date.DATA}} 
地区：{{region.DATA}} 
天气：{{weather.DATA}} 
气温：{{temp.DATA}} 
风向：{{wind_dir.DATA}} 
对你说的话：{{today_note.DATA}}
```

### 项目配置 
Fork本项目
进入自己项目的Settings  ----> Secrets and variables ---> Actions --> New repository secret
配置好以下四个值（见上文）

<img width="590" alt="image" src="https://github.com/tech-shrimp/GithubActionSample/assets/154193368/9e6b799d-9230-4d3e-8966-6c6f49e9b89f">

进入自己项目的Action  ----> 天气预报推送 ---> weather_report.yml --> 修改cron表达式的执行时间
<img width="503" alt="image" src="https://github.com/tech-shrimp/GithubActionSample/assets/154193368/badcc0fa-def5-428f-9238-fa6b549baefc">


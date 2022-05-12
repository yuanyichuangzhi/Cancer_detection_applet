# Cancer_detection_applet
这是一个癌症检测小程序，通过PaddlePaddle训练模型，并使用PaddleJS部署到微信小程序，面向所有人提供癌症检测服务
PaddleJsInWechat
运用paddlejs的微信小程序模板，开箱即用

项目预览


部署准备
注册一个微信小程序
开通云开发，并获得云开发code
准备好你的paddlejs模型
模型训练教程https://aistudio.baidu.com/aistudio/projectdetail/807809

部署流程
克隆项目
git clone https://github.com/sovlookup/PaddleJsInWechat

修改配置
app.js第5行填写云开发code
project.config.json第36行修改你的appid
<可选>pages/detail和pages/gallery的wxml文件中修改页面，模板只显示样本的name
<可选>使用服务器预测功能填写pages/index/index.js 119行接口地址并修改接口函数
部署模型
建立两条记录一条为model，记录模型元信息 
字段名称	字段内容
categories	类别数量
filecount	paddlejs模型分片数
files	模型分片名称
map	模型输出与预测对象的映射
modelurl	模型下载URL地址
name	这个字段不要修改
version	模型版本，小程序每次启动都会检测更新
一条为parrots，这里放你的识别的物品信息，字段结构除了name可以自行修改 
注意点：
调试基础库版本 >= 2.13.1
TODO：
 优化显示过度动画
 worker 预测

### 注意 ###

**加以区分，Autoapi-test为旧版（有大bug，项目名字为这个的，必须更新），AutoApi 、AutoApiSecret、AutoApiSR、AutoApiS为新版（项目名字为这两个的，无bug，不用更新）**

* 更新 4-30-20(00:00)
  * AutoApiS超级版正式发布
  
* 修复 3-26-20(01:00)
  * 修复AutoApiSR时差问题
  
         github服务器与中国时间有时差，导致AutoApiSR脱离设计本意(修改位置：autoapi.yml里的schedule，9,13,16改成了1,5,8)
* 小更新 3-21-20(19:00)
  * 增加模仿人为开发版
       
         分离refresh_token更新与api调用
* 重大更新 3-8-20(23:00)
  * 1 ，修复了一个不为人知的超大bug

         修复无法复写刷新refresh_token。 （旧版autoapi-test的问题）
  * 2 ，增加加密版。
-------------------
# 请跳转：
* 普通版项目地址：https://github.com/wangziyingwen/AutoApi
* 加密版项目地址：https://github.com/wangziyingwen/AutoApiSecret
* 模仿人为开发版：https://github.com/wangziyingwen/AutoApiSR
* 超级版地址: https://github.com/wangziyingwen/AutoApiS

### 区别 ###
   [普通版（弃用）](https://github.com/wangziyingwen/AutoApi)：密钥暴露，不在乎的话可以使用
   
   [加密版（推荐）](https://github.com/wangziyingwen/AutoApiSecret)：应用id机密加密隐藏，提高安全性

   [模仿人为应用开发版（半弃用）](https://github.com/wangziyingwen/AutoApiSR)：顾名思义，加密版的升级版。由于超级版兼容模拟版的功能，此版本处于一种尴尬位置。（当然也可以正常使用）
   
   [超级版（不建议）](https://github.com/wangziyingwen/AutoApiS)：进一步升级版，增加自定义参数、模式。按目前情况，微软续订要求很低，暂时不需要使用此项目。

### 最后 ###
有修改建议可以发邮件给我:
wz.lxh@outlook.com
  
基安id-卷腿毛菌

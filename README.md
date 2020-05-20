
### 问题 ###

**部署过程中**出错：

1，提示 refresh_token 错误之前
       
       原因：refresh格式错误、设置里的id/机密位置混乱了

       解决办法：首先确认设置secret里的id、机密是否填对位置。然后用rclone重新获取refresh_token替换1.txt，注意末尾不要有**空格/空行**。

2，提示 *** 错误
       
       原因：设置secret里，config_id/config_key格式错误

       解决办法：详细看readme，注意格式，删除并新建config_id跟config_key。

3，api数缺少
     
       解决办法：首先，查看api赋权是否正确（s版请按readme的api权限授权），是否“代表管理员授权”。
               
               再，确保onedrive已成功初始化/激活，还没就等。

**正常运行后的**出错

1，之前正常运行，莫名其妙出错 并 提示 refresh_token 错误

      原因：不明，出现几率很低。应该是微软方面的问题，触发了某种安全策略？token库存满了？导致token过期失效。
      
      解决办法：1，如果有备份应用id跟机密的：用rclone重新获取token替换1.txt

               2，没有备份的：回到azure（注册应用的那个网页）里找到之前注册的应用，找到应用id；机密需要新建一个。然后用rclone获取token替换一下。
               
2，不自动运行

      原因：不明，只在autoapiSR版出现。（我自己新建小号测试是可以的，奇怪。。。）
      
      解决办法：删掉再部署一遍
           
              还不行，建议放弃SR版。坚持要用的话，自己新建项目，然后把SR版的代码上传上去，肯定就行了。

------------------

### 更新日志 ###

**加以区分，Autoapi-test为旧版（有大bug，项目名字为这个的，必须更新），AutoApi 、AutoApiSecret、AutoApiSR、AutoApiS为新版（项目名字为这两个的，无bug，不用更新）**

* 更新 4-30-20(00:00)
  * AutoApiS超级版正式发布
  
* 修复 3-26-20(01:00)
  * 改善AutoApiSR时差问题
  
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

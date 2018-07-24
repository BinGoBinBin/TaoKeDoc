##阿里妈妈API  

淘宝客商品详情、淘宝客优惠券、淘口令的生成和解密、s.click地址解密商品id

**1.获取商品详情**  

* taoke/api/tao/v1/info?pid={商品Id}&uid={用户Id}

**2.获取商品链接信息**   

* taoke/api/tao/v1/item?pid={商品Id}&uid={用户Id} 

**注意**
> 1. 如果该商品有优惠券，则返回优惠券地址+商品的转链地址（该地址无优惠券）；
> * 如果该商品无优惠券，则仅仅返回链接地址，该地址自动申请定向计划最高佣金。如果该商品是鹊桥，则无法获取鹊桥的佣金，仅仅是普通佣金；
> * 该接口对普通商品，自动申请定向计划最高佣金。

**3.淘口令生成**

* taoke/api/tao/v1/kouling?pid={商品id}&uid=123 
* GET请求

**注意**
> 1.如果该商品有优惠券，则返回优惠券地址对应的淘口令；  
> 2.如果该商品无优惠券，则返回该商品普通推广链接对应的淘口令。

**4.淘口令解析**

* taoke/api/tao/v1/kouling
* POST请求
* 参数：{"uid":"123","text":"你的淘口令"}
* 返回淘口令对应商品的商品Id

**5.根据推广链接，优惠券地址查询对应商品的Id**

* taoke/api/tao/v1/urlparse?uid=123&url=https://s.click.xxxx
* GET请求
* url参数只用URLEncoder进行编码
* 返回该地址对应的商品Id


其它API正在开发中，coming soon...

测试uid=123，大家可以先测试。如果有需要使用请企鹅联系:493619247

####使用API的时候请大家尽量缓存相关数据，避免你的API请求次数被后妈限制
####免费使用。请求栗子：[http://api.520pikachu.cn/taoke/api/tao/v1/item?pid=552458923357&uid=123](http://api.520pikachu.cn/taoke/api/tao/v1/item?pid=552458923357&uid=123)
##阿里妈妈API  

淘宝客商品详情、淘宝客优惠券、淘口令的生成和解密、s.click地址解密商品id

**获取商品详情**  

* taoke/api/tao/v1/info?pid={商品Id}&uid={用户Id}

**获取商品链接信息**   

* taoke/api/tao/v1/item?pid={商品Id}&uid={用户Id} 

> 1. 如果该商品有优惠券，则返回优惠券地址+商品的转链地址（该地址无优惠券）；
> * 如果该商品无优惠券，则仅仅返回链接地址，该地址自动申请定向计划最高佣金。如果该商品是鹊桥，则无法获取鹊桥的佣金，仅仅是普通佣金；


其它API正在开发中，coming soon...

测试uid=123，大家可以先测试。如果有需要使用请企鹅联系:493619247

####免费使用。请求栗子：[http://api.520pikachu.cn/taoke/api/tao/v1/item?pid=552458923357&uid=123](http://api.520pikachu.cn/taoke/api/tao/v1/item?pid=552458923357&uid=123)
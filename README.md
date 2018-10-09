# SeckillPro<br/>
描述：秒杀活动，模拟<br/>
架构：mvc+webapi+console+redis，netcore开发<br/>
线上效果地址：http://www.lovexins.com:3333<br/>
架构设计图如下：
<hr/>
<img src="http://files.cnblogs.com/files/wangrudong003/%E7%A7%92%E6%9D%80%E8%AE%BE%E8%AE%A11.gif"/>
<hr/>
<img src="http://files.cnblogs.com/files/wangrudong003/%E7%A7%92%E6%9D%80%E8%AE%BE%E8%AE%A12.gif"/>
<hr/>
<img src="http://files.cnblogs.com/files/wangrudong003/%E7%A7%92%E6%9D%80%E8%AE%BE%E8%AE%A13.gif"/>

 SeckillPro.Web：面向用户的web站点，主要提供商品展示，秒杀抢购，抢购结果，订单列表等功能；

 SeckillPro.Api：主要处理秒杀活动的请求，然后加入到秒杀队列中，以及订单状态的查询接口；

 SeckillPro.Server：处理秒杀队列的服务；根据Redis模糊匹配key的方式，开启多个商品秒杀的任务，并处理秒杀请求和改变订单抢购状态；

 SeckillPro.Com：集成公共的方法；这里面前有操作Redis的list，hash，string的封装类；

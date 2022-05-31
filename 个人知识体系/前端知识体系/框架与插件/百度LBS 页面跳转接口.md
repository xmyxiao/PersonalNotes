**百度LBS 页面跳转接口**</br>
　　地址: <http://developer.baidu.com/map/wiki/index.php?title=uri/api/web></br>
　　参考地址：<http://www.tuicool.com/articles/BVzI73></br>
　　地图详细接口：<http://developer.baidu.com/map/jsdemo.htm#a1_2></br>

　　引用：</br>

```javascript
<script type="text/javascript" src="http://api.map.baidu.com/api?ak=165c70fb6496adae904f0f43e7f98dc5&v=2.0&services=false"></script>
```

　　使用: </br>

```javascript
<a href="http://api.map.baidu.com/geocoder?address=福建省福州市仓山区冠浦路142&amp;output=html" target="_blank"><img type="location" style="width:250px; height:250px;" src="http://api.map.baidu.com/staticimage?&#10;&#9;&#9;&#9;&#9;width=250&amp;height=250&amp;zoom=16&amp;center=福建省福州市仓山区冠浦路142"></a>
```

　　展示小图 点击跳转百度地图 address=要定位的地址 output=html必须 否则无法打开</br>
　　zoom=16 级别可使用3-18数值越大地图放大级数越大</br>
　　`&#10;&#9;&#9;&#9;&#9 &amp` 为HTML特殊字符 符号不可去除</br>
　　usionconfig项目下的map页面为实例</br>

```javascript
 (function(global){
   var mapPage;
   mapPage = global.mapPage = {};
   mapPage = {
     map:null,
     gc:null
   }
 })(this);
```

　　先设置全局变量  在地图的使用中多数地方使用到了全局变量</br>
　　mapPage.map = new BMap.Map("container");//在指定的容器内创建地图实例</br>
　　mapPage.gc = new BMap.Geocoder();  //新建一个地址解析类</br>

```javascript
 mapPage.gc.getLocation(e.point, function(rs){
  showLocationInfo(e.point, rs);
 });
```

　　e.point为位置的经纬度信息  rs为地点的详细位置信息</br>
　　mapPage.map.clearOverlays();清除地图覆盖物</br>

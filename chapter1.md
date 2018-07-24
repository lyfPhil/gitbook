# 地图叠加层

### 叠加层

* 点   标记是 Gmarker类型的对象,可以用GIcon 类型的对象自定义
* 线   折线是GPolyline 类型的对象
* 区域   闭合的折线
* 地图本身是使用图块叠加层显示  GTileLayerOverlay
* 信息窗口是一种特殊的叠加层

### Google 地图 - 添加标记

* 设定经纬度

```
var myCenter = new google.maps.LatLng(纬度,经度);
```

* 实例化Marker对象

```
var marker = new google.maps.Marker({
    position:myCenter,
});
```

* 在地图上添加标记  \(map为Map对象\)

```
marker.setMap(map);
```

* 动画的标记   BOUNCE 弹跳

```
var marker = new google.maps.Marker({
    position:myCenter,
    animation:google.maps.Animation.BOUNCE
});
```

* 自定义图标

```
var mark = new google.maps.Marker({
    position:myCenter,
    icon:'1.png'
})
```

### Google 地图 - 添加折线

Polyline对象

```
var myTrip = [1,2,3];  //1,2,3 设置过经纬度

var flightPath = new google.maps.Polyline({
    path:myTrip,
    strokeColor:'#0000FF',
    strokeOpacity:0.8,
    strokeWeight:2,
    editable:true/false,
});

flightPath.setMap(map);
```

### Google 地图 - 多边形

Polygon对象

```
var myTrip = [1,2,3,1];

var flightPath = new google.maps.Polygon({
      path:myTrip,
      strokeColor:"#0000FF",
      strokeOpacity:0.8,
      strokeWeight:2,
      fillColor:"#0000FF",
      fillOpacity:0.4
});

flightPath.setMap(map);
```

### Google 地图 - 圆

Circle对象

```
var myCity = new google.maps.Circle({
  center:amsterdam,  //圆中心参数
  radius:20000,      //半径,米
  strokeColor:"#0000FF",
  strokeOpacity:0.8,
  strokeWeight:2,
  fillColor:"#0000FF",
  fillOpacity:0.4
});

myCity.setMap(map);
```

### Google 地图 - 信息窗口

```
var infowindow = new google.maps.InfoWindow({
    content:"Hello World!"
});

infowindow.open(map,marker);
```




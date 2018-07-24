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








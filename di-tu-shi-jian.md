# Google 地图事件

### 点击事件

标记marker点击后触发改变属性事件

```
google.maps.event.addListener(marker,'click',function(){
    map.setZoom(9);
    map.setCenter(marker.getPosition());
});
```

标记marker点击后触发打开信息窗口事件

```
var infowindow = new google.maps.InfoWindow({
    center:"hello world"
});

google.maps.event.addListener(marker,'click',function(){
    infowindow.open(map,marker);
});
```

### change事件

中心点改变后触发

```
google.maps.event.addListener(map,'center_changed',function() {
  window.setTimeout(function() {
    map.panTo(marker.getPosition());
  },3000);
});
```




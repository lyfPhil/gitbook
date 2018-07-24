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

点击地图上的点后调用其他函数,显示点的位置信息

```
function initialize(){
    google.maps.event.addListener(map,'click',function(event){
        placeMarker(event.latLng);
    });
}

function placeMarker(location){
    var marker = new google.maps.Marker({
        position:location,
        map:map,
    });
    var infowindow = new google.maps.InfoWindow({
        content="经度:"+location.lat()+"纬度"+location.lng();
    });
    infowindow.open(map,marker);
}
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




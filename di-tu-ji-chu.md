1. 声明HTML    &lt;!DOCTYPE html&gt;
2. 添加API key   &lt;script src="[http://maps.googleapis.com/maps/api/js?key=\*\*YOUR\_API\_KEY\*\*&sensor=\*\*TRUE\_OR\_FALSE\*\*"&gt;&lt;/script](http://maps.googleapis.com/maps/api/js?key=**YOUR_API_KEY**&sensor=**TRUE_OR_FALSE**"></script&gt)&gt;;
3. 定义地图属性  center\(中心点\)  zoom \(缩放级数\)  mapTypeId\(地图初始类型\)
4. 地图显示位置  &lt;div id="googleMap"&gt;&lt;/div&gt;
5. 实例化Map类 var map = new google.maps.Map\(\)
6. 加载地图  google.maps.event.addDomListener\(window, 'load', innitialize\);

例子:

```
<!DOCTYPE html>
<html>

<head>
<script src="http://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&sensor=TRUE_OR_FALSE"></script>
<script>
function initialize()
{
    var mapProp = {
        center:new google.maps.LatLng(51.508742,-0.120850),
        zoom:5,
        mapTypeId:google.maps.MapTypeId.ROADMAP
    };
    var map=new google.maps.Map(document.getElementById("googleMap"), mapProp);
}

google.maps.event.addDomListener(window, 'load', initialize);
</script>
</head>

<body>

 <div id="googleMap" style="width:500px;height:380px;"></div>

</body>
</html>
```




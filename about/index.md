---
layout: page
title: 课题组介绍

---
* content
{:toc}

袁增伟教授课题组位于南京大学仙林校区环境学院 (见 <a href="#map" 
class="page-scroll">地图如下</a> 导航)。您可以在南京市乘坐地铁二号线，往经天路方向，倒数第二站即可到达，交通十分便捷。

 
### 研究领域

课题组主要从事环境规划与管理研究，致力于人类活动的资源和环境效应评估，重点开展多尺度营养物质和重金属循环过程模拟，阐释其时空格局演变规律和驱动机制，并定量评估其资源和环境效应，为系统调控人类活动和推动区域可持续发展提供决策依据。

### 主要研究方向

多源环境数据融合与同化

多尺度氮磷循环及其环境效应

磷资源开发利用过程含磷废物资源化技术

### 主要技术咨询业务

污染防治/环境保护/生态文明/循环经济规划

企业清洁生产/能源审计方案
       
环境风险评估/应急预案编制

其他环境规划与管理咨询

### 研究手段与方法

遥感（RS）
     
地理信息系统（GIS）

物质流分析（SFA）

生命周期评价（LCA）

数据挖掘（DM）

清单分析（EIA）

成本-效益分析（CBA）

GaBi6.0数据库平台。

### 发展历程

2002年10月，毕军教授怀着对祖国日益严峻的环境污染形势的担忧和对我国环境保护事业的满腔热情，辞去在世界银行的工作回到南京大学，开始致力于中国环境规划与管理领域的研究和实践。从2002年到2013年，伴随着国家环境问题的变化和环境管理战略的调整，毕军教授带领其研究团队先后开展了产业生态学与循环经济、环境管理与经济政策、环境风险预警与应急管理、能源环境与低碳发展等领域研究。2013年12月，为推动学科精细化发展和跨学科研究，毕军教授将团队中原有的四个研究方向进一步整合为清洁空气与环境健康、物质循环及其环境效应两个方向，本课题组正是在原产业生态学与循环经济基础上形成和发展起来的物质循环及其环境效应方向。

### 发展目标

培养创新型环境规划与管理人才。

### 地图
---

<section id="map" class="map">
   <meta http-equiv="Content-Type" content="text/html; charset=gb2312" />
<style type="text/css">
    html,body{margin:0;padding:0;}
    .iw_poi_title {color:#CC5522;font-size:14px;font-weight:bold;overflow:hidden;padding-right:13px;white-space:nowrap}
    .iw_poi_content {font:12px arial,sans-serif;overflow:visible;padding-top:4px;white-space:-moz-pre-wrap;word-wrap:break-word}
</style>
<script type="text/javascript" src="http://api.map.baidu.com/api?key=&v=1.1&services=true"></script>
<div style="width:100%px;height:500px;border:#ccc solid 1px;" id="dituContent"></div>
<script type="text/javascript">
    //创建和初始化地图函数：
    function initMap(){
        createMap();//创建地图
        setMapEvent();//设置地图事件
        addMapControl();//向地图添加控件
        addMarker();//向地图中添加marker
    }
    
    //创建地图函数：
    function createMap(){
        var map = new BMap.Map("dituContent");//在百度地图容器中创建一个地图
        var point = new BMap.Point(118.960073,32.123373);//定义一个中心点坐标
        map.centerAndZoom(point,18);//设定地图的中心点和坐标并将地图显示在地图容器中
        window.map = map;//将map变量存储在全局
    }
    
    //地图事件设置函数：
    function setMapEvent(){
        map.enableDragging();//启用地图拖拽事件，默认启用(可不写)
        map.enableScrollWheelZoom();//启用地图滚轮放大缩小
        map.enableDoubleClickZoom();//启用鼠标双击放大，默认启用(可不写)
        map.enableKeyboard();//启用键盘上下左右键移动地图
    }
    
    //地图控件添加函数：
    function addMapControl(){
        //向地图中添加缩放控件
	var ctrl_nav = new BMap.NavigationControl({anchor:BMAP_ANCHOR_TOP_LEFT,type:BMAP_NAVIGATION_CONTROL_LARGE});
	map.addControl(ctrl_nav);
        //向地图中添加缩略图控件
	var ctrl_ove = new BMap.OverviewMapControl({anchor:BMAP_ANCHOR_BOTTOM_RIGHT,isOpen:0});
	map.addControl(ctrl_ove);
        //向地图中添加比例尺控件
	var ctrl_sca = new BMap.ScaleControl({anchor:BMAP_ANCHOR_BOTTOM_LEFT});
	map.addControl(ctrl_sca);
    }
    
    //标注点数组
    var markerArr = [{title:"环境学院",content:"栖霞区仙林大道163号南京大学仙林校区",point:"118.960024|32.123396",isOpen:1,icon:{w:23,h:25,l:0,t:21,x:9,lb:12}}
		 ];
    //创建marker
    function addMarker(){
        for(var i=0;i<markerArr.length;i++){
            var json = markerArr[i];
            var p0 = json.point.split("|")[0];
            var p1 = json.point.split("|")[1];
            var point = new BMap.Point(p0,p1);
			var iconImg = createIcon(json.icon);
            var marker = new BMap.Marker(point,{icon:iconImg});
			var iw = createInfoWindow(i);
			var label = new BMap.Label(json.title,{"offset":new BMap.Size(json.icon.lb-json.icon.x+10,-20)});
			marker.setLabel(label);
            map.addOverlay(marker);
            label.setStyle({
                        borderColor:"#808080",
                        color:"#333",
                        cursor:"pointer"
            });
			
			(function(){
				var index = i;
				var _iw = createInfoWindow(i);
				var _marker = marker;
				_marker.addEventListener("click",function(){
				    this.openInfoWindow(_iw);
			    });
			    _iw.addEventListener("open",function(){
				    _marker.getLabel().hide();
			    })
			    _iw.addEventListener("close",function(){
				    _marker.getLabel().show();
			    })
				label.addEventListener("click",function(){
				    _marker.openInfoWindow(_iw);
			    })
				if(!!json.isOpen){
					label.hide();
					_marker.openInfoWindow(_iw);
				}
			})()
        }
    }
    //创建InfoWindow
    function createInfoWindow(i){
        var json = markerArr[i];
        var iw = new BMap.InfoWindow("<b class='iw_poi_title' title='" + json.title + "'>" + json.title + "</b><div class='iw_poi_content'>"+json.content+"</div>");
        return iw;
    }
    //创建一个Icon
    function createIcon(json){
        var icon = new BMap.Icon("http://app.baidu.com/map/images/us_mk_icon.png", new BMap.Size(json.w,json.h),{imageOffset: new BMap.Size(-json.l,-json.t),infoWindowOffset:new BMap.Size(json.lb+5,1),offset:new BMap.Size(json.x,json.h)})
        return icon;
    }
    
    initMap();//创建和初始化地图
</script>
</section>


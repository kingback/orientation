## Orientation

- BY 虎牙

## 简介

> 判断与监听当前设备是横屏还是竖屏，针对不同场景对页面进行自适应

## API及使用例子

    <script src="./src/orientation.js"></script>       
    
    //是否为横屏
    Orientation.isLandscape();
    
    //是否为竖屏
    Orientation.isPortrait();
    
    //获取当前横竖屏信息
    //info.landscape 是否为横屏
    //info.portrait 是否为竖屏
    //info.orientation 角度（横屏为90度或-90度）
    Orientation.getInfo(); //或者直接引用 Orientation.info
        
    //监听横竖屏变换
    Orientation.change(function(e) {
        //e.landscape
        //e.portrait
        //e.orientation
        //e.originType 原生事件名称（orientationchange or resize）原生不支持的用resize模拟
        //e.originEvent 原生事件对象
    });
    
    //绑定after事件，setTimeout 0ms 后执行
    Orientation.change(function(e) {
        //同上
    }, true);
    
    //创造新的实例对象（一般用不着）
    var newOrientation = Orientation.create({
        delay: 250 //延时250ms触发回调，默认为400ms，保证横竖屏完全切换完毕
    }); 
    
   
# jQuery-smartMenu
jQuery 右键菜单插件，代码源：http://www.zhangxinxu.com/study/201105/jquery-plugin-smart-menu-demo.html

# 用法：
```js
var imageMenuData = [
    [{
        text: "图片描边",
        data: [[{
            text: "5像素深蓝",
            func: function() {
                $(this).css("border", "5px solid #34538b");
            }
        }, {
            text: "5像素浅蓝",
            func: function() {
                $(this).css("border", "5px solid #a0b3d6");
            }
        }, {
            text: "5像素淡蓝",
            func: function() {
                $(this).css("border", "5px solid #cad5eb");
            }
        }]]
    }, {
        text: "图片内间距",
        func: function() {
            $(this).css("padding", "10px");
        }
    }, {
        text: "图片背景色",
        func: function() {
            $(this).css("background-color", "#beceeb");
        }
    }],
    [{
        text: "查看原图",
        func: function() {
            var src = $(this).attr("src");
            window.open(src.replace("/s512", ""));    
        }
    }]
];
var bodyMenuData = [[{ text: "页面空白处点击是否冲突测试" }]];
$("#testImage").smartMenu(imageMenuData, {
    name: "image"    
});
$("body").smartMenu(bodyMenuData, {
    name: "body"    
});
```

# h5-alert
 
 > 为了方便调用，绑定事件需要自行绑定
 
 - 基于`jquery`
 - 如果同一个页面需要多个弹出框，需要单独给`.dialogWarp`定义`class`
 
 ```javascript

    //显示默认的弹出框
    $('.dialog-btn').click(function () {
        var dialogAlert = new dialog({
            dialogBtn: this,
            default: function () {
                console.log("取消按钮1")
            },
            primary: function () {
                console.log("确定按钮1")
            }
        })
    });


    //生成弹出框
    $('.dialog-btn2').click(function () {
        var dialogAlert2 = new dialog({
            append: true,
            dialogBtn: this,
            dialogText: '提示信息2',
            dialogTitle: '提示标题2',
            default: function () {
                console.log("取消按钮2")
            },
            primary: function () {
                console.log("确定按钮2")
            }
        })
    });
```

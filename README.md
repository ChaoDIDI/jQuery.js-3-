### 来做一个小动画吧用jquery ###

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>jQuery-event相关</title>
    <style>
        .block{
            width:300px;
            height: 60px;
            margin: 20px auto;
            background-color: #703210;
        }
    </style>
</head>
<body>
    <div class="block" id="block">

    </div>
    <a href="javascript:void(0)" id="btn">点我</a>
    <script src="node_modules/jquery/dist/jquery.js"></script>
    <script src="js/event.js"></script>
</body>
</html>
```

```javascript
  $(function(){
  if($"#block").css("display")=="none"{
    $("#btn").text("显示");
  }
  else{
  $("#btn").text("隐藏");
  }
  
  $("#btn").bind("click",function(){
    var text = $(this).text();
    if(text=="显示"){
    $(this).text("隐藏");
    //$("block").show();//展示元素
    }else{
    $(this).text("显示");
    //$("#block").hide();//隐藏元素
    }
    $("#block").toggle(2000);
  })
  })
```


就这么简单的实现了一个放大缩小动画.其实不然哦..是因为我在他打开关闭的时候添加了toggle(2000);因为我们代码中是一毫秒计算的.你们要记住这个技巧了蛮实用的

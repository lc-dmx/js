![](https://github.com/lc-dmx/js/blob/master/%E8%B7%B3%E8%BD%AC%E7%BD%91%E9%A1%B5/2935550262.gif)
主要代码如下：
```
<script type="text/javascript">  
 
   //获取显示秒数的元素，通过定时器来更改秒数。
    var num=document.getElementById("second").innerHTML;
    var i=setInterval("start()",1000);
    
    function start(){
        
        num--;
        document.getElementById("second").innerHTML=num;
        
        if(num==0){
            window.open("http://www.imooc.com/");
            clearInterval(i);
        }
    }
    
   //通过window的location和history对象来控制网页的跳转。
   function back() {
        window.history.back();
   }
 </script> 
```

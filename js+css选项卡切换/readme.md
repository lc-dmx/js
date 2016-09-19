效果如下：
![](https://github.com/lc-dmx/js/blob/master/js%2Bcss%E9%80%89%E9%A1%B9%E5%8D%A1%E5%88%87%E6%8D%A2/1.jpg)
主要代码如下：
```
<script type="text/javascript">
         
    // JS实现选项卡切换
    window.onload=function(){ 
        var a=document.getElementById("tab");
        var b=a.getElementsByTagName("ul")[0];
        var c=b.getElementsByTagName("li");
        var d=a.getElementsByTagName("div");
        
        for(var i=0;i<c.length;i++){
            c[i].index=i;
            c[i].onclick=function(){
            for(var j=0;j<c.length;j++){
                c[j].className="";
                d[j].className="hide";
            }
            this.className="on";
            d[this.index].className="";
            };
        }
    }
    </script>
```

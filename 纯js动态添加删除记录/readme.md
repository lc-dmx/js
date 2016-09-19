效果如下：
![](https://github.com/lc-dmx/js/blob/master/%E7%BA%AFjs%E5%8A%A8%E6%80%81%E6%B7%BB%E5%8A%A0%E5%88%A0%E9%99%A4%E8%AE%B0%E5%BD%95/1.jpg)
![](https://github.com/lc-dmx/js/blob/master/%E7%BA%AFjs%E5%8A%A8%E6%80%81%E6%B7%BB%E5%8A%A0%E5%88%A0%E9%99%A4%E8%AE%B0%E5%BD%95/2.jpg)
![](https://github.com/lc-dmx/js/blob/master/%E7%BA%AFjs%E5%8A%A8%E6%80%81%E6%B7%BB%E5%8A%A0%E5%88%A0%E9%99%A4%E8%AE%B0%E5%BD%95/3.jpg)
主要代码如下：
```
<script type="text/javascript"> 
    
      window.onload = function(){
                  
     // 鼠标移动改变背景,可以通过给每行绑定鼠标移上事件和鼠标移除事件来改变所在行背景色。
        var tr=document.getElementsByTagName("tr"); 
        for(var i=0;i<tr.length;i++){
            bgcChange(tr[i]);
    	}
	 }
     
     function bgcChange(obj){
        obj.onmouseover=function(){
            obj.style.backgroundColor="#f2f2f2";
        }
        obj.onmouseout=function(){
            obj.style.backgroundColor="#fff";
        }
     }
      // 编写一个函数，供添加按钮调用，动态在表格的最后一行添加子节点；
    function add(){
        var table=document.getElementById("table")
        var txt=table.rows[document.getElementsByTagName("tr").length-1].cells[0].innerHTML;
         
        var num=parseInt(txt.substr(4));
        num++;
        
        var tr=document.createElement("tr");
        
        var td1=document.createElement("td");
        td1.innerHTML="xh00"+num;
        tr.appendChild(td1);
        var td2=document.createElement("td");         
        td2.innerHTML=prompt("请输入姓名");
        tr.appendChild(td2);
        var td3=document.createElement("td");
        td3.innerHTML="<a href='javascript:;' onclick='del(this)'>删除</a>";       
        tr.appendChild(td3);
        
        var table=document.getElementById("table");
        table.appendChild(tr);
        
     }
   	 
     // 创建删除函数
     function del(obj){
        var tr=obj.parentNode.parentNode;
        tr.parentNode.removeChild(tr);
     }
  </script>
```

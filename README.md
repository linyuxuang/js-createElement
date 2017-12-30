# js-createElement
在js中使用createElement创建HTML对象和元素



1.创建链接









                      var o = document.body; 
                      //创建链接 
                      function createA(url,text) 
                      { 
                      var a = document.createElement("a"); 
                      a.href = url; 
                      a.innerHTML = text; 
                      a.style.color = "red"; 
                      o.appendChild(a); 
                      } 
                      createA("http://www.ffasp.com/","网页教学网"); 


2.创建DIV


                      var o = document.body; 
                      //创建DIV 
                      function createDIV(text) 
                      { 
                      var div = document.createElement("div"); 
                      div.innerHTML = text; 
                      o.appendChild(div); 
                      } 
                      createDIV("网页教学网：http://www.ffasp.com/");    
                      </script> 

                      3.创建表单项
                      <script language="javascript"> 
                      var o = document.body; 
                      //创建表单项 
                      function createInput(sType,sValue) 
                      { 
                      var input = document.createElement("input"); 
                      input.type = sType; 
                      input.value = sValue; 
                      o.appendChild(input); 
                      } 
                      createInput("button","ooo"); 
 
 
4.创建表格

                     var o = document.body; 
                      function createTable(w,h,r,c) 
                      { 
                      var table = document.createElement("table"); 
                      var tbody = document.createElement("tbody"); 
                      table.width = w; 
                      table.height = h; 
                      table.border = 1;    
                      for(var i=1;i<=r;i++) 
                      { 
                      var tr = document.createElement("tr"); 
                      for(var j=1;j<=c;j++) 
                      { 
                      var td = document.createElement("td"); 
                      td.innerHTML = i + "" + j; 
                      //td.appendChild(document.createTextNode(i + "" + j)); 
                      td.style.color = "#FF0000"; 
                      tr.appendChild(td); 
                      } 
                      tbody.appendChild(tr);    
                      } 
                      table.appendChild(tbody); 
                      o.appendChild(table); 
                      } 
                      createTable(270,270,9,9); 
                      5.创建select
                      jquery 的话这样
                      <select id="selectid">
                      </select>

                      $(function(){
                         $("#selectid").click(function(){
                              $("#selectid").append("<option value='"+entity+"'>"+entity+"</option>");//entity 变量
                      }); 

                      });

                      js的话
                      function padd(){
                       var objOption = document.createElement("OPTION");
                       objOption.text= 2; 
                       objOption.value=2; 
                       document.getElementById("padd").options.add(objOption);
                      }

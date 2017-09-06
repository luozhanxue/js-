# js-
页面注册
<html>
	<head>
    <meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
    <title></title>
    </head>
    <style>
    	#div1{
			width:500px;
			height:600px;
			background:#CCF;
			margin:0px auto;
		}
		#div1 h2{
			padding:30px 10px;
		} 
		#div1 hr{
			width:450px;
		}
		#tex1{
			width:330px;
			height:40px;
			color:gray;
			margin:10px;
		}
		#tex2{
			width:320px;
			height:40px;
			color:gray;
			margin:10px;
		}
		#tex3{
			width:300px;
			height:40px;
			color:gray;
			margin:10px;
		}
		#tex4{
			width:320px;
			height:40px;
			color:gray;
			margin:10px;
		}
		#tex5{
			width:330px;
			height:40px;
			color:gray;
			margin:10px;
		}
		#but{
			width:100px;
			height:30px;
			background:green;
		}
		#div1 span{
			margin-left:200px;
		}
    </style>
    <script>
    	window.onload = function(){
			
			var oBut = document.getElementById('but');
			var oDiv2 = document.getElementById('div2');
			var aTex = oDiv2.getElementsByTagName('input');
			
			for(var i=0; i<aTex.length; i++){
				aTex[i].index = i;
				aTex[i].onclick = function(){
					this.value = '';
					this.style.color = 'black';
				}
			}
			
			oBut.onclick = function(){
				if(aTex[0].value.length < 6 || aTex[0].value.length >16){
				alert("你输入的用户名有误,为6-16位");
				
				} else if(aTex[3].value.length != 11){
					alert("输入的手机号有误，为11位");
				} else if(aTex[4].value.length < 6 || aTex[4].value.length >32){
					alert("输入的邮箱有误，为6-32位");	
				} else if(aTex[5].value <6 || aTex[5].value <16){
					alert("输入的密码有误，为6-16");	
				} else if(aTex[6].value.length != aTex[6].value.length){
					alert("两次密码不一至");
				} else{
					var name=aTex[0].value;
					var phone = aTex[3].value;
					var get = aTex[4].value;
					var password = aTex[5].value;
					var sex;
					if(aTex[1].checked == true){
						sex = '男';
					} else{
						sex = '女';	
					}
					alert("用户名" + name + ",性别" + sex + ",手机号"+ phone + ",邮箱" + get + ",密码" +password);
				}
			}
		}
    </script>
    <body>
    	<div id="div1">
        	<div id="div2">
        	<center><h2>用户注册</h2></center>
            <hr />
            <font style="padding:10px 30px;">用&nbsp;户&nbsp;名:<input type="text" value="长度6-16位，英文，数字，字符组合" id="tex1"></font>
            <font style="padding:10px 30px;">性&nbsp;&nbsp;&nbsp;&nbsp;别:<input type="radio" value="男">男<input type="radio" value="女">女</font><br />
            <font style="padding:10px 30px;">手&nbsp;机&nbsp;号:<input type="text" value="长度11位" id="tex2"></font>
            <font style="padding:10px 30px;">邮&nbsp;&nbsp;&nbsp;&nbsp;箱:<input type="text" value="长度6-32位" id="tex3"></font>
            <font style="padding:10px 30px;">密&nbsp;&nbsp;&nbsp;&nbsp;码:<input type="password" value="123456" id="tex4"></font>
            <font style="padding:10px 30px;">确认密码:<input type="password" value="12345" id="tex5"></font>
            <hr />
            </div>
            <span><input type="button" value="注册" id="but" ></span>
        </div>
    </body>
</html>

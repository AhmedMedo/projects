projects
========

simple game with javascript
<!DOCTYPE html>

<html>
	<head>
		<link rel="stylesheet" type="text/css" href="project.css" >
		<meta charset="utf-8"/>
		<meta http-equiv="Content-type" content="text/html; charset=utf-8" />	
		<meta name="viewport" content="width=device-width, initial-scale=1" />	
		<style>
			#box{
				height:200px;
				width:200px;
				background-color:red;
				display:none;
				position:relative;
	

				}
			#text{
				font-family:verdana;
				font-weight:bold;
			}
		</style>

	
	
	
	
	
	
	</head>
	<body>
		<h1>Can you do it?!</h1>
		<p id="text">your time is: <span id="time"></span> </p>

		<div id="box"></div>
		<script type="text/javascript" src="project.js">
			function getRandomColor() {
			var letters = '0123456789ABCDEF'.split('');
			var color = '#';
			for (var i = 0; i < 6; i++ ) {
				color += letters[Math.floor(Math.random() * 15)];
				}
			return color;
			}

			var clickedTime;var createdTime; var reactionTime;
			function myBox(){
				var time=Math.random();
				time=time*500;
				setTimeout(function(){
				if (Math.random()>0.5) {	
	
					document.getElementById("box").style.borderRadius="100px";	
		
		 	 	 	 }
		 	 	 else {		 	
					document.getElementById("box").style.borderRadius="0";	 	 	 	 	
	 	 	 	 }
	 	 	 	 var top=Math.random();	
	 	 	 	 	
	 	 	 	 top=top*300;	
	 	 	 	 	
	 	 	 	 var left=Math.random();	
	 	 	 	 	
	 	 	 	 left=left*500;	
	 	 	 	 	
	 	 	 	 document.getElementById("box").style.top=top+"px";	
	 	 	 	 	
	 	 	 	 document.getElementById("box").style.left=left+"px";		
					document.getElementById("box").style.backgroundColor=getRandomColor();
					document.getElementById("box").style.display="block";
					createdTime=Date.now();
					
					},time);
				}
			document.getElementById("box").onclick=function(){
				clickedTime=Date.now();
				reactionTime=(clickedTime-createdTime)/1000;
				document.getElementById("time").innerHTML=reactionTime+"s";
				this.style.display="none";	
				myBox();
				
				}
				myBox();
				if(reactionTime=.488){
					alret("Great!");
					
					
					
					}
		

			
		
		</script>
	
	
	
	
	
	
	
	
	</body>




</html>

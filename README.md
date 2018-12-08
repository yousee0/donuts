# a New website just started!
## 랄랄라
<!doctype html>
<html>
<head>
<meta charset="utf-8">
  <title>일상의장소 세운인터뷰</title>
<script type="text/javascript" src="http://code.jquery.com/jquery-1.7.1.min.js"></script>
<script type="text/javascript" src="../../turn.min.js"></script>

<style type="text/css">
body{
	background:#101011;
}
#magazine{
    margin-top:100px;
    margin-left:200px;
	width:900px;
	height:500px;
}
#magazine .turn-page{
	background-color:#ccc;
	background-size:100% 100%;
}
</style>
</head>
<body>

<div id="magazine">
	<div style="background-image:url(pages/01.jpg);"></div>
	<div style="background-image:url(pages/02.jpg);"></div>
	<div style="background-image:url(pages/03.jpg);"></div>
	<div style="background-image:url(pages/04.jpg);"></div>
	<div style="background-image:url(pages/05.jpg);"></div>
	<div style="background-image:url(pages/06.jpg);"></div>
</div>
    
 <div class="magazine">
    <div class="magazine"></div>
    <div class="book-cover"></div>   
 </div>



<script type="text/javascript">

	$(window).ready(function() {
		$('#magazine').turn({
							display: 'double',
							acceleration: true,
							gradients: !$.isTouch,
							elevation:50,
							when: {
								turned: function(e, page) {
									/*console.log('Current view: ', $(this).turn('view'));*/
								}
							}
						});
	});
	
	
	$(window).bind('keydown', function(e){
		
		if (e.keyCode==37)
			$('#magazine').turn('previous');
		else if (e.keyCode==39)
			$('#magazine').turn('next');
			
	});

</script>

</body>
</html>

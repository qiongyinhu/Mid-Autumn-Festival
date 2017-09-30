var music=document.getElementById("music");

var audio=document.getElementsByTagName("audio")[0];

var n11=document.getElementById("n1");//加音量

var n12=document.getElementById("n2");//减音量

audio.volume = 0.6;

n11.addEventListener("touchstart",function(event){

	if(audio.volume>=0&&audio.volume<=1){
	
		audio.volume=audio.volume+0.1;
		
	}	
	
},false);

n12.addEventListener("touchstart",function(event){

	if(audio.volume>=0&&audio.volume<=1){
	
		audio.volume=audio.volume-0.1;
		
	}
	
},false);

audio.addEventListener("ended",function(event){

	music.setAttribute("class","");
	
},false)

music.addEventListener("touchstart",function(event){

	if(audio.paused){
	
		audio.play();
		
		this.setAttribute("class","play");
		
		}else{
		
		audio.pause();
		
		this.setAttribute("class","");
		
		}
		
},false);

page1.addEventListener("touchstart",function(event){

	page1.style.display="none";
	
	page2.style.display="block";
	
	page3.style.display="block";
	
	page3.style.top="100%"

	setTimeout(function(){
	
		page2.setAttribute("class","page fadeOut");
		
		page3.setAttribute("class","page fadeIn");
		
	},5500)
	
},false);

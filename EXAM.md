@@ -1,40 +1,267 @@
 ### 1. Get DOM elements using Javascript selectors
 
 * Select an __IMG__ element
 * 
      //IMPORTANT NOTE:
      //The ones called testing lines will usually be the data stored into a variable, string, object... etc
      // They are a simple test line that will make easier to test that the code actually works. This is 
      //only for evaluation porpuses. It would never be done in a work environment.

+      *<script>
+      function myFunction() {
+      	//Select all elements with the tag <img>.
+      	var _myimg = document.getElementsByTagName("img");
+      	for (i=0;i<_myimg.length;i++){
+      		//within our <img> container we search for the one we'll need to use.
+      		if(_myimg[i].title == "Iglesias añade a su declaración lo que cobró de tertuliano"){
+      		//A simple testing line
+      		//document.getElementById("demo").innerHTML ="hi";
+      		}
+      	}
+      }
+      </script>
+
 * Select all __H2__ elements
+      *//all h2 are selected and stored in _myh2
+      var _myh2 = document.getElementsByTagName("h2");
+      //We will create a loop to work with our data in the future
+      //for (i = 0; i < _myh2.length; i++) {
+      	//        Commands
+      //    }
+
 * Select all __A__ elements that have the attribute _title_
+      * function myFunction() {
+      	//Select all elements with the tag <a>
+      	var _mya = document.getElementsByTagName("a");
+      	for (i = 0; i < _mya.length; i++) {
+      		if(_mya[i].title != ""){
+      			//If they do have a title
+      			//A simple testing line
+      			//document.getElementById("demo").innerHTML ="hi";
+      		}
+      	}  
+      }
+
 * Select only the __IMG__ elements that are inside an __A__ element
+      * function myFunction() {
+      	//Select all elements with the tag <a>
+      	var _mya = document.getElementsByTagName("a");
+      	for (i = 0; i < _mya.length; i++) {
+      		//Select the ones with the tag <img> inside a <a> element.
+      		var _myimg = document.getElementsByTagName("img");
+      	}
+      }
+
 * Select all elements with class _article_
+      * <script>
+      function myFunction() {
+      	//Get all elements
+      	var all = document.getElementsByTagName("*");
+      	for (i=0;i<all.length;i++){
+      		//if it does have a className
+      		if(all[i].className != false){
+      			//Testing line
+      			//document.getElementById("demo").innerHTML +="hi";
+      		}
+      	}   
+      }
+      </script>
+
 * Select all _article_ from the middle and right column, but not from the left column
+      *<script>
+      function myFunction() {
+      	//Select all <tag> elements
+      	var _myrandl = document.getElementsByTagName("*");
+      	for (i=0;i<_myrandl .length;i++){
+      		//if they have the word "right" in their class name they belong to the middle col
+      		if(_myrandl [i].className.indexOf("right") != -1){
+      			//Test line
+      			//document.getElementById("demo").innerHTML ="hi";
+      		}
+      		//if they have the word "aside" in their class name they belong to the right col
+      		else if(_myrandl[i].className.indexOf("aside") != -1){
+      			//Test line
+      			//document.getElementById("demo").innerHTML ="hi";
+      		}
+      	}   
+      }
+      </script>
+
 * Select the 4th and 5th _article_ from the left column
+      * <script>
+      function myFunction() {
+      	//Get all <tag> elements
+      	var _myimg = document.getElementsByTagName("*");
+      	//variable to count elements
+      	var x = 0;
+      	for (i=0;i<_myimg.length;i++){
+      		//if they belong to the left col
+      		if(_myimg[i].className.indexOf("left") != -1){
+      			x++;
+      			//If it is the 4th or 5th element
+      			if (x==4||x==5){
+      				//Test line
+      				//document.getElementById("demo").innerHTML +="hi";
+      			}
+      		}
+      	}   
+      }
+      </script>
+
 * Select the logo of the website
+      * <script>
+      function myFunction() {
+      	//Select <link> elements
+      	var _myimg = document.getElementsByTagName("link");
+      	for (i=0;i<_myimg.length;i++){
+      		//If the logo is changed we will need to either change the 
+      		//URL or select the item in another way. However we will need only to 			change 
+      		//the if statement
+      		if(_myimg[i].href == "http://sstatic.net/stackoverflow/img/favicon.ico"){
+      			//Test line
+      			//document.getElementById("demo").innerHTML ="hi";
+      		}
+      	}
+      }
+
 * Select all __IMG__ elements whose _SRC_ attribute is a _JPG_ file
+* <script>
+      function myFunction() {
+      	//get all <img> elements
+      	var _myimg = document.getElementsByTagName("img");
+      	for (i=0;i<_myimg.length;i++){
+      		//if they've got the word "jpg" in them
+      		if(_myimg[i].src.indexOf("jpg") != -1){
+      			//Test line
+      			//document.getElementById("demo").innerHTML ="hi";
+      		}
+      	}   
+      }
+      </script>
+
 
 ### 2. Apply CSS to DOM
 
 * Change the main article title to FF0000
+      * <script>
+      function myFunction() {
+      	//Select the element by class
+      	var _mytitle = document.getElementsByClassName("art-tit fs-67");
+      	//Set color to FF0000
+      	_mytitle[0].style.color = "#FF0000";
+      	//Or change the title to FF0000
+      	_myimg[0].title = "FF00000";   
+      }
+      </script>
+
 * Change page background color to green
+      * <script>
+      function myFunction() {
+      	//Get element by id and change background color to green
+      	document.getElementById("content").style.background = "green";
+      }
+      </script>
+
 * Change subtitles to lowercase
+      * <script>
+      function myFunction() {
+      	//Select subtitles by class
+      	  var _mysubtitle = document.getElementsByClassName("news-pin-link");
+      	 for(i=0;i<_mysubtitle.length;i++){
+      		//Change to lowercase the innerHTML of each one of them 
+      		_mysubtitle[i].innerHTML = _mysubtitle[i].innerHTML.toLowerCase();
+      	}
+      }
+      </script>
+
 * Hide opinion column
+      * //include Jquery
+      <script src="http://ajax.googleapis.com/ajax/libs/jquery/1.11.2/jquery.min.js"></script>
+      <script>
+      function myFunction() {
+      	var _myopinion = document.getElementsByClassName("op-aside-container");
+      	$(_myopinion[0]).hide();
+      }
+      </script>
+
 * Make top Ad banner sticky at the bottom
+* <script>
+      function myFunction() {
+          //select element by class
+          var _myadd = document.getElementsByClassName("hide-ad");
+          //modify its style. Note that we can still modify more css data
+          _myadd[0].style.bottom = "10px";
+      }
+      </script>
+
 
 ### 3. DOM Manipulation with Javascript
 
-* Add a 10px red border around all __IMG__ elements 
+* Add a 10px red border around all __IMG__ elements
+      * <script>
+      function myFunction() {
+      	//Select all <img> elements
+      	_myimgs = document.getElementsByTagName("img");
+      	for(i=0;i<_myimgs.length;i++){
+      		//Assign a thick solid red border to every single one of them
+      		_myimgs[i].style.border = "thick solid red";
+      	}
+      }
+      </script>
 * Fade out all __IMG__ elements
+      * <script>
+      
+      function myFunction() {
+      	//Select all <img> elements
+      	var _myfadeout = document.getElementsByTagName("img");
+      	for (i=0;i<_myfadeout.length;i++){
+      		//fade them out with .display since we don't know how many of them are in the page 
+      		//and they are randomly distributed(not under our control) we won't use hide() here now.
+      		_myfadeout[i].style.display ="none";
+      	}
+      }
+      </script>
 * Add a 10px red border around all __IMG__ and fade out the images after 3 seconds
+      function myFunction() {
+      	//get all <img> elements
+      	var _myfadeout = document.getElementsByTagName("img");
+      	for(i=0;i<_myfadeout.length;i++){
+      	//assign a thik solid red border to every one of them
+      		_myfadeout[i].style.border = "thick solid red";
+      	}
+      	//Timeout(function(){},time);
+      	setTimeout(function(){ for (i=0;i<_myfadeout.length;i++){
+      	//fade each one
+      		 _myfadeout[i].style.display ="none";
+      	//after 3 seconds
+      	}}, 3000);    
+      }
+      </script>
 
 ### 4. Answer the following points
 
 * Justify the chosen method used to hide opinion column
+      * Even though I need to load the Jquery file, this Jquery method will make all children hidden too wich is very important since the opinion column is got a lot and could have as many children as the owner of the website wants to have.
+      
+      Also, by doing that in css, the element will be hidden but it will be using the space designed for him and, as we don't know how many childrens it has, I assume that space as infinite and that would, eventually, cause troubles.
 
 * Explain the difference between position static, relative, absolute and fixed
+      * Static: The default position. The element will flow into the site as it would normally. 
+      
+      Relative: Meaning “relative to itself”, the element must be relative to another one. Otherwise it could, and most likely will, disappear(not show);
+      
+      Absolute: It is not affected by other objects and won't affect any other ones. It allows you to place the element exactly where you want.
+      
+      Fixed: A riscky one. The element will be relative to the viewport. It can overlap so it needs to be highly tested.
 
 * What are data SRCs? When would you use them?
+      * A piece of metadata included withing a tag that will be invisible. We will do this to use the data in our scripts.
 
 * What benefits you get by using a CSS preprocessor?
+      * A scripting language that extends CSS and gets compiled into regular CSS syntax.(Sass,LESS,Stylus...)
+      
+      Cleaner and reusable code.
+      Allows you to do thing such as math calculations and if statements.
+      Shareable code(libraries).
+      CSS that works across browsers.
 
 * Why would you use unit testing?
+      * Yes. It allows you to test small pieces of code separetly and to make sure that everything will work correctly within a big application.
+
 
 * How would you accelerate an element by hardware and why?
 * 
It depends on the target user. It is extremly useful in mobile applications since it reduces the resource comsumption in the device. On the other hand we must be careful about what are we accelerating, how and who is using our application.A usual way to do so is to accelerate css animations and transforms via GPU.



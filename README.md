


<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title> ⊽ Norbert's Personal Site
  </title>
  </head>
  <body>
  <style>
    
    <style>
* {box-sizing: border-box;}

.img-magnifier-container {
  position:relative;
}

.img-magnifier-glass {
  position: absolute;
  border: 3px solid #000;
  border-radius: 50%;
  cursor: none;
  /*Set the size of the magnifier glass:*/
  width: 100px;
  height: 100px;
}
</style>
<script>
function magnify(imgID, zoom) {
  var img, glass, w, h, bw;
  img = document.getElementById(imgID);
  /*create magnifier glass:*/
  glass = document.createElement("DIV");
  glass.setAttribute("class", "img-magnifier-glass");
  /*insert magnifier glass:*/
  img.parentElement.insertBefore(glass, img);
  /*set background properties for the magnifier glass:*/
  glass.style.backgroundImage = "url('" + img.src + "')";
  glass.style.backgroundRepeat = "no-repeat";
  glass.style.backgroundSize = (img.width * zoom) + "px " + (img.height * zoom) + "px";
  bw = 3;
  w = glass.offsetWidth / 2;
  h = glass.offsetHeight / 2;
  /*execute a function when someone moves the magnifier glass over the image:*/
  glass.addEventListener("mousemove", moveMagnifier);
  img.addEventListener("mousemove", moveMagnifier);
  /*and also for touch screens:*/
  glass.addEventListener("touchmove", moveMagnifier);
  img.addEventListener("touchmove", moveMagnifier);
  function moveMagnifier(e) {
    var pos, x, y;
    /*prevent any other actions that may occur when moving over the image*/
    e.preventDefault();
    /*get the cursor's x and y positions:*/
    pos = getCursorPos(e);
    x = pos.x;
    y = pos.y;
    /*prevent the magnifier glass from being positioned outside the image:*/
    if (x > img.width - (w / zoom)) {x = img.width - (w / zoom);}
    if (x < w / zoom) {x = w / zoom;}
    if (y > img.height - (h / zoom)) {y = img.height - (h / zoom);}
    if (y < h / zoom) {y = h / zoom;}
    /*set the position of the magnifier glass:*/
    glass.style.left = (x - w) + "px";
    glass.style.top = (y - h) + "px";
    /*display what the magnifier glass "sees":*/
    glass.style.backgroundPosition = "-" + ((x * zoom) - w + bw) + "px -" + ((y * zoom) - h + bw) + "px";
  }
  function getCursorPos(e) {
    var a, x = 0, y = 0;
    e = e || window.event;
    /*get the x and y positions of the image:*/
    a = img.getBoundingClientRect();
    /*calculate the cursor's x and y coordinates, relative to the image:*/
    x = e.pageX - a.left;
    y = e.pageY - a.top;
    /*consider any page scrolling:*/
    x = x - window.pageXOffset;
    y = y - window.pageYOffset;
    return {x : x, y : y};
  }
}
</script>
<body>

<h1>Soy Bundi</h1>


<div class="img-magnifier-container">
  <img id="myimage" src="https://scontent-ams4-1.cdninstagram.com/v/t51.2885-15/e35/53521086_2235977566675244_2916928562214346892_n.jpg?_nc_ht=scontent-ams4-1.cdninstagram.com&_nc_cat=108&oh=d508cd75f27e81ab711c8c35bc988191&oe=5E869200" width="600" height="600">
</div>


<script>
/* Initiate Magnify Function
with the id of the image, and the strength of the magnifier glass:*/
magnify("myimage", 3);
</script>

<p>
Adásvételi Szerződés


A megállapodás létrejött alulírott Felek között, az alábbi jármű tulajdonjogának átruházása tárgyában: 


Jármű adatai: 

Alvázszám:
Márka:
Model:
Típus:
Gyártás éve:
Jármű színe: 


Eladó adatai: 

Családi és utóneve: 
Személyi igazolvány száma
Születési helye és ideje: 
Anyja neve: 
Lakcíme:


Vevő adatai: 

Családi és utóneve: 
Személyi igazolvány száma
Születési helye és ideje: 
Anyja neve: 
Lakcíme:
A járműnek a vevő birtokába kerülési időpontja:

A jármű vételára:
Fizetés módja és ideje:




----------------------								-------------------
Eladó aláírása									Vevő aláírása


</p>

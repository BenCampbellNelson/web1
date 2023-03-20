<!-- HTML - structure -->


<div id ="menu">
  <div id="menu-items">
    <a href="/" class="menu-item">HOME</a>
    <a href="/" class="menu-item">SHOP</a>
    <a href="/about.html" class="menu-item">ABOUT</a>
    <a href="/" class="menu-item">CONTACT</a>
  </div>
  <div id="menu-background-image"></div>
</div>

<head>
  <meta charset="utf-8"/>
  <title>Home</title>
</head>

<body>
  <a href="about.html">About</a>
</body>

<div id ="mainDiv">This is a div styled by an ID</div>

<div class="secondDiv">This is a div styled by a class</div>
 
<button on:click={changeColour} style="background:{randomColour}">
  Clicked {count} {count == 1 ? 'time' : 'times'}
</button>

<h2> {writeName()}</h2>

<p>You can reach Ben at:</p>

<ul>
  <li><a href= "facebook.com">Website</a></li>
  <li><a href= "campbf2@student.op.ac.nz">Email</a></li>
  <li><a href= "0271234567">Phone</a></li>
</ul>



<!-- CC - styling -->
<style>

    h1{
        color:blue;
        font-size:70px;
        font-style:bold;
        font-weight:normal;
        font-family: Arial;
    }
button {
        background-color: #701111;
        color: #FFFFFF;
        padding: 10px;
        border-radius: 10px;
        -moz-border-radius: 10px;
        -webkit-border-radius: 10px;
        margin:10px
}
h2{
  background-position-x: right;
  background-color: bisque;
  background-size: 50px;
}

p{
  color:dimgrey;
  width:500px;
  font: caption;
}

ul{
  font: menu;
  font-size: larger;
}

#mainDiv{
    font-size: 20px;
    color: green;
    height: bold;
}
/*use # for ID and use . for class*/
.secondDiv{
    font-size: 30px;
    color: blue;
    text-decoration-line: line-through;

}

body{
  background-color: rgb(20, 20, 20);
}

#menu{
  height: 100vh;
  display: flex;
  align-items: center;
}
/*clamp(min, val, max)*/
.menu-item{
  color:white;
  font-size: clamp(3rem, 8vw, 8rem);
  font-family: "Franklin Gothic Medium", serif;
  letter-spacing: -0.05em;


  display: block;
  text-decoration: none;
  padding: clamp(0.25rem, 0.5vw, 1rem) 0rem;
  transition: opacity 400ms ease;
}

#menu-items{
  margin-left: clamp(4rem, 20vw, 48rem);
  position: relative;
  z-index: 2;
}

#menu-items:hover > .menu-item {
  opacity: 0.3;
}

#menu-items:hover > .menu-item:hover {
opacity: 1;
}

#menu-background-image {
  height: 100%;
  width: 100%;

  background-image: url(https://c4.wallpaperflare.com/wallpaper/566/212/992/the-last-of-us-game-wallpaper-preview.jpg);

  position: absolute;
  left: 0px;
  top: 0px;
  z-index: 0;

  background-position: center 40%;
  background-size: 100vmax;
  opacity: 0.15;

  /**SO that background transition is smooth*/
  transition: opacity 800ms ease,
  background-size 800ms ease,
  background-position 800ms ease;
}

#menu-items:hover ~ #menu-background-image{
  background-size: 104vmax;
  opacity: 0.10;
}

</style>





<!-- JS - functionality -->
<script>

   let count = 0;
   let first_name = "Ben"
   let last_name = "Campbell"
   const space = " "

   function incrementCount()
   {
        //count = count+1
        count++;
   }
   function writeName()
   {
        return (first_name + space + last_name)
   }

   let randomColour;

   function changeColour()
   {
        let r = Math.floor(Math.random() * 255);
        let g = Math.floor(Math.random() * 255);
        let b = Math.floor(Math.random() * 255);

        //randomColour = "rgb(" + r + "," + g + "," + b + ")";
        randomColour = `rgb(${r},${g},${b})`
   }



</script>






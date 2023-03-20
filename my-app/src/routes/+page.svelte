<!-- HTML - structure -->
<div id ="menu">
  <div id="menu-items">
    <a href="/" class="menu-item">HOME</a>   
    <a href="/my-app\src\routes\about.html"class="menu-item">ABOUT</a>
    <a href="/my-app\src\routes\blank.html" class="menu-item">CONTACT</a>
  </div>
  <div class="name">
    <div class = "item item-1">item 1</div>
    <div class = "item item-1">item 1</div>
    <div class = "item item-1">item 1</div>
  </div>
  <div id="menu-background-image"></div>
</div>
<div>
  <div id="menu-background-image-2"></div>
</div>
<head>
  <meta charset="utf-8"/>
  <title>Home</title>
</head>


<h2> {writeName()}</h2>


<p>You can reach Ben at:</p>

<ul>
  <li><a href= "facebook.com">Website</a></li>
  <li><a href= "campbf2@student.op.ac.nz">Email</a></li>
  <li><a href= "0271234567">Phone</a></li>
</ul>

<button on:click={changeColour} style="background:{randomColour}">
  Clicked {count} {count == 1 ? 'time' : 'times'}
</button>

<body>
  <a href="about.html">About</a>
</body>

<div id ="mainDiv">This is a div styled by an ID</div>

<div class="secondDiv">This is a div styled by a class</div>

<!-- CC - styling -->
<style>
h1 {
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
  color:white;
  font-size: clamp(3rem, 8vw, 8rem);
  font-family: "Franklin Gothic Medium", serif;
  letter-spacing: -0.05em;


  display: block;
  text-decoration: none;
  padding: clamp(0.25rem, 0.5vw, 1rem) 0rem;
  transition: opacity 400ms ease;
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

.name{
  color:white;
  font-size: clamp(2rem, 8vw, 2rem);
  font-family: "Franklin Gothic Medium", serif;
  letter-spacing: -0.05em;

  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
}

body{
  background-color: rgb(20, 20, 20);
}

#menu {
  height: 100vh;
  display: flex;
  align-items: center;
}
/*clamp(min, val, max)*/
.menu-item {
  color:white;
  font-size: clamp(3rem, 8vw, 8rem);
  font-family: "Franklin Gothic Medium", serif;
  letter-spacing: -0.05em;


  display: block;
  text-decoration: none;
  padding: clamp(0.25rem, 0.5, 1rem) 0rem;
  transition: opacity 400ms ease;
}

#menu-items {
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

  background-image: url(https://images.saatchiart.com/saatchi/1092649/art/6429107/5498859-HSC00001-7.jpg);

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


#menu-background-image-2{
  height: 100%;
  width: 100%;

  background-image: url();

  position: absolute;
  left: 0px;
  top: 0px;
  z-index: 0;

  background-position: center 40%;
  background-size: 100vmax;
  opacity: 0.15;

  transition: opacity 800ms ease,
  background-size 800ms ease,
  background-position 800ms ease;
}

a {
  background-image: linear-gradient(
    to right,
    #01e1ffb4 ,
    #ffffff 50%
  );
  background-size: 200% 100%;
  background-position: -100%;
  display: inline-block;
  padding: 5px 0;
  position: relative;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  transition: all 0.3s ease-in-out;
}

a:before{
  content: '';
  background: #01e1ffb4;
  display: block;
  position: absolute;
  bottom: -3px;
  left: 0;
  width: 0;
  height: 3px;
  transition: all 0.3s ease-in-out;
}

a:hover {
 background-position: 0;
}

a:hover::before{
  width: 100%;
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






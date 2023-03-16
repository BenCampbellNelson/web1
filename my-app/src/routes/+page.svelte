<!-- CC - styling -->
<style>

    h1{
        color:blue;
        font-size:70px;
        font-style: italic;
        font-weight:normal;
    }
</style>
<!-- JS - functionality -->>
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



<h1>{writeName()}</h1>
<!-- HTML - structure -->
<button on:click={changeColour} style="background:{randomColour}">
    Clicked {count} {count == 1 ? 'time' : 'times'}
</button>

<h2> {writeName()}</h2>

<div>
    {writeName()}
</div>

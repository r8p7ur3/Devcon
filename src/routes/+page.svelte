<script>
    import pentagon from "$lib/images/devcon-items/pentagon.png"
    import corklogo from "$lib/images/devcon-items/logo.png"
    import devcon from "$lib/images/devcon-items/devcon.png"
    import ucc from "$lib/images/devcon-items/ucc.png"

    //for when divs enter viewport
    // i tried having a dedicated .svelte for it and importing but it wouldn't import script
    import { onDestroy, onMount } from "svelte";

  let inViewPort = false;
  let inViewPort2 = false;
  let inViewPort3 = false;
  /**@type {HTMLElement}*/
  let root;
  /**@type {HTMLElement}*/
  let root2;
  /**@type {HTMLElement}*/
  let root3;
  //for tracking
  let done = false;
  let countdown

  


  onMount(() => {
    if (!root) return //ok so when reloading page there wasn't enough time for the DOM to load before this ran, so if no root 
    // which is binded to the divs is found it simply keeps going till it is 
    let observer = new IntersectionObserver((entries) => {
    entries.forEach((entry) => {
      if (entry.isIntersecting) {
        inViewPort = true;
        observer.disconnect();
      };
     
    });
  });
   let observer2 = new IntersectionObserver((entries) => {
    entries.forEach((entry) => {
      if (entry.isIntersecting) {
        inViewPort2 = true;
        observer2.disconnect();
      };
     
    });
  });
   let observer3 = new IntersectionObserver((entries) => {
    entries.forEach((entry) => {
      if (entry.isIntersecting) {
        inViewPort3 = true;
        observer3.disconnect();
      };
     
    });
  });
    observer.observe(root);
    observer2.observe(root2);
    
  });

  
    //typescript end
</script>
<!--fix your pngs to high res at some point-->
<div id="welcome" class="bg-black  h-214.5 relative overflow-visible overflow-x-clip border-5 border-black">
<!-- pentagons-->
    <img class=" absolute z-0 opacity-10  top-0 left-[-350px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
    <img class=" absolute  z-0 top-[-330px] opacity-10 right-[210px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
    <img class=" absolute z-0 bottom-[-330px] opacity-10 left-[100px]  size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
    <img class=" absolute z-0 bottom-[-300px] motion-opacity-in-0 opacity-10 left-[1550px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
<!-- second div petagons-->    
     <img class=" absolute opacity-10 z-0  top-[1400px] left-[-250px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
    <img class=" absolute  top-[1430px] opacity-10 right-[310px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
    <img class=" absolute  bottom-[-1430px] opacity-10 left-[200px]  size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
    <img class=" absolute bottom-[-1400px] motion-opacity-in-0 opacity-10 left-[1550px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
<!--Third div pentagons -->
 <img class=" absolute opacity-10  top-[2300px] left-[-350px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
    <img class=" absolute  top-[-2330px] opacity-10 right-[210px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
    <img class=" absolute  bottom-[-2330px] opacity-10 left-[100px]  size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
    <img class=" absolute bottom-[-2300px] motion-opacity-in-0 opacity-10 left-[1550px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">


    <!-- logo and stuff-->
     <img class="absolute motion-delay-500 motion-opacity-in-0 left-[350px] bottom-[290px] -z-0" src="{corklogo}" alt="logo">
     <img class=" absolute -z-0 motion-delay-1000 motion-duration-1000 motion-opacity-in-0 left-[820px] bottom-[450px]  w-130" src="{devcon}" alt="devcon">
     <img class="absolute -z-0 motion-delay-1000 motion-opacity-in-0 left-[800px] bottom-[340px] w-130 " src="{ucc}" alt="ucc-cs-logo">



</div>
<!-- motion-preset-typewriter not being maintained -_- (oh well)-->
 <!-- i'll figure something else out-->

    
<div bind:this={root} class=" bg-black  h-257.5" id="About">
    {#if inViewPort === true }

    <h1 class=" relative text-white text-center top-[250px] text-6xl font-extrabold motion-delay-500 motion-opacity-in-0 motion-translate-y-in-100">About</h1>
    <p class="relative text-2xl text-white top-[300px] text-center font-extrabold typewriter-10 motion-delay-200 motion-opacity-in-0 motion-translate-y-in-100">Devcon is a Cork-based tech confrence that's held annually in UCC. 
       <br> It brings awareness to  the exciting and innovative technology developments
        <br>from all across ireland, and helps to bridge the gap between students
        <br>and the tech industry. Cork Devcon is an initiative by UCC Netsoc.
    </p>
    {/if}
</div>



 
<div bind:this={root2}  class=" bg-black h-347.5" id="Guests">
    {#if inViewPort2===true}
    <!-- to be done once i begin emailing-->
     <h1 class=" relative text-white top-[300px] text-center text-6xl font-extrabold motion-delay-500 motion-opacity-in-0 motion-translate-y-in-100">Guests Speakers</h1>
    <p class="text-2xl relative top-[300px] text-white text-center font-extrabold typewriter-10 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100">To Be Announced</p>

    {/if}
</div>





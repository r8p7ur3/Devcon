<script>
    import pentagon from "$lib/images/devcon-items/pentagon.png"
    import corklogo from "$lib/images/devcon-items/logo.png"
    import devcon from "$lib/images/devcon-items/devcon.png"
    import ucc from "$lib/images/devcon-items/ucc.png"
    import { onMount } from "svelte";


    // having typescript here since im not sure how to call from dif file, figure out and fix later :/
    let isVisible = false;
    let AboutDiv;
    let Countdown;
    let Guests;

    //to handle whenever a div comes into view (WiP)
    onMount(() => {
    const observer = new IntersectionObserver(
      ([AboutDiv]) => {
        observer.observe(AboutDiv.target)
        if (AboutDiv.isIntersecting) {
          isVisible = true;
          observer.unobserve(AboutDiv.target); // only animate once
        }
      },
      { threshold: 0.1 }
    );

  });
    


    //typescript end
</script>
<!--fix your pngs to high res at some point-->
<div id="welcome" class="bg-black w-screen h-214.5 relative overflow-visible overflow-x-clip border-5 border-black">
<!-- pentagons-->
    <img class=" absolute opacity-10  top-0 left-[-350px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
    <img class=" absolute  top-[-330px] opacity-10 right-[210px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
    <img class=" absolute  bottom-[-330px] opacity-10 left-[100px]  size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
    <img class=" absolute bottom-[-300px] motion-opacity-in-0 opacity-10 left-[1550px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
<!-- second div petagons-->    
     <img class=" absolute opacity-10  top-[1400px] left-[-250px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
    <img class=" absolute  top-[1430px] opacity-10 right-[310px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
    <img class=" absolute  bottom-[-1430px] opacity-10 left-[200px]  size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
    <img class=" absolute bottom-[-1400px] motion-opacity-in-0 opacity-10 left-[1550px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
<!--Third div pentagons -->
 <img class=" absolute opacity-10  top-[2300px] left-[-350px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
    <img class=" absolute  top-[-2330px] opacity-10 right-[210px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
    <img class=" absolute  bottom-[-2330px] opacity-10 left-[100px]  size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
    <img class=" absolute bottom-[-2300px] motion-opacity-in-0 opacity-10 left-[1550px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">


    <!-- logo and stuff-->
     <img class="absolute motion-delay-2000 motion-opacity-in-0 left-[350px] bottom-[290px]" src="{corklogo}" alt="logo">
     <img class=" absolute motion-delay-4000 motion-duration-1000 motion-opacity-in-0 left-[820px] bottom-[450px]  w-130" src="{devcon}" alt="devcon">
     <img class="absolute motion-delay-4000 motion-opacity-in-0 left-[800px] bottom-[340px] w-130 " src="{ucc}" alt="ucc-cs-logo">



</div>
<!-- motion-preset-typewriter not being maintained :( oh well)-->
 <!-- i'll figure something else out-->

<div bind:this={AboutDiv}  class=" bg-black w-screen h-217.5" id="Abouts">
    <div class="">
    <h1 class="text-center text-6xl font-extrabold motion-opacity-in-0 motion-delay-800 motion-translate-y-in-100">About</h1>
    </div>
    <p class="text-2xl text-white text-center font-extrabold typewriter-10 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100">Devcon is a Cork-based tech confrence that's held annually in UCC. 
       <br> It brings awareness to  the exciting and innovative technology developments
        <br>from all across ireland, and helps to bridge the gap between students
        <br>and the tech industry. Cork Devcon is an initiative by UCC Netsoc.
    </p>
</div>

<div bind:this={Countdown} class=" bg-black w-screen h-217.5" id="Countdown">
    <p class="text-2xl text-white text-center font-extrabold typewriter-10 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100">countdown will be going here (not sure how to do it yet)</p>

</div>
<div bind:this={Guests} class=" bg-black w-screen h-217.5" id="Guests">
    <p class="text-2xl text-white text-center font-extrabold typewriter-10 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100">Guests Speakers section, being worked on but i have a good idea going foward</p>

</div>

<script>
    import asset_pentagon from "$lib/images/devcon-items/pentagon.png"
    import asset_corklogo from "$lib/images/devcon-items/logo.png"
    import asset_devcon from "$lib/images/devcon-items/devcon.png"
    import asset_ucc from "$lib/images/devcon-items/ucc.png"


    // for timer
    import { onMount } from "svelte";

    // baby ducks :3
    import jona from "$lib/images/1:1/jonathan.jpg"
    import el from "$lib/images/1:1/el.png"
    import scott from "$lib/images/1:1/scott.jpg"
    import ivan from "$lib/images/1:1/ivan.jpg"





  // =========================
  // Countdown to DevCon Logic
  // =========================
  let countdown = getCountdown();
  let seconds = 1000; 
  let minutes = seconds * 60;
  let hours = minutes * 60;
  let days = hours * 24;
  let daysD = 0;
  let hoursD = 0;
  let minutesD = 0;
  let secondsD = 0;
  function getCountdown() {
    const devconDate = new Date("2025-09-27T00:00:00");
    return devconDate.getTime() - Date.now();    
  }
  
  let interval;

  onMount(() => {
    interval = setInterval(() => {
      countdown = getCountdown();
      daysD = Math.floor(countdown/days);
      hoursD = Math.floor((countdown % days) / hours)
      minutesD = Math.floor ((countdown % hours) / minutes)
      secondsD = Math.floor ((countdown % minutes) / seconds)
    }, 1000);

    
  });



     

</script>



<main class="relative overflow-clip">
  <!-- Welcome: Logo and intro -->
  <section id="welcome" class="p-7 min-h-[200px] sm:min-h-[500px] lg:min-h-[700px] gap-y-38  flex flex-col lg:flex-row justify-center items-center gap-8 bg-black">

    <!-- Logo Group -->
    <div class="devcon-logo-group scale-250 sm:scale-200 md:scale-150 lg:scale-100 items-center right-3 sm:right-10 relative top-3">
      <div class="dlg-cork">
        <img class=" motion-delay-500 motion-duration-1000 motion-opacity-in-0" src="{asset_corklogo}" alt="logo">
      </div>
      <div class="dlg-devcon">
        <img class="motion-delay-700 motion-duration-1000 motion-opacity-in-0" src="{asset_devcon}" alt="devcon">
      </div>
      <img class="dlg-ucc motion-delay-1000 motion-duration-1000 motion-opacity-in-0" src="{asset_ucc}" alt="ucc-cs-logo">
    </div>

    <!-- Intro spiel -->
    <div class="max-w-[65ch] motion-delay-1500 motion-opacity-in-0 motion-translate-y-in-100 relative top-[-70px] sm:top-[0px]">
      <p>DevCon is a Cork-based <strong><em>Tech Conference</em></strong> about <strong><em>Bridging the Gap between Students and the Tech Industry</em></strong> that's held annually in UCC.</p>
      <p>Showcasing the exciting and innovative technology developments from all across Ireland</p>
      <p>Cork DevCon is an initiative by <a href="https://netsoc.co/" target="_blank">UCC Netsoc</a>.</p>
    </div>

  </section>

  <!-- Guest speakers -->
  <section id="guests" class="p-5 min-h-[200px] sm:min-h-[400px] lg:min-h-[700px] flex flex-col justify-center items-center gap-8 bg-black">
    <h1 class="mt-6 text-white text-center text-6xl font-extrabold motion-delay-1200 motion-opacity-in-0 motion-translate-y-in-100">Guests Speakers</h1>

    <p><strong class="text-center motion-delay-1400 motion-opacity-in-0 motion-translate-y-in-100" style="color: red;">To Be Announced.</strong></p>
  </section>

  <!-- Countdown -->
  <section id="countdown" class="p-5 min-h-[400px] lg:min-h-[700px] m-auto flex flex-col justify-center items-center gap-8 bg-black">
    <h1 class="mt-6 text-white text-center text-6xl z-10 font-extrabold motion-delay-1200 motion-opacity-in-0 motion-translate-y-in-100">Countdown To DevCon</h1>

    <div class="flex mt-6 flex-col lg:flex-row justify-center gap-4 m-4 z-30">
      <div class ="bg-amber-300 rounded-2xl w-30 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100" id="days">
        <p class="text-2xl text-white text-center font-extrabold typewriter-10 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100">{daysD} <br> Days</p>
      </div>
      <div class="bg-amber-400 rounded-2xl w-30 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100" id="hours">
        <p class="text-2xl text-white text-center font-extrabold typewriter-10 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100">{hoursD} <br> Hours</p>
      </div>
      <div class="bg-amber-500 rounded-2xl w-30 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100" id="minutes">
        <p class="text-2xl text-white text-center font-extrabold typewriter-10 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100">{minutesD} <br> Minutes</p>
      </div>
      <div class="bg-amber-600 rounded-2xl w-30 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100" id="seconds">
        <p class="text-2xl text-white text-center font-extrabold typewriter-10 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100">{secondsD} <br> Seconds</p>
      </div>
    </div>
  </section>

  <!-- Explainer -->
  <section id="explainer" class="p-5 min-h-[800px] lg:min-h-[700px]  flex flex-col justify-center items-center gap-8 bg-black">
    <h1 class="mt-6 text-white text-center text-6xl font-extrabold motion-delay-1200 motion-opacity-in-0 motion-translate-y-in-100">What's Happening this Year?</h1>
    <!-- ToDo: Add what is ACTUALLY happening during the day, what events, food, drink, etc.    for explaining to ppl who've never heard of devcon -->
     <div class="max-w-[60ch] space-y-5 mt-6 motion-delay-1500 motion-opacity-in-0 motion-translate-y-in-100">
    <p class="text-center">Attendees of can look forward to a diverse and engaging lineup of talks and presentations designed to inform, inspire, and connect. The event will include focused presentations by professionals in their respective fields on a diverse set of technologies.</p>
    <p class="text-center">There will be oppertunities to directly engage with speakers, ask questions and connect with fellow attendees from both academia and Industry </p>
    <p class="text-center">DevCon is designed to be inclusive and accessible, welcoming students, professionals, and anyone with a passion for technology and innovation.  </p>
      </div>
  </section>

  <!-- Tickets -->
  <section id="tickets" class=" min-h-[700px] lg:min-h-[1000px] motion-opacity-in-0 motion-translate-y-in-100 motion-blur-in-md bg-black">
    <div class=" relative items-center lg:top-[220px]">
    <h1 class=" text-white text-center text-6xl font-extrabold motion-delay-1200 motion-opacity-in-0 motion-translate-y-in-100">Get Tickets</h1>
    <h2 class="text-white text-center text-2xl font-extrabold motion-delay-1200 motion-opacity-in-0 motion-translate-y-in-100">Ticket sales go live 23rd July</h2>

    <div class="pt-6 mt-6 flex flex-col lg:flex-row gap-10 justify-center items-center">
        <a class="flex flex-col lg:min-h-[250px] justify-self-center lg:justify-start items-center gap-5 w-[95%] lg:w-[25%] bg-[#3f3301] text-slate-300 drop-shadow-2xl rounded-4xl hover:scale-105 duration-600 hover:cursor-pointer p-3" href="javascript:void(0)">
            <p class="text-center font-extrabold scale-200 text-white">Free</p>
            <button class="bg-amber-500 w-[60%] rounded-3xl text-center text-3xl font-extrabold scale-110">€ 0</button>
            <ul class="ml-2 list-disc">
                <li>Access to all dev con talks online</li>
                <li>Get emailed on <strong>September 27th</strong> with link to event</li>
            </ul>
        </a>

        <a class="flex flex-col lg:min-h-[250px] justify-start items-center gap-5 w-[95%] lg:w-[25%] bg-[#3f3301] text-slate-300 drop-shadow-2xl rounded-4xl relative   hover:scale-105 duration-600 hover:cursor-pointer p-3" href="javascript:void(0)">
            <p class="text-center font-extrabold scale-200 text-white">In-Person</p>
            <button class="bg-amber-500 w-[60%] rounded-3xl text-center text-3xl font-extrabold scale-110">€ 5</button>
            <ul class="ml-2 list-disc">
                <li>Access to <strong>all DevCon talks in person</strong></li>
                <li>Get emailed on <strong>September 27th</strong> with link to event</li>
                <li><strong>Food provided</strong> at event</li>
                <li>Access to <strong>recordings of talks</strong></li>
                <li><strong>Goodie Bag</strong></li>
            </ul>
        </a>

        <a class="flex flex-col lg:min-h-[250px] justify-start items-center gap-5 w-[95%] lg:w-[25%] bg-[#3f3301] text-slate-300 drop-shadow-2xl rounded-4xl hover:scale-105 duration-600 hover:cursor-pointer p-3" href="javascript:void(0)">
            <p class="text-center font-extrabold scale-200 text-white">Online</p>
            <button class="bg-amber-500 w-[60%] rounded-3xl text-center text-3xl font-extrabold scale-110">€ 2</button>
            <ul class="ml-2 list-disc">
                <li>Access to all <strong>DevCon talks online</strong></li>
                <li>Get emailed on <strong>September 27th</strong> with link to event</li>
                <li>Access to <strong>recordings of talks</strong></li>
                <li><strong>Goodie Bag</strong></li>
            </ul>
        </a>
    </div>

    <p class="mt-4 text-center">By ordering a ticket, you agree to receive emails informing you about the event. Read the <a href="policy#top">privacy policy</a> for more information.</p>
    </div>
  </section>

  <!-- The Team (+ Contact Us Section) -->
  <section id="the-team" class="p-5 min-h-[700px] flex flex-col justify-center items-center gap-8 bg-black">
    <h1 class="mt-6 text-white text-center text-6xl font-extrabold motion-delay-1200 motion-opacity-in-0 motion-translate-y-in-100">The DevCon Team</h1>


    <div class="w-full flex flex-col z-10 lg:flex-row gap-4 items-center justify-center motion-delay-1500 motion-opacity-in-0 motion-translate-y-in-100">
      <div class="person text-center">
        <img class="w-[300px] h-[300px] md:w-[400px] md:h-[400px]" src="{jona}" alt="">
        <h3 class="font-bold">Jonathan Namanda</h3>
        <h4>Director</h4>
      </div>
      <div class="person text-center">
        <img class="w-[300px] h-[300px] md:w-[400px] md:h-[400px]" src="{ivan}" alt="">
        <h3 class="font-bold">Ivan Fonagy</h3>
        <h4>Vice Director</h4>
      </div>
      <div class="person text-center">
        <img class="w-[300px] h-[300px] md:w-[400px] md:h-[400px]" src="{el}" alt="">
        <h3 class="font-bold">El Morley</h3>
        <h4>Sponsorship</h4>
      </div>
      <div class="person text-center">
        <img class="w-[300px] h-[300px] md:w-[400px] md:h-[400px]" src="{scott}" alt="">
        <h3 class="font-bold">Scott Widger</h3>
        <h4>Building Layout Managment</h4>
      </div>
      
    </div>

    <p class="text-center">Want to get in touch with us? Email us at <a href="mailto:mailto:devcon@netsoc.co" target="_blank">devcon@netsoc.co</a>.</p>

  </section>


  <!-- Todo: figure out how to deal with on hover scaling issue with ticket:online and pentagon in background -->
  <div class="">
    <!-- pentagons-->
    <img class=" absolute opacity-10  top-0 left-[-350px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{asset_pentagon}" alt="pentagon">
    <img class="max-lg:hidden absolute  top-[-330px] opacity-10 right-[210px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{asset_pentagon}" alt="pentagon">
    <img class=" absolute  bottom-[-330px] opacity-10 left-[100px]  size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{asset_pentagon}" alt="pentagon">
    <img class=" absolute max-lg:hidden bottom-[2430px] opacity-10 right-[100px]  size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{asset_pentagon}" alt="pentagon">
    <img class=" absolute max-lg:hidden bottom-[1530px] opacity-10 right-[100px]  size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{asset_pentagon}" alt="pentagon">
    <img class=" absolute max-lg:hidden  bottom-[2130px] opacity-10 left-[100px]  size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{asset_pentagon}" alt="pentagon">
    <img class=" absolute  bottom-[300px] motion-opacity-in-0 opacity-10 left-[1550px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{asset_pentagon}" alt="pentagon">  
    <img class=" absolute opacity-10   top-[800px] left-[-250px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{asset_pentagon}" alt="pentagon">
    <img class="absolute max-lg:hidden  top-[600px]  opacity-10 right-[10px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{asset_pentagon}" alt="pentagon">
  

  </div>
</main>

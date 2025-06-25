<script>
    import asset_pentagon from "$lib/images/devcon-items/pentagon.png"
    import asset_corklogo from "$lib/images/devcon-items/logo.png"
    import asset_devcon from "$lib/images/devcon-items/devcon.png"
    import asset_ucc from "$lib/images/devcon-items/ucc.png"

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
    const devconDate = new Date("2025-10-10T00:00:00");
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
  <section id="welcome" class="p-5 flex flex-row justify-center items-center gap-8">

    <!-- Logo Group -->
    <div class="devcon-logo-group">
      <div class="dlg-cork">
        <img class="max-w-[80%] motion-delay-500 motion-duration-1000 motion-opacity-in-0" src="{asset_corklogo}" alt="logo">
      </div>
      <div class="dlg-devcon">
        <img class="motion-delay-700 motion-duration-1000 motion-opacity-in-0" src="{asset_devcon}" alt="devcon">
      </div>
      <img class="dlg-ucc motion-delay-1000 motion-duration-1000 motion-opacity-in-0" src="{asset_ucc}" alt="ucc-cs-logo">
    </div>

    <!-- Intro spiel -->
    <div class="max-w-[65ch]">
      <p>DevCon is a Cork-based <strong><em>Tech Conference</em></strong> about <strong><em>Bridging the Gap between Students and the Tech Industry</em></strong> that's held annually in UCC.</p>
      <p>Showcasing the exciting and innovative technology developments from all across Ireland</p>
      <p>Cork Devcon is an initiative by <a href="https://netsoc.co/" target="_blank">UCC Netsoc</a>.</p>
    </div>

  </section>

  <!-- Guest speakers -->
  <section id="guests" class="p-5 flex flex-col justify-center items-center gap-8 bg-black">
    <h1 class="mt-6 text-white text-center text-6xl font-extrabold motion-delay-1200 motion-opacity-in-0 motion-translate-y-in-100">Guests Speakers</h1>

    <p><strong class="text-center motion-delay-1400 motion-opacity-in-0 motion-translate-y-in-100" style="color: red;">To Be Announced.</strong></p>
  </section>

  <!-- Countdown -->
  <section id="countdown" class="p-5 flex flex-col justify-center items-center gap-8">
    <h1 class="mt-6 text-white text-center text-6xl font-extrabold motion-delay-1200 motion-opacity-in-0 motion-translate-y-in-100">Countdown To DevCon</h1>

    <div class="flex flex-row justify-center gap-4 m-4">
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
  <section id="explainer" class="p-5 flex flex-col justify-center items-center gap-8 bg-black">
    <h1 class="mt-6 text-white text-center text-6xl font-extrabold motion-delay-1200 motion-opacity-in-0 motion-translate-y-in-100">What's Happening this Year?</h1>
    <!-- ToDo: Add what is ACTUALLY happening during the day, what events, food, drink, etc.    for explaining to ppl who've never heard of devcon -->
    <p class="text-center">Lorem ipsum dolor sit amet consectetur, adipisicing elit. Voluptas provident accusantium dicta dignissimos quas facere mollitia rem itaque cumque molestias.</p>
  </section>

  <!-- Tickets -->
  <section id="tickets" class="motion-opacity-in-0 motion-translate-y-in-100 motion-blur-in-md">
    <h1 class="my-6 text-white text-center text-6xl font-extrabold motion-delay-1200 motion-opacity-in-0 motion-translate-y-in-100">Get Tickets</h1>

    <div class="pt-6 flex flex-col lg:flex-row gap-10 justify-center">
        <a class="flex flex-col justify-start items-center gap-5 w-[95%] lg:w-[25%] bg-[#3f3301] text-slate-300 drop-shadow-2xl rounded-4xl hover:scale-105 duration-600 hover:cursor-pointer p-3" href="javascript:void(0)">
            <p class="text-center font-extrabold scale-200 text-white">Free</p>
            <button class="bg-amber-500 w-[60%] rounded-3xl text-center text-3xl font-extrabold scale-110">€ 0</button>
            <ul class="ml-2 list-disc">
                <li>Access to all dev con talks online</li>
                <li>Get emailed on (insert date) with link to event</li>
            </ul>
        </a>

        <a class="flex flex-col justify-start items-center gap-5 w-[95%] lg:w-[25%] bg-[#3f3301] text-slate-300 drop-shadow-2xl rounded-4xl relative top-[-1rem] scale-110 hover:scale-115 duration-600 hover:cursor-pointer p-3" href="javascript:void(0)">
            <p class="text-center font-extrabold scale-200 text-white">In-Person</p>
            <button class="bg-amber-500 w-[60%] rounded-3xl text-center text-3xl font-extrabold scale-110">€ 2</button>
            <ul class="ml-2 list-disc">
                <li>Access to <strong>all DevCon talks in person</strong></li>
                <li>Get emailed on <strong>October 1st</strong> with link to event</li>
                <li><strong>Food provided</strong> at event</li>
                <li>Access to <strong>recordings of talks</strong></li>
                <li><strong>Goodie Bag</strong></li>
            </ul>
        </a>

        <a class="flex flex-col justify-start items-center gap-5 w-[95%] lg:w-[25%] bg-[#3f3301] text-slate-300 drop-shadow-2xl rounded-4xl hover:scale-105 duration-600 hover:cursor-pointer p-3" href="javascript:void(0)">
            <p class="text-center font-extrabold scale-200 text-white">Online</p>
            <button class="bg-amber-500 w-[60%] rounded-3xl text-center text-3xl font-extrabold scale-110">€ 2</button>
            <ul class="ml-2 list-disc">
                <li>Access to all <strong>DevCon talks online</strong></li>
                <li>Get emailed on <strong>(insert date)</strong> with link to event</li>
                <li>Access to <strong>recordings of talks</strong></li>
                <li><strong>Goodie Bag</strong></li>
            </ul>
        </a>
    </div>

    <p class="mt-4 text-center">By ordering a ticket, you agree to receive emails informing you about the event. Read the <a href="policy#top">privacy policy</a> for more information.</p>
  </section>

  <!-- The Team (+ Contact Us Section) -->
  <section id="the-team" class="p-5 flex flex-col justify-center items-center gap-8 bg-black">
    <h1 class="mt-6 text-white text-center text-6xl font-extrabold motion-delay-1200 motion-opacity-in-0 motion-translate-y-in-100">The DevCon Team</h1>

    <p class="text-center">Want to get in touch with us? Email us at <a href="mailto:mailto:devcon@netsoc.co" target="_blank">mailto:devcon@netsoc.co</a>.</p>


    <div class="w-full flex flex-col lg:flex-row gap-4 items-center justify-center">
      <div class="person">
        <img src="" alt="">
        <h3>Person Name</h3>
        <h4>Job Title</h4>
      </div>
      <div class="person">
        <img src="" alt="">
        <h3>Person Name</h3>
        <h4>Job Title</h4>
      </div>
      <div class="person">
        <img src="" alt="">
        <h3>Person Name</h3>
        <h4>Job Title</h4>
      </div>
      <div class="person">
        <img src="" alt="">
        <h3>Person Name</h3>
        <h4>Job Title</h4>
      </div>
      <div class="person">
        <img src="" alt="">
        <h3>Person Name</h3>
        <h4>Job Title</h4>
      </div>
    </div>
  </section>


  <!-- Jonathan's Spinners (! ToDo: adjust so they don't extend page boundarys as they currently do) -->
  <div>
    <!-- pentagons-->
    <img class=" absolute z-0 opacity-10  top-0 left-[-350px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{asset_pentagon}" alt="pentagon">
    <img class=" absolute  z-0 top-[-330px] opacity-10 right-[210px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{asset_pentagon}" alt="pentagon">
    <img class=" absolute z-0 bottom-[-330px] opacity-10 left-[100px]  size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{asset_pentagon}" alt="pentagon">
    <img class=" absolute z-0 bottom-[-300px] motion-opacity-in-0 opacity-10 left-[1550px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{asset_pentagon}" alt="pentagon">
    <!-- second div petagons-->    
    <img class=" absolute opacity-10 z-0  top-[1400px] left-[-250px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{asset_pentagon}" alt="pentagon">
    <img class=" absolute  top-[1430px] opacity-10 right-[310px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{asset_pentagon}" alt="pentagon">
    <img class=" absolute  bottom-[-1430px] opacity-10 left-[200px]  size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{asset_pentagon}" alt="pentagon">
    <img class=" absolute bottom-[-1400px] motion-opacity-in-0 opacity-10 left-[1550px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{asset_pentagon}" alt="pentagon">
    <!--Third div pentagons -->
    <img class=" absolute opacity-10  top-[2300px] left-[-350px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{asset_pentagon}" alt="pentagon">
    <img class=" absolute  top-[-2330px] opacity-10 right-[210px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{asset_pentagon}" alt="pentagon">
    <img class=" absolute  bottom-[-2330px] opacity-10 left-[100px]  size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{asset_pentagon}" alt="pentagon">
    <img class=" absolute bottom-[-2300px] motion-opacity-in-0 opacity-10 left-[1550px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{asset_pentagon}" alt="pentagon">
  </div>
</main>
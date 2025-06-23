<script>
  import { onMount } from 'svelte';
  import pentagon from "$lib/images/devcon-items/pentagon.png"
  let countdown = getCountdown();
  let seconds = 1000; 
  let minutes = seconds * 60;
  let hours = minutes * 60;
  let days = hours * 24;
  let daysD;
  let hoursD;
  let minutesD;
  let secondsD;
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
<!-- plan here is to have p elements be inside flexbox, then flex-col for mobile devices and flex-row for anything over md breakpoint -->
<div   class="bg-black w-screen h-214.5 relative overflow-hidden overflow-x-clip border-5 border-black" id="Countdown">
  <p class="relative text-2xl text-white text-center  font-extrabold top-[100px] motion-delay-900 motion-opacity-in-0 motion-translate-y-in-100 scale-150">Countdown to Devcon</p>
   <img class=" absolute opacity-10  top-0 left-[-350px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
    <img class=" absolute  top-[-330px] opacity-10 right-[210px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
    <img class=" absolute  bottom-[-330px] opacity-10 left-[100px]  size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
    <img class=" absolute bottom-[-300px] motion-opacity-in-0 opacity-10 left-[1550px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon"> 
    <div class="relative justify-center  top-[400px] flex flex-row space-x-30 rounded-4xl scale-200">
      <div class ="bg-amber-300 rounded-2xl w-30  motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100" id="days">
    <p class="text-2xl text-white text-center  font-extrabold typewriter-10 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100">Days</p><p class="text-2xl text-white text-center  font-extrabold typewriter-10 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100">{daysD}</p>
    </div>
    <div class="bg-amber-400 rounded-xl w-30  motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100" id="hours">
    <p class="text-xl text-white text-center  font-extrabold typewriter-10 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100">Hours</p><p class="text-2xl text-white text-center  font-extrabold typewriter-10 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100">{hoursD}</p>
    </div>
    <div class="bg-amber-500 rounded-2xl w-30  motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100" id="minutes">
    <p class="text-2xl text-white text-center  font-extrabold typewriter-10 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100">minutes</p><p class="text-2xl text-white text-center  font-extrabold typewriter-10 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100">{minutesD}</p>
    </div>
    <div class="bg-amber-600 rounded-2xl w-30  motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100" id="seconds">
    <p class="text-2xl text-white text-center  font-extrabold typewriter-10 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100">seconds</p><p class="text-2xl text-white text-center  font-extrabold typewriter-10 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100">{secondsD}</p>
    </div>
    
    </div>

    
</div>
 

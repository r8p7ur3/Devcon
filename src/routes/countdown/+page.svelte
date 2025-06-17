<script>
  import { onMount } from 'svelte';

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

<div  class=" bg-black w-screen h-217.5" id="Countdown">
    <div class="relative  top-[100px] size">
      <div class ="bg-amber-300" id="days">
    <p class="text-2xl text-white text-center  font-extrabold typewriter-10 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100">Days</p><p class="text-2xl text-white text-center  font-extrabold typewriter-10 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100">{daysD}</p>
    </div>
    <div class="bg-amber-400" id="hours">
    <p class="text-2xl text-white text-center  font-extrabold typewriter-10 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100">Hours</p><p class="text-2xl text-white text-center  font-extrabold typewriter-10 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100">{hoursD}</p>
    </div>
    <div class="bg-amber-500" id="minutes">
    <p class="text-2xl text-white text-center  font-extrabold typewriter-10 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100">minutes</p><p class="text-2xl text-white text-center  font-extrabold typewriter-10 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100">{minutesD}</p>
    </div>
    <div class="bg-amber-600" id="seconds">
    <p class="text-2xl text-white text-center  font-extrabold typewriter-10 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100">seconds</p><p class="text-2xl text-white text-center  font-extrabold typewriter-10 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100">{secondsD}</p>
    </div>
    
    </div>

    
</div>
 

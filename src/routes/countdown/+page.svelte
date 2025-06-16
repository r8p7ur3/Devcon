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
    <p class="text-2xl text-white text-center  font-extrabold typewriter-10 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100">Days Hours Minutes Seconds
    </p>
    </div>

    
</div>

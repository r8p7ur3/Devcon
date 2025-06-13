<script>
  import { onMount } from 'svelte';

  let countdown = getCountdown();
  let minutes = countdown / 60;
  let hours = minutes / 60;
  let days = hours / 24;

  function getCountdown() {
    const devconDate = new Date("2025-10-10T00:00:00");
    return devconDate.getTime() - Date.now();
  }

  let interval;

  onMount(() => {
    interval = setInterval(() => {
      countdown = ((getCountdown()*1000));
      minutes = (countdown / 60);
      hours = ((countdown / 60)/60);
      days = (((countdown /60)/60)/ 240);
      
    }, 1000);

    
  });
</script>

<div  class=" bg-black w-screen h-217.5" id="Countdown">
    
    <p class="text-2xl text-white text-center font-extrabold typewriter-10 motion-delay-1300 motion-opacity-in-0 motion-translate-y-in-100">{days}</p>


    
</div>

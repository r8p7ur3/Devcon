<script lang="ts">
	import "../app.css";
  import pentagon from "$lib/images/devcon-items/pentagon.png"
	let { children } = $props();


	
	import "../style.css";

  
  import { page } from "$app/state";
</script>
<!--nothing here points to anything yet, ignore plz (unless there's something dumb im doing then do point out)-->
  <ul class="flex space-x-35 bg-black py-6 justify-center font-extrabold text-2xl w-screen">
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/">Home</a>
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/#About">About</a>
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/countdown">Countdown</a>
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/tickets">Tickets</a>
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/contact">Contact</a>
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/TheTeam">The Team</a>
  </ul>




{@render children()}


 

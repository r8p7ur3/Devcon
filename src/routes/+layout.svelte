<script lang="ts">
	import "../app.css";
  import pentagon from "$lib/images/devcon-items/pentagon.png"
	let { children } = $props();


	
	import "../style.css";

  
  import { page } from "$app/state";

  // for dropdown menu handing on smaller screen sizes
function OnToggle(){

};
</script>
<!--nothing here points to anything yet, ignore plz (unless there's something dumb im doing then do point out)-->
 <!-- desktop navbar-->
<ul id="navbar" class="hidden sticky z-10 top-0 md:flex md:space-x-10  bg-black py-6 md:justify-center font-extrabold text-2xl">
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/">Home</a>
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/#About">About</a>
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/countdown">Countdown</a>
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/tickets">Tickets</a>
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/contact">Contact</a>
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/TheTeam">The Team</a>
  </ul>

<!-- mobile navbar, im thinking hamburger buttone that opens dropdown, need a OnToggle function-->
<ul id="navbar" class="md:hidden sticky z-10 top-0 md:space-x-10  bg-black py-6 md:justify-center font-extrabold text-2xl">
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/">Home</a>
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/#About">About</a>
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/countdown">Countdown</a>
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/tickets">Tickets</a>
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/contact">Contact</a>
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/TheTeam">The Team</a>
  </ul>



{@render children()}


 

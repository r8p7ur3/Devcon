<script lang="ts">
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
    <img class=" absolute opacity-10  top-0 left-[-350px] size-110 scale-in-7 motion-duration-7000 motion-rotate-loop-360/reset motion-ease-linear" src="{pentagon}" alt="pentagon">
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/">Home</a>
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/#About">About</a>
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/countdown">Countdown</a>
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/tickets">Tickets</a>
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/contact">Contact</a>
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/TheTeam">The Team</a>
  </ul>

<!-- mobile navbar, im thinking hamburger buttone that opens dropdown, need a OnToggle function-->
 <button id="burger" class="flex sticky z-10 top-0 bg-black text-amber-50 md:hidden space-x-10 justify-center w-full text-2xl font-extrabold ">burger</button>
<ul id="navbar" class="hidden sticky z-10 top-0 space-x-10  bg-black py-6 md:justify-center font-extrabold text-2xl">
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/">Home</a>
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/#About">About</a>
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/countdown">Countdown</a>
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/tickets">Tickets</a>
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/contact">Contact</a>
    <a class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/TheTeam">The Team</a>
  </ul>



{@render children()}


 

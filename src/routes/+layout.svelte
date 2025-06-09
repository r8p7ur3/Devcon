<script lang="ts">
	import "../app.css";
  import pentagon from "$lib/images/devcon-items/pentagon.png"
	let { children } = $props();


	
	import "../style.css";

  
  import { page } from "$app/state";
</script>

  <ul class="flex space-x-35 bg-black py-6 justify-center font-extrabold text-2xl">
    <li class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/">Home</li>
    <li class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/about">About</li>
    <li class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/docs/components/navbar">Countdown</li>
    <li class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/pricing">Pricing</li>
    <li class="transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/contact">Contact</li>
  </ul>


<div class="p-8">

</div>

{@render children()}


 

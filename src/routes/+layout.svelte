<script lang="ts">
	import "../app.css";
  import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from "flowbite-svelte";
	
	let { children } = $props();
	
	import "../style.css";

  import { Alert } from "flowbite-svelte";
</script>

<Navbar>
  <NavBrand href="/">
    <img src="/images/flowbite-svelte-icon-logo.svg" class="me-3 h-6 sm:h-9" alt="Flowbite Logo" />
    <span class=" self-center text-xl font-semibold whitespace-nowrap dark:text-white">Flowbite</span>
  </NavBrand>
  <NavHamburger />
  <NavUl>
    <NavLi href="/">Home</NavLi>
    <NavLi href="/about">About</NavLi>
    <NavLi href="/docs/components/navbar">Navbar</NavLi>
    <NavLi href="/pricing">Pricing</NavLi>
    <NavLi href="/contact">Contact</NavLi>
  </NavUl>
</Navbar>


<div class="p-8">
<Alert>
<span class="font-medium">Info alert!</span>
I need to take a huge shit
</Alert>
</div>

{@render children()}


 

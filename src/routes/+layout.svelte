<script lang="ts">
  import assets_devcon from "$lib/images/devcon-items/devcon.png"
	let { children } = $props();

//hamburger menu
  import assets_menu from "$lib/images/devcon-items/menu.png"
	
	import "../style.css";


  

  // for dropdown menu handing on smaller screen sizes
function toggleNav(){
  let nav_toggle: HTMLElement | null = document.getElementById("header-nav-toggle");

  if (nav_toggle != null) {
    nav_toggle.addEventListener('click', function() {
        console.log('Nav button clicked')
        let nav: HTMLElement | null = document.getElementById("header-nav");

        if (nav != null) {
          console.log('Current display:', nav.style.display)
          switch (nav.style.display) {
              case 'none':
                  nav.style.display = 'flex';
                  break;
              case 'flex':
                  nav.style.display = 'none';
                  break
              default:
                  break;
          }
        }
  
    });
  }
};
</script>

<header class="sticky z-20 top-0 bg-black py-6 px-8 font-extrabold text-2xl flex flex-col lg:flex-row justify-between items-center">
  <a class="max-w-[45%] md:max-w-[20%] lg:max-w-[10%]" href="/#welcome"><img class=""  src="{assets_devcon}" alt="DevCon"></a>

  <button id="header-nav-toggle" class="visible lg:hidden text-4xl" onclick={toggleNav}>☰</button>
  
  <nav id="header-nav" style="display: none;" class="hidden lg:!flex flex-col lg:flex-row gap-8  lg:gap-2 lg:space-x-10 lg:justify-center"> <!-- This inline style display: none; is intentionally here and can be ignored, it is only here for the benefit of my JavaScript (as the script requires an inline style to "toggle" the mobile nav as I've done.) -->
    <a class="w-full lg:w-auto transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/#guests">Speakers</a>
    <a class="w-full lg:w-auto transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/#countdown">Countdown</a>
    <a class="w-full lg:w-auto transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/#explainer">Whats Happening?</a>
    <a class="w-full lg:w-auto transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/#tickets">Get Tickets</a>
    <a class="w-full lg:w-auto transform motion-safe:hover:scale-110 text-white hover:text-orange-600 transition duration-500" href="/#the-team">The Team</a>
  </nav>
</header>
{@render children()}


 

<script lang="ts">
let { children } = $props();

</script>
<nav>
<a href="/"> Home</a>
<a href="/about"> About Devcon </a>
<a href="/countdown"> Countdown </a>


</nav>

{@render children()}


 
<style>
@import './style.css';
p{
  color: green;
 }

</style>

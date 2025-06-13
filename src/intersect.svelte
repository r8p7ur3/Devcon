<script lang="ts">
  import { onDestroy, onMount } from "svelte";

  let inViewPort = false;
  let root;

  let observer = new IntersectionObserver((entries) => {
    entries.forEach((entry) => {
      if (entry.isIntersecting) {
        inViewPort = true;
        observer.disconnect();
      }
    });
  });

  onMount(() => {
    observer.observe(root);
  });

  onDestroy(() => {
    observer.disconnect();
  });
</script>



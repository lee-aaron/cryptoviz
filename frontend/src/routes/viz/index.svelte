<script lang="ts">
  import { onMount } from "svelte";

  let el;

  onMount(async () => {
    // mount three.js
    const scene = await import ("../../components/viz/scene");
    scene.createScene(el);
  });
</script>

<main>
  <h1>Visualizer</h1>

  <canvas bind:this={el} />
</main>

<style>
  main {
    justify-content: center;
    text-align: center;
  }
</style>

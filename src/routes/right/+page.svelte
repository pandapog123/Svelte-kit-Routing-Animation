<script lang="ts">
  import { linear } from "svelte/easing";
  import type { TransitionConfig } from "svelte/transition";

  function animateBody(node: HTMLElement): TransitionConfig {
    return {
      delay: 0,
      duration: 600,
      easing: linear,
      css: (t, u) => `transform: translate(${u * 100}vw);  position: absolute;`,
    };
  }
</script>

<div transition:animateBody>
  <h1>Right Page</h1>
</div>

<script lang="ts">
  import { linear } from "svelte/easing";
  import type { TransitionConfig } from "svelte/transition";

  function animateBody(node: HTMLElement): TransitionConfig {
    return {
      delay: 0,
      duration: 600,
      easing: linear,
      css: (t, u) => `opacity: ${1 - u}; position: absolute;`,
    };
  }
</script>

<div transition:animateBody>
  <h1>Error</h1>
  <div>
    <span>lost?</span>

    <a href="/">Go Home!</a>
  </div>
</div>

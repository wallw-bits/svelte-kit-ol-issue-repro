<script lang="ts">
  import Feature from "ol/Feature";
  import { onMount } from "svelte";

  let feature;

  onMount(() => {
    feature = new Feature({ value: 42 });
  });
</script>

{#if feature}
  <p>It worked!</p>
{/if}

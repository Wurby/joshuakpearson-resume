<script>
  import { navigate } from "svelte-routing/src/history";

  export let href = "";
  export let external = false;

  const handleClick = () => {
    navigate(href);
  };
  $: target = external ? "_blank" : "_self";
</script>

<span
  class="text-teal-800 border-b border-teal-800 dark:border-teal-300 hover:text-teal-600 hover:border-teal-600 dark:text-teal-300 dark:hover:border-teal-400 dark:hover:text-teal-400"
>
  {#if external}
    <a {href} {target}>
      <slot />
    </a>
  {:else}
    <span on:click={handleClick} on:keydown={handleClick}>
      <slot />
    </span>
  {/if}
</span>

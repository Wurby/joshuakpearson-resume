<script lang="ts">
  import { navigate } from "svelte-routing/src/history";

  export let classList = "";
  export let onClick = () => {
    navigate("/" + title.toLowerCase());
  };
  export let title = "";
</script>

<div
  class="flex space-x-2 justify-baseline align-center hover:text-slate-600 dark:hover:text-slate-300 cursor-pointer"
  on:click={onClick}
  on:keydown={onClick}
>
  <div class="m-auto">
    <svg
      xmlns="http://www.w3.org/2000/svg"
      fill="none"
      viewBox="0 0 24 24"
      stroke-width="1.5"
      stroke="currentColor"
      class={"w-6 h-6" + classList}
    >
      <slot />
    </svg>
  </div>
  <div class="m-auto">
    <p class="text-sm">{title}</p>
  </div>
</div>

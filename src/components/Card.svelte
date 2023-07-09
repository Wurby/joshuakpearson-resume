<script>
  import Icon from "./icons/Icon.svelte";

  export let className = "";

  export let arrow = false;
</script>

<div
  class="flex-col rounded-lg shadow-lg ring-1 ring-slate-500/30 bg-slate-200 text-slate-900 dark:bg-slate-800 dark:text-slate-100 mb-4 {className}"
>
  <section class="p-2 grid grid-cols-4 grid-rows-2">
    <div class="col-span-1 row-span-2 w-12 h-12 my-auto ml-auto mr-2">
      <slot name="image" />
    </div>
    <div class="col-span-2 m-auto border-b-2 border-slate-500">
      <slot name="title" />
    </div>
    <div class="col-span-2 text-sm text-slate-600 dark:text-slate-400 m-auto">
      <slot name="subtitle" />
    </div>
  </section>
  <section
    class="flex justify-between md:justify-around bg-slate-300 dark:bg-slate-700 p-2 ring-1 ring-slate-400/50 dark:ring-slate-500/50 text-sm font-semibold"
  >
    <div class="my-auto">
      <slot name="accent1" />
    </div>
    {#if arrow}
      <div class="self-center">
        <Icon
          ><path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M17.25 8.25L21 12m0 0l-3.75 3.75M21 12H3"
          /></Icon
        >
      </div>
    {:else}
      <div class="w-4 h-4 m-1" />
    {/if}
    <div class="my-auto">
      <slot name="accent2" />
    </div>
  </section>
  <section class="p-2 text-sm">
    <slot name="content" />
  </section>
</div>

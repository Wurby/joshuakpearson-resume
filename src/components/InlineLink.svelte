<script>
  export let href = "";
  export let external = false;

  $: target = external ? "_blank" : "_self";
</script>

<span
  class="text-teal-800 border-b border-teal-800 dark:border-teal-300 hover:text-teal-600 hover:border-teal-600 dark:text-teal-300 dark:hover:border-teal-400 dark:hover:text-teal-400"
>
  <a {href} {target}>
    <slot />
  </a>
</span>

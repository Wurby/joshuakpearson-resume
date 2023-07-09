<script>
  export let src = "https://picsum.photos/200/300";
  export let alt = "avatar";
  export let classList =
    "w-12 h-12 object-cover rounded-full ring-2 ring-slate-400";
</script>

<img {src} {alt} class={classList} />

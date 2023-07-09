<script lang="ts">
  import { onMount } from "svelte";
  import Icon from "./icons/Icon.svelte";

  let dark = localStorage.getItem("dark");

  onMount(() => {
    const html = document.querySelector("html");

    if (dark === "true") {
      html.classList.add("dark");
    }
  });

  const toggleDarkMode = () => {
    const html = document.querySelector("html");
    html.classList.toggle("dark");
    if (html.classList.contains("dark")) {
      localStorage.setItem("dark", "true");
    } else {
      localStorage.setItem("dark", "false");
    }
  };
</script>

<div
  class="ring-2 ring-slate-500/50 flex justify-around space-x-reverse flex-row-reverse fixed w-full h-16 bottom-0 bg-slate-300 dark:bg-slate-800"
>
  <Icon onClick={toggleDarkMode}>
    <path
      stroke-linecap="round"
      stroke-linejoin="round"
      d="M12 18v-5.25m0 0a6.01 6.01 0 001.5-.189m-1.5.189a6.01 6.01 0 01-1.5-.189m3.75 7.478a12.06 12.06 0 01-4.5 0m3.75 2.383a14.406 14.406 0 01-3 0M14.25 18v-.192c0-.983.658-1.823 1.508-2.316a7.5 7.5 0 10-7.517 0c.85.493 1.509 1.333 1.509 2.316V18"
    />
  </Icon>
  <Icon title="Contact">
    ><path
      stroke-linecap="round"
      stroke-linejoin="round"
      d="M7.5 8.25h9m-9 3H12m-9.75 1.51c0 1.6 1.123 2.994 2.707 3.227 1.129.166 2.27.293 3.423.379.35.026.67.21.865.501L12 21l2.755-4.133a1.14 1.14 0 01.865-.501 48.172 48.172 0 003.423-.379c1.584-.233 2.707-1.626 2.707-3.228V6.741c0-1.602-1.123-2.995-2.707-3.228A48.394 48.394 0 0012 3c-2.392 0-4.744.175-7.043.513C3.373 3.746 2.25 5.14 2.25 6.741v6.018z"
    />
  </Icon>
  <Icon title="Portfolio">
    ><path
      stroke-linecap="round"
      stroke-linejoin="round"
      d="M9 17.25v1.007a3 3 0 01-.879 2.122L7.5 21h9l-.621-.621A3 3 0 0115 18.257V17.25m6-12V15a2.25 2.25 0 01-2.25 2.25H5.25A2.25 2.25 0 013 15V5.25m18 0A2.25 2.25 0 0018.75 3H5.25A2.25 2.25 0 003 5.25m18 0V12a2.25 2.25 0 01-2.25 2.25H5.25A2.25 2.25 0 013 12V5.25"
    />
  </Icon>
  <Icon title="Home">
    ><path
      stroke-linecap="round"
      stroke-linejoin="round"
      d="M2.25 12l8.954-8.955c.44-.439 1.152-.439 1.591 0L21.75 12M4.5 9.75v10.125c0 .621.504 1.125 1.125 1.125H9.75v-4.875c0-.621.504-1.125 1.125-1.125h2.25c.621 0 1.125.504 1.125 1.125V21h4.125c.621 0 1.125-.504 1.125-1.125V9.75M8.25 21h8.25"
    />
  </Icon>
</div>

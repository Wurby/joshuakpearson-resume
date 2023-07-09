<script lang="ts">
  import Nav from "./components/Nav.svelte";
  import { Router, Route } from "svelte-routing";
  import Home from "./pages/Home.svelte";
  import Portfolio from "./pages/Portfolio.svelte";
  import Contact from "./pages/Contact.svelte";
  import { onMount } from "svelte";
  import { navigate } from "svelte-routing/src/history";

  document
    .querySelector("body")
    .classList.add("bg-slate-50", "dark:bg-slate-900");

  onMount(() => {
    if (location.pathname === "/") {
      navigate("/home");
    }
  });
</script>

<Router basepath="/">
  <div
    class="h-full bg-slate-50 text-slate-800 dark:bg-slate-900 dark:text-slate-100"
  >
    <div class="mb-16">
      <main class="p-2">
        <Route path="/contact" component={Contact} />
        <Route path="/portfolio" component={Portfolio} />
        <Route path="/home" component={Home} />
      </main>
      <Nav />
    </div>
  </div>
</Router>

<script>
  import { selected } from "./stores/selected.store.js";
  import Header from "./layout/Header.svelte";
  import Main from "./layout/Main.svelte";
  import Footer from "./layout/Footer.svelte";
  export let name;
</script>

<style>

</style>

<div class="row" id="nav">
  <Header />
</div>
<div class="clearfix" />
<div class="row" id="main">
  <Main />
</div>
<div class="clearfix" />
<div class="row" id="footer">
  <Footer />
</div>

<script>
  import MainHeader from "./components/MainHeader.svelte";
  import Styleguide from "./components/Styleguide.svelte";
  import MainFooter from "./components/MainFooter.svelte";
  import CreateAccount from "./components/CreateAccount.svelte";
</script>

<MainHeader />
<main class="main">
  <div class="container">
    <CreateAccount />
  </div>
</main>
<MainFooter />

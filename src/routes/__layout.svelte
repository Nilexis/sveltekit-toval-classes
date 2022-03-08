<script lang="ts">
  import Header from "$lib/header/Header.svelte";
  import "../app.css";
  import logo from "$lib/svelte-logo.svg";
</script>

<Header />

<main>
  <slot />
</main>

<footer>
  <hr />
  <p class="flex">
    Built using &nbsp
    <a href="https://kit.svelte.dev" class="flex">
      <img src={logo} id="svelte-logo" alt="Svelte logo" />
      SvelteKit
    </a>
  </p>
  <p class="text-gray-500 text-xs">&copy;2022 Almog Hershkovitz. All rights reserved.</p>
</footer>

<style>
  main {
    flex: 1;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 1rem;
    width: 100%;
    max-width: 1024px;
    min-height: 80vh;
    margin: 0 auto;
    box-sizing: border-box;
  }

  footer {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 40px;
  }

  footer a {
    font-weight: bold;
  }

  #svelte-logo {
    height: 1.3rem;
  }

  @media (min-width: 480px) {
    footer {
      padding: 40px 0;
    }
  }
</style>

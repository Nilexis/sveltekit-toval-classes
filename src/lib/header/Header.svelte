<script lang="ts">
  import { page } from "$app/stores";

  $: p = $page.url.pathname;

  const pages = [
    {
      name: "פתיחת בקשה",
      route: "/request"
    },
    {
      name: "בקשות שנפתחו",
      route: "/request/history"
    }
  ];
</script>

<header>
  <nav class="bg-gray-800" dir="rtl">
    <div class="mx-auto px-2">
      <div class="flex items-center justify-between h-16">
        <div class="flex-1 flex items-center justify-start">
          <div class="flex items-center">
            <img
              class="lg:block h-8 w-auto mx-4"
              src="https://tailwindui.com/img/logos/workflow-logo-indigo-500-mark-white-text.svg"
              alt="TovalClasses"
            />
          </div>
          <div class="ml-6">
            <div class="flex">
              {#each pages as page}
                <a
                  href={page.route}
                  class="{p === page.route
                    ? 'bg-gray-900 text-white'
                    : 'text-gray-300 hover:bg-gray-700 hover:text-white'} px-3 py-2 rounded-md text-sm font-medium"
                >
                  {page.name}
                </a>
              {/each}
            </div>
          </div>
        </div>
      </div>
    </div>
  </nav>
</header>

<style>
</style>

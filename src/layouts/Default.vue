<template>
  <div class="layout font-nunito text-gray-900">
    <header class="bg-black text-white tracking-widest">
      <div
        class="w-full max-w-7xl mx-auto align-end flex justify-between p-4 font-light"
      >
        <div>
          <g-link class="uppercase hover:text-red-500" to="/">{{
            $static.metadata.siteName
          }}</g-link>
          <div
            class="inline-block mx-4 px-3 py-1 border border-red-500 text-red-500 uppercase tracking-widest text-sm text-center rounded"
          >
            <p class="text-xs">In development</p>
          </div>
        </div>
        <nav class="nav">
          <a
            href="https://www.luissantanderart.com"
            target="_blank"
            class="px-2 uppercase hover:text-red-500"
            to="/"
          >
            <svg
              class="w-5 -mt-1 mr-2 inline-block"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 20 20"
              fill="currentColor"
            >
              <path
                d="M11 3a1 1 0 100 2h2.586l-6.293 6.293a1 1 0 101.414 1.414L15 6.414V9a1 1 0 102 0V4a1 1 0 00-1-1h-5z"
              />
              <path
                d="M5 5a2 2 0 00-2 2v8a2 2 0 002 2h8a2 2 0 002-2v-3a1 1 0 10-2 0v3H5V7h3a1 1 0 000-2H5z"
              />
            </svg>

            <span>3D Portolio</span>
          </a>

          <g-link
            class="nav__link ml-2 px-2 uppercase  hover:text-red-500"
            to="/about/"
            >About</g-link
          >
        </nav>
      </div>
    </header>
    <slot />
    <footer class="bg-black text-white text-sm p-4 text-center">
      <div
        class="w-full max-w-7xl text-center mx-auto flex justify-center uppercase tracking-wider"
      >
        <a
          class="mx-2 hover:text-red-500"
          href="https://www.artstation.com/luissantander"
          >ArtStation</a
        >
        <a class="mx-2 hover:text-red-500" href="https://twitter.com/yetzero"
          >Twitter</a
        >
        <a
          class="mx-2 hover:text-red-500"
          href="https://www.youtube.com/channel/UCZm8FtR5xt96qpqhzSsrBNA"
          >YouTube</a
        >
        <a
          class="mx-2  hover:text-red-500"
          href="https://www.linkedin.com/in/luissantander/"
          >LinkedIn</a
        >
      </div>
    </footer>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style>
body {
  margin: 0;
}
</style>

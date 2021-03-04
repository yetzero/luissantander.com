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
            class="px-2 uppercase hover:text-red-500"
            >Portfolio</a
          >
          <!--<g-link class="px-2 uppercase hover:text-red-500" to="/projects/">
            Projects
          </g-link> -->

          <g-link
            class="nav__link ml-2 px-2 uppercase  hover:text-red-500"
            to="/about/"
            >About</g-link
          >
        </nav>
      </div>
    </header>
    <transition name="fade" appear>
      <main>
        <slot />
      </main>
    </transition>
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

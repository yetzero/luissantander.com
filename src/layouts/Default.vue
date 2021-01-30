<template>
  <div class="layout font-nunito">
    <header class="bg-black text-white tracking-widest">
      <div class="w-full max-w-7xl mx-auto flex justify-between p-4">
        <g-link class="uppercase hover:text-red-500" to="/">{{
          $static.metadata.siteName
        }}</g-link>
        <nav class="nav">
          <a
            href="https://www.luissantanderart.com"
            target="_blank"
            class="px-2 uppercase hover:text-red-500"
            to="/"
            >Portolio</a
          >
          <g-link
            class="nav__link px-2 uppercase  hover:text-red-500"
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

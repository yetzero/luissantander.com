<template>
  <Layout>
    <div class="flex align-middle w-full max-w-7xl mx-auto">
      <div class="flex-shrink-0 flex-grow-0 flex flex-col justify-center ">
        <g-image
          class="rounded-full mx-auto mb-10"
          src="~/assets/img/avatar.jpg"
          width="200"
        />
      </div>
      <div class="px-10 py-40">
        <h1 class="text-6xl mb-10">About me</h1>
        <p>
          I'm a developer and artist from Santiago Chile. I work in several
          areas: web development, 3D modeling, rendering, game engines, etc.
        </p>
        <p>
          Maybe I can help you with your project. Let me know at
          <a class="text-red-500" href="mailto:hello@luissantanderart.com"
            >hello@luissantanderart.com</a
          >
        </p>
      </div>
    </div>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: "About me | luissantander.com",
  },
};
</script>

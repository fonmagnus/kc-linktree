<template>
  <div>
    <div class="mx-auto w-full px-4 py-10">
      <div class="mx-auto w-40"> <img src="~static/kc-logo.png" class = "mb-8"></div>
      <h1 class="font-mono text-5xl text-center font-bold text-gray-800 mb-4">{{ title }}</h1>
      <h2 class="font-mono text-xl text-center font-semi-bold text-gray-700 mb-6">{{ subtitle }}</h2>
      <p class="font-mono text-l text-center font-regular text-gray-500 mb-10">{{ description }}</p>
      <div class="grid justify-center grid-row gap-4 mb-10">
        <Link v-for="Link in Links" :key="Link.title" :title="Link.title" :description="Link.description" :url="Link.url" />
      </div>
      <div class="font-mono text-s text-center font-regular text-gray-800">{{footer}}</div>
    </div>
  </div>
</template>

<script>
import Link from '~/components/Link.vue';

export default {
  components: {
    Link
  },
  data() {
    return {
      title: 'KOKOCODER',
      subtitle: 'Hello, nice to see you! 👋',
      description: 'Connect with us through our social medias',
      footer: '© 2023 Kokocoder Group',
      Links: [
        {
          title: 'PUBLIC RELATION WHATSAPP 💬',
          description: 'For further information and registration.',
          url: 'https://wa.me/6287785857166'
        },
        {
          title: 'KC INSTAGRAM 📸',
          description: 'Check out our activities and updates!',
          url: 'https://www.instagram.com/kokocoder'
        },
        {
          title: 'KC WEBSITE 💻',
          description: 'Check out to know more about us!',
          url: 'https://kokocoder.com/'
        },
        {
          title: 'Portal 🌐',
          description: 'Where the exciting part begins :>',
          url: 'https://portal.kokocoder.com/'
        }
      ]
    }
  }
}
</script>

<style>

</style>

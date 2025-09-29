<template>
  <UPage>
    <UPageHero
      title="Acoustic Symposium"
      headline="Edition 4 | 27th May 2026"
      description="Let’s engineer a quieter, smarter, and more sustainable future—together."
      :links="[
        { label: 'Watch the promo', icon: 'i-simple-icons-youtube', color: 'secondary', size: 'xl', to: 'https://youtu.be/6wJT2MvFaYA', target: '_blank' },
        { label: 'Register now', icon: 'i-heroicons-arrow-right-20-solid', size: 'xl', to: '/getting-started', disabled: !status?.registration }
      ]"
      :ui="{ root: 'main-bg', description: 'text-white font-bold', headline: 'text-white', links: 'gap-x-4' }"
    >
      <template #title>
        <div class="text-4xl font-extrabold leading-tight tracking-tight text-white sm:text-5xl lg:text-6xl drop-shadow-lg -mt-4">
          <span class="text-secondary">Acoustic</span> Symposium
        </div>
      </template>
    </UPageHero>

    <UPageSection
      title="About the Symposium"
      description="As the automotive industry transitions to electrification, automation, and sustainable design, NVH engineering is taking center stage—shaping comfort, character, and performance in next-generation vehicles."
      orientation="horizontal"
      reverse
      :ui="{ container: 'lg:py-16' }"
    >
      <template #description>
        <p class="pb-2">
          As the automotive industry transitions to electrification, automation, and sustainable design, NVH engineering is taking center stage—shaping comfort, character, and performance in next-generation vehicles.
        </p>
        <p>Join us at Acoustics for an Evolving World, where experts from across the mobility ecosystem will explore the latest innovations in acoustic simulation, materials, AI applications, and vehicle-level NVH development. With a focus on practical solutions and future challenges, this event is your opportunity to connect, share, and shape the acoustic landscape of the future.</p>
      </template>

      <img
        class="rounded-lg"
        src="/IMG-20190918-WA0011.jpg"
      >
    </UPageSection>

    <USeparator
      class="lg:px-48"
      size="md"
      type="dashed"
    />

    <UPageSection
      title="Key Topics"
      description="Explore the forefront of acoustic innovation with sessions on cutting-edge simulation techniques, advanced materials, AI-driven solutions, and comprehensive vehicle-level NVH strategies. Our symposium is designed to provide you with practical insights and future-focused discussions that will empower you to tackle the evolving challenges in the mobility sector."
      :features="[
        { title: 'Porous & Damping Materials', description: 'Explore the latest advancements in porous materials and damping technologies that are transforming noise reduction and vibration control in vehicles. Learn about innovative applications and case studies that highlight their effectiveness in enhancing acoustic performance.' },
        { title: 'Acoustic Simulation', description: 'Delve into the latest advancements in acoustic simulation technologies, including finite element analysis (FEA), boundary element methods (BEM), and hybrid approaches. Learn how these tools are being used to predict and mitigate noise issues in modern vehicles.' },
        { title: 'Advanced Materials', description: 'Discover innovative materials and composites that are revolutionizing noise reduction and vibration control. Explore case studies on the application of lightweight, sustainable materials that enhance acoustic performance without compromising vehicle efficiency.' },
        { title: 'AI-Driven Solutions', description: 'Examine the role of artificial intelligence and machine learning in acoustic engineering. From predictive maintenance to real-time noise monitoring, explore how AI is transforming the way we approach NVH challenges.' },
        { title: 'Vehicle-Level NVH Development', description: 'Gain insights into holistic NVH strategies that encompass the entire vehicle architecture. Learn about integrated approaches to noise and vibration control that consider powertrain, chassis, and body interactions for optimal acoustic performance.' }
      ]"
      :ui="{ container: 'lg:py-16' }"
    />

    <USeparator
      class="lg:px-48"
      size="md"
      type="dashed"
    />

    <UPageSection
      title="Venue"
      description="The Acoustic Symposium will be held at Lingotto Fiere, a renowned congress hall in Turin, Italy. The venue offers modern facilities and is easily accessible from the city center. Join us in this iconic location for a unique experience in automotive acoustics and NVH engineering."
      orientation="horizontal"
      :ui="{ container: 'lg:py-16' }"
    >
      <img
        class="rounded-lg"
        src="/pista-500-torino.webp"
      >
    </UPageSection>

    <USeparator
      class="lg:px-48"
      size="md"
      type="dashed"
    />

    <UPageCTA
      class="overflow-hidden"
      variant="naked"
      title="Register Your Interest"
      description="Registration will open soon. In the meantime, you can view highlights from our previous symposiums and register your interest to attend the next event."
    >
      <div>
        <form
          class="flex flex-col sm:flex-row gap-2 w-full max-w-2xl mx-auto"
          action="https://formspree.io/f/maykzvdp"
          method="POST"
        >
          <input
            class="flex-1 px-4 py-3 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-secondary focus:border-transparent"
            type="email"
            name="email"
            placeholder="Enter your email"
            required
          >

          <button
            class="px-6 py-3 bg-secondary text-white font-semibold rounded-md hover:bg-secondary-dark focus:outline-none focus:ring-2 focus:ring-secondary focus:ring-offset-2"
            type="submit"
          >
            Notify Me
          </button>
        </form>

        <div class="text-center mt-4 text-sm text-gray-600">
          We respect your privacy. Unsubscribe at any time.
        </div>
      </div>
    </UPageCTA>
  </UPage>
</template>

<script setup lang="ts">
const { data: status } = await useFetch('/api/status')

useSeoMeta({
  title: 'Welcome',
  description: 'Join us at Acoustics for an Evolving World, where experts from across the mobility ecosystem will explore the latest innovations in acoustic simulation, materials, AI applications, and vehicle-level NVH development.'
})
</script>

<style scoped>
.main-bg {
  background: url('/splash2.jpeg') no-repeat center center fixed;
  background-size: auto;
}
</style>

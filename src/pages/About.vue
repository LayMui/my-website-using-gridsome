<template>
  <Layout>
    <main>
      <header class="max-w-xl md:max-w-2xl xl:max-w-3xl mx-auto text-center px-6 pt-24">
        <h1 class="text-4xl sm:text-5xl md:text-6xl font-sans font-bold mb-1">About</h1>
        <p class="text-grey-dark text-lg sm:text-3xl">My Introduction &hellip;</p>
      </header>
      <nav class="absolute top-0 left-0 z-20 mt-6 ml-6">
        <g-link to="/" class="text-gray-900 border-gray-400 text-sm border opacity-75 hover:opacity-100 rounded-full px-4 py-2 transition-opacity duration-300">&larr; Home</g-link>
      </nav>
      <article class="max-w-xl md:max-w-2xl xl:max-w-3xl mx-auto px-6 sm:px-12 pt-16 border-b border-gray-300 pb-10 mb-16">
        <div class="markdown text-lg leading-normal text-gray-700">
          <p>Hi there. My name is LayMui, I am a software developer with focus in testing.</p>
          <p>Microsoft has a term of such role called SDET</p>
          <hr>
          <h2>Communication skills</h2>
          <p>This is a soft skill that I want to work on</p>
          <p>It's all about relationship how I can build good rapport and relationship with people</p>
          <h2>From QA to expand into DevOps</h2>
          <p>A dream written down with a date become a goal</p>
          <p>A goal broken down into steps becomes a plan</p>
          <p>A plan backed by actions make your dream a reality</p>
           <p>Roadmap of 2021: How to move to become DevTestOps or TestDevOps</p>
           <p>What are the necessary skillsets to acquire</p>
            <p class="text-muted text-center">
      watch this -> <a href="youtube channel" target="_blank">https://www.youtube.com/watch?v=9pZ2xmsSDdo</a>
    </p>

           <p>My first step is the AZ400 course and to get the certication</p>
           <p>頑張ってください</p>

        </div>
      </article>
      <site-footer class="pb-8 sm:pb-10" />
    </main>
  </Layout>
</template>

<script>
import config from '~/.temp/config.js'
import SiteFooter from '@/components/Footer'

export default {
  components: {
    SiteFooter
  },
  metaInfo () {
    return {
      title: 'About',
      meta: [
        {
          key: 'description',
          name: 'description',
          content: this.ogDescription
        },

        { property: "og:type", content: 'article' },
        { property: "og:title", content:'About' },
        { property: "og:description", content: this.ogDescription },
        { property: "og:url", content: `${this.config.siteUrl}/about/` },
        { property: "og:image", content: this.ogImageUrl },

        { name: "twitter:card", content: "summary_large_image" },
        { name: "twitter:title", content: 'About' },
        { name: "twitter:description", content: this.ogDescription },
        { name: "twitter:site", content: "@laymui" },
        { name: "twitter:creator", content: "@laymui" },
        { name: "twitter:image", content: this.ogImageUrl },
      ],
    }
  },
  computed: {
    config () {
      return config
    },
    ogDescription () {
      return 'Introduction to the Bleda blog starter for Gridsome.'
    },
    ogImageUrl () {
      return `${this.config.siteUrl}/images/bleda-card.png`
    }
  },
}
</script>

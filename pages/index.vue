<template>
  <section class="section">
    <div class="columns">
      <div
        v-for="(feature, i) of features"
        :key="i"
        class="column">
        <div class="card">
          <header class="card-header">
            <p class="card-header-title has-text-grey">
              {{ feature.title }}
            </p>
          </header>
          <div class="card-content">
            <div class="content has-text-centered">
              <b-icon
                :icon="feature.icon"
                size="is-large"
                type="is-primary"/>
            </div>
          </div>
          <footer class="card-footer">
            <div
              class="card-footer-item"
              v-html="feature.content"/>
          </footer>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import BLogo from '@/components/Logo'

export default {
  name: 'HomePage',
  components: {BLogo},
  data() {
    return {
      features: [
        { icon: 'github-circle', title: 'Free', content: `<span>Open source on <a href="https://github.com/buefy/buefy"> GitHub</a></span>` },
      ]
    }
  }
}
</script>

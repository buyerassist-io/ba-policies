<template>
  <Layout :sidebar="false">
    <div class="content">
      <h1>BuyerAssist Compliance Policies</h1>
      <p class="lead">This is the public version of BuyerAssist's HIPAA Compliance Policies. For pull requests, or to download the source, please visit the github project for this site. If you have any further questions, please reach out to us at hello@datica.com.</p>
      <nav>
        <!-- To use other icons here, you need to import them in the Shortcut component -->
        <Shortcut link="/purpose" text="Purpose and Scope" icon="align-center-icon" />
        <Shortcut link="/roles" text="Roles and Responsibilities" icon="users-icon" />
        <Shortcut link="/policies" text="Policies" icon="check-square-icon" />
      </nav>
      <GitLink class="git" size="large" />
      <span class="sitelink">Visit <a href="https://datica.com/" title="BuyerAssist Main Site">BuyerAssist</a> main site</span>
    </div>
  </Layout>
</template>

<script>
import GitLink from '~/components/GitLink.vue'
import Shortcut from '~/components/Shortcut.vue'

export default {
  components: {
    GitLink,
    Shortcut
  },
  metaInfo: {
    title: 'BuyerAssist Compliance Policies',
    meta: [
      { key: 'description', name: 'description', content: 'BuyerAssist open-source compliance policies.' }
    ]
  }
}
</script>

<style lang="scss" scoped>
.content {
  display: flex;
  flex-direction: column;
}

h1 {
  text-align: center;
  max-width: 600px;
  margin: 1.5em auto 1.5em;

  @include respond-above(md) {
    max-width: 1000px;
  }
}

h2 {
  font-size: 1.4rem;
  margin: 0;
}

nav {
  display: flex;
  justify-content: space-between;
  flex-direction: column;

  @include respond-above(sm) {
    flex-direction: row;
  }
}

.git {
  margin: 3em 0 0;
  align-self: center;

  @include respond-above(md) {
    margin: 5em 0 0;
  }
}
p.lead {
  margin: 1rem auto 3rem auto;
  max-width: 50em;
}
.sitelink {
  margin: 1rem;
  text-align: center;
  a {
    font-weight: bold;
  }
}
</style>

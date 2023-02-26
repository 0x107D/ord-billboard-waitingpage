<template>
  <div id="app">
    <Head>
      <Title>OrdinalBoard - The immortal map</Title>
      <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    </Head>
    <header>
      <BigButton />
    </header>
    <main>
      <p>Hey Legend ! We'll be there in the next few minutes...</p>
      <p>
        <a href="https://discord.gg/3d634w89Vk" target="_blank">Join the discord</a>
      </p>
    </main>
  </div>
</template>

<script>
import BigButton from '@/components/BigButton/index.vue';

export default {
  components: {
    BigButton,
  }
}
</script>

<style lang="scss">
#app {
  background-color: $blackColor;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  overflow-y: auto;

  header {
    max-width: 480px;
    margin: 0 auto;
    margin-top: 10vh;

    .big-button {
      font-size: 4rem;
      height: 82px;
      line-height: 82px;

      .ti-cursor {
        font-size: 4rem;
      }
    }
  }

  main {
    max-width: 480px;
    margin: 42px auto;

    p {
      font-size: 22px;
      color: gainsboro;
    }
  }
}
</style>

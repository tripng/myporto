<template>
  <div class="parent">
    <div class="squareLine">
      <h1 class="openTag">{</h1>
      <div class="main">
        <particles-bg type="cobweb" num="10" color="#ffffff" :bg="true" />
        <Nuxt />
      </div>
      <h1 class="closeTag">}</h1>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DefaultLayout',
}
</script>

<style lang="scss" scoped>
.parent {
  position: relative;
  height: 100vh;
  padding: 20px;
  .squareLine {
    border: 1px solid $c-md-light;
    z-index: 999;
    color: $c-md-light;
    height: 100%;
    position: relative;
    .openTag {
      position: absolute;
      margin: 10px 0 0 10px;
    }
    h1 {
      color: $c-md-light;
    }

    .main {
      z-index: 1;
      padding: 1rem 4rem;
      height: 100%;
      @media screen and (max-width: $s-sm) {
        padding: 1rem 1.2em;
      }
    }

    .closeTag {
      position: absolute;
      right: 10px;
      bottom: 10px;
    }
  }
}
</style>

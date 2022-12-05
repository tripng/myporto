<template>
  <div class="container">
    <div class="head">
      <Header title="Projects" desc="Informatics Engineering" />
      <Navbar />
    </div>
    <div class="parent-content">
      <div class="content">
        <h1 v-if="$route.params.slug == 'thriftAja'">
          {{ $route.params.slug }} project hasn't been published yet
        </h1>
        <h1 v-if="$route.params.slug == 'bkkbn'">
          {{ $route.params.slug }} project hasn't been published yet
        </h1>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: '404Page',
}
</script>

<style lang="scss" scoped>
.parent-content {
  width: 80%;

  .content {
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;

    h1 {
      text-align: center;
      font-weight: bold;
    }
  }
}
</style>

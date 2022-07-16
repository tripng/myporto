<template>
  <div class="container">
    <div class="head">
      <Header />
      <Navbar />
    </div>
    <div class="parent-content">
      <div class="content">
        <p class="last-paragraph"></p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PageHome',
  head() {
    return {
      title: 'Home | TP',
    }
  },
}
</script>

<style lang="scss" scoped></style>

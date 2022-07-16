<template>
  <div class="container">
    <div class="head">
      <Header />
      <Navbar />
    </div>
    <div class="parent-content">
      <div class="content">
        <h2>Hi !</h2>
        <p>
          My name is Tri Pananggung i am a 6th semester informatics engineering
          student at Malang state university
        </p>
        <p class="last-paragraph">
          I like programming because it's like playing a game even though it
          often makes me dizzy :D
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MainPage',
  head() {
    return {
      title: 'TP',
    }
  },
}
</script>

<style lang="scss" scoped>
.parent-content {
  width: 50%;
  @media screen and (max-width: $s-sm) {
    height: 100%;
    width: 100%;
    align-items: flex-end;
  }
}
.content {
  width: 30%;
  position: absolute;
  bottom: 0;
  right: 0;
  .last-paragraph {
    margin-top: 20px;
  }
  @media screen and (max-width: $s-sm) {
    position: relative;
    width: 100%;
  }
}
</style>

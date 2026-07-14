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
        Tri Pananggung here, a programmer who really likes clean code and automation
        </p>
        <p class="last-paragraph">
        An Information Technology graduate and Fullstack Web Developer with experience building efficient, scalable, and user-centric modern web applications. He has deep expertise in the Laravel, React, Inertia.js, and Tailwind CSS ecosystems. He is well-versed in designing complex systems such as Computer Assisted Test (CAT) applications and developing automation to improve operational efficiency. He is highly dedicated to writing clean code and is always enthusiastic about exploring new technologies.
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

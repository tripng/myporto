<template>
  <div class="container">
    <div class="head">
      <Header />
      <Navbar />
    </div>
    <div class="parent-content">
      <div class="content">
        <p class="last-paragraph">
          Halo, saya Tri Wahyu Ade Firmansyah Pananggung — fullstack developer
          asal Gorontalo. Saya menguasai web (Nuxt JS, Laravel, CodeIgniter,
          Vue.js), aplikasi mobile dengan Flutter, aplikasi desktop dengan
          Electron, serta bot Telegram, menggunakan Js, PHP, Python, dan Dart.
          Saat ini saya berkarya sebagai teknisi di MAN 1 Kota Gorontalo
          (2025&ndash;now), sebelumnya di Jayatama Information System dan Trans
          TV (2024&ndash;2025), dan terus belajar lewat freeCodeCamp serta
          Coursera (2023&ndash;now). Beberapa project yang telah saya buat:
          SIPANDU, Al-Harmain POS, Sheet Game, Teams Transmedia, Jayatama
          Information System, MAN 1 Kota Gorontalo, serta bot @man1kotagorontalo
          dan @MANSATV. Hobi saya renang, gym, dan mendengarkan musik.
        </p>
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

<style lang="scss" scoped>
.last-paragraph {
  text-align: right;
  color: $c-md-light;
  font-size: 1.1em;
  line-height: 1.6;
  margin-top: 1em;

  @media screen and (max-width: $s-sm) {
    font-size: 0.8em;
    line-height: 1.4;
  }
}
</style>

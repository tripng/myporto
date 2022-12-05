<template>
  <div class="container">
    <div class="head">
      <Header title="About Me" desc="Nobody is perfect" />
      <Navbar />
    </div>
    <div class="parent-content">
      <div class="content">
        <img src="~/assets/img/me.png" alt="Tri Pananggung" />
        <div class="my-desc">
          const myProfile = () => <span>{</span>
          <p>
            <span class="property">'name'</span> : 'Tri Wahyu Ade Firmansyah
            Pananggung',
          </p>
          <p><span class="property">'place'</span> : ['Gorontalo','Malang'],</p>
          <p>
            <span class="property">'hoby'</span> : ['watching anime', 'playing
            games'],
          </p>
          <p><span class="property">'birthday'</span> : 28-09-2002,</p>
          <p>
            <span class="property">'framework'</span> : {'Nuxt
            JS','Laravel','CodeIgniter'},
          </p>
          <p>
            <span class="property">'programming language'</span> :
            {'Js','PHP','Python'},
          </p>
          <span>}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PageAbout',
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
  .content {
    position: absolute;
    bottom: 0;
    right: 0;
    img {
      display: block;
      margin: auto;
      width: 200px;
      border-radius: 50%;
      padding: 10px;
      border-bottom: 2px solid $c-light;
      margin-bottom: 30px;

      @media screen and (max-width: $s-sm) {
        width: 100px;
      }
    }
    .my-desc {
      span {
        color: yellow;
      }
      p {
        margin: 5px 20px;
        @media screen and (max-width: $s-sm) {
          font-size: 0.7em;
        }
      }
      .property {
        color: lightgreen;
      }
    }
  }
}
</style>

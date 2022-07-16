<template>
  <div class="nav">
    <ul>
      <NavChild
        v-for="item in navlist"
        :key="item.to"
        :to="item.to"
        :title="item.title"
        :exact="item.exact"
        class="link"
      />
    </ul>
  </div>
</template>

<script>
export default {
  name: 'NavbarPage',
  data() {
    return {
      navlist: [
        {
          to: '',
          title: 'Home',
        },
        {
          to: 'about',
          title: 'About Me',
        },
        {
          to: 'resume',
          title: 'Resume',
        },
        {
          to: 'projects',
          title: 'Projects',
          exact: false,
        },
        {
          to: 'contact',
          title: 'Contact',
        },
      ],
    }
  },
}
</script>

<style lang="scss">
.nav {
  margin-top: 3em;
  @media screen and (max-width: $s-sm) {
    margin-top: 1em;
  }
  .link {
    color: $c-light;
    transition: 0.5s;
    &:hover {
      color: $c-md-light;
    }
  }
  a.nuxt-link-exact-active {
    color: $c-md-light;
    border-bottom: 1px solid $c-md-light;
  }
  a.nuxt-link-active {
    color: $c-md-light;
    border-bottom: 1px solid $c-md-light;
  }
  ul {
    @media screen and (max-width: $s-sm) {
      display: flex;
      justify-content: space-between;
      font-size: 0.9em;
    }
  }
}
</style>

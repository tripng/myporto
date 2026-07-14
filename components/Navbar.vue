<template>
  <div class="nav">
    <ul>
      <NavChild
        v-for="item in navlist"
        :key="item.to"
        :to="item.to"
        :title="item.title"
        :icon="item.icon"
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
          icon: 'home',
        },
        {
          to: 'about',
          title: 'About Me',
          icon: 'about',
        },
        {
          to: 'resume',
          title: 'Resume',
          icon: 'resume',
        },
        {
          to: 'projects',
          title: 'Projects',
          icon: 'projects',
          exact: false,
        },
        {
          to: 'contact',
          title: 'Contact',
          icon: 'contact',
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
      flex-wrap: wrap;
      gap: 0.6em 1em;
      font-size: 0.9em;
    }
  }
  .nav-icon {
    display: none;
    width: 1.6em;
    height: 1.6em;
    color: $c-light;
    filter: grayscale(1);
    svg {
      width: 100%;
      height: 100%;
      display: block;
    }
  }
  @media screen and (max-width: $s-sm) {
    ul {
      justify-content: space-around;
    }
    .link {
      border-bottom: none !important;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .nav-text {
      display: none;
    }
    .nav-icon {
      display: block;
    }
    a.nuxt-link-active,
    a.nuxt-link-exact-active {
      .nav-icon {
        color: $c-md-light;
        filter: none;
      }
    }
  }
}
</style>

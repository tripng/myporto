<template>
  <div>
    <NuxtLink :to="to" class="link project-list">
      <img :src="require('~/assets/img/project/' + img + '.png')" alt="" />
      <span class="date">{{ desc }}</span>
      <h1 class="project-title">{{ title }}</h1>
    </NuxtLink>
  </div>
</template>

<script>
export default {
  name: 'ProjectComponent',
  props: {
    to: {
      type: String,
      default: '/',
    },
    img: {
      type: String,
      default: '',
    },
    desc: {
      type: String,
      default: '',
    },
    title: {
      type: String,
      default: '',
    },
  },
}
</script>

<style lang="scss" scoped>
.project-list {
  position: relative;
  border-bottom: 1px solid $c-md-light;
  display: flex;
  justify-content: flex-end;

  @media screen and (max-width: $s-sm) {
    width: 100%;
  }
  &:hover {
    :is(h1, span) {
      color: $c-md-light;
    }
    h1::after {
      content: '●';
      margin: 0 5px;
      color: $c-light;
    }
    img {
      display: block;
    }
  }

  img {
    z-index: 10;
    display: none;
    will-change: transform;
    transition: 0.5s;
    position: absolute;
    left: 0;
    bottom: -90%;
    transform-style: preserve-3d;
    animation: projectImage 1s;
  }

  .project-title {
    font-size: 3em;
    transition: 0.5s;
    @media screen and (max-width: $s-sm) {
      font-size: 1.5em;
    }
  }
  .date {
    color: $c-light;
    align-self: flex-end;
  }
}
</style>

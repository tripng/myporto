<template>
  <li>
    <NuxtLink class="link" :to="'/' + to" :exact="exact">{{ title }}</NuxtLink>
  </li>
</template>

<script>
export default {
  name: 'NavChild',
  props: {
    to: {
      type: String,
      default: '/',
    },
    title: {
      type: String,
      default: '',
    },
    exact: {
      type: Boolean,
      default: true,
    },
  },
}
</script>

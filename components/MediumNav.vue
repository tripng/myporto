<template>
  <li>
    <NuxtLink class="link" :to="'/' + to" :exact="exact">
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512">
        <path :d="d" />
      </svg>
    </NuxtLink>
  </li>
</template>
<script>
export default {
  name: 'MediumNav',
  props: {
    to: {
      type: String,
      default: '/',
    },
    d: {
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

<template>
  <div>
    <h1>{{ title }}</h1>
    <span>{{ desc }}</span>
  </div>
</template>

<script>
export default {
  name: 'HeaderComponent',
  props: {
    title: {
      type: String,
      default: 'Tri Pananggung',
    },
    desc: {
      type: String,
      default: 'Informatics Engineering Student',
    },
  },
}
</script>

<style lang="scss">
h1 {
  color: $c-light;
  font-size: 3.5em;
  font-weight: 1;

  @media screen and (max-width: $s-sm) {
    font-size: 1.5em;
  }
}
</style>

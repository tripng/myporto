<template>
  <div class="container">
    <div class="head">
      <Header title="Contact" desc="Nice to know you" />
      <Navbar />
    </div>
    <div class="parent-content">
      <div class="content">
        <div class="info">
          <p>0822-9202-1678</p>
          <p>triwahyupananggung10@gmail.com</p>
        </div>
        <a class="link" href="https://github.com">Github</a>
        <a
          class="link"
          href="https://www.linkedin.com/in/tri-pananggung-276b43188/"
          >Linkedln</a
        >
        <a class="link" href="https://www.instagram.com/triwahyu.png/"
          >Instagram</a
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PageContact',
  head() {
    return {
      title: 'Contact | TP',
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
  width: 100%;
  position: absolute;
  bottom: 0;
  right: 0;
  display: flex;
  flex-direction: column;
  text-align: right;

  .info {
    margin-bottom: 20px;
  }
  .link {
    color: $c-light;
    text-decoration: none;
    transition: 0.5s;
    &:hover {
      color: $c-md-light;

      &::after {
        content: '>';
      }
      &::before {
        content: '<';
      }
    }
  }
}
</style>

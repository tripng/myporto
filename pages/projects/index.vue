<template>
  <div class="container">
    <div class="head">
      <Header title="Projects" desc="My Project" />
      <Navbar />
    </div>
    <div class="parent-content">
      <div class="content">
        <ul>
          <li>
            <a
              href="https://talent.callon.id"
              target="_blank"
              class="link project-list"
            >
              <img src="~/assets/img/project/talent-callon.png" alt="" />
              <span class="date">Apply For A Job / 2022</span>
              <h1 class="project-title">Tallent Callon</h1>
            </a>
            <a
              href="https://ratihharry.netlify.app"
              target="_blank"
              class="link project-list"
            >
              <img src="~/assets/img/project/wedding.png" alt="" />
              <span class="date">Wedding / 2021</span>
              <h1 class="project-title">RatihHarry</h1>
            </a>
            <a
              target="_blank"
              href="http://tripananggung.nurulfikri.com/"
              class="link project-list"
            >
              <img src="~/assets/img/project/mbkm.png" alt="" />
              <span class="date">Save Task / 2022</span>
              <h1 class="project-title">Assignment MBKM</h1>
            </a>
            <a
              target="_blank"
              href="https://tripng.github.io/myportfolio/"
              class="link project-list"
            >
              <img src="~/assets/img/project/oldporto.png" alt="" />
              <span class="date">Portfolio / 2022</span>
              <h1 class="project-title">Old Portofolio</h1>
            </a>
            <ProjectLink
              v-for="(item, index) in projectLink"
              :key="index"
              :to="item.to"
              :img="item.img"
              :desc="item.desc"
              :title="item.title"
            />
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PageProject',
  data() {
    return {
      projectLink: [
        {
          to: 'projects/thriftAja',
          img: 'thriftaja',
          desc: 'Ecommerce / 2022',
          title: 'ThriftAja',
        },
        {
          to: 'projects/bkkbn',
          img: 'bkkbn',
          desc: 'Business / 2022',
          title: 'BKKBN Gorontalo',
        },
      ],
    }
  },
  head() {
    return {
      title: 'Projects | TP',
    }
  },
}
</script>

<style lang="scss" scoped>
.parent-content {
  width: 80%;
  display: flex;
  align-items: flex-end;

  @media screen and (max-width: $s-sm) {
    width: 100%;
  }
}
.content {
  width: 100%;
}
.project-list {
  position: relative;
  border-bottom: 1px solid $c-md-light;
  display: flex;
  justify-content: flex-end;
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
    @media screen and (max-width: $s-sm) {
      font-size: 0.8em;
    }
  }
}
@keyframes projectImage {
  0% {
    transform: translateX(-30px);
  }
  100% {
    transform: translateX(0px);
  }
}
</style>

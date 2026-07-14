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
              href="https://github.com/aldy-san/gpm"
              target="_blank"
              class="link project-list"
            >
              <img src="~/assets/img/project/gpm.png" alt="" />
              <span class="date">Kuisioner / 2022</span>
              <h1 class="project-title">Gugus Penjamin Mutu</h1>
            </a>
            <a
              href="https://callon.id/"
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
              href="https://github.com/tripng/tugas-mbkm"
              class="link project-list"
            >
              <img src="~/assets/img/project/mbkm.png" alt="" />
              <span class="date">Save Task / 2022</span>
              <h1 class="project-title">Assignment MBKM</h1>
            </a>
            <a
              href="https://play.google.com/store/apps/details?id=com.teams.user&hl=id"
              target="_blank"
              class="link project-list"
            >
              <img src="~/assets/img/project/teams-transmedia.png" alt="" />
              <span class="date">Mobile App / 2024</span>
              <h1 class="project-title">Teams Transmedia</h1>
            </a>
            <a
              href="https://jis.jayatama.id/index.php"
              target="_blank"
              class="link project-list"
            >
              <img src="~/assets/img/project/jis.png" alt="" />
              <span class="date">Web App / 2024</span>
              <h1 class="project-title">Jayatama Information System</h1>
            </a>
            <a
              href="https://sipandu.man1kotagorontalo.sch.id/"
              target="_blank"
              class="link project-list"
            >
              <img src="~/assets/img/project/sipandu.png" alt="" />
              <span class="date">SIPANDU / 2025-2026</span>
              <h1 class="project-title">SIPANDU</h1>
            </a>
            <a
              href="https://github.com/tripng/alharmain-pos"
              target="_blank"
              class="link project-list"
            >
              <img src="~/assets/img/project/alharmain.png" alt="" />
              <span class="date">Desktop App / 2025</span>
              <h1 class="project-title">Al-Harmain POS</h1>
            </a>
            <a
              href="https://github.com/tripng/sheetgame"
              target="_blank"
              class="link project-list"
            >
              <img src="~/assets/img/project/sheetgame.png" alt="" />
              <span class="date">Web Game / 2023</span>
              <h1 class="project-title">Sheet Game</h1>
            </a>
            <a
              href="https://man1kotagorontalo.sch.id/"
              target="_blank"
              class="link project-list"
            >
              <img src="~/assets/img/project/man1gorontalo.png" alt="" />
              <span class="date">Website / 2025-now</span>
              <h1 class="project-title">MAN 1 Kota Gorontalo</h1>
            </a>
            <a
              href="https://t.me/man1kotagorontalo"
              target="_blank"
              class="link project-list"
            >
              <img src="~/assets/img/project/bot-man1.png" alt="" />
              <span class="date">Telegram Bot / 2026</span>
              <h1 class="project-title">Bot @man1kotagorontalo</h1>
            </a>
            <a
              href="https://t.me/MANSATV"
              target="_blank"
              class="link project-list"
            >
              <img src="~/assets/img/project/bot-mansatv.png" alt="" />
              <span class="date">Telegram Bot / 2026</span>
              <h1 class="project-title">Bot @MANSATV</h1>
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
    padding: 0 4px;
  }
}
.content {
  width: 100%;
  max-height: 78vh;
  overflow-y: auto;
  scrollbar-width: none;
  -ms-overflow-style: none;

  &::-webkit-scrollbar {
    display: none;
  }
  @media screen and (max-width: $s-sm) {
    padding: 0 4px;
  }
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
    width: clamp(180px, 22vw, 300px);
    height: auto;
    transform-style: preserve-3d;
    animation: projectImage 1s;

    @media screen and (max-width: $s-sm) {
      position: static;
      display: none;
      width: 70%;
      max-width: 320px;
      margin: 12px auto 0;
      bottom: auto;
      left: auto;
    }
  }

  &:focus-within > img,
  &:active > img {
    @media screen and (max-width: $s-sm) {
      display: block;
    }
  }

  .project-title {
    font-size: 3em;
    transition: 0.5s;
    overflow-wrap: anywhere;

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

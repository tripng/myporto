<template>
  <div class="container">
    <div class="head">
      <Header title="Resume" desc="Life is Learning" />
      <Navbar />
    </div>
    <div class="parent-content">
      <div class="content">
        <div class="course">
          <h3>■ Course</h3>
          <div class="list">
            <span>Feb 2022 - Apr 2022</span>
            <h1>Codepolitan X PZN</h1>
          </div>
          <p>
            Learning program provided by codepolitan and taught by professional
            programmers from Programmer Zaman Now here I learn backend for web
            development, from basics to using the Laravel framework.
          </p>
        </div>
        <div class="experience">
          <h3>■ Experience</h3>
          <div class="list">
            <span>Feb 2022 - Jul 2022</span>
            <h1>Nurul Fikri Computer</h1>
          </div>
          <p>
            organizes courses in Digital Marketing, Management, Programming and
            Web, Linux Networking & Cloud Computing, Data Science, Database,
            Office Application, Graphic Design, Video Editing, Multimedia,
            Engineering Design from basic to advanced level. here I learn as a
            fullstack developer
          </p>
        </div>
        <div class="education">
          <h3>■ Education</h3>
          <div class="list">
            <span>Aug 2019 - Now</span>
            <h1>State University of Malang</h1>
          </div>
          <p>
            Bachelor of Engineering, Informatic Engineering. Cumulative GPA:
            3.44/4.00
          </p>
          <div class="list">
            <span>Mar 2016 - 2019</span>
            <h1>Madrasah Aliyah Gorontalo</h1>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ResumePage',
  head() {
    return {
      title: 'Resume | TP',
    }
  },
}
</script>

<style lang="scss" scoped>
.parent-content {
  width: 70%;
  @media screen and (max-width: $s-sm) {
    width: 100%;
  }
}
.content {
  p {
    text-align: right;
    color: $c-md-light;
    margin-top: 10px;
  }
  .list {
    display: flex;
    justify-content: flex-end;

    span {
      align-self: flex-end;
      @media screen and (max-width: $s-sm) {
        font-size: 0.8em;
      }
    }
    h1 {
      font-size: 3em;
      @media screen and (max-width: $s-sm) {
        font-size: 1.4em;
      }
    }
  }
  :is(.course, .experience, .education) {
    text-align: right;
    margin: 5em 0;
  }
}
</style>

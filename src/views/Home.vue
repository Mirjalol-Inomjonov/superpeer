<template>
  <div class="home">
    <Header />
    <Main />
    <Section />
    <Service />
    <Intro />
    <Footer />
  </div>
</template>

<script>
import Main from "../components/Main.vue";
import Header from "../components/Header.vue";
import Section from "../components/Section.vue";
import Service from "../components/Service.vue";
import Intro from "../components/Intro.vue";
import Footer from "../components/Footer.vue";

export default {
  name: "Home",
  components: {
    Header,
    Main,
    Section,
    Service,
    Intro,
    Footer,
  },
};
</script>

<style lang="scss">
* {
  padding: 0;
  margin: 0;
}
@keyframes circleScale {
  from {
    -webkit-transform: scale(1);
    transform: scale(1);
  }

  50% {
    -webkit-transform: scale(0.85);
    transform: scale(0.85);
  }

  to {
    -webkit-transform: scale(1);
    transform: scale(1);
  }
}
.button {
  font-family: sans-serif !important;
  padding: 13px 16px;
  outline: none;
  background: #ffd338;
  border-radius: 8px;
  border: none;
  font-family: Roboto;
  font-style: normal;
  font-weight: normal;
  font-size: 16px;
  line-height: 22px;
  text-transform: uppercase;
  align-items: center !important;

  &:hover {
    opacity: 0.8;
  }
}

.button-md {
  font-family: sans-serif;
  padding: 16px 32px;
  background: #ffedc2;
  border-radius: 8px;
  font-size: 16px;
  line-height: 22px;
  text-align: center;
  text-transform: uppercase;
  color: #222222;
  border: none;
  outline: none;

  &:hover {
    background: #ffe29e;
  }
}

.title {
  font-family: sans-serif;
  font-style: normal;
  font-weight: normal;
  font-size: 64px;
  line-height: 70px;
  text-align: center;
  letter-spacing: 1px;
  color: #222222;

  &_md-bold {
    font-weight: bold;
    font-size: 48px;
    line-height: 53px;
  }

  &_sm {
    font-weight: bold;
    font-size: 22px;
    line-height: 29px;
  }
}

.subtitle {
  font-family: sans-serif;
  font-style: normal;
  font-weight: normal;
  font-size: 22px;
  line-height: 29px;
  text-align: center;
  color: #555555;

  &_md {
    font-size: 16px;
    line-height: 22px;
  }

  &_sm {
    font-size: 12px;
    line-height: 17px;
  }

  &_color-black {
    color: #000;
  }
}

.card {
  border: none;
  background-color: transparent;
  &__img {
    width: 100%;
  }
}

.teacher-card {
  background-color: transparent;
  text-align: center;
  width: 244px;

  &__img {
    width: 100%;
    margin-bottom: 24px;
  }
}

@media screen and (max-width: 576px) {
  .card {
    margin: 50px 0;
  }
}
</style>

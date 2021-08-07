<template>
  <section class="service">
    <div class="container text-center">
      <h2 class="title title-md-bold">What can Superpeer do for you?</h2>
      <p class="subtitle subtitle_md">
        Turn your audience into loyal, paying followers with our seamless video
        experience and subscriber management tools.
      </p>

      <div
        class="
          teacher-card-wrapper
          d-flex
          align-items-center
          justify-content-between
        "
      >
        <div class="teacher-card">
          <img
            class="teacher-card__img"
            src="../assets/service-img1.png"
            alt=""
          />
          <h3 class="title title_sm">Engage with your audience</h3>
          <p class="subtitle subtitle_md">
            Connect with your subscribers through interactive livestreams, 1:1s,
            and our newest feature, Series.
          </p>
        </div>
        <div class="teacher-card">
          <img
            class="teacher-card__img"
            src="../assets/service-img2.png"
            alt=""
          />
          <h3 class="title title_sm">Manage easier</h3>
          <p class="subtitle subtitle_md">
            We take care of scheduling, payments, and protecting your privacy,
            so that you don’t have to.
          </p>
        </div>
        <div class="teacher-card">
          <img
            class="teacher-card__img"
            src="../assets/service-img3.png"
            alt=""
          />
          <h3 class="title title_sm">Earn, your way</h3>
          <p class="subtitle subtitle_md">
            Set your own rates and earn revenue through weekly livestreams,
            channel subscriptions, and even donations.
          </p>
        </div>
      </div>

      <button class="button-md">All Features</button>

      <div class="carusel">
        <h2 class="title_md-bold">Don’t just take our word for it</h2>
        <div class="carusel__slider">
          <VueSlickCarousel :arrows="true" :dots="true" id="slickCarusel">
            <div>
              <p class="subtitle">
                “I've been using Superpeer with about 10-12 calls per week, and
                so far the experience has been flawless.”
              </p>
            </div>
            <div>
              <p class="subtitle">
                “I've been using Superpeer with about 10-12 calls per week, and
                so far the experience has been flawless.”
              </p>
            </div>
            <div>
              <p class="subtitle">
                “I've been using Superpeer with about 10-12 calls per week, and
                so far the experience has been flawless.”
              </p>
            </div>
            <div>
              <p class="subtitle">
                “I've been using Superpeer with about 10-12 calls per week, and
                so far the experience has been flawless.”
              </p>
            </div>
          </VueSlickCarousel>
        </div>
        <img
          class="carusel__avatar mb-3"
          src="../assets/carusel img.png"
          alt=""
        />
        <p class="subtitle subtitle_md">Janine Sickmeyer</p>
        <p class="subtitle subtitle_sm">Tech entrepreneur & Angel investor</p>
      </div>
    </div>
    <img class="service__vector" src="../assets/intro vector.png" alt="" />
  </section>
</template>

<script>
import VueSlickCarousel from "vue-slick-carousel";
import "vue-slick-carousel/dist/vue-slick-carousel.css";
// optional style for arrows & dots
import "vue-slick-carousel/dist/vue-slick-carousel-theme.css";
export default {
  components: { VueSlickCarousel },
  name: "Service",
};
</script>

<style lang="scss">
.service {
  overflow: hidden;
  padding-top: 119px;
  background: linear-gradient(180deg, #fde6e6 0%, #ffffff 100%);

  .title {
    margin-bottom: 29px;
  }

  .teacher-card-wrapper {
    margin: 103px 0 80px 0;
  }

  .button-md {
    margin-bottom: 150px;
  }

  .carusel {
    position: relative;
    padding: 99px 177px 64px;
    background: linear-gradient(
      180deg,
      #fffaec 0%,
      rgba(255, 255, 255, 0) 100%
    );

    &__slider {
      margin: 107px 0 88px 0;
    }
    .slick-prev:before,
    .slick-next:before {
      color: #333;
    }
  }

  &__vector {
    width: 100%;
  }
}

@media screen and (max-width: 576px) {
  .service {
    padding-top: 35px;
    .title {
      font-weight: bold;
      font-size: 28px;
      line-height: 43px;
    }

    .teacher-card-wrapper {
      margin-top: 90px;
      margin-bottom: 10px;
      display: flex;
      flex-direction: column;

      .teacher-card {
        margin-bottom: 25px;
        .title {
          font-size: 24px;
          line-height: 36px;
        }
      }
    }

    .button-md {
      margin-bottom: 60px;
    }

    .carusel {
      padding: 0;
    }
  }
  // #slickCarusel {
  //   width: 100%;
  // }
}
</style>

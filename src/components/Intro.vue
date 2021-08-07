<template>
  <section class="intro">
    <div class="container text-center">
      <div class="row">
        <div class="col-12 col-sm-8 offset-sm-2">
          <div class="text-right">
            <h2 class="title title_md-bold">Introducing Superpeer Series</h2>
            <img
              class="intro__arrowe"
              src="../assets/intro arrowe.png"
              alt=""
            />
          </div>
          <p class="subtitle subtitle_md mb-sm-5 mt-sm-5">
            With series, you can create and sell any combination of on-demand
            video and live stream content. With cohort-based classes you can
            interact with your audience in a more engaging way.
          </p>
        </div>
      </div>

      <img class="intro__img" src="../assets/intro img.png" alt="" />

      <div
        class="
          intro-teacher-card
          d-flex
          align-items-center
          justify-content-between
        "
      >
        <div class="teacher-card">
          <img
            class="teacher-card__img"
            src="../assets/into card img1.png"
            alt=""
          />
          <h3 class="title title_sm">Customize the content</h3>
          <p class="subtitle subtitle_md">
            Organize your live streams, pre-recorded videos, and hosted events
            into purchasable content packages for your audience.
          </p>
        </div>
        <div class="teacher-card">
          <img
            class="teacher-card__img"
            src="../assets/into card img2.png"
            alt=""
          />
          <h3 class="title title_sm">Set the pace</h3>
          <p class="subtitle subtitle_md">
            Series can be cohort-based for engaging group discussions or even
            on-demand for the self-paced learner.
          </p>
        </div>
        <div class="teacher-card">
          <img
            class="teacher-card__img"
            src="../assets/into card img3.png"
            alt=""
          />
          <h3 class="title title_sm">Immerse the audience</h3>
          <p class="subtitle subtitle_md">
            Participants can chat with each other, send private messages, and
            raise a hand to be brought up on the stage during live events.
          </p>
        </div>
      </div>

      <div class="circle-section">
        <img class="intro__logo" src="../assets/intro logo.png" alt="" />
        <div>
          <h2 class="title title_md-bold">Become a Superpeer</h2>
          <img
            class="circle-section__arrowe"
            src="../assets/orange arrowe.png"
            alt=""
          />
        </div>
        <button class="button">Create Account</button>
        <img
          class="circle-section__bgr"
          src="../assets/intro-circle-bgr.png"
          alt=""
        />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Intro",
};
</script>

<style lang="scss">
.intro {
  padding: 128px 0 28px 0;
  background: linear-gradient(180deg, #e4ddff 0%, rgba(255, 255, 255, 0) 100%);

  .text-right {
    text-align: right;
  }

  &__img {
    margin: 94px 0 67px 0;
    width: 100%;
  }

  .intro-teacher-card {
    margin-top: 70px;
  }

  &__logo {
    animation: circleScale 5s linear 0s 1000000 normal none;
  }

  .circle-section {
    position: relative;
    margin: 250px 0 170px 0;

    &__bgr {
      position: absolute;
      bottom: -175px;
      left: -153px;
      z-index: -1;
      animation: circleScale 5s linear 0s 1000000 normal none;
    }

    &__arrowe {
      width: 200px;
    }

    .button {
      margin-top: 42px;
    }
  }
}

@media screen and (max-width: 576px) {
  .intro {
    padding-top: 35px;
    .title {
      font-size: 36px;
      line-height: 46px;
    }
    &__arrowe {
      width: 170px;
      margin-bottom: 15px;
    }
    &__img {
      margin: 20px 0 0 0;
      width: 100%;
    }

    &__logo {
      width: 100px;
    }

    .intro-teacher-card {
      display: flex;
      flex-direction: column;

      .title {
        font-size: 33px;
        line-height: 43px;
      }
      .subtitle_md {
        font-size: 15px;
      }
    }
  }

  .intro .circle-section {
    margin: 3px 0 0 0;

    .title {
      font-size: 29px;
    }

    &__bgr {
      bottom: 70px;
      left: 0px;
      width: 334px;
    }
  }
}
</style>

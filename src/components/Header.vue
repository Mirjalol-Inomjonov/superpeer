<template>
  <header class="header">
    <div class="container d-flex align-items-center justify-content-between">
      <img class="logo" src="../assets/logo.png" alt="" />
      <div class="nav gap-sm-5 gap-3 d-flex" :class="show ? 'nav-rwd' : ''">
        <div class="nav__close d-sm-none" @click="showing()">x</div>

        <router-link class="header__rlink" to="#">Home</router-link>
        <router-link class="header__rlink" to="#">Features</router-link>
        <router-link class="header__rlink" to="#">About Us</router-link>
      </div>
      <div class="d-flex gap-5">
        <button class="signIn-btn">Sign In</button>
        <button class="button">
          <svg
            width="15"
            height="16"
            viewBox="0 0 15 16"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M13.26 12.45L10.56 11.86C10.77 11.71 11 11.39 11 10.99C11 10.53 10.76 10.27 10.57 10.13C10.82 9.93001 11.17 9.59 11.17 8.96C11.17 8.29 10.71 7.94 10.47 7.78C10.66 7.6 10.93 7.24 10.93 6.74C10.93 5.86 10.25 5.46 9.70001 5.24C9.03774 5.06784 8.3538 4.99372 7.67001 5.02C6.46001 5.02 5.36001 5.11 4.83001 5.11C4.21001 5.11 4.29001 4.79 4.51001 4.49C4.66001 4.33 6.43001 1.99 6.76001 1.57C6.99001 1.27 7.26001 0.970004 7.46001 1.08C7.68001 1.2 7.59001 1.74 7.36001 2.32C7.02001 3.24 6.53001 3.83 6.42001 4.03L7.24001 4.53C7.55001 4.13 8.59001 2.41 8.59001 1.3C8.59001 0.800004 8.39001 0.380004 8.03001 0.150004C7.66001 -0.0599956 7.18001 -0.0499956 6.76001 0.200004C6.48001 0.370004 6.20001 0.610004 5.96001 0.920004L3.46001 4.09C2.76001 5.02 3.08001 6.17 4.60001 6.17C5.14001 6.17 6.89001 6.04 7.57001 6.04C8.35001 6.04 8.73001 6.08 9.00001 6.12C9.50001 6.19 9.80001 6.42 9.80001 6.72C9.80001 6.95 9.70001 7.1 9.52001 7.22C9.34001 7.35 9.18001 7.55 9.18001 7.82C9.18001 8.13 9.47001 8.26 9.66001 8.39001C9.92001 8.56001 10.07 8.67 10.07 8.94C10.07 9.18 9.89001 9.32001 9.69001 9.47001C9.52001 9.60001 9.30001 9.74 9.30001 10.04C9.30001 10.3 9.50001 10.44 9.62001 10.54C9.75001 10.64 9.89001 10.75 9.89001 10.97C9.89001 11.19 9.79001 11.29 9.53001 11.44C9.33001 11.56 9.03001 11.77 9.03001 12.08C9.03001 12.42 9.28001 12.58 9.57001 12.65C10.27 12.82 12.37 13.27 13.08 13.43C13.31 13.48 13.54 13.56 13.54 13.75C13.54 13.95 13.24 14.03 12.8 14.03C11.3 14.03 7.10001 13.73 4.64001 12.87C2.97001 12.31 2.05001 11.27 2.05001 10.04C2.05001 8.96 2.77001 8.01 3.55001 7.46L2.85001 6.74C2.29138 7.10164 1.82741 7.59172 1.49687 8.16929C1.16633 8.74687 0.978823 9.39516 0.950012 10.06C0.950012 11.56 1.85001 13.1 4.31001 13.93C6.93001 14.81 10.9 15.08 12.75 15.08C14.02 15.08 14.63 14.56 14.63 13.77C14.62 13.01 14 12.6 13.26 12.45Z"
              fill="#222222"
            />
          </svg>
          &nbsp; Become a Superpeer
        </button>

        <div class="burger-wrapper" @click="showing()">
          <div
            class="
              burger
              d-flex
              flex-column
              align-items-center
              justify-content-center
            "
          >
            <div class="burger__item"></div>
            <div class="burger__item"></div>
            <div class="burger__item"></div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      show: false,
    };
  },
  methods: {
    showing() {
      this.show = !this.show;
    },
  },
};
</script>

<style lang="scss">
.header {
  padding: 15px 0;
  background-color: #fff;
  box-shadow: 0 1px 30px -6px #ffd338;
  // margin-bottom: 138px;

  .logo {
    cursor: pointer;
  }

  &__rlink {
    font-size: 16px;
    line-height: 22px;
    text-transform: uppercase;
    color: #222222;
    text-decoration: none;

    &::after {
      content: "";
      width: 0;
      height: 2px;
      background-color: #ffd338;
      display: block;
      margin: auto;
      transition: all 0.25s linear;
      transform: translate(0, 10px);
    }

    &:hover::after {
      width: 100%;
    }

    &:hover {
      color: #222222;
    }
  }

  .signIn-btn {
    font-size: 16px;
    line-height: 22px;
    text-transform: uppercase;
    color: #222222;
    background-color: transparent;
    text-decoration: none;
    border: none;
    outline: none;
    &:hover {
      color: #ffd338;
    }
  }

  .burger-wrapper {
    display: none;
    .burger {
      width: 38px;
      height: 38px;
      border-radius: 50%;
      background-color: #ffd338;

      &__item {
        width: 16px;
        height: 3px;
        background-color: #fff;
        border-radius: 6px;

        &:nth-child(2) {
          margin: 3px 0;
        }
      }
    }
  }
}

@media screen and (max-width: 576px) {
  .header {
    padding: 10px 0;
    .burger-wrapper {
      display: block;
    }

    .button,
    .signIn-btn {
      display: none;
    }

    &__rlink {
      margin: 25px 0;
      font-weight: bold;
      font-size: 25px;
    }

    .nav {
      position: fixed;
      top: 0;
      left: -100%;
      flex-direction: column;
      background-color: #ffd338;
      width: 100%;
      text-align: center;
      height: 100vh;
      z-index: 15;
      transition: all 0.5s ease-in;

      &__close {
        font-size: 36px;
        font-weight: bold;
        color: #222222;
        text-align: right;
        margin: 20px 35px 0 0;
      }
    }
    .nav-rwd {
      left: 0;
    }
  }
}
</style>

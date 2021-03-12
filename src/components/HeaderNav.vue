<template>
  <header class="header">
    <div class="burger" id="burger">
      <div class="bar bar-1"></div>
      <div class="bar bar-2">menu</div>
      <div class="bar bar-3"></div>
    </div>

    <!-- <h1 class="main-title">
      Thomas Loegel
    </h1> -->

    <nav class="nav-menu" id="nav-menu">
      <ul class="nav-list">
        <li class="nav-item">
          <router-link class="nav-link" to="/">Home</router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/about">About</router-link>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  data: () => ({
    name: 'HeaderNav'
  }),
  mounted () {
    const burger = document.querySelectorAll('#burger')
    const nav = document.querySelector('#nav-menu')

    for (var i = 0; i < burger.length; i++) {
      burger[i].addEventListener('click', function () {
        if (this.classList.contains('active')) {
          this.classList.remove('active')
          nav.classList.remove('active')
        } else {
          this.classList.add('active')
          nav.classList.add('active')
        }
      })
    }
  }
}
</script>

<style lang="scss" scoped>
.header {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  background-color: var(--background-base);
  background-image: linear-gradient(var(--font-base), var(--font-base));
  background-repeat: no-repeat;
  background-position: right;
  background-size: .06rem 100%;

  // Burger
  .burger {
    position: relative;
    width: 50px;
    height: 45px;
    margin: 1rem;

    cursor: pointer;

    &:hover {

      .bar-2 {
        color: var(--hover);
      }
    }

    .bar {
      position: absolute;
      left: 0;
      width: 100%;
      height: 15%;
      background: var(--font-base);
      transition: all 0.2s ease;
    }

    .bar-1 {
      top: 0;
      transform: rotate(0deg);
      transform-origin: 0% 100%;
    }

    .bar-2 {
      bottom: 45%;
      transform: scale(1, 1);
      transform-origin: 0% 45%;
      transition: all .1s .1s ease;
      background: none;
      font-size: 1rem;
      text-align: center;
      letter-spacing: 0.4rem;
      font-weight: 400;
      text-transform: uppercase;
    }

    .bar-3 {
      bottom: 0;
      transform: rotate(0deg);
      transform-origin: 0% 0%;
    }

    &.active {
      .bar {
        background: var(--hover);
      }

      .bar-1 {
        width: 100%;
        left: 10%;
        transform: rotate(45deg);
      }

      .bar-2 {
        transform: scale(1, 0);
        transition: all .1s ease;
        background: none;
      }

      .bar-3 {
        width: 100%;
        left: 10%;
        transform: rotate(-45deg);
      }
    }
  }

  // Main title
  .main-title {
    place-self: center;
  }

  // Nav-menu
  .nav-menu {
    position: absolute;
    top: 80px;
    left: -50px;
    width: 2.2rem;
    transition: all .2s ease;

    &.active {
      left: 25px;
      transition: all .2s ease;
    }

    .nav-list {
      .nav-item {
        margin-top: 2rem;
        writing-mode: vertical-rl;
        transform: rotate(180deg);

        .nav-link {
          text-decoration: none;
          color: inherit;
          padding-bottom: 0.2rem;
          animation: out .2s ease;

          @keyframes out {
            from {
              background-image: linear-gradient(var(--hover), var(--hover));
              background-repeat: no-repeat;
              background-position: bottom left;
              background-size: 0.6rem 100%;
            }
            to {
              background-image: linear-gradient(var(--hover),var(--hover));
              background-repeat: no-repeat;
              background-position: bottom left;
              background-size: 0.6rem 0%;
            }
          }

          &:hover {
            background-image: linear-gradient(var(--hover), var(--hover));
            background-position: bottom left;
            background-repeat: no-repeat;
            background-size: 0.6rem 100%;
            animation: in .2s ease;

            @keyframes in {
              from {
                background-position: top left;
                background-size: 0.6rem 0%;
              }
              to {
                background-position: top left;
                background-size: 0.6rem 100%;
              }
            }
          }
        }
      }
    }
  }
}
</style>

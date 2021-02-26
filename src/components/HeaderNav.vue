<template>
  <header class="header">
    <div class="burger" id="burger">
      <div class="bar bar-1"></div>
      <div class="bar bar-2">menu</div>
      <div class="bar bar-3"></div>
    </div>

    <nav class="nav-menu" id="nav-menu">
      <ul class="nav-list">
        <li class="nav-item"><router-link class="nav-link" to="/">Home</router-link></li>
        <li class="nav-item"><router-link class="nav-link" to="/about">About</router-link></li>
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
  display: flex;
  flex-direction: column;
  align-items: flex-start;

  // Burger
  .burger {
    position: relative;
    width: 50px;
    height: 45px;
    margin: 1rem;
    cursor: pointer;

    .bar {
      position: absolute;
      left: 0;
      width: 100%;
      height: 20%;
      background:#333;
      transition: all .3s ease;
    }

    .bar-1 {
      top: 0;
      transform: rotate(0deg);
      transform-origin: 0% 100%;
    }

    .bar-2 {
      top: 40%;
      transform: scale(1, 1);
      transform-origin: 0% 50%;
      transition: all .3s .3s ease;
      background: none;
      font-size: 1.1rem;
      text-align: center;
      letter-spacing: 0.4rem;
      font-weight: 400;
      text-transform: uppercase;
    }

    .bar-3 {
      top: 80%;
      transform: rotate(0deg);
      transform-origin: 0% 0%;
    }

    &.active {

      .bar {
        background:#333;
      }

      .bar-1 {
        width: 95%;
        left: 10%;
        transform: rotate(45deg);
      }

      .bar-2 {
        transform: scale(1, 0);
        transition: all .1s ease;
        background: none;
      }

      .bar-3 {
        width: 95%;
        left: 10%;
        transform: rotate(-45deg);
      }
    }
  }

  // Nav-menu
  .nav-menu {
    position: absolute;
    top: 70px;
    left: -50px;
    transition: all .1s ease;

    &.active {
      left: 10px;
      transition: all .1s ease;
    }

    .nav-list {

      .nav-item {
        margin-bottom: 8px;

        .nav-link {
          text-decoration: none;
          color: inherit;
          padding-bottom: 2px;
          animation : .2s out;

          @keyframes out {
            from {
              background-image: linear-gradient(#333, #333);
              background-repeat: no-repeat;
              background-position: right bottom;
              background-size: 100% 2px;
            }
            to {
              background-image: linear-gradient(#333, #333);
              background-repeat: no-repeat;
              background-position: right bottom;
              background-size: 0% 2px;
            }
          }

          &:hover {
            background-image: linear-gradient(#333, #333);
            background-position: bottom;
            background-repeat: no-repeat;
            background-size: 100% 2px;
            animation : .2s in;

            @keyframes in {
              from {
                background-position: left bottom;
                background-size: 0% 2px;
              }
              to {
                background-position: left bottom;
                background-size: 100% 2px;
              }
            }
          }
        }
      }
    }
  }
}

</style>

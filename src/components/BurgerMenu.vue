<template>
  <div class="burger">
    <button
      @click="closeBurger"
      class="burger__icon"
      :class="{ isClosed: burger }"
    >
      <span></span>
      <span></span>
      <span></span>
    </button>
    <div class="menu" :class="{ showMenu: burger }">
      <ul>
        <li>
          <a href="https://www.codewars.com/users/pylsar" rel="nofollow" target="_blank">
            <svg class="social-link">
              <use xlink:href="../assets/img/sprite.svg#iconfinder_codewars_4691329"></use>
            </svg>
          </a>
        </li>
        <li>
          <a href="https://codepen.io/collection/Aawzba" rel="nofollow" target="_blank">
            <svg class="social-link">
              <use xlink:href="../assets/img/sprite.svg#iconfinder_Codepen_4550862"></use>
            </svg>
          </a>
        </li>
        <li>
          <a href="https://codesandbox.io/u/pylsar" rel="nofollow" target="_blank">
            <svg class="social-link">
              <use xlink:href="../assets/img/sprite.svg#iconfinder_codesandbox_4691539"></use>
            </svg>
          </a>
        </li>
        <li>
          <a href="https://github.com/pylsar" rel="nofollow" target="_blank">
            <svg class="social-link">
              <use xlink:href="../assets/img/sprite.svg#github"></use>
            </svg>
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
import { TimelineMax } from "gsap/all";
export default {
  name: "BurgerMenu",
  data() {
    return {
      burger: false,
    };
  },
  methods: {
    closeBurger() {
      this.burger = !this.burger;
        let tl = new TimelineMax();
        tl.fromTo(".social-link", 4, { opacity: 0 }, { opacity: 1 })
        // tl.staggerFromTo('.social-link', 0.3, {y: 40, opacity: 0}, {y: 0, opacity: 1}, 0.05)
    },
  },
  mounted() {

  },
};
</script>

<style lang="scss">
.burger {
  &__icon {
    background: none;
    border: none;
    outline: none;
    width: 30px;
    height: 24px;
    cursor: pointer;
    position: relative;
    top: 0;
    z-index: 10;
    & span {
      display: block;
      width: 30px;
      height: 2px;
      background: #fff;
      transition: all 0.3s ease;
      &:first-child {
        position: absolute;
        top: 0;
        left: 0;
      }
      &:last-child {
        position: absolute;
        bottom: 0;
        left: 0;
      }
    }
  }
  .isClosed {
    & span:first-child {
      transform: rotate(45deg) translate(7px, 8px);
    }
    & span:nth-child(2) {
      opacity: 0;
    }
    & span:last-child {
      transform: rotate(-45deg) translate(7px, -8px);
    }
  }
}
.menu {
  width: 100%;
  height: 20vh;
  background: green;
  position: absolute;
  top: 0;
  left: 0;
  z-index: 9;
  transform: translateY(-300px);
  transition: all 0.5s ease;
  & ul {
    display: flex;
    justify-content: space-around;
    align-items: center;
    width: 100%;
    height: 100%;
    & li {
      list-style: none;
      & a {
        & svg {
          width: 50px;
          height: 50px;
        }
      }
    }
  }
}
.showMenu {
  transform: translateY(0px);
  transition: all 0.5s ease;
}
</style>
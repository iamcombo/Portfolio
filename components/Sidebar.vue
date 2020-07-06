<template>
  <div class="wrapper">
    <transition name="slide-side">
      <div class="navbar" v-if="createMenu" :style="{width: createMenu ? '6%' : '0'}">
        <div class="nav-toggle" @click="handleNav">menu</div>
      </div>
    </transition>
    <div class="container">
      <transition name="slide-side">
        <div class="nav" v-if="toggleSidebar" :style="{width: toggleSidebar ? '100%':'0'}">
          <div class="nav-items">
            <div class="nav-item">
              <a href="#" :style="{top: afterToggle ? '0px' : '160px'}">Home</a>
              <div class="nav-item-wrapper"></div>
            </div>
            <div class="nav-item">
              <a href="#" :style="{top: afterToggle ? '0px' : '160px'}">Portfolio</a>
              <div class="nav-item-wrapper"></div>
            </div>
            <div class="nav-item">
              <a href="#" :style="{top: afterToggle ? '0px' : '160px'}">About</a>
              <div class="nav-item-wrapper"></div>
            </div>
            <div class="nav-item">
              <a href="#" :style="{top: afterToggle ? '0px' : '160px'}">Contact</a>
              <div class="nav-item-wrapper"></div>
            </div>
          </div>
        </div>
      </transition> 
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      toggleSidebar: false,
      afterToggle: false,
      createMenu: false
    }
  },
  created() {
    setTimeout(() => {
      this.createMenu = true;
    }, 300);
  },
  methods: {
    async handleNav() {
      if(this.toggleSidebar) {
        this.afterToggle = await false;
        this.toggleSidebar = await false;
      } else {
        this.toggleSidebar = await true;
        setTimeout(async () => {
          this.afterToggle = await true;
        }, 1600);
      }
    }
  }
}
</script>

<style scoped>
.hero-title {
  color: #fff;
  text-transform: uppercase;
  font-size: 48px;
}
/* .wrapper {
  position: fixed;
  width: 100%;
  height: 100vh;
} */
.navbar {
  box-sizing: border-box;
  position: fixed;
  width: 0%;
  height: 100vh;
  background: #a72929;
  display: flex;
  align-items: center;
  justify-content: center;
  border-right: 2.4px solid #fff;
  z-index: 2;
}
.nav-toggle {
  cursor: pointer;
  transform: rotate(-90deg);
  color: #fff;
  text-transform: uppercase;
}
.nav {
  position: fixed;
  width: 0%;
  height: 100%;
  overflow: hidden;
  display: flex;
  align-items: center;
  left: 6%;
  background: #252e2d;
}
.nav-items {
  margin: 60px;
}
.nav-item {
  position: relative;
  font-size: 120px;
}
.nav-item a {
  position: relative;
  top: 160px;
  text-decoration: none;
  color: #a72929;
  text-transform: uppercase;
  font-size: 140px;
  font-weight: lighter;
  letter-spacing: -8px;
  transition: 1s;
}
.nav-item-wrapper:after {
  content: "";
  position: absolute;
  top: 160px;
  left: 0;
  width: 110%;
  height: 100%;
  background: #252e2d;
  margin: 0 auto;
  transition: 1s;
}
.nav-item:after {
  content: "";
  position: absolute;
  top: 50%;
  left: 0;
  width: 0%;
  height: 2.8px;
  background: #fff;
  transition: 0.3s;
}
.nav-item:hover:after {
  width: 100%;
}
.slide-side-enter-active,
.slide-side-leave-active {
  transition: all 1.6s ease-in-out;
}
.slide-side-enter,
.slide-side-leave-to {
  transform: translateX(-100%);
}
@media (max-width: 990px) {
  html,
  body {
    overflow: hidden;
  }

  .navbar {
    width: 16%;
  }

  .nav {
    left: 16%;
  }

  .nav-item a {
    font-size: 40px;
    letter-spacing: 0;
  }

  .nav-item:after {
    display: none;
  }
}
</style>
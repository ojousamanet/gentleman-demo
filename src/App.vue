<template>
  <div class="wraper">
    <div class="container py-3">
      <ul class="nav nav-pills nav-justified px-1">
        <li class="nav-item">
          <router-link
          class="nav-link fw-bold"
          to="/"
          active-class="active">HOME</router-link>
        </li>
        <li class="nav-item">
          <router-link
          class="nav-link fw-bold"
          to="/about"
          active-class="active">ABOUT</router-link>
        </li>
        <li class="nav-item">
          <a class="nav-link fw-bold btn btn-primary"
          data-bs-toggle="offcanvas"
          href="#offcanvasExample"
          role="button"
          aria-controls="offcanvasExample">PROFILE</a>
        </li>
      </ul>    
    </div>
    <div class="offcanvas offcanvas-start" tabindex="-1" id="offcanvasExample" aria-labelledby="offcanvasExampleLabel">
      <div class="offcanvas-header">
        <h5 class="offcanvas-title" id="offcanvasExampleLabel">Offcanvas</h5>
        <button type="button" class="btn-close text-reset" data-bs-dismiss="offcanvas" aria-label="Close"></button>
      </div>
      <div class="offcanvas-body">
        <div>
          Some text as placeholder. In real life you can have the elements you have chosen. Like, text, images, lists, etc.
          <a href="https://twitter.com/ojousamanet" target="_blank" rel="noopener">@ojousamanet</a>.
        </div>
      </div>
    </div>
    <router-view></router-view>
    <FooterComponens />
  </div>
</template>

<style>
</style>

<script>
// @ is an alias to /src
import FooterComponens from '@/components/Footer.vue'

export default {
  name: 'App',
  components: {
    FooterComponens
  }
}
</script>

<style lang="scss" scoped>
:root{
    --main-color:#3bbd90;
}
html{
    background-color: var(--main-color);
}
#app{
    font-family: 'Noto Sans JP', sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    background-color:#2a292e;
}
.nav{
  &-item{}
  &-link{
      color: var(--main-color);
      &.active{
          background-color: var(--main-color);
          color: #fff;
      }
  }
}
</style>
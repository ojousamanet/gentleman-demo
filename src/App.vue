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
    <div class="offcanvas offcanvas-start w-75" tabindex="-1" id="offcanvasExample" aria-labelledby="offcanvasExampleLabel">
      <div class="offcanvas-header">
        <h5 class="offcanvas-title" id="offcanvasExampleLabel">作者プロフィール</h5>
        <button type="button" class="btn-close text-reset" data-bs-dismiss="offcanvas" aria-label="Close"></button>
      </div>
      <div class="offcanvas-body">
        <div>
          風俗業界の裏方で店舗のサポートしてた人。今は転職して美容業界に転身。
          自分のことを良客とか紳士とか自称する同性には共感性羞恥心がする人。<br>
          ただ、良客育成には興味があるので、（自称ではなく）周りから評価される良客を増やすのは進めたい<br>
          どんな人を良客って言うの？清潔で優しくて、性病検査を受けていて、ルールを守れて、余裕があって…<br>
          それは普通のお客さんか<br>
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
html{
    background-color: var(--main-color);
}
#app{
    font-family: 'Noto Sans JP', sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
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
}
</style>
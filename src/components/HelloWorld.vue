<template>
  <div class="hello">
    <div class="container">
      <div class="pt-3 pb-1">
        <h1 class="fs-1 fw-bold text-white">{{ msg }}</h1>
      </div>
      <div class="text-start p-2 small">
        <p class="text-light fst-normal">風俗を利用する人間には2種類のタイプがいる。良客と良客以外。
          良客は自らを良客や紳士と自称したりしません。なぜなら、それらの評価は他者によって与えられるものだと当俱楽部は解釈しています。
          女性を評価するのではなく、自らを見つめなおし改善すべき箇所を改めることで、女性に評価されるような紳士へと成長しませんか？会員募集中
        </p>
      </div>
      <div class="p-2 d-grid gap-2">
        <router-link to="/" class="btn btn-light btn-lg">
          <span class="fw-bold text-dark">入会テストを受ける</span>
        </router-link>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>

<template>
  <div class="about">
    <div class="container">
      <div class="pt-3 pb-1 text-center">
        <h1 class="fs-2 fw-bold text-white">風俗紳士倶楽部とは？</h1>
      </div>
      <div class="text-start p-2 small">
        <p class="text-light fst-normal">「風俗紳士倶楽部」は風俗を利用するお客様の中で、模範的なユーザーだけが入会できる大人の倶楽部です。
          その規範は、「①ルールやマナーを遵守すること」「②お相手の女性に敬意を払い丁重に接すること」「③業界の健全化に寄与し、それに反する事象の解決に努めること」
          と決して難しい内容ではありません。
        </p>
      </div>
    </div>
    <MemberList/>
  </div>
</template>

<script>
import MemberList from '@/components/MemberList.vue'
export default {
  components: {
    MemberList
  }
}
</script>
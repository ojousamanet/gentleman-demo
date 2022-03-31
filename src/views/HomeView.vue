<template>
  <div class="home">
    <div class="container">
      <div class="px-5 py-2">
        <img class="px-2" alt="site logo" src="@/assets/men.svg">
      </div>
    </div>
    <HelloWorld msg="風俗紳士倶楽部"/>
    <!-- Button trigger modal -->
    

    <!-- Modal -->
    <div class="modal fade" id="staticBackdrop" data-bs-backdrop="static" data-bs-keyboard="false" tabindex="-1" aria-labelledby="staticBackdropLabel" aria-hidden="true">
      <div class="modal-dialog modal-dialog-centered modal-dialog-scrollable">
        <ExaminationForm />
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import ExaminationForm from '@/components/ExaminationForm.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld,
    ExaminationForm
  }
}
</script>

<style lang="scss" scoped>

</style>
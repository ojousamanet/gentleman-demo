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
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="staticBackdropLabel">入会審査</h5>
            <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
          </div>
          <div class="modal-body">
            <div class="border-bottom">
              <div class="progress" style="height: 8px;">
                <div class="progress-bar progress-bar-striped bg-main progress-bar-animated"
                role="progressbar"
                aria-valuenow="25"
                aria-valuemin="0" aria-valuemax="100" style="width: 25%"></div>
              </div>
              <form action="" class="form">
                <div class="container">
                  <div class="py-2">
                    <div class="form-check form-check-inline">
                      <input class="form-check-input" type="radio" name="inlineRadioOptions" id="inlineRadio1" value="option1">
                      <label class="form-check-label" for="inlineRadio1">受けた</label>
                    </div>
                    <div class="form-check form-check-inline">
                      <input class="form-check-input" type="radio" name="inlineRadioOptions" id="inlineRadio2" value="option2">
                      <label class="form-check-label" for="inlineRadio2">受けていない</label>
                    </div>
                  </div>
                </div>
              </form>
            </div>
          </div>
          <div class="modal-footer">
            <div class="row w-100 m-0 px-1">
              <div class="col-6 ps-0 pe-2">
                <div class="d-grid gap-2">
                  <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">入会を諦める</button>
                </div>
              </div>
              <div class="col-6 ps-2 pe-0">
                <div class="d-grid gap-2">
                  <button type="button" class="btn btn-main">審査を受ける！</button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  }
}
</script>

<style lang="scss" scoped>
.form{
  &-check{
    display: inline-flex;
    align-items: center;
    justify-content: flex-start;
    &-input{
      width: 1.5em;
      height: 1.5em;
      margin-right: 0.5em;
      &:checked{
        background-color: #1fb36e;
        border-color: #2bad71;
      }
    }
    &-label{}
  }
}
.btn{
  &-main{
    background-color: var(--main-color);
    color: #fff;
  }
}
.bg{
  &-main{
    background-color: var(--main-color);
    color: #fff;
  }
}
</style>
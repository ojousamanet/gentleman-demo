<template>
  <div class="modal-content">
    <div class="modal-header">
      <h5 class="modal-title" id="staticBackdropLabel">{{title}}</h5>
      <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
    <div class="modal-body p-0">
      <div class="border-bottom px-2 py-3 bg-white">
        <div class="progress" style="height: 8px;">
          <div class="progress-bar progress-bar-striped bg-main progress-bar-animated"
          role="progressbar"
          aria-valuenow="25"
          aria-valuemin="0" aria-valuemax="100" style="width: 25%"></div>
        </div>
        <form action="" class="form py-3">
          <div class="form-floating mb-3">
            <input type="email" class="form-control" id="floatingInput" placeholder="name@example.com">
            <label for="floatingInput">お名前</label>
          </div>
          <div v-for="List in checkList" :key="List.id" class="container rounded-xl bg-light my-3">
            <legend class="mb-0 pt-2 fs-5 small fw-bold">
              <span class="small">{{List[1]["title"]}}</span>
            </legend>
            <div class="py-2 row w-100 mx-0">
              <div v-for="(answer, index) in List[2]['answer']" :key="index" class="form-check form-check-inline col-6 mx-0">
                <input class="form-check-input" type="radio" name="inlineRadioOptions" :id="'answer-'+List[0]['id']" :value="'val-'+List[0]['id']">
                <label class="form-check-label" v-bind:for="'answer-'+List[0]['id']">{{answer}}</label>
              </div>
            </div>
          </div>
          <div class="form-floating">
            <textarea class="form-control" placeholder="最大0000文字" id="floatingTextarea2" style="height: 100px"></textarea>
            <label for="floatingTextarea2">利用時に心がけていることは？</label>
          </div>
        </form>
      </div>
    </div>
    <div class="modal-footer">
      <div class="row w-100 m-0 px-1">
        <div class="col-6 ps-0 pe-2">
          <div class="d-grid gap-2">
            <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">入部を諦める</button>
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
</template>

<script>
export default {
  name: 'ExaminationForm',
  data(){
    return{
      title:"入部審査",
      checkList:[
        [
          {id:1},
          {title:"性病検査を受けましたか？"},
          {answer:["受けた","受けていない"]},
          {correct:"1"}
        ],[
          {id:2},
          {title:"予約以外のDMを送っていませんか？"},
          {answer:["送った","送っていない"]},
          {correct:"0"}
        ],[
          {id:2},
          {title:"爪や髭は綺麗に切っている？"},
          {answer:["切っている","切っていない"]},
          {correct:"0"}
        ],[
          {id:3},
          {title:"写メ日記の画像は保存禁止"},
          {answer:["保存している","保存していない"]},
          {correct:"1"}
        ],[
          {id:4},
          {title:"毎日の歯磨きや口臭ケアは？"},
          {answer:["していない","徹底している"]},
          {correct:"0"}
        ],[
          {id:5},
          {title:"AVはフィクションだよ"},
          {answer:["知っている","知らなかった"]},
          {correct:"0"}
        ],[
          {id:6},
          {title:"利用ルールや禁止事項は読んだ？"},
          {answer:["読み込んだ","読んでいない"]},
          {correct:"0"}
        ],[
          {id:7},
          {title:"女性に喜ばれるプレゼントは？"},
          {answer:["現金","飲み物やお菓子"]},
          {correct:"0"}
        ]
      ]
    }
  },
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
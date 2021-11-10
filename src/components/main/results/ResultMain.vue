<template>
  <div class="result-main">

    <div class="result-main__block-qr">
      <h6 class="result-main__block-qr-title">
        Відскануй QR - код, щоб отримати електронну копію
      </h6>

      <img
          alt
          class="result-main__block-qr-img"
          :src='require(`@/assets/images/${result.QRCode}`)'
      >
    </div>

    <result-main-info
        class="result-main__result-main-info"
        :result="result"
    />


  </div>
</template>

<script>
import ResultMainInfo from "./ResultMainInfo";

export default {
  name: "ResultMain",
  props: {
    result: {
      type: Object
    }
  },
  components: {
    ResultMainInfo
  }
}
</script>

<style lang="scss" scoped>
.result-main {
  color: #111111;
  display: flex;
  flex-direction: row;

  &__block-qr {
    width: 250px;
    margin-right: 60px;
  }

  &__block-qr-title {
    text-align: left;
    font-size: 18px;
    line-height: 22px;
    padding-bottom: 20px;
  }

}
</style>
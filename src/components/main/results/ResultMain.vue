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
  display: flex;
  flex-direction: row;

  &__block-qr {
    width: 250px;
    margin-right: 60px;
    order: 1;
  }

  &__block-qr-title {
    text-align: left;
    font-size: 18px;
    line-height: 22px;
    padding-bottom: 20px;
  }

  &__result-main-info {
    order: 2;
  }
}

@media (max-width: 428px) {
  .result-main {
    justify-content: space-between;
    position: relative;

    &__block-qr {
      width: 86px;
      margin-right: 0;
      order: 2;
    }

    &__block-qr-title {
      font-weight: 300;
      font-size: 9px;
      line-height: 11px;
      padding-bottom: 5px;
    }

    &__block-qr-img {
      height: 86px;
      width: 86px;
    }

    &__result-main-info {
      order: 1;
    }
  }
}
</style>
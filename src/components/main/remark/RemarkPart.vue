<template>
  <div class="remark-part">

    <h2 class="remark-part__title">
      Примітка
    </h2>

    <p class="remark-part__info">
      Лікар: {{ result.doctor }}
    </p>

    <img
        alt
        class="remark-part__img"
        src="../../../assets/images/signature.png"
    >

    <hr class="remark-part__line">

    <!-- Info block -->
    <div class="remark-part__block">

      <p class="remark-part__info-first">
        Інформаційна підтримка Контакт-центру Люкс Медикал: <br class="br"> 0 800 21 78 78 <br class="br">
        символом * позначаються результати, що виходять за <br class="br"> межі референтних
      </p>

      <p class="remark-part__info-second">
        Дата друку {{ result.dateOfPrinting }}
      </p>

    </div>
  </div>
</template>

<script>
export default {
  name: "RemarkPart",
  props: {
    result: {
      type: Object
    }
  }
}
</script>

<style lang="scss" scoped>
.remark-part {
  height: 548px;
  background-image: url("../../../assets/images/remark-part-bg.png");
  background-size: inherit;
  background-repeat: no-repeat;
  background-position: 783px 31px;
  padding-top: 129px;

  .br {
    display: none;
  }

  &__line {
    display: none;
  }

  &__title {
    font-weight: 500;
    font-size: 36px;
    line-height: 44px;
    margin-bottom: 47px;
  }

  &__info {
    font-weight: 500;
    font-size: 21px;
    line-height: 25px;
    margin-bottom: 38px;
  }

  &__img {
    margin-left: 30px;
    margin-bottom: 69px;
  }

  &__block {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: self-end;
  }

  &__info-first {
    width: 762px;
    font-size: 21px;
    line-height: 32px;
  }

  &__info-second {
    font-weight: 500;
    font-size: 21px;
    line-height: 25px;
    padding-bottom: 5px;
    padding-right: 14px;
  }
}

@media (max-width: 428px) {
  .remark-part {
    height: 364px;
    padding-top: 40px;
    background-image: url("../../../assets/images/remark-part-bg.png");
    background-size: 60%;
    background-repeat: no-repeat;
    background-position: 120% 120px;
    position: relative;

    &__title {
      font-size: 19px;
      line-height: 23px;
      margin-bottom: 45px;
    }

    &__info {
      font-size: 16px;
      line-height: 19px;
      margin-bottom: 45px;
    }

    &__img {
      height: 88px;
      width: 184px;
      margin: 0 0 90px;
    }

    &__line {
      display: block;
      height: 3px;
      position: absolute;
      width: 108%;
      left: 50%;
      transform: translate(-50%);
      background-color: #40A7E1;
    }

    &__block {
      width: 100%;
      margin-top: 27px;
      flex-direction: column;
    }

    &__info-first {
      width: 100%;
      font-size: 12px;
      line-height: 23px;
      text-align: center;
      margin-bottom: 21px;
    }

    .br {
      display: block;
    }

    &__info-second {
      width: 100%;
      text-align: center;
      font-size: 14px;
      line-height: 17px;
    }

  }
}
</style>
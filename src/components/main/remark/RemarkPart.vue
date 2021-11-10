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

    <!-- Info block -->
    <div class="remark-part__block">

      <p class="remark-part__info-first">
        Інформаційна підтримка Контакт-центру Люкс Медикал: 0 800 21 78 78.
        символом * позначаються результати, що виходять за межі референтних
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
</style>
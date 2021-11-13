<template>
  <div class="conclusion-part">

    <h2 class="conclusion-part__title">
      Заключення
    </h2>

    <div class="conclusion-part__block">

      <p class="conclusion-part__info">
        У разі збереження підозри на інфікування, наявності ознак ГРВЗ чи проявів схожих на коронавірусну хворобу
        рекомендується звернутися до лікаря, щоб отримати подальші рекомендації та виконувати заходи безпеки
        (використовувати засоби індивідуального захисту, дотримуватись соціальної дистанції).
      </p>

    </div>


  </div>
</template>

<script>
export default {
  name: "ConclusionPart"
}
</script>

<style lang="scss" scoped>
.conclusion-part {
  &__title {
    font-weight: 500;
    font-size: 36px;
    line-height: 44px;
    margin-bottom: 18px;
  }

  &__block {
    height: 223px;
    padding: 27px 431px 0 27px;
    background-image: url("../../../assets/images/conclusion-bg.png");
    background-size: inherit;
    background-repeat: no-repeat;
    background-position: 1024px 31px;
    background-color: #FFFFFF;
    box-shadow: 0 16px 24px rgba(0, 0, 0, 0.06), 0 2px 6px rgba(0, 0, 0, 0.04), 0 0 1px rgba(0, 0, 0, 0.04);
    border-radius: 3px;
  }

  &__info {
    font-size: 21px;
    line-height: 32px;
  }
}

@media (max-width: 428px) {
  .conclusion-part {

    &__title {
      font-weight: 500;
      font-size: 19px;
      line-height: 23px;
      margin-bottom: 12px;
    }

    &__block {
      height: 152px;
      padding: 14px;
      background-image: url("../../../assets/images/conclusion-bg-428.png");
      background-position: 98.5% 30px;
    }

    &__info {
      font-weight: normal;
      font-size: 11px;
      line-height: 21px;
    }
  }
}

@media (max-width: 390px) {
  .conclusion-part {

    &__block {
      height: 152px;
      padding: 14px 23px;
    }
  }
}
</style>
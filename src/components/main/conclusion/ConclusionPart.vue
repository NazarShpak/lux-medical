<template>
  <div class="conclusion-part">

    <h2 class="conclusion-part__title">
      Заключення
    </h2>

    <p class="conclusion-part__info">
      У разі збереження підозри на інфікування, наявності ознак ГРВЗ чи проявів схожих на коронавірусну хворобу
      рекомендується звернутися до лікаря, щоб отримати подальші рекомендації та виконувати заходи безпеки
      (використовувати засоби індивідуального захисту, дотримуватись соціальної дистанції).
    </p>

  </div>
</template>

<script>
export default {
  name: "ConclusionPart"
}
</script>

<style lang="scss" scoped>
.conclusion-part {
  height: 285px;

  &__title {
    font-weight: 500;
    font-size: 36px;
    line-height: 44px;
    margin-bottom: 18px;
  }

  &__info {
    height: 223px;
    padding: 27px 431px 0 27px;
    font-size: 21px;
    line-height: 32px;
    background-image: url("../../../assets/images/conclusion-bg.png");
    background-size: inherit;
    background-repeat: no-repeat;
    background-position: 1024px 31px;
    background-color: #FFFFFF;
    box-shadow: 0 16px 24px rgba(0, 0, 0, 0.06), 0 2px 6px rgba(0, 0, 0, 0.04), 0 0 1px rgba(0, 0, 0, 0.04);
    border-radius: 3px;
  }
}
</style>
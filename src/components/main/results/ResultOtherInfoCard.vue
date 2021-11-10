<template>
  <div class="result-other-info-card">

    <!-- Top -->
    <div class="result-other-info-card__top">
      <h6
          class="result-other-info-card__title"
      >
        {{ title }}
      </h6>
    </div>

    <!-- Bottom -->
    <div class="result-other-info-card__bottom">
      <p
          class="result-other-info-card__content"
          :class="content === 'Не виявлено' ? 'green' : content === 'Виявлено' ? 'red' : '' "
      >
        {{ content }}
      </p>
    </div>

  </div>
</template>

<script>
export default {
  name: "ResultOtherInfoCard",
  props: {
    title: {
      type: String
    },
    content: {
      type: String
    }
  }
}
</script>

<style lang="scss" scoped>
.result-other-info-card {
  width: 447px;
  height: 213px;

  .green,
  .red {
    font-size: 21px;
    line-height: 25px;
    padding-left: 0;
  }

  .green {
    color: #37D3A4;
  }

  .red {
    color: #FA3333;
  }

  &__top,
  &__bottom {
    display: flex;
    justify-content: center;
  }

  &__top {
    height: 57px;
    background: #40A7E1;
    border-radius: 3px;
    align-items: center;
  }

  &__title {
    font-weight: 500;
    font-size: 21px;
    line-height: 25px;
    color: #FFFFFF;
  }

  &__bottom {
    height: 156px;
    background: #FFFFFF;
    opacity: 0.7;
    box-shadow: 0 16px 24px rgba(0, 0, 0, 0.06), 0 2px 6px rgba(0, 0, 0, 0.04), 0 0 1px rgba(0, 0, 0, 0.04);
    border-radius: 3px;
    padding-top: 15px;
  }

  &__content {
    padding-left: 12px;
    text-align: left;
    font-weight: bold;
    font-size: 19px;
    line-height: 29px;
    color: #111111;
  }
}
</style>
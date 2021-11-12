<template>
  <div class="result-main-info">

    <!-- First block -->
    <div class="result-main-info__block first">
      <ul class="result-main-info__list">

        <li class="result-main-info__item">
          Пацієнт: <span class="full-name">{{ result.fullName }}</span>
        </li>

        <li class="result-main-info__item">
          Дата народження: {{ result.dateOfBirth }}
        </li>

        <li class="result-main-info__item">
          Стать: {{ result.sex }}
        </li>

      </ul>
    </div>

    <!-- Second block -->
    <div class="result-main-info__block second">
      <ul class="result-main-info__list">

        <li class="result-main-info__item">
          Дата забору: {{ result.dateOfSampling }}
        </li>

        <li class="result-main-info__item">
          Дата виконання: {{ result.dateOfExecution }}
        </li>

        <li class="result-main-info__item">
          Забірний пункт: {{ result.address }}
        </li>

      </ul>
    </div>

  </div>
</template>

<script>
export default {
  name: "ResultMainInfo",
  props: {
    result: {
      type: Object
    }
  }
}
</script>

<style lang="scss" scoped>
.result-main-info {
  text-align: left;
  padding-top: 64px;
  display: flex;
  flex-direction: row;

  &__item + &__item {
    margin-top: 25px;
  }

  .full-name {
    font-weight: 500;
  }

  &__block + &__block {
    margin-left: 86px;
  }
}

@media (max-width: 428px) {
  .result-main-info {
    padding-top: 0;
    font-size: 14px;
    line-height: 17px;
    flex-direction: column;

    .first {
      width: 200px;
    }

    &__item + &__item {
      margin-top: 16px;
    }

    .full-name {
      display: inline;
      font-weight: 500;
    }

    &__block + &__block {
      margin-left: 0;
      margin-top: 56px;
    }
  }
}
</style>
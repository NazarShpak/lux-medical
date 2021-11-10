<template>
  <div class="results-part">

    <h1 class="results-part__title">
      Результати досліджень
    </h1>

    <h2 class="results-part__subtitle">
      № {{ result.number }}
    </h2>

    <result-main
        class="results-part__result-main"
        :result="result"
    />

    <result-other-info
        class="results-part__result-other-info"
        :result="result"
    />

    <hr class="results-part__line">

    <p class="results-part__other-info">
      *Дане дослідження призначене для виявлення генетичного матеріалу вірусу SARS-CoV-2.
    </p>

  </div>
</template>

<script>
import ResultMain from "./ResultMain";
import ResultOtherInfo from "./ResultOtherInfo";

export default {
  name: "ResultsPart",
  components: {
    ResultMain,
    ResultOtherInfo
  },
  props: {
    result: {
      type: Object
    }
  }
}
</script>

<style lang="scss" scoped>
.results-part {
  height: 876px;
  text-align: center;
  padding-top: 68px;

  &__title,
  &__subtitle {
    font-weight: 500;
    font-size: 36px;
    line-height: 44px;
  }

  &__title {
    margin-bottom: 10px;
  }

  &__subtitle {
    margin-bottom: 70px;
  }

  &__result-main {
    margin-bottom: 50px;
  }

  &__result-other-info {
    margin-bottom: 26px;
  }

  &__line {
    height: 2px;
    background-color: #40A7E1;
    margin: 0;
  }

  &__other-info {
    font-size: 10px;
    line-height: 29px;
    height: 29px;
    display: flex;
    justify-content: right;
  }
}
</style>
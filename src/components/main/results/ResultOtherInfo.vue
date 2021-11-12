<template>
  <div class="result-other-info">

      <result-other-info-card
          class="result-other-info__result-other-info-card"
          v-for="(info, index) of infos"
          :key="index"
          :title="info.title"
          :content="info.content"
      />

  </div>
</template>

<script>
import ResultOtherInfoCard from "./ResultOtherInfoCard";

export default {
  name: "ResultOtherInfo",
  components: {
    ResultOtherInfoCard
  },
  props: {
    result: {
      type: Object
    }
  },
  computed: {
    infos() {
      return [
        {
          title: 'Назва дослідження',
          content: this.result.nameOfStudy
        },
        {
          title: 'Результат',
          content: this.result.resultOfStudy
        },
        {
          title: 'Коментарі',
          content: this.result.comment
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.result-other-info {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
}

@media (max-width: 428px) {
  .result-other-info {
    flex-direction: column;
    align-items: self-start;
    justify-content: center;

    &__result-other-info-card + &__result-other-info-card {
      margin-top: 35px;
    }
  }
}
</style>
<template>
  <div class="result-other-info">

    <div
        class="result-other-info__block"
        v-for="(info, index) of infos"
        :key="index"
    >

      <result-other-info-card
          class="result-other-info__result-other-info-card"
          :title="info.title"
          :content="info.content"
      />

    </div>

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
</style>
<template>
  <div class="main-part">
    <div class="container">
      <div class="main-part__block">

        <results-part
            class="main-part__results-part"
            :result="result"
        />

      </div>
    </div>
  </div>
</template>

<script>
import ResultsPart from "./results/ResultsPart";

export default {
  name: "MainPart",
  data() {
    return {
      result: {
        number: 2280773,
        QRCode: 'qrcode_4579317_ 1.png',
        fullName: 'Жмишенко Валерій Альбертович',
        dateOfBirth: '10.10.2010',
        sex: 'Чоловіча',
        dateOfSampling: '10.10.2021 20:40',
        dateOfExecution: '10.10.2021 22:40',
        address: ' вул. Підвисоцького, 6а',
        nameOfStudy: 'Коронавірус (SARS - Cov-2), COVID-19, PHK RT-ПЛР-якісний, FTD (терміновий)',
        resultOfStudy: 'Не виявлено',
        comment: 'Методика RT-ПЛР акредитована відповідно до стандарту ДСТУ ISO 15189'
      }
    }
  },
  components: {
    ResultsPart
  }
}
</script>

<style lang="scss" scoped>
.main-part {
  height: 1848px;

  &__block {
    height: 1848px;
    background-image: url("../../assets/images/main-bg.png");
    background-size: inherit;
    background-repeat: no-repeat;
    background-position: center -32px;
  }
}
</style>
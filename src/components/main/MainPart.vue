<template>
  <div class="main-part">
    <div class="container">
      <div class="main-part__block">

        <results-part
            class="main-part__results-part"
            :result="result"
        />

        <conclusion-part
            class="main-part__conclusion-part"
        />

        <remark-part
            class="main-part__remark-part"
            :result="result"
        />

      </div>
    </div>
  </div>
</template>

<script>
import ResultsPart from "./results/ResultsPart";
import ConclusionPart from "./conclusion/ConclusionPart";
import RemarkPart from "./remark/RemarkPart";

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
        comment: 'Методика RT-ПЛР акредитована відповідно до стандарту ДСТУ ISO 15189',
        doctor: 'Копацил Мезим Контролокович',
        dateOfPrinting: '11.09.2021 02:02:02'
      }
    }
  },
  components: {
    ResultsPart,
    ConclusionPart,
    RemarkPart
  }
}
</script>

<style lang="scss" scoped>
.main-part {
  min-height: 1848px;

  .container {
    padding: 0 16px;
  }


  &__block {
    min-height: 1848px;
    background-image: url("../../assets/images/main-bg.png");
    background-size: inherit;
    background-repeat: no-repeat;
    background-position: center -32px;
    width: 100%;
  }

  &__results-part {
    margin-bottom: 65px;
  }
}

@media (max-width: 428px) {
  .main-part {
    position: relative;
    min-height: 1815px;

    &__line-first {
      top: 14.1%;
    }

    &__block {
      min-height: 1815px;
      background-image: url("../../assets/images/main-bg-428.png");
      background-position: center top;
    }

    &__results-part {
      margin-bottom: 40px;
    }
  }
}
</style>
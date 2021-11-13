<template>
  <div class="main-part">

    <hr class="main-part__line-first">


    <div class="container">
      <div class="main-part__block">

        <results-part
            class="main-part__results-part"
            :result="result"
        />

        <conclusion-part
            class="main-part__conclusion-part"
        />

<!--        <remark-part-->
<!--            class="main-part__remark-part"-->
<!--            :result="result"-->
<!--        />-->

      </div>
    </div>
  </div>
</template>

<script>
import ResultsPart from "./results/ResultsPart";
import ConclusionPart from "./conclusion/ConclusionPart";
// import RemarkPart from "./remark/RemarkPart";

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
    // RemarkPart
  }
}
</script>

<style lang="scss" scoped>
.main-part {
  height: 1848px;

  &__line-first {
    display: none;
  }

  .container {
    padding: 0 16px;
  }


  &__block {
    height: 1848px;
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

    &__line-first {
      display: inline-block;
      height: 3px;
      width: 100%;
      background: #40A7E1;
      position: absolute;
    }

    &__line-first {
      top: 13.8%;
    }

    &__results-part {
      margin-bottom: 40px;
    }
  }
}
</style>
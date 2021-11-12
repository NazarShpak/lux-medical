<template>
  <div class="header-part">
    <div class="container">

      <!-- Top block -->
      <div class="header-part__block-top">

        <!-- Top info first block -->
        <div class="header-part__block-info-first">

          <!-- First info part -->
          <p class="header-part__info-first">
            Інформаційно-сервісна служба: 0 800 21 78 78
          </p>

          <!-- Second info part -->
          <p class="header-part__info-second">
            Україна, 01103, м. Київ, вул. Підвисоцького, 6A
          </p>
        </div>

        <!-- Logo -->
        <img
            alt
            class="header-part__logo"
            src="../../assets/icons/logo.png"
        >

        <!-- Top info second block -->
        <div class="header-part__block-info-second">

          <!-- Third info part -->
          <p class="header-part__info-third">
            lux-medical.online
          </p>

          <!-- Fourth info part -->
          <p class="header-part__info-fourth">
            0 800 21 78 78
          </p>
        </div>

      </div>

      <!-- Bottom block -->
      <div class="header-part__block-bottom">

        <h2 class="header-part__title">
          Гарантія точності та достовірності результатів досліджень!
        </h2>

        <div class="header-part__info-block">
          <p class="header-part__info">
            Атестат про акредитацію відповідно до ДСТУ EN ISO 15189:2015 (EN ISO 15189: 2012. IDT) ND 30001 від
            04.09.2020
            p
          </p>
        </div>

      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HeaderPart"
}
</script>

<style lang="scss" scoped>
.header-part {
  min-height: 337px;
  padding-top: 46px;
  background-image: url("../../assets/images/header-top-bg.png");
  background-size: inherit;
  background-repeat: no-repeat;
  background-position: center top;

  &__block-top,
  &__block-bottom {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    padding-bottom: 30px;
  }

  &__block-info-first {
    width: 377px;
    padding-left: 3px;
  }

  &__info-first {
    font-weight: 300;
    margin-bottom: 15px;
  }

  &__info-second {
    width: 239px;
    font-weight: 300;
    font-size: 21px;
    line-height: 25px;
  }

  &__logo {
    margin-right: 165px;
  }

  &__info-third {
    padding-right: 9px;
    font-weight: 300;
  }

  &__info-fourth {
    display: none;
  }

  &__block-bottom {
    padding: 0;
    flex-direction: column;
    align-items: center;
  }

  &__title {
    font-weight: 500;
    margin-bottom: 30px;
  }

  &__info-block {
    height: 57px;
    width: 100%;
    background: #F0F0F0;
    border-radius: 3px;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  &__info {
    font-size: 18px;
    line-height: 22px;
  }
}

@media (max-width: 428px) {
  .header-part {
    padding-top: 44px;
    background-image: url("../../assets/images/header-top-bg-428.png");
    position: relative;

    .container {
      padding: 0 16px;
    }

    &__block-top {
      margin-bottom: 122px;
      padding-bottom: 0;
    }

    &__block-info-first {
      width: auto;
    }

    &__info-first {
      display: none;
    }

    &__info-second {
      width: 158px;
      font-size: 14px;
      line-height: 17px;
    }

    &__logo {
      position: absolute;
      margin-right: 0;
      width: 173px;
      height: 112px;
      top: 95px;
      left: 50%;
      transform: translate(-50%);
    }

    &__info-third,
    &__info-fourth {
      font-weight: 300;
      font-size: 14px;
      line-height: 17px;
    }

    &__info-fourth {
      display: inline;
    }

    &__title {
      font-weight: 500;
      font-size: 16px;
      line-height: 23px;
      width: 284px;
      text-align: center;
      margin-bottom: 23px;
    }

    &__info {
      font-weight: 300;
      font-size: 12px;
      line-height: 20px;
      text-align: center;
      width: 369px;
    }

    &__info-block {
      height: 80px;
    }
  }
}

@media (max-width: 410px) {
  .header-part {
    background-image: url("../../assets/images/header-top-bg-390.png");

    &__info {
      width: 231px;
    }
  }
}
</style>
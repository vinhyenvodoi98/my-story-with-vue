<template>
  <div class="WhereILive">
    <div class="options">
      <div
        class="option"
        v-on:click="chagneImage(1)"
        v-bind:class="{active : isActive_1}"
        style="--optionBackground:url(https://66.media.tumblr.com/6fb397d822f4f9f4596dff2085b18f2e/tumblr_nzsvb4p6xS1qho82wo1_1280.jpg);"
      >
        <div class="shadow"></div>
        <div class="label">
          <div class="icon">
            <i class="fas fa-walking"></i>
          </div>
          <div class="info">
            <div class="main">Blonkisoaz</div>
            <div class="sub">Omuke trughte a otufta</div>
          </div>
        </div>
      </div>
      <div
        class="option"
        v-on:click="chagneImage(2)"
        v-bind:class="{active : isActive_2}"
        style="--optionBackground:url(https://66.media.tumblr.com/8b69cdde47aa952e4176b4200052abf4/tumblr_o51p7mFFF21qho82wo1_1280.jpg);"
      >
        <div class="shadow"></div>
        <div class="label">
          <div class="icon">
            <i class="fas fa-snowflake"></i>
          </div>
          <div class="info">
            <div class="main">Oretemauw</div>
            <div class="sub">Omuke trughte a otufta</div>
          </div>
        </div>
      </div>
      <div
        class="option"
        v-on:click="chagneImage(3)"
        v-bind:class="{active : isActive_3}"
        style="--optionBackground:url(https://66.media.tumblr.com/5af3f8303456e376ceda1517553ba786/tumblr_o4986gakjh1qho82wo1_1280.jpg);"
      >
        <div class="shadow"></div>
        <div class="label">
          <div class="icon">
            <i class="fas fa-tree"></i>
          </div>
          <div class="info">
            <div class="main">Iteresuselle</div>
            <div class="sub">Omuke trughte a otufta</div>
          </div>
        </div>
      </div>
      <div
        class="option"
        v-on:click="chagneImage(4)"
        v-bind:class="{active : isActive_4}"
        style="--optionBackground:url(https://66.media.tumblr.com/5516a22e0cdacaa85311ec3f8fd1e9ef/tumblr_o45jwvdsL11qho82wo1_1280.jpg);"
      >
        <div class="shadow"></div>
        <div class="label">
          <div class="icon">
            <i class="fas fa-tint"></i>
          </div>
          <div class="info">
            <div class="main">Idiefe</div>
            <div class="sub">Omuke trughte a otufta</div>
          </div>
        </div>
      </div>
      <div
        class="option"
        v-on:click="chagneImage(5)"
        v-bind:class="{active : isActive_5}"
        style="--optionBackground:url(https://66.media.tumblr.com/f19901f50b79604839ca761cd6d74748/tumblr_o65rohhkQL1qho82wo1_1280.jpg);"
      >
        <div class="shadow"></div>
        <div class="label">
          <div class="icon">
            <i class="fas fa-sun"></i>
          </div>
          <div class="info">
            <div class="main">Inatethi</div>
            <div class="sub">Omuke trughte a otufta</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
$optionDefaultColours: #ed5565, #fc6e51, #ffce54, #2ecc71, #5d9cec, #ac92ec;

body {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  overflow: hidden;

  height: 100vh;

  font-family: "Roboto", sans-serif;
  .credit {
    position: absolute;
    bottom: 20px;
    left: 20px;

    color: #000;
  }
  .options {
    margin: auto;
    display: flex;
    flex-direction: row;
    align-items: stretch;
    overflow: hidden;

    min-width: 600px;
    max-width: 900px;
    width: calc(100% - 100px);

    height: 400px;

    @for $i from 1 through 4 {
      @media screen and (max-width: 798px - $i*80) {
        min-width: 600px - $i * 80;
        .option:nth-child(#{6-$i}) {
          display: none;
        }
      }
    }

    .option {
      position: relative;
      overflow: hidden;

      min-width: 60px;
      margin: 10px;
      //border:0px solid --defaultColor;

      background: var(--optionBackground, var(--defaultBackground, #e6e9ed));
      background-size: auto 120%;
      background-position: center;

      cursor: pointer;

      transition: 0.5s cubic-bezier(0.05, 0.61, 0.41, 0.95);

      @for $i from 1 through length($optionDefaultColours) {
        &:nth-child(#{$i}) {
          --defaultBackground: #{nth($optionDefaultColours, $i)};
        }
      }
      &.active {
        flex-grow: 10000;
        transform: scale(1);

        max-width: 600px;
        margin: 0px;
        border-radius: 40px;

        background-size: auto 100%;
        .shadow {
          box-shadow: inset 0 -120px 120px -120px black,
            inset 0 -120px 120px -100px black;
        }
        .label {
          bottom: 20px;
          left: 20px;
          .info > div {
            left: 0px;
            opacity: 1;
          }
        }
        /*&:active {
               transform:scale(0.9);
            }*/
      }
      &:not(.active) {
        flex-grow: 1;

        border-radius: 30px;
        .shadow {
          bottom: -40px;
          box-shadow: inset 0 -120px 0px -120px black,
            inset 0 -120px 0px -100px black;
        }
        .label {
          bottom: 10px;
          left: 10px;
          .info > div {
            left: 20px;
            opacity: 0;
          }
        }
      }
      .shadow {
        position: absolute;
        bottom: 0px;
        left: 0px;
        right: 0px;

        height: 120px;

        transition: 0.5s cubic-bezier(0.05, 0.61, 0.41, 0.95);
      }
      .label {
        display: flex;
        position: absolute;
        right: 0px;

        height: 40px;
        transition: 0.5s cubic-bezier(0.05, 0.61, 0.41, 0.95);
        .icon {
          display: flex;
          flex-direction: row;
          justify-content: center;
          align-items: center;

          min-width: 40px;
          max-width: 40px;
          height: 40px;
          border-radius: 100%;

          background-color: white;
          color: var(--defaultBackground);
        }
        .info {
          display: flex;
          flex-direction: column;
          justify-content: center;

          margin-left: 10px;

          color: white;

          white-space: pre;
          > div {
            position: relative;

            transition: 0.5s cubic-bezier(0.05, 0.61, 0.41, 0.95),
              opacity 0.5s ease-out;
          }
          .main {
            font-weight: bold;
            font-size: 1.2rem;
          }
          .sub {
            transition-delay: 0.1s;
          }
        }
      }
    }
  }
}
</style>

<script>
export default {
  data: function() {
    return {
      isActive_1: true,
      isActive_2: false,
      isActive_3: false,
      isActive_4: false,
      isActive_5: false
    };
  },
  name: "WhereILive",
  methods: {
    chagneImage: function(number) {
      if (number === 1) {
        this.isActive_1 = true;
        this.isActive_2 = false;
        this.isActive_3 = false;
        this.isActive_4 = false;
        this.isActive_5 = false;
      }
      if (number === 2) {
        this.isActive_1 = false;
        this.isActive_2 = true;
        this.isActive_3 = false;
        this.isActive_4 = false;
        this.isActive_5 = false;
      }
      if (number === 3) {
        this.isActive_1 = false;
        this.isActive_2 = false;
        this.isActive_3 = true;
        this.isActive_4 = false;
        this.isActive_5 = false;
      }
      if (number === 4) {
        this.isActive_1 = false;
        this.isActive_2 = false;
        this.isActive_3 = false;
        this.isActive_4 = true;
        this.isActive_5 = false;
      }
      if (number === 5) {
        this.isActive_1 = false;
        this.isActive_2 = false;
        this.isActive_3 = false;
        this.isActive_4 = false;
        this.isActive_5 = true;
      }
    }
  }
};
</script>

<style lang="scss">
.p7 {
  background-image: url("/img/pages/6.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;

  //title 1
  .content1 {
    position: absolute;
    top: 263px;
    left: 28px;
    text-align: center;
    line-height: 13px;
    font-size: 8px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 90px;
      left: 100px;
      width: 200px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 90px;
      left: 10px;
      width: 100%;
    }

    .text {
      color: #ffffff;
      font-size: 0; //broke

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        font-size: 9px;
        line-height: 9px;
        font-weight: 900;
      }

      @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
        font-size: 0.65rem;
        line-height: 11px;
      }

      @media (min-width: $breakpoint-sm) and (max-width: 480px) {
        font-size: 9px;
        line-height: 9px;
        font-weight: 900;
      }
    }
  }
  //paragraf 1
  .content2 {
    position: absolute;
    top: 263px;
    left: 28px;
    text-align: left;
    line-height: 13px;
    font-size: 8px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 105px;
      left: 140px;
      width: 200px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 105px;
      left: 130px;
      width: 60%;
    }

    .text {
      color: #ffffff;
      font-size: 0; //broke

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        font-size: 7px;
        line-height: 9px;
        font-weight: 0;
      }

      @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
        font-size: 0.65rem;
        line-height: 11px;
      }

      @media (min-width: $breakpoint-sm) and (max-width: 480px) {
        font-size: 0.5rem;
        line-height: 9px;
      }
    }
  }
  //title 2
  .content3 {
    position: absolute;
    top: 263px;
    left: 28px;
    text-align: left;
    line-height: 13px;
    font-size: 8px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 220px;
      left: 140px;
      width: 200px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 210px;
      left: 120px;
      width: 80%;
    }

    .text {
      color: #ffffff;
      font-size: 0.7rem;

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        font-size: 9px;
        font-weight: 900;
        line-height: 9px;
      }

      @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
        font-size: 0.65rem;
        line-height: 11px;
      }

      @media (min-width: $breakpoint-sm) and (max-width: 480px) {
        font-size: 9px;
        line-height: 8px;
        font-weight: 900;
      }
    }
  }
  //paragraf 2
  .content4 {
    position: absolute;
    top: 263px;
    left: 28px;
    text-align: left;
    line-height: 14px;
    font-size: 8px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 235px;
      left: 140px;
      width: 220px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 225px;
      left: 130px;
      width: 166px;
    }

    .text {
      color: #ffffff;
      font-size: 0.7rem;

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        font-size: 7px;
        line-height: 9px;
        font-weight: 0;
      }

      @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
        font-size: 0.65rem;
        line-height: 11px;
      }

      @media (min-width: $breakpoint-sm) and (max-width: 480px) {
        font-size: 0.5rem;
        line-height: 9px;
      }
    }
  }
  //title 3
  .content5 {
    position: absolute;
    top: 263px;
    left: 1000px;
    text-align: left;
    line-height: 13px;
    font-size: 7px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 320px;
      left: 140px;
      width: 200px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 310px;
      left: 120px;
      width: 100%;
      font-weight: 900;
    }

    .text {
      color: #ffffff;
      font-size: 15px;

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        font-size: 9px;
        font-weight: 900;
        line-height: 9px;
      }

      @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
        font-size: 0.65rem;
        line-height: 11px;
      }

      @media (min-width: $breakpoint-sm) and (max-width: 480px) {
        font-size: 9px;
        line-height: 9px;
        font-weight: 900;
      }
    }
  }
  //paragraf 3
  .content6 {
    position: absolute;
    top: 263px;
    left: 1000px;
    text-align: left;
    line-height: 13px;
    font-size: 7px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 335px;
      left: 140px;
      width: 200px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 325px;
      left: 130px;
      width: 60%;
    }

    .text {
      color: #ffffff;
      font-size: 15px;

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        font-size: 7px;
        line-height: 9px;
        font-weight: 0;
      }

      @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
        font-size: 0.65rem;
        line-height: 11px;
      }

      @media (min-width: $breakpoint-sm) and (max-width: 480px) {
        font-size: 0.5rem;
        line-height: 9px;
      }
    }
  }
  
}
</style>

<template>
  <div>
    <div style="display: none">
      <div id="p6p1">{{ $t("p6.paragraph1") }}</div>
      <div id="p6p2">{{ $t("p6.paragraph2") }}</div>
      <div id="p6p3">{{ $t("p6.paragraph3") }}</div>
      <div id="p6p4">{{ $t("p6.paragraph4") }}</div>
      <div id="p6p5">{{ $t("p6.paragraph5") }}</div>
      <div id="p6p6">{{ $t("p6.paragraph6") }}</div>
    </div>
    <div class="content1">
      <div id="p6p1_" class="text"></div>
    </div>
    <div class="content2">
      <div id="p6p2_" class="text"></div>
    </div>
    <div class="content3">
      <div id="p6p3_" class="text"></div>
    </div>
    <div class="content4">
      <div id="p6p4_" class="text"></div>
    </div>
    <div class="content5">
      <div id="p6p5_" class="text"></div>
    </div>
    <div class="content6">
      <div id="p6p6_" class="text"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Page5",
  mounted() {
    let ref = this;
    ref.processText("p6p1");
    ref.processText("p6p2");
    ref.processText("p6p3");
    ref.processText("p6p4");
    ref.processText("p6p5");
    ref.processText("p6p6");
    window
      .jQuery("body")
      .on("DOMSubtreeModified", " #p6p1, #p6p2, #p6p3, #p6p4, #p6p5, #p6p6", function () {
        ref.processText(window.jQuery(this).attr("id"));
      });
  },
  methods: {
    processText(id) {
      let text = document.getElementById(id).textContent;
      let r = text.split("");
      document.getElementById(id + "_").innerHTML = "";
      window.jQuery.each(r, function (i, w) {
        var node = document.createElement("span");
        var textnode = document.createTextNode(
          w + (id.slice(-1) == "t" || id.slice(-1) == "s" ? "" : "")
        );
        node.appendChild(textnode);
        document.getElementById(id + "_").appendChild(node);
      });
    },
  },
};
</script>
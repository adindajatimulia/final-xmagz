<style lang="scss">
.p18 {
  background-image: url("/img/pages/17.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;

  .content1 {
    position: absolute;
    top: 200px;
    left: 60px;
    width: 270px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 32px;
      left: 16px;
      width: 54%;
      line-height: 15px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 172px;
      left: 50px;
      width: 211px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 35px;
      left: 10px;
      width: 170px;
    }

    .text {
      span {
        color: #ffffff;
        font-weight: 600;
        word-spacing: 1px;

        @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
          font-size: 18px;
        }

        @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
          font-size: 0.8rem;
        }

        @media (min-width: $breakpoint-sm) and (max-width: 480px) {
          font-size: 14px;
        }
      }
    }
  }

  //paragraf 2
  .content2 {
    position: absolute;
    top: 263px;
    left: 28px;
    text-align: left;
    line-height: 13px;
    font-size: 8px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 95px;
      left: 10px;
      width: 190px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 90px;
      left: 10px;
      width: 180px;
    }

    .text {
      color: #ffffff;
      font-size: 0.7rem;
      font-size: 900;

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        font-size: 7px;
        line-height: 9px;
      }

      @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
        font-size: 0.65rem;
        line-height: 11px;
      }

      @media (min-width: $breakpoint-sm) and (max-width: 480px) {
        font-size: 6.5px;
        line-height: 9px;
      }
    }
  }
  //paragraf 3
  .content3 {
    position: absolute;
    top: 263px;
    left: 28px;
    text-align: left;
    line-height: 13px;
    font-size: 8px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 188px;
      left: 10px;
      width: 190px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 182px;
      left: 10px;
      width: 166px;
    }

    .text {
      color: #ffffff;
      font-size: 0.7rem;

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        font-size: 7px;
        line-height: 9px;
      }

      @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
        font-size: 0.65rem;
        line-height: 11px;
      }

      @media (min-width: $breakpoint-sm) and (max-width: 480px) {
        font-size: 6.5px;
        line-height: 8px;
      }
    }
  }
  //paragraf 4
  .content4 {
    position: absolute;
    top: 263px;
    left: 1000px;
    text-align: left;
    line-height: 13px;
    font-size: 7px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 160px;
      left: 205px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 150px;
      left: 185px;
      width: 130px;
    }

    .text {
      color: #ffffff;
      font-size: 15px;

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        font-size: 7.7px;
        line-height: 9px;
      }

      @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
        font-size: 0.65rem;
        line-height: 11px;
      }

      @media (min-width: $breakpoint-sm) and (max-width: 480px) {
        font-size: 6.5px;
        line-height: 9px;
      }
    }
  }
}
</style>

<template>
  <div>
    <div style="display: none">
      <div id="p17p1">{{ $t("p17.paragraph1") }}</div>
      <div id="p17p2">{{ $t("p17.paragraph2") }}</div>
      <div id="p17p3">{{ $t("p17.paragraph3") }}</div>
      <div id="p17p4">{{ $t("p17.paragraph4") }}</div>
    </div>
    <div class="content1">
      <div id="p17p1_" class="text text1"></div>
    </div>
    <div class="content2">
      <div id="p17p2_" class="text"></div>
    </div>
    <div class="content3">
      <div id="p17p3_" class="text"></div>
    </div>
    <div class="content4">
      <div id="p17p4_" class="text"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Page17",
  mounted() {
    let ref = this;
    ref.processText("p17p1");
    ref.processText("p17p2");
    ref.processText("p17p3");
    ref.processText("p17p4");
    window
      .jQuery("body")
      .on("DOMSubtreeModified", " #p17p1, #p17p2, #p17p3, #p17p4", function () {
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
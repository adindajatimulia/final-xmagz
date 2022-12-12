<style lang="scss">
.p17 {
  background-image: url("/img/pages/16.jpg");
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
      top: 13px;
      left: 13px;
      width: 60%;
      line-height: 7px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 172px;
      left: 50px;
      width: 211px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 10px;
      left: 7px;
      width: 200px;
      line-height: 6.5px;
    }

    .text {
      span {
        color: #ffffff;
        font-weight: 0;
        word-spacing: 1px;

        @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
          font-size: 8px;
        }

        @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
          font-size: 0.8rem;
        }

        @media (min-width: $breakpoint-sm) and (max-width: 480px) {
          font-size: 8px;
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
      top: 167px;
      left: 150px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 155px;
      left: 135px;
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
        font-size: 6px;
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
      top: 222px;
      left: 150px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 200px;
      left: 135px;
      width: 180px;
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
        font-size: 6px;
        line-height: 10px;
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
      top: 277px;
      left: 150px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 260px;
      left: 135px;
      width: 180px;
    }

    .text {
      color: #ffffff;
      font-size: 15px;

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        font-size: 7px;
        line-height: 9px;
      }

      @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
        font-size: 0.65rem;
        line-height: 11px;
      }

      @media (min-width: $breakpoint-sm) and (max-width: 480px) {
        font-size: 6px;
        line-height: 9px;
      }
    }
  }
}
</style>

<template>
  <div>
    <div style="display: none">
      <!-- <div id="p16t">{{ $t("p16.title") }}</div> -->
      <div id="p16p1">{{ $t("p16.paragraph1") }}</div>
      <div id="p16p2">{{ $t("p16.paragraph2") }}</div>
      <div id="p16p3">{{ $t("p16.paragraph3") }}</div>
      <div id="p16p4">{{ $t("p16.paragraph4") }}</div>
    </div>
    <div class="content1">
      <div id="p16p1_" class="text text1"></div>
    </div>

    <div class="content2">
      <div id="p16p2_" class="text"></div>
    </div>
    <div class="content3">
      <div id="p16p3_" class="text"></div>
    </div>
    <div class="content4">
      <div id="p16p4_" class="text"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Page15",
  mounted() {
    let ref = this;
    // ref.processText("p16t");
    ref.processText("p16p1");
    ref.processText("p16p2");
    ref.processText("p16p3");
    ref.processText("p16p4");
    window
      .jQuery("body")
      .on("DOMSubtreeModified", " #p16p1, #p16p2, #p16p3, #p16p4", function () {
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
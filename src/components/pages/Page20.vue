<style lang="scss">
.p21 {
  background-image: url("/img/pages/20.jpg");
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
      top: 30px;
      left: 10px;
      width: 70%;
      line-height: 20px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 172px;
      left: 50px;
      width: 211px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 30px;
      left: 10px;
      width: 197px;
    }

    .text {
      span {
        color: #000066;
        font-weight: 900;
        word-spacing: 1px;

        @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
          font-size: 15px;
        }

        @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
          font-size: 0.8rem;
        }

        @media (min-width: $breakpoint-sm) and (max-width: 480px) {
          font-size: 15px;
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
      top: 140px;
      left: 10px;
      width: 55%;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 122px;
      left: 10px;
      width: 166px;
    }

    .text {
      color: #ffffff;
      font-size: 0.7rem;
      font-size: 900;

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        font-size: 8px;
        line-height: 11px;
      }

      @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
        font-size: 0.65rem;
        line-height: 11px;
      }

      @media (min-width: $breakpoint-sm) and (max-width: 480px) {
        font-size: 7.5px;
        line-height: 9.7px;
      }
    }
  }
  //paragraf 3
  /*.content3 {
    position: absolute;
    top: 263px;
    left: 28px;
    text-align: left;
    line-height: 13px;
    font-size: 8px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 140px;
      left: 200px;
      width: 40%;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 172px;
      left: 24px;
      width: 166px;
    }

    .text {
      color: #ffffff;
      font-size: 0.7rem;

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        font-size: 7px;
        line-height: 10px;
      }

      @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
        font-size: 0.65rem;
        line-height: 11px;
      }

      @media (min-width: $breakpoint-sm) and (max-width: 480px) {
        font-size: 0.5rem;
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
      top: 172px;
      left: 24px;
      width: 166px;
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
        font-size: 0.5rem;
        line-height: 9px;
      }
    }
  }*/
}
</style>

<template>
  <div>
    <div style="display: none">
      <div id="p20p1">{{ $t("p20.paragraph1") }}</div>
      <div id="p20p2">{{ $t("p20.paragraph2") }}</div>
      <!-- <div id="p19p3">{{ $t("p19.paragraph3") }}</div> -->
      <!-- <div id="p17p4">{{ $t("p17.paragraph4") }}</div> -->
    </div>
    <div class="content1">
      <div id="p20p1_" class="text text1"></div>
    </div>

    <div class="content2">
      <div id="p20p2_" class="text"></div>
    </div>
    <!-- <div class="content3">
      <div id="p19p3_" class="text"></div>
    </div> -->
    <!-- <div class="content4">
      <div id="p17p4_" class="text"></div>
    </div> -->
  </div>
</template>

<script>
export default {
  name: "Page20",
  mounted() {
    let ref = this;
    // ref.processText("p16t");
    ref.processText("p20p1");
    ref.processText("p20p2");
    // ref.processText("p19p3");
    // ref.processText("p17p4");
    window
      .jQuery("body")
      .on("DOMSubtreeModified", " #p20p1, #p20p2", function () {
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
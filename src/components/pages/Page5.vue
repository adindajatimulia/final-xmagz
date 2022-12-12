<style lang="scss">
.p6 {
  background-image: url("/img/pages/5.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;

  //title 
  .content1 {
    position: absolute;
    width: 100px;
    text-align: left;
    

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 15px;
      left: 20px;
      width: 280px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 172px;
      left: 50px;
      width: 211px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 13px;
      left: 15px;
      width: 90%;
    }

    .text {
      span {
        color: #ffffff;
        font-weight: 700;

        @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
          font-size: 30px;
          
        }

        @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
          font-size: 0.8rem;
        }

        @media (min-width: $breakpoint-sm) and (max-width: 480px) {
          font-size: 30px;
        }
      }
    }
  }
  //title 1
  .content2 {
    position: absolute;
    top: 263px;
    left: 28px;
    text-align: center;
    line-height: 13px;
    font-size: 8px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 120px;
      left: 130px;
      width: 200px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 110px;
      left: 60px;
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
  .content3 {
    position: absolute;
    top: 263px;
    left: 28px;
    text-align: left;
    line-height: 13px;
    font-size: 8px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 135px;
      left: 130px;
      width: 200px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 125px;
      left: 130px;
      width: 60%;
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
        font-size: 0.5rem;
        line-height: 8px;
      }
    }
  }
  //title 2
  .content4 {
    position: absolute;
    top: 263px;
    left: 28px;
    text-align: center;
    line-height: 13px;
    font-size: 8px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 240px;
      left: 130px;
      width: 220px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 230px;
      left: 90px;
      width: 80%;
    }

    .text {
      color: #ffffff;
      font-size: 0.7rem;

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
        font-size: 0.5rem;
        line-height: 8px;
        font-weight: 900;
      }
    }
  }
  //paragraf 2
  .content5 {
    position: absolute;
    top: 263px;
    left: 1000px;
    text-align: left;
    line-height: 13px;
    font-size: 7px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 260px;
      left: 130px;
      width: 200px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 242px;
      left: 130px;
      width: 60%;
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
  }
  //title 3
  .content6 {
    position: absolute;
    top: 263px;
    left: 1000px;
    text-align: left;
    line-height: 13px;
    font-size: 7px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 370px;
      left: 130px;
      width: 200px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 345px;
      left: 125px;
      width: 100%;
      font-weight: 900;
    }

    .text {
      color: #ffffff;
      font-size: 15px;

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
      }
    }
  }
  //paragraf 3
  .content7 {
    position: absolute;
    top: 263px;
    left: 1000px;
    text-align: left;
    line-height: 13px;
    font-size: 7px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 390px;
      left: 130px;
      width: 200px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 360px;
      left: 130px;
      width: 60%;
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
  }
  
}
</style>

<template>
  <div>
    <div style="display: none">
      <div id="p5p1">{{ $t("p5.paragraph1") }}</div>
      <div id="p5p2">{{ $t("p5.paragraph2") }}</div>
      <div id="p5p3">{{ $t("p5.paragraph3") }}</div>
      <div id="p5p4">{{ $t("p5.paragraph4") }}</div>
      <div id="p5p5">{{ $t("p5.paragraph5") }}</div>
      <div id="p5p6">{{ $t("p5.paragraph6") }}</div>
      <div id="p5p7">{{ $t("p5.paragraph7") }}</div>
    </div>
    <div class="content1">
      <div id="p5p1_" class="text"></div>
    </div>
    <div class="content2">
      <div id="p5p2_" class="text"></div>
    </div>
    <div class="content3">
      <div id="p5p3_" class="text"></div>
    </div>
    <div class="content4">
      <div id="p5p4_" class="text"></div>
    </div>
    <div class="content5">
      <div id="p5p5_" class="text"></div>
    </div>
    <div class="content6">
      <div id="p5p6_" class="text"></div>
    </div>
    <div class="content7">
      <div id="p5p7_" class="text"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Page5",
  mounted() {
    let ref = this;
    ref.processText("p5p1");
    ref.processText("p5p2");
    ref.processText("p5p3");
    ref.processText("p5p4");
    ref.processText("p5p5");
    ref.processText("p5p6");
    ref.processText("p5p7");
    window
      .jQuery("body")
      .on("DOMSubtreeModified", " #p5p1, #p5p2, #p5p3, #p5p4, #p5p5, #p5p6, #p5p7", function () {
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
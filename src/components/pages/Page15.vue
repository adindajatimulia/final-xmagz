<style lang="scss">
.p16 {
  background-image: url("/img/pages/15.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;

  
  .content1 {
    position: absolute;
    top: 204px;
    left: 60px;
    width: 270px;
    line-height:15px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 290px;
      left: 20px;
      width: 40%;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 172px;
      left: 50px;
      width: 211px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 270px;
      left: 10px;
      width: 140px;
    }

    .title {
      span {
        color: #ffffff;
        font-weight: 100;
        word-spacing: 1px;
        line-height:0px;

        @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
          font-size: 10px;
          font-weight: 600;
          line-height: 2px!important;
        }

        @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
          font-size: 0.8rem;
        }

        @media (min-width: $breakpoint-sm) and (max-width: 480px) {
          font-size: 0.6rem;
        }
      }
    }
  }
  //paragraf 1
  .content2 {
    position: absolute;
    top: 263px;
    left: 28px;
    width: 240px;
    text-align: left;
    line-height: 13px;
    font-size: 8px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 295px;
      left: 180px;
      width: 50%;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 275px;
      left: 160px;
      width: 160px;
    }

    .text {
      color: #ffffff;
      font-size: 0.7rem;
      font-size: 900;

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        font-size: 9px;
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
  //paragraf 2
  .content3 {
    position: absolute;
    top: 263px;
    left: 28px;
    width: 240px;
    text-align: left;
    line-height: 13px;
    font-size: 8px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 340px;
      left: 180px;
      width: 25%;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 315px;
      left: 160px;
      width: 23%;
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
        line-height: 8px;
      }
    }
  }
  //paragraf 3
  .content4 {
    position: absolute;
    top: 263px;
    text-align: left;
    line-height: 13px;
    font-size: 7px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 340px;
      left: 270px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 314px;
      left: 235px;
      width: 25%;
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
      <div id="p15t">{{ $t("p15.title") }}</div>
      <div id="p15p1">{{ $t("p15.paragraph1") }}</div>
      <div id="p15p2">{{ $t("p15.paragraph2") }}</div>
      <div id="p15p3">{{ $t("p15.paragraph3") }}</div>
    </div>
    <div class="content1">
      <div id="p15t_" class="title"></div>
    </div>

    <div class="content2">
      <div id="p15p1_" class="text text1"></div>
    </div>
    <div class="content3">
      <div id="p15p2_" class="text"></div>
    </div>
    <div class="content4">
      <div id="p15p3_" class="text"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Page15",
  mounted() {
    let ref = this;
    ref.processText("p15t");
    ref.processText("p15p1");
    ref.processText("p15p2");
    ref.processText("p15p3");
    window
      .jQuery("body")
      .on("DOMSubtreeModified", "#p15t, #p15p1, #p15p2, #p15p3", function () {
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
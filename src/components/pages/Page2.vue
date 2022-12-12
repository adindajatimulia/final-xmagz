<style lang="scss">
.p3 {
  background-image: url("/img/pages/2.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;

  //title
  .content1 {
    position: absolute;
    top: 200px;
    left: 60px;
    width: 270px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 240px;
      left: 10px;
      width: 100%;
      line-height: 24px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 172px;
      left: 50px;
      width: 211px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 225px;
      left: 20px;
      width: 197px;
    }

    .text {
      span {
        color: #ffffff;
        font-weight: 900;
        word-spacing: 1px;

        @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
          font-size: 32px;
        }

        @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
          font-size: 0.8rem;
        }

        @media (min-width: $breakpoint-sm) and (max-width: 480px) {
          font-size: 0.8rem;
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
      top: 270px;
      left: 10px;
      width: 40%;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 250px;
      left: 15px;
      width: 140px;
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
        font-size: 8px;
        line-height: 8px;
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
      top: 270px;
      left: 165px;
      width: 50%;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 250px;
      left: 165px;
      width: 150px;
    }

    .text {
      color: #ffffff;
      font-size: 0.7rem;

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        font-size: 8px;
        line-height: 11px;
      }

      @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
        font-size: 0.65rem;
        line-height: 11px;
      }

      @media (min-width: $breakpoint-sm) and (max-width: 480px) {
        font-size: 8px;
        line-height: 8px;
      }
    }
  }
}
</style>

<template>
  <div>
    <div style="display: none">
      <div id="p2p1">{{ $t("p2.paragraph1") }}</div>
      <div id="p2p2">{{ $t("p2.paragraph2") }}</div>
      <div id="p2p3">{{ $t("p2.paragraph3") }}</div>
    </div>
    <div class="content1">
      <div id="p2p1_" class="text text1"></div>
    </div>

    <div class="content2">
      <div id="p2p2_" class="text"></div>
    </div>
    <div class="content3">
      <div id="p2p3_" class="text"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Page17",
  mounted() {
    let ref = this;
    ref.processText("p2p1");
    ref.processText("p2p2");
    ref.processText("p2p3");
    window
      .jQuery("body")
      .on("DOMSubtreeModified", " #p2p1, #p2p2, #p2p3", function () {
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
<style lang="scss">
.p13 {
  background-image: url("/img/pages/12.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;

  .content1 {
    position: absolute;
    top: 26px;
    left: 60px;
    width: 412px;
    line-height:30px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 15px;
      left: 30px;
      width: 300px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 30px;
      left: 50px;
      width: 300px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 15px;
      left: 20px;
      width: 283px;
    }

    .title {
      color: #000066;
      font-size: 3rem;

      @media (min-width: $breakpoint-sm) and (max-width: ($breakpoint-xl - 1px)) {
        font-size: 2rem;
      }

      span {
        font-weight: 900;
      }
    }
  }

  .content {
    line-height: 10px;
    left: 51px;
    right: 10000px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      right: 200px;
      left: 30px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      left: 42px;
      width: 338px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      left: 15px;
      width: 150px;
    }

    &.content2 {
      position: absolute;
      top: 170px;

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        top: 90px;
      }

      @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
        top: 136px;
      }

      @media (min-width: $breakpoint-sm) and (max-width: 480px) {
        top: 95px;
      }
    }

    &.content3 {
      position: absolute;
      top: 307px;

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        top: 210px;
        
      }

      @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
        top: 276px;
      }

      @media (min-width: $breakpoint-sm) and (max-width: 480px) {
        top: 200px;
      }
    }

    &.content4 {
      position: absolute;
      top: 500px;

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        top: 90px;
        right: 0px;
        left: 180px;
      }

      @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
        top: 443px;
      }

      @media (min-width: $breakpoint-sm) and (max-width: 480px) {
        top: 90px;
        left: 170px;
      }
    }

    .text {
      font-size: 8px;
      line-height: 12px;

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        font-size: 8px;
        line-height: 9.2px;
        font-weight: 900;
      }

      @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
        font-size: 0.55rem;
        line-height: 10px;
      }

      @media (min-width: $breakpoint-sm) and (max-width: 480px) {
        font-size: 9px;
        line-height: 9px;
      }

      .title {
        margin-bottom: 5px;

        span {
          font-weight: 900;
        }
      }
    }
  }
}
</style>

<template>
  <div>
    <div style="display: none">
      <div id="p12pt">{{ $t("p12.title") }}</div>
      <div id="p12p1">{{ $t("p12.paragraph1") }}</div>
      <div id="p12p2">{{ $t("p12.paragraph2") }}</div>
      <div id="p12p3">{{ $t("p12.paragraph3") }}</div>
    </div>

    <div class="content1">
      <div id="p12pt_" class="title"></div>
    </div>
    <div class="content content2">
      <div class="text">
        <div id="p12p1_" class="desc"></div>
      </div>
    </div>
    <div class="content content3">
      <div class="text">
        <div id="p12p2_" class="desc"></div>
      </div>
    </div>
    <div class="content content4">
      <div class="text">
        <div id="p12p3_" class="desc"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Page12",
  mounted() {
    let ref = this;
    ref.processText("p12pt");
    ref.processText("p12p1");
    ref.processText("p12p2");
    ref.processText("p12p3");
    window
      .jQuery("body")
      .on(
        "DOMSubtreeModified",
        "#p12pt,#p12p1,#p12p2,#p12p3",
        function () {
          ref.processText(window.jQuery(this).attr("id"));
        }
      );
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
    showImage(url) {
      this.$parent.showImage(url);
    },
  },
};
</script>
<style lang="scss">
.p4 {
  background-image: url("/img/pages/3.jpg");
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
      top: 70px;
      left: 35px;
      width: 80%;
      line-height: 28px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 172px;
      left: 50px;
      width: 211px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 60px;
      left: 29px;
      width: 210px;
      line-height: 22px;
      letter-spacing: 0px;
    }

    .text {
      span {
        color: #ffffff;
        font-weight: 900;
        word-spacing: 8px;

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

  //paragraf 1
  .content2 {
    position: absolute;
    top: 263px;
    left: 28px;
    text-align: left;
    line-height: 13px;
    font-size: 8px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 190px;
      left: 35px;
      width: 80%;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 150px;
      left: 30px;
      width: 80%;
    }

    .text {
      color: #ffffff;
      font-size: 0.7rem;
      font-size: 900;

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        font-size: 10px;
        line-height: 12px;
      }

      @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
        font-size: 0.65rem;
        line-height: 11px;
      }

      @media (min-width: $breakpoint-sm) and (max-width: 480px) {
        font-size: 10px;
        line-height: 12px;
      }
    }
    .text::first-letter{
      font-size: 30px;
    }
  }
}
</style>

<template>
  <div>
    <div style="display: none">
      <div id="p3p1">{{ $t("p3.paragraph1") }}</div>
      <div id="p3p2">{{ $t("p3.paragraph2") }}</div>
    </div>
    <div class="content1">
      <div id="p3p1_" class="text text1"></div>
    </div>

    <div class="content2">
      <div id="p3p2_" class="text"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Page3",
  mounted() {
    let ref = this;
    ref.processText("p3p1");
    ref.processText("p3p2");
    window
      .jQuery("body")
      .on("DOMSubtreeModified", " #p3p1, #p3p2", function () {
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
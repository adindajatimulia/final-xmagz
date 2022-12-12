<style lang="scss">
.p19 {
  background-image: url("/img/pages/18.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;

  .content1 {
    position: absolute;
    top: 200px;
    left: 60px;
    width: 290px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 170px;
      left: 35px;
      width: 70%;
      line-height: 15px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 172px;
      left: 50px;
      width: 211px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 160px;
      left: 29px;
      width: 197px;
      line-height: 13px;
    }

    .text {
      span {
        color: #ffffff;
        font-weight: 900;
        word-spacing: 1px;

        @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
          font-size: 15px;
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
      top: 220px;
      left: 35px;
      width: 280px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 202px;
      left: 30px;
      width: 265px;
    }

    .text {
      color: #ffffff;
      font-size: 0.7rem;
      font-size: 900;

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        font-size: 8px;
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
      <div id="p18p1">{{ $t("p18.paragraph1") }}</div>
      <div id="p18p2">{{ $t("p18.paragraph2") }}</div>
      <!-- <div id="p17p3">{{ $t("p18.paragraph3") }}</div>
      <div id="p18p4">{{ $t("p18.paragraph4") }}</div> -->
    </div>
    <div class="content1">
      <div id="p18p1_" class="text text1"></div>
    </div>

    <div class="content2">
      <div id="p18p2_" class="text"></div>
    </div>
    <!-- <div class="content3">
      <div id="p18p3_" class="text"></div>
    </div>
    <div class="content4">
      <div id="p18p4_" class="text"></div>
    </div> -->
  </div>
</template>

<script>
export default {
  name: "Page17",
  mounted() {
    let ref = this;
    ref.processText("p18p1");
    ref.processText("p18p2");
    // ref.processText("p18p3");
    // ref.processText("p18p4");
    window
      .jQuery("body")
      .on("DOMSubtreeModified", " #p18p1, #p18p2", function () {
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
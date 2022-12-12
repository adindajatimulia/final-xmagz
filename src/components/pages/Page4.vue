<style lang="scss">
.p5 {
  background-image: url("/img/pages/4.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;

  .content1 {
    position: absolute;
    top: 204px;
    left: 60px;
    width: 270px;
    color: #ffffff;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 25px;
      left: 10px;
      width: 45%;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 172px;
      left: 50px;
      width: 211px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 10px;
      left: 10px;
      width: 45%;
    }

    .text {
      color: #ffffff;
      font-weight: 0;
      word-spacing: 1px;

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        font-size: 10px;
        font-weight: 0;
        line-height: 12px;
      }

      @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
        font-size: 0.8rem;
      }

      @media (min-width: $breakpoint-sm) and (max-width: 480px) {
        font-size: 10px;
        line-height: 10px;
      }
    }
  }

  //paragraf 2
  .content2 {
    position: absolute;
    top: 263px;
    left: 28px;
    width: 240px;
    text-align: left;
    line-height: 13px;
    font-size: 8px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 25px;
      left: 180px;
      width: 48%;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 229px;
      left: 27px;
      width: 207px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 10px;
      left: 160px;
      width: 50%;
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
        line-height: 10px;
      }
    }
  }
}
</style>

<template>
  <div>
    <div style="display: none">
      
      <div id="p4p1">{{ $t("p4.paragraph1") }}</div>
      <div id="p4p2">{{ $t("p4.paragraph2") }}</div>
    </div>
    <div class="content1">
      <div id="p4p1_" class="text text1"></div>
    </div>
    <div class="content2">
      <div id="p4p2_" class="text"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Page15",
  mounted() {
    let ref = this;
    ref.processText("p4p1");
    ref.processText("p4p2");
    window
      .jQuery("body")
      .on("DOMSubtreeModified", "#p4p1, #p4p2", function () {
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
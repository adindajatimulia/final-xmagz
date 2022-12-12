<style lang="scss">
.p2 {
  background-image: url("/img/pages/1.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;

  //paragraf 1
  .content1 {
    position: absolute;
    top: 200px;
    left: 60px;
    width: 270px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 31px;
      left: 16px;
      width: 80%;
      line-height: 22px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 172px;
      left: 50px;
      width: 211px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 20px;
      left: 20px;
      width: 60%;
    }

    .text {
      span {
        color: #ffffff;
        font-weight: 600;
        word-spacing: 2px;

        @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
          font-size: 30px;
        }

        @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
          font-size: 0.8rem;
        }

        @media (min-width: $breakpoint-sm) and (max-width: 480px) {
          font-size: 20px;
        }
      }
    }
  }
}
</style>

<template>
  <div>
    <div style="display: none">
      <div id="p1p1">{{ $t("p1.paragraph1") }}</div>
    </div>
    <div class="content1">
      <div id="p1p1_" class="text text1"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Page1",
  mounted() {
    let ref = this;
    ref.processText("p1p1");
    window
      .jQuery("body")
      .on("DOMSubtreeModified", " #p1p1", function () {
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
<style lang="scss" >

.p12 {
  background-image: url("/img/pages/11.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;


  .content2 {
    position: absolute;
    font-size: 0.7rem;
    text-align: left;
    color: #ffffff;
    word-spacing: 2px;
    

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      left: 20px;
      font-size: 8px;
      font-family: 'monserrat';
      top: 150px;
      width: 185px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 202px;
      width: 210px;
      left: 185px;
      font-size: 0.65rem;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 134px;
      width: 181px;
      left: 10px;
      font-size: 0.5rem;
    }

    .text1 {
      line-height: 16px;
      margin-top: 5px;

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        line-height: 10px;
        right: 60px;
        font-weight: 600;
      }

      @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
        line-height: 11px;
      }

      @media (min-width: $breakpoint-sm) and (max-width: 480px) {
        line-height: 9.7px;
      }
    }
  }
}
</style>

<template>
  <div>
    <div style="display: none">
      <div id="p11p1">{{ $t("p11.paragraph1") }}</div>
    </div>
    <div class="content2">
      <div id="p11p1_" class="text1"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Page11",
  mounted() {
    let ref = this;
    ref.processText("p11p1");
    window
      .jQuery("body")
      .on("DOMSubtreeModified", ", #p11p1", function () {
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
<style lang="scss">
.p23 {
  background-image: url("/img/pages/22.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;

  .content1 {
    color: #ffffff;
    position: absolute;
    top: 50px;
    left: 10px;
    right: 45px;

    .title {
      font-size: 2rem;
      line-height: 30px;

      @media (min-width: $breakpoint-sm) and (max-width: ($breakpoint-xl - 1px)) {
        font-size: 3rem;
        line-height: 45px;
        letter-spacing: 4x;
      }

      span {
        font-weight: 900;
      }
    }

  }

  .row {
    position: absolute;
    top: 335px;
    font-size: 0.7rem;
    text-align: left;
    text-indent: 0px;
    right: 100px;
    letter-spacing: 0.2px;
    color: #ffffff;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 135px;
      font-size: 10px;
      line-height: 14px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 290px;
      font-size: 0.65rem;
      line-height: 13px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 150px;
      font-size: 0.5rem;
      line-height: 10px;
    }

    .content2 {
      padding-left: 15px;
      padding-right: 0px;
      font-weight: 200;
    }

    .content3 {
      padding-left: 15px;
      padding-right: 15px;
    }

    .content3 {
      padding-left: 15px;
      padding-right: 15px;
    }

    .content4 {
      padding-left: 15px;
      padding-right: 15px;
    }
  }
}
</style>

<template>
  <div>
    <div style="display: none">
      <div id="p22t">{{ $t("p22.title") }}</div>
      <div id="p22p1">{{ $t("p22.paragraph1") }}</div>
    </div>

    <div class="content1">
      <div id="p22t_" class="title"></div>
    </div>

    <div class="row">
      <div id="p22p1_" class="content2"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Page22",
  mounted() {
    let ref = this;
    ref.processText("p22t");
    ref.processText("p22p1");
    window
      .jQuery("body")
      .on(
        "DOMSubtreeModified",
        "#p22t,#p22p1",
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
  },
};
</script>
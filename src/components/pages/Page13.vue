<style lang="scss">
.p14 {
  background-image: url("/img/pages/13.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;

  .content1 {
    color: #000066;
    position: absolute;
    top: 10px;
    left: 10px;
    right: 30px;

    .title {
      font-size: 2rem;
      line-height: 30px;

      @media (min-width: $breakpoint-sm) and (max-width: ($breakpoint-xl - 1px)) {
        font-size: 1.3rem;
        line-height: 24px;
        width: 80%;
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
    right: 110px;
    letter-spacing: 0.2px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 129px;
      font-size: 8px;
      line-height: 11px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 290px;
      font-size: 0.65rem;
      line-height: 13px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 110px;
      font-size: 0.5rem;
      line-height: 10.5px;
      width: 67%;
      left: 10px;
    }

    .content2 {
      padding-left: 0px;
      padding-right: 15px;
      font-weight: 900;
    }
  }
}
</style>

<template>
  <div>
    <div style="display: none">
      <div id="p13t">{{ $t("p13.title") }}</div>
      <div id="p13p1">{{ $t("p13.paragraph1") }}</div>
    </div>

    <div class="content1">
      <div id="p13t_" class="title"></div>
    </div>
    <div class="row">
      <div id="p13p1_" class="content2"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Page13",
  mounted() {
    let ref = this;
    ref.processText("p13t");
    ref.processText("p13p1");
    window
      .jQuery("body")
      .on(
        "DOMSubtreeModified",
        "#p13t,,#p13p1",
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
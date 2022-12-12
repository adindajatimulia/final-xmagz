<style lang="scss">
.p15 {
  background-image: url("/img/pages/14.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;

  .content {
    text-align: left;
    font-size: 0.7rem;
    line-height: 14px;
    text-indent: 0px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      font-size: 1.1rem;
      line-height: 17px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      font-size: 0.65rem;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      font-size: 0.5rem;
      line-height: 9px;
    }

    //title
    &.content1 {
      position: absolute;
      color: #000066;
      top: 50px;
      left: 20px;
      width: 368px;

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        top: 160px;
        width: 275px;
        font-weight: 900;
      }

      @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
        top: 35px;
        width: 275px;
      }

      @media (min-width: $breakpoint-sm) and (max-width: 480px) {
        top: 150px;
        width: 230px;
      }

      span {
        font-weight: 900;
      }
    }

    //paragraf1
    &.content2 {
      position: absolute;
      top: 120px;
      display: grid;
      bottom: 100px;
      grid-template-columns: 55% 55%;

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        top: 215px;
        font-size: 8px;
        font-weight: 900;
        line-height: 10.2px;
        bottom: 0px; //tidak bisa
      }

      @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
        top: 35px;
      }

      @media (min-width: $breakpoint-sm) and (max-width: 480px) {
        top: 175px;
        left: 20px;
        width: 90%;
      }

      & > div {
        &:first-child {
          padding-left: 0px;
        }

        padding-left: 10px;
        padding-right: 10px;
      }
    }

    //paragraf2
    &.content3 {
      position: absolute;
      top: 100px;

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        top: 0px;
        left: 180px;
        font-size: 8px;
        font-weight: 900;
        line-height: 10.2px;
      }

      @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
        top: 35px;
      }

      @media (min-width: $breakpoint-sm) and (max-width: 480px) {
        top: 0px;
        left: 140px;
        width: 55%;
      }
    }
  }
}
</style>

<template>
  <div>
    <div style="display: none">
      <div id="p14t">{{ $t("p14.title") }}</div>
      <div id="p14p1">{{ $t("p14.paragraph1") }}</div>
      <div id="p14p3">{{ $t("p14.paragraph3") }}</div>
    </div>

    <div id="p14t_" class="content content1"></div>
    <div class="content content2">
      <div>
        <div id="p14p1_"></div>
      </div>
      <div id="p14p3_" class="content content3"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Page14",
  mounted() {
    let ref = this;
    ref.processText("p14t");
    ref.processText("p14p1");
    ref.processText("p14p3");
    window
      .jQuery("body")
      .on(
        "DOMSubtreeModified",
        "#p14t,#p14p1,#p14p3",
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
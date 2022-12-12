<style lang="scss">
.p11 {
  background-image: url("/img/pages/10.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;

  .content1 {
    color: #ffffff;
    position: absolute;
    top: 500px;
    width: 203px;
    text-align: left;
    text-indent: 10px;
    line-height: 12px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 120px;
      right: 25px;
      width: 144px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 45px;
      left: 26px;
      width: 174px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 115px;
      left: 165px;
      width: 150px;
    }
    .text {
      font-size: 200px;

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        font-size: 6.6px;
        line-height: 8.5px;
      }

      @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
        font-size: 0.69rem;
        line-height: 10px;
      }

      @media (min-width: $breakpoint-sm) and (max-width: 480px) {
        font-size: 0.4rem;
        line-height: 8.5px;
      }
    }
  }
  .content2 {
    color: #000066;
    position: absolute;
    top: 500px;
    right: 31px;
    width: 203px;
    text-align: left;
    line-height: 12px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 30px;
      right: 20px;
      width: 144px;
      font-weight: 900;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 45px;
      left: 26px;
      width: 174px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 25px;
      left: 172px;
      width: 136px;
      font-weight: 900;
    }
    .title {

      @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
        font-size: 25px;
        line-height: 25px; 
      }

      @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
        font-size: 0.69rem;
        line-height: 10px;
      }

      @media (min-width: $breakpoint-sm) and (max-width: 480px) {
        font-size: 1.5rem;
        line-height: 25px;
      }
    }
  }

  /*.content2 {
    position: absolute;
    top: 382px;
    left: 31px;
    width: 203px;

    @media (min-width: $breakpoint-lg) and (max-width: ($breakpoint-xl - 1px)) {
      top: 37px;
      left: 23px;
      width: 144px;
    }

    @media (min-width: 481px) and (max-width: ($breakpoint-lg - 1px)) {
      top: 325px;
      left: 26px;
      width: 174px;
    }

    @media (min-width: $breakpoint-sm) and (max-width: 480px) {
      top: 258px;
      left: 22px;
      width: 136px;
    }

    img {
      width: 100%;
      height: auto;
      cursor: pointer;
    }
  }*/
}
</style>

<template>
  <div>
    <div style="display: none">
      <div id="p10t">{{ $t("p10.title") }}</div>
      <div id="p10p1">{{ $t("p10.paragraph1") }}</div>
      <div id="p10p2">{{ $t("p10.paragraph2") }}</div>
    </div>

    <div class="content2">
      <div id="p10t_" class="title"></div>
    </div>
    <div class="content1">
      <div id="p10p1_" class="text"></div>
      <div id="p10p2_" class="text"></div>
    </div>

    <!-- <div class="content2">
      <img
        src="/img/pages/10_1.jpg"
        v-on:click="showImage('/img/pages/10_1.jpg')"
      />
      <img
        src="/img/pages/10_2.jpg"
        v-on:click="showImage('/img/pages/10_2.jpg')"
      />
    </div> -->
  </div>
</template>

<script>
export default {
  name: "Page10",
  mounted() {
    let ref = this;
    ref.processText("p10t");
    ref.processText("p10p1");
    ref.processText("p10p2");
    window
      .jQuery("body")
      .on("DOMSubtreeModified", "#p10t, #p10p1, #p10p2", function () {
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
    showImage(url) {
      this.$parent.showImage(url);
    }
  },
};
</script>
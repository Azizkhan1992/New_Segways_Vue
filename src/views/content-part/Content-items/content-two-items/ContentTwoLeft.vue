<template>
  <div class="two-left-container">
    <div class="two-left-title">
      <a href="#">In stock</a>
      <h1>SEGWAY Ninebot Kickscooter MAX</h1>
    </div>
    <div class="two-mobile-extends">
      <div class="two-mobile-title">
        <h1>Segway Protective Gear Set <i>as a gift</i></h1>
        <span
          >The cost of a protection kit when buying a scooter is $0 instead of
          $29.99</span
        >
      </div>
      <img src="@/assets/Content/ContentTwo/TwoMobile/image.svg" alt="" />
    </div>
    <div class="two-extends-input">
      <div class="extends-inputs">
        <h5>Add an extended warranty from <i>Extend</i></h5>
        <div class="input-items">
          <button>1 Year - $139</button>
          <button>2 Year - $209</button>
          <button>3 Year - $279</button>
          <button class="two-left-mobile">
            <p>1 Year</p>
            <i> $139</i>
          </button>
          <button class="two-left-mobile">
            <p>2 Year</p>
            <i> $209</i>
          </button>
          <button class="two-left-mobile">
            <p>3 Year</p>
            <i> $279</i>
          </button>
        </div>
      </div>
      <div class="extends-price">
        <div class="price-title">
          <h6>$1049.99</h6>
          <h1>$949.99</h1>
        </div>
        <a href="#">Segway Protective Gear Set as a gift</a>
        <img src="@/assets/Content/ContentTwo/image1.svg" alt="" />
      </div>
      <div class="extends-btn">
        <button>BUY IT Now</button>
        <button>ADD TO CART</button>
      </div>
    </div>
    <two-left-items />
  </div>
</template>
<script>
import TwoLeftItems from "./TwoLeftItems.vue";
export default {
  name: "two-left",
  components: { TwoLeftItems },
};
</script>

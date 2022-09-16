<template>
  <div class="price-title-two">
    <div class="price-title-content">
      <div class="price-title-header">
        <button class="price-header-btn">В наличии</button>
        <h1>SEGWAY Ninebot Kickscooter MAX</h1>
      </div>
      <div class="price-title-items">
        <div class="mobile-price-items">
          <div class="mobile-price-title">
            <h1>Segway Protective Gear Set as a gift</h1>
            <span
              >The cost of a protection kit when buying a scooter is $0 instead
              of $29.99</span
            >
          </div>
          <img src="@/assets/Content/ContentFourten/Price/image2.svg" alt="" />
        </div>
        <price-title-extend />
        <price-title-items />
      </div>
    </div>
  </div>
</template>
<script>
import PriceTitleExtend from "./PriceTitleExtend.vue";
import PriceTitleItems from "./PriceTitleItems.vue";
export default {
  name: "price-title",
  components: { PriceTitleExtend, PriceTitleItems },
};
</script>

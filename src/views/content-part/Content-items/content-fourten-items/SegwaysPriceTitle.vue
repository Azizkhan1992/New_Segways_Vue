<template>
  <div class="price-title-two">
    <div class="price-title-content">
      <div class="price-title-header">
        <button class="price-header-btn">В наличии</button>
        <h1>SEGWAY Ninebot Kickscooter MAX</h1>
      </div>
      <div class="price-title-items">
        <price-title-extend/>
        <price-title-items/>
      </div>
    </div>
  </div>
</template>
<script>
    import PriceTitleExtend from './PriceTitleExtend.vue';
    import PriceTitleItems from './PriceTitleItems.vue'
export default {
  name: "price-title",
  components: {PriceTitleExtend, PriceTitleItems}
};
</script>

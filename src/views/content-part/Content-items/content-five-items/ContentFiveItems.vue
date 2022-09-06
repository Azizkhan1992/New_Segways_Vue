<template>
  <div class="five-items-container">
    <div class="items">
      <item-one />
    </div>
    <div class="items">
      <item-two />
    </div>
    <div class="items">
      <item-three />
    </div>
    <div class="items">
      <item-four />
    </div>
    <div class="items">
      <item-five />
    </div>
    <div class="items">
      <item-six />
    </div>
    <div class="items">
      <item-seven />
    </div>
    <div class="items">
      <item-eight />
    </div>
    <div class="items">
      <item-nine />
    </div>
  </div>
</template>
<script>
import ItemOne from "./five-items/ItemOne.vue";
import ItemTwo from "./five-items/ItemTwo.vue";
import ItemThree from "./five-items/ItemThree.vue";
import ItemFour from "./five-items/ItemFour.vue";
import ItemFive from "./five-items/ItemFive.vue";
import ItemSix from "./five-items/ItemSix.vue";
import ItemSeven from "./five-items/ItemSeven.vue";
import ItemEight from "./five-items/ItemEight.vue";
import ItemNine from "./five-items/ItemNine.vue";
export default {
  name: "five-items",
  components: {
    ItemOne,
    ItemTwo,
    ItemThree,
    ItemFour,
    ItemFive,
    ItemSix,
    ItemSeven,
    ItemEight,
    ItemNine,
  },
};
</script>

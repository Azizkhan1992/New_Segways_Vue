<template>
  <div class="content-seven-container">
    <seven-top-item />
    <seven-bottom-item />
  </div>
</template>
<script>
import SevenTopItem from "./Content-items/content-seven-items/SevenTopItem.vue";
import SevenBottomItem from "./Content-items/content-seven-items/SevenBottomItem.vue";
export default {
  name: "contnet-seven",
  components: { SevenTopItem, SevenBottomItem },
};
</script>

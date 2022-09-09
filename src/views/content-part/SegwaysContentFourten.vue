<template>
    <div class="content-fourten-container">
        <smartphone-control/>
        <segways-price-title/>
        <segways-models/>
    </div>
</template>
<script>
    import SmartphoneControl from './Content-items/content-fourten-items/SmartphoneControl.vue';
    import SegwaysPriceTitle from './Content-items/content-fourten-items/SegwaysPriceTitle.vue';
    import SegwaysModels from './Content-items/content-fourten-items/SegwaysModels.vue';
export default {
    name: 'content-fourten',
    components: {SmartphoneControl, SegwaysPriceTitle, SegwaysModels}
}
</script>
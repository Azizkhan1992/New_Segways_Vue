<template>
    <div class="content-two-container">
        <div class="content-two-content">
            <content-two-left />
            <content-two-slider />
        </div>
    </div>
</template>
<script>
import ContentTwoLeft from './Content-items/content-two-items/ContentTwoLeft.vue';
import ContentTwoSlider from './Content-items/content-two-items/ContentTwoSlider.vue';
export default {
    name: 'content-two',
    components: { ContentTwoLeft, ContentTwoSlider }
}
</script>
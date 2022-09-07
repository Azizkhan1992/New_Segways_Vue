<template>
    <div class="content-eight-container">
        <content-eight-top/>
        <content-eight-bottom/>
    </div>
</template>
<script>
    import ContentEightTop from './Content-items/content-eight-items/ContentEightTop.vue';
    import ContentEightBottom from './Content-items/content-eight-items/ContentEightBottom.vue';
export default {
    name: 'content-eight',
    components: {ContentEightTop, ContentEightBottom}
}
</script>
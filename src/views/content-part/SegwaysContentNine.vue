<template>
    <div class="content-nine-container">
        <content-nine-top/>
        <content-nine-bottom/>
    </div>
</template>
<script>
    import ContentNineTop from './Content-items/content-nine-items/ContentNineTop.vue';
    import ContentNineBottom from './Content-items/content-nine-items/ContentNineBottom.vue';
export default {
    name: 'content-nine',
    components: {ContentNineTop, ContentNineBottom}
}
</script>
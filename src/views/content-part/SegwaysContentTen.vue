<template>
    <div class="content-ten-container">
        <content-ten-top/>
        <content-ten-bottom/>
    </div>
</template>
<script>
    import ContentTenTop from './Content-items/content-ten-items/ContentTenTop.vue';
    import ContentTenBottom from './Content-items/content-ten-items/ContentTenBottom.vue';
export default {
    name: 'content-ten',
    components: {ContentTenTop, ContentTenBottom}
}
</script>
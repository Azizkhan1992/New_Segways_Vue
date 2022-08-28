<template>
    <div class="content-one-container">
        <content-one-top/>
        <content-one-bottom/>
        <div class="one-footer">
            <a href="#">Free 1 day shipping within California.</a>
        </div>
    </div>
</template>
<script>
    import ContentOneTop from './Content-items/content-one-items/ContentOneTop.vue';
    import ContentOneBottom from './Content-items/content-one-items/ContentOneBottom.vue';
    export default{
        name: 'content-one',
        components: {ContentOneTop, ContentOneBottom}
    }
</script>
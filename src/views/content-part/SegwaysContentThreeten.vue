<template>
    <div class="content-threeten-container">
        <content-threeten-top/>
        <content-threeten-bottom/>
    </div>
</template>
<script>
    import ContentThreetenTop from './Content-items/content-threeten-items/ContentThreetenTop.vue';
    import ContentThreetenBottom from './Content-items/content-threeten-items/ContentThreetenBottom.vue';
export default {
    name: 'content-threeten',
    components: {ContentThreetenTop, ContentThreetenBottom}
}
</script>
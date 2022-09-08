<template>
    <div class="content-elewen-container">
        <content-elewen-top/>
        <content-elewen-bottom/>
    </div>
</template>
<script>
    import ContentElewenTop from './Content-items/content-elewen-items/ContentElewenTop.vue';
    import ContentElewenBottom from './Content-items/content-elewen-items/ContentElewenBottom.vue';
export default {
    name: 'content-elewen',
    components: {ContentElewenTop, ContentElewenBottom}
}
</script>
<template>
    <div class="content-four-container">
        <div class="content-four-content">
            <content-four-left/>
            <content-four-right/>
        </div>
    </div>
</template>
<script>
    import ContentFourLeft from './Content-items/content-four-items/ContentFourLeft.vue';
    import ContentFourRight from './Content-items/content-four-items/ContentFourRight.vue';
export default {
    name: 'content-four',
    components: {ContentFourLeft, ContentFourRight}
}
</script>
<template>
    <div class="content-five-container">
        <div class="content-five-content">
            <h1>Accessories</h1>
            <content-five-items/>
            <button class="five-footer-btn">SEE MORE</button>
        </div>
    </div>
</template>
<script>
    import ContentFiveItems from './Content-items/content-five-items/ContentFiveItems.vue';
export default {
    name: 'content-five',
    components: {ContentFiveItems}
}
</script>
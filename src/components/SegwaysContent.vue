<template>
    <div class="segways-content-container">
        <segways-content-one/>
        <segways-content-two/>
    </div>
</template>
<script>
    import SegwaysContentOne from '@/views/content-part/SegwaysContentOne.vue';
    import SegwaysContentTwo from '@/views/content-part/SegwaysContentTwo.vue';
    export default{
        name: 'segways-content',
        components:{
            SegwaysContentOne,
            SegwaysContentTwo
        }
    }
</script>

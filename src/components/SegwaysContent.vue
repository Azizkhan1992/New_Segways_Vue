<template>
    <div class="segways-content-container">
        <segways-content-one/>
        <segways-content-two/>
        <segways-content-three/>
    </div>
</template>
<script>
    import SegwaysContentOne from '@/views/content-part/SegwaysContentOne.vue';
    import SegwaysContentTwo from '@/views/content-part/SegwaysContentTwo.vue';
    import SegwaysContentThree from '@/views/content-part/SegwaysContentThree.vue';
    export default{
        name: 'segways-content',
        components:{
            SegwaysContentOne,
            SegwaysContentTwo,
            SegwaysContentThree
        }
    }
</script>

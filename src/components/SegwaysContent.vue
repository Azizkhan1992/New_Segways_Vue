<template>
    <div class="segways-content-container">
        <segways-content-one/>
        <segways-content-two/>
        <segways-content-three/>
        <segways-content-four/>
        <segways-content-five/>
        <segways-content-six/>
    </div>
</template>
<script>
    import SegwaysContentOne from '@/views/content-part/SegwaysContentOne.vue';
    import SegwaysContentTwo from '@/views/content-part/SegwaysContentTwo.vue';
    import SegwaysContentThree from '@/views/content-part/SegwaysContentThree.vue';
    import SegwaysContentFour from '@/views/content-part/SegwaysContentFour.vue';
    import SegwaysContentFive from '@/views/content-part/SegwaysContentFive.vue';
    import SegwaysContentSix from '@/views/content-part/SegwaysContentSix.vue';
    export default{
        name: 'segways-content',
        components:{
            SegwaysContentOne,
            SegwaysContentTwo,
            SegwaysContentThree,
            SegwaysContentFour,
            SegwaysContentFive,
            SegwaysContentSix
        }
    }
</script>

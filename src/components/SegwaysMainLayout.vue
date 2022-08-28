<template>
    <div class="segways-main-container">
            <header-layout/>
            <segways-content/>
    </div>
</template>
<script>
    import HeaderLayout from './HeaderLayout.vue';
    import SegwaysContent from './SegwaysContent.vue';
    export default{
        name: 'segways-main-layout',
        components:{HeaderLayout, SegwaysContent}
    }
</script>
<template>
    <div class="segways-main-container">
            <header-layout/>
            <segways-content/>
            <segways-footer/>
    </div>
</template>
<script>
    import HeaderLayout from './HeaderLayout.vue';
    import SegwaysContent from './SegwaysContent.vue';
    import SegwaysFooter from './SegwaysFooter.vue';
    export default{
        name: 'segways-main-layout',
        components:{HeaderLayout, SegwaysContent, SegwaysFooter}
    }
</script>
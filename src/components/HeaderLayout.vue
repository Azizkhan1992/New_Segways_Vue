<template>
    <div class="header-container">
        <header-sidebar/>
        <header-title/>
    </div>
</template>
<script>
    import HeaderSidebar from '@/views/header-part/HeaderSidebar.vue';  
    import HeaderTitle from '@/views/header-part/HeaderTitle.vue';
    export default{
        name: 'header-layout',
        components:{HeaderSidebar, HeaderTitle}
    }
</script>
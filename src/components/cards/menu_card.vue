<template>
    <router-link :to="menu.url">
        <div class="menu-card">
            <div class="img-menu">
                <img :src='menu.icon' :alt="menu.infos" width="30px">
            </div>
            <div class="menu-info title">
                {{ menu.name }}
            </div>
            <div class="menu-info">
                {{ menu.infos }}
            </div>
        </div>
    </router-link>
</template>

<script>
export default {
    props:{
        menu:{
            type:Object,
            required: true
        },
    }
};
</script>

<style scoped>
.menu-card{
    display: inline-flex;
    align-items: center;
    text-align: center;
    flex-direction: column;
    width: 140px;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    padding: 10px 5px 10px 5px;
    margin: 10px;
    background-color: #fff;
    border-radius: 5px;
    white-space: nowrap;
    position: relative;
    overflow: hidden;
    color: #000;
}
.menuname{
    max-width: 130px;
    overflow: hidden;
}
.menu-card:hover{
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}
.img-menu{
    width: 90px;
    height: 90px;
    border-radius: 50%;
    background-color: #ddd;
    overflow: hidden;
}
.img-menu img{
    width: 100%;
    margin:auto;
}
.title{
    font-weight: bold;
}
</style>

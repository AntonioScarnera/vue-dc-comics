<template>
    <div class="card">
        <img :src="thumb">
        <span>{{ series }}</span>
    </div>
</template>

<script>
export default {
    name: 'CardComponent',
    props:['thumb', 'series']
}
</script>

<style lang="scss" scoped>
@import '../style/variables';
@import '../style/general';
    .card{

        width: calc(100% / 6);
        padding: 10px;
        cursor: pointer;

        img{
            width: 100%;
            height: 150px;
            object-position:top;
            object-fit: cover;
            &:hover{
                transform: scale(1.05);
            }
        }
        span{
            color: white;
            font-size: $font-medium;
        }
        

    }
</style>
<template>
    <div class="block" v-if="showBlock">
        click me
    </div>
</template>

<script>
export default{
    props: ['delay'],
    data(){
        return {
            showBlock: false
        }
    },
    mounted(){
        setTimeout(() => {
            this.showBlock = true;
        }, this.delay)

    },
    updated(){
        
    }
}

</script>

<style>
.block{
    width:400px;
    border-radius: 20px;
    background-color: coral;
    color: white;
    padding: 100px 0;
    margin: 40px auto;
    text-align: center;
}
</style>
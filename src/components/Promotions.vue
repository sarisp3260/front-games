<template>
    <div class="back" @click.self="closeWindow">
        <div class="window">
            <button class="closeBTN" @click="closeWindow"><i class="fas fa-times"></i></button>
            <slot><img class="cupon" src="@/assets/Cupon.png"></slot>
            <button class="rediretC">Adquierelo</button>
        </div>
    </div>
</template>

<script>
export default {
    methods:{
        closeWindow(){
            this.$emit("close")
        }
    }
}
</script>

<style>
    .window
    {width: 400px;padding: 5px;margin: 100px auto;background: var(--secundary-color);border-radius: 10px;}
    .back
    {top: 0;position: fixed;background: rgba(0, 0, 0, 0.5);width: 100%;    height: 100%;}
    .cupon
    {width: 400px;height: auto;}
    .closeBTN
    {border: none;background: var(--secundary-color);padding: 5px;padding-left: 90%;}
    .rediretC
    {margin: 0 0 20px; background: var(--palette-pink); color: var(--secundary-color); border:none; padding: 10px; border-radius: 10px; font-weight: 700; font-size: 20px;}

    
</style>
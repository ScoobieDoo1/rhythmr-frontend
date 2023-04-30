<template>
    <div class="inst-cont">
        <div class="img-cont">
            <img :src="instrument.imageUrl" :alt="instrument.name" />
        </div>
        <div class="inst-desc">
            <p v-text="instrument.name"></p>
            <p v-text="instrument.category"></p>
            <p v-text="instrument.model"></p>
            <p v-text="instrument.brand"></p>
            <p><b>{{instrument.price}}</b></p>
           
        </div>
    </div>
</template>

<script>
export default{
    name: 'InstrumentComp',
    props: ['instrument']

}
</script>

<style>

.inst-cont{
    display: flex;
    flex-direction: row;
    margin: 10px 0;
    max-width: 450px;
    max-height: 400px;
}
.img-cont{
    width: 250px;
    height: 400px;
}
.img-cont img{
    width: 100%;
    height: 100%;
    object-fit: cover;

}
</style>
<template>
    <br/><br/><br/>
    <div id="inst-outer-cont" >
        <div v-for="instrument in instruments" :key="instrument.id">
            <InstrumentComp :instrument="instrument"/>
        </div>
    </div>
</template>

<script>
import InstrumentComp from './InstrumentComp.vue';
// import data from './../../data.json';

export default{
    name: 'InstrumentCont',
    components:{
        InstrumentComp,
    },
    data(){
        return{
            instruments: []
        }
    },
    methods:{
        async callApi(){
            const res = await fetch('https://rhythmr-backend.onrender.com/api');
            const data = res.json();
            console.log(data);
            return data;
        }
    },
    async created(){
        this.instruments = await this.callApi();
    }
}
</script>


<style>

#inst-outer-cont{
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: space-evenly;
    align-items: center;
    color: black;
}


#inst-outer-cont{
    background-color:#fff;
}


</style>
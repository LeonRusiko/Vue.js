<script>
export default{
    data(){
        return{
            counter:0,
            arr:[]
        }
    },
    methods:{
        generator(){
            this.arr.push(Math.random()*100)
        }
    }
}
</script>

<template>
    <div>
        <button @click="generator()">Gen</button>
        <ul>
            <li v-for="none in arr" :key="none">{{none}}</li>
        </ul>
    </div>
</template>

<style scoped>

</style>

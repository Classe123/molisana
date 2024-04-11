<template>
    <div class="col-12 col-md-4">
                    <h4 @click="cambiaTitolo">{{ titleUppercase }}</h4>
                    <ul>
                            <li v-for="(item, index) in menuItem.links" :key="index">
                                <a :href="item.url">{{ item.text }}</a>
                            </li>
                    </ul>
                </div>
</template>

<script>
    export default {
        name: 'MenuComponent',
        props:{
            menuItem: Object
        },
        
        data(){
            return{
                variabile1: 'Clelia'
            }
        },
        methods:{
           cambiaTitolo(){
            this.$emit('pippo',this.variabile1);
           }
        },
        computed:{
            titleUppercase(){
                return this.menuItem.title.toUpperCase();
            }
        }

    }
</script>

<style lang="scss" scoped>

</style>
<template>
    <footer>
        <div class="container">
            <div class="row">
                <div class="col-12 col-md-4">
                    <img src="../assets/img/la-molisana-logo.png" alt="Logo">
                </div>
                <MenuComponent v-for="(item, index) in menu" :key="index" :menuItem="item"  @pippo="changeTitle"/>
                <!-- mi devi passare un oggetto così strutturato 
                    {
                        title: String,
                        links:[
                                {
                                    text:string, 
                                    url:string
                                },
                                ....
                            ]
                    } 
                    e mette a disposizione un evento @pippo e ritorna un nuovo titolo
                -->
            </div>
        </div>
    </footer>
</template>

<script>
import {footerMenu} from '../data/store.js';
import MenuComponent from './MenuComponent.vue';
export default {
    name: 'FooterComponent',
    components: {
        MenuComponent
    },
    data() {
        return {
            menu: footerMenu
        }
    },
    methods:{
        changeTitle(title){
            this.menu[0].title = title;
        }
    }
}
</script>

<style lang="scss" >
@use '../assets/styles/partials/variables' as *;
footer {
    background-image: url('../assets/img/footer-montagne-bottom.jpg');
    background-position: bottom;
    background-repeat: no-repeat;
    padding: 20px 0;

    h4 {
            // text-transform: uppercase;
            font-size: 1.25em;
            font-weight: 600;
            margin-bottom: 1rem;
            color: $bluetext;
        }
    ul {
        list-style: none;
        margin:0;
        padding:0;
        li a {
                display: inline-block;
                margin-bottom: 0.25rem;
                text-decoration: none;
                font-size: 0.875em;


                &:hover {
                    color: $bluetext;
                }
            }
        }
    }

</style>
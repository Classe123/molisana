<template>
    <footer>
        <div class="container">
            <div class="row">
                <div class="col-12 col-md-4">
                    <img src="../assets/img/la-molisana-logo.png" alt="Logo">
                </div>
                <MenuComponent v-for="(item, index) in menu" :key="index" :title="item.title" :items="item.links" />
                
            </div>
        </div>
    </footer>
</template>

<script>
import MenuComponent from './MenuComponent.vue';
export default {
    name: 'FooterComponent',
    components: {
        MenuComponent
    },
    data() {
        return {
            menu: [
                {
                    title: 'Pastificio',
                    links: [
                        {
                            text: "Il Pastificio",
                            url: "#",
                        },
                        {
                            text: "Grano",
                            url: "#",
                        },
                        {
                            text: "Filiera",
                            url: "#",
                        },
                        {
                            text: "100 anni di pasta",
                            url: "#",
                        },
                        {
                            text: "Sartoria della pasta",
                            url: "#",
                        }

                    ]
                },
                {
                    title: 'Prodotti',
                    links: [
                        {
                            text: "Le classiche",
                            url: "#",
                        },
                        {
                            text: "Le Integrali",
                            url: "#",
                        },
                        {
                            text: "Le Speciali",
                            url: "#",
                        },
                        {
                            text: "Le Biologiche",
                            url: "#",
                        },
                        {
                            text: "SLe Gluten-free",
                            url: "#",
                        }
                    ]
                },

            ]

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
            text-transform: uppercase;
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
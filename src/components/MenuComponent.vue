<template>
    <div class="col-12 col-md-4">
                    <h5>{{ title }}</h5>
                    <ul>
                            <li v-for="(item, index) in items" :key="index">
                                <a :href="item.url">{{ item.text }}</a>
                            </li>
                    </ul>
                </div>
</template>

<script>
    export default {
        name: 'MenuComponent',
        props:['title', 'items']
    }
</script>

<style lang="scss" scoped>

</style>
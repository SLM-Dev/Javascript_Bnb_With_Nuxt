<template>
    <div>
    <div v-for="home in homes" :key="home.objectID" style="float:left;margin:10px">
        <home-card :home="home"/>
    </div>
    </div>
</template>

<script>
import homes from '~/data/homes'

// Part of Nuxt Config
// import HomeCard from '~/components/HomeCard'

export default{

    // Moved to Nuxt.config
    // components: {
    //     HomeCard,
    // },
    data(){
        return {
            homes: homes.slice(0,3)
        }
    }
}
</script>
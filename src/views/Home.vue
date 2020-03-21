<template>
    <div class="home">
        <HomeComponent :show.sync="isclock"></HomeComponent>
        <van-button type="info" size="mini" @click="open" style="marginTop:20px">打开</van-button>
    </div>
</template>

<script>
// @ is an alias to /src
import HomeComponent from '@/components/homeComponent.vue'

export default {
    name: 'Home',
    components: {
        HomeComponent
    },
    data() {
        return {
            isclock: true
        }
    },
    methods: {
        open() {
            this.isclock = !this.isclock
        }
    }
}
</script>

<template>
    <section>
        <div class="list-disc">
            <SingleCardDisc  v-for="(album, index) in albumList" :key="index" :albumDetails="album" />
        </div>
        
    </section>
</template>

<script>
import SingleCardDisc from './SingleCardDisc.vue';
import axios from "axios";

export default {
    name: "SectionListDisc",
    components: { 
        SingleCardDisc
    },
    data() {
        return {
            url:"https://flynn.boolean.careers/exercises/api/array/music",
            albumList: [],
        }
    },
    created() {
        this.getAlbums();
    },
    methods: {
        getAlbums() {
            axios.get(this.url).then((albumResult) => {
                this.albumList = albumResult.data.response;

                console.log(this.albumList);
            })

            .catch((err) => {
                 console.log("error", err);
            });
        }
    }
}

</script>

<style lang="scss" scoped>
@import '../assets/style/variables.scss';

section {

    .list-disc {
        width: 80%;
        padding: 30px 0;
        margin: 0 auto;
        display: flex;
        flex-wrap: wrap;
        gap: 20px;
    }
}
</style>
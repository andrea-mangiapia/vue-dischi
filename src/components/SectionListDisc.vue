<template>
    <section>
        <!-- Filter Menu Genre -->
        <div class="filter-select">
            <SelectComponent />
        </div>

        <!-- Album List -->
        <div class="list-disc">
            <SingleCardDisc  v-for="(album, index) in albumList" :key="index" :albumDetails="album" />
        </div>
        
    </section>
</template>

<script>
import SingleCardDisc from './SingleCardDisc.vue';
import axios from "axios";
import SelectComponent from './SelectComponent.vue';

export default {
    name: "SectionListDisc",
    components: {
    SingleCardDisc,
    SelectComponent
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
    width: 80%;
    margin: 0 auto;
    padding: 30px 0;

    .filter-select {
        padding-bottom: 20px;
    }

    .list-disc {
        display: flex;
        flex-wrap: wrap;
        gap: 20px;
    }
}
</style>
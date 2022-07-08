<template>
    <section>
        <div class="list-disc">
            <SingleCardDisc />
            <SingleCardDisc />
            <SingleCardDisc />
            <SingleCardDisc />
            <SingleCardDisc />
            <SingleCardDisc />
            <SingleCardDisc />
            <SingleCardDisc />
            <SingleCardDisc />
            <SingleCardDisc />

        </div>

        
    </section>
</template>

<script>
import SingleCardDisc from './SingleCardDisc.vue'

export default {
    name: 'SectionListDisc',
    components: {
        SingleCardDisc,
    },
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
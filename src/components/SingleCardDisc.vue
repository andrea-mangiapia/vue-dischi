<template>
    <div class="single-card">
        <div class="img-card">
            <img src="https://picsum.photos/300/300" alt="Titolo Img">
        </div>
        <div class="title-card">
            <h2>
                Titolo
            </h2>
            <div class="author-card">
                Autore
            </div>
            <div class="year-card">
                Anno
            </div>

        </div>
    </div>
</template>

<script>
export default {
    name: 'SingleCardDisc'
}
</script>

<style lang="scss" scoped>
@import '../assets/style/variables.scss';
.single-card {
    width: calc((100% / 5) - 20px);
    background-color: $brand_primary_color;
    padding: 10px;
    text-align: center;

    h2 {
        font-size: 16px;
        text-transform: uppercase;
        color: $primary_text;
        padding: 10px 0;
    }

    &, .autor-card, .year-card {
        font-size: 12px;
        color: $secondary_text;
    }

}
</style>
<template>
    <div class="content-select">
        <label for="genre">
            Seleziona un genere:
        </label>

        <select name="genre" id="genre">
            <option value="all">
                Tutti
            </option>
            <option value="Rock">
                Rock
            </option>
            <option value="Pop">
                Pop
            </option>
            <option value="Jazz">
                Jazz
            </option>
            <option value="Metal">
                Metal
            </option>
        </select>

    </div>
</template>

<script>
export default {
    name: 'SelectComponent',
}
</script>

<style lang="scss" scoped>
.content-select {
    color: white;

    label {
        padding-right: 5px;
    }
}
</style>
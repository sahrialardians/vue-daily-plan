<template>
    <div class="form-check">
        <input class="form-check-input" type="checkbox" value="" id="defaultCheck1">
        <label class="form-check-label item" v-bind:class="{'item-done':taskMe.status}" for="defaultCheck1">
        {{ taskMe.nameTask }}
        </label>
    </div>
</template>

<script>
export default {
    name: "ItemTask",
    props: ["taskMe"]
}
</script>

<style scoped>

</style>
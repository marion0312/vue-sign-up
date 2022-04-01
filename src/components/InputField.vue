<template>
    <div class="form-control">
        <input placeholder=" " :type="type">
        <label>{{ placeholder }}</label>
    </div>
</template>

<script>
export default {
    name: "InputField",
    props: {
        type: String,
        placeholder: String,
    },
}
</script>

<style scoped>

</style>
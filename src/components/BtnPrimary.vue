<template>
    <button class="btn-primary">See all</button>
</template>

<script>
export default {
    name: "BtnPrimary",
    data() {
        return {}
    }
}
</script>

<style scoped>
    .btn-primary {
        background-color: transparent;
        font-family: var(--font-family-Josefin-Sans);
        border: 2px solid var(--Black);
        text-transform: uppercase;
        padding: 10px 40px;
        font-size: 1.1rem;
        font-weight: 400;
        letter-spacing: 2px;
        transition: .4s;
    }
    .btn-primary:where(:hover, :focus-visible) {
        background-color: var(--Black);
        color: var(--White);
        transition: .4s;
    }
</style>
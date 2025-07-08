<script>
export default {

}
</script>

<template>
    <footer>
        <a href="http://" target="_blank" rel="noopener noreferrer">
            <p>Nabila Abubakar (c) 2025 </p>
        </a>
    </footer>
</template>

<style lang="scss">
footer {
    background: var(--purple-color);

    height: 10vh;
    bottom: 0;

    border-top-left-radius: 30px;
    border-top-right-radius: 30px;

    font-size: 2rem;
    text-align: center;

    a p {
        color: #fafafa;

        &:hover {
            color: var(--purple-color-2);
        }
    }
}
</style>
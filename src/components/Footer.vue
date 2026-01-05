<script>
export default {

}
</script>

<template>
    <footer>
        <a href="https://beela303.vercel.app/" target="_blank" rel="noopener noreferrer">
            <p>Nabila Abubakar (c) 2026 </p>
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
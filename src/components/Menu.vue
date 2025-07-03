<script>
</script>

<template>
    <div id="navbar">
        <ul>
            <li><a href="#home"><span class="material-icons">home</span></a></li>
            <li><a href="#about"><span class="material-icons">person</span></a></li>
            <li><a href="#tech-stack"><span class="material-icons">layers</span></a></li>
            <li><a href="#portfolio-title"><span class="material-icons">work</span></a></li>
            <li><a href="#contact"><span class="material-icons">alternate_email</span></a></li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
#navbar {
    width: 50%;

    margin-left: 25%;
    bottom: 50px;

    border-radius: 30px;

    overflow: hidden;
    position: fixed;

    background: var(--main-gradient);

    ul {
        display: flex;
        justify-content: space-between;

        li {
            a {
                color: var(--text-color) !important;

                padding: 14px 16px;

                font-size: 3rem;

                &:hover {
                    background: var(--purple-color) !important;
                }
            }
        }
    }
}

@media screen and (max-width: 600px) {
    #navbar {
        width: 95%;

        margin-left: 0;
        bottom: 30px;
    }
}
</style>
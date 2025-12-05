<script>
import VTooltip from 'v-tooltip';

export default {
    directives: {
        tooltip: VTooltip,
    }
}
</script>

<template>
    <div id="navbar">
        <ul>
            <li v-tooltip="Home"><a href="#home" title="Home"><span class="material-icons">home</span></a></li>
            <li v-tooltip="About"><a href="#about" title="About Me"><span class="material-icons">person</span></a></li>
            <li v-tooltip="Skills"><a href="#tech-stack" title="Skills"><span class="material-icons">layers</span></a>
            </li>
            <li v-tooltip="Project"><a href="#project-title" title="Project"><span
                        class="material-icons">work</span></a></li>
            <li v-tooltip="Contact"><a href="#contact" title="Contact"><span
                        class="material-icons">alternate_email</span></a></li>
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

@media screen and (max-width: 400px) {
    #navbar {
        width: 100%;
        margin-top: 77vh;
    }
}
</style>
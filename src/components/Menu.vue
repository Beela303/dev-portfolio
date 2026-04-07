<script setup>
import { ref } from 'vue';

const isOpen = ref(false);

const toggleMenu = () => {
    isOpen.value = !isOpen.value
}

</script>

<template>
    <div id="navbar">
        <button @click="toggleMenu" id="icon">
            <i :class="isOpen? 'fas fa-xmark' : 'fas fa-bars'"></i>
        </button>
        
        <div v-if="isOpen" id="menu">
            <ul>
                <li><a href="#me"><span class="material-icons">person</span>Intro</a></li>
                <li><a href="#tech-stack"><span class="material-icons">layers</span>Tech Stack</a></li>
                <li><a href="#experiences"><span class="material-icons">business_center</span>Experience</a></li>
                <li><a href="#project-start"><span class="material-icons">work</span>Projects</a></li>
                <li><a href="#contact-me"><span class="material-icons">email</span>Contact Me</a></li>
            </ul>
        </div>
    </div>
</template>

<style lang="scss" scoped>
#navbar {
    text-align: center;
    
    #icon {
        height: 65px;
        width: 65px;

        top: 85%;
        left: 30px;

        border-radius: 30px;
        position: fixed;

        background: var(--main-gradient);
        i {
            color: var(--text-color);
            font-size: 35px;
        }
    }
    
    #menu {
        background: var(--main-gradient);
        //background-color: var(--dark);

        width: 30vw;
        height: 45vh;

        //bottom: 4%;
        //left: 95px;
        bottom: 15%;
        left: 30px;

        border-radius: 30px;
        position: fixed;
        
        ul {

            li {
                margin-bottom: 4vh;

                font-size: 1.5rem;

                a {
                    color: var(--text-color);

                    &:hover {
                        //color: var(--background-color);
                        color: var(--pastel-color-2);
                    }
                }
            }
        }
    }
}

@media screen and (max-width: 600px) {
    #navbar {
        #menu {
            width: 50vw;
        }
    }
}
</style>
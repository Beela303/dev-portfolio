<template>
    <footer>
        <div id="socials">
            <ul>
                <li>
                    <a href="https://instagram.com/beela303" target="_blank" rel="noopener noreferrer">
                        <i class="fa-brands fa-instagram"></i>
                    </a>
                </li>
                
                <li>
                    <a href="https://x.com/beela303" target="_blank" rel="noopener noreferrer">
                        <i class="fa-brands fa-twitter"></i>
                        <!--<p>X/Twitter</p>-->
                    </a>
                </li>

                <li>
                    <a href="https://beela303.blogspot.com" target="_blank" rel="noopener noreferrer">
                        <i class="fas fa-blog"></i>
                        <!--<p>Blog</p>-->
                    </a>
                </li>

                <li>
                    <a href="https://beela303.blogspot.com" target="_blank" rel="noopener noreferrer">
                        <i class="fas fa-envelope"></i>
                        <!--<p>Email</p>-->
                    </a>
                </li>
                

                <li>
                    <a href="https://beela303.hashnode.dev" target="_blank" rel="noopener noreferrer">
                        <i class="fa-brands fa-hashnode"></i>
                        <!--<p>Hashnode (Dev Blog)</p>-->
                    </a>
                </li>

                <li>
                    <a href="https://youtube.com/@beela303" target="_blank" rel="noopener noreferrer">
                        <i class="fa-brands fa-youtube"></i>
                        <!--<p>YouTube</p>-->
                    </a>
                </li>

                <li>
                    <a href="https://linkedin.com/in/nabilaabubakar" target="_blank" rel="noopener noreferrer">
                        <i class="fa-brands fa-linkedin-in"></i>
                        <!--<p>Linkedin</p>-->
                    </a>
                </li>
            </ul>

        </div>

        <a href="https://beela303.vercel.app/" target="_blank" rel="noopener noreferer" id="footer-name">
            <p>Nabila Abubakar (c) 2026 </p>
        </a>
    </footer>
</template>

<style lang="scss">
footer {
    background: var(--purple-color);

    a {
        color: var(--text-color);
    }

    i {
        font-size: 1.5rem;
    }

    #socials {
        ul {
            display: flex;

            justify-content: center;

            li {
                &:first-child {
                    margin-left: 0px;
                }

                //background-color: var(--pastel-color-1);
                margin: 10px;
                padding: 5px;

                border: 1px solid var(--text-color);
            }
        }
    }

    #footer-name {
        text-align: center;
    }
}

@media screen and (max-width: 500px) {
    footer {
    i {
        font-size: 1.3rem;
    }

    #socials {
        ul {
            display: block;

            li {
                margin: 3px;
                padding: 3px;
            }
        }
    }

}
}
</style>
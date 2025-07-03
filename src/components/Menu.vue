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
    background: #333;

    width: 50%;
    height: 10vh;

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

            /*
            &:before {
                content: '';

                background: linear-gradient(60deg, #f79533, #f37055, #ef4e7b, #a166ab, #5073b8, #1098ad, #07b39b, #6fba82);

                width: 80%;
                height: 70%;
                top: 15%;
                left: 10%;

                filter: blur(100px);

                transition: .3s opacity ease-in-out;

                display: block;
                position: absolute;

                opacity: 0;
                z-index: 1;
            }

            &:hover:before {
                background: linear-gradient(60deg, #f79533, #f37055, #ef4e7b, #a166ab, #5073b8, #1098ad, #07b39b, #6fba82);

                opacity: 1;

                transition: .3s opacity ease-in-out;

                filter: blur(100px);
            }
*/
            &:after {
                width: 92%;
                height: 80%;
                left: 4%;
                border-radius: 180px;

                content: 'CLICK ME';

                color: rgba(235, 235, 235, 1);
                background-color: rgb(19, 20, 22);

                font-size: 18px;
                font-weight: bold;

                line-height: 40;
                text-align: center;

                display: block;
                position: absolute;

                z-index: 5;
            }

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
</style>
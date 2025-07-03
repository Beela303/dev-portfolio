<script>
</script>

<template>
  <div id="home">
    <h1>Hello, there!</h1>
    <h2>I'm Nabila Abubakar</h2>
    <h2>Full Stack Developer</h2>
  </div>

  <div id="about">
    <h2>About Me:</h2>
    <p>Highly skilled Full Stack Web Developer with expertise in Front-end and Back-end development.</p>
    <p>Passionate about Delivering High Quality Web Applications that meet client needs.</p>
    <p>Proficient in HTML, CSS, SASS, Bootstrap, jQuery, JavaScript, Vue, Nuxt.js, Django & MySQL</p>
  </div>

  <div id="tech-stack">
    <h2>TECH STACK</h2>
    <div class="stack">
      <h3>FRONTEND</h3>
      <ul>
        <li><i class="devicon-html5-plain colored"></i>HTML</li>
        <li><i class="devicon-css3-plain colored"></i>CSS</li>
        <li><i class="devicon-sass-plain colored"></i>Sass</li>
        <li><i class="devicon-bootstrap-plain colored"></i>BootStrap</li>
        <li><i class="devicon-bulma-plain colored"></i>Bulma</li>
        <li><i class="devicon-vuejs-plain colored"></i>Vue</li>
        <li><i class="devicon-nuxtjs-plain colored"></i>Nuxt</li>
      </ul>
    </div>

    <div class="stack">
      <h3>BACKEND</h3>
      <ul>
        <li><i class="devicon-django-plain colored"></i>Django</li>
        <li><i class="devicon-djangorest-plain colored"></i>Django Rest Framework</li>
        <li><i class="devicon-graphql-plain colored"></i>GraphQL</li>
        <li><i class="devicon-mysql-plain colored"></i>MySQL</li>
      </ul>
    </div>

    <div class="stack">
      <h3>DEVOPS & INFRASTRUCTURE</h3>
      <ul>
        <li><i class="devicon-vercel-plain colored"></i>Vercel</li>
        <li><i class="devicon-cloudflare-plain colored"></i>Cloudflare</li>
      </ul>
    </div>

    <div class="stack">
      <h3>TOOLS & UTILITIES</h3>
      <ul>
        <li><i class="devicon-github-plain colored"></i>GitHUb</li>
        <li><i class="devicon-npm-original-wordmark colored"></i>NPM</li>
        <li><i class="devicon-postman-plain colored"></i>Postman</li>
        <li><i class="devicon-babel-plain colored"></i>Babel</li>
      </ul>
    </div>
  </div>

  <h2 id="portfolio-title">Portfolio</h2>
  <div id="portfolio">
    <div class="project">
      <img src="../assets/1.jpg" alt="">
      <h2>Project Title</h2>
      <p class="desc">Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores est quia ipsum nulla fuga soluta
        perspiciatis! Nesciunt culpa officiis c</p>
      <div class="languages">
        <!---<p>HTML, CSS, JS</p>-->
        <i class="devicon-html5-plain colored"></i>
        <i class="devicon-css3-plain colored"></i>
        <i class="devicon-sass-plain colored"></i>
        <i class="devicon-bootstrap-plain colored"></i>
        <i class="devicon-bulma-plain colored"></i>
        <i class="devicon-vuejs-plain colored"></i>
      </div>

      <div class="live-code">
        <button><a href="http://" target="_blank" rel="noopener noreferrer">Live Demo</a></button>
        <button><a href="http://" target="_blank" rel="noopener noreferrer">GitHub</a></button>
      </div>
    </div>

    <div class="project">
      <img src="../assets/1.jpg" alt="">
      <h2>Project Title</h2>
      <p class="desc">Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores est quia ipsum nulla fuga soluta
        perspiciatis! Nesciunt culpa officiis c</p>
      <div class="languages">
        <!---<p>HTML, CSS, JS</p>-->
        <i class="devicon-html5-plain colored"></i>
        <i class="devicon-css3-plain colored"></i>
        <i class="devicon-sass-plain colored"></i>
        <i class="devicon-bootstrap-plain colored"></i>
        <i class="devicon-bulma-plain colored"></i>
        <i class="devicon-vuejs-plain colored"></i>
      </div>

      <div class="live-code">
        <button><a href="http://" target="_blank" rel="noopener noreferrer">Live Demo</a></button>
        <button><a href="http://" target="_blank" rel="noopener noreferrer">GitHub</a></button>
      </div>
    </div>

    <div class="project">
      <img src="../assets/1.jpg" alt="">
      <h2>Project Title</h2>
      <p class="desc">Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores est quia ipsum nulla fuga soluta
        perspiciatis! Nesciunt culpa officiis c</p>
      <div class="languages">
        <!---<p>HTML, CSS, JS</p>-->
        <i class="devicon-html5-plain colored"></i>
        <i class="devicon-css3-plain colored"></i>
        <i class="devicon-sass-plain colored"></i>
        <i class="devicon-bootstrap-plain colored"></i>
        <i class="devicon-bulma-plain colored"></i>
        <i class="devicon-vuejs-plain colored"></i>
      </div>

      <div class="live-code">
        <button><a href="http://" target="_blank" rel="noopener noreferrer">Live Demo</a></button>
        <button><a href="http://" target="_blank" rel="noopener noreferrer">GitHub</a></button>
      </div>
    </div>

    <div class="project">
      <img src="../assets/1.jpg" alt="">
      <h2>Project Title</h2>
      <p class="desc">Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolores est quia ipsum nulla fuga soluta
        perspiciatis! Nesciunt culpa officiis c</p>
      <div class="languages">
        <!---<p>HTML, CSS, JS</p>-->
        <i class="devicon-html5-plain colored"></i>
        <i class="devicon-css3-plain colored"></i>
        <i class="devicon-sass-plain colored"></i>
        <i class="devicon-bootstrap-plain colored"></i>
        <i class="devicon-bulma-plain colored"></i>
        <i class="devicon-vuejs-plain colored"></i>
      </div>

      <div class="live-code">
        <button><a href="http://" target="_blank" rel="noopener noreferrer">Live Demo</a></button>
        <button><a href="http://" target="_blank" rel="noopener noreferrer">GitHub</a></button>
      </div>
    </div>

  </div>
</template>

<style lang="scss" scoped>
#home {
  background: var(--main-gradient);

  height: 30vh;
  border-radius: 30px;

  display: grid;
  justify-content: center;
  text-align: center;

  h1 {
    font-size: 4rem;
  }

  h2 {
    font-size: 3rem;
  }
}

#about {
  height: 70vh;
  display: grid;

  h2 {
    font-size: 4rem;
    text-align: center;
  }

  p {
    font-size: 1.5rem;
  }
}

#tech-stack {
  h2 {
    font-size: 3rem;
    text-align: center;
  }

  .stack {
    margin: 30px;

    column-count: 2;
    column-width: 50%;

    h3 {
      font-size: 2rem;
    }

    ul {


      li {
        color: var(--text-color);
        background: var(--purple-color);

        width: 70%;

        padding: 5px;
        margin: 2%;

        text-align: center;
        font-size: 1.5rem;

        border: 3px solid var(--pastel-color-2);
        border-radius: 15px;

        i {
          font-size: 2rem;
        }
      }
    }
  }
}

#portfolio-title {
  font-size: 3rem;
  text-align: center;
}

#portfolio {
  column-count: 2;
  column-width: 50%;

  .project {
    color: var(--text-color);

    height: 90vh;

    margin: 5%;
    padding: 20px;

    border: 2px solid var(--purple-color);
    border-radius: 15px;

    transition: 2s;

    img {
      width: 100%;
      height: 40vh;

      border-radius: 30px;

      object-fit: cover;
    }

    h2 {
      font-size: 2rem;

      text-align: center;
    }

    .desc {
      margin: 2%;
      font-size: 1.5rem;
    }

    .languages {
      color: var(--dark);
      background: var(--pastel-color-2);

      min-height: 5vh;

      display: flex;
      justify-content: space-between;

      i {
        font-size: 3rem;
      }
    }

    .live-code {
      button:first-child {
        background: var(--purple-color);

        &:hover {
          background: none;
          border: 2px solid var(--purple-color);
        }
      }

      button {
        border: 2px solid var(--purple-color);

        width: 45%;
        height: 7vh;

        margin: 2%;
        bottom: 2vh;

        transition: 1s;

        &:hover {
          background: var(--purple-color);
        }

        a {
          color: var(--text-color);
          font-size: 1.5rem;
        }
      }
    }
  }
}

@media screen and (max-width: 768px) {
  #tech-stack {
    .stack {
      ul {
        li {
          width: 100%;
        }
      }
    }
  }

  #portfolio {
    columns: 1;
    column-width: 100%;
  }
}
</style>
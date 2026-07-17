<script setup>
import { ref, computed } from 'vue';

const aboutSection = ref(false)
const techStackSection = ref(false)
const experienceSection = ref(false)
const projectsSection = ref(false)
const contactSection = ref(false)
const socialsSection = ref(false)

const frontendSection = ref(false)
const backendSection = ref(false)
const fullstackSection = ref(false)


const experiences = ref([
  {
    id: 1,
    role: 'Frontend Developer Intern',
    company: 'FexiSAF Edusoft Limited',
    dates: 'January 2026 - April 2026',
    description: 'Developing scalable web applications using React.',
    category: 'Frontend',
    icon: 'fa-code',
    tags: ['React', 'JavaScript', 'HTML/CSS']
  },
  {
    id: 2,
    role: 'Backend Developer Intern',
    company: 'FexiSAF Edusoft Limited',
    dates: 'May 2026 - Present',
    description: 'Developing scalable secure backend applications.',
    category: 'Backend',
    icon: 'fa-code',
    tags: ['Java', 'Springboot']
  },
]);

const categories = ['All', 'Frontend', 'Backend'];
const selectedCategory = ref('All');

const filteredJobs = computed(() => {
    const reversedList = [...experiences.value].reverse();

    if (selectedCategory.value === 'All') {
        return reversedList;
    }
    return reversedList.filter(job => job.category === selectedCategory.value);
});

</script>

<template>
  <div id="intro">
    <h1>Welcome to the Portfolio<span class="highlight-text">Verse</span></h1>
    <h2><span class="highlight-text">
      <a href="https://beela303.vercel.app/" target="_blank" rel="noopener noreferrer">
        Nabila's</a>
      </span> Version</h2>
  </div>

  <div id="navigations">
    <div class="nav" :disabled="aboutSection" @click="aboutSection = true">
      <!--<img src="../assets/icons/Treetog-Junior-Folder-fav.256.png" alt="About">-->
      <span class="material-icons">person</span>
      <h2>About</h2>
    </div>

    <div class="nav" :disabled="techStackSection" @click="techStackSection = true">
      <!--<img src="../assets/icons/Franksouza183-Fs-Apps-konsole.512.png" alt="Tech Stack">-->
      <span class="material-icons">layers</span>
      <h2>Tech Stack</h2>
    </div>

    <div class="nav" :disabled="experienceSection" @click="experienceSection = true">
      <!--<img src="../assets/icons/Anabellafalivene-Cute-Folders-Folder-Balloons.512.png" alt="Experience">-->
      <span class="material-icons">business_center</span>
      <h2>Experience</h2>
    </div>

    <div class="nav" :disabled="projectsSection" @click="projectsSection = true">
      <!--<img src="../assets/icons/Franksouza183-Fs-Places-folder-black.512.png" alt="Projects">-->
      <span class="material-icons">work</span>
      <h2>Projects</h2>
    </div>

    <div class="nav" :disabled="contactSection" @click="contactSection = true">
      <!--<img src="../assets/icons/Uriy1966-Steel-System-Desktop.512.png" alt="Contact">-->
      <span class="material-icons">email</span>
      <h2>Contact</h2>
    </div>

    <div class="nav" :disabled="socialsSection" @click="socialsSection = true">
      <!--<img src="../assets/icons/Franksouza183-Fs-Categories-applications-internet.512.png" alt="socials">-->
      <span class="material-icons">tag</span>
      <h2>Socials</h2>
    </div>
  </div>

  <section id="all-sections">
    <!--ABOUT SECTION-->
    <section class="section" v-if="aboutSection">
      <div class="top">
        <h1>ABOUT</h1>
        <span class="material-icons" :disabled="aboutSection" @click="aboutSection = false">close</span>
      </div>

      <hr>

      <div class="division">
        <div class="left">
          <img src="../assets/43.webp" alt="">
        </div>

        <div class="right">
          <p>Name: <span class="answer">Nabila Abubakar</span></p>
          <p>Work: <span class="answer">Software Developer</span></p>
          <p>Skills: <span class="answer">Web & App Development</span></p>
          <p>Resume:
            <a href="Software Developer - Nabila Abubakar.pdf" download="Software Developer - Nabila Abubakar.pdf"
              class="answer">
              Download Resume
            </a>
          </p>
        </div>
      </div>

    </section>

    <!--TECHSTACK SECTION-->
    <section class="section" v-if="techStackSection">
      <div class="top">
        <h1>TECH STACK</h1>
        <span class="material-icons" :disabled="techStackSection" @click="techStackSection = false">close</span>
      </div>

      <hr>

      <div id="tech-stack">
        <h3>FRONTEND</h3>
        <div class="stack">
          <ul>
            <li><i class="devicon-react-plain colored"></i>React</li>
            <!--<li><i class="devicon-nuxtjs-plain colored"></i>Nuxt</li>-->
            <li><i class="devicon-vuejs-plain colored"></i>Vue</li>
            <li><i class="devicon-sass-plain colored"></i>SASS</li>
            <li><i class="devicon-html5-plain colored"></i>HTML</li>
            <li><i class="devicon-css3-plain colored"></i>CSS</li>
            <li><i class="devicon-bootstrap-plain colored"></i>BootStrap</li>
            <li><i class="devicon-tailwindcss-plain colored"></i>Tailwind</li>
            <!--<li><i class="devicon-bulma-plain colored"></i>Bulma</li>-->
            <li><i class="devicon-javascript-plain colored"></i>JavaScript</li>
            <li><i class="devicon-jquery-plain colored"></i>jQuery</li>
          </ul>
        </div>

        <h3>BACKEND</h3>
        <div class="stack">
          <ul>
            <li><i class="devicon-django-plain"></i>Django</li>
            <li><i class="devicon-djangorest-plain"></i>DRF</li>
            <li><i class="devicon-graphql-plain colored"></i>GraphQL</li>
            <li><i class="devicon-postgresql-plain colored"></i>PostgreSQL</li>
            <!--<li><i class="devicon-mysql-plain colored"></i>MySQL</li>-->
          </ul>
        </div>

        <h3>APP DEVELOPMENT</h3>
        <div class="stack">
          <ul>
            <li><i class="devicon-electron-original colored"></i>Electron</li>
            <li><i class="devicon-ionic-original colored"></i>Ionic</li>
          </ul>
        </div>

        <h3>DEVOPS & INFRASTRUCTURE</h3>
        <div class="stack">
          <ul>
            <li><i class="devicon-vercel-plain"></i>Vercel</li>
            <li><i class="devicon-cloudflare-plain colored"></i>Cloudflare</li>
            <li><i class="devicon-netlify-plain"></i>Netlify</li>
            <!--<li><i class="devicon-render-plain colored"></i>Render</li>-->
            <li>Render</li>
          </ul>
        </div>

        <h3>TOOLS & UTILITIES</h3>
        <div class="stack">
          <ul>
            <li><i class="devicon-github-plain colored"></i>GitHub</li>
            <li><i class="devicon-npm-original-wordmark colored"></i>NPM</li>
            <li><i class="devicon-postman-plain colored"></i>Postman</li>
            <li><i class="devicon-vscode-plain colored"></i>VS Code</li>
            <!--<li><i class="devicon-babel-plain colored"></i>Babel</li>-->
          </ul>
        </div>
      </div>

    </section>

    <!--EXPERIENCE SECTION-->
    <section class="section" v-if="experienceSection">
      <div class="top">
        <h1>EXPERIENCE</h1>
        <span class="material-icons" :disabled="experienceSection" @click="experienceSection = false">close</span>
      </div>

      <hr>

      <!--<div id="experiences">
        <div class="experience">
          <span class="time">May 2026 - Present</span>
          <h3 class="title">Backend Developer Intern</h3>
          <h4><span class="framework">Language & Framework:</span> Java, SpringBoot</h4>
          <p class="company">FlexiSAF Edusoft Limited</p>
        </div>

        <div class="experience">
          <span class="time">Jan 2026 - April 2026</span>
          <h3 class="title">Frontend Developer Intern</h3>
          <h4><span class="framework">Language & Framework:</span> JavaScript, React</h4>
          <p class="company">FlexiSAF Edusoft Limited</p>
        </div>
      </div>-->

      <div class="experience-page">
        <!-- Category Tags Navigation -->
        <div class="categories">
            <button v-for="category in categories" :key="category"
                :class="['tag', { active: selectedCategory === category }]" @click="selectedCategory = category">
                {{ category }}
            </button>
        </div>

        <!-- Timeline Wrapper -->
        <div class="timeline">
            <!-- TransitionGroup enables fluid shuffling/filtering animations -->
            <TransitionGroup name="timeline-list">
                <div v-for="(job, index) in filteredJobs" :key="job.id" class="timeline-item">
                    <!-- Dynamic Font Awesome Icon replaces standard dot -->
                    <div class="timeline-dot-icon">
                        <i :class="['fas', job.icon]"></i>
                    </div>

                    <div class="timeline-content">
                        <h3>{{ job.role }}</h3>
                        <h4>{{ job.company }}</h4>
                        <p class="date">{{ job.dates }}</p>
                        <p class="description">{{ job.description }}</p>
                        <div class="job-tags">
                            <span v-for="tag in job.tags" :key="tag" class="job-tag">{{ tag }}</span>
                        </div>
                    </div>
                </div>
            </TransitionGroup>
        </div>
    </div>
    </section>

    <!--PROJECTS SECTION-->
    <section class="section" v-if="projectsSection">
      <div class="top">
        <h1>PROJECTS</h1>
        <span class="material-icons" :disabled="projectsSection" @click="projectsSection = false">close</span>
      </div>

      <hr>

      <div id="projects-tab">
        <button class="project-tab" :disabled="frontendSection" @click="frontendSection = true">Frontend</button>
        <button class="project-tab" :disabled="backendSection" @click="backendSection = true">Backend</button>
        <button class="project-tab" :disabled="fullstackSection" @click="fullstackSection = true">Full Stack</button>
      </div>
    </section>

    <section class="section" v-if="frontendSection">
      <div class="top">
        <h1>FRONTEND</h1>
        <span class="material-icons" :disabled="frontendSection" @click="frontendSection = false">close</span>
      </div>

      <hr>

      <div class="projects">
        <div class="project">
          <div class="left">
            <img src="../assets/website assets/srv-home-page-01.jpg" alt="Smart Results Viewer">
          </div>

          <div class="right">
            <h2>Smart Results Viewer</h2>
            <p class="desc">Final project for my frontend internship.
              It's functionality includes search results by name, course or index number,
              downloadable summary, performance graphs and more.
              The JSON file is hosted on <a href="https://smart-results-viewer.onrender.com/students/" target="_blank"
                rel="noopener noreferrer">
                Render</a> and the frontend on <a href="https://smart-results-viewer-nabila.netlify.app/" target="_blank"
                  rel="noopener noreferrer">Netlify</a>.
            </p>
            <div class="languages">
              <i class="devicon-react-plain colored"></i>
              <i class="devicon-tailwindcss-plain colored"></i>
              <i class="devicon-json-plain colored"></i>
            </div>

            <div class="live-code">
              <button><a href="https://smart-results-viewer-nabila.netlify.app/" target="_blank"
                  rel="noopener noreferrer">Live
                  Demo</a></button>
              <button><a href="https://github.com/Beela303/Smart-Results-Viewer/" target="_blank"
                  rel="noopener noreferrer">GitHub</a></button>
            </div>
          </div>
        </div>

        <div class="project">
          <div class="left">
            <img src="../assets/website assets/login - inventory dashboard.jpg" alt="Inventory Dashboard">
          </div>

          <div class="right">
            <h2>
              Inventory Dashboard
            </h2>
            <p class="desc">An Inventory Dashboard which features products, categories, stocks,
               stock management, sales, low stock and their equivalent add pages and information pages.
            </p>
            <div class="languages">
              <i class="devicon-react-plain colored"></i>
              <i class="devicon-tailwindcss-plain colored"></i>
            </div>

            <div class="live-code">
              <button><a href="https://github.com/Beela303/inventory-dashboard/" target="_blank"
                  rel="noopener noreferrer">GitHub</a></button>
            </div>
          </div>
        </div>

        <div class="project">
          <div class="left">
            <img src="../assets/website assets/Space Tourism HomePage.png" alt="Space Tourism Homepage">
          </div>

          <div class="right">
            <h2>Space Tourism Website (Frontend Challenge)</h2>
            <p class="desc">This is a challenge by <a href="http://frontendmentor.io" target="_blank"
                rel="noopener noreferrer">Frontend Mentor</a>. It features the HomePage, Destination, Crew, Technology
              and
              several other
              nested pages.</p>
            <div class="languages">
              <i class="devicon-vuejs-plain colored"></i>
              <i class="devicon-sass-plain colored"></i>
            </div>

            <div class="live-code">
              <button><a href="https://space-tourism-flax-gamma.vercel.app/" target="_blank"
                  rel="noopener noreferrer">Live
                  Demo</a></button>
              <button><a href="https://github.com/Beela303/space-tourism/" target="_blank"
                  rel="noopener noreferrer">GitHub</a></button>
            </div>
          </div>
        </div>

        <div class="project">
          <div class="left">
            <img src="../assets/website assets/art sphere home page 1.png" alt="Art Sphere Homepage">
          </div>

          <div class="right">
            <h2>Art Sphere (Artist's Portfolio)</h2>
            <p class="desc">Portfolio site for an artist which showcases the artist's skills and talents. It includes
              the
              home, about, gallery and contact pages.</p>
            <div class="languages">
              <i class="devicon-vuejs-plain colored"></i>
              <i class="devicon-sass-plain colored"></i>
            </div>

            <div class="live-code">
              <button><a href="https://art-sphere-vue.vercel.app" target="_blank" rel="noopener noreferrer">Live
                  Demo</a></button>
              <button><a href="https://github.com/Beela303/art-sphere-vue-" target="_blank"
                  rel="noopener noreferrer">GitHub</a></button>
            </div>
          </div>
        </div>

        <div class="project">
          <div class="left">
            <img src="../assets/website assets/Queen Beela v2 blogs.jpg" alt="Queen Beela v2 Blogs page">
          </div>
          
          <div class="right">
            <h2>Queen Beela v2 (Personal Website)</h2>
            <p class="desc">This is my personal website which has pages for my blog, homepage, podcast, portfolio, gallery and
              socials.</p>
            <div class="languages">
              <i class="devicon-vuejs-plain colored"></i>
              <i class="devicon-sass-plain colored"></i>
            </div>

            <div class="live-code">
              <button><a href="https://beela303.vercel.app/" target="_blank" rel="noopener noreferrer">Live
                  Demo</a></button>
              <button><a href="https://github.com/Beela303/Queen-Beela-vue-" target="_blank"
                  rel="noopener noreferrer">GitHub</a></button>
            </div>
          </div>
        </div>

        <div class="project">
          <div class="left">
            <img src="../assets/website assets/Movies Database search page.png" alt="Movies Database Homepage">
          </div>

          <div class="right">
            <h2>Movies DataBase</h2>
            <p class="desc">This is a website that uses the OMDB API to fetch movies and display it on the screen when a
              movie
              is searched.</p>
            <div class="languages">
              <i class="devicon-vuejs-plain colored"></i>
              <i class="devicon-sass-plain colored"></i>
            </div>

            <div class="live-code">
              <button><a href="https://movies-db-beta-nine.vercel.app/" target="_blank" rel="noopener noreferrer">Live
                  Demo</a></button>
              <button><a href="https://github.com/Beela303/movies_db" target="_blank"
                  rel="noopener noreferrer">GitHub</a></button>
            </div>
          </div>
        </div>

        <div class="project">
          <div class="left">
            <img src="../assets/website assets/blog website - blog list.jpeg" alt="Blog website's blog list">
          </div>
          
          <div class="right">
            <h2>Blog Website</h2>
            <p class="desc">A blog website for a content creator with a light & dark theme, home page and blog page.</p>
            <div class="languages">
              <i class="devicon-html5-plain colored"></i>
              <i class="devicon-css3-plain colored"></i>
              <i class="devicon-javascript-plain colored"></i>
              <i class="devicon-jquery-plain colored"></i>
            </div>

            <div class="live-code">
              <button><a href="https://beela303.github.io/blog-website" target="_blank" rel="noopener noreferrer">Live
                  Demo</a></button>
              <button><a href="https://github.com/Beela303/blog-website" target="_blank"
                  rel="noopener noreferrer">GitHub</a></button>
            </div>
          </div>
        </div>

        <div class="project">
          <div class="left">
            <img src="../assets/website assets/e-commerce website - homepage.jpeg" alt="E-commerce website Homepage">
          </div>
          
          <div class="right">
            <h2>E-commerce Website</h2>
            <p class="desc">This is an e-commerce website showcasing the home page, products, account, about, contact and cart
              pages.</p>
            <div class="languages">
              <i class="devicon-html5-plain colored"></i>
              <i class="devicon-css3-plain colored"></i>
              <i class="devicon-javascript-plain colored"></i>
              <i class="devicon-jquery-plain colored"></i>
            </div>

            <div class="live-code">
              <button><a href="https://beela303.github.io/e-commerce-website" target="_blank" rel="noopener noreferrer">Live
                  Demo</a></button>
              <button><a href="https://github.com/Beela303/e-commerce-website" target="_blank"
                  rel="noopener noreferrer">GitHub</a></button>
            </div>
          </div>
        </div>

        <div class="project">
          <div class="left">
            <img src="../assets/website assets/Queen Beela v1 gallery.jpg" alt="Queen Beela v1 Gallery page">
          </div>
          
          <div class="right">
            <h2>Queen Beela v1 (Personal Website)</h2>
            <p class="desc">This was my personal website which has pages for my blog, homepage, podcast, portfolio, gallery and
              socials.</p>
            <div class="languages">
              <i class="devicon-html5-plain colored"></i>
              <i class="devicon-css3-plain colored"></i>
              <i class="devicon-javascript-plain colored"></i>
              <i class="devicon-jquery-plain colored"></i>
            </div>

            <div class="live-code">
              <button><a href="https://beela303.github.io/QueenBeela" target="_blank" rel="noopener noreferrer">Live
                  Demo</a></button>
              <button><a href="https://github.com/Beela303/QueenBeela" target="_blank"
                  rel="noopener noreferrer">GitHub</a></button>
            </div>
          </div>
        </div>

        <div class="project">
          <div class="left">
            <img src="../assets/website assets/Company website - services.jpeg" alt="Company website services page">
          </div>
          
          <div class="right">
            <h2>Company Website</h2>
            <p class="desc">A single page website for a company using HTML, CSS and JavaScript.</p>
            <div class="languages">
              <i class="devicon-html5-plain colored"></i>
              <i class="devicon-css3-plain colored"></i>
              <i class="devicon-javascript-plain colored"></i>
              <i class="devicon-jquery-plain colored"></i>
            </div>

            <div class="live-code">
              <button><a href="https://beela303.github.io/Company-website/" target="_blank" rel="noopener noreferrer">Live
                  Demo</a></button>
              <button><a href="https://github.com/Beela303/company-website/" target="_blank"
                  rel="noopener noreferrer">GitHub</a></button>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="section" v-if="backendSection">
      <div class="top">
        <h1>BACKEND</h1>
        <span class="material-icons" :disabled="backendSection" @click="backendSection = false">close</span>
      </div>

      <hr>

      <div class="projects">
        <div class="project">
          <div class="left">
            <img src="../assets/website assets/login - inventory dashboard.jpg" alt="Inventory Dashboard">
          </div>

          <div class="right">
            <h2>
              Inventory Dashboard
            </h2>
            <p class="desc">This is an inventory dashboard with an accounts, inventory and sales app.
              it features products, categories, stocks, stock management, sales and low stock with appropriate permissions.
            </p>
            <div class="languages">
              <i class="devicon-django-plain"></i>
              <i class="devicon-djangorest-plain"></i>
              <i class="devicon-postgresql-plain colored"></i>
            </div>

            <div class="live-code">
              <button><a href="https://github.com/Beela303/inventory-dashboard/" target="_blank"
                  rel="noopener noreferrer">GitHub</a></button>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="section" v-if="fullstackSection">
      <div class="top">
        <h1>FULL STACK</h1>
        <span class="material-icons" :disabled="fullstackSection" @click="fullstackSection = false">close</span>
      </div>

      <hr>

      <div class="projects">
        <div class="project">
          <div class="left">
            <img src="../assets/website assets/login - inventory dashboard.jpg" alt="Inventory Dashboard">
          </div>

          <div class="right">
            <h2>
              Inventory Dashboard
            </h2>
            <p class="desc">This is a full stack inventory dashboard with an accounts, inventory and sales app.
              it features products, category, stocks, stock management, sales and low stock with related
             permissions.
            </p>
            <div class="languages">
              <i class="devicon-react-plain colored"></i>
              <i class="devicon-tailwindcss-plain colored"></i>
              <i class="devicon-django-plain"></i>
              <i class="devicon-djangorest-plain"></i>
              <i class="devicon-postgresql-plain colored"></i>
            </div>

            <div class="live-code">
              <button><a href="https://github.com/Beela303/inventory-dashboard/" target="_blank"
                  rel="noopener noreferrer">GitHub</a></button>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!--CONTACT SECTION-->
    <section class="section" v-if="contactSection">
      <div class="top">
        <h1>CONTACT ME</h1>
        <span class="material-icons" :disabled="contactSection" @click="contactSection = false">close</span>
      </div>

      <hr>

      <div id="contact-form">
        <form action="https://formsubmit.co/dc027401bb393a2c66cb207f9cccd3e2" method="POST">
          <!--Honeypot-->
          <input type="text" name="_honey" style="display:none" />

          <!--Disable initial captcha-->
          <input type="hidden" name="_captcha" value="true" />

          <!--Custom response-->
          <input type="hidden" name="_autoresponse"
            value="Thank you for reaching out! I can't wait to work with you!!! You'll receive a reply soon :)" />

          <!--Subject-->
          <input type="hidden" name="_subject" value="New Submission!" />

          <label for="name">Name: </label>
          <br />
          <input type="text" id="name" name="name" placeholder="Your Name" required>
          <br />

          <label for="name">Email: </label>
          <br />
          <input type="email" id="email" name="email" placeholder="Your Email" required>
          <br />

          <label for="content">Content:</label>
          <br />
          <textarea type="text" id="content" name="content" placeholder="I'm looking for..." rows="5" cols="40"
            required></textarea>
          <br />

          <button type="submit">Submit</button>
        </form>

      </div>
    </section>

    <!--SOCIALS SECTION-->
    <section class="section" v-if="socialsSection">
      <div class="top">
        <h1>SOCIALS</h1>
        <span class="material-icons" :disabled="socialsSection" @click="socialsSection = false">close</span>
      </div>

      <hr>

      <div id="socials">
        <ul>
          <li>
            <a href="https://beela303.vercel.app/" target="_blank" rel="noopener noreferrer">
              <i class="fas fa-globe"></i>
            </a>
          </li>

          <li>
            <a href="mailto:nabilaabubakar333@gmail.com" target="_blank" rel="noopener noreferrer">
              <i class="fas fa-envelope"></i>
              <!--<p>Email</p>-->
            </a>
          </li>

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
    </section>

  </section>

</template>

<style lang="scss" scoped>
.highlight-text {
  color: var(--purple-color);

  a {
    color: var(--purple-color);
  }
}

#intro {
  text-align: center;

  margin: 3rem;
}

#navigations {
  display: grid;

  grid-template-columns: repeat(3, 200px);
  grid-gap: 10px;

  place-content: center;
  justify-items: center;

  //grid-auto-rows: 50px;
  //width: 516px;
  /*display: grid;
  place-content: center;
  justify-items: center;
  min-height: 100vh;
  gap: 15px;*/

  //justify-content: space-between;

  .nav {
    width: 150px;
    height: 150px;

    margin-bottom: 50px;

    border: 1px dashed var(--pastel-color);
    border-radius: 15px;

    text-align: center;

    cursor: pointer;

    img {
      width: 150px;
      height: 150px;

      padding: 20px;
      border-radius: 30px;

      transition: var(--transition);
    }

    span {
      padding: 20px;
      font-size: 4rem;

      transition: var(--transition);
    }

    &:hover {
      border-radius: 30px;

      img {
        padding: 0;
      }
    }
  }
}

.section {
  //background: var(--dark-alt);

  top: 5%;
  left: 5%;
  width: 90%;
  height: 90%;

  box-shadow: inset 0 0 0 8px var(--purple-color);
  /*box-shadow: inset 0 0 0 15px var(--purple-color);*/
  border-radius: 45px;

  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(10px);

  background-color: #160b17;
  //background-color: rgba(255, 255, 255, 0.3);

  position: fixed;
  justify-self: center;

  z-index: 1000;

  overflow-y: scroll;

  .top {
    padding: 20px 70px;

    display: flex;
    justify-content: space-between;

    span {
      font-size: 2.5rem;

      cursor: pointer;
      transition: var(--transition);

      &:hover {
        color: var(--dark);
      }
    }
  }

  hr {
    color: var(--pastel-color-2);
    margin-bottom: 20px;
  }

  // ABOUT SECTION
  .division {
    padding: 50px;

    display: flex;
    justify-content: space-between;

    .left,
    .right {
      width: 50%;
    }

    .left {
      img {
        width: 30vw !important;
        height: 60vh !important;
        //height: 90%;
        //width: 90%;

        rotate: 90deg;

        border-radius: 30px;
        object-fit: cover;
      }
    }

    .right {
      font-size: 2rem;

      p {
        line-height: 70px;
        //color: var(--dark-color);
        
        .answer {
          color: var(--text-color);
          transition: var(--transition);
        }

        a:hover {
          color: var(--pastel-color-2);
          transition: var(--transition);
        }
      }
    }
  }

  // TECH STACH
  #tech-stack {
    padding: 30px;
    padding-top: 0;

    h3 {
      margin-top: 15px;
      
      &:first-child {
        margin-top: 0;
      }
    }

    ul {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr 1fr;
      gap: 20px;

      li {
        background-color: var(--purple-color);
        //background-color: var(--dark);

        height: 40px;
        margin: 10px;
        margin-bottom: 0;
        padding: 5px;

        font-size: 1.5rem;

        border: 1px solid var(--text-color);
        border-radius: 15px;
      }
    }
  }

  // EXPERIENCE SECTION

  #experiences {
    padding: 15px 30px;

    .experience {
      background-color: var(--dark);

      margin: 15px;
      padding: 15px;

      border: 1px dashed var(--text-color);
      border-radius: 30px;

      .time {
        font-size: 1.3rem;
      }

      .title {
        color: var(--purple-color);
        //color: var(--pastel-color);

        margin: 0;
        font-size: 1.6rem;
      }

      h4 {
        margin: 5px 0;

        /*.framework {
        color: var(--grey);
      }*/
      }

      .company {
        font-size: 1.4rem;
      }
    }
  }

  // TIMELINE EXPERIENCE
  .experience-page {
    max-width: 800px;
    margin: 0 auto;
    padding: 2rem;

    /* Category Filter Tags Style */
    .categories {
        margin-bottom: 3.5rem;
        gap: 12px;

        display: flex;
        justify-content: center;

        .tag {
            color: #4b5563;
            background: var(--text-color);

            padding: 10px 20px;

            border: 1px solid #e5e7eb;
            border-radius: 25px;

            font-weight: 500;

            box-shadow: 0 1px 2px rgba(0, 0, 0, 0.05);
            transition: all 0.25s cubic-bezier(0.4, 0, 0.2, 1);

            cursor: pointer;

            &.active,
            &:hover {
                color: var(--text-color);
                background: var(--purple-color);
                //background: var(--main-color);

                border-color: var(--pastel-color-2);

                transform: translateY(-1px);
                box-shadow: 0 4px 6px -1px rgba(59, 130, 246, 0.2);
            }
        }
    }

    /* Timeline Layout Base Line */
    .timeline {
        margin-left: 1.5rem;
        padding-left: 2.5rem;

        border-left: 2px solid #e5e7eb;

        position: relative;

        .timeline-item {
            background: var(--dark-color);
            //background: var(--text-color);

            margin-bottom: 2.5rem;
            padding: 1.25rem;

            border-radius: 8px;
            border: 1px solid var(--pastel-color-2);
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.05);

            position: relative;

            .timeline-dot-icon {
                color: var(--text-color);
                background: var(--purple-color);
                //background: var(--main-color);

                left: -3.45rem;
                top: 14px;

                width: 28px;
                height: 28px;
                border-radius: 50%;

                box-shadow: 0 0 0 4px #ffffff, 0 2px 4px rgba(0, 0, 0, 0.1);

                font-size: 0.85rem;

                display: flex;
                align-items: center;
                justify-content: center;

                position: absolute;
                z-index: 2;
            }

            .timeline-content {
                color: var(--text-color);
                background-color: var(--dark-color);

                h3 {
                    color: var(--text-color);
                    //color: #111827;

                    margin: 0;
                    font-size: 1.25rem;
                }

                h4 {
                    color: #b6b5af;
                    //color: #4b5563;

                    margin: 0.35rem 0 0;
                    font-weight: 500;
                }

                .date {
                    color: #c1cada;
                    //color: #9ca3af;

                    margin: 0.5rem 0 0.75rem;

                    font-size: 0.85rem;
                    font-weight: 500;
                }

                .description {
                  color: #d5d9e0;
                  //color: #374151;

                  margin: 0;
                  line-height: 1.5;
                }

                .job-tags {
                    margin-top: 1rem;

                    gap: 8px;

                    display: flex;
                    flex-wrap: wrap;

                    .job-tag {
                        color: var(--text-color);
                        background: var(--purple-color);

                        //color: #4b5563;
                        //background: var(--text-color);

                        padding: 4px 10px;

                        border-radius: 6px;
                        border: 1px solid var(--pastel-color-2);

                        font-weight: 500;
                        font-size: 0.75rem;
                    }
                }
            }
        }
    }
}

/* --- Vue TransitionGroup Classes --- */

/* Elements Entering and Leaving */
.timeline-list-enter-active,
.timeline-list-leave-active {
    transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
}

/* From State (Entering) / To State (Leaving) */
.timeline-list-enter-from,
.timeline-list-leave-to {
    opacity: 0;
    transform: translateX(-30px);
}

/* Absolute positioning during leave ensures smooth grid collapsing */
.timeline-list-leave-active {
    position: absolute;
    width: calc(100% - 2.5rem);
}

/* Smooth reordering layout movement (v-move) */
.timeline-list-move {
    transition: transform 0.4s cubic-bezier(0.4, 0, 0.2, 1);
}

  // PROJECTS
  #projects-tab {
    margin-top: 50px;
    display: grid;

    grid-template-columns: 1fr 1fr;
    //grid-template-columns: repeat(2, 200px);
    grid-gap: 10px;

    place-content: center;
    justify-items: center;

    button {
      color: var(--text-color);
      background: var(--purple-color);

      width: 25vw;
      height: 25vh;
      //width: 150px;
      //height: 100px;

      margin-bottom: 30px;

      font-size: 1.5rem;
      border-radius: 30px;

      transition: var(--transition);

      &:hover {
        background: var(--text-color);
        color: var(--dark);
      }
    }
  }

  .projects {
    .project {
      background: var(--dark-color);

      height: 60vh;

      padding: 25px;
      margin: 25px;

      border: 1px dashed var(--text-color);
      border-radius: 30px;

      display: flex;

      .left {
        width: 50vw;

        img {
          width: 50vw;
          height: 50vh;

          border-radius: 40px;
          object-fit: cover;
        }
      }

      .right {
        width: 50vw;
        padding: 20px;

        h2 {
          margin-bottom: 15px;
          text-align: center;
        }

        .desc {
          font-size: 1.2rem;

          a {
            color: var(--pastel-color-2);
          }
        }

        .languages {
          margin: 10px;
          text-align: center;

          i {
            //color: var(--text-color);
            font-size: 2.5rem;
          }
        }

        .live-code {
          justify-content: center;
          text-align: center;

          button {
            &:last-child {
              margin-left: 10px;
            }

            background: var(--purple-color);
            //background: var(--pastel-color);

            width: 45%;
            height: 30px;

            font-size: 1.2rem;

            a {
              color: var(--text-color);

            }
          }
        }
      }
    }
  }

  // CONTACT FORM
  #contact-form {
    display: grid;
    justify-content: center !important;

    form {
      background-color: var(--dark-color);
      //background-color: var(--dark);

      width: 50vw;
      padding: 25px;

      margin: 25px;
      margin-bottom: 12vh;

      border: 1px dashed var(--text-color);
      border-radius: 30px;

      label {
        font-size: 1.2rem;
      }

      input {
        width: 100%;
        height: 40px;

        margin: 10px;
        border-radius: 25px;
      }

      textarea {
        width: 100%;
        margin: 10px;
        border-radius: 25px;

        resize: none;
      }

      button {
        color: var(--text-color);
        background: var(--main-gradient);
        border: 1px solid var(--pastel-color);

        width: 70%;
        height: 8vh;

        margin-left: 15%;
        border-radius: 30px;

        font-size: 1.5rem;
      }
    }
  }

  // SOCIALS SECTION
  /*#socials {
    //background: var(--purple-color);

    ul {
      display: grid;

      grid-template-columns: repeat(3, 200px);
      grid-gap: 10px;

      place-content: center;
      justify-items: center;

      li {
        //background-color: var(--pastel-color-1);

        margin: 10px;
        padding: 15px;

        border: 1px dashed var(--text-color);
        border-radius: 25px;

        transition: var(--transition);

        a {
          color: var(--text-color);

          i {
            font-size: 4rem;
          }
        }

        &:hover {
          padding: 10px;
        }
      }
    }
  }*/
 
  #socials {
  //columns: 3;
  //column-gap: 200px;

  padding: 30px;
  //margin-bottom: 5vh;

    ul {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      //grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
      place-items: center;

      li {
        background-color: var(--dark-color);

        width: 10rem;
        height: 15vh;

        margin-bottom: 5%;

        border-radius: 20px;
        border: 1px solid var(--pastel-color-2);

        text-align: center;

        &:hover {
          transform: var(--transform);
          transition: var(--transition);
        }

        .fas,
        .fa-brands {
          font-size: 3rem;
        }

        a {
          i {
            color: var(--text-color); //#fffafa

            font-size: 1.3rem;
            text-decoration: none;

            padding: 15px;
            margin-bottom: 5vh;
          }
        }
      }
    }
  }
}

@media screen and (min-width: 769px) {
  .section {
    .division {
     .left {
        img {
          width: 30vw !important;
          height: 60vh !important;
          //width: 90%;
          //height: 50%;
        }
      }
    }
  }
}

@media screen and (max-width: 900px) {
  .section {
    // ABOUT SECTION
    .division {
      padding-top: 0;
      display: block;

      .left,
      .right {
        width: 100%;
      }

      .left {
        img {      
          width: 50vw !important;
          height: 90vw !important;
          //width: 100%;
          //height: 50vh !important;

          justify-self: center !important;
        }
      }

      .right {
        font-size: 1.5rem;

        p {
          line-height: 50px;
        }
      }
    }
  }
}

@media screen and (max-width: 768px) {
  #navigations {
    grid-template-columns: repeat(2, 200px);
  }

  .section {
    box-shadow: inset 0 0 0 10px var(--purple-color);

    .top {
      height: 10vh;
      padding: 20px 50px;

      h1 {
        font-size: 1.8rem;
      }

      span {
        font-size: 2rem;
      }
    }
    
    // EXPERIENCE SECTION
    #experiences {
      padding: 5px 10px !important;
      
      .experience {
        margin: 10px !important;
        padding: 10px !important;
      }
    }
    
    // TECH STACK SECTION
    #tech-stack {
      ul {
        grid-template-columns: 1fr 1fr 1fr !important;
      }
    }
    
    // PROJECT SECTION
    .projects {
      .project {
        width: 90% !important;
        height: 90vh !important;
        display: grid !important;
        
        .left {
          width: 100% !important;
          
          img {
            width: 100% !important;
            height: 30vh !important;
          }
        }
        
        .right {
          width: 100% !important;
          padding: 0 !important;
          
          h2 {
            margin-bottom: 5px !important;
          }
          
          .desc {
            font-size: 1.5rem !important;
          }
          
          .languages {
            margin: 5px !important;
            
            i {
              font-size: 3rem !important;
            }
          }
    
          .live-code {
            button {
              font-size: 1.5rem;
              height: 40px;
            }
          }
        }
      }
    }
    
    // CONTACT SECTION  
    #contact-form {
      justify-content: left;
      display: block;
      
      form {
        width: 80vw !important;
        margin: 0;
        margin-left: 5.3vw;
        margin-bottom: 12vh;
        
        label {
          font-size: 1.3rem;
        }
          
        input {
          height: 35px;
        }
      }
    }
            
    // SOCIALS
    #socials {
      ul {
        grid-template-columns: 1fr 1fr;
        //grid-template-columns: repeat(2, 200px) !important;
      }
    }
  }
}

@media screen and (max-width: 600px) {
  .section {
    // TECH STACK SECTION
    #tech-stack {
      padding: 15px;
      
      ul {
        grid-template-columns: 1fr 1fr !important;
        gap: 10px;
      }
    }
    
  // CONTACT SECTION  
  #contact-form {
    padding-top: 30px !important;
  }
  
  // SOCIALS SECTION  
  /*#socials {
    grid-template-columns: 1fr 1fr !important;
    }*/
  }
}

@media screen and (max-width: 500px) {
  #navigations {
    grid-template-columns: repeat(2, 170px);
  }

  .section {
    box-shadow: inset 0 0 0 7px var(--purple-color);

    .top {
      height: 8vh;
      padding: 20px 50px;

      h1 {
        font-size: 1.5rem;
      }

      span {
        font-size: 1.8rem;
      }
    }

    // PROJECTS
    #projects-tab {
      padding-top: 15px;
      //display: block;

      button {
        width: 30vw;
        height: 20vh;
        margin-left: 6%;
        margin-bottom: 50px;
        
        font-size: 1.25rem;
      }
    }

    // PROJECT SECTION
    .projects {
      .project {
        
        .right {
          .desc {
            font-size: 1.2rem !important;
          }
          
          .languages {
            i {
              font-size: 2.5rem !important;
            }
          }
    
          .live-code {
            button {
              font-size: 1.2rem;
            }
          }
        }
      }
    }

    // SOCIALS
    /*#socials {
      ul {
        grid-template-columns: repeat(2, 170px) !important;
      }
    }*/
  }
}


@media screen and (max-width: 400px) {
  .section {
  // TECH STACK SECTION
    #tech-stack {
      ul {
        grid-template-columns: 1fr !important;
      }
    }
  }

  // TIMELINE EXPERIENCE
  .experience-page {
    .categories {
      overflow-x: scroll;
    }
  }

  #socials {
    ul {
      li {
        width: 7rem;
        height: 13vh;
        padding: 5px;

        .fas,
        .fa-brands {
            font-size: 2.5rem;
        }

        a {
          i {
            font-size: 1.2rem;
          }
        }
      }
    }
  }
}

@media screen and (max-width: 420px) {
  // SOCIALS
  #socials {
    ul {
      /*grid-template-columns: repeat(2, 100px) !important;
      grid-gap: 5px;*/

      li {
        a {
          i {
            font-size: 3rem !important;
          }
        }
      }
    }
  }
}

@media screen and (max-width: 350px) {
  #intro {
    margin: 2rem;
  }

  #navigations {
    grid-template-columns: repeat(2, 150px);
    grid-gap: 10px;

    .nav {
      width: 120px;
      height: 120px;

      margin-bottom: 50px;

      img {
        width: 120px;
        height: 120px;
      }
    }
  }
  
  .section {
    box-shadow: inset 0 0 0 5px var(--purple-color);

    .top {
      height: 8vh;
      padding: 10px 30px;

      h1 {
        font-size: 1.3rem;
      }

      span {
        font-size: 1.6rem;
      }
    }

    // PROJECT SECTION
    .projects {
      .project { 
        .right {
          h2 {
            font-size: 1.3rem;
          }

          .desc {
            font-size: 1rem !important;
          }
          
          /*.languages {
            i {
              font-size: 1.3rem !important;
            }
          }*/
    
          .live-code {
            button {
              font-size: 1rem;
              height: 25px !important;
            }
          }
        }
      }
    }
  }
}

/*
@media screen and (max-width: 400px) {
  #socials {
    ul {
      li {
        width: 7rem;
        height: 13vh;
        padding: 5px;

        .fas,
        .fa-brands {
            font-size: 2.5rem;
        }

        a {
          i {
            font-size: 1.2rem;
          }
        }
      }
    }
  }
}
*/

@media screen and (max-width: 330px) {
  #socials {
    grid-template-columns: 1fr !important;
  }
}

@media screen and (max-width: 300px) {
  .section {
  // PROJECT SECTION
    .projects {
      .project { 
        width: 95% !important;
        padding: 10px;
        margin: 10px;
      }
    }
  }
}

@media screen and (max-width: 280px) {
  #intro {
    margin: 1rem;
  }
}

/*@media screen and (max-width: 400px) {
  // CONTACT FORM
  #contact-form {
    form {
      button {
        width: 50%;
        height: 7vh;

        font-size: 1.3rem;
      }
    }
  }
}*/
</style>
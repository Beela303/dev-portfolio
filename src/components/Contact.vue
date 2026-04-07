<template>
  <div id="contact">
    <h2>Contact Me</h2>
    <p>Have a Beautiful design that you'd like to come to life? Send an e-mail and let's talk.</p>
    <p>E-Mail: <a href="mailto:nabilaabubakar333@gmail.com">nabilaabubakar333@gmail.com</a></p>

    <h3>Socials:</h3>
    <a href="http://github.com/beela303" target="_blank" rel="noopener noreferrer">GitHub</a>
    <a href="http://linkedin.com/in/nabilaabubakar" target="_blank" rel="noopener noreferrer">LinkedIn</a>
    <a href="http://instagram.com/beela303" target="_blank" rel="noopener noreferrer">Instagram</a>
    <a href="http://x.com/beela303" target="_blank" rel="noopener noreferrer">X/Twitter</a>
  </div>
</template>

<style lang="scss" scoped>
#contact {
  height: 100vh;
  font-size: 2.5rem;

  display: grid;

  h2 {
    font-size: 4rem;
    text-align: center;
  }

  a {
    color: var(--pastel-color);

    &:hover {
      color: var(--pastel-color-2);
    }
  }
}

@media screen and (max-width: 600px) {
  #contact {
    font-size: 2rem;

    h2 {
      font-size: 3rem;
    }
  }
}

@media screen and (max-width: 500px) {
  #contact {
    font-size: 1.8rem;

    h2 {
      font-size: 2.5rem;
    }
  }
}

@media screen and (max-width: 430px) {
  #contact {
    font-size: 1.5rem;
  }
}
</style>
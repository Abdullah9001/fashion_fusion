<template>
  <section id="hero">
    <div class="container">
      <img src="hero.png" alt="hero page image" />
      <div class="hero-text">
        <h1 class="heading">
          Welcome to Our <br />
          <span> E-Commerce</span> Store
        </h1>
        <p class="para">Discover amazing products and shop with confidence.</p>
        <a href="/products" class="btn">Shop Now</a>
      </div>
    </div>
  </section>
</template>

<style scoped>
#hero {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 90vh;
}

.heading {
  font-size: 3rem;
  color: #1eb8b8;
  font-family: 'Rubik', sans-serif;
  font-weight: 300;
  padding-bottom: 0.6rem;
}
span {
  color: #fff;
}

.para {
  color: #fff;
  font-family: 'Rubik', sans-serif;
  letter-spacing: 3px;
  margin-bottom: 1.5rem;
}
.btn {
  text-decoration: none;
  text-transform: uppercase;
  font-size: 1.2rem;
  font-family: 'Belanosima', sans-serif;
  padding: 0.5rem 1rem;
  background-color: #ffffff;
  border-radius: 5px;
  font-weight: bold;
  color: black;
  border: 1px solid #fff;
  transition: 1s;
}

.btn:hover {
  background: #13cfcf;
  background: repeating-radial-gradient(
    circle farthest-corner at center center,
    #13cfcf 0%,
    #cf87a8 100%
  );
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.container {
  margin: 0 40px;

  display: flex;
  flex-direction: row-reverse;
  justify-content: space-around;
  align-items: center;
}

img {
  height: 590px;
  width: auto;
  object-fit: cover;
  filter: drop-shadow(17px 36px 9px #000);
}

/* Media queries */

@media (max-width: 1100px) {
  .hero-text h1 {
    font-size: 2rem;
  }
  img {
    height: 400px;
    width: auto;
    object-fit: cover;
  }
}

@media (max-width: 884px) {
  .container {
    margin-top: 10px;
    flex-direction: column;
  }
  img {
    display: none;
  }
  .hero-text {
    width: 100%;
    text-align: center;
  }
  .hero-text h1 {
    font-size: 3rem;
  }
}

@media (max-width: 678px) {
  .hero-text h1 {
    font-size: 2.5rem;
  }
}
</style>

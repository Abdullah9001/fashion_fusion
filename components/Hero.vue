<template>
  <section id="hero">
    <div class="hero-content">
      <h1 class="heading">
        Welcome to Our <br />
        <span> E-Commerce</span> Store
      </h1>
      <p class="para">Discover amazing products and shop with confidence.</p>
      <a href="/shop" class="btn">Shop Now</a>
    </div>
    <div class="image">
      <img src="hero.png" alt="hero page image" />
    </div>
  </section>
</template>

<style scoped>
#hero {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 90vh;
  padding: 4rem;
}

.heading {
  font-size: 3rem;
  color: #079992;
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
  /* -webkit-text-fill-color: transparent; */
}

img {
  height: 592px;
  width: auto;
  object-fit: cover;
}
</style>

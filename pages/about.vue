<template>
  <div class="about">
    <div class="head">
      <h1>About Us</h1>
    </div>
    <div class="about-section">
      <div class="about-details">
        <h1>Welcome To Our Website</h1>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Natus dicta
          architecto eligendi illo nulla corrupti illum vel, tenetur ut! Tempora
          laudantium, veniam cupiditate libero optio ad sapiente, voluptas hic
          suscipit aspernatur reprehenderit dignissimos cumque unde earum esse
          iste officia nulla? Illo voluptates assumenda modi rerum,
        </p>
        <NuxtLink to="/products">Product</NuxtLink>
      </div>
      <div class="about-img">
        <img src="about.jpg" alt="about image" />
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.about {
  padding: 4rem;
}

.head {
  display: flex;
  text-align: center;
  align-items: center;
  justify-content: center;
}

.head h1 {
  color: #fff;
  font-size: 2.3rem;
  font-family: 'Rubik', sans-serif;
  padding-bottom: 10px;
  border-bottom: 2px solid #fff;
  margin-bottom: 2rem;
}

.about-section {
  padding: 2rem;
  display: flex;
}

.about-details {
  margin-right: 2rem;
}
.about-details h1 {
  color: #fff;
  font-family: 'Rubik', sans-serif;
  padding: 20px 0;
}
.about-details p {
  color: #fff;
  font-family: 'Rubik', sans-serif;
  margin-bottom: 20px;
  line-height: 30px;
}
a {
  padding: 10px 20px;
  margin: 1rem 0;
  font-family: 'Rubik', sans-serif;
  cursor: pointer;
  border: 1px solid #fff;
  color: #fff;
  text-decoration: none;
}
img {
  width: 500px;
}

@media (max-width: 1000px) {
  .about {
    padding: 1rem;
  }
  .about-section {
    display: flex;
    flex-direction: column;
    text-align: center;
    align-items: center;
    justify-content: center;
  }
  .about-details {
    margin-bottom: 2rem;
  }
  img {
    width: 400px;
  }
}
</style>

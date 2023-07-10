<template>
  <div class="news">
    <div class="news-text">
      <h1>News Letter</h1>
      <p>Subscribe to receive discount & mores</p>
      <input type="text" placeholder=" Email" />
      <button>Subscribe</button>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.news {
  padding: 2rem 5.5rem;
}
.news-text {
  display: flex;
  flex-direction: column;
  text-align: center;
  justify-content: center;
  align-items: center;
  padding: 3rem;
  border: 2px solid #4897;
}

h1 {
  color: #fff;
  font-size: 2rem;
  font-family: 'Rubik', sans-serif;
  margin-bottom: 1rem;
}

p {
  color: #fff;
  font-family: 'Rubik', sans-serif;
  margin-bottom: 1rem;
}

input {
  height: 50px;
  width: 400px;
  padding-left: 10px;
  font-family: 'Rubik', sans-serif;
  color: black;
  font-weight: bold;
  margin-bottom: 1rem;
  border: none;
  border-radius: 5px;
  outline: none;
}

button {
  height: 50px;
  width: 400px;
  font-family: 'Rubik', sans-serif;
  color: black;
  font-weight: bold;
  cursor: pointer;
  margin-bottom: 1rem;
  border: none;
  border-radius: 5px;
}

@media (max-width: 678px) {
  input {
    height: 40px;
    width: 250px;
  }

  button {
    height: 40px;
    width: 250px;
  }
}
</style>

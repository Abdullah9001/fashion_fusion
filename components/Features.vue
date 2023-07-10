<template>
  <div>
    <div class="features-text">
      <h1>Our Features</h1>
    </div>
    <div class="cardd">
      <div class="card-contentt">
        <img src="features/f1.png" />
        <h6 class="f-1">Free Shipping</h6>
      </div>
      <div class="card-contentt">
        <img src="features/f2.png" />
        <h6 class="f-2">Online Order</h6>
      </div>
      <div class="card-contentt">
        <img src="features/f3.png" />
        <h6 class="f-3">Save Money</h6>
      </div>
      <div class="card-contentt">
        <img src="features/f4.png" />
        <h6 class="f-4">Promotions</h6>
      </div>
      <div class="card-contentt">
        <img src="features/f5.png" />
        <h6 class="f-5">Happy Sell</h6>
      </div>
      <div class="card-contentt">
        <img src="features/f6.png" />
        <h6 class="f-6">F24/7 Suport</h6>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.features-text {
  display: flex;
  flex-direction: column;
  text-align: center;
  justify-content: center;
  align-items: center;
}

h1 {
  color: #fff;
  font-size: 2rem;
  font-family: 'Rubik', sans-serif;
}
.cardd {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  margin-top: 1rem;
  padding: 0 4rem;
}

.card-contentt {
  height: 170px;
  width: 150px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin: 1rem;
  background-color: aliceblue;
  padding: 10px;
  border: 1px solid #e0dfdf;
}
h6 {
  font-family: 'Rubik', sans-serif;
  font-weight: bold;
  margin-top: 10px;
  padding: 5px;
  border-radius: 5px;
  cursor: pointer;
  color: #242222;
}

.f-1 {
  background-color: #8eeae7;
}
.f-2 {
  background-color: #ebacd9;
}
.f-3 {
  background-color: #adf0a0;
}
.f-4 {
  background-color: #8ecaea;
}
.f-5 {
  background-color: #bda2db;
}
.f-6 {
  background-color: #d9bfb5;
}
</style>

<template>
  <div class="footer">
    <div class="footer-title">
      <h1>Fashion Fusion</h1>
    </div>
    <div class="footer-icon">
      <div class="icon" v-for="icon in icons" :key="icon">
        <img class="footer-img" :src="`${icon.src}`" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      icons: [
        {
          src: 'facebook-f.svg',
        },
        { src: 'twitter.svg' },
        { src: 'github.svg' },
        { src: 'square-instagram.svg' },
      ],
    }
  },
}
</script>

<style scoped>
.footer {
  display: flex;
  flex-direction: column;
  text-align: center;
  align-items: center;
  justify-content: center;
  margin: auto;
  background-color: #000000;
}
h1 {
  background: #13cfcf;
  background: repeating-radial-gradient(
    circle farthest-corner at center center,
    #13cfcf 0%,
    #cf87a8 100%
  );
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  font-family: 'Belanosima', sans-serif;
  font-size: 1.5rem;
  padding: 1rem;
}
.icon {
  padding: 6px;
  margin: 6px;
  background-color: rgb(255, 255, 255);
  border-radius: 50%;
}

.footer-icon {
  display: flex;
  text-align: center;
  align-items: center;
  justify-content: center;
}
.footer-img {
  width: 20px;
  height: 15px;
}
</style>

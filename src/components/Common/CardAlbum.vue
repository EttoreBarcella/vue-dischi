<template>
  <div class="card">
      <img :src="album.poster" :alt="album.title">
      <h3>{{album.title}}</h3>
      <p>{{album.author}}</p>
      <p>{{album.year}}</p>
  </div>
</template>

<script>
export default {
    name:"CardAlbum",
    props: {
        album: Object,
    }
}
</script>

<style lang="scss" scoped>
.card{
    background-color: var(--primary-color);
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: .625rem;
    width: 300px;
    h3{
        text-transform: uppercase;
        padding-bottom: 1.5625rem;
        font-weight: bold;
        font-size: 1.75rem;
    }
    img{
        width: 200px;
        padding: 20px;
    }
    p{
        line-height: 5px;
        color: gray;
        font-size: small;
    }
}
</style>
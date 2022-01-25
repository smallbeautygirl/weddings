<template>
  <section class="page-section bg-light" id="video">
    <div class="text-center">
      <h2 class="section-heading text-uppercase">婚紗花絮影片</h2>
      <!-- <h3 class="section-subheading text-muted">
        Lorem ipsum dolor sit amet consectetur.
      </h3> -->
    </div>
    <v-container class="d-flex justify-center">
      <iframe
        width="560"
        height="315"
        src="https://www.youtube.com/embed/vmDn0KFtaYQ"
        title="YouTube video player"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen
      ></iframe>
    </v-container>
    <!-- <div class="author">
      Made By 漂亮表姊
      <img
        :src="require('@/assets/img/celebration.png')"
      />
    </div> -->
  </section>
</template>

<style scoped>
.author {
  font-family: "Architects Daughter", cursive;
  background-color: blanchedalmond;
  font-weight: bold;
  text-align: center;
  font-size: 1.5rem;
  margin-left: 50rem;
  margin-right: 50rem;
  display: flex;
}
img {
  border-radius: 8px;
  height: 20%;
  width: 20%;
}
</style>

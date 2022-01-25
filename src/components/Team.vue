<template>
  <section class="page-section" id="team">
    <div class="container">
      <div class="text-center">
        <h2 class="section-heading text-uppercase">Our Amazing Team</h2>
        <!-- <h3 class="section-subheading text-muted">
          Lorem ipsum dolor sit amet consectetur.
        </h3> -->
      </div>
      <div class="row">
        <div class="col-lg-3">
          <div class="team-member">
            <img
              class="mx-auto rounded-circle"
              :src="require('@/assets/img/team/flower-2.png')"
              alt="..."
            />
            <h4>樊小花</h4>
            <p class="text-muted">Pet NO1</p>
            <a
              class="btn btn-social mx-2"
              target="blank"
              href="https://instagram.com/little_flower0520?utm_medium=copy_link"
              ><i class="fab fa-instagram fa-3x"></i
            ></a>
          </div>
        </div>
        <div class="col-lg-3">
          <div class="team-member">
            <img
              class="mx-auto rounded-circle"
              :src="require('@/assets/img/team/pudding-1.png')"
              alt="..."
            />
            <h4>樊布丁</h4>
            <p class="text-muted">Pet NO2</p>
            <a
              class="btn btn-social mx-2"
              target="blank"
              href="https://instagram.com/little_flower0520?utm_medium=copy_link"
              ><i class="fab fa-instagram fa-3x"></i
            ></a>
          </div>
        </div>
        <div class="col-lg-3">
          <div class="team-member">
            <img
              class="mx-auto rounded-circle"
              :src="require('@/assets/img/team/vivian-2.png')"
              alt="..."
            />
            <h4>樊紹萱</h4>
            <p class="text-muted">Bride</p>
            <a class="btn btn-social mx-2" href="mailto:a0970318352@gmail.com">
              <i class="fas fa-envelope fa-3x"></i>
            </a>
          </div>
        </div>
        <div class="col-lg-3">
          <div class="team-member">
            <img
              class="mx-auto rounded-circle"
              :src="require('@/assets/img/team/penguin.png')"
              alt="..."
            />
            <h4>林俊銓</h4>
            <p class="text-muted">Bridegroom</p>
            <a
              class="btn btn-social mx-2"
              href="mailto:gogopenguin1995@gmail.com"
            >
              <i class="fas fa-envelope fa-3x"></i>
            </a>
          </div>
        </div>
      </div>
      <!-- <div class="row">
        <div class="col-lg-8 mx-auto text-center">
          <p class="large text-muted">
            Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aut eaque,
            laboriosam veritatis, quos non quis ad perspiciatis, totam corporis
            ea, alias ut unde.
          </p>
        </div>
      </div> -->
    </div>
  </section>
</template>

<style scoped>
.section-heading {
  font-family: "Architects Daughter", cursive;
}
.social-media {
  font-family: "Architects Daughter", cursive;
}
.btn-social:hover {
  color: #fff;
  /* background-color: #d9aa00; */
  /* border-color: #cca000; */
}
</style>

<template>
  <div id="carouselExampleControls" class="carousel slide" data-ride="carousel">
    <ol class="carousel-indicators">
      <li
        data-target="#carouselExampleControls"
        data-slide-to="0"
        class="active"
      ></li>
      <li data-target="#carouselExampleControls" data-slide-to="1"></li>
      <li data-target="#carouselExampleControls" data-slide-to="2"></li>
    </ol>
    <div class="carousel-inner bandar">
      <div class="carousel-item active">
        <img
          class="d-block w-60 m-auto"
          src="@/assets/carousel/pexels-simon-migaj-747470.jpg"
          alt="First slide"
        />
        <div class="carousel-caption d-none d-md-block">
          <h5>Red Jacket</h5>
          <p>Photo by Simon Migaj from Pexels</p>
        </div>
      </div>
      <div class="carousel-item">
        <img
          class="d-block w-60 m-auto"
          src="@/assets/carousel/pexels-sindre-strøm-1040945.jpg"
          alt="Second slide"
        />
        <div class="carousel-caption d-none d-md-block">
          <h5>Blue Denim Jacket</h5>
          <p>Photo by Sindre Strøm from Pexels</p>
        </div>
      </div>
      <div class="carousel-item">
        <img
          class="d-block w-60 m-auto"
          src="@/assets/carousel/pexels-lisa-fotios-1476055.jpg"
          alt="Third slide"
        />
        <div class="carousel-caption d-none d-md-block text-dark">
          <h5>Blue Top</h5>
          <p>Photo by Anj Namoro from Pexels</p>
        </div>
      </div>
    </div>
    <a
      class="carousel-control-prev"
      href="#carouselExampleControls"
      role="button"
      data-slide="prev"
    >
      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
      <span class="sr-only">Previous</span>
    </a>
    <a
      class="carousel-control-next"
      href="#carouselExampleControls"
      role="button"
      data-slide="next"
    >
      <span class="carousel-control-next-icon" aria-hidden="true"></span>
      <span class="sr-only">Next</span>
    </a>
  </div>
</template>

<script>
// Photo by Sindre Strøm from Pexels no 2
// Photo by Simon Migaj from Pexels no 1
// Photo by Lisa Fotios from Pexels no 3
export default {}
</script>

<style scoped>
img {
  width: 60%;
  /* max-height: 1000px; */
}

.bandar {
  background-color: rgba(42, 37, 37, 0.548);
}

.carousel-control-prev-icon,
.carousel-control-next-icon {
  height: 100px;
  width: 100px;
  background-size: 100%, 100%;
}
</style>

<template>
  <div>
    <!-- The social media icon bar -->
    <div class="icon-bar">
      <a href="#" class="facebook"><i class="fa fa-facebook"></i></a>
      <a href="#" class="twitter"><i class="fa fa-twitter"></i></a>
      <a href="#" class="instagram"><i class="fa fa-instagram"></i></a>
      <a href="#" class="youtube"><i class="fa fa-youtube"></i></a>
    </div>
    <a href="https://icons8.com/icon/83361/help">Help icon by Icons8</a>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
/* Fixed/sticky icon bar (vertically aligned 50% from the top of the screen) */
.icon-bar {
  position: fixed;
  top: 50%;
  right: 0%;
  -webkit-transform: translateY(-50%);
  -ms-transform: translateY(-50%);
  transform: translateY(-50%);
}

/* Style the icon bar links */
.icon-bar a {
  display: block;
  text-align: center;
  padding: 16px;
  transition: all 0.3s ease;
  color: white;
  font-size: 20px;
}

/* Style the social media icons with color, if you want */
.icon-bar a:hover {
  background-color: #000;
}

.facebook {
  background: #3b5998;
  color: white;
}

.twitter {
  background: #55acee;
  color: white;
}

.instagram {
  background: #c73882;
  color: white;
}
.youtube {
  background: #bb0000;
  color: white;
}
</style>

<template>
  <div class="p-5">
    <!-- The social media icon bar -->
    <div class="icon-bar">
      <a href="#" class="facebook"><i class="fa fa-facebook"></i></a>
      <a href="#" class="twitter"><i class="fa fa-twitter"></i></a>
      <a href="#" class="instagram"><i class="fa fa-instagram"></i></a>
      <a href="#" class="email"><i class="fa fa-envelope"></i></a>
    </div>
    <div class="carouselContainer">
      <div class="filter">
        <a @click="toggleFilter" href="#" class="email"
          ><i class="fa fa-filter"></i
        ></a>
      </div>
      <Carousal />
    </div>
    <a class="thanks" href="https://icons8.com/icon/83361/help"
      >Help icon by Icons8</a
    >
    <FilterModal v-if="filterOpen" @close="filterOpen = false" />
  </div>
</template>

<script>
import Carousal from '@/components/Carousal.vue'
import FilterModal from '@/components/FilterModal.vue'
export default {
  data() {
    return {
      filterOpen: false
    }
  },
  components: {
    Carousal,
    FilterModal
  },
  methods: {
    toggleFilter() {
      this.filterOpen = !this.filterOpen
    }
  }
}
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
  font-size: 30px;
}

.filter a:hover {
  background-color: #000;
}

.filter {
  position: fixed;
  top: 50%;
  left: 0%;
  -webkit-transform: translateY(-50%);
  -ms-transform: translateY(-50%);
  transform: translateY(-50%);
}

.filter a {
  display: block;
  text-align: center;
  padding: 16px;
  transition: all 0.3s ease;
  color: white;
  font-size: 30px;
}

/* Style the social media icons with color, if you want */
.icon-bar a:hover {
  background-color: #000;
}

.facebook {
  background: #3b5998;
  color: white;
}

.email {
  background: rgb(49, 46, 46);
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

.thanks {
  position: fixed;
  bottom: 0%;
  right: 50%;
  -webkit-transform: translateY(-50%);
  -ms-transform: translateY(-50%);
  transform: translateY(-50%);
}

.carouselContainer {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  width: 65vw;
  height: auto;
  margin: auto;
}
</style>

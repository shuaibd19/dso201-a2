<template>
  <div>
    <Keypress key-event="keyup" :key-code="72" @success="toggleModal" />
    <Keypress key-event="keyup" :key-code="27" @success="isOpen = false" />
    <Keypress key-event="keyup" :key-code="83" @success="toggleSearch" />
    <nav class="navbar navbar-light justify-content-between nsg">
      <a @click="toggleModal" href="#" class="miz">
        <img src="https://img.icons8.com/material/50/000000/help--v2.png" />
        <Accessability />
      </a>
      <a class="navbar-brand">
        <img class="logo" src="@/assets/brand.svg" alt="shuaibs_Shop" />
      </a>
      <form class="form-inline">
        <input
          class="form-control mr-sm-2"
          type="search"
          placeholder="Search"
          aria-label="Search"
        />
        <button class="btn btn-warning my-2 my-sm-0" type="submit">
          Search
        </button>
        <a class="navbar-brand" href="#">
          <img
            src="https://img.icons8.com/windows/48/000000/shopping-bag.png"
          />
        </a>
      </form>
    </nav>
    <Modal v-if="isOpen" @close="isOpen = false" />
    <SearchModal v-if="searchOpen" @close="searchOpen = false" />
  </div>
</template>

<script>
import Accessability from '@/components/Accessability.vue'
import Modal from '@/components/Modal.vue'
import SearchModal from '@/components/SearchModal.vue'
export default {
  data() {
    return {
      isOpen: false,
      searchOpen: false
    }
  },
  components: {
    Accessability,
    Modal,
    SearchModal,
    Keypress: () => import('vue-keypress')
  },
  methods: {
    toggleModal() {
      if (this.searchOpen) {
        this.searchOpen = !this.searchOpen
      }
      this.isOpen = !this.isOpen
      console.log('Your pressed h!')
    },
    toggleSearch() {
      if (this.isOpen) {
        this.isOpen = !this.isOpen
      }
      this.searchOpen = !this.searchOpen
      console.log('Your pressed s!')
      // added functionality in the future includes allowing customer to type
      // in the search area without triggering the global key press
    }
  }
}
</script>

<style scoped>
.miz {
  text-decoration: none;
}
.logo {
  height: 5.5rem;
  /* max-height: 100px; */
}

.nsg {
  background: rgb(7, 125, 141);
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}
</style>

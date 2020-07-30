<template>
  <div>
    <nav class="navbar navbar-light justify-content-between nsg">
      <a
        href="#"
        class="miz"
        data-toggle="modal"
        data-target="#exampleModalCenter"
        @keyup.65="doSomething"
      >
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
    <div
      class="modal fade"
      id="exampleModalCenter"
      tabindex="-1"
      role="dialog"
      aria-labelledby="exampleModalCenterTitle"
      aria-hidden="true"
    >
      <div class="modal-dialog modal-dialog-centered" role="document">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="exampleModalLongTitle">Modal title</h5>
            <button
              type="button"
              class="close"
              data-dismiss="modal"
              aria-label="Close"
            >
              <span aria-hidden="true">&times;</span>
            </button>
          </div>
          <div class="modal-body">
            ...
          </div>
          <div class="modal-footer">
            <button
              type="button"
              class="btn btn-secondary"
              data-dismiss="modal"
            >
              Close
            </button>
            <button type="button" class="btn btn-primary">Save changes</button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Accessability from '@/components/Accessability.vue'
export default {
  components: {
    Accessability
  },
  methods: {
    doSomething() {
      console.log('Your pressed a!')
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

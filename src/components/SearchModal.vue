<template>
  <transition name="modal">
    <div class="modal-mask">
      <div class="content-inside">
        <form class="form-inline ">
          <input
            class="form-control form-control-lg mr-sm-2"
            type="search"
            placeholder="Search"
            aria-label="Search"
          />
          <button class="btn btn-warning my-2 my-sm-0" type="submit">
            Search
          </button>
        </form>
      </div>
    </div>
  </transition>
</template>

<script>
export default {}
</script>

<style scoped>
.modal-mask {
  position: fixed;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 9997;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  background-color: rgba(80, 75, 75, 0.712);
  transition: opacity 0.3s ease;
}

.content-inside {
  background-color: white;
  display: flex;
  flex-direction: row;
  height: auto;
  width: 100%;
  height: 10%;
  justify-content: center;
  align-items: center;
}

.modal-enter {
  opacity: 0;
}

.modal-leave-active {
  opacity: 0;
}

.modal-enter .modal-container,
.modal-leave-active .modal-container {
  -webkit-transform: scale(1.1);
  transform: scale(1.1);
}
</style>

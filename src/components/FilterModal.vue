<template>
  <transition name="modal">
    <div class="modal-mask">
      <div class="content-inside">
        <a href="#">Price Range</a>
        <a href="#">Brand</a>
        <a href="#">Colour</a>
        <a href="#">Material</a>
        <a href="#">Sale</a>
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
  justify-content: start;
  align-items: flex-start;
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
  flex-direction: column;
  height: auto;
  width: 20%;
  height: 100%;
  justify-content: flex-start;
  align-items: center;
}

.content-inside a {
  width: 100%;
  height: 5%;
  background-color: rgb(7, 125, 141);
  font-size: 2em;
  color: white;
  text-decoration: none;
  border: solid white 5px;
  text-align: center;
  transition-duration: 0.4s;
}

.content-inside a:hover {
  background-color: black;
  border-left: solid rgb(223, 212, 212) 20px;
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

<template>
  <div>
    <transition name="modal">
      <div class="modal-mask">
        <div class="content-inside">
          <div class="lft-column">
            <div class="imageRow">
              <img src="@/assets/keyboard-shortcuts/h-help.png" alt="help" />
              <p>Help</p>
            </div>
            <div class="imageRow">
              <img src="@/assets/keyboard-shortcuts/s-search.png" alt="searh" />
              <p>Search</p>
            </div>
            <div class="imageRow">
              <img src="@/assets/keyboard-shortcuts/c-cart.png" alt="cart" />
              <p>Cart</p>
            </div>
            <div class="imageRow">
              <img
                src="@/assets/keyboard-shortcuts/f-filter.png"
                alt="filter"
              />
              <p>Filter Results</p>
            </div>
            <div class="imageRow">
              <img src="@/assets/keyboard-shortcuts/e-email.png" alt="email" />
              <p>Email</p>
            </div>
          </div>
          <div class="rght-column">
            <div class="imageRow">
              <img
                src="@/assets/keyboard-shortcuts/d-right.png"
                alt="swipe-right"
              />
              <p>Swipe Right</p>
            </div>
            <div class="imageRow">
              <img
                src="@/assets/keyboard-shortcuts/a-left.png"
                alt="swipe-left"
              />
              <p>Swipe Left</p>
            </div>
            <div class="imageRow">
              <img
                src="@/assets/keyboard-shortcuts/n-decrease text size.png"
                alt="decrease"
              />
              <p>Text Smaller</p>
            </div>
            <div class="imageRow">
              <img
                src="@/assets/keyboard-shortcuts/m-increase text size.png"
                alt="increase"
              />
              <p>Text Bigger</p>
            </div>
          </div>
        </div>
      </div>
    </transition>
  </div>
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
  z-index: 9998;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  background-color: rgba(80, 75, 75, 0.712);
  transition: opacity 0.3s ease;
}

.content-inside {
  background-color: rgb(235, 226, 213);
  display: flex;
  flex-direction: row;
  height: auto;
  width: 40vh;
}

.rght-column {
  /* background-color: cadetblue; */
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
  width: 50%;
  color: #5a3e10;
  font-weight: bold;
  padding: 5%;
}

.lft-column {
  /* background-color: cyan; */
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
  width: 50%;
  color: #5a3e10;
  font-weight: bold;
  padding: 5%;
}

.imageRow {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: flex-start;
  text-align: center;
  width: 100%;
}

img {
  height: 5vh;
}

p {
  margin-top: auto;
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

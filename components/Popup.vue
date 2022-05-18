<template>

  <div class="popup">
    <div class="popup-inner" >
      <v-card class="border-4 grid justify-items-center" color="#fcfcfc">
        <img id="imgcheck" src="@/static/check.png" height="250" width="250" />
        <v-card-title class="md:text-xl text-sm font-bold text-black">
		  <slot />
        </v-card-title>
      </v-card>
    </div>
  </div>
</template>

<script>
export default {
//   props: ["TogglePopup"],
props: {
    textt: {
      type: String,
      default: ''
    },
}
};
</script>

<style lang="scss" scoped>
.popup {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: 99;
  background-color: rgba(0, 0, 0, 0.2);

  display: flex;
  align-items: center;
  justify-content: center;

  .popup-inner {
    background: #fff;
    padding: 32px;
  }
#imgcheck{
	width: 120px;
    height: 100px;
    display: flex;
  align-items: center;
  justify-content: center;
  background: black;
}
}
</style>
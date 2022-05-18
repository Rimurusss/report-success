<template>

  <div class="popup">
    <div class="popup-inner" >
      <v-card id="pop2" class="border-4 grid justify-items-center" color="#fcfcfc">
        <img id="imgcheck" src="@/static/check.png" />
        <v-card-title class="md:text-xl text-sm font-bold text-black">
            <div class="text-s"><slot /></div>
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
@import url('https://fonts.googleapis.com/css2?family=Itim&display=swap');
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
    padding: 32px;
  }
.text-s{
  font-family: 'Itim', cursive;
  margin-top: 30px;
  margin-bottom: -50px;
}
#pop2{
  background:black;
  border-radius: 25px;
  padding: 80px;
}
#imgcheck{
	width: 150px;
  display: flex;
  // align-items: center;
  // justify-content: center;
  margin: auto;
  margin-top: -50px;
}
}
</style>
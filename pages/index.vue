<template>
  <main>
    <h1>Vue Popups</h1>
    <v-btn elevation="2" @click="() => TogglePopup('buttonTrigger')"
      >Open Popup</v-btn
    >
    <Popup
      v-if="popupTriggers.buttonTrigger"
      :TogglePopup="() => TogglePopup('buttonTrigger')"
    >
      <h2>ส่งรายงานเรียบร้อย</h2>
      
    </Popup>
  </main>
</template>

<script>
import { ref } from "@nuxtjs/composition-api";
import Popup from "~/components/Popup";

export default {
  setup() {
    const popupTriggers = ref({
      buttonTrigger: false,
    });


    const TogglePopup = (trigger) => {
      popupTriggers.value[trigger] = !popupTriggers.value[trigger];
      setTimeout(() => {
      popupTriggers.value.buttonTrigger = false;
    }, 5000);
    };

    

    return {
      Popup,
      popupTriggers,
      TogglePopup,
    };
  },
};
</script>

<style>
.Popup {
  width: 100%;
        height: auto;
        text-align: center;
}
#botton_p {
  margin-right: 1000px;
}
</style>
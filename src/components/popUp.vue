<template>
  <div class="popUp">
    <div class="inner_popUp">
      <slot />
      <h4>
        A link has been sent to your registered Mail-Id to reset the password
      </h4>
      <button class="closeAlert" @click="TooglePopUp()">OKAY</button>
    </div>
  </div>
</template>

<script>
export default {
  props: ["TogglePopUp"],
};
</script>
<style>
.popUp {
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
  text-align: center;
}
.inner_popUp {
  background: rgba(255, 255, 255, 0.75);
  padding: 32px;
  display: inline-block;
  width: 250px;
  align-content: center;
  justify-content: center;
  border-radius: 15px;
}
.closeAlert {
  width: 80px;
  height: 50px;
  background: linear-gradient(90deg, blue, rgb(49, 36, 109));
  color: white;
}
</style>

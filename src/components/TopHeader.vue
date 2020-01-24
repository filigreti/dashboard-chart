<template>
  <main class="top-header d-flex justify-content-between align-items-center">
    <img src="@/assets/Toggle.svg" alt="" />
    <div class="d-flex align-items-center">
      <img class="pr-4" src="@/assets/avatar.svg" alt="" />
      <div class="d-flex align-items-center">
        <div class="avatar-header">
          <div class="text-header">Bidemi Yusuf</div>
          <div class="text-small d-flex justify-content-end ">
            Executive
          </div>
        </div>

        <img class="triangle" src="@/assets/caret-down-solid.svg" alt="" />
      </div>
    </div>
  </main>
</template>

<script>
export default {};
</script>

<style scoped>
.text-header {
  font-size: 15px;
  font-weight: 600;
  line-height: 1.33;
  letter-spacing: normal;
  color: #000000;
}
.text-small {
  font-style: normal;
  line-height: 1.18;
  letter-spacing: normal;
  font-size: 11px;
  padding-top: 3px;
}
.avatar-header {
  padding-right: 8px;
}
.triangle {
  width: 11px;
}
</style>

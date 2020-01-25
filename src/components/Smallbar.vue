<template>
  <main
    class="side w-100  align-items-center justify-content-center d-flex flex-column "
  >
    <img class="fluids mt-2" src="@/assets/SVG/logo.svg" alt="" />
    <div class="router-links d-flex flex-column mm ">
      <router-link to="/" class="d-flex align-items-center bottom  btn-routes">
        <img src="@/assets/Home.svg" alt="" />
      </router-link>
      <router-link
        to="/budget"
        class="d-flex align-items-center bottom btn-routes"
      >
        <img src="@/assets/Requests.svg" alt="" />
      </router-link>
      <router-link to="/approval" class="d-flex align-items-center btn-routes">
        <img src="@/assets/Approval.svg" alt="" />
      </router-link>
    </div>
  </main>
</template>

<script>
export default {};
</script>

<style>
.side {
  padding: 1rem;
  font-family: 'Source Sans Pro', sans-serif;
  font-weight: 600;
  font-size: 15px;
}
.mm {
  margin-top: 48px;
}
.bottom {
  margin-bottom: 12px;
}
.btn-routes {
  padding: 11px;
}
.space {
  padding-left: 8px;
}
.fluids {
  height: 32px;
}
</style>

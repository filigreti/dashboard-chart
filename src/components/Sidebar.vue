<template>
  <main class="side w-100">
    <img class="img-fluid pl-2 mt-1" src="@/assets/Logo.svg" alt="" />
    <div class="router-links d-flex flex-column ">
      <router-link to="/" class="d-flex align-items-center bottom  btn-route">
        <img src="@/assets/Home.svg" alt="" />
        <div class="space">Dashboard</div>
      </router-link>
      <router-link
        to="/budget"
        class="d-flex align-items-center bottom btn-route"
      >
        <img src="@/assets/Requests.svg" alt="" />
        <div class="space">Budget</div>
      </router-link>
      <router-link to="/approval" class="d-flex align-items-center btn-route">
        <img src="@/assets/Approval.svg" alt="" />
        <div class="space">Approval</div>
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
.flex-column {
  margin-top: 48px;
}
.bottom {
  margin-bottom: 12px;
}
.btn-route {
  padding: 8px 0 8px 16px;
}
.space {
  padding-left: 8px;
}
</style>

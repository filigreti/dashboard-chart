<template>
  <main class="home">
    <div class="d-flex justify-content-between align-items-center">
      <h3 class="dashboard">Dashboard</h3>
      <div class="date">20 Dec 2019, Friday</div>
    </div>
    <div class="d-flex head-count">
      <div class="budget ">
        <div class="first-budget card-shadow">
          <div class="budget-header d-flex justify-content-between">
            <div class="d-flex align-items-center">
              <img src="@/assets/purple.svg" alt="" />
              <div class="status-heading">
                Total Annual CAPEX Budget
              </div>

              <b-button class="ml-3 purp p-1 px-3" size="sm"
                >N50,000,000</b-button
              >
            </div>
            <b-dropdown
              size="sm"
              text="Annual"
              variant="success"
              class="mr-3 annual"
            >
              <b-dropdown-item-button>Action</b-dropdown-item-button>
              <b-dropdown-item-button>Another action</b-dropdown-item-button>
              <b-dropdown-item-button
                >Something else here...</b-dropdown-item-button
              >
            </b-dropdown>
          </div>
        </div>
        <div class="second-budget card-shadow ">
          <div class="budget-header d-flex justify-content-between">
            <div class=" d-flex align-items-center">
              <img src="@/assets/green-chart.svg" alt="" />
              <div class="status-heading">
                Total Annual OPEX Budget
              </div>
              <b-button class="ml-3 green p-1 px-3" size="sm"
                >N20,000,000</b-button
              >
            </div>
            <b-dropdown
              style="background:green;"
              size="sm"
              text="Annual"
              variant="success"
              class="mr-3 annual"
            >
              <b-dropdown-item-button>Action</b-dropdown-item-button>
              <b-dropdown-item-button>Another action</b-dropdown-item-button>
              <b-dropdown-item-button
                >Something else here...</b-dropdown-item-button
              >
            </b-dropdown>
          </div>
        </div>
      </div>
      <div class=" status">
        <div class="status-one card-shadow ">
          <div class="status-header">
            <img src="@/assets/yellow-chart.svg" alt="" />
            <div class="status-heading">Pending Budget Reassignment Status</div>
          </div>
          <div class="status-data">
            <div class="grey">200</div>
          </div>
        </div>
        <div class="status-two card-shadow">
          <div class="status-header">
            <img src="@/assets/green-chart.svg" alt="" />
            <div class="status-heading">
              Approved Budget Reassignment Status
            </div>
          </div>
          <div class="status-data">
            <div class="grey">373</div>
          </div>
        </div>
        <div class="status-three card-shadow">
          <div class="status-header">
            <img src="@/assets/red-chart.svg" alt="" />
            <div class="status-heading">
              Declined Budget Reassignment Status
            </div>
          </div>
          <div class="status-data">
            <div class="grey">372</div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'home'
};
</script>

<style scoped>
.home {
  font-family: 'Source Sans Pro', sans-serif;
}
.dashboard {
  font-family: 'Abril Fatface', cursive;
  color: #13244e;
  font-size: 1.375rem;
}
.date {
  font-size: 13px;
  font-size: 100;
}

.budget {
  flex: 6;
  margin-right: 20px;
  margin-left: 3px;
  height: 67vh;
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: repeat(4, 1fr);
  grid-row-gap: 20px;
}
.status {
  flex: 3.5;
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: repeat(6, 1fr);
  grid-row-gap: 0.75rem;
  height: 67vh;
}

.first-budget {
  grid-area: 1 / 1 / 3 / 2;
}
.second-budget {
  grid-area: 3 / 1 / 5 / 2;
}
.status-one {
  grid-area: 1 / 1 / 3 / 2;
}
.status-two {
  grid-area: 3 / 1 / 5 / 2;
}
.status-three {
  grid-area: 5 / 1 / 7 / 2;
}
.card-shadow {
  border-radius: 6px;
  box-shadow: 0 7px 64px 0 rgba(19, 36, 78, 0.07);
  background-color: #ffffff;
}
.head-count {
  margin-top: 8px;
}
.status-header {
  height: 31%;
  width: 100%;
  border-bottom: 1px solid #f0f3f7;
  display: flex;
  align-items: center;
  padding-left: 14px;
}
.status-heading {
  font-size: 0.875rem;
  color: #13244e;
  font-weight: 600;
  padding-left: 0.75rem;
}
.status-data {
  padding: 0.75rem 20px 25px;
  height: 69%;
}
.grey {
  border-radius: 8px;
  background-color: #f0f3f9;
  height: 100%;
  font-size: 2.1875rem;
  font-weight: bold;
  display: flex;
  justify-content: center;
  align-items: center;
}
.budget-header {
  height: 20%;
  width: 100%;
  border-bottom: 1px solid #f0f3f7;
  display: flex;
  align-items: center;
  padding-left: 14px;
}
.amount {
  border-radius: 6px;
  margin-left: 8px;
  padding: 4px 10px;
  font-weight: 600;
}
.purp {
  background-color: rgba(81, 44, 98, 0.2);
  font-weight: bold;
  font-size: 14px;
  border-radius: 6px;
  color: #512c62 !important;
  border: none;
}
.purp:hover,
.purp:focus,
.purp:active {
  background-color: rgba(81, 44, 98, 0.2) !important;
  font-weight: 600;
  border-radius: 6px;
  color: #512c62 !important;
  outline: none !important;
  box-shadow: none;
}
.green {
  background-color: rgba(31, 171, 137, 0.2);
  font-weight: bold;
  font-size: 14px;
  border-radius: 6px;
  color: #512c62 !important;
  border: none;
}
.green:hover,
.green:focus,
.green:active {
  background-color: rgba(31, 171, 137, 0.2) !important;
  font-weight: 600;
  border-radius: 6px;
  color: #512c62 !important;
  outline: none !important;
  box-shadow: none;
}
.annual,
.btn-success {
  color: #4dd599 !important;
  border-radius: 6px;
  background: rgba(77, 213, 153, 0.2) !important;
}
</style>
